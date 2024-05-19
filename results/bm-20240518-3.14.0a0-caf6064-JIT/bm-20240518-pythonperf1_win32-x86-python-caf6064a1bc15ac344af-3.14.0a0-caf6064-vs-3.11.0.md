# Results vs. 3.11.0

- fork: python
- ref: caf6064a1bc15ac344af
- machine: windows-x86
- commit hash: caf6064
- commit date: 2024-05-18
- overall geometric mean: 1.34x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 247 ms: 1.14x faster                                                           |
| chameleon      | 8.08 ms                                                         | 6.01 ms: 1.34x faster                                                          |
| docutils       | 2.10 sec                                                        | 1.88 sec: 1.12x faster                                                         |
| html5lib       | 54.3 ms                                                         | 45.1 ms: 1.20x faster                                                          |
| tornado_http   | 118 ms                                                          | 95.8 ms: 1.24x faster                                                          |
| Geometric mean | (ref)                                                           | 1.21x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 229 ms: 1.50x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 279 ms: 1.47x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 207 ms: 1.46x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 260 ms: 1.45x faster                                                           |
| async_tree_io              | 754 ms                                                          | 536 ms: 1.41x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 537 ms: 1.39x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 465 ms: 1.24x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 482 ms: 1.22x faster                                                           |
| Geometric mean             | (ref)                                                           | 1.39x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 53.3 ms: 2.36x faster                                                          |
| float          | 76.1 ms                                                         | 40.6 ms: 1.87x faster                                                          |
| pidigits       | 203 ms                                                          | 196 ms: 1.03x faster                                                           |
| Geometric mean | (ref)                                                           | 1.66x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 90.7 ms: 1.63x faster                                                          |
| regex_dna      | 122 ms                                                          | 121 ms: 1.01x faster                                                           |
| regex_v8       | 15.2 ms                                                         | 15.9 ms: 1.05x slower                                                          |
| regex_effbot   | 1.82 ms                                                         | 1.99 ms: 1.09x slower                                                          |
| Geometric mean | (ref)                                                           | 1.09x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 135 us: 1.71x faster                                                           |
| tomli_loads          | 2.31 sec                                                        | 1.42 sec: 1.63x faster                                                         |
| pickle_pure_python   | 309 us                                                          | 199 us: 1.55x faster                                                           |
| json_dumps           | 9.80 ms                                                         | 6.67 ms: 1.47x faster                                                          |
| xml_etree_process    | 55.0 ms                                                         | 39.9 ms: 1.38x faster                                                          |
| xml_etree_generate   | 71.6 ms                                                         | 54.9 ms: 1.30x faster                                                          |
| xml_etree_iterparse  | 75.6 ms                                                         | 60.4 ms: 1.25x faster                                                          |
| unpickle_list        | 3.28 us                                                         | 2.88 us: 1.14x faster                                                          |
| xml_etree_parse      | 114 ms                                                          | 103 ms: 1.11x faster                                                           |
| pickle               | 7.99 us                                                         | 8.16 us: 1.02x slower                                                          |
| pickle_dict          | 20.1 us                                                         | 20.9 us: 1.04x slower                                                          |
| json_loads           | 20.0 us                                                         | 21.1 us: 1.05x slower                                                          |
| pickle_list          | 3.27 us                                                         | 3.62 us: 1.11x slower                                                          |
| unpickle             | 9.23 us                                                         | 10.2 us: 1.11x slower                                                          |
| Geometric mean       | (ref)                                                           | 1.20x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 20.4 ms: 1.08x slower                                                          |
| python_startup         | 22.0 ms                                                         | 24.2 ms: 1.10x slower                                                          |
| Geometric mean         | (ref)                                                           | 1.09x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|-----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 5.30 ms: 1.94x faster                                                          |
| genshi_text     | 26.8 ms                                                         | 21.5 ms: 1.24x faster                                                          |
| django_template | 37.4 ms                                                         | 30.9 ms: 1.21x faster                                                          |
| genshi_xml      | 61.2 ms                                                         | 51.8 ms: 1.18x faster                                                          |
| Geometric mean  | (ref)                                                           | 1.36x faster                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 143 us: 3.36x faster                                                           |
| spectral_norm              | 122 ms                                                          | 47.5 ms: 2.56x faster                                                          |
| nbody                      | 126 ms                                                          | 53.3 ms: 2.36x faster                                                          |
| generators                 | 52.2 ms                                                         | 22.6 ms: 2.31x faster                                                          |
| logging_silent             | 119 ns                                                          | 53.9 ns: 2.21x faster                                                          |
| deepcopy_memo              | 40.0 us                                                         | 20.3 us: 1.97x faster                                                          |
| comprehensions             | 22.1 us                                                         | 11.2 us: 1.97x faster                                                          |
| mako                       | 10.3 ms                                                         | 5.30 ms: 1.94x faster                                                          |
| float                      | 76.1 ms                                                         | 40.6 ms: 1.87x faster                                                          |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.32 ms: 1.83x faster                                                          |
| fannkuch                   | 399 ms                                                          | 224 ms: 1.78x faster                                                           |
| scimark_fft                | 291 ms                                                          | 167 ms: 1.74x faster                                                           |
| pylint                     | 418 ms                                                          | 240 ms: 1.74x faster                                                           |
| unpickle_pure_python       | 231 us                                                          | 135 us: 1.71x faster                                                           |
| scimark_monte_carlo        | 70.8 ms                                                         | 41.5 ms: 1.71x faster                                                          |
| hexiom                     | 7.51 ms                                                         | 4.43 ms: 1.70x faster                                                          |
| richards_super             | 58.7 ms                                                         | 34.9 ms: 1.68x faster                                                          |
| sqlglot_parse              | 1.49 ms                                                         | 895 us: 1.67x faster                                                           |
| raytrace                   | 327 ms                                                          | 198 ms: 1.65x faster                                                           |
| deltablue                  | 4.10 ms                                                         | 2.51 ms: 1.63x faster                                                          |
| tomli_loads                | 2.31 sec                                                        | 1.42 sec: 1.63x faster                                                         |
| regex_compile              | 148 ms                                                          | 90.7 ms: 1.63x faster                                                          |
| nqueens                    | 111 ms                                                          | 68.8 ms: 1.62x faster                                                          |
| crypto_pyaes               | 79.4 ms                                                         | 49.2 ms: 1.61x faster                                                          |
| pyflate                    | 471 ms                                                          | 292 ms: 1.61x faster                                                           |
| richards                   | 48.8 ms                                                         | 30.3 ms: 1.61x faster                                                          |
| chaos                      | 84.4 ms                                                         | 52.8 ms: 1.60x faster                                                          |
| pickle_pure_python         | 309 us                                                          | 199 us: 1.55x faster                                                           |
| sqlglot_transpile          | 1.78 ms                                                         | 1.15 ms: 1.55x faster                                                          |
| scimark_sor                | 135 ms                                                          | 89.7 ms: 1.51x faster                                                          |
| async_tree_none            | 343 ms                                                          | 229 ms: 1.50x faster                                                           |
| json_dumps                 | 9.80 ms                                                         | 6.67 ms: 1.47x faster                                                          |
| coroutines                 | 23.7 ms                                                         | 16.2 ms: 1.47x faster                                                          |
| async_tree_memoization     | 408 ms                                                          | 279 ms: 1.47x faster                                                           |
| pprint_pformat             | 1.70 sec                                                        | 1.16 sec: 1.46x faster                                                         |
| async_tree_none_tg         | 301 ms                                                          | 207 ms: 1.46x faster                                                           |
| logging_simple             | 10.8 us                                                         | 7.43 us: 1.45x faster                                                          |
| async_tree_memoization_tg  | 378 ms                                                          | 260 ms: 1.45x faster                                                           |
| pprint_safe_repr           | 819 ms                                                          | 567 ms: 1.45x faster                                                           |
| logging_format             | 11.5 us                                                         | 7.98 us: 1.44x faster                                                          |
| async_tree_io              | 754 ms                                                          | 536 ms: 1.41x faster                                                           |
| sympy_sum                  | 149 ms                                                          | 106 ms: 1.40x faster                                                           |
| scimark_lu                 | 102 ms                                                          | 73.4 ms: 1.39x faster                                                          |
| async_tree_io_tg           | 746 ms                                                          | 537 ms: 1.39x faster                                                           |
| xml_etree_process          | 55.0 ms                                                         | 39.9 ms: 1.38x faster                                                          |
| go                         | 147 ms                                                          | 107 ms: 1.38x faster                                                           |
| sympy_str                  | 283 ms                                                          | 207 ms: 1.37x faster                                                           |
| chameleon                  | 8.08 ms                                                         | 6.01 ms: 1.34x faster                                                          |
| xml_etree_generate         | 71.6 ms                                                         | 54.9 ms: 1.30x faster                                                          |
| pycparser                  | 1.04 sec                                                        | 805 ms: 1.30x faster                                                           |
| sympy_integrate            | 19.9 ms                                                         | 15.4 ms: 1.29x faster                                                          |
| asyncio_tcp                | 787 ms                                                          | 611 ms: 1.29x faster                                                           |
| deepcopy                   | 381 us                                                          | 300 us: 1.27x faster                                                           |
| meteor_contest             | 90.9 ms                                                         | 71.9 ms: 1.26x faster                                                          |
| mdp                        | 2.07 sec                                                        | 1.64 sec: 1.26x faster                                                         |
| xml_etree_iterparse        | 75.6 ms                                                         | 60.4 ms: 1.25x faster                                                          |
| sympy_expand               | 462 ms                                                          | 370 ms: 1.25x faster                                                           |
| genshi_text                | 26.8 ms                                                         | 21.5 ms: 1.24x faster                                                          |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 465 ms: 1.24x faster                                                           |
| sqlglot_optimize           | 51.8 ms                                                         | 41.8 ms: 1.24x faster                                                          |
| tornado_http               | 118 ms                                                          | 95.8 ms: 1.24x faster                                                          |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 482 ms: 1.22x faster                                                           |
| deepcopy_reduce            | 3.32 us                                                         | 2.73 us: 1.21x faster                                                          |
| django_template            | 37.4 ms                                                         | 30.9 ms: 1.21x faster                                                          |
| html5lib                   | 54.3 ms                                                         | 45.1 ms: 1.20x faster                                                          |
| genshi_xml                 | 61.2 ms                                                         | 51.8 ms: 1.18x faster                                                          |
| coverage                   | 58.0 ms                                                         | 49.6 ms: 1.17x faster                                                          |
| bench_thread_pool          | 1.14 ms                                                         | 986 us: 1.15x faster                                                           |
| 2to3                       | 282 ms                                                          | 247 ms: 1.14x faster                                                           |
| thrift                     | 801 us                                                          | 703 us: 1.14x faster                                                           |
| sqlite_synth               | 2.15 us                                                         | 1.89 us: 1.14x faster                                                          |
| unpickle_list              | 3.28 us                                                         | 2.88 us: 1.14x faster                                                          |
| docutils                   | 2.10 sec                                                        | 1.88 sec: 1.12x faster                                                         |
| xml_etree_parse            | 114 ms                                                          | 103 ms: 1.11x faster                                                           |
| json                       | 4.78 ms                                                         | 4.39 ms: 1.09x faster                                                          |
| pidigits                   | 203 ms                                                          | 196 ms: 1.03x faster                                                           |
| regex_dna                  | 122 ms                                                          | 121 ms: 1.01x faster                                                           |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.9 sec: 1.01x faster                                                         |
| pickle                     | 7.99 us                                                         | 8.16 us: 1.02x slower                                                          |
| telco                      | 5.29 ms                                                         | 5.47 ms: 1.03x slower                                                          |
| pickle_dict                | 20.1 us                                                         | 20.9 us: 1.04x slower                                                          |
| gc_traversal               | 1.38 ms                                                         | 1.44 ms: 1.05x slower                                                          |
| regex_v8                   | 15.2 ms                                                         | 15.9 ms: 1.05x slower                                                          |
| bench_mp_pool              | 70.9 ms                                                         | 74.4 ms: 1.05x slower                                                          |
| json_loads                 | 20.0 us                                                         | 21.1 us: 1.05x slower                                                          |
| pathlib                    | 79.9 ms                                                         | 85.8 ms: 1.07x slower                                                          |
| python_startup_no_site     | 18.8 ms                                                         | 20.4 ms: 1.08x slower                                                          |
| regex_effbot               | 1.82 ms                                                         | 1.99 ms: 1.09x slower                                                          |
| python_startup             | 22.0 ms                                                         | 24.2 ms: 1.10x slower                                                          |
| pickle_list                | 3.27 us                                                         | 3.62 us: 1.11x slower                                                          |
| unpickle                   | 9.23 us                                                         | 10.2 us: 1.11x slower                                                          |
| async_generators           | 260 ms                                                          | 293 ms: 1.13x slower                                                           |
| create_gc_cycles           | 618 us                                                          | 754 us: 1.22x slower                                                           |
| sqlglot_normalize          | 113 ms                                                          | 218 ms: 1.92x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.34x faster                                                                   |

Benchmark hidden because not significant (1): flaskblogging
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.29x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.26x

# Memory
- memory change: unknown