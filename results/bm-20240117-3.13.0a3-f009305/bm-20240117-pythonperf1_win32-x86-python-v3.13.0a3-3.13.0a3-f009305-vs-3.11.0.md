# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a3
- machine: windows-x86
- commit hash: f009305
- commit date: 2024-01-17
- overall geometric mean: 1.28x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf1_win32-x86-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 232 ms: 1.22x faster                                                |
| chameleon      | 8.08 ms                                                         | 5.40 ms: 1.49x faster                                               |
| docutils       | 2.10 sec                                                        | 1.72 sec: 1.22x faster                                              |
| html5lib       | 54.3 ms                                                         | 44.0 ms: 1.23x faster                                               |
| tornado_http   | 118 ms                                                          | 96.3 ms: 1.23x faster                                               |
| Geometric mean | (ref)                                                           | 1.28x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf1_win32-x86-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 241 ms: 1.42x faster                                                |
| async_tree_memoization     | 408 ms                                                          | 303 ms: 1.35x faster                                                |
| async_tree_none_tg         | 301 ms                                                          | 229 ms: 1.31x faster                                                |
| async_tree_io_tg           | 746 ms                                                          | 571 ms: 1.31x faster                                                |
| async_tree_memoization_tg  | 378 ms                                                          | 290 ms: 1.30x faster                                                |
| async_tree_io              | 754 ms                                                          | 588 ms: 1.28x faster                                                |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 499 ms: 1.18x faster                                                |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 489 ms: 1.18x faster                                                |
| Geometric mean             | (ref)                                                           | 1.29x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf1_win32-x86-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 74.0 ms: 1.70x faster                                               |
| float          | 76.1 ms                                                         | 51.1 ms: 1.49x faster                                               |
| pidigits       | 203 ms                                                          | 199 ms: 1.02x faster                                                |
| Geometric mean | (ref)                                                           | 1.37x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf1_win32-x86-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 92.5 ms: 1.59x faster                                               |
| regex_dna      | 122 ms                                                          | 125 ms: 1.02x slower                                                |
| regex_effbot   | 1.82 ms                                                         | 1.92 ms: 1.05x slower                                               |
| regex_v8       | 15.2 ms                                                         | 16.1 ms: 1.06x slower                                               |
| Geometric mean | (ref)                                                           | 1.09x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf1_win32-x86-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 140 us: 1.65x faster                                                |
| pickle_pure_python   | 309 us                                                          | 204 us: 1.52x faster                                                |
| json_dumps           | 9.80 ms                                                         | 6.75 ms: 1.45x faster                                               |
| tomli_loads          | 2.31 sec                                                        | 1.62 sec: 1.43x faster                                              |
| xml_etree_process    | 55.0 ms                                                         | 41.1 ms: 1.34x faster                                               |
| xml_etree_generate   | 71.6 ms                                                         | 58.8 ms: 1.22x faster                                               |
| xml_etree_iterparse  | 75.6 ms                                                         | 66.4 ms: 1.14x faster                                               |
| unpickle_list        | 3.28 us                                                         | 3.08 us: 1.06x faster                                               |
| xml_etree_parse      | 114 ms                                                          | 108 ms: 1.05x faster                                                |
| pickle               | 7.99 us                                                         | 7.71 us: 1.04x faster                                               |
| json_loads           | 20.0 us                                                         | 19.8 us: 1.01x faster                                               |
| pickle_dict          | 20.1 us                                                         | 20.0 us: 1.01x faster                                               |
| pickle_list          | 3.27 us                                                         | 3.33 us: 1.02x slower                                               |
| unpickle             | 9.23 us                                                         | 9.71 us: 1.05x slower                                               |
| Geometric mean       | (ref)                                                           | 1.18x faster                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf1_win32-x86-python-v3.13.0a3-3.13.0a3-f009305 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                         | 22.7 ms: 1.03x slower                                               |
| python_startup_no_site | 18.8 ms                                                         | 20.5 ms: 1.09x slower                                               |
| Geometric mean         | (ref)                                                           | 1.06x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf1_win32-x86-python-v3.13.0a3-3.13.0a3-f009305 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 6.84 ms: 1.50x faster                                               |
| genshi_text     | 26.8 ms                                                         | 18.1 ms: 1.48x faster                                               |
| genshi_xml      | 61.2 ms                                                         | 41.6 ms: 1.47x faster                                               |
| django_template | 37.4 ms                                                         | 29.0 ms: 1.29x faster                                               |
| Geometric mean  | (ref)                                                           | 1.43x faster                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf1_win32-x86-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 87.7 us: 5.46x faster                                               |
| generators                 | 52.2 ms                                                         | 22.9 ms: 2.28x faster                                               |
| logging_silent             | 119 ns                                                          | 57.1 ns: 2.09x faster                                               |
| comprehensions             | 22.1 us                                                         | 11.2 us: 1.97x faster                                               |
| spectral_norm              | 122 ms                                                          | 63.0 ms: 1.93x faster                                               |
| pylint                     | 418 ms                                                          | 217 ms: 1.92x faster                                                |
| deltablue                  | 4.10 ms                                                         | 2.18 ms: 1.88x faster                                               |
| richards_super             | 58.7 ms                                                         | 31.4 ms: 1.87x faster                                               |
| chaos                      | 84.4 ms                                                         | 45.5 ms: 1.85x faster                                               |
| deepcopy_memo              | 40.0 us                                                         | 21.6 us: 1.85x faster                                               |
| hexiom                     | 7.51 ms                                                         | 4.14 ms: 1.81x faster                                               |
| sqlglot_parse              | 1.49 ms                                                         | 848 us: 1.76x faster                                                |
| richards                   | 48.8 ms                                                         | 27.8 ms: 1.75x faster                                               |
| raytrace                   | 327 ms                                                          | 191 ms: 1.72x faster                                                |
| nbody                      | 126 ms                                                          | 74.0 ms: 1.70x faster                                               |
| scimark_lu                 | 102 ms                                                          | 60.2 ms: 1.70x faster                                               |
| scimark_sor                | 135 ms                                                          | 79.6 ms: 1.70x faster                                               |
| coroutines                 | 23.7 ms                                                         | 14.2 ms: 1.67x faster                                               |
| sqlglot_transpile          | 1.78 ms                                                         | 1.08 ms: 1.66x faster                                               |
| unpickle_pure_python       | 231 us                                                          | 140 us: 1.65x faster                                                |
| scimark_monte_carlo        | 70.8 ms                                                         | 44.3 ms: 1.60x faster                                               |
| regex_compile              | 148 ms                                                          | 92.5 ms: 1.59x faster                                               |
| crypto_pyaes               | 79.4 ms                                                         | 51.0 ms: 1.56x faster                                               |
| go                         | 147 ms                                                          | 95.1 ms: 1.55x faster                                               |
| pyflate                    | 471 ms                                                          | 306 ms: 1.54x faster                                                |
| nqueens                    | 111 ms                                                          | 72.6 ms: 1.53x faster                                               |
| pprint_pformat             | 1.70 sec                                                        | 1.12 sec: 1.52x faster                                              |
| pickle_pure_python         | 309 us                                                          | 204 us: 1.52x faster                                                |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.79 ms: 1.52x faster                                               |
| sympy_sum                  | 149 ms                                                          | 98.5 ms: 1.51x faster                                               |
| pprint_safe_repr           | 819 ms                                                          | 543 ms: 1.51x faster                                                |
| mako                       | 10.3 ms                                                         | 6.84 ms: 1.50x faster                                               |
| chameleon                  | 8.08 ms                                                         | 5.40 ms: 1.49x faster                                               |
| fannkuch                   | 399 ms                                                          | 267 ms: 1.49x faster                                                |
| deepcopy                   | 381 us                                                          | 255 us: 1.49x faster                                                |
| deepcopy_reduce            | 3.32 us                                                         | 2.22 us: 1.49x faster                                               |
| float                      | 76.1 ms                                                         | 51.1 ms: 1.49x faster                                               |
| genshi_text                | 26.8 ms                                                         | 18.1 ms: 1.48x faster                                               |
| scimark_fft                | 291 ms                                                          | 198 ms: 1.47x faster                                                |
| genshi_xml                 | 61.2 ms                                                         | 41.6 ms: 1.47x faster                                               |
| sympy_str                  | 283 ms                                                          | 194 ms: 1.46x faster                                                |
| json_dumps                 | 9.80 ms                                                         | 6.75 ms: 1.45x faster                                               |
| tomli_loads                | 2.31 sec                                                        | 1.62 sec: 1.43x faster                                              |
| sympy_integrate            | 19.9 ms                                                         | 14.0 ms: 1.42x faster                                               |
| async_tree_none            | 343 ms                                                          | 241 ms: 1.42x faster                                                |
| logging_simple             | 10.8 us                                                         | 7.69 us: 1.41x faster                                               |
| logging_format             | 11.5 us                                                         | 8.33 us: 1.37x faster                                               |
| sqlglot_optimize           | 51.8 ms                                                         | 38.2 ms: 1.36x faster                                               |
| mdp                        | 2.07 sec                                                        | 1.53 sec: 1.35x faster                                              |
| async_tree_memoization     | 408 ms                                                          | 303 ms: 1.35x faster                                                |
| sympy_expand               | 462 ms                                                          | 343 ms: 1.35x faster                                                |
| xml_etree_process          | 55.0 ms                                                         | 41.1 ms: 1.34x faster                                               |
| pycparser                  | 1.04 sec                                                        | 793 ms: 1.32x faster                                                |
| async_tree_none_tg         | 301 ms                                                          | 229 ms: 1.31x faster                                                |
| async_tree_io_tg           | 746 ms                                                          | 571 ms: 1.31x faster                                                |
| async_tree_memoization_tg  | 378 ms                                                          | 290 ms: 1.30x faster                                                |
| django_template            | 37.4 ms                                                         | 29.0 ms: 1.29x faster                                               |
| async_tree_io              | 754 ms                                                          | 588 ms: 1.28x faster                                                |
| asyncio_tcp                | 787 ms                                                          | 638 ms: 1.23x faster                                                |
| meteor_contest             | 90.9 ms                                                         | 73.7 ms: 1.23x faster                                               |
| html5lib                   | 54.3 ms                                                         | 44.0 ms: 1.23x faster                                               |
| tornado_http               | 118 ms                                                          | 96.3 ms: 1.23x faster                                               |
| docutils                   | 2.10 sec                                                        | 1.72 sec: 1.22x faster                                              |
| xml_etree_generate         | 71.6 ms                                                         | 58.8 ms: 1.22x faster                                               |
| 2to3                       | 282 ms                                                          | 232 ms: 1.22x faster                                                |
| sqlite_synth               | 2.15 us                                                         | 1.81 us: 1.19x faster                                               |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 499 ms: 1.18x faster                                                |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 489 ms: 1.18x faster                                                |
| json                       | 4.78 ms                                                         | 4.12 ms: 1.16x faster                                               |
| xml_etree_iterparse        | 75.6 ms                                                         | 66.4 ms: 1.14x faster                                               |
| bench_thread_pool          | 1.14 ms                                                         | 1.01 ms: 1.12x faster                                               |
| unpickle_list              | 3.28 us                                                         | 3.08 us: 1.06x faster                                               |
| xml_etree_parse            | 114 ms                                                          | 108 ms: 1.05x faster                                                |
| pickle                     | 7.99 us                                                         | 7.71 us: 1.04x faster                                               |
| pidigits                   | 203 ms                                                          | 199 ms: 1.02x faster                                                |
| json_loads                 | 20.0 us                                                         | 19.8 us: 1.01x faster                                               |
| pickle_dict                | 20.1 us                                                         | 20.0 us: 1.01x faster                                               |
| gc_traversal               | 1.38 ms                                                         | 1.40 ms: 1.02x slower                                               |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 17.4 sec: 1.02x slower                                              |
| pickle_list                | 3.27 us                                                         | 3.33 us: 1.02x slower                                               |
| regex_dna                  | 122 ms                                                          | 125 ms: 1.02x slower                                                |
| python_startup             | 22.0 ms                                                         | 22.7 ms: 1.03x slower                                               |
| async_generators           | 260 ms                                                          | 271 ms: 1.04x slower                                                |
| regex_effbot               | 1.82 ms                                                         | 1.92 ms: 1.05x slower                                               |
| unpickle                   | 9.23 us                                                         | 9.71 us: 1.05x slower                                               |
| create_gc_cycles           | 618 us                                                          | 651 us: 1.05x slower                                                |
| bench_mp_pool              | 70.9 ms                                                         | 74.9 ms: 1.06x slower                                               |
| telco                      | 5.29 ms                                                         | 5.62 ms: 1.06x slower                                               |
| regex_v8                   | 15.2 ms                                                         | 16.1 ms: 1.06x slower                                               |
| python_startup_no_site     | 18.8 ms                                                         | 20.5 ms: 1.09x slower                                               |
| pathlib                    | 79.9 ms                                                         | 88.6 ms: 1.11x slower                                               |
| sqlglot_normalize          | 113 ms                                                          | 197 ms: 1.74x slower                                                |
| coverage                   | 58.0 ms                                                         | 479 ms: 8.25x slower                                                |
| thrift                     | 801 us                                                          | 10.3 ms: 12.81x slower                                              |
| Geometric mean             | (ref)                                                           | 1.28x faster                                                        |

Benchmark hidden because not significant (1): flaskblogging
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.30x
- 95% likely to have a speedup of 1.29x
- 99% likely to have a speedup of 1.26x

# Memory
- memory change: unknown