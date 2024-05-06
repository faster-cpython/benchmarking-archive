# Results vs. 3.11.0

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: windows-x86
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.30x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.31x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 231 ms: 1.22x faster                                                            |
| chameleon      | 8.08 ms                                                         | 5.57 ms: 1.45x faster                                                           |
| docutils       | 2.10 sec                                                        | 1.77 sec: 1.18x faster                                                          |
| html5lib       | 54.3 ms                                                         | 42.8 ms: 1.27x faster                                                           |
| tornado_http   | 118 ms                                                          | 94.4 ms: 1.25x faster                                                           |
| Geometric mean | (ref)                                                           | 1.27x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 213 ms: 1.61x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 262 ms: 1.56x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 196 ms: 1.53x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 250 ms: 1.51x faster                                                            |
| async_tree_io              | 754 ms                                                          | 515 ms: 1.46x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 524 ms: 1.42x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 447 ms: 1.32x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 439 ms: 1.31x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.46x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 74.3 ms: 1.70x faster                                                           |
| float          | 76.1 ms                                                         | 51.3 ms: 1.48x faster                                                           |
| pidigits       | 203 ms                                                          | 200 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                           | 1.37x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 95.0 ms: 1.55x faster                                                           |
| regex_effbot   | 1.82 ms                                                         | 1.91 ms: 1.05x slower                                                           |
| regex_v8       | 15.2 ms                                                         | 16.1 ms: 1.06x slower                                                           |
| regex_dna      | 122 ms                                                          | 131 ms: 1.08x slower                                                            |
| Geometric mean | (ref)                                                           | 1.07x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 139 us: 1.66x faster                                                            |
| pickle_pure_python   | 309 us                                                          | 202 us: 1.53x faster                                                            |
| tomli_loads          | 2.31 sec                                                        | 1.60 sec: 1.45x faster                                                          |
| json_dumps           | 9.80 ms                                                         | 6.79 ms: 1.44x faster                                                           |
| xml_etree_process    | 55.0 ms                                                         | 42.9 ms: 1.28x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 57.9 ms: 1.24x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 64.0 ms: 1.18x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 2.87 us: 1.14x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 105 ms: 1.08x faster                                                            |
| pickle               | 7.99 us                                                         | 7.87 us: 1.01x faster                                                           |
| pickle_list          | 3.27 us                                                         | 3.22 us: 1.01x faster                                                           |
| json_loads           | 20.0 us                                                         | 20.3 us: 1.01x slower                                                           |
| unpickle             | 9.23 us                                                         | 9.93 us: 1.08x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.19x faster                                                                    |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                         | 22.2 ms: 1.01x slower                                                           |
| python_startup_no_site | 18.8 ms                                                         | 19.8 ms: 1.05x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.03x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 6.89 ms: 1.49x faster                                                           |
| genshi_text     | 26.8 ms                                                         | 18.8 ms: 1.43x faster                                                           |
| genshi_xml      | 61.2 ms                                                         | 43.2 ms: 1.42x faster                                                           |
| django_template | 37.4 ms                                                         | 28.8 ms: 1.30x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.41x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 90.5 us: 5.29x faster                                                           |
| generators                 | 52.2 ms                                                         | 22.3 ms: 2.34x faster                                                           |
| logging_silent             | 119 ns                                                          | 57.2 ns: 2.08x faster                                                           |
| pylint                     | 418 ms                                                          | 204 ms: 2.05x faster                                                            |
| comprehensions             | 22.1 us                                                         | 11.2 us: 1.97x faster                                                           |
| deltablue                  | 4.10 ms                                                         | 2.15 ms: 1.91x faster                                                           |
| spectral_norm              | 122 ms                                                          | 66.3 ms: 1.84x faster                                                           |
| richards_super             | 58.7 ms                                                         | 32.2 ms: 1.82x faster                                                           |
| deepcopy_memo              | 40.0 us                                                         | 22.0 us: 1.82x faster                                                           |
| chaos                      | 84.4 ms                                                         | 46.5 ms: 1.82x faster                                                           |
| hexiom                     | 7.51 ms                                                         | 4.18 ms: 1.80x faster                                                           |
| raytrace                   | 327 ms                                                          | 184 ms: 1.78x faster                                                            |
| unpack_sequence            | 65.2 ns                                                         | 36.9 ns: 1.77x faster                                                           |
| richards                   | 48.8 ms                                                         | 28.1 ms: 1.74x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 860 us: 1.73x faster                                                            |
| scimark_sor                | 135 ms                                                          | 78.5 ms: 1.72x faster                                                           |
| coroutines                 | 23.7 ms                                                         | 13.9 ms: 1.70x faster                                                           |
| nbody                      | 126 ms                                                          | 74.3 ms: 1.70x faster                                                           |
| nqueens                    | 111 ms                                                          | 66.0 ms: 1.69x faster                                                           |
| unpickle_pure_python       | 231 us                                                          | 139 us: 1.66x faster                                                            |
| scimark_lu                 | 102 ms                                                          | 61.7 ms: 1.66x faster                                                           |
| sqlglot_transpile          | 1.78 ms                                                         | 1.09 ms: 1.64x faster                                                           |
| async_tree_none            | 343 ms                                                          | 213 ms: 1.61x faster                                                            |
| scimark_monte_carlo        | 70.8 ms                                                         | 44.7 ms: 1.58x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 262 ms: 1.56x faster                                                            |
| regex_compile              | 148 ms                                                          | 95.0 ms: 1.55x faster                                                           |
| pyflate                    | 471 ms                                                          | 308 ms: 1.53x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 196 ms: 1.53x faster                                                            |
| pickle_pure_python         | 309 us                                                          | 202 us: 1.53x faster                                                            |
| go                         | 147 ms                                                          | 96.6 ms: 1.52x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 250 ms: 1.51x faster                                                            |
| mako                       | 10.3 ms                                                         | 6.89 ms: 1.49x faster                                                           |
| pprint_pformat             | 1.70 sec                                                        | 1.14 sec: 1.48x faster                                                          |
| float                      | 76.1 ms                                                         | 51.3 ms: 1.48x faster                                                           |
| fannkuch                   | 399 ms                                                          | 270 ms: 1.48x faster                                                            |
| sympy_sum                  | 149 ms                                                          | 101 ms: 1.48x faster                                                            |
| crypto_pyaes               | 79.4 ms                                                         | 54.1 ms: 1.47x faster                                                           |
| async_tree_io              | 754 ms                                                          | 515 ms: 1.46x faster                                                            |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.89 ms: 1.46x faster                                                           |
| pprint_safe_repr           | 819 ms                                                          | 562 ms: 1.46x faster                                                            |
| chameleon                  | 8.08 ms                                                         | 5.57 ms: 1.45x faster                                                           |
| logging_simple             | 10.8 us                                                         | 7.47 us: 1.45x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.60 sec: 1.45x faster                                                          |
| sympy_str                  | 283 ms                                                          | 196 ms: 1.44x faster                                                            |
| json_dumps                 | 9.80 ms                                                         | 6.79 ms: 1.44x faster                                                           |
| deepcopy                   | 381 us                                                          | 266 us: 1.43x faster                                                            |
| genshi_text                | 26.8 ms                                                         | 18.8 ms: 1.43x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 524 ms: 1.42x faster                                                            |
| sympy_integrate            | 19.9 ms                                                         | 14.0 ms: 1.42x faster                                                           |
| genshi_xml                 | 61.2 ms                                                         | 43.2 ms: 1.42x faster                                                           |
| logging_format             | 11.5 us                                                         | 8.12 us: 1.41x faster                                                           |
| deepcopy_reduce            | 3.32 us                                                         | 2.36 us: 1.40x faster                                                           |
| scimark_fft                | 291 ms                                                          | 210 ms: 1.38x faster                                                            |
| sqlglot_optimize           | 51.8 ms                                                         | 38.3 ms: 1.35x faster                                                           |
| pycparser                  | 1.04 sec                                                        | 772 ms: 1.35x faster                                                            |
| sympy_expand               | 462 ms                                                          | 345 ms: 1.34x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 447 ms: 1.32x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 439 ms: 1.31x faster                                                            |
| mdp                        | 2.07 sec                                                        | 1.57 sec: 1.31x faster                                                          |
| django_template            | 37.4 ms                                                         | 28.8 ms: 1.30x faster                                                           |
| xml_etree_process          | 55.0 ms                                                         | 42.9 ms: 1.28x faster                                                           |
| html5lib                   | 54.3 ms                                                         | 42.8 ms: 1.27x faster                                                           |
| asyncio_tcp                | 787 ms                                                          | 623 ms: 1.26x faster                                                            |
| tornado_http               | 118 ms                                                          | 94.4 ms: 1.25x faster                                                           |
| xml_etree_generate         | 71.6 ms                                                         | 57.9 ms: 1.24x faster                                                           |
| meteor_contest             | 90.9 ms                                                         | 74.0 ms: 1.23x faster                                                           |
| 2to3                       | 282 ms                                                          | 231 ms: 1.22x faster                                                            |
| docutils                   | 2.10 sec                                                        | 1.77 sec: 1.18x faster                                                          |
| xml_etree_iterparse        | 75.6 ms                                                         | 64.0 ms: 1.18x faster                                                           |
| bench_thread_pool          | 1.14 ms                                                         | 983 us: 1.16x faster                                                            |
| json                       | 4.78 ms                                                         | 4.17 ms: 1.15x faster                                                           |
| unpickle_list              | 3.28 us                                                         | 2.87 us: 1.14x faster                                                           |
| sqlite_synth               | 2.15 us                                                         | 1.93 us: 1.11x faster                                                           |
| xml_etree_parse            | 114 ms                                                          | 105 ms: 1.08x faster                                                            |
| bench_mp_pool              | 70.9 ms                                                         | 68.0 ms: 1.04x faster                                                           |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.7 sec: 1.02x faster                                                          |
| pidigits                   | 203 ms                                                          | 200 ms: 1.02x faster                                                            |
| pickle                     | 7.99 us                                                         | 7.87 us: 1.01x faster                                                           |
| pickle_list                | 3.27 us                                                         | 3.22 us: 1.01x faster                                                           |
| python_startup             | 22.0 ms                                                         | 22.2 ms: 1.01x slower                                                           |
| json_loads                 | 20.0 us                                                         | 20.3 us: 1.01x slower                                                           |
| gc_traversal               | 1.38 ms                                                         | 1.43 ms: 1.04x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.91 ms: 1.05x slower                                                           |
| python_startup_no_site     | 18.8 ms                                                         | 19.8 ms: 1.05x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 16.1 ms: 1.06x slower                                                           |
| unpickle                   | 9.23 us                                                         | 9.93 us: 1.08x slower                                                           |
| regex_dna                  | 122 ms                                                          | 131 ms: 1.08x slower                                                            |
| pathlib                    | 79.9 ms                                                         | 86.4 ms: 1.08x slower                                                           |
| async_generators           | 260 ms                                                          | 286 ms: 1.10x slower                                                            |
| telco                      | 5.29 ms                                                         | 5.86 ms: 1.11x slower                                                           |
| create_gc_cycles           | 618 us                                                          | 726 us: 1.18x slower                                                            |
| sqlglot_normalize          | 113 ms                                                          | 200 ms: 1.77x slower                                                            |
| coverage                   | 58.0 ms                                                         | 470 ms: 8.10x slower                                                            |
| thrift                     | 801 us                                                          | 9.91 ms: 12.38x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.30x faster                                                                    |

Benchmark hidden because not significant (1): pickle_dict
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.34x
- 95% likely to have a speedup of 1.34x
- 99% likely to have a speedup of 1.31x

# Memory
- memory change: unknown