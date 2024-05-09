# Results vs. 3.11.0

- fork: python
- ref: v3.13.0b1
- machine: linux-x86_64
- commit hash: 2268289
- commit date: 2024-05-08
- overall geometric mean: 1.03x faster
- HPT reliability: 93.61%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-pythonperf2-x86_64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 290 ms: 1.01x slower                                             |
| chameleon      | 7.92 ms                                                      | 7.66 ms: 1.03x faster                                            |
| docutils       | 2.85 sec                                                     | 3.03 sec: 1.06x slower                                           |
| html5lib       | 72.2 ms                                                      | 75.9 ms: 1.05x slower                                            |
| tornado_http   | 124 ms                                                       | 120 ms: 1.04x faster                                             |
| Geometric mean | (ref)                                                        | 1.01x slower                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-pythonperf2-x86_64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| async_tree_none            | 518 ms                                                       | 371 ms: 1.39x faster                                             |
| async_tree_none_tg         | 474 ms                                                       | 345 ms: 1.38x faster                                             |
| async_tree_memoization_tg  | 600 ms                                                       | 444 ms: 1.35x faster                                             |
| async_tree_memoization     | 629 ms                                                       | 467 ms: 1.35x faster                                             |
| async_tree_io              | 1.17 sec                                                     | 870 ms: 1.35x faster                                             |
| async_tree_io_tg           | 1.15 sec                                                     | 889 ms: 1.30x faster                                             |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 586 ms: 1.28x faster                                             |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 619 ms: 1.22x faster                                             |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-pythonperf2-x86_64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 90.1 ms: 1.03x faster                                            |
| pidigits       | 251 ms                                                       | 252 ms: 1.00x slower                                             |
| float          | 74.9 ms                                                      | 81.1 ms: 1.08x slower                                            |
| Geometric mean | (ref)                                                        | 1.02x slower                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-pythonperf2-x86_64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 147 ms: 1.06x faster                                             |
| regex_v8       | 24.4 ms                                                      | 25.6 ms: 1.05x slower                                            |
| regex_effbot   | 3.34 ms                                                      | 3.56 ms: 1.06x slower                                            |
| regex_dna      | 227 ms                                                       | 243 ms: 1.07x slower                                             |
| Geometric mean | (ref)                                                        | 1.03x slower                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-pythonperf2-x86_64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.9 ms: 1.22x faster                                            |
| json_loads           | 28.9 us                                                      | 24.4 us: 1.18x faster                                            |
| xml_etree_parse      | 155 ms                                                       | 144 ms: 1.07x faster                                             |
| unpickle_pure_python | 238 us                                                       | 222 us: 1.07x faster                                             |
| xml_etree_iterparse  | 107 ms                                                       | 103 ms: 1.04x faster                                             |
| pickle_dict          | 32.3 us                                                      | 31.2 us: 1.04x faster                                            |
| pickle_pure_python   | 316 us                                                       | 318 us: 1.01x slower                                             |
| unpickle_list        | 4.60 us                                                      | 4.75 us: 1.03x slower                                            |
| pickle               | 9.89 us                                                      | 10.4 us: 1.05x slower                                            |
| xml_etree_process    | 55.9 ms                                                      | 60.6 ms: 1.08x slower                                            |
| xml_etree_generate   | 79.7 ms                                                      | 88.9 ms: 1.11x slower                                            |
| pickle_list          | 3.94 us                                                      | 4.49 us: 1.14x slower                                            |
| tomli_loads          | 2.25 sec                                                     | 2.58 sec: 1.15x slower                                           |
| unpickle             | 13.3 us                                                      | 15.5 us: 1.17x slower                                            |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-pythonperf2-x86_64-python-v3.13.0b1-3.13.0b1-2268289 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 8.86 ms: 1.15x slower                                            |
| python_startup         | 10.7 ms                                                      | 12.9 ms: 1.21x slower                                            |
| Geometric mean         | (ref)                                                        | 1.18x slower                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-pythonperf2-x86_64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| mako           | 11.0 ms                                                      | 10.5 ms: 1.05x faster                                            |
| genshi_xml     | 57.1 ms                                                      | 57.8 ms: 1.01x slower                                            |
| genshi_text    | 25.5 ms                                                      | 26.2 ms: 1.03x slower                                            |
| Geometric mean | (ref)                                                        | 1.00x faster                                                     |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-pythonperf2-x86_64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 174 us: 3.05x faster                                             |
| asyncio_tcp                | 747 ms                                                       | 380 ms: 1.96x faster                                             |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.95x faster                                           |
| generators                 | 54.6 ms                                                      | 33.3 ms: 1.64x faster                                            |
| pylint                     | 514 ms                                                       | 346 ms: 1.48x faster                                             |
| comprehensions             | 25.1 us                                                      | 17.1 us: 1.46x faster                                            |
| async_tree_none            | 518 ms                                                       | 371 ms: 1.39x faster                                             |
| async_tree_none_tg         | 474 ms                                                       | 345 ms: 1.38x faster                                             |
| async_tree_memoization_tg  | 600 ms                                                       | 444 ms: 1.35x faster                                             |
| async_tree_memoization     | 629 ms                                                       | 467 ms: 1.35x faster                                             |
| async_tree_io              | 1.17 sec                                                     | 870 ms: 1.35x faster                                             |
| async_tree_io_tg           | 1.15 sec                                                     | 889 ms: 1.30x faster                                             |
| coroutines                 | 27.8 ms                                                      | 21.5 ms: 1.29x faster                                            |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 586 ms: 1.28x faster                                             |
| chaos                      | 74.9 ms                                                      | 59.4 ms: 1.26x faster                                            |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 619 ms: 1.22x faster                                             |
| json_dumps                 | 13.3 ms                                                      | 10.9 ms: 1.22x faster                                            |
| json_loads                 | 28.9 us                                                      | 24.4 us: 1.18x faster                                            |
| sympy_sum                  | 186 ms                                                       | 157 ms: 1.18x faster                                             |
| deltablue                  | 3.97 ms                                                      | 3.39 ms: 1.17x faster                                            |
| raytrace                   | 309 ms                                                       | 268 ms: 1.15x faster                                             |
| crypto_pyaes               | 83.3 ms                                                      | 72.9 ms: 1.14x faster                                            |
| fannkuch                   | 416 ms                                                       | 365 ms: 1.14x faster                                             |
| scimark_lu                 | 114 ms                                                       | 101 ms: 1.13x faster                                             |
| nqueens                    | 103 ms                                                       | 91.1 ms: 1.13x faster                                            |
| bench_thread_pool          | 1.00 ms                                                      | 895 us: 1.12x faster                                             |
| sympy_str                  | 337 ms                                                       | 302 ms: 1.12x faster                                             |
| logging_simple             | 7.24 us                                                      | 6.50 us: 1.11x faster                                            |
| mdp                        | 2.77 sec                                                     | 2.50 sec: 1.11x faster                                           |
| hexiom                     | 6.98 ms                                                      | 6.37 ms: 1.10x faster                                            |
| pathlib                    | 18.9 ms                                                      | 17.3 ms: 1.09x faster                                            |
| logging_format             | 7.71 us                                                      | 7.09 us: 1.09x faster                                            |
| sympy_integrate            | 25.8 ms                                                      | 23.8 ms: 1.09x faster                                            |
| sympy_expand               | 553 ms                                                       | 514 ms: 1.08x faster                                             |
| xml_etree_parse            | 155 ms                                                       | 144 ms: 1.07x faster                                             |
| unpickle_pure_python       | 238 us                                                       | 222 us: 1.07x faster                                             |
| regex_compile              | 156 ms                                                       | 147 ms: 1.06x faster                                             |
| sqlglot_parse              | 1.51 ms                                                      | 1.44 ms: 1.05x faster                                            |
| mako                       | 11.0 ms                                                      | 10.5 ms: 1.05x faster                                            |
| richards_super             | 63.6 ms                                                      | 61.0 ms: 1.04x faster                                            |
| sqlglot_transpile          | 1.91 ms                                                      | 1.83 ms: 1.04x faster                                            |
| json                       | 5.58 ms                                                      | 5.36 ms: 1.04x faster                                            |
| xml_etree_iterparse        | 107 ms                                                       | 103 ms: 1.04x faster                                             |
| logging_silent             | 100 ns                                                       | 96.6 ns: 1.04x faster                                            |
| pickle_dict                | 32.3 us                                                      | 31.2 us: 1.04x faster                                            |
| tornado_http               | 124 ms                                                       | 120 ms: 1.04x faster                                             |
| chameleon                  | 7.92 ms                                                      | 7.66 ms: 1.03x faster                                            |
| dask                       | 410 ms                                                       | 396 ms: 1.03x faster                                             |
| nbody                      | 92.9 ms                                                      | 90.1 ms: 1.03x faster                                            |
| pycparser                  | 1.31 sec                                                     | 1.27 sec: 1.03x faster                                           |
| thrift                     | 931 us                                                       | 908 us: 1.03x faster                                             |
| pidigits                   | 251 ms                                                       | 252 ms: 1.00x slower                                             |
| pickle_pure_python         | 316 us                                                       | 318 us: 1.01x slower                                             |
| deepcopy                   | 391 us                                                       | 395 us: 1.01x slower                                             |
| 2to3                       | 287 ms                                                       | 290 ms: 1.01x slower                                             |
| genshi_xml                 | 57.1 ms                                                      | 57.8 ms: 1.01x slower                                            |
| meteor_contest             | 131 ms                                                       | 132 ms: 1.01x slower                                             |
| pprint_pformat             | 1.67 sec                                                     | 1.69 sec: 1.01x slower                                           |
| go                         | 158 ms                                                       | 160 ms: 1.02x slower                                             |
| sqlglot_optimize           | 59.0 ms                                                      | 60.1 ms: 1.02x slower                                            |
| mypy2                      | 762 ms                                                       | 780 ms: 1.02x slower                                             |
| deepcopy_reduce            | 3.40 us                                                      | 3.48 us: 1.03x slower                                            |
| spectral_norm              | 95.1 ms                                                      | 97.5 ms: 1.03x slower                                            |
| genshi_text                | 25.5 ms                                                      | 26.2 ms: 1.03x slower                                            |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.19 ms: 1.03x slower                                            |
| pprint_safe_repr           | 805 ms                                                       | 830 ms: 1.03x slower                                             |
| unpickle_list              | 4.60 us                                                      | 4.75 us: 1.03x slower                                            |
| regex_v8                   | 24.4 ms                                                      | 25.6 ms: 1.05x slower                                            |
| deepcopy_memo              | 37.5 us                                                      | 39.4 us: 1.05x slower                                            |
| pickle                     | 9.89 us                                                      | 10.4 us: 1.05x slower                                            |
| html5lib                   | 72.2 ms                                                      | 75.9 ms: 1.05x slower                                            |
| docutils                   | 2.85 sec                                                     | 3.03 sec: 1.06x slower                                           |
| regex_effbot               | 3.34 ms                                                      | 3.56 ms: 1.06x slower                                            |
| regex_dna                  | 227 ms                                                       | 243 ms: 1.07x slower                                             |
| scimark_sor                | 110 ms                                                       | 117 ms: 1.07x slower                                             |
| pyflate                    | 449 ms                                                       | 480 ms: 1.07x slower                                             |
| gunicorn                   | 966 us                                                       | 1.04 ms: 1.08x slower                                            |
| float                      | 74.9 ms                                                      | 81.1 ms: 1.08x slower                                            |
| xml_etree_process          | 55.9 ms                                                      | 60.6 ms: 1.08x slower                                            |
| richards                   | 49.7 ms                                                      | 54.0 ms: 1.09x slower                                            |
| aiohttp                    | 986 us                                                       | 1.08 ms: 1.10x slower                                            |
| xml_etree_generate         | 79.7 ms                                                      | 88.9 ms: 1.11x slower                                            |
| sqlite_synth               | 2.52 us                                                      | 2.83 us: 1.12x slower                                            |
| gc_traversal               | 4.15 ms                                                      | 4.66 ms: 1.12x slower                                            |
| pickle_list                | 3.94 us                                                      | 4.49 us: 1.14x slower                                            |
| async_generators           | 322 ms                                                       | 367 ms: 1.14x slower                                             |
| tomli_loads                | 2.25 sec                                                     | 2.58 sec: 1.15x slower                                           |
| python_startup_no_site     | 7.73 ms                                                      | 8.86 ms: 1.15x slower                                            |
| unpickle                   | 13.3 us                                                      | 15.5 us: 1.17x slower                                            |
| scimark_fft                | 281 ms                                                       | 328 ms: 1.17x slower                                             |
| python_startup             | 10.7 ms                                                      | 12.9 ms: 1.21x slower                                            |
| flaskblogging              | 3.88 ms                                                      | 4.75 ms: 1.22x slower                                            |
| coverage                   | 66.1 ms                                                      | 83.7 ms: 1.27x slower                                            |
| create_gc_cycles           | 1.58 ms                                                      | 2.02 ms: 1.28x slower                                            |
| telco                      | 6.81 ms                                                      | 175 ms: 25.65x slower                                            |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                     |

Benchmark hidden because not significant (6): scimark_monte_carlo, sqlglot_normalize, dulwich_log, django_template, asyncio_websockets, bench_mp_pool
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 93.61% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x