# Results vs. 3.11.0

- fork: python
- ref: 44995aab499b09a550de
- machine: windows-x86
- commit hash: 44995aa
- commit date: 2024-05-13
- overall geometric mean: 1.16x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 257 ms: 1.10x faster                                                            |
| chameleon      | 8.08 ms                                                         | 6.38 ms: 1.27x faster                                                           |
| docutils       | 2.10 sec                                                        | 2.01 sec: 1.04x faster                                                          |
| html5lib       | 54.3 ms                                                         | 50.8 ms: 1.07x faster                                                           |
| tornado_http   | 118 ms                                                          | 99.6 ms: 1.19x faster                                                           |
| Geometric mean | (ref)                                                           | 1.13x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 233 ms: 1.47x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 282 ms: 1.45x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 261 ms: 1.45x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 208 ms: 1.45x faster                                                            |
| async_tree_io              | 754 ms                                                          | 534 ms: 1.41x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 538 ms: 1.39x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 458 ms: 1.26x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 487 ms: 1.21x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.38x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 79.5 ms: 1.58x faster                                                           |
| float          | 76.1 ms                                                         | 57.2 ms: 1.33x faster                                                           |
| pidigits       | 203 ms                                                          | 202 ms: 1.00x faster                                                            |
| Geometric mean | (ref)                                                           | 1.28x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 126 ms: 1.17x faster                                                            |
| regex_dna      | 122 ms                                                          | 118 ms: 1.03x faster                                                            |
| regex_effbot   | 1.82 ms                                                         | 1.91 ms: 1.04x slower                                                           |
| regex_v8       | 15.2 ms                                                         | 16.3 ms: 1.07x slower                                                           |
| Geometric mean | (ref)                                                           | 1.02x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 9.80 ms                                                         | 6.98 ms: 1.40x faster                                                           |
| tomli_loads          | 2.31 sec                                                        | 1.68 sec: 1.38x faster                                                          |
| unpickle_pure_python | 231 us                                                          | 181 us: 1.28x faster                                                            |
| xml_etree_process    | 55.0 ms                                                         | 44.5 ms: 1.24x faster                                                           |
| pickle_pure_python   | 309 us                                                          | 255 us: 1.21x faster                                                            |
| unpickle_list        | 3.28 us                                                         | 2.73 us: 1.20x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 62.0 ms: 1.16x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 66.5 ms: 1.14x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 104 ms: 1.10x faster                                                            |
| pickle_dict          | 20.1 us                                                         | 20.7 us: 1.03x slower                                                           |
| pickle               | 7.99 us                                                         | 8.24 us: 1.03x slower                                                           |
| json_loads           | 20.0 us                                                         | 20.7 us: 1.03x slower                                                           |
| unpickle             | 9.23 us                                                         | 10.2 us: 1.10x slower                                                           |
| pickle_list          | 3.27 us                                                         | 3.64 us: 1.11x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.12x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 18.4 ms: 1.02x faster                                                           |
| python_startup         | 22.0 ms                                                         | 22.3 ms: 1.02x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.00x faster                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 7.78 ms: 1.32x faster                                                           |
| genshi_text     | 26.8 ms                                                         | 20.6 ms: 1.30x faster                                                           |
| genshi_xml      | 61.2 ms                                                         | 48.4 ms: 1.26x faster                                                           |
| django_template | 37.4 ms                                                         | 31.9 ms: 1.17x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.26x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240513-pythonperf1_win32-x86-python-44995aab499b09a550de-3.13.0b1+-44995aa |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 146 us: 3.27x faster                                                            |
| generators                 | 52.2 ms                                                         | 23.4 ms: 2.23x faster                                                           |
| pylint                     | 418 ms                                                          | 244 ms: 1.71x faster                                                            |
| nbody                      | 126 ms                                                          | 79.5 ms: 1.58x faster                                                           |
| chaos                      | 84.4 ms                                                         | 53.3 ms: 1.58x faster                                                           |
| richards_super             | 58.7 ms                                                         | 37.1 ms: 1.58x faster                                                           |
| spectral_norm              | 122 ms                                                          | 78.6 ms: 1.55x faster                                                           |
| raytrace                   | 327 ms                                                          | 214 ms: 1.53x faster                                                            |
| comprehensions             | 22.1 us                                                         | 14.7 us: 1.50x faster                                                           |
| richards                   | 48.8 ms                                                         | 32.6 ms: 1.50x faster                                                           |
| coroutines                 | 23.7 ms                                                         | 16.0 ms: 1.49x faster                                                           |
| async_tree_none            | 343 ms                                                          | 233 ms: 1.47x faster                                                            |
| logging_silent             | 119 ns                                                          | 81.3 ns: 1.47x faster                                                           |
| nqueens                    | 111 ms                                                          | 76.8 ms: 1.45x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 1.03 ms: 1.45x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 282 ms: 1.45x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 261 ms: 1.45x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 208 ms: 1.45x faster                                                            |
| async_tree_io              | 754 ms                                                          | 534 ms: 1.41x faster                                                            |
| deltablue                  | 4.10 ms                                                         | 2.90 ms: 1.41x faster                                                           |
| json_dumps                 | 9.80 ms                                                         | 6.98 ms: 1.40x faster                                                           |
| scimark_sor                | 135 ms                                                          | 97.1 ms: 1.39x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 538 ms: 1.39x faster                                                            |
| sqlglot_transpile          | 1.78 ms                                                         | 1.29 ms: 1.38x faster                                                           |
| logging_simple             | 10.8 us                                                         | 7.82 us: 1.38x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.68 sec: 1.38x faster                                                          |
| logging_format             | 11.5 us                                                         | 8.40 us: 1.36x faster                                                           |
| fannkuch                   | 399 ms                                                          | 299 ms: 1.34x faster                                                            |
| float                      | 76.1 ms                                                         | 57.2 ms: 1.33x faster                                                           |
| scimark_fft                | 291 ms                                                          | 220 ms: 1.32x faster                                                            |
| deepcopy_memo              | 40.0 us                                                         | 30.3 us: 1.32x faster                                                           |
| mako                       | 10.3 ms                                                         | 7.78 ms: 1.32x faster                                                           |
| crypto_pyaes               | 79.4 ms                                                         | 60.2 ms: 1.32x faster                                                           |
| genshi_text                | 26.8 ms                                                         | 20.6 ms: 1.30x faster                                                           |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.29 ms: 1.29x faster                                                           |
| scimark_monte_carlo        | 70.8 ms                                                         | 55.1 ms: 1.28x faster                                                           |
| unpickle_pure_python       | 231 us                                                          | 181 us: 1.28x faster                                                            |
| pprint_pformat             | 1.70 sec                                                        | 1.33 sec: 1.27x faster                                                          |
| chameleon                  | 8.08 ms                                                         | 6.38 ms: 1.27x faster                                                           |
| pprint_safe_repr           | 819 ms                                                          | 648 ms: 1.26x faster                                                            |
| genshi_xml                 | 61.2 ms                                                         | 48.4 ms: 1.26x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 458 ms: 1.26x faster                                                            |
| sympy_sum                  | 149 ms                                                          | 118 ms: 1.26x faster                                                            |
| go                         | 147 ms                                                          | 118 ms: 1.25x faster                                                            |
| xml_etree_process          | 55.0 ms                                                         | 44.5 ms: 1.24x faster                                                           |
| mdp                        | 2.07 sec                                                        | 1.68 sec: 1.23x faster                                                          |
| pycparser                  | 1.04 sec                                                        | 853 ms: 1.22x faster                                                            |
| hexiom                     | 7.51 ms                                                         | 6.16 ms: 1.22x faster                                                           |
| pickle_pure_python         | 309 us                                                          | 255 us: 1.21x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 487 ms: 1.21x faster                                                            |
| scimark_lu                 | 102 ms                                                          | 84.5 ms: 1.21x faster                                                           |
| unpickle_list              | 3.28 us                                                         | 2.73 us: 1.20x faster                                                           |
| sympy_integrate            | 19.9 ms                                                         | 16.7 ms: 1.19x faster                                                           |
| sympy_str                  | 283 ms                                                          | 237 ms: 1.19x faster                                                            |
| tornado_http               | 118 ms                                                          | 99.6 ms: 1.19x faster                                                           |
| deepcopy                   | 381 us                                                          | 321 us: 1.19x faster                                                            |
| pyflate                    | 471 ms                                                          | 397 ms: 1.19x faster                                                            |
| deepcopy_reduce            | 3.32 us                                                         | 2.81 us: 1.18x faster                                                           |
| django_template            | 37.4 ms                                                         | 31.9 ms: 1.17x faster                                                           |
| sqlglot_optimize           | 51.8 ms                                                         | 44.2 ms: 1.17x faster                                                           |
| regex_compile              | 148 ms                                                          | 126 ms: 1.17x faster                                                            |
| xml_etree_generate         | 71.6 ms                                                         | 62.0 ms: 1.16x faster                                                           |
| meteor_contest             | 90.9 ms                                                         | 79.7 ms: 1.14x faster                                                           |
| xml_etree_iterparse        | 75.6 ms                                                         | 66.5 ms: 1.14x faster                                                           |
| sqlite_synth               | 2.15 us                                                         | 1.91 us: 1.13x faster                                                           |
| json                       | 4.78 ms                                                         | 4.25 ms: 1.13x faster                                                           |
| 2to3                       | 282 ms                                                          | 257 ms: 1.10x faster                                                            |
| sympy_expand               | 462 ms                                                          | 421 ms: 1.10x faster                                                            |
| bench_thread_pool          | 1.14 ms                                                         | 1.04 ms: 1.10x faster                                                           |
| xml_etree_parse            | 114 ms                                                          | 104 ms: 1.10x faster                                                            |
| asyncio_tcp                | 787 ms                                                          | 719 ms: 1.09x faster                                                            |
| html5lib                   | 54.3 ms                                                         | 50.8 ms: 1.07x faster                                                           |
| docutils                   | 2.10 sec                                                        | 2.01 sec: 1.04x faster                                                          |
| regex_dna                  | 122 ms                                                          | 118 ms: 1.03x faster                                                            |
| python_startup_no_site     | 18.8 ms                                                         | 18.4 ms: 1.02x faster                                                           |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.9 sec: 1.01x faster                                                          |
| pidigits                   | 203 ms                                                          | 202 ms: 1.00x faster                                                            |
| python_startup             | 22.0 ms                                                         | 22.3 ms: 1.02x slower                                                           |
| bench_mp_pool              | 70.9 ms                                                         | 72.8 ms: 1.03x slower                                                           |
| pickle_dict                | 20.1 us                                                         | 20.7 us: 1.03x slower                                                           |
| pickle                     | 7.99 us                                                         | 8.24 us: 1.03x slower                                                           |
| json_loads                 | 20.0 us                                                         | 20.7 us: 1.03x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.91 ms: 1.04x slower                                                           |
| gc_traversal               | 1.38 ms                                                         | 1.46 ms: 1.06x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 16.3 ms: 1.07x slower                                                           |
| unpickle                   | 9.23 us                                                         | 10.2 us: 1.10x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 88.3 ms: 1.10x slower                                                           |
| pickle_list                | 3.27 us                                                         | 3.64 us: 1.11x slower                                                           |
| async_generators           | 260 ms                                                          | 290 ms: 1.12x slower                                                            |
| create_gc_cycles           | 618 us                                                          | 761 us: 1.23x slower                                                            |
| telco                      | 5.29 ms                                                         | 6.89 ms: 1.30x slower                                                           |
| sqlglot_normalize          | 113 ms                                                          | 227 ms: 2.01x slower                                                            |
| coverage                   | 58.0 ms                                                         | 331 ms: 5.71x slower                                                            |
| thrift                     | 801 us                                                          | 11.8 ms: 14.69x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.16x faster                                                                    |

Benchmark hidden because not significant (1): flaskblogging
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: unknown