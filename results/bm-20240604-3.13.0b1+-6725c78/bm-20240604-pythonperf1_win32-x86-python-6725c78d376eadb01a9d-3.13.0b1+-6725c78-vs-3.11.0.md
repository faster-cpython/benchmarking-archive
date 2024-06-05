# Results vs. 3.11.0

- fork: python
- ref: 6725c78d376eadb01a9d
- machine: windows-x86
- commit hash: 6725c78
- commit date: 2024-06-04
- overall geometric mean: 1.25x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 233 ms: 1.21x faster                                                            |
| chameleon      | 8.08 ms                                                         | 5.85 ms: 1.38x faster                                                           |
| docutils       | 2.10 sec                                                        | 1.79 sec: 1.17x faster                                                          |
| html5lib       | 54.3 ms                                                         | 45.1 ms: 1.20x faster                                                           |
| tornado_http   | 118 ms                                                          | 94.2 ms: 1.26x faster                                                           |
| Geometric mean | (ref)                                                           | 1.24x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 230 ms: 1.49x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 203 ms: 1.48x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 256 ms: 1.47x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 278 ms: 1.47x faster                                                            |
| async_tree_io              | 754 ms                                                          | 532 ms: 1.42x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 529 ms: 1.41x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 445 ms: 1.30x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 466 ms: 1.27x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.41x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 73.9 ms: 1.70x faster                                                           |
| float          | 76.1 ms                                                         | 52.6 ms: 1.45x faster                                                           |
| pidigits       | 203 ms                                                          | 199 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                           | 1.36x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 100.0 ms: 1.48x faster                                                          |
| regex_v8       | 15.2 ms                                                         | 15.8 ms: 1.04x slower                                                           |
| regex_dna      | 122 ms                                                          | 127 ms: 1.04x slower                                                            |
| regex_effbot   | 1.82 ms                                                         | 1.97 ms: 1.08x slower                                                           |
| Geometric mean | (ref)                                                           | 1.06x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 146 us: 1.58x faster                                                            |
| tomli_loads          | 2.31 sec                                                        | 1.62 sec: 1.43x faster                                                          |
| json_dumps           | 9.80 ms                                                         | 6.94 ms: 1.41x faster                                                           |
| pickle_pure_python   | 309 us                                                          | 219 us: 1.41x faster                                                            |
| xml_etree_process    | 55.0 ms                                                         | 42.4 ms: 1.30x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 60.1 ms: 1.19x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 64.6 ms: 1.17x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 2.87 us: 1.14x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 103 ms: 1.10x faster                                                            |
| pickle               | 7.99 us                                                         | 8.01 us: 1.00x slower                                                           |
| pickle_dict          | 20.1 us                                                         | 20.4 us: 1.02x slower                                                           |
| json_loads           | 20.0 us                                                         | 21.1 us: 1.06x slower                                                           |
| unpickle             | 9.23 us                                                         | 10.2 us: 1.10x slower                                                           |
| pickle_list          | 3.27 us                                                         | 3.65 us: 1.12x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.16x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup | 22.0 ms                                                         | 23.0 ms: 1.04x slower                                                           |
| Geometric mean | (ref)                                                           | 1.02x slower                                                                    |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 6.97 ms: 1.47x faster                                                           |
| genshi_text     | 26.8 ms                                                         | 19.2 ms: 1.39x faster                                                           |
| genshi_xml      | 61.2 ms                                                         | 44.4 ms: 1.38x faster                                                           |
| django_template | 37.4 ms                                                         | 30.6 ms: 1.22x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.36x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 139 us: 3.45x faster                                                            |
| generators                 | 52.2 ms                                                         | 21.3 ms: 2.45x faster                                                           |
| logging_silent             | 119 ns                                                          | 58.2 ns: 2.05x faster                                                           |
| pylint                     | 418 ms                                                          | 218 ms: 1.92x faster                                                            |
| deltablue                  | 4.10 ms                                                         | 2.23 ms: 1.84x faster                                                           |
| spectral_norm              | 122 ms                                                          | 66.3 ms: 1.83x faster                                                           |
| comprehensions             | 22.1 us                                                         | 12.0 us: 1.83x faster                                                           |
| chaos                      | 84.4 ms                                                         | 47.9 ms: 1.76x faster                                                           |
| hexiom                     | 7.51 ms                                                         | 4.30 ms: 1.75x faster                                                           |
| raytrace                   | 327 ms                                                          | 190 ms: 1.73x faster                                                            |
| deepcopy_memo              | 40.0 us                                                         | 23.4 us: 1.71x faster                                                           |
| nbody                      | 126 ms                                                          | 73.9 ms: 1.70x faster                                                           |
| scimark_lu                 | 102 ms                                                          | 60.0 ms: 1.70x faster                                                           |
| richards_super             | 58.7 ms                                                         | 34.9 ms: 1.68x faster                                                           |
| scimark_sor                | 135 ms                                                          | 80.6 ms: 1.68x faster                                                           |
| nqueens                    | 111 ms                                                          | 69.3 ms: 1.61x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 934 us: 1.60x faster                                                            |
| unpickle_pure_python       | 231 us                                                          | 146 us: 1.58x faster                                                            |
| scimark_monte_carlo        | 70.8 ms                                                         | 45.0 ms: 1.57x faster                                                           |
| richards                   | 48.8 ms                                                         | 31.2 ms: 1.57x faster                                                           |
| coroutines                 | 23.7 ms                                                         | 15.4 ms: 1.54x faster                                                           |
| pyflate                    | 471 ms                                                          | 307 ms: 1.54x faster                                                            |
| sqlglot_transpile          | 1.78 ms                                                         | 1.17 ms: 1.53x faster                                                           |
| fannkuch                   | 399 ms                                                          | 266 ms: 1.50x faster                                                            |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.83 ms: 1.50x faster                                                           |
| async_tree_none            | 343 ms                                                          | 230 ms: 1.49x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 203 ms: 1.48x faster                                                            |
| regex_compile              | 148 ms                                                          | 100.0 ms: 1.48x faster                                                          |
| async_tree_memoization_tg  | 378 ms                                                          | 256 ms: 1.47x faster                                                            |
| mako                       | 10.3 ms                                                         | 6.97 ms: 1.47x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 278 ms: 1.47x faster                                                            |
| go                         | 147 ms                                                          | 102 ms: 1.45x faster                                                            |
| float                      | 76.1 ms                                                         | 52.6 ms: 1.45x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.62 sec: 1.43x faster                                                          |
| logging_simple             | 10.8 us                                                         | 7.61 us: 1.42x faster                                                           |
| async_tree_io              | 754 ms                                                          | 532 ms: 1.42x faster                                                            |
| sympy_sum                  | 149 ms                                                          | 105 ms: 1.42x faster                                                            |
| crypto_pyaes               | 79.4 ms                                                         | 56.1 ms: 1.41x faster                                                           |
| json_dumps                 | 9.80 ms                                                         | 6.94 ms: 1.41x faster                                                           |
| scimark_fft                | 291 ms                                                          | 207 ms: 1.41x faster                                                            |
| pickle_pure_python         | 309 us                                                          | 219 us: 1.41x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 529 ms: 1.41x faster                                                            |
| genshi_text                | 26.8 ms                                                         | 19.2 ms: 1.39x faster                                                           |
| logging_format             | 11.5 us                                                         | 8.23 us: 1.39x faster                                                           |
| chameleon                  | 8.08 ms                                                         | 5.85 ms: 1.38x faster                                                           |
| genshi_xml                 | 61.2 ms                                                         | 44.4 ms: 1.38x faster                                                           |
| pprint_pformat             | 1.70 sec                                                        | 1.25 sec: 1.36x faster                                                          |
| sympy_str                  | 283 ms                                                          | 209 ms: 1.35x faster                                                            |
| deepcopy                   | 381 us                                                          | 282 us: 1.35x faster                                                            |
| sympy_integrate            | 19.9 ms                                                         | 14.8 ms: 1.35x faster                                                           |
| pprint_safe_repr           | 819 ms                                                          | 611 ms: 1.34x faster                                                            |
| pycparser                  | 1.04 sec                                                        | 786 ms: 1.33x faster                                                            |
| xml_etree_process          | 55.0 ms                                                         | 42.4 ms: 1.30x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 445 ms: 1.30x faster                                                            |
| sqlglot_optimize           | 51.8 ms                                                         | 40.2 ms: 1.29x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 466 ms: 1.27x faster                                                            |
| deepcopy_reduce            | 3.32 us                                                         | 2.63 us: 1.26x faster                                                           |
| sympy_expand               | 462 ms                                                          | 367 ms: 1.26x faster                                                            |
| tornado_http               | 118 ms                                                          | 94.2 ms: 1.26x faster                                                           |
| mdp                        | 2.07 sec                                                        | 1.67 sec: 1.23x faster                                                          |
| django_template            | 37.4 ms                                                         | 30.6 ms: 1.22x faster                                                           |
| meteor_contest             | 90.9 ms                                                         | 74.7 ms: 1.22x faster                                                           |
| 2to3                       | 282 ms                                                          | 233 ms: 1.21x faster                                                            |
| html5lib                   | 54.3 ms                                                         | 45.1 ms: 1.20x faster                                                           |
| xml_etree_generate         | 71.6 ms                                                         | 60.1 ms: 1.19x faster                                                           |
| bench_thread_pool          | 1.14 ms                                                         | 969 us: 1.17x faster                                                            |
| docutils                   | 2.10 sec                                                        | 1.79 sec: 1.17x faster                                                          |
| xml_etree_iterparse        | 75.6 ms                                                         | 64.6 ms: 1.17x faster                                                           |
| asyncio_tcp                | 787 ms                                                          | 686 ms: 1.15x faster                                                            |
| unpickle_list              | 3.28 us                                                         | 2.87 us: 1.14x faster                                                           |
| xml_etree_parse            | 114 ms                                                          | 103 ms: 1.10x faster                                                            |
| json                       | 4.78 ms                                                         | 4.36 ms: 1.10x faster                                                           |
| sqlite_synth               | 2.15 us                                                         | 2.00 us: 1.08x faster                                                           |
| pidigits                   | 203 ms                                                          | 199 ms: 1.02x faster                                                            |
| bench_mp_pool              | 70.9 ms                                                         | 69.5 ms: 1.02x faster                                                           |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.8 sec: 1.01x faster                                                          |
| pickle                     | 7.99 us                                                         | 8.01 us: 1.00x slower                                                           |
| flaskblogging              | 2.03 sec                                                        | 2.04 sec: 1.00x slower                                                          |
| pickle_dict                | 20.1 us                                                         | 20.4 us: 1.02x slower                                                           |
| gc_traversal               | 1.38 ms                                                         | 1.42 ms: 1.03x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 15.8 ms: 1.04x slower                                                           |
| regex_dna                  | 122 ms                                                          | 127 ms: 1.04x slower                                                            |
| async_generators           | 260 ms                                                          | 271 ms: 1.04x slower                                                            |
| pathlib                    | 79.9 ms                                                         | 83.3 ms: 1.04x slower                                                           |
| python_startup             | 22.0 ms                                                         | 23.0 ms: 1.04x slower                                                           |
| json_loads                 | 20.0 us                                                         | 21.1 us: 1.06x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.97 ms: 1.08x slower                                                           |
| unpickle                   | 9.23 us                                                         | 10.2 us: 1.10x slower                                                           |
| pickle_list                | 3.27 us                                                         | 3.65 us: 1.12x slower                                                           |
| telco                      | 5.29 ms                                                         | 6.15 ms: 1.16x slower                                                           |
| create_gc_cycles           | 618 us                                                          | 745 us: 1.21x slower                                                            |
| sqlglot_normalize          | 113 ms                                                          | 207 ms: 1.83x slower                                                            |
| coverage                   | 58.0 ms                                                         | 304 ms: 5.24x slower                                                            |
| thrift                     | 801 us                                                          | 9.80 ms: 12.23x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.25x faster                                                                    |

Benchmark hidden because not significant (1): python_startup_no_site
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.29x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: unknown