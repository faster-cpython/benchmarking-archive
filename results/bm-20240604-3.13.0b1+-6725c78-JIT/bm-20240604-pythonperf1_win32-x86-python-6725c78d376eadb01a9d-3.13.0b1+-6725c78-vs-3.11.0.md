# Results vs. 3.11.0

- fork: python
- ref: 6725c78d376eadb01a9d
- machine: windows-x86
- commit hash: 6725c78
- commit date: 2024-06-04
- overall geometric mean: 1.27x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 245 ms: 1.15x faster                                                            |
| chameleon      | 8.08 ms                                                         | 6.12 ms: 1.32x faster                                                           |
| docutils       | 2.10 sec                                                        | 1.87 sec: 1.12x faster                                                          |
| html5lib       | 54.3 ms                                                         | 45.2 ms: 1.20x faster                                                           |
| tornado_http   | 118 ms                                                          | 96.7 ms: 1.22x faster                                                           |
| Geometric mean | (ref)                                                           | 1.20x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 225 ms: 1.52x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 273 ms: 1.50x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 203 ms: 1.48x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 257 ms: 1.47x faster                                                            |
| async_tree_io              | 754 ms                                                          | 527 ms: 1.43x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 528 ms: 1.41x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 454 ms: 1.27x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 472 ms: 1.25x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.41x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 54.6 ms: 2.31x faster                                                           |
| float          | 76.1 ms                                                         | 41.2 ms: 1.85x faster                                                           |
| pidigits       | 203 ms                                                          | 196 ms: 1.03x faster                                                            |
| Geometric mean | (ref)                                                           | 1.64x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 93.9 ms: 1.57x faster                                                           |
| regex_dna      | 122 ms                                                          | 123 ms: 1.01x slower                                                            |
| regex_v8       | 15.2 ms                                                         | 16.0 ms: 1.06x slower                                                           |
| regex_effbot   | 1.82 ms                                                         | 1.95 ms: 1.07x slower                                                           |
| Geometric mean | (ref)                                                           | 1.08x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 135 us: 1.72x faster                                                            |
| tomli_loads          | 2.31 sec                                                        | 1.39 sec: 1.66x faster                                                          |
| pickle_pure_python   | 309 us                                                          | 199 us: 1.55x faster                                                            |
| json_dumps           | 9.80 ms                                                         | 6.68 ms: 1.47x faster                                                           |
| xml_etree_process    | 55.0 ms                                                         | 40.4 ms: 1.36x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 55.6 ms: 1.29x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 61.1 ms: 1.24x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 103 ms: 1.11x faster                                                            |
| unpickle_list        | 3.28 us                                                         | 2.96 us: 1.11x faster                                                           |
| pickle               | 7.99 us                                                         | 8.05 us: 1.01x slower                                                           |
| json_loads           | 20.0 us                                                         | 20.6 us: 1.03x slower                                                           |
| pickle_dict          | 20.1 us                                                         | 20.7 us: 1.03x slower                                                           |
| pickle_list          | 3.27 us                                                         | 3.63 us: 1.11x slower                                                           |
| unpickle             | 9.23 us                                                         | 10.3 us: 1.12x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.20x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 20.1 ms: 1.07x slower                                                           |
| python_startup         | 22.0 ms                                                         | 24.4 ms: 1.11x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.09x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 5.35 ms: 1.92x faster                                                           |
| genshi_text     | 26.8 ms                                                         | 21.4 ms: 1.25x faster                                                           |
| django_template | 37.4 ms                                                         | 30.7 ms: 1.22x faster                                                           |
| genshi_xml      | 61.2 ms                                                         | 51.7 ms: 1.18x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.36x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 141 us: 3.40x faster                                                            |
| spectral_norm              | 122 ms                                                          | 48.4 ms: 2.51x faster                                                           |
| nbody                      | 126 ms                                                          | 54.6 ms: 2.31x faster                                                           |
| generators                 | 52.2 ms                                                         | 23.0 ms: 2.27x faster                                                           |
| logging_silent             | 119 ns                                                          | 55.6 ns: 2.14x faster                                                           |
| deepcopy_memo              | 40.0 us                                                         | 20.6 us: 1.94x faster                                                           |
| comprehensions             | 22.1 us                                                         | 11.4 us: 1.94x faster                                                           |
| mako                       | 10.3 ms                                                         | 5.35 ms: 1.92x faster                                                           |
| float                      | 76.1 ms                                                         | 41.2 ms: 1.85x faster                                                           |
| pylint                     | 418 ms                                                          | 236 ms: 1.77x faster                                                            |
| fannkuch                   | 399 ms                                                          | 229 ms: 1.74x faster                                                            |
| scimark_monte_carlo        | 70.8 ms                                                         | 40.7 ms: 1.74x faster                                                           |
| scimark_fft                | 291 ms                                                          | 168 ms: 1.74x faster                                                            |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.45 ms: 1.73x faster                                                           |
| unpickle_pure_python       | 231 us                                                          | 135 us: 1.72x faster                                                            |
| richards_super             | 58.7 ms                                                         | 34.9 ms: 1.68x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.39 sec: 1.66x faster                                                          |
| crypto_pyaes               | 79.4 ms                                                         | 48.3 ms: 1.64x faster                                                           |
| hexiom                     | 7.51 ms                                                         | 4.57 ms: 1.64x faster                                                           |
| nqueens                    | 111 ms                                                          | 68.4 ms: 1.63x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 916 us: 1.63x faster                                                            |
| deltablue                  | 4.10 ms                                                         | 2.55 ms: 1.61x faster                                                           |
| chaos                      | 84.4 ms                                                         | 52.9 ms: 1.60x faster                                                           |
| richards                   | 48.8 ms                                                         | 31.0 ms: 1.57x faster                                                           |
| regex_compile              | 148 ms                                                          | 93.9 ms: 1.57x faster                                                           |
| raytrace                   | 327 ms                                                          | 209 ms: 1.57x faster                                                            |
| pickle_pure_python         | 309 us                                                          | 199 us: 1.55x faster                                                            |
| async_tree_none            | 343 ms                                                          | 225 ms: 1.52x faster                                                            |
| coroutines                 | 23.7 ms                                                         | 15.7 ms: 1.52x faster                                                           |
| sqlglot_transpile          | 1.78 ms                                                         | 1.18 ms: 1.51x faster                                                           |
| logging_simple             | 10.8 us                                                         | 7.19 us: 1.50x faster                                                           |
| scimark_sor                | 135 ms                                                          | 90.1 ms: 1.50x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 273 ms: 1.50x faster                                                            |
| pprint_pformat             | 1.70 sec                                                        | 1.14 sec: 1.48x faster                                                          |
| async_tree_none_tg         | 301 ms                                                          | 203 ms: 1.48x faster                                                            |
| pyflate                    | 471 ms                                                          | 321 ms: 1.47x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 257 ms: 1.47x faster                                                            |
| json_dumps                 | 9.80 ms                                                         | 6.68 ms: 1.47x faster                                                           |
| logging_format             | 11.5 us                                                         | 7.82 us: 1.46x faster                                                           |
| pprint_safe_repr           | 819 ms                                                          | 563 ms: 1.46x faster                                                            |
| async_tree_io              | 754 ms                                                          | 527 ms: 1.43x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 528 ms: 1.41x faster                                                            |
| scimark_lu                 | 102 ms                                                          | 72.4 ms: 1.41x faster                                                           |
| sympy_sum                  | 149 ms                                                          | 106 ms: 1.40x faster                                                            |
| xml_etree_process          | 55.0 ms                                                         | 40.4 ms: 1.36x faster                                                           |
| go                         | 147 ms                                                          | 109 ms: 1.35x faster                                                            |
| sympy_str                  | 283 ms                                                          | 210 ms: 1.35x faster                                                            |
| pycparser                  | 1.04 sec                                                        | 789 ms: 1.32x faster                                                            |
| chameleon                  | 8.08 ms                                                         | 6.12 ms: 1.32x faster                                                           |
| xml_etree_generate         | 71.6 ms                                                         | 55.6 ms: 1.29x faster                                                           |
| mdp                        | 2.07 sec                                                        | 1.61 sec: 1.29x faster                                                          |
| sympy_integrate            | 19.9 ms                                                         | 15.5 ms: 1.29x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 454 ms: 1.27x faster                                                            |
| asyncio_tcp                | 787 ms                                                          | 625 ms: 1.26x faster                                                            |
| meteor_contest             | 90.9 ms                                                         | 72.5 ms: 1.25x faster                                                           |
| genshi_text                | 26.8 ms                                                         | 21.4 ms: 1.25x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 472 ms: 1.25x faster                                                            |
| sqlglot_optimize           | 51.8 ms                                                         | 41.6 ms: 1.25x faster                                                           |
| deepcopy                   | 381 us                                                          | 307 us: 1.24x faster                                                            |
| xml_etree_iterparse        | 75.6 ms                                                         | 61.1 ms: 1.24x faster                                                           |
| sympy_expand               | 462 ms                                                          | 376 ms: 1.23x faster                                                            |
| tornado_http               | 118 ms                                                          | 96.7 ms: 1.22x faster                                                           |
| django_template            | 37.4 ms                                                         | 30.7 ms: 1.22x faster                                                           |
| deepcopy_reduce            | 3.32 us                                                         | 2.73 us: 1.21x faster                                                           |
| html5lib                   | 54.3 ms                                                         | 45.2 ms: 1.20x faster                                                           |
| genshi_xml                 | 61.2 ms                                                         | 51.7 ms: 1.18x faster                                                           |
| 2to3                       | 282 ms                                                          | 245 ms: 1.15x faster                                                            |
| bench_thread_pool          | 1.14 ms                                                         | 993 us: 1.15x faster                                                            |
| json                       | 4.78 ms                                                         | 4.22 ms: 1.13x faster                                                           |
| sqlite_synth               | 2.15 us                                                         | 1.90 us: 1.13x faster                                                           |
| docutils                   | 2.10 sec                                                        | 1.87 sec: 1.12x faster                                                          |
| xml_etree_parse            | 114 ms                                                          | 103 ms: 1.11x faster                                                            |
| unpickle_list              | 3.28 us                                                         | 2.96 us: 1.11x faster                                                           |
| pidigits                   | 203 ms                                                          | 196 ms: 1.03x faster                                                            |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.9 sec: 1.01x faster                                                          |
| regex_dna                  | 122 ms                                                          | 123 ms: 1.01x slower                                                            |
| pickle                     | 7.99 us                                                         | 8.05 us: 1.01x slower                                                           |
| json_loads                 | 20.0 us                                                         | 20.6 us: 1.03x slower                                                           |
| pickle_dict                | 20.1 us                                                         | 20.7 us: 1.03x slower                                                           |
| telco                      | 5.29 ms                                                         | 5.49 ms: 1.04x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 83.3 ms: 1.04x slower                                                           |
| gc_traversal               | 1.38 ms                                                         | 1.44 ms: 1.05x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 16.0 ms: 1.06x slower                                                           |
| python_startup_no_site     | 18.8 ms                                                         | 20.1 ms: 1.07x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.95 ms: 1.07x slower                                                           |
| bench_mp_pool              | 70.9 ms                                                         | 76.4 ms: 1.08x slower                                                           |
| python_startup             | 22.0 ms                                                         | 24.4 ms: 1.11x slower                                                           |
| pickle_list                | 3.27 us                                                         | 3.63 us: 1.11x slower                                                           |
| unpickle                   | 9.23 us                                                         | 10.3 us: 1.12x slower                                                           |
| async_generators           | 260 ms                                                          | 291 ms: 1.12x slower                                                            |
| create_gc_cycles           | 618 us                                                          | 768 us: 1.24x slower                                                            |
| sqlglot_normalize          | 113 ms                                                          | 221 ms: 1.96x slower                                                            |
| coverage                   | 58.0 ms                                                         | 332 ms: 5.72x slower                                                            |
| thrift                     | 801 us                                                          | 10.3 ms: 12.81x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.27x faster                                                                    |

Benchmark hidden because not significant (1): flaskblogging
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.29x
- 95% likely to have a speedup of 1.28x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: unknown