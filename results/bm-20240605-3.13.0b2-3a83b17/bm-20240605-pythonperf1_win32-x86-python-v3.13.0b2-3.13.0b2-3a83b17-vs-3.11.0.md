# Results vs. 3.11.0

- fork: python
- ref: v3.13.0b2
- machine: windows-x86
- commit hash: 3a83b17
- commit date: 2024-06-05
- overall geometric mean: 1.26x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 233 ms: 1.21x faster                                                |
| chameleon      | 8.08 ms                                                         | 5.71 ms: 1.41x faster                                               |
| docutils       | 2.10 sec                                                        | 1.81 sec: 1.16x faster                                              |
| html5lib       | 54.3 ms                                                         | 45.4 ms: 1.19x faster                                               |
| tornado_http   | 118 ms                                                          | 94.3 ms: 1.26x faster                                               |
| Geometric mean | (ref)                                                           | 1.24x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 228 ms: 1.51x faster                                                |
| async_tree_memoization_tg  | 378 ms                                                          | 254 ms: 1.49x faster                                                |
| async_tree_none_tg         | 301 ms                                                          | 203 ms: 1.48x faster                                                |
| async_tree_memoization     | 408 ms                                                          | 275 ms: 1.48x faster                                                |
| async_tree_io              | 754 ms                                                          | 530 ms: 1.42x faster                                                |
| async_tree_io_tg           | 746 ms                                                          | 529 ms: 1.41x faster                                                |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 447 ms: 1.29x faster                                                |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 471 ms: 1.25x faster                                                |
| Geometric mean             | (ref)                                                           | 1.41x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 76.9 ms: 1.64x faster                                               |
| float          | 76.1 ms                                                         | 52.4 ms: 1.45x faster                                               |
| pidigits       | 203 ms                                                          | 199 ms: 1.02x faster                                                |
| Geometric mean | (ref)                                                           | 1.34x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 99.9 ms: 1.48x faster                                               |
| regex_dna      | 122 ms                                                          | 118 ms: 1.03x faster                                                |
| regex_effbot   | 1.82 ms                                                         | 1.88 ms: 1.03x slower                                               |
| regex_v8       | 15.2 ms                                                         | 15.7 ms: 1.04x slower                                               |
| Geometric mean | (ref)                                                           | 1.09x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 147 us: 1.57x faster                                                |
| pickle_pure_python   | 309 us                                                          | 213 us: 1.45x faster                                                |
| json_dumps           | 9.80 ms                                                         | 6.84 ms: 1.43x faster                                               |
| tomli_loads          | 2.31 sec                                                        | 1.65 sec: 1.41x faster                                              |
| xml_etree_process    | 55.0 ms                                                         | 42.1 ms: 1.31x faster                                               |
| xml_etree_generate   | 71.6 ms                                                         | 59.6 ms: 1.20x faster                                               |
| xml_etree_iterparse  | 75.6 ms                                                         | 64.2 ms: 1.18x faster                                               |
| unpickle_list        | 3.28 us                                                         | 2.93 us: 1.12x faster                                               |
| xml_etree_parse      | 114 ms                                                          | 104 ms: 1.09x faster                                                |
| pickle               | 7.99 us                                                         | 8.07 us: 1.01x slower                                               |
| json_loads           | 20.0 us                                                         | 20.5 us: 1.02x slower                                               |
| pickle_dict          | 20.1 us                                                         | 20.8 us: 1.03x slower                                               |
| unpickle             | 9.23 us                                                         | 9.79 us: 1.06x slower                                               |
| pickle_list          | 3.27 us                                                         | 3.57 us: 1.09x slower                                               |
| Geometric mean       | (ref)                                                           | 1.16x faster                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 18.2 ms: 1.03x faster                                               |
| python_startup         | 22.0 ms                                                         | 22.2 ms: 1.01x slower                                               |
| Geometric mean         | (ref)                                                           | 1.01x faster                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 6.94 ms: 1.48x faster                                               |
| genshi_xml      | 61.2 ms                                                         | 44.3 ms: 1.38x faster                                               |
| genshi_text     | 26.8 ms                                                         | 20.1 ms: 1.33x faster                                               |
| django_template | 37.4 ms                                                         | 30.1 ms: 1.24x faster                                               |
| Geometric mean  | (ref)                                                           | 1.36x faster                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1_win32-x86-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 136 us: 3.53x faster                                                |
| generators                 | 52.2 ms                                                         | 21.2 ms: 2.47x faster                                               |
| logging_silent             | 119 ns                                                          | 57.9 ns: 2.06x faster                                               |
| pylint                     | 418 ms                                                          | 217 ms: 1.93x faster                                                |
| comprehensions             | 22.1 us                                                         | 11.9 us: 1.86x faster                                               |
| deltablue                  | 4.10 ms                                                         | 2.23 ms: 1.83x faster                                               |
| spectral_norm              | 122 ms                                                          | 68.0 ms: 1.79x faster                                               |
| hexiom                     | 7.51 ms                                                         | 4.23 ms: 1.78x faster                                               |
| chaos                      | 84.4 ms                                                         | 48.0 ms: 1.76x faster                                               |
| raytrace                   | 327 ms                                                          | 189 ms: 1.74x faster                                                |
| scimark_lu                 | 102 ms                                                          | 59.4 ms: 1.72x faster                                               |
| deepcopy_memo              | 40.0 us                                                         | 23.5 us: 1.70x faster                                               |
| scimark_sor                | 135 ms                                                          | 81.0 ms: 1.67x faster                                               |
| richards_super             | 58.7 ms                                                         | 35.5 ms: 1.65x faster                                               |
| nbody                      | 126 ms                                                          | 76.9 ms: 1.64x faster                                               |
| nqueens                    | 111 ms                                                          | 68.7 ms: 1.62x faster                                               |
| unpickle_pure_python       | 231 us                                                          | 147 us: 1.57x faster                                                |
| scimark_monte_carlo        | 70.8 ms                                                         | 45.2 ms: 1.57x faster                                               |
| richards                   | 48.8 ms                                                         | 31.2 ms: 1.56x faster                                               |
| sqlglot_parse              | 1.49 ms                                                         | 964 us: 1.55x faster                                                |
| coroutines                 | 23.7 ms                                                         | 15.5 ms: 1.53x faster                                               |
| pyflate                    | 471 ms                                                          | 308 ms: 1.53x faster                                                |
| async_tree_none            | 343 ms                                                          | 228 ms: 1.51x faster                                                |
| sqlglot_transpile          | 1.78 ms                                                         | 1.19 ms: 1.50x faster                                               |
| async_tree_memoization_tg  | 378 ms                                                          | 254 ms: 1.49x faster                                                |
| async_tree_none_tg         | 301 ms                                                          | 203 ms: 1.48x faster                                                |
| async_tree_memoization     | 408 ms                                                          | 275 ms: 1.48x faster                                                |
| mako                       | 10.3 ms                                                         | 6.94 ms: 1.48x faster                                               |
| fannkuch                   | 399 ms                                                          | 270 ms: 1.48x faster                                                |
| regex_compile              | 148 ms                                                          | 99.9 ms: 1.48x faster                                               |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.87 ms: 1.47x faster                                               |
| scimark_fft                | 291 ms                                                          | 198 ms: 1.47x faster                                                |
| go                         | 147 ms                                                          | 101 ms: 1.46x faster                                                |
| float                      | 76.1 ms                                                         | 52.4 ms: 1.45x faster                                               |
| pickle_pure_python         | 309 us                                                          | 213 us: 1.45x faster                                                |
| logging_simple             | 10.8 us                                                         | 7.47 us: 1.45x faster                                               |
| json_dumps                 | 9.80 ms                                                         | 6.84 ms: 1.43x faster                                               |
| crypto_pyaes               | 79.4 ms                                                         | 55.8 ms: 1.42x faster                                               |
| async_tree_io              | 754 ms                                                          | 530 ms: 1.42x faster                                                |
| sympy_sum                  | 149 ms                                                          | 105 ms: 1.42x faster                                                |
| chameleon                  | 8.08 ms                                                         | 5.71 ms: 1.41x faster                                               |
| async_tree_io_tg           | 746 ms                                                          | 529 ms: 1.41x faster                                                |
| logging_format             | 11.5 us                                                         | 8.13 us: 1.41x faster                                               |
| tomli_loads                | 2.31 sec                                                        | 1.65 sec: 1.41x faster                                              |
| genshi_xml                 | 61.2 ms                                                         | 44.3 ms: 1.38x faster                                               |
| pprint_pformat             | 1.70 sec                                                        | 1.24 sec: 1.37x faster                                              |
| deepcopy                   | 381 us                                                          | 280 us: 1.36x faster                                                |
| sympy_integrate            | 19.9 ms                                                         | 14.6 ms: 1.36x faster                                               |
| pprint_safe_repr           | 819 ms                                                          | 607 ms: 1.35x faster                                                |
| pycparser                  | 1.04 sec                                                        | 777 ms: 1.34x faster                                                |
| sympy_str                  | 283 ms                                                          | 211 ms: 1.34x faster                                                |
| genshi_text                | 26.8 ms                                                         | 20.1 ms: 1.33x faster                                               |
| xml_etree_process          | 55.0 ms                                                         | 42.1 ms: 1.31x faster                                               |
| sqlglot_optimize           | 51.8 ms                                                         | 39.7 ms: 1.31x faster                                               |
| mdp                        | 2.07 sec                                                        | 1.60 sec: 1.29x faster                                              |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 447 ms: 1.29x faster                                                |
| deepcopy_reduce            | 3.32 us                                                         | 2.59 us: 1.28x faster                                               |
| tornado_http               | 118 ms                                                          | 94.3 ms: 1.26x faster                                               |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 471 ms: 1.25x faster                                                |
| django_template            | 37.4 ms                                                         | 30.1 ms: 1.24x faster                                               |
| sympy_expand               | 462 ms                                                          | 375 ms: 1.23x faster                                                |
| meteor_contest             | 90.9 ms                                                         | 74.1 ms: 1.23x faster                                               |
| 2to3                       | 282 ms                                                          | 233 ms: 1.21x faster                                                |
| xml_etree_generate         | 71.6 ms                                                         | 59.6 ms: 1.20x faster                                               |
| html5lib                   | 54.3 ms                                                         | 45.4 ms: 1.19x faster                                               |
| asyncio_tcp                | 787 ms                                                          | 662 ms: 1.19x faster                                                |
| xml_etree_iterparse        | 75.6 ms                                                         | 64.2 ms: 1.18x faster                                               |
| json                       | 4.78 ms                                                         | 4.10 ms: 1.17x faster                                               |
| docutils                   | 2.10 sec                                                        | 1.81 sec: 1.16x faster                                              |
| bench_thread_pool          | 1.14 ms                                                         | 985 us: 1.15x faster                                                |
| unpickle_list              | 3.28 us                                                         | 2.93 us: 1.12x faster                                               |
| sqlite_synth               | 2.15 us                                                         | 1.96 us: 1.10x faster                                               |
| xml_etree_parse            | 114 ms                                                          | 104 ms: 1.09x faster                                                |
| python_startup_no_site     | 18.8 ms                                                         | 18.2 ms: 1.03x faster                                               |
| regex_dna                  | 122 ms                                                          | 118 ms: 1.03x faster                                                |
| bench_mp_pool              | 70.9 ms                                                         | 69.4 ms: 1.02x faster                                               |
| pidigits                   | 203 ms                                                          | 199 ms: 1.02x faster                                                |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.9 sec: 1.01x faster                                              |
| pickle                     | 7.99 us                                                         | 8.07 us: 1.01x slower                                               |
| python_startup             | 22.0 ms                                                         | 22.2 ms: 1.01x slower                                               |
| async_generators           | 260 ms                                                          | 266 ms: 1.02x slower                                                |
| json_loads                 | 20.0 us                                                         | 20.5 us: 1.02x slower                                               |
| pickle_dict                | 20.1 us                                                         | 20.8 us: 1.03x slower                                               |
| regex_effbot               | 1.82 ms                                                         | 1.88 ms: 1.03x slower                                               |
| regex_v8                   | 15.2 ms                                                         | 15.7 ms: 1.04x slower                                               |
| gc_traversal               | 1.38 ms                                                         | 1.43 ms: 1.04x slower                                               |
| pathlib                    | 79.9 ms                                                         | 83.9 ms: 1.05x slower                                               |
| unpickle                   | 9.23 us                                                         | 9.79 us: 1.06x slower                                               |
| pickle_list                | 3.27 us                                                         | 3.57 us: 1.09x slower                                               |
| telco                      | 5.29 ms                                                         | 6.03 ms: 1.14x slower                                               |
| create_gc_cycles           | 618 us                                                          | 756 us: 1.22x slower                                                |
| sqlglot_normalize          | 113 ms                                                          | 206 ms: 1.82x slower                                                |
| coverage                   | 58.0 ms                                                         | 307 ms: 5.29x slower                                                |
| thrift                     | 801 us                                                          | 9.73 ms: 12.15x slower                                              |
| Geometric mean             | (ref)                                                           | 1.26x faster                                                        |

Benchmark hidden because not significant (1): flaskblogging
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.30x
- 95% likely to have a speedup of 1.29x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: unknown