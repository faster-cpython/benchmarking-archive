# Results vs. 3.11.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.06x faster
- HPT reliability: 93.83%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 298 ms: 1.04x slower                                                         |
| chameleon      | 7.92 ms                                                      | 7.57 ms: 1.05x faster                                                        |
| docutils       | 2.85 sec                                                     | 3.05 sec: 1.07x slower                                                       |
| html5lib       | 72.2 ms                                                      | 74.6 ms: 1.03x slower                                                        |
| tornado_http   | 124 ms                                                       | 122 ms: 1.02x faster                                                         |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 426 ms: 1.41x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 341 ms: 1.39x faster                                                         |
| async_tree_none            | 518 ms                                                       | 372 ms: 1.39x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 467 ms: 1.35x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 881 ms: 1.31x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 903 ms: 1.30x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 595 ms: 1.26x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 617 ms: 1.22x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 74.9 ms                                                      | 75.6 ms: 1.01x slower                                                        |
| pidigits       | 251 ms                                                       | 261 ms: 1.04x slower                                                         |
| nbody          | 92.9 ms                                                      | 98.2 ms: 1.06x slower                                                        |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 145 ms: 1.07x faster                                                         |
| regex_effbot   | 3.34 ms                                                      | 3.47 ms: 1.04x slower                                                        |
| regex_dna      | 227 ms                                                       | 241 ms: 1.06x slower                                                         |
| regex_v8       | 24.4 ms                                                      | 26.2 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.8 ms: 1.23x faster                                                        |
| json_loads           | 28.9 us                                                      | 24.8 us: 1.17x faster                                                        |
| unpickle_pure_python | 238 us                                                       | 219 us: 1.09x faster                                                         |
| xml_etree_parse      | 155 ms                                                       | 144 ms: 1.07x faster                                                         |
| xml_etree_iterparse  | 107 ms                                                       | 101 ms: 1.05x faster                                                         |
| tomli_loads          | 2.25 sec                                                     | 2.14 sec: 1.05x faster                                                       |
| pickle_pure_python   | 316 us                                                       | 311 us: 1.02x faster                                                         |
| pickle_dict          | 32.3 us                                                      | 32.5 us: 1.00x slower                                                        |
| xml_etree_process    | 55.9 ms                                                      | 57.6 ms: 1.03x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 83.7 ms: 1.05x slower                                                        |
| pickle               | 9.89 us                                                      | 10.8 us: 1.09x slower                                                        |
| pickle_list          | 3.94 us                                                      | 4.41 us: 1.12x slower                                                        |
| unpickle             | 13.3 us                                                      | 15.3 us: 1.15x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                                 |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 9.45 ms: 1.22x slower                                                        |
| python_startup         | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.24x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 11.0 ms                                                      | 9.93 ms: 1.11x faster                                                        |
| genshi_text    | 25.5 ms                                                      | 26.0 ms: 1.02x slower                                                        |
| genshi_xml     | 57.1 ms                                                      | 58.3 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                        | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 121 us: 4.40x faster                                                         |
| asyncio_tcp                | 747 ms                                                       | 374 ms: 2.00x faster                                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                       |
| generators                 | 54.6 ms                                                      | 33.5 ms: 1.63x faster                                                        |
| pylint                     | 514 ms                                                       | 362 ms: 1.42x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 426 ms: 1.41x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 341 ms: 1.39x faster                                                         |
| async_tree_none            | 518 ms                                                       | 372 ms: 1.39x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 467 ms: 1.35x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 881 ms: 1.31x faster                                                         |
| comprehensions             | 25.1 us                                                      | 19.2 us: 1.31x faster                                                        |
| async_tree_io              | 1.17 sec                                                     | 903 ms: 1.30x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 595 ms: 1.26x faster                                                         |
| coroutines                 | 27.8 ms                                                      | 22.1 ms: 1.25x faster                                                        |
| json_dumps                 | 13.3 ms                                                      | 10.8 ms: 1.23x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 617 ms: 1.22x faster                                                         |
| richards_super             | 63.6 ms                                                      | 52.2 ms: 1.22x faster                                                        |
| json_loads                 | 28.9 us                                                      | 24.8 us: 1.17x faster                                                        |
| logging_simple             | 7.24 us                                                      | 6.25 us: 1.16x faster                                                        |
| chaos                      | 74.9 ms                                                      | 65.6 ms: 1.14x faster                                                        |
| sympy_sum                  | 186 ms                                                       | 162 ms: 1.14x faster                                                         |
| raytrace                   | 309 ms                                                       | 271 ms: 1.14x faster                                                         |
| logging_format             | 7.71 us                                                      | 6.89 us: 1.12x faster                                                        |
| fannkuch                   | 416 ms                                                       | 374 ms: 1.11x faster                                                         |
| mako                       | 11.0 ms                                                      | 9.93 ms: 1.11x faster                                                        |
| sympy_str                  | 337 ms                                                       | 306 ms: 1.10x faster                                                         |
| unpickle_pure_python       | 238 us                                                       | 219 us: 1.09x faster                                                         |
| pathlib                    | 18.9 ms                                                      | 17.5 ms: 1.08x faster                                                        |
| sympy_expand               | 553 ms                                                       | 510 ms: 1.08x faster                                                         |
| bench_thread_pool          | 1.00 ms                                                      | 926 us: 1.08x faster                                                         |
| crypto_pyaes               | 83.3 ms                                                      | 77.3 ms: 1.08x faster                                                        |
| richards                   | 49.7 ms                                                      | 46.2 ms: 1.07x faster                                                        |
| regex_compile              | 156 ms                                                       | 145 ms: 1.07x faster                                                         |
| xml_etree_parse            | 155 ms                                                       | 144 ms: 1.07x faster                                                         |
| mdp                        | 2.77 sec                                                     | 2.59 sec: 1.07x faster                                                       |
| pycparser                  | 1.31 sec                                                     | 1.23 sec: 1.06x faster                                                       |
| logging_silent             | 100 ns                                                       | 94.7 ns: 1.06x faster                                                        |
| xml_etree_iterparse        | 107 ms                                                       | 101 ms: 1.05x faster                                                         |
| tomli_loads                | 2.25 sec                                                     | 2.14 sec: 1.05x faster                                                       |
| sqlglot_parse              | 1.51 ms                                                      | 1.44 ms: 1.05x faster                                                        |
| chameleon                  | 7.92 ms                                                      | 7.57 ms: 1.05x faster                                                        |
| json                       | 5.58 ms                                                      | 5.35 ms: 1.04x faster                                                        |
| thrift                     | 931 us                                                       | 893 us: 1.04x faster                                                         |
| sqlglot_transpile          | 1.91 ms                                                      | 1.84 ms: 1.04x faster                                                        |
| deltablue                  | 3.97 ms                                                      | 3.83 ms: 1.04x faster                                                        |
| sympy_integrate            | 25.8 ms                                                      | 25.0 ms: 1.03x faster                                                        |
| dask                       | 410 ms                                                       | 399 ms: 1.03x faster                                                         |
| spectral_norm              | 95.1 ms                                                      | 92.7 ms: 1.03x faster                                                        |
| deepcopy                   | 391 us                                                       | 382 us: 1.02x faster                                                         |
| nqueens                    | 103 ms                                                       | 100 ms: 1.02x faster                                                         |
| tornado_http               | 124 ms                                                       | 122 ms: 1.02x faster                                                         |
| pickle_pure_python         | 316 us                                                       | 311 us: 1.02x faster                                                         |
| dulwich_log                | 67.4 ms                                                      | 66.6 ms: 1.01x faster                                                        |
| deepcopy_memo              | 37.5 us                                                      | 37.3 us: 1.01x faster                                                        |
| pickle_dict                | 32.3 us                                                      | 32.5 us: 1.00x slower                                                        |
| meteor_contest             | 131 ms                                                       | 131 ms: 1.01x slower                                                         |
| float                      | 74.9 ms                                                      | 75.6 ms: 1.01x slower                                                        |
| sqlglot_normalize          | 122 ms                                                       | 123 ms: 1.01x slower                                                         |
| genshi_text                | 25.5 ms                                                      | 26.0 ms: 1.02x slower                                                        |
| genshi_xml                 | 57.1 ms                                                      | 58.3 ms: 1.02x slower                                                        |
| hexiom                     | 6.98 ms                                                      | 7.15 ms: 1.03x slower                                                        |
| pprint_pformat             | 1.67 sec                                                     | 1.71 sec: 1.03x slower                                                       |
| xml_etree_process          | 55.9 ms                                                      | 57.6 ms: 1.03x slower                                                        |
| pprint_safe_repr           | 805 ms                                                       | 831 ms: 1.03x slower                                                         |
| html5lib                   | 72.2 ms                                                      | 74.6 ms: 1.03x slower                                                        |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.20 ms: 1.03x slower                                                        |
| 2to3                       | 287 ms                                                       | 298 ms: 1.04x slower                                                         |
| regex_effbot               | 3.34 ms                                                      | 3.47 ms: 1.04x slower                                                        |
| pidigits                   | 251 ms                                                       | 261 ms: 1.04x slower                                                         |
| scimark_monte_carlo        | 69.8 ms                                                      | 72.6 ms: 1.04x slower                                                        |
| xml_etree_generate         | 79.7 ms                                                      | 83.7 ms: 1.05x slower                                                        |
| nbody                      | 92.9 ms                                                      | 98.2 ms: 1.06x slower                                                        |
| regex_dna                  | 227 ms                                                       | 241 ms: 1.06x slower                                                         |
| gc_traversal               | 4.15 ms                                                      | 4.40 ms: 1.06x slower                                                        |
| sqlglot_optimize           | 59.0 ms                                                      | 62.6 ms: 1.06x slower                                                        |
| sqlite_synth               | 2.52 us                                                      | 2.68 us: 1.06x slower                                                        |
| docutils                   | 2.85 sec                                                     | 3.05 sec: 1.07x slower                                                       |
| regex_v8                   | 24.4 ms                                                      | 26.2 ms: 1.07x slower                                                        |
| pyflate                    | 449 ms                                                       | 483 ms: 1.07x slower                                                         |
| mypy2                      | 762 ms                                                       | 820 ms: 1.08x slower                                                         |
| pickle                     | 9.89 us                                                      | 10.8 us: 1.09x slower                                                        |
| scimark_lu                 | 114 ms                                                       | 125 ms: 1.10x slower                                                         |
| pickle_list                | 3.94 us                                                      | 4.41 us: 1.12x slower                                                        |
| scimark_fft                | 281 ms                                                       | 316 ms: 1.12x slower                                                         |
| go                         | 158 ms                                                       | 178 ms: 1.13x slower                                                         |
| gunicorn                   | 966 us                                                       | 1.10 ms: 1.13x slower                                                        |
| aiohttp                    | 986 us                                                       | 1.13 ms: 1.14x slower                                                        |
| unpickle                   | 13.3 us                                                      | 15.3 us: 1.15x slower                                                        |
| telco                      | 6.81 ms                                                      | 8.06 ms: 1.18x slower                                                        |
| create_gc_cycles           | 1.58 ms                                                      | 1.88 ms: 1.19x slower                                                        |
| coverage                   | 66.1 ms                                                      | 79.5 ms: 1.20x slower                                                        |
| async_generators           | 322 ms                                                       | 388 ms: 1.21x slower                                                         |
| python_startup_no_site     | 7.73 ms                                                      | 9.45 ms: 1.22x slower                                                        |
| python_startup             | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                                        |
| scimark_sor                | 110 ms                                                       | 152 ms: 1.39x slower                                                         |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                                 |

Benchmark hidden because not significant (5): bench_mp_pool, asyncio_websockets, unpickle_list, deepcopy_reduce, django_template
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 93.83% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x