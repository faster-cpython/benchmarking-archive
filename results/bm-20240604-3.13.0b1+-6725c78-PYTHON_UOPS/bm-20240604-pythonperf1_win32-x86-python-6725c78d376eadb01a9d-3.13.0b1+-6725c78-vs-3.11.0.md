# Results vs. 3.11.0

- fork: python
- ref: 6725c78d376eadb01a9d
- machine: windows-x86
- commit hash: 6725c78
- commit date: 2024-06-04
- overall geometric mean: 1.18x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 254 ms: 1.11x faster                                                            |
| chameleon      | 8.08 ms                                                         | 6.33 ms: 1.28x faster                                                           |
| docutils       | 2.10 sec                                                        | 2.00 sec: 1.05x faster                                                          |
| html5lib       | 54.3 ms                                                         | 50.7 ms: 1.07x faster                                                           |
| tornado_http   | 118 ms                                                          | 99.7 ms: 1.19x faster                                                           |
| Geometric mean | (ref)                                                           | 1.14x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 236 ms: 1.45x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 263 ms: 1.44x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 210 ms: 1.43x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 295 ms: 1.39x faster                                                            |
| async_tree_io              | 754 ms                                                          | 545 ms: 1.38x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 542 ms: 1.38x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 456 ms: 1.26x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 486 ms: 1.21x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.37x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 75.2 ms: 1.68x faster                                                           |
| float          | 76.1 ms                                                         | 52.9 ms: 1.44x faster                                                           |
| pidigits       | 203 ms                                                          | 198 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                           | 1.35x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 124 ms: 1.19x faster                                                            |
| regex_dna      | 122 ms                                                          | 119 ms: 1.02x faster                                                            |
| regex_effbot   | 1.82 ms                                                         | 1.92 ms: 1.05x slower                                                           |
| regex_v8       | 15.2 ms                                                         | 16.0 ms: 1.06x slower                                                           |
| Geometric mean | (ref)                                                           | 1.02x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.80 ms                                                         | 6.74 ms: 1.45x faster                                                           |
| tomli_loads          | 2.31 sec                                                        | 1.62 sec: 1.43x faster                                                          |
| unpickle_pure_python | 231 us                                                          | 172 us: 1.35x faster                                                            |
| xml_etree_process    | 55.0 ms                                                         | 43.1 ms: 1.28x faster                                                           |
| pickle_pure_python   | 309 us                                                          | 247 us: 1.25x faster                                                            |
| xml_etree_generate   | 71.6 ms                                                         | 60.0 ms: 1.19x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 64.2 ms: 1.18x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 2.95 us: 1.11x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 104 ms: 1.10x faster                                                            |
| pickle_dict          | 20.1 us                                                         | 20.6 us: 1.03x slower                                                           |
| pickle               | 7.99 us                                                         | 8.25 us: 1.03x slower                                                           |
| json_loads           | 20.0 us                                                         | 20.9 us: 1.04x slower                                                           |
| pickle_list          | 3.27 us                                                         | 3.65 us: 1.12x slower                                                           |
| unpickle             | 9.23 us                                                         | 10.4 us: 1.13x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.13x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 18.3 ms: 1.03x faster                                                           |
| python_startup         | 22.0 ms                                                         | 22.6 ms: 1.03x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.00x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 7.24 ms: 1.42x faster                                                           |
| genshi_text     | 26.8 ms                                                         | 21.2 ms: 1.26x faster                                                           |
| genshi_xml      | 61.2 ms                                                         | 50.1 ms: 1.22x faster                                                           |
| django_template | 37.4 ms                                                         | 32.4 ms: 1.15x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.26x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf1_win32-x86-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 147 us: 3.25x faster                                                            |
| generators                 | 52.2 ms                                                         | 23.6 ms: 2.21x faster                                                           |
| pylint                     | 418 ms                                                          | 242 ms: 1.73x faster                                                            |
| spectral_norm              | 122 ms                                                          | 71.5 ms: 1.70x faster                                                           |
| nbody                      | 126 ms                                                          | 75.2 ms: 1.68x faster                                                           |
| richards_super             | 58.7 ms                                                         | 35.4 ms: 1.66x faster                                                           |
| comprehensions             | 22.1 us                                                         | 13.7 us: 1.61x faster                                                           |
| logging_silent             | 119 ns                                                          | 74.2 ns: 1.61x faster                                                           |
| chaos                      | 84.4 ms                                                         | 53.0 ms: 1.59x faster                                                           |
| richards                   | 48.8 ms                                                         | 31.3 ms: 1.56x faster                                                           |
| raytrace                   | 327 ms                                                          | 212 ms: 1.54x faster                                                            |
| coroutines                 | 23.7 ms                                                         | 15.6 ms: 1.52x faster                                                           |
| nqueens                    | 111 ms                                                          | 73.6 ms: 1.51x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 1.02 ms: 1.46x faster                                                           |
| async_tree_none            | 343 ms                                                          | 236 ms: 1.45x faster                                                            |
| scimark_sor                | 135 ms                                                          | 93.0 ms: 1.45x faster                                                           |
| json_dumps                 | 9.80 ms                                                         | 6.74 ms: 1.45x faster                                                           |
| deepcopy_memo              | 40.0 us                                                         | 27.6 us: 1.45x faster                                                           |
| deltablue                  | 4.10 ms                                                         | 2.83 ms: 1.45x faster                                                           |
| fannkuch                   | 399 ms                                                          | 277 ms: 1.44x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 263 ms: 1.44x faster                                                            |
| float                      | 76.1 ms                                                         | 52.9 ms: 1.44x faster                                                           |
| scimark_monte_carlo        | 70.8 ms                                                         | 49.5 ms: 1.43x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 210 ms: 1.43x faster                                                            |
| tomli_loads                | 2.31 sec                                                        | 1.62 sec: 1.43x faster                                                          |
| mako                       | 10.3 ms                                                         | 7.24 ms: 1.42x faster                                                           |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.01 ms: 1.41x faster                                                           |
| scimark_fft                | 291 ms                                                          | 207 ms: 1.41x faster                                                            |
| logging_simple             | 10.8 us                                                         | 7.69 us: 1.41x faster                                                           |
| crypto_pyaes               | 79.4 ms                                                         | 56.6 ms: 1.40x faster                                                           |
| sqlglot_transpile          | 1.78 ms                                                         | 1.28 ms: 1.40x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 295 ms: 1.39x faster                                                            |
| async_tree_io              | 754 ms                                                          | 545 ms: 1.38x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 542 ms: 1.38x faster                                                            |
| logging_format             | 11.5 us                                                         | 8.41 us: 1.36x faster                                                           |
| unpickle_pure_python       | 231 us                                                          | 172 us: 1.35x faster                                                            |
| pprint_pformat             | 1.70 sec                                                        | 1.27 sec: 1.34x faster                                                          |
| pprint_safe_repr           | 819 ms                                                          | 615 ms: 1.33x faster                                                            |
| hexiom                     | 7.51 ms                                                         | 5.66 ms: 1.33x faster                                                           |
| go                         | 147 ms                                                          | 113 ms: 1.30x faster                                                            |
| scimark_lu                 | 102 ms                                                          | 80.0 ms: 1.28x faster                                                           |
| asyncio_tcp                | 787 ms                                                          | 615 ms: 1.28x faster                                                            |
| xml_etree_process          | 55.0 ms                                                         | 43.1 ms: 1.28x faster                                                           |
| chameleon                  | 8.08 ms                                                         | 6.33 ms: 1.28x faster                                                           |
| pyflate                    | 471 ms                                                          | 371 ms: 1.27x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 456 ms: 1.26x faster                                                            |
| genshi_text                | 26.8 ms                                                         | 21.2 ms: 1.26x faster                                                           |
| sympy_sum                  | 149 ms                                                          | 118 ms: 1.26x faster                                                            |
| pickle_pure_python         | 309 us                                                          | 247 us: 1.25x faster                                                            |
| deepcopy                   | 381 us                                                          | 308 us: 1.24x faster                                                            |
| genshi_xml                 | 61.2 ms                                                         | 50.1 ms: 1.22x faster                                                           |
| mdp                        | 2.07 sec                                                        | 1.70 sec: 1.22x faster                                                          |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 486 ms: 1.21x faster                                                            |
| sympy_integrate            | 19.9 ms                                                         | 16.4 ms: 1.21x faster                                                           |
| sympy_str                  | 283 ms                                                          | 237 ms: 1.20x faster                                                            |
| xml_etree_generate         | 71.6 ms                                                         | 60.0 ms: 1.19x faster                                                           |
| regex_compile              | 148 ms                                                          | 124 ms: 1.19x faster                                                            |
| meteor_contest             | 90.9 ms                                                         | 76.4 ms: 1.19x faster                                                           |
| deepcopy_reduce            | 3.32 us                                                         | 2.79 us: 1.19x faster                                                           |
| tornado_http               | 118 ms                                                          | 99.7 ms: 1.19x faster                                                           |
| pycparser                  | 1.04 sec                                                        | 882 ms: 1.18x faster                                                            |
| xml_etree_iterparse        | 75.6 ms                                                         | 64.2 ms: 1.18x faster                                                           |
| sqlglot_optimize           | 51.8 ms                                                         | 44.1 ms: 1.17x faster                                                           |
| django_template            | 37.4 ms                                                         | 32.4 ms: 1.15x faster                                                           |
| json                       | 4.78 ms                                                         | 4.18 ms: 1.14x faster                                                           |
| bench_thread_pool          | 1.14 ms                                                         | 1.01 ms: 1.12x faster                                                           |
| sqlite_synth               | 2.15 us                                                         | 1.93 us: 1.11x faster                                                           |
| 2to3                       | 282 ms                                                          | 254 ms: 1.11x faster                                                            |
| unpickle_list              | 3.28 us                                                         | 2.95 us: 1.11x faster                                                           |
| xml_etree_parse            | 114 ms                                                          | 104 ms: 1.10x faster                                                            |
| sympy_expand               | 462 ms                                                          | 419 ms: 1.10x faster                                                            |
| html5lib                   | 54.3 ms                                                         | 50.7 ms: 1.07x faster                                                           |
| docutils                   | 2.10 sec                                                        | 2.00 sec: 1.05x faster                                                          |
| python_startup_no_site     | 18.8 ms                                                         | 18.3 ms: 1.03x faster                                                           |
| pidigits                   | 203 ms                                                          | 198 ms: 1.02x faster                                                            |
| regex_dna                  | 122 ms                                                          | 119 ms: 1.02x faster                                                            |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.9 sec: 1.01x faster                                                          |
| flaskblogging              | 2.03 sec                                                        | 2.04 sec: 1.00x slower                                                          |
| bench_mp_pool              | 70.9 ms                                                         | 71.4 ms: 1.01x slower                                                           |
| pickle_dict                | 20.1 us                                                         | 20.6 us: 1.03x slower                                                           |
| python_startup             | 22.0 ms                                                         | 22.6 ms: 1.03x slower                                                           |
| pickle                     | 7.99 us                                                         | 8.25 us: 1.03x slower                                                           |
| gc_traversal               | 1.38 ms                                                         | 1.44 ms: 1.04x slower                                                           |
| json_loads                 | 20.0 us                                                         | 20.9 us: 1.04x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 83.9 ms: 1.05x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.92 ms: 1.05x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 16.0 ms: 1.06x slower                                                           |
| telco                      | 5.29 ms                                                         | 5.80 ms: 1.10x slower                                                           |
| async_generators           | 260 ms                                                          | 285 ms: 1.10x slower                                                            |
| pickle_list                | 3.27 us                                                         | 3.65 us: 1.12x slower                                                           |
| unpickle                   | 9.23 us                                                         | 10.4 us: 1.13x slower                                                           |
| create_gc_cycles           | 618 us                                                          | 766 us: 1.24x slower                                                            |
| sqlglot_normalize          | 113 ms                                                          | 229 ms: 2.03x slower                                                            |
| coverage                   | 58.0 ms                                                         | 325 ms: 5.59x slower                                                            |
| thrift                     | 801 us                                                          | 11.6 ms: 14.46x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.18x faster                                                                    |
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.20x
- 95% likely to have a speedup of 1.19x
- 99% likely to have a speedup of 1.18x

# Memory
- memory change: unknown