# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a5
- machine: windows-x86
- commit hash: 076d169
- commit date: 2024-03-12
- overall geometric mean: 1.28x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.28x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf1_win32-x86-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 237 ms: 1.19x faster                                                |
| chameleon      | 8.08 ms                                                         | 5.53 ms: 1.46x faster                                               |
| docutils       | 2.10 sec                                                        | 1.70 sec: 1.24x faster                                              |
| html5lib       | 54.3 ms                                                         | 42.0 ms: 1.29x faster                                               |
| tornado_http   | 118 ms                                                          | 93.5 ms: 1.27x faster                                               |
| Geometric mean | (ref)                                                           | 1.29x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf1_win32-x86-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 241 ms: 1.42x faster                                                |
| async_tree_memoization     | 408 ms                                                          | 301 ms: 1.35x faster                                                |
| async_tree_io_tg           | 746 ms                                                          | 574 ms: 1.30x faster                                                |
| async_tree_memoization_tg  | 378 ms                                                          | 291 ms: 1.30x faster                                                |
| async_tree_none_tg         | 301 ms                                                          | 233 ms: 1.29x faster                                                |
| async_tree_io              | 754 ms                                                          | 591 ms: 1.27x faster                                                |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 484 ms: 1.22x faster                                                |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 477 ms: 1.21x faster                                                |
| Geometric mean             | (ref)                                                           | 1.30x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf1_win32-x86-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 74.7 ms: 1.69x faster                                               |
| float          | 76.1 ms                                                         | 53.8 ms: 1.41x faster                                               |
| pidigits       | 203 ms                                                          | 196 ms: 1.03x faster                                                |
| Geometric mean | (ref)                                                           | 1.35x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf1_win32-x86-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 94.7 ms: 1.56x faster                                               |
| regex_dna      | 122 ms                                                          | 119 ms: 1.02x faster                                                |
| regex_effbot   | 1.82 ms                                                         | 1.90 ms: 1.04x slower                                               |
| regex_v8       | 15.2 ms                                                         | 15.9 ms: 1.05x slower                                               |
| Geometric mean | (ref)                                                           | 1.10x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf1_win32-x86-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 139 us: 1.67x faster                                                |
| pickle_pure_python   | 309 us                                                          | 206 us: 1.50x faster                                                |
| json_dumps           | 9.80 ms                                                         | 6.67 ms: 1.47x faster                                               |
| tomli_loads          | 2.31 sec                                                        | 1.58 sec: 1.47x faster                                              |
| xml_etree_process    | 55.0 ms                                                         | 40.5 ms: 1.36x faster                                               |
| xml_etree_generate   | 71.6 ms                                                         | 57.9 ms: 1.24x faster                                               |
| unpickle_list        | 3.28 us                                                         | 2.82 us: 1.16x faster                                               |
| xml_etree_iterparse  | 75.6 ms                                                         | 65.4 ms: 1.15x faster                                               |
| xml_etree_parse      | 114 ms                                                          | 107 ms: 1.06x faster                                                |
| pickle               | 7.99 us                                                         | 7.74 us: 1.03x faster                                               |
| pickle_list          | 3.27 us                                                         | 3.22 us: 1.01x faster                                               |
| pickle_dict          | 20.1 us                                                         | 20.0 us: 1.00x faster                                               |
| unpickle             | 9.23 us                                                         | 9.87 us: 1.07x slower                                               |
| Geometric mean       | (ref)                                                           | 1.20x faster                                                        |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf1_win32-x86-python-v3.13.0a5-3.13.0a5-076d169 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                         | 22.8 ms: 1.04x slower                                               |
| python_startup_no_site | 18.8 ms                                                         | 20.6 ms: 1.10x slower                                               |
| Geometric mean         | (ref)                                                           | 1.07x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf1_win32-x86-python-v3.13.0a5-3.13.0a5-076d169 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 6.75 ms: 1.52x faster                                               |
| genshi_xml      | 61.2 ms                                                         | 41.0 ms: 1.49x faster                                               |
| genshi_text     | 26.8 ms                                                         | 18.3 ms: 1.46x faster                                               |
| django_template | 37.4 ms                                                         | 28.6 ms: 1.31x faster                                               |
| Geometric mean  | (ref)                                                           | 1.44x faster                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf1_win32-x86-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 90.2 us: 5.30x faster                                               |
| generators                 | 52.2 ms                                                         | 21.9 ms: 2.39x faster                                               |
| logging_silent             | 119 ns                                                          | 57.3 ns: 2.08x faster                                               |
| comprehensions             | 22.1 us                                                         | 11.0 us: 2.00x faster                                               |
| pylint                     | 418 ms                                                          | 217 ms: 1.93x faster                                                |
| deltablue                  | 4.10 ms                                                         | 2.13 ms: 1.92x faster                                               |
| spectral_norm              | 122 ms                                                          | 65.6 ms: 1.85x faster                                               |
| richards_super             | 58.7 ms                                                         | 31.8 ms: 1.85x faster                                               |
| hexiom                     | 7.51 ms                                                         | 4.16 ms: 1.81x faster                                               |
| deepcopy_memo              | 40.0 us                                                         | 22.4 us: 1.78x faster                                               |
| chaos                      | 84.4 ms                                                         | 47.5 ms: 1.78x faster                                               |
| sqlglot_parse              | 1.49 ms                                                         | 856 us: 1.74x faster                                                |
| scimark_lu                 | 102 ms                                                          | 58.7 ms: 1.74x faster                                               |
| richards                   | 48.8 ms                                                         | 28.2 ms: 1.73x faster                                               |
| raytrace                   | 327 ms                                                          | 192 ms: 1.71x faster                                                |
| scimark_sor                | 135 ms                                                          | 79.3 ms: 1.70x faster                                               |
| nbody                      | 126 ms                                                          | 74.7 ms: 1.69x faster                                               |
| coroutines                 | 23.7 ms                                                         | 14.1 ms: 1.68x faster                                               |
| unpickle_pure_python       | 231 us                                                          | 139 us: 1.67x faster                                                |
| nqueens                    | 111 ms                                                          | 67.6 ms: 1.65x faster                                               |
| sqlglot_transpile          | 1.78 ms                                                         | 1.08 ms: 1.65x faster                                               |
| scimark_monte_carlo        | 70.8 ms                                                         | 44.5 ms: 1.59x faster                                               |
| go                         | 147 ms                                                          | 94.3 ms: 1.56x faster                                               |
| regex_compile              | 148 ms                                                          | 94.7 ms: 1.56x faster                                               |
| pyflate                    | 471 ms                                                          | 309 ms: 1.53x faster                                                |
| mako                       | 10.3 ms                                                         | 6.75 ms: 1.52x faster                                               |
| crypto_pyaes               | 79.4 ms                                                         | 52.3 ms: 1.52x faster                                               |
| sympy_sum                  | 149 ms                                                          | 98.5 ms: 1.51x faster                                               |
| pickle_pure_python         | 309 us                                                          | 206 us: 1.50x faster                                                |
| genshi_xml                 | 61.2 ms                                                         | 41.0 ms: 1.49x faster                                               |
| fannkuch                   | 399 ms                                                          | 268 ms: 1.49x faster                                                |
| json_dumps                 | 9.80 ms                                                         | 6.67 ms: 1.47x faster                                               |
| tomli_loads                | 2.31 sec                                                        | 1.58 sec: 1.47x faster                                              |
| pprint_pformat             | 1.70 sec                                                        | 1.16 sec: 1.46x faster                                              |
| genshi_text                | 26.8 ms                                                         | 18.3 ms: 1.46x faster                                               |
| deepcopy                   | 381 us                                                          | 261 us: 1.46x faster                                                |
| chameleon                  | 8.08 ms                                                         | 5.53 ms: 1.46x faster                                               |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.91 ms: 1.46x faster                                               |
| sympy_str                  | 283 ms                                                          | 195 ms: 1.46x faster                                                |
| scimark_fft                | 291 ms                                                          | 201 ms: 1.45x faster                                                |
| pprint_safe_repr           | 819 ms                                                          | 565 ms: 1.45x faster                                                |
| logging_simple             | 10.8 us                                                         | 7.53 us: 1.44x faster                                               |
| deepcopy_reduce            | 3.32 us                                                         | 2.32 us: 1.43x faster                                               |
| async_tree_none            | 343 ms                                                          | 241 ms: 1.42x faster                                                |
| sympy_integrate            | 19.9 ms                                                         | 14.1 ms: 1.42x faster                                               |
| float                      | 76.1 ms                                                         | 53.8 ms: 1.41x faster                                               |
| logging_format             | 11.5 us                                                         | 8.10 us: 1.41x faster                                               |
| sqlglot_optimize           | 51.8 ms                                                         | 37.6 ms: 1.38x faster                                               |
| xml_etree_process          | 55.0 ms                                                         | 40.5 ms: 1.36x faster                                               |
| sympy_expand               | 462 ms                                                          | 341 ms: 1.36x faster                                                |
| async_tree_memoization     | 408 ms                                                          | 301 ms: 1.35x faster                                                |
| pycparser                  | 1.04 sec                                                        | 777 ms: 1.34x faster                                                |
| mdp                        | 2.07 sec                                                        | 1.58 sec: 1.31x faster                                              |
| django_template            | 37.4 ms                                                         | 28.6 ms: 1.31x faster                                               |
| async_tree_io_tg           | 746 ms                                                          | 574 ms: 1.30x faster                                                |
| async_tree_memoization_tg  | 378 ms                                                          | 291 ms: 1.30x faster                                                |
| html5lib                   | 54.3 ms                                                         | 42.0 ms: 1.29x faster                                               |
| async_tree_none_tg         | 301 ms                                                          | 233 ms: 1.29x faster                                                |
| async_tree_io              | 754 ms                                                          | 591 ms: 1.27x faster                                                |
| tornado_http               | 118 ms                                                          | 93.5 ms: 1.27x faster                                               |
| asyncio_tcp                | 787 ms                                                          | 622 ms: 1.27x faster                                                |
| xml_etree_generate         | 71.6 ms                                                         | 57.9 ms: 1.24x faster                                               |
| docutils                   | 2.10 sec                                                        | 1.70 sec: 1.24x faster                                              |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 484 ms: 1.22x faster                                                |
| meteor_contest             | 90.9 ms                                                         | 74.9 ms: 1.21x faster                                               |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 477 ms: 1.21x faster                                                |
| 2to3                       | 282 ms                                                          | 237 ms: 1.19x faster                                                |
| json                       | 4.78 ms                                                         | 4.10 ms: 1.17x faster                                               |
| unpickle_list              | 3.28 us                                                         | 2.82 us: 1.16x faster                                               |
| xml_etree_iterparse        | 75.6 ms                                                         | 65.4 ms: 1.15x faster                                               |
| bench_thread_pool          | 1.14 ms                                                         | 986 us: 1.15x faster                                                |
| sqlite_synth               | 2.15 us                                                         | 1.91 us: 1.13x faster                                               |
| xml_etree_parse            | 114 ms                                                          | 107 ms: 1.06x faster                                                |
| pidigits                   | 203 ms                                                          | 196 ms: 1.03x faster                                                |
| pickle                     | 7.99 us                                                         | 7.74 us: 1.03x faster                                               |
| regex_dna                  | 122 ms                                                          | 119 ms: 1.02x faster                                                |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.7 sec: 1.02x faster                                              |
| pickle_list                | 3.27 us                                                         | 3.22 us: 1.01x faster                                               |
| pickle_dict                | 20.1 us                                                         | 20.0 us: 1.00x faster                                               |
| gc_traversal               | 1.38 ms                                                         | 1.40 ms: 1.02x slower                                               |
| python_startup             | 22.0 ms                                                         | 22.8 ms: 1.04x slower                                               |
| regex_effbot               | 1.82 ms                                                         | 1.90 ms: 1.04x slower                                               |
| bench_mp_pool              | 70.9 ms                                                         | 74.1 ms: 1.04x slower                                               |
| regex_v8                   | 15.2 ms                                                         | 15.9 ms: 1.05x slower                                               |
| create_gc_cycles           | 618 us                                                          | 657 us: 1.06x slower                                                |
| unpickle                   | 9.23 us                                                         | 9.87 us: 1.07x slower                                               |
| python_startup_no_site     | 18.8 ms                                                         | 20.6 ms: 1.10x slower                                               |
| pathlib                    | 79.9 ms                                                         | 89.2 ms: 1.12x slower                                               |
| telco                      | 5.29 ms                                                         | 5.99 ms: 1.13x slower                                               |
| sqlglot_normalize          | 113 ms                                                          | 193 ms: 1.71x slower                                                |
| coverage                   | 58.0 ms                                                         | 497 ms: 8.56x slower                                                |
| thrift                     | 801 us                                                          | 10.1 ms: 12.61x slower                                              |
| Geometric mean             | (ref)                                                           | 1.28x faster                                                        |

Benchmark hidden because not significant (3): flaskblogging, async_generators, json_loads
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.30x
- 95% likely to have a speedup of 1.29x
- 99% likely to have a speedup of 1.28x

# Memory
- memory change: unknown