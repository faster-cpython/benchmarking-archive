# Results vs. 3.11.0

- fork: python
- ref: edb6883ef3f7a8ef0c83
- machine: linux-x86_64
- commit hash: edb6883
- commit date: 2024-06-01
- overall geometric mean: 1.07x faster
- HPT reliability: 99.16%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-pythonperf2-x86_64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 293 ms: 1.02x slower                                                         |
| chameleon      | 7.92 ms                                                      | 7.46 ms: 1.06x faster                                                        |
| docutils       | 2.85 sec                                                     | 2.98 sec: 1.05x slower                                                       |
| html5lib       | 72.2 ms                                                      | 73.7 ms: 1.02x slower                                                        |
| tornado_http   | 124 ms                                                       | 119 ms: 1.04x faster                                                         |
| Geometric mean | (ref)                                                        | 1.00x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-pythonperf2-x86_64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 518 ms                                                       | 368 ms: 1.41x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 428 ms: 1.40x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 345 ms: 1.38x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 464 ms: 1.36x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 885 ms: 1.32x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 581 ms: 1.29x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 906 ms: 1.27x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 612 ms: 1.23x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-pythonperf2-x86_64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 87.0 ms: 1.07x faster                                                        |
| pidigits       | 251 ms                                                       | 253 ms: 1.01x slower                                                         |
| float          | 74.9 ms                                                      | 79.2 ms: 1.06x slower                                                        |
| Geometric mean | (ref)                                                        | 1.00x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-pythonperf2-x86_64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 144 ms: 1.09x faster                                                         |
| regex_v8       | 24.4 ms                                                      | 25.5 ms: 1.04x slower                                                        |
| regex_effbot   | 3.34 ms                                                      | 3.59 ms: 1.08x slower                                                        |
| regex_dna      | 227 ms                                                       | 251 ms: 1.10x slower                                                         |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-pythonperf2-x86_64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                        |
| json_loads           | 28.9 us                                                      | 24.8 us: 1.17x faster                                                        |
| xml_etree_parse      | 155 ms                                                       | 144 ms: 1.07x faster                                                         |
| unpickle_pure_python | 238 us                                                       | 224 us: 1.06x faster                                                         |
| xml_etree_iterparse  | 107 ms                                                       | 102 ms: 1.04x faster                                                         |
| pickle_dict          | 32.3 us                                                      | 31.1 us: 1.04x faster                                                        |
| pickle_pure_python   | 316 us                                                       | 310 us: 1.02x faster                                                         |
| unpickle_list        | 4.60 us                                                      | 4.79 us: 1.04x slower                                                        |
| pickle               | 9.89 us                                                      | 10.4 us: 1.05x slower                                                        |
| tomli_loads          | 2.25 sec                                                     | 2.40 sec: 1.06x slower                                                       |
| xml_etree_process    | 55.9 ms                                                      | 60.5 ms: 1.08x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 86.7 ms: 1.09x slower                                                        |
| pickle_list          | 3.94 us                                                      | 4.43 us: 1.12x slower                                                        |
| unpickle             | 13.3 us                                                      | 15.2 us: 1.14x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-pythonperf2-x86_64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 8.79 ms: 1.14x slower                                                        |
| python_startup         | 10.7 ms                                                      | 13.1 ms: 1.22x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.18x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-pythonperf2-x86_64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 11.0 ms                                                      | 10.7 ms: 1.03x faster                                                        |
| genshi_text    | 25.5 ms                                                      | 25.9 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                        | 1.00x faster                                                                 |

