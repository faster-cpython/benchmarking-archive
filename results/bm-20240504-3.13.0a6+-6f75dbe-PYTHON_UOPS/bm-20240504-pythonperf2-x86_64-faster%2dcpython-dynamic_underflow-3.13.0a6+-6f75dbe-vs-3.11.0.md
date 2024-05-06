# Results vs. 3.11.0

- fork: faster-cpython
- ref: dynamic_underflow
- machine: linux-x86_64
- commit hash: 6f75dbe
- commit date: 2024-05-04
- overall geometric mean: 1.12x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-6f75dbe |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| chameleon      | 7.92 ms                                                      | 8.59 ms: 1.08x slower                                                               |
| tornado_http   | 124 ms                                                       | 141 ms: 1.14x slower                                                                |
| Geometric mean | (ref)                                                        | 1.11x slower                                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-6f75dbe |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| async_tree_none            | 518 ms                                                       | 391 ms: 1.32x faster                                                                |
| async_tree_none_tg         | 474 ms                                                       | 360 ms: 1.32x faster                                                                |
| async_tree_memoization_tg  | 600 ms                                                       | 458 ms: 1.31x faster                                                                |
| async_tree_memoization     | 629 ms                                                       | 496 ms: 1.27x faster                                                                |
| async_tree_io_tg           | 1.15 sec                                                     | 920 ms: 1.26x faster                                                                |
| async_tree_io              | 1.17 sec                                                     | 937 ms: 1.25x faster                                                                |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 629 ms: 1.19x faster                                                                |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 644 ms: 1.17x faster                                                                |
| Geometric mean             | (ref)                                                        | 1.26x faster                                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-6f75dbe |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 259 ms: 1.03x slower                                                                |
| float          | 74.9 ms                                                      | 98.7 ms: 1.32x slower                                                               |
| nbody          | 92.9 ms                                                      | 130 ms: 1.40x slower                                                                |
| Geometric mean | (ref)                                                        | 1.24x slower                                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-6f75dbe |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| regex_effbot   | 3.34 ms                                                      | 3.58 ms: 1.07x slower                                                               |
| regex_dna      | 227 ms                                                       | 246 ms: 1.08x slower                                                                |
| regex_v8       | 24.4 ms                                                      | 27.0 ms: 1.10x slower                                                               |
| regex_compile  | 156 ms                                                       | 231 ms: 1.48x slower                                                                |
| Geometric mean | (ref)                                                        | 1.17x slower                                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-6f75dbe |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 11.2 ms: 1.18x faster                                                               |
| json_loads           | 28.9 us                                                      | 24.5 us: 1.18x faster                                                               |
| xml_etree_parse      | 155 ms                                                       | 147 ms: 1.05x faster                                                                |
| pickle_dict          | 32.3 us                                                      | 32.9 us: 1.02x slower                                                               |
| unpickle_list        | 4.60 us                                                      | 4.72 us: 1.03x slower                                                               |
| pickle               | 9.89 us                                                      | 10.7 us: 1.08x slower                                                               |
| xml_etree_iterparse  | 107 ms                                                       | 116 ms: 1.08x slower                                                                |
| unpickle             | 13.3 us                                                      | 14.8 us: 1.11x slower                                                               |
| pickle_list          | 3.94 us                                                      | 4.44 us: 1.13x slower                                                               |
| xml_etree_process    | 55.9 ms                                                      | 68.1 ms: 1.22x slower                                                               |
| xml_etree_generate   | 79.7 ms                                                      | 99.2 ms: 1.24x slower                                                               |
| unpickle_pure_python | 238 us                                                       | 338 us: 1.42x slower                                                                |
| pickle_pure_python   | 316 us                                                       | 471 us: 1.49x slower                                                                |
| tomli_loads          | 2.25 sec                                                     | 3.36 sec: 1.49x slower                                                              |
| Geometric mean       | (ref)                                                        | 1.12x slower                                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-6f75dbe |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 8.95 ms: 1.16x slower                                                               |
| python_startup         | 10.7 ms                                                      | 13.0 ms: 1.21x slower                                                               |
| Geometric mean         | (ref)                                                        | 1.19x slower                                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-6f75dbe |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| django_template | 39.3 ms                                                      | 47.5 ms: 1.21x slower                                                               |
| mako            | 11.0 ms                                                      | 14.3 ms: 1.30x slower                                                               |
| Geometric mean  | (ref)                                                        | 1.25x slower                                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-6f75dbe |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 204 us: 2.61x faster                                                                |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.60 sec: 1.92x faster                                                              |
| asyncio_tcp                | 747 ms                                                       | 395 ms: 1.89x faster                                                                |
| generators                 | 54.6 ms                                                      | 35.6 ms: 1.54x faster                                                               |
| async_tree_none            | 518 ms                                                       | 391 ms: 1.32x faster                                                                |
| async_tree_none_tg         | 474 ms                                                       | 360 ms: 1.32x faster                                                                |
| async_tree_memoization_tg  | 600 ms                                                       | 458 ms: 1.31x faster                                                                |
| async_tree_memoization     | 629 ms                                                       | 496 ms: 1.27x faster                                                                |
| async_tree_io_tg           | 1.15 sec                                                     | 920 ms: 1.26x faster                                                                |
| async_tree_io              | 1.17 sec                                                     | 937 ms: 1.25x faster                                                                |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 629 ms: 1.19x faster                                                                |
| coroutines                 | 27.8 ms                                                      | 23.4 ms: 1.19x faster                                                               |
| json_dumps                 | 13.3 ms                                                      | 11.2 ms: 1.18x faster                                                               |
| json_loads                 | 28.9 us                                                      | 24.5 us: 1.18x faster                                                               |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 644 ms: 1.17x faster                                                                |
| pylint                     | 514 ms                                                       | 457 ms: 1.13x faster                                                                |
| xml_etree_parse            | 155 ms                                                       | 147 ms: 1.05x faster                                                                |
| pathlib                    | 18.9 ms                                                      | 18.5 ms: 1.02x faster                                                               |
| logging_simple             | 7.24 us                                                      | 7.09 us: 1.02x faster                                                               |
| thrift                     | 931 us                                                       | 914 us: 1.02x faster                                                                |
| mdp                        | 2.77 sec                                                     | 2.73 sec: 1.02x faster                                                              |
| json                       | 5.58 ms                                                      | 5.50 ms: 1.02x faster                                                               |
| asyncio_websockets         | 390 ms                                                       | 395 ms: 1.01x slower                                                                |
| pickle_dict                | 32.3 us                                                      | 32.9 us: 1.02x slower                                                               |
| unpickle_list              | 4.60 us                                                      | 4.72 us: 1.03x slower                                                               |
| pidigits                   | 251 ms                                                       | 259 ms: 1.03x slower                                                                |
| bench_mp_pool              | 4.70 ms                                                      | 4.90 ms: 1.04x slower                                                               |
| bench_thread_pool          | 1.00 ms                                                      | 1.05 ms: 1.05x slower                                                               |
| regex_effbot               | 3.34 ms                                                      | 3.58 ms: 1.07x slower                                                               |
| dask                       | 410 ms                                                       | 441 ms: 1.08x slower                                                                |
| pickle                     | 9.89 us                                                      | 10.7 us: 1.08x slower                                                               |
| regex_dna                  | 227 ms                                                       | 246 ms: 1.08x slower                                                                |
| xml_etree_iterparse        | 107 ms                                                       | 116 ms: 1.08x slower                                                                |
| chameleon                  | 7.92 ms                                                      | 8.59 ms: 1.08x slower                                                               |
| gc_traversal               | 4.15 ms                                                      | 4.52 ms: 1.09x slower                                                               |
| chaos                      | 74.9 ms                                                      | 81.9 ms: 1.09x slower                                                               |
| regex_v8                   | 24.4 ms                                                      | 27.0 ms: 1.10x slower                                                               |
| comprehensions             | 25.1 us                                                      | 27.7 us: 1.10x slower                                                               |
| unpickle                   | 13.3 us                                                      | 14.8 us: 1.11x slower                                                               |
| pickle_list                | 3.94 us                                                      | 4.44 us: 1.13x slower                                                               |
| tornado_http               | 124 ms                                                       | 141 ms: 1.14x slower                                                                |
| sympy_sum                  | 186 ms                                                       | 211 ms: 1.14x slower                                                                |
| crypto_pyaes               | 83.3 ms                                                      | 94.8 ms: 1.14x slower                                                               |
| meteor_contest             | 131 ms                                                       | 149 ms: 1.14x slower                                                                |
| python_startup_no_site     | 7.73 ms                                                      | 8.95 ms: 1.16x slower                                                               |
| sqlite_synth               | 2.52 us                                                      | 2.93 us: 1.16x slower                                                               |
| raytrace                   | 309 ms                                                       | 360 ms: 1.16x slower                                                                |
| sqlglot_parse              | 1.51 ms                                                      | 1.77 ms: 1.17x slower                                                               |
| coverage                   | 66.1 ms                                                      | 78.1 ms: 1.18x slower                                                               |
| pycparser                  | 1.31 sec                                                     | 1.55 sec: 1.18x slower                                                              |
| sqlglot_transpile          | 1.91 ms                                                      | 2.26 ms: 1.18x slower                                                               |
| sympy_integrate            | 25.8 ms                                                      | 30.6 ms: 1.19x slower                                                               |
| nqueens                    | 103 ms                                                       | 122 ms: 1.19x slower                                                                |
| fannkuch                   | 416 ms                                                       | 497 ms: 1.20x slower                                                                |
| django_template            | 39.3 ms                                                      | 47.5 ms: 1.21x slower                                                               |
| python_startup             | 10.7 ms                                                      | 13.0 ms: 1.21x slower                                                               |
| xml_etree_process          | 55.9 ms                                                      | 68.1 ms: 1.22x slower                                                               |
| deepcopy_reduce            | 3.40 us                                                      | 4.14 us: 1.22x slower                                                               |
| sympy_str                  | 337 ms                                                       | 417 ms: 1.24x slower                                                                |
| deepcopy                   | 391 us                                                       | 485 us: 1.24x slower                                                                |
| xml_etree_generate         | 79.7 ms                                                      | 99.2 ms: 1.24x slower                                                               |
| richards_super             | 63.6 ms                                                      | 79.8 ms: 1.25x slower                                                               |
| async_generators           | 322 ms                                                       | 403 ms: 1.25x slower                                                                |
| sympy_expand               | 553 ms                                                       | 698 ms: 1.26x slower                                                                |
| sqlglot_optimize           | 59.0 ms                                                      | 74.6 ms: 1.26x slower                                                               |
| sqlglot_normalize          | 122 ms                                                       | 155 ms: 1.27x slower                                                                |
| mako                       | 11.0 ms                                                      | 14.3 ms: 1.30x slower                                                               |
| gunicorn                   | 966 us                                                       | 1.26 ms: 1.31x slower                                                               |
| create_gc_cycles           | 1.58 ms                                                      | 2.06 ms: 1.31x slower                                                               |
| float                      | 74.9 ms                                                      | 98.7 ms: 1.32x slower                                                               |
| scimark_lu                 | 114 ms                                                       | 151 ms: 1.32x slower                                                                |
| mypy2                      | 762 ms                                                       | 1.01 sec: 1.33x slower                                                              |
| aiohttp                    | 986 us                                                       | 1.31 ms: 1.33x slower                                                               |
| flaskblogging              | 3.88 ms                                                      | 5.19 ms: 1.34x slower                                                               |
| telco                      | 6.81 ms                                                      | 9.15 ms: 1.34x slower                                                               |
| pprint_pformat             | 1.67 sec                                                     | 2.24 sec: 1.35x slower                                                              |
| dulwich_log                | 67.4 ms                                                      | 91.1 ms: 1.35x slower                                                               |
| pprint_safe_repr           | 805 ms                                                       | 1.10 sec: 1.36x slower                                                              |
| go                         | 158 ms                                                       | 217 ms: 1.38x slower                                                                |
| nbody                      | 92.9 ms                                                      | 130 ms: 1.40x slower                                                                |
| pyflate                    | 449 ms                                                       | 632 ms: 1.41x slower                                                                |
| unpickle_pure_python       | 238 us                                                       | 338 us: 1.42x slower                                                                |
| richards                   | 49.7 ms                                                      | 72.0 ms: 1.45x slower                                                               |
| regex_compile              | 156 ms                                                       | 231 ms: 1.48x slower                                                                |
| pickle_pure_python         | 316 us                                                       | 471 us: 1.49x slower                                                                |
| tomli_loads                | 2.25 sec                                                     | 3.36 sec: 1.49x slower                                                              |
| scimark_sor                | 110 ms                                                       | 165 ms: 1.51x slower                                                                |
| scimark_fft                | 281 ms                                                       | 428 ms: 1.53x slower                                                                |
| spectral_norm              | 95.1 ms                                                      | 147 ms: 1.54x slower                                                                |
| deltablue                  | 3.97 ms                                                      | 6.15 ms: 1.55x slower                                                               |
| hexiom                     | 6.98 ms                                                      | 10.9 ms: 1.56x slower                                                               |
| scimark_monte_carlo        | 69.8 ms                                                      | 109 ms: 1.57x slower                                                                |
| deepcopy_memo              | 37.5 us                                                      | 61.3 us: 1.63x slower                                                               |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 6.82 ms: 1.68x slower                                                               |
| logging_silent             | 100 ns                                                       | 185 ns: 1.84x slower                                                                |
| Geometric mean             | (ref)                                                        | 1.12x slower                                                                        |

Benchmark hidden because not significant (1): logging_format
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: 2to3, docutils, genshi_text, genshi_xml, html5lib, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.04x