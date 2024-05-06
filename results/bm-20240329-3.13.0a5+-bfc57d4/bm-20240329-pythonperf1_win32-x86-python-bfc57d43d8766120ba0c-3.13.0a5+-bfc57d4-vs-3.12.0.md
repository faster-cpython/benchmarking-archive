# Results vs. 3.12.0

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: windows-x86
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.22x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.21x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 231 ms: 1.21x faster                                                            |
| chameleon      | 7.75 ms                                                         | 5.57 ms: 1.39x faster                                                           |
| docutils       | 1.98 sec                                                        | 1.77 sec: 1.12x faster                                                          |
| tornado_http   | 105 ms                                                          | 94.4 ms: 1.11x faster                                                           |
| Geometric mean | (ref)                                                           | 1.20x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none_tg         | 278 ms                                                          | 196 ms: 1.41x faster                                                            |
| async_tree_none            | 298 ms                                                          | 213 ms: 1.40x faster                                                            |
| async_tree_memoization_tg  | 350 ms                                                          | 250 ms: 1.40x faster                                                            |
| async_tree_memoization     | 364 ms                                                          | 262 ms: 1.39x faster                                                            |
| async_tree_io              | 693 ms                                                          | 515 ms: 1.35x faster                                                            |
| async_tree_io_tg           | 677 ms                                                          | 524 ms: 1.29x faster                                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 447 ms: 1.26x faster                                                            |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 439 ms: 1.24x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.34x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 127 ms                                                          | 74.3 ms: 1.71x faster                                                           |
| float          | 76.7 ms                                                         | 51.3 ms: 1.50x faster                                                           |
| Geometric mean | (ref)                                                           | 1.37x faster                                                                    |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 95.0 ms: 1.36x faster                                                           |
| regex_effbot   | 2.04 ms                                                         | 1.91 ms: 1.07x faster                                                           |
| regex_dna      | 127 ms                                                          | 131 ms: 1.03x slower                                                            |
| regex_v8       | 15.0 ms                                                         | 16.1 ms: 1.07x slower                                                           |
| Geometric mean | (ref)                                                           | 1.07x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 210 us                                                          | 139 us: 1.51x faster                                                            |
| pickle_pure_python   | 286 us                                                          | 202 us: 1.41x faster                                                            |
| tomli_loads          | 2.20 sec                                                        | 1.60 sec: 1.37x faster                                                          |
| xml_etree_generate   | 72.1 ms                                                         | 57.9 ms: 1.25x faster                                                           |
| xml_etree_process    | 53.2 ms                                                         | 42.9 ms: 1.24x faster                                                           |
| xml_etree_iterparse  | 77.6 ms                                                         | 64.0 ms: 1.21x faster                                                           |
| json_dumps           | 7.40 ms                                                         | 6.79 ms: 1.09x faster                                                           |
| xml_etree_parse      | 113 ms                                                          | 105 ms: 1.07x faster                                                            |
| pickle_list          | 3.37 us                                                         | 3.22 us: 1.05x faster                                                           |
| unpickle_list        | 2.95 us                                                         | 2.87 us: 1.03x faster                                                           |
| pickle               | 7.79 us                                                         | 7.87 us: 1.01x slower                                                           |
| pickle_dict          | 19.9 us                                                         | 20.2 us: 1.01x slower                                                           |
| unpickle             | 9.71 us                                                         | 9.93 us: 1.02x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.14x faster                                                                    |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                         | 22.2 ms: 1.01x faster                                                           |
| python_startup_no_site | 19.1 ms                                                         | 19.8 ms: 1.04x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.02x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 9.96 ms                                                         | 6.89 ms: 1.44x faster                                                           |
| django_template | 36.9 ms                                                         | 28.8 ms: 1.28x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.36x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| logging_silent             | 101 ns                                                          | 57.2 ns: 1.76x faster                                                           |
| deepcopy_memo              | 38.4 us                                                         | 22.0 us: 1.74x faster                                                           |
| generators                 | 38.5 ms                                                         | 22.3 ms: 1.73x faster                                                           |
| comprehensions             | 19.2 us                                                         | 11.2 us: 1.71x faster                                                           |
| nbody                      | 127 ms                                                          | 74.3 ms: 1.71x faster                                                           |
| unpack_sequence            | 62.5 ns                                                         | 36.9 ns: 1.69x faster                                                           |
| raytrace                   | 308 ms                                                          | 184 ms: 1.68x faster                                                            |
| deltablue                  | 3.58 ms                                                         | 2.15 ms: 1.67x faster                                                           |
| scimark_sor                | 130 ms                                                          | 78.5 ms: 1.65x faster                                                           |
| hexiom                     | 6.82 ms                                                         | 4.18 ms: 1.63x faster                                                           |
| spectral_norm              | 104 ms                                                          | 66.3 ms: 1.57x faster                                                           |
| scimark_lu                 | 93.2 ms                                                         | 61.7 ms: 1.51x faster                                                           |
| unpickle_pure_python       | 210 us                                                          | 139 us: 1.51x faster                                                            |
| coroutines                 | 20.9 ms                                                         | 13.9 ms: 1.50x faster                                                           |
| float                      | 76.7 ms                                                         | 51.3 ms: 1.50x faster                                                           |
| chaos                      | 69.4 ms                                                         | 46.5 ms: 1.49x faster                                                           |
| scimark_monte_carlo        | 66.4 ms                                                         | 44.7 ms: 1.48x faster                                                           |
| richards                   | 41.3 ms                                                         | 28.1 ms: 1.47x faster                                                           |
| sqlglot_parse              | 1.25 ms                                                         | 860 us: 1.45x faster                                                            |
| mako                       | 9.96 ms                                                         | 6.89 ms: 1.44x faster                                                           |
| richards_super             | 46.5 ms                                                         | 32.2 ms: 1.44x faster                                                           |
| go                         | 137 ms                                                          | 96.6 ms: 1.42x faster                                                           |
| nqueens                    | 93.7 ms                                                         | 66.0 ms: 1.42x faster                                                           |
| pickle_pure_python         | 286 us                                                          | 202 us: 1.41x faster                                                            |
| async_tree_none_tg         | 278 ms                                                          | 196 ms: 1.41x faster                                                            |
| sqlglot_transpile          | 1.53 ms                                                         | 1.09 ms: 1.41x faster                                                           |
| async_tree_none            | 298 ms                                                          | 213 ms: 1.40x faster                                                            |
| async_tree_memoization_tg  | 350 ms                                                          | 250 ms: 1.40x faster                                                            |
| typing_runtime_protocols   | 126 us                                                          | 90.5 us: 1.40x faster                                                           |
| chameleon                  | 7.75 ms                                                         | 5.57 ms: 1.39x faster                                                           |
| async_tree_memoization     | 364 ms                                                          | 262 ms: 1.39x faster                                                            |
| pyflate                    | 424 ms                                                          | 308 ms: 1.38x faster                                                            |
| tomli_loads                | 2.20 sec                                                        | 1.60 sec: 1.37x faster                                                          |
| deepcopy_reduce            | 3.23 us                                                         | 2.36 us: 1.36x faster                                                           |
| regex_compile              | 129 ms                                                          | 95.0 ms: 1.36x faster                                                           |
| deepcopy                   | 360 us                                                          | 266 us: 1.36x faster                                                            |
| async_tree_io              | 693 ms                                                          | 515 ms: 1.35x faster                                                            |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 2.89 ms: 1.33x faster                                                           |
| pprint_pformat             | 1.50 sec                                                        | 1.14 sec: 1.31x faster                                                          |
| fannkuch                   | 354 ms                                                          | 270 ms: 1.31x faster                                                            |
| logging_simple             | 9.75 us                                                         | 7.47 us: 1.31x faster                                                           |
| async_tree_io_tg           | 677 ms                                                          | 524 ms: 1.29x faster                                                            |
| scimark_fft                | 271 ms                                                          | 210 ms: 1.29x faster                                                            |
| pprint_safe_repr           | 721 ms                                                          | 562 ms: 1.28x faster                                                            |
| logging_format             | 10.4 us                                                         | 8.12 us: 1.28x faster                                                           |
| django_template            | 36.9 ms                                                         | 28.8 ms: 1.28x faster                                                           |
| crypto_pyaes               | 69.2 ms                                                         | 54.1 ms: 1.28x faster                                                           |
| pycparser                  | 978 ms                                                          | 772 ms: 1.27x faster                                                            |
| sqlglot_optimize           | 48.5 ms                                                         | 38.3 ms: 1.26x faster                                                           |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 447 ms: 1.26x faster                                                            |
| sympy_integrate            | 17.5 ms                                                         | 14.0 ms: 1.25x faster                                                           |
| xml_etree_generate         | 72.1 ms                                                         | 57.9 ms: 1.25x faster                                                           |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 439 ms: 1.24x faster                                                            |
| xml_etree_process          | 53.2 ms                                                         | 42.9 ms: 1.24x faster                                                           |
| sympy_str                  | 240 ms                                                          | 196 ms: 1.22x faster                                                            |
| sympy_sum                  | 123 ms                                                          | 101 ms: 1.22x faster                                                            |
| mdp                        | 1.91 sec                                                        | 1.57 sec: 1.21x faster                                                          |
| xml_etree_iterparse        | 77.6 ms                                                         | 64.0 ms: 1.21x faster                                                           |
| 2to3                       | 280 ms                                                          | 231 ms: 1.21x faster                                                            |
| meteor_contest             | 86.9 ms                                                         | 74.0 ms: 1.17x faster                                                           |
| sympy_expand               | 398 ms                                                          | 345 ms: 1.15x faster                                                            |
| bench_thread_pool          | 1.10 ms                                                         | 983 us: 1.12x faster                                                            |
| docutils                   | 1.98 sec                                                        | 1.77 sec: 1.12x faster                                                          |
| tornado_http               | 105 ms                                                          | 94.4 ms: 1.11x faster                                                           |
| bench_mp_pool              | 75.4 ms                                                         | 68.0 ms: 1.11x faster                                                           |
| async_generators           | 313 ms                                                          | 286 ms: 1.10x faster                                                            |
| json_dumps                 | 7.40 ms                                                         | 6.79 ms: 1.09x faster                                                           |
| sqlite_synth               | 2.07 us                                                         | 1.93 us: 1.07x faster                                                           |
| xml_etree_parse            | 113 ms                                                          | 105 ms: 1.07x faster                                                            |
| regex_effbot               | 2.04 ms                                                         | 1.91 ms: 1.07x faster                                                           |
| asyncio_tcp                | 662 ms                                                          | 623 ms: 1.06x faster                                                            |
| pathlib                    | 91.4 ms                                                         | 86.4 ms: 1.06x faster                                                           |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 16.7 sec: 1.06x faster                                                          |
| pickle_list                | 3.37 us                                                         | 3.22 us: 1.05x faster                                                           |
| unpickle_list              | 2.95 us                                                         | 2.87 us: 1.03x faster                                                           |
| python_startup             | 22.4 ms                                                         | 22.2 ms: 1.01x faster                                                           |
| pickle                     | 7.79 us                                                         | 7.87 us: 1.01x slower                                                           |
| pickle_dict                | 19.9 us                                                         | 20.2 us: 1.01x slower                                                           |
| unpickle                   | 9.71 us                                                         | 9.93 us: 1.02x slower                                                           |
| regex_dna                  | 127 ms                                                          | 131 ms: 1.03x slower                                                            |
| python_startup_no_site     | 19.1 ms                                                         | 19.8 ms: 1.04x slower                                                           |
| telco                      | 5.51 ms                                                         | 5.86 ms: 1.06x slower                                                           |
| regex_v8                   | 15.0 ms                                                         | 16.1 ms: 1.07x slower                                                           |
| create_gc_cycles           | 652 us                                                          | 726 us: 1.11x slower                                                            |
| sqlglot_normalize          | 100 ms                                                          | 200 ms: 2.00x slower                                                            |
| coverage                   | 48.4 ms                                                         | 470 ms: 9.70x slower                                                            |
| Geometric mean             | (ref)                                                           | 1.22x faster                                                                    |

Benchmark hidden because not significant (4): gc_traversal, json_loads, pidigits, json
Ignored benchmarks (6) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240329-3.13.0a5+-bfc57d4/bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.24x
- 95% likely to have a speedup of 1.23x
- 99% likely to have a speedup of 1.21x

# Memory
- memory change: unknown