Benchmark hidden because not significant (2): genshi_xml, django_template

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240601-pythonperf2-x86_64-python-edb6883ef3f7a8ef0c83-3.13.0b1+-edb6883 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 174 us: 3.06x faster                                                         |
| asyncio_tcp                | 747 ms                                                       | 378 ms: 1.98x faster                                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                       |
| generators                 | 54.6 ms                                                      | 34.3 ms: 1.59x faster                                                        |
| pylint                     | 514 ms                                                       | 342 ms: 1.50x faster                                                         |
| comprehensions             | 25.1 us                                                      | 17.0 us: 1.47x faster                                                        |
| async_tree_none            | 518 ms                                                       | 368 ms: 1.41x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 428 ms: 1.40x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 345 ms: 1.38x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 464 ms: 1.36x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 885 ms: 1.32x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 581 ms: 1.29x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 906 ms: 1.27x faster                                                         |
| coroutines                 | 27.8 ms                                                      | 22.0 ms: 1.26x faster                                                        |
| json_dumps                 | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                        |
| chaos                      | 74.9 ms                                                      | 60.7 ms: 1.23x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 612 ms: 1.23x faster                                                         |
| sympy_sum                  | 186 ms                                                       | 155 ms: 1.20x faster                                                         |
| deltablue                  | 3.97 ms                                                      | 3.36 ms: 1.18x faster                                                        |
| scimark_lu                 | 114 ms                                                       | 97.4 ms: 1.17x faster                                                        |
| fannkuch                   | 416 ms                                                       | 355 ms: 1.17x faster                                                         |
| json_loads                 | 28.9 us                                                      | 24.8 us: 1.17x faster                                                        |
| raytrace                   | 309 ms                                                       | 265 ms: 1.17x faster                                                         |
| crypto_pyaes               | 83.3 ms                                                      | 72.7 ms: 1.15x faster                                                        |
| sympy_str                  | 337 ms                                                       | 297 ms: 1.14x faster                                                         |
| logging_simple             | 7.24 us                                                      | 6.39 us: 1.13x faster                                                        |
| nqueens                    | 103 ms                                                       | 91.1 ms: 1.13x faster                                                        |
| bench_thread_pool          | 1.00 ms                                                      | 903 us: 1.11x faster                                                         |
| logging_format             | 7.71 us                                                      | 6.97 us: 1.11x faster                                                        |
| mdp                        | 2.77 sec                                                     | 2.52 sec: 1.10x faster                                                       |
| sympy_integrate            | 25.8 ms                                                      | 23.5 ms: 1.10x faster                                                        |
| sympy_expand               | 553 ms                                                       | 506 ms: 1.09x faster                                                         |
| pathlib                    | 18.9 ms                                                      | 17.4 ms: 1.09x faster                                                        |
| regex_compile              | 156 ms                                                       | 144 ms: 1.09x faster                                                         |
| sqlglot_parse              | 1.51 ms                                                      | 1.41 ms: 1.08x faster                                                        |
| thrift                     | 931 us                                                       | 867 us: 1.07x faster                                                         |
| sqlglot_transpile          | 1.91 ms                                                      | 1.78 ms: 1.07x faster                                                        |
| xml_etree_parse            | 155 ms                                                       | 144 ms: 1.07x faster                                                         |
| nbody                      | 92.9 ms                                                      | 87.0 ms: 1.07x faster                                                        |
| json                       | 5.58 ms                                                      | 5.23 ms: 1.07x faster                                                        |
| hexiom                     | 6.98 ms                                                      | 6.55 ms: 1.07x faster                                                        |
| unpickle_pure_python       | 238 us                                                       | 224 us: 1.06x faster                                                         |
| chameleon                  | 7.92 ms                                                      | 7.46 ms: 1.06x faster                                                        |
| scimark_monte_carlo        | 69.8 ms                                                      | 66.2 ms: 1.06x faster                                                        |
| tornado_http               | 124 ms                                                       | 119 ms: 1.04x faster                                                         |
| xml_etree_iterparse        | 107 ms                                                       | 102 ms: 1.04x faster                                                         |
| dask                       | 410 ms                                                       | 393 ms: 1.04x faster                                                         |
| pickle_dict                | 32.3 us                                                      | 31.1 us: 1.04x faster                                                        |
| richards_super             | 63.6 ms                                                      | 61.5 ms: 1.03x faster                                                        |
| pycparser                  | 1.31 sec                                                     | 1.27 sec: 1.03x faster                                                       |
| mako                       | 11.0 ms                                                      | 10.7 ms: 1.03x faster                                                        |
| logging_silent             | 100 ns                                                       | 97.5 ns: 1.03x faster                                                        |
| deepcopy                   | 391 us                                                       | 380 us: 1.03x faster                                                         |
| pickle_pure_python         | 316 us                                                       | 310 us: 1.02x faster                                                         |
| meteor_contest             | 131 ms                                                       | 129 ms: 1.01x faster                                                         |
| deepcopy_memo              | 37.5 us                                                      | 37.3 us: 1.01x faster                                                        |
| sqlglot_optimize           | 59.0 ms                                                      | 59.4 ms: 1.01x slower                                                        |
| deepcopy_reduce            | 3.40 us                                                      | 3.42 us: 1.01x slower                                                        |
| pidigits                   | 251 ms                                                       | 253 ms: 1.01x slower                                                         |
| pprint_pformat             | 1.67 sec                                                     | 1.69 sec: 1.01x slower                                                       |
| go                         | 158 ms                                                       | 160 ms: 1.02x slower                                                         |
| genshi_text                | 25.5 ms                                                      | 25.9 ms: 1.02x slower                                                        |
| spectral_norm              | 95.1 ms                                                      | 96.8 ms: 1.02x slower                                                        |
| html5lib                   | 72.2 ms                                                      | 73.7 ms: 1.02x slower                                                        |
| 2to3                       | 287 ms                                                       | 293 ms: 1.02x slower                                                         |
| pprint_safe_repr           | 805 ms                                                       | 826 ms: 1.03x slower                                                         |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.19 ms: 1.03x slower                                                        |
| unpickle_list              | 4.60 us                                                      | 4.79 us: 1.04x slower                                                        |
| regex_v8                   | 24.4 ms                                                      | 25.5 ms: 1.04x slower                                                        |
| scimark_sor                | 110 ms                                                       | 114 ms: 1.04x slower                                                         |
| docutils                   | 2.85 sec                                                     | 2.98 sec: 1.05x slower                                                       |
| pickle                     | 9.89 us                                                      | 10.4 us: 1.05x slower                                                        |
| float                      | 74.9 ms                                                      | 79.2 ms: 1.06x slower                                                        |
| tomli_loads                | 2.25 sec                                                     | 2.40 sec: 1.06x slower                                                       |
| pyflate                    | 449 ms                                                       | 482 ms: 1.07x slower                                                         |
| regex_effbot               | 3.34 ms                                                      | 3.59 ms: 1.08x slower                                                        |
| gc_traversal               | 4.15 ms                                                      | 4.47 ms: 1.08x slower                                                        |
| aiohttp                    | 986 us                                                       | 1.07 ms: 1.08x slower                                                        |
| scimark_fft                | 281 ms                                                       | 304 ms: 1.08x slower                                                         |
| xml_etree_process          | 55.9 ms                                                      | 60.5 ms: 1.08x slower                                                        |
| gunicorn                   | 966 us                                                       | 1.05 ms: 1.09x slower                                                        |
| xml_etree_generate         | 79.7 ms                                                      | 86.7 ms: 1.09x slower                                                        |
| regex_dna                  | 227 ms                                                       | 251 ms: 1.10x slower                                                         |
| richards                   | 49.7 ms                                                      | 55.3 ms: 1.11x slower                                                        |
| sqlite_synth               | 2.52 us                                                      | 2.82 us: 1.12x slower                                                        |
| async_generators           | 322 ms                                                       | 359 ms: 1.12x slower                                                         |
| pickle_list                | 3.94 us                                                      | 4.43 us: 1.12x slower                                                        |
| python_startup_no_site     | 7.73 ms                                                      | 8.79 ms: 1.14x slower                                                        |
| unpickle                   | 13.3 us                                                      | 15.2 us: 1.14x slower                                                        |
| flaskblogging              | 3.88 ms                                                      | 4.70 ms: 1.21x slower                                                        |
| python_startup             | 10.7 ms                                                      | 13.1 ms: 1.22x slower                                                        |
| telco                      | 6.81 ms                                                      | 8.58 ms: 1.26x slower                                                        |
| create_gc_cycles           | 1.58 ms                                                      | 1.99 ms: 1.26x slower                                                        |
| coverage                   | 66.1 ms                                                      | 86.7 ms: 1.31x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.07x faster                                                                 |

Benchmark hidden because not significant (7): genshi_xml, asyncio_websockets, sqlglot_normalize, dulwich_log, django_template, mypy2, bench_mp_pool
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.16% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x