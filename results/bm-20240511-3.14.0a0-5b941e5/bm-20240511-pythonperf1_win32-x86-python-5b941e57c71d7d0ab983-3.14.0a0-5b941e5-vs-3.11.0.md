# Results vs. 3.11.0

- fork: python
- ref: 5b941e57c71d7d0ab983
- machine: windows-x86
- commit hash: 5b941e5
- commit date: 2024-05-11
- overall geometric mean: 1.32x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 234 ms: 1.21x faster                                                           |
| chameleon      | 8.08 ms                                                         | 5.83 ms: 1.38x faster                                                          |
| docutils       | 2.10 sec                                                        | 1.81 sec: 1.16x faster                                                         |
| html5lib       | 54.3 ms                                                         | 44.8 ms: 1.21x faster                                                          |
| tornado_http   | 118 ms                                                          | 94.6 ms: 1.25x faster                                                          |
| Geometric mean | (ref)                                                           | 1.24x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 228 ms: 1.50x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 202 ms: 1.49x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 255 ms: 1.48x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 277 ms: 1.48x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 530 ms: 1.41x faster                                                           |
| async_tree_io              | 754 ms                                                          | 538 ms: 1.40x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 450 ms: 1.28x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 470 ms: 1.26x faster                                                           |
| Geometric mean             | (ref)                                                           | 1.41x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 75.0 ms: 1.68x faster                                                          |
| float          | 76.1 ms                                                         | 52.0 ms: 1.46x faster                                                          |
| pidigits       | 203 ms                                                          | 199 ms: 1.02x faster                                                           |
| Geometric mean | (ref)                                                           | 1.36x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 97.3 ms: 1.52x faster                                                          |
| regex_dna      | 122 ms                                                          | 120 ms: 1.01x faster                                                           |
| regex_effbot   | 1.82 ms                                                         | 1.92 ms: 1.05x slower                                                          |
| regex_v8       | 15.2 ms                                                         | 16.2 ms: 1.07x slower                                                          |
| Geometric mean | (ref)                                                           | 1.08x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 147 us: 1.57x faster                                                           |
| pickle_pure_python   | 309 us                                                          | 212 us: 1.46x faster                                                           |
| json_dumps           | 9.80 ms                                                         | 6.79 ms: 1.44x faster                                                          |
| tomli_loads          | 2.31 sec                                                        | 1.63 sec: 1.42x faster                                                         |
| xml_etree_process    | 55.0 ms                                                         | 41.7 ms: 1.32x faster                                                          |
| xml_etree_generate   | 71.6 ms                                                         | 58.1 ms: 1.23x faster                                                          |
| xml_etree_iterparse  | 75.6 ms                                                         | 63.9 ms: 1.18x faster                                                          |
| xml_etree_parse      | 114 ms                                                          | 105 ms: 1.09x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 3.00 us: 1.09x faster                                                          |
| pickle               | 7.99 us                                                         | 7.92 us: 1.01x faster                                                          |
| json_loads           | 20.0 us                                                         | 20.3 us: 1.01x slower                                                          |
| pickle_dict          | 20.1 us                                                         | 20.6 us: 1.02x slower                                                          |
| pickle_list          | 3.27 us                                                         | 3.45 us: 1.06x slower                                                          |
| unpickle             | 9.23 us                                                         | 9.98 us: 1.08x slower                                                          |
| Geometric mean       | (ref)                                                           | 1.17x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 18.4 ms: 1.02x faster                                                          |
| Geometric mean         | (ref)                                                           | 1.01x faster                                                                   |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|-----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 6.85 ms: 1.50x faster                                                          |
| genshi_xml      | 61.2 ms                                                         | 45.1 ms: 1.36x faster                                                          |
| genshi_text     | 26.8 ms                                                         | 20.1 ms: 1.33x faster                                                          |
| django_template | 37.4 ms                                                         | 30.1 ms: 1.24x faster                                                          |
| Geometric mean  | (ref)                                                           | 1.36x faster                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 133 us: 3.61x faster                                                           |
| generators                 | 52.2 ms                                                         | 21.3 ms: 2.45x faster                                                          |
| logging_silent             | 119 ns                                                          | 58.2 ns: 2.05x faster                                                          |
| pylint                     | 418 ms                                                          | 219 ms: 1.91x faster                                                           |
| deltablue                  | 4.10 ms                                                         | 2.20 ms: 1.86x faster                                                          |
| comprehensions             | 22.1 us                                                         | 11.9 us: 1.85x faster                                                          |
| spectral_norm              | 122 ms                                                          | 67.9 ms: 1.79x faster                                                          |
| chaos                      | 84.4 ms                                                         | 47.3 ms: 1.79x faster                                                          |
| raytrace                   | 327 ms                                                          | 184 ms: 1.78x faster                                                           |
| hexiom                     | 7.51 ms                                                         | 4.28 ms: 1.76x faster                                                          |
| scimark_lu                 | 102 ms                                                          | 59.9 ms: 1.71x faster                                                          |
| deepcopy_memo              | 40.0 us                                                         | 23.5 us: 1.70x faster                                                          |
| nbody                      | 126 ms                                                          | 75.0 ms: 1.68x faster                                                          |
| richards_super             | 58.7 ms                                                         | 35.1 ms: 1.67x faster                                                          |
| nqueens                    | 111 ms                                                          | 68.2 ms: 1.63x faster                                                          |
| unpickle_pure_python       | 231 us                                                          | 147 us: 1.57x faster                                                           |
| scimark_sor                | 135 ms                                                          | 86.2 ms: 1.57x faster                                                          |
| richards                   | 48.8 ms                                                         | 31.2 ms: 1.56x faster                                                          |
| sqlglot_parse              | 1.49 ms                                                         | 958 us: 1.56x faster                                                           |
| pyflate                    | 471 ms                                                          | 304 ms: 1.55x faster                                                           |
| regex_compile              | 148 ms                                                          | 97.3 ms: 1.52x faster                                                          |
| scimark_monte_carlo        | 70.8 ms                                                         | 46.9 ms: 1.51x faster                                                          |
| async_tree_none            | 343 ms                                                          | 228 ms: 1.50x faster                                                           |
| mako                       | 10.3 ms                                                         | 6.85 ms: 1.50x faster                                                          |
| fannkuch                   | 399 ms                                                          | 266 ms: 1.50x faster                                                           |
| sqlglot_transpile          | 1.78 ms                                                         | 1.19 ms: 1.50x faster                                                          |
| async_tree_none_tg         | 301 ms                                                          | 202 ms: 1.49x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 255 ms: 1.48x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 277 ms: 1.48x faster                                                           |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.87 ms: 1.47x faster                                                          |
| coroutines                 | 23.7 ms                                                         | 16.1 ms: 1.47x faster                                                          |
| float                      | 76.1 ms                                                         | 52.0 ms: 1.46x faster                                                          |
| pickle_pure_python         | 309 us                                                          | 212 us: 1.46x faster                                                           |
| logging_simple             | 10.8 us                                                         | 7.44 us: 1.45x faster                                                          |
| json_dumps                 | 9.80 ms                                                         | 6.79 ms: 1.44x faster                                                          |
| go                         | 147 ms                                                          | 102 ms: 1.44x faster                                                           |
| crypto_pyaes               | 79.4 ms                                                         | 55.4 ms: 1.43x faster                                                          |
| sympy_sum                  | 149 ms                                                          | 104 ms: 1.43x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.63 sec: 1.42x faster                                                         |
| logging_format             | 11.5 us                                                         | 8.08 us: 1.42x faster                                                          |
| scimark_fft                | 291 ms                                                          | 206 ms: 1.41x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 530 ms: 1.41x faster                                                           |
| async_tree_io              | 754 ms                                                          | 538 ms: 1.40x faster                                                           |
| chameleon                  | 8.08 ms                                                         | 5.83 ms: 1.38x faster                                                          |
| sympy_integrate            | 19.9 ms                                                         | 14.4 ms: 1.38x faster                                                          |
| deepcopy                   | 381 us                                                          | 277 us: 1.38x faster                                                           |
| sympy_str                  | 283 ms                                                          | 206 ms: 1.37x faster                                                           |
| pprint_pformat             | 1.70 sec                                                        | 1.24 sec: 1.37x faster                                                         |
| genshi_xml                 | 61.2 ms                                                         | 45.1 ms: 1.36x faster                                                          |
| pprint_safe_repr           | 819 ms                                                          | 604 ms: 1.36x faster                                                           |
| pycparser                  | 1.04 sec                                                        | 782 ms: 1.33x faster                                                           |
| genshi_text                | 26.8 ms                                                         | 20.1 ms: 1.33x faster                                                          |
| xml_etree_process          | 55.0 ms                                                         | 41.7 ms: 1.32x faster                                                          |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 450 ms: 1.28x faster                                                           |
| sympy_expand               | 462 ms                                                          | 364 ms: 1.27x faster                                                           |
| mdp                        | 2.07 sec                                                        | 1.64 sec: 1.26x faster                                                         |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 470 ms: 1.26x faster                                                           |
| tornado_http               | 118 ms                                                          | 94.6 ms: 1.25x faster                                                          |
| deepcopy_reduce            | 3.32 us                                                         | 2.67 us: 1.24x faster                                                          |
| django_template            | 37.4 ms                                                         | 30.1 ms: 1.24x faster                                                          |
| sqlglot_optimize           | 51.8 ms                                                         | 41.9 ms: 1.24x faster                                                          |
| xml_etree_generate         | 71.6 ms                                                         | 58.1 ms: 1.23x faster                                                          |
| meteor_contest             | 90.9 ms                                                         | 74.8 ms: 1.21x faster                                                          |
| html5lib                   | 54.3 ms                                                         | 44.8 ms: 1.21x faster                                                          |
| 2to3                       | 282 ms                                                          | 234 ms: 1.21x faster                                                           |
| coverage                   | 58.0 ms                                                         | 48.7 ms: 1.19x faster                                                          |
| xml_etree_iterparse        | 75.6 ms                                                         | 63.9 ms: 1.18x faster                                                          |
| docutils                   | 2.10 sec                                                        | 1.81 sec: 1.16x faster                                                         |
| json                       | 4.78 ms                                                         | 4.15 ms: 1.15x faster                                                          |
| bench_thread_pool          | 1.14 ms                                                         | 1000 us: 1.14x faster                                                          |
| thrift                     | 801 us                                                          | 706 us: 1.13x faster                                                           |
| asyncio_tcp                | 787 ms                                                          | 694 ms: 1.13x faster                                                           |
| sqlite_synth               | 2.15 us                                                         | 1.94 us: 1.11x faster                                                          |
| xml_etree_parse            | 114 ms                                                          | 105 ms: 1.09x faster                                                           |
| unpickle_list              | 3.28 us                                                         | 3.00 us: 1.09x faster                                                          |
| python_startup_no_site     | 18.8 ms                                                         | 18.4 ms: 1.02x faster                                                          |
| pidigits                   | 203 ms                                                          | 199 ms: 1.02x faster                                                           |
| regex_dna                  | 122 ms                                                          | 120 ms: 1.01x faster                                                           |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.9 sec: 1.01x faster                                                         |
| pickle                     | 7.99 us                                                         | 7.92 us: 1.01x faster                                                          |
| bench_mp_pool              | 70.9 ms                                                         | 70.6 ms: 1.00x faster                                                          |
| json_loads                 | 20.0 us                                                         | 20.3 us: 1.01x slower                                                          |
| pickle_dict                | 20.1 us                                                         | 20.6 us: 1.02x slower                                                          |
| gc_traversal               | 1.38 ms                                                         | 1.43 ms: 1.04x slower                                                          |
| regex_effbot               | 1.82 ms                                                         | 1.92 ms: 1.05x slower                                                          |
| pickle_list                | 3.27 us                                                         | 3.45 us: 1.06x slower                                                          |
| regex_v8                   | 15.2 ms                                                         | 16.2 ms: 1.07x slower                                                          |
| async_generators           | 260 ms                                                          | 279 ms: 1.07x slower                                                           |
| unpickle                   | 9.23 us                                                         | 9.98 us: 1.08x slower                                                          |
| telco                      | 5.29 ms                                                         | 5.78 ms: 1.09x slower                                                          |
| pathlib                    | 79.9 ms                                                         | 88.5 ms: 1.11x slower                                                          |
| create_gc_cycles           | 618 us                                                          | 745 us: 1.21x slower                                                           |
| sqlglot_normalize          | 113 ms                                                          | 211 ms: 1.86x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.32x faster                                                                   |

Benchmark hidden because not significant (2): flaskblogging, python_startup
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.31x
- 95% likely to have a speedup of 1.29x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: unknown