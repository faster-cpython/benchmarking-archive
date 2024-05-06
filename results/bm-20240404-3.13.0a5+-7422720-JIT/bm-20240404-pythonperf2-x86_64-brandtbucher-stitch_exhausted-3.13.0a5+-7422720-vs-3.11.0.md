# Results vs. 3.11.0

- fork: brandtbucher
- ref: stitch_exhausted
- machine: linux-x86_64
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.05x faster
- HPT reliability: 84.51%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 302 ms: 1.05x slower                                                           |
| chameleon      | 7.92 ms                                                      | 7.46 ms: 1.06x faster                                                          |
| docutils       | 2.85 sec                                                     | 3.12 sec: 1.09x slower                                                         |
| html5lib       | 72.2 ms                                                      | 74.9 ms: 1.04x slower                                                          |
| tornado_http   | 124 ms                                                       | 123 ms: 1.01x faster                                                           |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_memoization     | 629 ms                                                       | 446 ms: 1.41x faster                                                           |
| async_tree_memoization_tg  | 600 ms                                                       | 426 ms: 1.41x faster                                                           |
| async_tree_none_tg         | 474 ms                                                       | 338 ms: 1.41x faster                                                           |
| async_tree_io              | 1.17 sec                                                     | 854 ms: 1.37x faster                                                           |
| async_tree_none            | 518 ms                                                       | 380 ms: 1.36x faster                                                           |
| async_tree_io_tg           | 1.15 sec                                                     | 866 ms: 1.33x faster                                                           |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 596 ms: 1.26x faster                                                           |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 613 ms: 1.23x faster                                                           |
| Geometric mean             | (ref)                                                        | 1.35x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| float          | 74.9 ms                                                      | 75.9 ms: 1.01x slower                                                          |
| pidigits       | 251 ms                                                       | 261 ms: 1.04x slower                                                           |
| nbody          | 92.9 ms                                                      | 97.1 ms: 1.04x slower                                                          |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 145 ms: 1.08x faster                                                           |
| regex_v8       | 24.4 ms                                                      | 25.4 ms: 1.04x slower                                                          |
| regex_dna      | 227 ms                                                       | 238 ms: 1.04x slower                                                           |
| regex_effbot   | 3.34 ms                                                      | 3.50 ms: 1.05x slower                                                          |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.6 ms: 1.26x faster                                                          |
| json_loads           | 28.9 us                                                      | 25.3 us: 1.14x faster                                                          |
| tomli_loads          | 2.25 sec                                                     | 2.13 sec: 1.06x faster                                                         |
| xml_etree_parse      | 155 ms                                                       | 147 ms: 1.05x faster                                                           |
| xml_etree_iterparse  | 107 ms                                                       | 102 ms: 1.05x faster                                                           |
| unpickle_pure_python | 238 us                                                       | 227 us: 1.05x faster                                                           |
| pickle_pure_python   | 316 us                                                       | 307 us: 1.03x faster                                                           |
| pickle_dict          | 32.3 us                                                      | 33.7 us: 1.04x slower                                                          |
| xml_etree_process    | 55.9 ms                                                      | 59.2 ms: 1.06x slower                                                          |
| xml_etree_generate   | 79.7 ms                                                      | 85.8 ms: 1.08x slower                                                          |
| pickle               | 9.89 us                                                      | 10.7 us: 1.09x slower                                                          |
| pickle_list          | 3.94 us                                                      | 4.43 us: 1.12x slower                                                          |
| unpickle             | 13.3 us                                                      | 15.2 us: 1.14x slower                                                          |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                                   |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                                          |
| python_startup_no_site | 7.73 ms                                                      | 11.8 ms: 1.53x slower                                                          |
| Geometric mean         | (ref)                                                        | 1.39x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako           | 11.0 ms                                                      | 9.98 ms: 1.10x faster                                                          |
| genshi_xml     | 57.1 ms                                                      | 59.5 ms: 1.04x slower                                                          |
| genshi_text    | 25.5 ms                                                      | 27.2 ms: 1.07x slower                                                          |
| Geometric mean | (ref)                                                        | 1.00x slower                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 121 us: 4.40x faster                                                           |
| asyncio_tcp                | 747 ms                                                       | 372 ms: 2.01x faster                                                           |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.95x faster                                                         |
| generators                 | 54.6 ms                                                      | 33.0 ms: 1.65x faster                                                          |
| pylint                     | 514 ms                                                       | 341 ms: 1.51x faster                                                           |
| async_tree_memoization     | 629 ms                                                       | 446 ms: 1.41x faster                                                           |
| async_tree_memoization_tg  | 600 ms                                                       | 426 ms: 1.41x faster                                                           |
| async_tree_none_tg         | 474 ms                                                       | 338 ms: 1.41x faster                                                           |
| async_tree_io              | 1.17 sec                                                     | 854 ms: 1.37x faster                                                           |
| async_tree_none            | 518 ms                                                       | 380 ms: 1.36x faster                                                           |
| async_tree_io_tg           | 1.15 sec                                                     | 866 ms: 1.33x faster                                                           |
| comprehensions             | 25.1 us                                                      | 19.7 us: 1.27x faster                                                          |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 596 ms: 1.26x faster                                                           |
| json_dumps                 | 13.3 ms                                                      | 10.6 ms: 1.26x faster                                                          |
| coroutines                 | 27.8 ms                                                      | 22.2 ms: 1.25x faster                                                          |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 613 ms: 1.23x faster                                                           |
| richards_super             | 63.6 ms                                                      | 51.9 ms: 1.23x faster                                                          |
| json_loads                 | 28.9 us                                                      | 25.3 us: 1.14x faster                                                          |
| chaos                      | 74.9 ms                                                      | 66.1 ms: 1.13x faster                                                          |
| logging_simple             | 7.24 us                                                      | 6.43 us: 1.13x faster                                                          |
| raytrace                   | 309 ms                                                       | 275 ms: 1.12x faster                                                           |
| sympy_sum                  | 186 ms                                                       | 165 ms: 1.12x faster                                                           |
| mako                       | 11.0 ms                                                      | 9.98 ms: 1.10x faster                                                          |
| richards                   | 49.7 ms                                                      | 45.3 ms: 1.10x faster                                                          |
| fannkuch                   | 416 ms                                                       | 381 ms: 1.09x faster                                                           |
| logging_format             | 7.71 us                                                      | 7.12 us: 1.08x faster                                                          |
| sympy_str                  | 337 ms                                                       | 311 ms: 1.08x faster                                                           |
| regex_compile              | 156 ms                                                       | 145 ms: 1.08x faster                                                           |
| sqlglot_parse              | 1.51 ms                                                      | 1.41 ms: 1.08x faster                                                          |
| crypto_pyaes               | 83.3 ms                                                      | 77.6 ms: 1.07x faster                                                          |
| chameleon                  | 7.92 ms                                                      | 7.46 ms: 1.06x faster                                                          |
| sympy_expand               | 553 ms                                                       | 522 ms: 1.06x faster                                                           |
| tomli_loads                | 2.25 sec                                                     | 2.13 sec: 1.06x faster                                                         |
| sqlglot_transpile          | 1.91 ms                                                      | 1.81 ms: 1.05x faster                                                          |
| xml_etree_parse            | 155 ms                                                       | 147 ms: 1.05x faster                                                           |
| mdp                        | 2.77 sec                                                     | 2.63 sec: 1.05x faster                                                         |
| pycparser                  | 1.31 sec                                                     | 1.24 sec: 1.05x faster                                                         |
| bench_thread_pool          | 1.00 ms                                                      | 952 us: 1.05x faster                                                           |
| xml_etree_iterparse        | 107 ms                                                       | 102 ms: 1.05x faster                                                           |
| unpickle_pure_python       | 238 us                                                       | 227 us: 1.05x faster                                                           |
| deltablue                  | 3.97 ms                                                      | 3.78 ms: 1.05x faster                                                          |
| thrift                     | 931 us                                                       | 897 us: 1.04x faster                                                           |
| json                       | 5.58 ms                                                      | 5.41 ms: 1.03x faster                                                          |
| pickle_pure_python         | 316 us                                                       | 307 us: 1.03x faster                                                           |
| spectral_norm              | 95.1 ms                                                      | 92.8 ms: 1.02x faster                                                          |
| logging_silent             | 100 ns                                                       | 98.2 ns: 1.02x faster                                                          |
| nqueens                    | 103 ms                                                       | 101 ms: 1.01x faster                                                           |
| tornado_http               | 124 ms                                                       | 123 ms: 1.01x faster                                                           |
| deepcopy_memo              | 37.5 us                                                      | 37.0 us: 1.01x faster                                                          |
| sympy_integrate            | 25.8 ms                                                      | 25.7 ms: 1.00x faster                                                          |
| scimark_lu                 | 114 ms                                                       | 115 ms: 1.01x slower                                                           |
| dulwich_log                | 67.4 ms                                                      | 68.2 ms: 1.01x slower                                                          |
| float                      | 74.9 ms                                                      | 75.9 ms: 1.01x slower                                                          |
| deepcopy_reduce            | 3.40 us                                                      | 3.45 us: 1.02x slower                                                          |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.18 ms: 1.03x slower                                                          |
| scimark_monte_carlo        | 69.8 ms                                                      | 72.1 ms: 1.03x slower                                                          |
| pprint_pformat             | 1.67 sec                                                     | 1.72 sec: 1.03x slower                                                         |
| html5lib                   | 72.2 ms                                                      | 74.9 ms: 1.04x slower                                                          |
| sqlglot_normalize          | 122 ms                                                       | 126 ms: 1.04x slower                                                           |
| meteor_contest             | 131 ms                                                       | 136 ms: 1.04x slower                                                           |
| pidigits                   | 251 ms                                                       | 261 ms: 1.04x slower                                                           |
| regex_v8                   | 24.4 ms                                                      | 25.4 ms: 1.04x slower                                                          |
| pathlib                    | 18.9 ms                                                      | 19.7 ms: 1.04x slower                                                          |
| pickle_dict                | 32.3 us                                                      | 33.7 us: 1.04x slower                                                          |
| genshi_xml                 | 57.1 ms                                                      | 59.5 ms: 1.04x slower                                                          |
| regex_dna                  | 227 ms                                                       | 238 ms: 1.04x slower                                                           |
| nbody                      | 92.9 ms                                                      | 97.1 ms: 1.04x slower                                                          |
| hexiom                     | 6.98 ms                                                      | 7.30 ms: 1.05x slower                                                          |
| pprint_safe_repr           | 805 ms                                                       | 841 ms: 1.05x slower                                                           |
| regex_effbot               | 3.34 ms                                                      | 3.50 ms: 1.05x slower                                                          |
| 2to3                       | 287 ms                                                       | 302 ms: 1.05x slower                                                           |
| xml_etree_process          | 55.9 ms                                                      | 59.2 ms: 1.06x slower                                                          |
| sqlite_synth               | 2.52 us                                                      | 2.68 us: 1.06x slower                                                          |
| genshi_text                | 25.5 ms                                                      | 27.2 ms: 1.07x slower                                                          |
| xml_etree_generate         | 79.7 ms                                                      | 85.8 ms: 1.08x slower                                                          |
| pyflate                    | 449 ms                                                       | 486 ms: 1.08x slower                                                           |
| pickle                     | 9.89 us                                                      | 10.7 us: 1.09x slower                                                          |
| go                         | 158 ms                                                       | 172 ms: 1.09x slower                                                           |
| sqlglot_optimize           | 59.0 ms                                                      | 64.5 ms: 1.09x slower                                                          |
| docutils                   | 2.85 sec                                                     | 3.12 sec: 1.09x slower                                                         |
| mypy2                      | 762 ms                                                       | 849 ms: 1.11x slower                                                           |
| pickle_list                | 3.94 us                                                      | 4.43 us: 1.12x slower                                                          |
| gc_traversal               | 4.15 ms                                                      | 4.66 ms: 1.12x slower                                                          |
| unpickle                   | 13.3 us                                                      | 15.2 us: 1.14x slower                                                          |
| scimark_fft                | 281 ms                                                       | 322 ms: 1.15x slower                                                           |
| gunicorn                   | 966 us                                                       | 1.11 ms: 1.15x slower                                                          |
| aiohttp                    | 986 us                                                       | 1.14 ms: 1.16x slower                                                          |
| async_generators           | 322 ms                                                       | 379 ms: 1.18x slower                                                           |
| create_gc_cycles           | 1.58 ms                                                      | 1.87 ms: 1.19x slower                                                          |
| telco                      | 6.81 ms                                                      | 8.32 ms: 1.22x slower                                                          |
| python_startup             | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                                          |
| coverage                   | 66.1 ms                                                      | 86.4 ms: 1.31x slower                                                          |
| scimark_sor                | 110 ms                                                       | 150 ms: 1.37x slower                                                           |
| python_startup_no_site     | 7.73 ms                                                      | 11.8 ms: 1.53x slower                                                          |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                                   |

Benchmark hidden because not significant (5): dask, deepcopy, asyncio_websockets, unpickle_list, bench_mp_pool
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 84.51% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x