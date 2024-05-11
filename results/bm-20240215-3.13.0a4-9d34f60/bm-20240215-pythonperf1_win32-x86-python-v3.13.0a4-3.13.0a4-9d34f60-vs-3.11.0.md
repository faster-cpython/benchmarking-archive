# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a4
- machine: windows-x86
- commit hash: 9d34f60
- commit date: 2024-02-15
- overall geometric mean: 1.28x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf1_win32-x86-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 230 ms: 1.23x faster                                                |
| chameleon      | 8.08 ms                                                         | 5.61 ms: 1.44x faster                                               |
| docutils       | 2.10 sec                                                        | 1.71 sec: 1.22x faster                                              |
| html5lib       | 54.3 ms                                                         | 43.9 ms: 1.24x faster                                               |
| tornado_http   | 118 ms                                                          | 93.5 ms: 1.27x faster                                               |
| Geometric mean | (ref)                                                           | 1.28x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf1_win32-x86-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 239 ms: 1.44x faster                                                |
| async_tree_memoization     | 408 ms                                                          | 299 ms: 1.36x faster                                                |
| async_tree_none_tg         | 301 ms                                                          | 225 ms: 1.34x faster                                                |
| async_tree_memoization_tg  | 378 ms                                                          | 284 ms: 1.33x faster                                                |
| async_tree_io_tg           | 746 ms                                                          | 570 ms: 1.31x faster                                                |
| async_tree_io              | 754 ms                                                          | 584 ms: 1.29x faster                                                |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 496 ms: 1.19x faster                                                |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 489 ms: 1.18x faster                                                |
| Geometric mean             | (ref)                                                           | 1.30x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf1_win32-x86-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 76.8 ms: 1.64x faster                                               |
| float          | 76.1 ms                                                         | 52.8 ms: 1.44x faster                                               |
| pidigits       | 203 ms                                                          | 197 ms: 1.03x faster                                                |
| Geometric mean | (ref)                                                           | 1.35x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf1_win32-x86-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 93.4 ms: 1.58x faster                                               |
| regex_dna      | 122 ms                                                          | 116 ms: 1.05x faster                                                |
| regex_effbot   | 1.82 ms                                                         | 1.89 ms: 1.03x slower                                               |
| regex_v8       | 15.2 ms                                                         | 16.0 ms: 1.06x slower                                               |
| Geometric mean | (ref)                                                           | 1.11x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf1_win32-x86-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 140 us: 1.65x faster                                                |
| pickle_pure_python   | 309 us                                                          | 210 us: 1.47x faster                                                |
| json_dumps           | 9.80 ms                                                         | 6.71 ms: 1.46x faster                                               |
| tomli_loads          | 2.31 sec                                                        | 1.62 sec: 1.43x faster                                              |
| xml_etree_process    | 55.0 ms                                                         | 41.2 ms: 1.33x faster                                               |
| xml_etree_generate   | 71.6 ms                                                         | 60.0 ms: 1.19x faster                                               |
| xml_etree_iterparse  | 75.6 ms                                                         | 66.2 ms: 1.14x faster                                               |
| unpickle_list        | 3.28 us                                                         | 2.88 us: 1.14x faster                                               |
| xml_etree_parse      | 114 ms                                                          | 110 ms: 1.04x faster                                                |
| pickle_dict          | 20.1 us                                                         | 19.8 us: 1.01x faster                                               |
| pickle               | 7.99 us                                                         | 7.90 us: 1.01x faster                                               |
| pickle_list          | 3.27 us                                                         | 3.25 us: 1.00x faster                                               |
| json_loads           | 20.0 us                                                         | 20.2 us: 1.01x slower                                               |
| unpickle             | 9.23 us                                                         | 10.0 us: 1.08x slower                                               |
| Geometric mean       | (ref)                                                           | 1.18x faster                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf1_win32-x86-python-v3.13.0a4-3.13.0a4-9d34f60 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 19.7 ms: 1.05x slower                                               |
| Geometric mean         | (ref)                                                           | 1.02x slower                                                        |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf1_win32-x86-python-v3.13.0a4-3.13.0a4-9d34f60 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 6.76 ms: 1.52x faster                                               |
| genshi_xml      | 61.2 ms                                                         | 41.8 ms: 1.46x faster                                               |
| genshi_text     | 26.8 ms                                                         | 18.9 ms: 1.41x faster                                               |
| django_template | 37.4 ms                                                         | 30.4 ms: 1.23x faster                                               |
| Geometric mean  | (ref)                                                           | 1.40x faster                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf1_win32-x86-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 87.8 us: 5.45x faster                                               |
| generators                 | 52.2 ms                                                         | 22.7 ms: 2.30x faster                                               |
| logging_silent             | 119 ns                                                          | 56.9 ns: 2.09x faster                                               |
| pylint                     | 418 ms                                                          | 217 ms: 1.93x faster                                                |
| comprehensions             | 22.1 us                                                         | 11.5 us: 1.92x faster                                               |
| deltablue                  | 4.10 ms                                                         | 2.17 ms: 1.89x faster                                               |
| spectral_norm              | 122 ms                                                          | 65.4 ms: 1.86x faster                                               |
| chaos                      | 84.4 ms                                                         | 46.3 ms: 1.82x faster                                               |
| deepcopy_memo              | 40.0 us                                                         | 22.0 us: 1.82x faster                                               |
| hexiom                     | 7.51 ms                                                         | 4.20 ms: 1.79x faster                                               |
| richards_super             | 58.7 ms                                                         | 33.7 ms: 1.74x faster                                               |
| scimark_lu                 | 102 ms                                                          | 59.0 ms: 1.73x faster                                               |
| richards                   | 48.8 ms                                                         | 28.4 ms: 1.72x faster                                               |
| raytrace                   | 327 ms                                                          | 191 ms: 1.72x faster                                                |
| sqlglot_parse              | 1.49 ms                                                         | 868 us: 1.72x faster                                                |
| coroutines                 | 23.7 ms                                                         | 14.1 ms: 1.68x faster                                               |
| scimark_sor                | 135 ms                                                          | 80.9 ms: 1.67x faster                                               |
| nqueens                    | 111 ms                                                          | 66.9 ms: 1.67x faster                                               |
| unpickle_pure_python       | 231 us                                                          | 140 us: 1.65x faster                                                |
| nbody                      | 126 ms                                                          | 76.8 ms: 1.64x faster                                               |
| sqlglot_transpile          | 1.78 ms                                                         | 1.10 ms: 1.62x faster                                               |
| regex_compile              | 148 ms                                                          | 93.4 ms: 1.58x faster                                               |
| scimark_monte_carlo        | 70.8 ms                                                         | 44.9 ms: 1.58x faster                                               |
| go                         | 147 ms                                                          | 95.1 ms: 1.55x faster                                               |
| pyflate                    | 471 ms                                                          | 307 ms: 1.53x faster                                                |
| mako                       | 10.3 ms                                                         | 6.76 ms: 1.52x faster                                               |
| crypto_pyaes               | 79.4 ms                                                         | 52.6 ms: 1.51x faster                                               |
| sympy_sum                  | 149 ms                                                          | 99.4 ms: 1.50x faster                                               |
| fannkuch                   | 399 ms                                                          | 271 ms: 1.48x faster                                                |
| pickle_pure_python         | 309 us                                                          | 210 us: 1.47x faster                                                |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.88 ms: 1.47x faster                                               |
| scimark_fft                | 291 ms                                                          | 198 ms: 1.47x faster                                                |
| genshi_xml                 | 61.2 ms                                                         | 41.8 ms: 1.46x faster                                               |
| sympy_str                  | 283 ms                                                          | 194 ms: 1.46x faster                                                |
| json_dumps                 | 9.80 ms                                                         | 6.71 ms: 1.46x faster                                               |
| deepcopy                   | 381 us                                                          | 261 us: 1.46x faster                                                |
| pprint_pformat             | 1.70 sec                                                        | 1.16 sec: 1.46x faster                                              |
| logging_simple             | 10.8 us                                                         | 7.46 us: 1.45x faster                                               |
| pprint_safe_repr           | 819 ms                                                          | 568 ms: 1.44x faster                                                |
| float                      | 76.1 ms                                                         | 52.8 ms: 1.44x faster                                               |
| chameleon                  | 8.08 ms                                                         | 5.61 ms: 1.44x faster                                               |
| async_tree_none            | 343 ms                                                          | 239 ms: 1.44x faster                                                |
| tomli_loads                | 2.31 sec                                                        | 1.62 sec: 1.43x faster                                              |
| deepcopy_reduce            | 3.32 us                                                         | 2.32 us: 1.43x faster                                               |
| sympy_integrate            | 19.9 ms                                                         | 14.0 ms: 1.42x faster                                               |
| logging_format             | 11.5 us                                                         | 8.10 us: 1.41x faster                                               |
| genshi_text                | 26.8 ms                                                         | 18.9 ms: 1.41x faster                                               |
| async_tree_memoization     | 408 ms                                                          | 299 ms: 1.36x faster                                                |
| sympy_expand               | 462 ms                                                          | 341 ms: 1.36x faster                                                |
| sqlglot_optimize           | 51.8 ms                                                         | 38.6 ms: 1.34x faster                                               |
| async_tree_none_tg         | 301 ms                                                          | 225 ms: 1.34x faster                                                |
| xml_etree_process          | 55.0 ms                                                         | 41.2 ms: 1.33x faster                                               |
| pycparser                  | 1.04 sec                                                        | 784 ms: 1.33x faster                                                |
| async_tree_memoization_tg  | 378 ms                                                          | 284 ms: 1.33x faster                                                |
| mdp                        | 2.07 sec                                                        | 1.57 sec: 1.31x faster                                              |
| async_tree_io_tg           | 746 ms                                                          | 570 ms: 1.31x faster                                                |
| async_tree_io              | 754 ms                                                          | 584 ms: 1.29x faster                                                |
| asyncio_tcp                | 787 ms                                                          | 618 ms: 1.27x faster                                                |
| tornado_http               | 118 ms                                                          | 93.5 ms: 1.27x faster                                               |
| html5lib                   | 54.3 ms                                                         | 43.9 ms: 1.24x faster                                               |
| django_template            | 37.4 ms                                                         | 30.4 ms: 1.23x faster                                               |
| 2to3                       | 282 ms                                                          | 230 ms: 1.23x faster                                                |
| docutils                   | 2.10 sec                                                        | 1.71 sec: 1.22x faster                                              |
| xml_etree_generate         | 71.6 ms                                                         | 60.0 ms: 1.19x faster                                               |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 496 ms: 1.19x faster                                                |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 489 ms: 1.18x faster                                                |
| meteor_contest             | 90.9 ms                                                         | 77.4 ms: 1.17x faster                                               |
| sqlite_synth               | 2.15 us                                                         | 1.85 us: 1.16x faster                                               |
| bench_thread_pool          | 1.14 ms                                                         | 984 us: 1.16x faster                                                |
| json                       | 4.78 ms                                                         | 4.16 ms: 1.15x faster                                               |
| xml_etree_iterparse        | 75.6 ms                                                         | 66.2 ms: 1.14x faster                                               |
| unpickle_list              | 3.28 us                                                         | 2.88 us: 1.14x faster                                               |
| regex_dna                  | 122 ms                                                          | 116 ms: 1.05x faster                                                |
| xml_etree_parse            | 114 ms                                                          | 110 ms: 1.04x faster                                                |
| pidigits                   | 203 ms                                                          | 197 ms: 1.03x faster                                                |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.8 sec: 1.02x faster                                              |
| pickle_dict                | 20.1 us                                                         | 19.8 us: 1.01x faster                                               |
| pickle                     | 7.99 us                                                         | 7.90 us: 1.01x faster                                               |
| bench_mp_pool              | 70.9 ms                                                         | 70.4 ms: 1.01x faster                                               |
| pickle_list                | 3.27 us                                                         | 3.25 us: 1.00x faster                                               |
| async_generators           | 260 ms                                                          | 262 ms: 1.01x slower                                                |
| gc_traversal               | 1.38 ms                                                         | 1.39 ms: 1.01x slower                                               |
| json_loads                 | 20.0 us                                                         | 20.2 us: 1.01x slower                                               |
| regex_effbot               | 1.82 ms                                                         | 1.89 ms: 1.03x slower                                               |
| python_startup_no_site     | 18.8 ms                                                         | 19.7 ms: 1.05x slower                                               |
| regex_v8                   | 15.2 ms                                                         | 16.0 ms: 1.06x slower                                               |
| create_gc_cycles           | 618 us                                                          | 662 us: 1.07x slower                                                |
| unpickle                   | 9.23 us                                                         | 10.0 us: 1.08x slower                                               |
| telco                      | 5.29 ms                                                         | 5.76 ms: 1.09x slower                                               |
| pathlib                    | 79.9 ms                                                         | 88.6 ms: 1.11x slower                                               |
| sqlglot_normalize          | 113 ms                                                          | 201 ms: 1.78x slower                                                |
| coverage                   | 58.0 ms                                                         | 460 ms: 7.92x slower                                                |
| thrift                     | 801 us                                                          | 9.86 ms: 12.32x slower                                              |
| Geometric mean             | (ref)                                                           | 1.28x faster                                                        |

Benchmark hidden because not significant (2): python_startup, flaskblogging
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.31x
- 95% likely to have a speedup of 1.30x
- 99% likely to have a speedup of 1.27x

# Memory
- memory change: unknown