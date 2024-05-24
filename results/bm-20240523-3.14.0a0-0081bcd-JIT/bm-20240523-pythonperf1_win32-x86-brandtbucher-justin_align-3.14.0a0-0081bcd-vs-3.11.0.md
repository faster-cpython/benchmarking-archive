# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_align
- machine: windows-x86
- commit hash: 0081bcd
- commit date: 2024-05-23
- overall geometric mean: 1.33x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf1_win32-x86-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 249 ms: 1.13x faster                                                         |
| chameleon      | 8.08 ms                                                         | 6.18 ms: 1.31x faster                                                        |
| docutils       | 2.10 sec                                                        | 1.90 sec: 1.10x faster                                                       |
| html5lib       | 54.3 ms                                                         | 46.0 ms: 1.18x faster                                                        |
| tornado_http   | 118 ms                                                          | 97.3 ms: 1.22x faster                                                        |
| Geometric mean | (ref)                                                           | 1.19x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf1_win32-x86-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 232 ms: 1.48x faster                                                         |
| async_tree_none_tg         | 301 ms                                                          | 207 ms: 1.46x faster                                                         |
| async_tree_memoization_tg  | 378 ms                                                          | 262 ms: 1.44x faster                                                         |
| async_tree_memoization     | 408 ms                                                          | 284 ms: 1.44x faster                                                         |
| async_tree_io_tg           | 746 ms                                                          | 536 ms: 1.39x faster                                                         |
| async_tree_io              | 754 ms                                                          | 545 ms: 1.38x faster                                                         |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 456 ms: 1.26x faster                                                         |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 478 ms: 1.24x faster                                                         |
| Geometric mean             | (ref)                                                           | 1.38x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf1_win32-x86-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 51.8 ms: 2.43x faster                                                        |
| float          | 76.1 ms                                                         | 40.9 ms: 1.86x faster                                                        |
| pidigits       | 203 ms                                                          | 198 ms: 1.02x faster                                                         |
| Geometric mean | (ref)                                                           | 1.67x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf1_win32-x86-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 96.3 ms: 1.53x faster                                                        |
| regex_dna      | 122 ms                                                          | 119 ms: 1.02x faster                                                         |
| regex_effbot   | 1.82 ms                                                         | 1.88 ms: 1.03x slower                                                        |
| regex_v8       | 15.2 ms                                                         | 15.7 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                           | 1.10x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf1_win32-x86-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.31 sec                                                        | 1.37 sec: 1.69x faster                                                       |
| unpickle_pure_python | 231 us                                                          | 137 us: 1.69x faster                                                         |
| pickle_pure_python   | 309 us                                                          | 204 us: 1.52x faster                                                         |
| json_dumps           | 9.80 ms                                                         | 6.63 ms: 1.48x faster                                                        |
| xml_etree_process    | 55.0 ms                                                         | 42.6 ms: 1.29x faster                                                        |
| xml_etree_iterparse  | 75.6 ms                                                         | 59.9 ms: 1.26x faster                                                        |
| xml_etree_generate   | 71.6 ms                                                         | 58.0 ms: 1.23x faster                                                        |
| unpickle_list        | 3.28 us                                                         | 2.85 us: 1.15x faster                                                        |
| xml_etree_parse      | 114 ms                                                          | 102 ms: 1.12x faster                                                         |
| pickle_dict          | 20.1 us                                                         | 20.7 us: 1.03x slower                                                        |
| json_loads           | 20.0 us                                                         | 21.0 us: 1.05x slower                                                        |
| unpickle             | 9.23 us                                                         | 10.0 us: 1.09x slower                                                        |
| pickle_list          | 3.27 us                                                         | 3.60 us: 1.10x slower                                                        |
| pickle               | 7.99 us                                                         | 9.05 us: 1.13x slower                                                        |
| Geometric mean       | (ref)                                                           | 1.19x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf1_win32-x86-brandtbucher-justin_align-3.14.0a0-0081bcd |
|------------------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 20.5 ms: 1.09x slower                                                        |
| python_startup         | 22.0 ms                                                         | 24.3 ms: 1.11x slower                                                        |
| Geometric mean         | (ref)                                                           | 1.10x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf1_win32-x86-brandtbucher-justin_align-3.14.0a0-0081bcd |
|-----------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 5.38 ms: 1.91x faster                                                        |
| genshi_text     | 26.8 ms                                                         | 21.4 ms: 1.25x faster                                                        |
| genshi_xml      | 61.2 ms                                                         | 50.5 ms: 1.21x faster                                                        |
| django_template | 37.4 ms                                                         | 31.7 ms: 1.18x faster                                                        |
| Geometric mean  | (ref)                                                           | 1.36x faster                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240523-pythonperf1_win32-x86-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 137 us: 3.50x faster                                                         |
| spectral_norm              | 122 ms                                                          | 47.9 ms: 2.54x faster                                                        |
| nbody                      | 126 ms                                                          | 51.8 ms: 2.43x faster                                                        |
| generators                 | 52.2 ms                                                         | 23.4 ms: 2.23x faster                                                        |
| logging_silent             | 119 ns                                                          | 55.0 ns: 2.17x faster                                                        |
| comprehensions             | 22.1 us                                                         | 11.0 us: 2.01x faster                                                        |
| deepcopy_memo              | 40.0 us                                                         | 20.6 us: 1.94x faster                                                        |
| mako                       | 10.3 ms                                                         | 5.38 ms: 1.91x faster                                                        |
| float                      | 76.1 ms                                                         | 40.9 ms: 1.86x faster                                                        |
| fannkuch                   | 399 ms                                                          | 215 ms: 1.86x faster                                                         |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.37 ms: 1.79x faster                                                        |
| scimark_fft                | 291 ms                                                          | 167 ms: 1.74x faster                                                         |
| pylint                     | 418 ms                                                          | 241 ms: 1.73x faster                                                         |
| scimark_monte_carlo        | 70.8 ms                                                         | 41.2 ms: 1.72x faster                                                        |
| pyflate                    | 471 ms                                                          | 278 ms: 1.70x faster                                                         |
| tomli_loads                | 2.31 sec                                                        | 1.37 sec: 1.69x faster                                                       |
| chaos                      | 84.4 ms                                                         | 49.8 ms: 1.69x faster                                                        |
| unpickle_pure_python       | 231 us                                                          | 137 us: 1.69x faster                                                         |
| hexiom                     | 7.51 ms                                                         | 4.45 ms: 1.69x faster                                                        |
| richards_super             | 58.7 ms                                                         | 35.5 ms: 1.66x faster                                                        |
| nqueens                    | 111 ms                                                          | 67.5 ms: 1.65x faster                                                        |
| raytrace                   | 327 ms                                                          | 202 ms: 1.62x faster                                                         |
| sqlglot_parse              | 1.49 ms                                                         | 922 us: 1.62x faster                                                         |
| deltablue                  | 4.10 ms                                                         | 2.55 ms: 1.60x faster                                                        |
| crypto_pyaes               | 79.4 ms                                                         | 49.6 ms: 1.60x faster                                                        |
| richards                   | 48.8 ms                                                         | 30.7 ms: 1.59x faster                                                        |
| regex_compile              | 148 ms                                                          | 96.3 ms: 1.53x faster                                                        |
| pickle_pure_python         | 309 us                                                          | 204 us: 1.52x faster                                                         |
| scimark_sor                | 135 ms                                                          | 89.4 ms: 1.51x faster                                                        |
| pprint_safe_repr           | 819 ms                                                          | 542 ms: 1.51x faster                                                         |
| sqlglot_transpile          | 1.78 ms                                                         | 1.19 ms: 1.50x faster                                                        |
| pprint_pformat             | 1.70 sec                                                        | 1.13 sec: 1.50x faster                                                       |
| json_dumps                 | 9.80 ms                                                         | 6.63 ms: 1.48x faster                                                        |
| async_tree_none            | 343 ms                                                          | 232 ms: 1.48x faster                                                         |
| coroutines                 | 23.7 ms                                                         | 16.2 ms: 1.46x faster                                                        |
| async_tree_none_tg         | 301 ms                                                          | 207 ms: 1.46x faster                                                         |
| scimark_lu                 | 102 ms                                                          | 70.6 ms: 1.45x faster                                                        |
| async_tree_memoization_tg  | 378 ms                                                          | 262 ms: 1.44x faster                                                         |
| async_tree_memoization     | 408 ms                                                          | 284 ms: 1.44x faster                                                         |
| logging_simple             | 10.8 us                                                         | 7.54 us: 1.43x faster                                                        |
| logging_format             | 11.5 us                                                         | 8.07 us: 1.42x faster                                                        |
| async_tree_io_tg           | 746 ms                                                          | 536 ms: 1.39x faster                                                         |
| async_tree_io              | 754 ms                                                          | 545 ms: 1.38x faster                                                         |
| sympy_sum                  | 149 ms                                                          | 108 ms: 1.37x faster                                                         |
| go                         | 147 ms                                                          | 108 ms: 1.36x faster                                                         |
| sympy_str                  | 283 ms                                                          | 212 ms: 1.34x faster                                                         |
| chameleon                  | 8.08 ms                                                         | 6.18 ms: 1.31x faster                                                        |
| pycparser                  | 1.04 sec                                                        | 804 ms: 1.30x faster                                                         |
| xml_etree_process          | 55.0 ms                                                         | 42.6 ms: 1.29x faster                                                        |
| mdp                        | 2.07 sec                                                        | 1.60 sec: 1.29x faster                                                       |
| sympy_integrate            | 19.9 ms                                                         | 15.7 ms: 1.27x faster                                                        |
| deepcopy                   | 381 us                                                          | 300 us: 1.27x faster                                                         |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 456 ms: 1.26x faster                                                         |
| xml_etree_iterparse        | 75.6 ms                                                         | 59.9 ms: 1.26x faster                                                        |
| genshi_text                | 26.8 ms                                                         | 21.4 ms: 1.25x faster                                                        |
| asyncio_tcp                | 787 ms                                                          | 634 ms: 1.24x faster                                                         |
| meteor_contest             | 90.9 ms                                                         | 73.5 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 478 ms: 1.24x faster                                                         |
| xml_etree_generate         | 71.6 ms                                                         | 58.0 ms: 1.23x faster                                                        |
| sympy_expand               | 462 ms                                                          | 376 ms: 1.23x faster                                                         |
| sqlglot_optimize           | 51.8 ms                                                         | 42.3 ms: 1.23x faster                                                        |
| tornado_http               | 118 ms                                                          | 97.3 ms: 1.22x faster                                                        |
| genshi_xml                 | 61.2 ms                                                         | 50.5 ms: 1.21x faster                                                        |
| deepcopy_reduce            | 3.32 us                                                         | 2.75 us: 1.20x faster                                                        |
| django_template            | 37.4 ms                                                         | 31.7 ms: 1.18x faster                                                        |
| html5lib                   | 54.3 ms                                                         | 46.0 ms: 1.18x faster                                                        |
| sqlite_synth               | 2.15 us                                                         | 1.85 us: 1.16x faster                                                        |
| coverage                   | 58.0 ms                                                         | 50.3 ms: 1.15x faster                                                        |
| unpickle_list              | 3.28 us                                                         | 2.85 us: 1.15x faster                                                        |
| 2to3                       | 282 ms                                                          | 249 ms: 1.13x faster                                                         |
| bench_thread_pool          | 1.14 ms                                                         | 1.01 ms: 1.13x faster                                                        |
| thrift                     | 801 us                                                          | 714 us: 1.12x faster                                                         |
| xml_etree_parse            | 114 ms                                                          | 102 ms: 1.12x faster                                                         |
| json                       | 4.78 ms                                                         | 4.30 ms: 1.11x faster                                                        |
| docutils                   | 2.10 sec                                                        | 1.90 sec: 1.10x faster                                                       |
| pidigits                   | 203 ms                                                          | 198 ms: 1.02x faster                                                         |
| regex_dna                  | 122 ms                                                          | 119 ms: 1.02x faster                                                         |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.9 sec: 1.01x faster                                                       |
| pickle_dict                | 20.1 us                                                         | 20.7 us: 1.03x slower                                                        |
| regex_effbot               | 1.82 ms                                                         | 1.88 ms: 1.03x slower                                                        |
| regex_v8                   | 15.2 ms                                                         | 15.7 ms: 1.03x slower                                                        |
| json_loads                 | 20.0 us                                                         | 21.0 us: 1.05x slower                                                        |
| gc_traversal               | 1.38 ms                                                         | 1.45 ms: 1.05x slower                                                        |
| bench_mp_pool              | 70.9 ms                                                         | 74.8 ms: 1.05x slower                                                        |
| telco                      | 5.29 ms                                                         | 5.63 ms: 1.06x slower                                                        |
| pathlib                    | 79.9 ms                                                         | 86.4 ms: 1.08x slower                                                        |
| unpickle                   | 9.23 us                                                         | 10.0 us: 1.09x slower                                                        |
| python_startup_no_site     | 18.8 ms                                                         | 20.5 ms: 1.09x slower                                                        |
| pickle_list                | 3.27 us                                                         | 3.60 us: 1.10x slower                                                        |
| python_startup             | 22.0 ms                                                         | 24.3 ms: 1.11x slower                                                        |
| async_generators           | 260 ms                                                          | 291 ms: 1.12x slower                                                         |
| pickle                     | 7.99 us                                                         | 9.05 us: 1.13x slower                                                        |
| create_gc_cycles           | 618 us                                                          | 764 us: 1.24x slower                                                         |
| sqlglot_normalize          | 113 ms                                                          | 221 ms: 1.95x slower                                                         |
| Geometric mean             | (ref)                                                           | 1.33x faster                                                                 |

Benchmark hidden because not significant (1): flaskblogging
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.29x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: unknown