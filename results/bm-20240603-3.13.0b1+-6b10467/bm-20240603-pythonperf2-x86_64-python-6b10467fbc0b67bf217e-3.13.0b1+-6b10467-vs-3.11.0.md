# Results vs. 3.11.0

- fork: python
- ref: 6b10467fbc0b67bf217e
- machine: linux-x86_64
- commit hash: 6b10467
- commit date: 2024-06-03
- overall geometric mean: 1.07x faster
- HPT reliability: 99.15%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf2-x86_64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 292 ms: 1.02x slower                                                         |
| chameleon      | 7.92 ms                                                      | 7.49 ms: 1.06x faster                                                        |
| docutils       | 2.85 sec                                                     | 2.98 sec: 1.05x slower                                                       |
| html5lib       | 72.2 ms                                                      | 74.2 ms: 1.03x slower                                                        |
| tornado_http   | 124 ms                                                       | 118 ms: 1.05x faster                                                         |
| Geometric mean | (ref)                                                        | 1.00x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf2-x86_64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 518 ms                                                       | 368 ms: 1.41x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 428 ms: 1.40x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 342 ms: 1.39x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 467 ms: 1.35x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 897 ms: 1.31x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 577 ms: 1.30x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 909 ms: 1.27x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 612 ms: 1.23x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf2-x86_64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 89.0 ms: 1.04x faster                                                        |
| pidigits       | 251 ms                                                       | 253 ms: 1.01x slower                                                         |
| float          | 74.9 ms                                                      | 79.8 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf2-x86_64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 143 ms: 1.09x faster                                                         |
| regex_effbot   | 3.34 ms                                                      | 3.48 ms: 1.04x slower                                                        |
| regex_v8       | 24.4 ms                                                      | 26.1 ms: 1.07x slower                                                        |
| regex_dna      | 227 ms                                                       | 245 ms: 1.08x slower                                                         |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf2-x86_64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                        |
| json_loads           | 28.9 us                                                      | 24.6 us: 1.17x faster                                                        |
| unpickle_pure_python | 238 us                                                       | 210 us: 1.14x faster                                                         |
| pickle_dict          | 32.3 us                                                      | 30.1 us: 1.07x faster                                                        |
| xml_etree_parse      | 155 ms                                                       | 145 ms: 1.06x faster                                                         |
| xml_etree_iterparse  | 107 ms                                                       | 103 ms: 1.03x faster                                                         |
| pickle_pure_python   | 316 us                                                       | 314 us: 1.01x faster                                                         |
| pickle               | 9.89 us                                                      | 10.3 us: 1.04x slower                                                        |
| unpickle_list        | 4.60 us                                                      | 4.79 us: 1.04x slower                                                        |
| tomli_loads          | 2.25 sec                                                     | 2.39 sec: 1.06x slower                                                       |
| xml_etree_process    | 55.9 ms                                                      | 59.9 ms: 1.07x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 85.5 ms: 1.07x slower                                                        |
| pickle_list          | 3.94 us                                                      | 4.30 us: 1.09x slower                                                        |
| unpickle             | 13.3 us                                                      | 15.4 us: 1.16x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf2-x86_64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 8.82 ms: 1.14x slower                                                        |
| python_startup         | 10.7 ms                                                      | 13.2 ms: 1.23x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.18x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf2-x86_64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 11.0 ms                                                      | 10.3 ms: 1.06x faster                                                        |
| genshi_xml     | 57.1 ms                                                      | 55.2 ms: 1.03x faster                                                        |
| genshi_text    | 25.5 ms                                                      | 25.8 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                        | 1.02x faster                                                                 |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf2-x86_64-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 175 us: 3.05x faster                                                         |
| asyncio_tcp                | 747 ms                                                       | 378 ms: 1.98x faster                                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.95x faster                                                       |
| generators                 | 54.6 ms                                                      | 33.2 ms: 1.65x faster                                                        |
| pylint                     | 514 ms                                                       | 341 ms: 1.51x faster                                                         |
| comprehensions             | 25.1 us                                                      | 17.0 us: 1.47x faster                                                        |
| async_tree_none            | 518 ms                                                       | 368 ms: 1.41x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 428 ms: 1.40x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 342 ms: 1.39x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 467 ms: 1.35x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 897 ms: 1.31x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 577 ms: 1.30x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 909 ms: 1.27x faster                                                         |
| coroutines                 | 27.8 ms                                                      | 21.9 ms: 1.27x faster                                                        |
| json_dumps                 | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 612 ms: 1.23x faster                                                         |
| chaos                      | 74.9 ms                                                      | 61.4 ms: 1.22x faster                                                        |
| sympy_sum                  | 186 ms                                                       | 154 ms: 1.20x faster                                                         |
| deltablue                  | 3.97 ms                                                      | 3.33 ms: 1.19x faster                                                        |
| json_loads                 | 28.9 us                                                      | 24.6 us: 1.17x faster                                                        |
| scimark_lu                 | 114 ms                                                       | 98.4 ms: 1.16x faster                                                        |
| nqueens                    | 103 ms                                                       | 88.7 ms: 1.16x faster                                                        |
| sympy_str                  | 337 ms                                                       | 295 ms: 1.14x faster                                                         |
| unpickle_pure_python       | 238 us                                                       | 210 us: 1.14x faster                                                         |
| crypto_pyaes               | 83.3 ms                                                      | 73.5 ms: 1.13x faster                                                        |
| fannkuch                   | 416 ms                                                       | 368 ms: 1.13x faster                                                         |
| raytrace                   | 309 ms                                                       | 276 ms: 1.12x faster                                                         |
| mdp                        | 2.77 sec                                                     | 2.49 sec: 1.11x faster                                                       |
| bench_thread_pool          | 1.00 ms                                                      | 898 us: 1.11x faster                                                         |
| logging_simple             | 7.24 us                                                      | 6.52 us: 1.11x faster                                                        |
| hexiom                     | 6.98 ms                                                      | 6.31 ms: 1.11x faster                                                        |
| sympy_integrate            | 25.8 ms                                                      | 23.4 ms: 1.10x faster                                                        |
| pathlib                    | 18.9 ms                                                      | 17.2 ms: 1.10x faster                                                        |
| sympy_expand               | 553 ms                                                       | 504 ms: 1.10x faster                                                         |
| regex_compile              | 156 ms                                                       | 143 ms: 1.09x faster                                                         |
| logging_format             | 7.71 us                                                      | 7.09 us: 1.09x faster                                                        |
| pickle_dict                | 32.3 us                                                      | 30.1 us: 1.07x faster                                                        |
| xml_etree_parse            | 155 ms                                                       | 145 ms: 1.06x faster                                                         |
| richards_super             | 63.6 ms                                                      | 59.8 ms: 1.06x faster                                                        |
| mako                       | 11.0 ms                                                      | 10.3 ms: 1.06x faster                                                        |
| json                       | 5.58 ms                                                      | 5.26 ms: 1.06x faster                                                        |
| sqlglot_parse              | 1.51 ms                                                      | 1.43 ms: 1.06x faster                                                        |
| pycparser                  | 1.31 sec                                                     | 1.24 sec: 1.06x faster                                                       |
| chameleon                  | 7.92 ms                                                      | 7.49 ms: 1.06x faster                                                        |
| sqlglot_transpile          | 1.91 ms                                                      | 1.81 ms: 1.06x faster                                                        |
| tornado_http               | 124 ms                                                       | 118 ms: 1.05x faster                                                         |
| logging_silent             | 100 ns                                                       | 95.8 ns: 1.05x faster                                                        |
| nbody                      | 92.9 ms                                                      | 89.0 ms: 1.04x faster                                                        |
| dask                       | 410 ms                                                       | 393 ms: 1.04x faster                                                         |
| scimark_monte_carlo        | 69.8 ms                                                      | 67.1 ms: 1.04x faster                                                        |
| thrift                     | 931 us                                                       | 896 us: 1.04x faster                                                         |
| deepcopy                   | 391 us                                                       | 378 us: 1.04x faster                                                         |
| genshi_xml                 | 57.1 ms                                                      | 55.2 ms: 1.03x faster                                                        |
| xml_etree_iterparse        | 107 ms                                                       | 103 ms: 1.03x faster                                                         |
| meteor_contest             | 131 ms                                                       | 129 ms: 1.01x faster                                                         |
| asyncio_websockets         | 390 ms                                                       | 387 ms: 1.01x faster                                                         |
| pickle_pure_python         | 316 us                                                       | 314 us: 1.01x faster                                                         |
| sqlglot_normalize          | 122 ms                                                       | 122 ms: 1.00x slower                                                         |
| pprint_pformat             | 1.67 sec                                                     | 1.67 sec: 1.00x slower                                                       |
| deepcopy_reduce            | 3.40 us                                                      | 3.43 us: 1.01x slower                                                        |
| pidigits                   | 251 ms                                                       | 253 ms: 1.01x slower                                                         |
| genshi_text                | 25.5 ms                                                      | 25.8 ms: 1.01x slower                                                        |
| deepcopy_memo              | 37.5 us                                                      | 38.0 us: 1.01x slower                                                        |
| sqlglot_optimize           | 59.0 ms                                                      | 59.9 ms: 1.02x slower                                                        |
| 2to3                       | 287 ms                                                       | 292 ms: 1.02x slower                                                         |
| spectral_norm              | 95.1 ms                                                      | 96.9 ms: 1.02x slower                                                        |
| pprint_safe_repr           | 805 ms                                                       | 823 ms: 1.02x slower                                                         |
| html5lib                   | 72.2 ms                                                      | 74.2 ms: 1.03x slower                                                        |
| regex_effbot               | 3.34 ms                                                      | 3.48 ms: 1.04x slower                                                        |
| pickle                     | 9.89 us                                                      | 10.3 us: 1.04x slower                                                        |
| unpickle_list              | 4.60 us                                                      | 4.79 us: 1.04x slower                                                        |
| docutils                   | 2.85 sec                                                     | 2.98 sec: 1.05x slower                                                       |
| tomli_loads                | 2.25 sec                                                     | 2.39 sec: 1.06x slower                                                       |
| float                      | 74.9 ms                                                      | 79.8 ms: 1.07x slower                                                        |
| regex_v8                   | 24.4 ms                                                      | 26.1 ms: 1.07x slower                                                        |
| pyflate                    | 449 ms                                                       | 481 ms: 1.07x slower                                                         |
| xml_etree_process          | 55.9 ms                                                      | 59.9 ms: 1.07x slower                                                        |
| xml_etree_generate         | 79.7 ms                                                      | 85.5 ms: 1.07x slower                                                        |
| richards                   | 49.7 ms                                                      | 53.4 ms: 1.07x slower                                                        |
| scimark_sor                | 110 ms                                                       | 118 ms: 1.07x slower                                                         |
| gc_traversal               | 4.15 ms                                                      | 4.47 ms: 1.08x slower                                                        |
| regex_dna                  | 227 ms                                                       | 245 ms: 1.08x slower                                                         |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.42 ms: 1.09x slower                                                        |
| gunicorn                   | 966 us                                                       | 1.05 ms: 1.09x slower                                                        |
| pickle_list                | 3.94 us                                                      | 4.30 us: 1.09x slower                                                        |
| aiohttp                    | 986 us                                                       | 1.08 ms: 1.09x slower                                                        |
| scimark_fft                | 281 ms                                                       | 311 ms: 1.11x slower                                                         |
| sqlite_synth               | 2.52 us                                                      | 2.84 us: 1.12x slower                                                        |
| async_generators           | 322 ms                                                       | 363 ms: 1.13x slower                                                         |
| python_startup_no_site     | 7.73 ms                                                      | 8.82 ms: 1.14x slower                                                        |
| unpickle                   | 13.3 us                                                      | 15.4 us: 1.16x slower                                                        |
| flaskblogging              | 3.88 ms                                                      | 4.63 ms: 1.19x slower                                                        |
| python_startup             | 10.7 ms                                                      | 13.2 ms: 1.23x slower                                                        |
| telco                      | 6.81 ms                                                      | 8.61 ms: 1.27x slower                                                        |
| coverage                   | 66.1 ms                                                      | 83.9 ms: 1.27x slower                                                        |
| create_gc_cycles           | 1.58 ms                                                      | 2.06 ms: 1.31x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.07x faster                                                                 |

Benchmark hidden because not significant (5): dulwich_log, django_template, go, mypy2, bench_mp_pool
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.15% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x