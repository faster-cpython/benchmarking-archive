# Results vs. 3.11.0

- fork: python
- ref: 6b10467fbc0b67bf217e
- machine: windows-x86
- commit hash: 6b10467
- commit date: 2024-06-03
- overall geometric mean: 1.26x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf1_win32-x86-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 230 ms: 1.23x faster                                                            |
| chameleon      | 8.08 ms                                                         | 5.70 ms: 1.42x faster                                                           |
| docutils       | 2.10 sec                                                        | 1.81 sec: 1.16x faster                                                          |
| html5lib       | 54.3 ms                                                         | 43.9 ms: 1.24x faster                                                           |
| tornado_http   | 118 ms                                                          | 94.1 ms: 1.26x faster                                                           |
| Geometric mean | (ref)                                                           | 1.26x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf1_win32-x86-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 224 ms: 1.53x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 201 ms: 1.50x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 273 ms: 1.50x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 254 ms: 1.49x faster                                                            |
| async_tree_io              | 754 ms                                                          | 529 ms: 1.43x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 525 ms: 1.42x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 468 ms: 1.23x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 486 ms: 1.21x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.41x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf1_win32-x86-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 75.9 ms: 1.66x faster                                                           |
| float          | 76.1 ms                                                         | 52.8 ms: 1.44x faster                                                           |
| pidigits       | 203 ms                                                          | 196 ms: 1.04x faster                                                            |
| Geometric mean | (ref)                                                           | 1.35x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf1_win32-x86-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 97.2 ms: 1.52x faster                                                           |
| regex_dna      | 122 ms                                                          | 119 ms: 1.02x faster                                                            |
| regex_effbot   | 1.82 ms                                                         | 1.88 ms: 1.03x slower                                                           |
| regex_v8       | 15.2 ms                                                         | 15.8 ms: 1.04x slower                                                           |
| Geometric mean | (ref)                                                           | 1.10x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf1_win32-x86-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 147 us: 1.57x faster                                                            |
| tomli_loads          | 2.31 sec                                                        | 1.58 sec: 1.46x faster                                                          |
| json_dumps           | 9.80 ms                                                         | 6.84 ms: 1.43x faster                                                           |
| pickle_pure_python   | 309 us                                                          | 221 us: 1.40x faster                                                            |
| xml_etree_process    | 55.0 ms                                                         | 41.6 ms: 1.32x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 59.1 ms: 1.21x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 63.4 ms: 1.19x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 2.88 us: 1.14x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 103 ms: 1.11x faster                                                            |
| pickle               | 7.99 us                                                         | 7.95 us: 1.00x faster                                                           |
| pickle_dict          | 20.1 us                                                         | 20.6 us: 1.03x slower                                                           |
| json_loads           | 20.0 us                                                         | 20.8 us: 1.04x slower                                                           |
| pickle_list          | 3.27 us                                                         | 3.54 us: 1.08x slower                                                           |
| unpickle             | 9.23 us                                                         | 10.1 us: 1.09x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.17x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf1_win32-x86-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 18.3 ms: 1.03x faster                                                           |
| python_startup         | 22.0 ms                                                         | 22.4 ms: 1.02x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.00x faster                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf1_win32-x86-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 6.95 ms: 1.48x faster                                                           |
| genshi_xml      | 61.2 ms                                                         | 42.8 ms: 1.43x faster                                                           |
| genshi_text     | 26.8 ms                                                         | 18.9 ms: 1.42x faster                                                           |
| django_template | 37.4 ms                                                         | 29.1 ms: 1.28x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.40x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240603-pythonperf1_win32-x86-python-6b10467fbc0b67bf217e-3.13.0b1+-6b10467 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 135 us: 3.55x faster                                                            |
| generators                 | 52.2 ms                                                         | 21.4 ms: 2.44x faster                                                           |
| logging_silent             | 119 ns                                                          | 58.1 ns: 2.05x faster                                                           |
| pylint                     | 418 ms                                                          | 217 ms: 1.92x faster                                                            |
| deltablue                  | 4.10 ms                                                         | 2.22 ms: 1.84x faster                                                           |
| spectral_norm              | 122 ms                                                          | 66.6 ms: 1.83x faster                                                           |
| comprehensions             | 22.1 us                                                         | 12.1 us: 1.82x faster                                                           |
| chaos                      | 84.4 ms                                                         | 47.1 ms: 1.79x faster                                                           |
| raytrace                   | 327 ms                                                          | 186 ms: 1.76x faster                                                            |
| hexiom                     | 7.51 ms                                                         | 4.38 ms: 1.72x faster                                                           |
| deepcopy_memo              | 40.0 us                                                         | 23.8 us: 1.68x faster                                                           |
| richards_super             | 58.7 ms                                                         | 35.0 ms: 1.67x faster                                                           |
| nbody                      | 126 ms                                                          | 75.9 ms: 1.66x faster                                                           |
| scimark_lu                 | 102 ms                                                          | 61.7 ms: 1.66x faster                                                           |
| nqueens                    | 111 ms                                                          | 68.1 ms: 1.64x faster                                                           |
| scimark_sor                | 135 ms                                                          | 84.1 ms: 1.61x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 940 us: 1.59x faster                                                            |
| richards                   | 48.8 ms                                                         | 31.0 ms: 1.57x faster                                                           |
| unpickle_pure_python       | 231 us                                                          | 147 us: 1.57x faster                                                            |
| async_tree_none            | 343 ms                                                          | 224 ms: 1.53x faster                                                            |
| coroutines                 | 23.7 ms                                                         | 15.5 ms: 1.53x faster                                                           |
| pyflate                    | 471 ms                                                          | 308 ms: 1.53x faster                                                            |
| sqlglot_transpile          | 1.78 ms                                                         | 1.17 ms: 1.53x faster                                                           |
| regex_compile              | 148 ms                                                          | 97.2 ms: 1.52x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 201 ms: 1.50x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 273 ms: 1.50x faster                                                            |
| scimark_monte_carlo        | 70.8 ms                                                         | 47.5 ms: 1.49x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 254 ms: 1.49x faster                                                            |
| logging_simple             | 10.8 us                                                         | 7.31 us: 1.48x faster                                                           |
| mako                       | 10.3 ms                                                         | 6.95 ms: 1.48x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.58 sec: 1.46x faster                                                          |
| fannkuch                   | 399 ms                                                          | 274 ms: 1.46x faster                                                            |
| go                         | 147 ms                                                          | 102 ms: 1.45x faster                                                            |
| logging_format             | 11.5 us                                                         | 7.93 us: 1.45x faster                                                           |
| float                      | 76.1 ms                                                         | 52.8 ms: 1.44x faster                                                           |
| sympy_sum                  | 149 ms                                                          | 104 ms: 1.44x faster                                                            |
| json_dumps                 | 9.80 ms                                                         | 6.84 ms: 1.43x faster                                                           |
| genshi_xml                 | 61.2 ms                                                         | 42.8 ms: 1.43x faster                                                           |
| crypto_pyaes               | 79.4 ms                                                         | 55.6 ms: 1.43x faster                                                           |
| async_tree_io              | 754 ms                                                          | 529 ms: 1.43x faster                                                            |
| pprint_pformat             | 1.70 sec                                                        | 1.19 sec: 1.42x faster                                                          |
| async_tree_io_tg           | 746 ms                                                          | 525 ms: 1.42x faster                                                            |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.98 ms: 1.42x faster                                                           |
| genshi_text                | 26.8 ms                                                         | 18.9 ms: 1.42x faster                                                           |
| chameleon                  | 8.08 ms                                                         | 5.70 ms: 1.42x faster                                                           |
| scimark_fft                | 291 ms                                                          | 207 ms: 1.41x faster                                                            |
| pprint_safe_repr           | 819 ms                                                          | 583 ms: 1.41x faster                                                            |
| pickle_pure_python         | 309 us                                                          | 221 us: 1.40x faster                                                            |
| sympy_integrate            | 19.9 ms                                                         | 14.5 ms: 1.38x faster                                                           |
| deepcopy                   | 381 us                                                          | 278 us: 1.37x faster                                                            |
| sympy_str                  | 283 ms                                                          | 207 ms: 1.37x faster                                                            |
| pycparser                  | 1.04 sec                                                        | 776 ms: 1.35x faster                                                            |
| xml_etree_process          | 55.0 ms                                                         | 41.6 ms: 1.32x faster                                                           |
| sqlglot_optimize           | 51.8 ms                                                         | 39.7 ms: 1.30x faster                                                           |
| django_template            | 37.4 ms                                                         | 29.1 ms: 1.28x faster                                                           |
| sympy_expand               | 462 ms                                                          | 363 ms: 1.27x faster                                                            |
| mdp                        | 2.07 sec                                                        | 1.63 sec: 1.27x faster                                                          |
| tornado_http               | 118 ms                                                          | 94.1 ms: 1.26x faster                                                           |
| deepcopy_reduce            | 3.32 us                                                         | 2.66 us: 1.25x faster                                                           |
| html5lib                   | 54.3 ms                                                         | 43.9 ms: 1.24x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 468 ms: 1.23x faster                                                            |
| 2to3                       | 282 ms                                                          | 230 ms: 1.23x faster                                                            |
| meteor_contest             | 90.9 ms                                                         | 74.4 ms: 1.22x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 486 ms: 1.21x faster                                                            |
| xml_etree_generate         | 71.6 ms                                                         | 59.1 ms: 1.21x faster                                                           |
| xml_etree_iterparse        | 75.6 ms                                                         | 63.4 ms: 1.19x faster                                                           |
| json                       | 4.78 ms                                                         | 4.11 ms: 1.16x faster                                                           |
| docutils                   | 2.10 sec                                                        | 1.81 sec: 1.16x faster                                                          |
| bench_thread_pool          | 1.14 ms                                                         | 982 us: 1.16x faster                                                            |
| asyncio_tcp                | 787 ms                                                          | 681 ms: 1.16x faster                                                            |
| unpickle_list              | 3.28 us                                                         | 2.88 us: 1.14x faster                                                           |
| sqlite_synth               | 2.15 us                                                         | 1.93 us: 1.12x faster                                                           |
| xml_etree_parse            | 114 ms                                                          | 103 ms: 1.11x faster                                                            |
| pidigits                   | 203 ms                                                          | 196 ms: 1.04x faster                                                            |
| python_startup_no_site     | 18.8 ms                                                         | 18.3 ms: 1.03x faster                                                           |
| bench_mp_pool              | 70.9 ms                                                         | 69.1 ms: 1.03x faster                                                           |
| regex_dna                  | 122 ms                                                          | 119 ms: 1.02x faster                                                            |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.9 sec: 1.01x faster                                                          |
| pickle                     | 7.99 us                                                         | 7.95 us: 1.00x faster                                                           |
| flaskblogging              | 2.03 sec                                                        | 2.03 sec: 1.00x slower                                                          |
| python_startup             | 22.0 ms                                                         | 22.4 ms: 1.02x slower                                                           |
| pickle_dict                | 20.1 us                                                         | 20.6 us: 1.03x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.88 ms: 1.03x slower                                                           |
| async_generators           | 260 ms                                                          | 269 ms: 1.04x slower                                                            |
| json_loads                 | 20.0 us                                                         | 20.8 us: 1.04x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 83.1 ms: 1.04x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 15.8 ms: 1.04x slower                                                           |
| gc_traversal               | 1.38 ms                                                         | 1.44 ms: 1.04x slower                                                           |
| pickle_list                | 3.27 us                                                         | 3.54 us: 1.08x slower                                                           |
| telco                      | 5.29 ms                                                         | 5.75 ms: 1.09x slower                                                           |
| unpickle                   | 9.23 us                                                         | 10.1 us: 1.09x slower                                                           |
| create_gc_cycles           | 618 us                                                          | 756 us: 1.22x slower                                                            |
| sqlglot_normalize          | 113 ms                                                          | 209 ms: 1.85x slower                                                            |
| coverage                   | 58.0 ms                                                         | 308 ms: 5.31x slower                                                            |
| thrift                     | 801 us                                                          | 9.80 ms: 12.24x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.26x faster                                                                    |
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.30x
- 95% likely to have a speedup of 1.28x
- 99% likely to have a speedup of 1.26x

# Memory
- memory change: unknown