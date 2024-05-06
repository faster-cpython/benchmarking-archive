# Results vs. 3.11.0

- fork: python
- ref: v3.12.3
- machine: windows-x86
- commit hash: f6650f9
- commit date: 2024-04-09
- overall geometric mean: 1.10x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 269 ms: 1.05x faster                                            |
| chameleon      | 8.08 ms                                                         | 7.39 ms: 1.09x faster                                           |
| docutils       | 2.10 sec                                                        | 1.94 sec: 1.08x faster                                          |
| html5lib       | 54.3 ms                                                         | 51.5 ms: 1.05x faster                                           |
| tornado_http   | 118 ms                                                          | 104 ms: 1.13x faster                                            |
| Geometric mean | (ref)                                                           | 1.08x faster                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|----------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 296 ms: 1.16x faster                                            |
| async_tree_memoization     | 408 ms                                                          | 358 ms: 1.14x faster                                            |
| async_tree_io_tg           | 746 ms                                                          | 662 ms: 1.13x faster                                            |
| async_tree_none_tg         | 301 ms                                                          | 269 ms: 1.12x faster                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 338 ms: 1.12x faster                                            |
| async_tree_io              | 754 ms                                                          | 683 ms: 1.10x faster                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 534 ms: 1.08x faster                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 553 ms: 1.07x faster                                            |
| Geometric mean             | (ref)                                                           | 1.11x faster                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| pidigits       | 203 ms                                                          | 199 ms: 1.02x faster                                            |
| nbody          | 126 ms                                                          | 125 ms: 1.01x faster                                            |
| Geometric mean | (ref)                                                           | 1.01x faster                                                    |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 130 ms: 1.13x faster                                            |
| regex_v8       | 15.2 ms                                                         | 15.3 ms: 1.01x slower                                           |
| regex_dna      | 122 ms                                                          | 129 ms: 1.06x slower                                            |
| regex_effbot   | 1.82 ms                                                         | 2.00 ms: 1.10x slower                                           |
| Geometric mean | (ref)                                                           | 1.01x slower                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| json_dumps           | 9.80 ms                                                         | 7.49 ms: 1.31x faster                                           |
| unpickle_pure_python | 231 us                                                          | 217 us: 1.07x faster                                            |
| tomli_loads          | 2.31 sec                                                        | 2.19 sec: 1.06x faster                                          |
| pickle_pure_python   | 309 us                                                          | 299 us: 1.03x faster                                            |
| xml_etree_process    | 55.0 ms                                                         | 53.5 ms: 1.03x faster                                           |
| pickle               | 7.99 us                                                         | 7.85 us: 1.02x faster                                           |
| pickle_list          | 3.27 us                                                         | 3.23 us: 1.01x faster                                           |
| xml_etree_parse      | 114 ms                                                          | 113 ms: 1.01x faster                                            |
| xml_etree_generate   | 71.6 ms                                                         | 73.6 ms: 1.03x slower                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 77.8 ms: 1.03x slower                                           |
| unpickle             | 9.23 us                                                         | 9.53 us: 1.03x slower                                           |
| json_loads           | 20.0 us                                                         | 20.9 us: 1.05x slower                                           |
| Geometric mean       | (ref)                                                           | 1.03x faster                                                    |

Benchmark hidden because not significant (2): unpickle_list, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 18.1 ms: 1.04x faster                                           |
| python_startup         | 22.0 ms                                                         | 21.3 ms: 1.03x faster                                           |
| Geometric mean         | (ref)                                                           | 1.04x faster                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|-----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| genshi_xml      | 61.2 ms                                                         | 53.9 ms: 1.14x faster                                           |
| genshi_text     | 26.8 ms                                                         | 24.9 ms: 1.08x faster                                           |
| mako            | 10.3 ms                                                         | 9.97 ms: 1.03x faster                                           |
| django_template | 37.4 ms                                                         | 36.7 ms: 1.02x faster                                           |
| Geometric mean  | (ref)                                                           | 1.06x faster                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240409-pythonperf1_win32-x86-python-v3.12.3-3.12.3-f6650f9 |
|----------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 114 us: 4.18x faster                                            |
| pylint                     | 418 ms                                                          | 249 ms: 1.68x faster                                            |
| comprehensions             | 22.1 us                                                         | 15.7 us: 1.40x faster                                           |
| json_dumps                 | 9.80 ms                                                         | 7.49 ms: 1.31x faster                                           |
| generators                 | 52.2 ms                                                         | 39.9 ms: 1.31x faster                                           |
| sympy_sum                  | 149 ms                                                          | 116 ms: 1.29x faster                                            |
| sqlalchemy_imperative      | 15.4 ms                                                         | 12.1 ms: 1.28x faster                                           |
| chaos                      | 84.4 ms                                                         | 68.1 ms: 1.24x faster                                           |
| sympy_str                  | 283 ms                                                          | 232 ms: 1.22x faster                                            |
| richards_super             | 58.7 ms                                                         | 48.2 ms: 1.22x faster                                           |
| asyncio_tcp                | 787 ms                                                          | 646 ms: 1.22x faster                                            |
| nqueens                    | 111 ms                                                          | 92.6 ms: 1.20x faster                                           |
| sqlglot_parse              | 1.49 ms                                                         | 1.26 ms: 1.18x faster                                           |
| sympy_integrate            | 19.9 ms                                                         | 16.9 ms: 1.18x faster                                           |
| sqlglot_transpile          | 1.78 ms                                                         | 1.54 ms: 1.16x faster                                           |
| async_tree_none            | 343 ms                                                          | 296 ms: 1.16x faster                                            |
| sympy_expand               | 462 ms                                                          | 402 ms: 1.15x faster                                            |
| coverage                   | 58.0 ms                                                         | 50.4 ms: 1.15x faster                                           |
| spectral_norm              | 122 ms                                                          | 106 ms: 1.15x faster                                            |
| async_tree_memoization     | 408 ms                                                          | 358 ms: 1.14x faster                                            |
| aiohttp                    | 1.17 ms                                                         | 1.03 ms: 1.14x faster                                           |
| logging_silent             | 119 ns                                                          | 105 ns: 1.14x faster                                            |
| deltablue                  | 4.10 ms                                                         | 3.61 ms: 1.14x faster                                           |
| mdp                        | 2.07 sec                                                        | 1.82 sec: 1.14x faster                                          |
| genshi_xml                 | 61.2 ms                                                         | 53.9 ms: 1.14x faster                                           |
| coroutines                 | 23.7 ms                                                         | 20.9 ms: 1.13x faster                                           |
| tornado_http               | 118 ms                                                          | 104 ms: 1.13x faster                                            |
| regex_compile              | 148 ms                                                          | 130 ms: 1.13x faster                                            |
| async_tree_io_tg           | 746 ms                                                          | 662 ms: 1.13x faster                                            |
| sqlalchemy_declarative     | 115 ms                                                          | 102 ms: 1.13x faster                                            |
| logging_simple             | 10.8 us                                                         | 9.61 us: 1.13x faster                                           |
| richards                   | 48.8 ms                                                         | 43.5 ms: 1.12x faster                                           |
| async_tree_none_tg         | 301 ms                                                          | 269 ms: 1.12x faster                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 338 ms: 1.12x faster                                            |
| logging_format             | 11.5 us                                                         | 10.3 us: 1.11x faster                                           |
| pprint_pformat             | 1.70 sec                                                        | 1.52 sec: 1.11x faster                                          |
| dulwich_log                | 62.8 ms                                                         | 56.7 ms: 1.11x faster                                           |
| crypto_pyaes               | 79.4 ms                                                         | 71.7 ms: 1.11x faster                                           |
| pprint_safe_repr           | 819 ms                                                          | 742 ms: 1.10x faster                                            |
| sqlglot_normalize          | 113 ms                                                          | 102 ms: 1.10x faster                                            |
| async_tree_io              | 754 ms                                                          | 683 ms: 1.10x faster                                            |
| dask                       | 355 ms                                                          | 322 ms: 1.10x faster                                            |
| fannkuch                   | 399 ms                                                          | 363 ms: 1.10x faster                                            |
| mypy2                      | 626 ms                                                          | 571 ms: 1.10x faster                                            |
| chameleon                  | 8.08 ms                                                         | 7.39 ms: 1.09x faster                                           |
| sqlglot_optimize           | 51.8 ms                                                         | 47.6 ms: 1.09x faster                                           |
| pyflate                    | 471 ms                                                          | 433 ms: 1.09x faster                                            |
| go                         | 147 ms                                                          | 135 ms: 1.09x faster                                            |
| hexiom                     | 7.51 ms                                                         | 6.93 ms: 1.08x faster                                           |
| json                       | 4.78 ms                                                         | 4.42 ms: 1.08x faster                                           |
| docutils                   | 2.10 sec                                                        | 1.94 sec: 1.08x faster                                          |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 534 ms: 1.08x faster                                            |
| deepcopy                   | 381 us                                                          | 353 us: 1.08x faster                                            |
| raytrace                   | 327 ms                                                          | 304 ms: 1.08x faster                                            |
| genshi_text                | 26.8 ms                                                         | 24.9 ms: 1.08x faster                                           |
| pycparser                  | 1.04 sec                                                        | 970 ms: 1.08x faster                                            |
| scimark_fft                | 291 ms                                                          | 271 ms: 1.07x faster                                            |
| meteor_contest             | 90.9 ms                                                         | 84.8 ms: 1.07x faster                                           |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.96 ms: 1.07x faster                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 553 ms: 1.07x faster                                            |
| unpickle_pure_python       | 231 us                                                          | 217 us: 1.07x faster                                            |
| deepcopy_memo              | 40.0 us                                                         | 37.7 us: 1.06x faster                                           |
| scimark_lu                 | 102 ms                                                          | 96.6 ms: 1.06x faster                                           |
| scimark_monte_carlo        | 70.8 ms                                                         | 67.0 ms: 1.06x faster                                           |
| tomli_loads                | 2.31 sec                                                        | 2.19 sec: 1.06x faster                                          |
| bench_thread_pool          | 1.14 ms                                                         | 1.08 ms: 1.05x faster                                           |
| html5lib                   | 54.3 ms                                                         | 51.5 ms: 1.05x faster                                           |
| 2to3                       | 282 ms                                                          | 269 ms: 1.05x faster                                            |
| deepcopy_reduce            | 3.32 us                                                         | 3.16 us: 1.05x faster                                           |
| python_startup_no_site     | 18.8 ms                                                         | 18.1 ms: 1.04x faster                                           |
| scimark_sor                | 135 ms                                                          | 130 ms: 1.04x faster                                            |
| thrift                     | 801 us                                                          | 773 us: 1.04x faster                                            |
| pickle_pure_python         | 309 us                                                          | 299 us: 1.03x faster                                            |
| python_startup             | 22.0 ms                                                         | 21.3 ms: 1.03x faster                                           |
| mako                       | 10.3 ms                                                         | 9.97 ms: 1.03x faster                                           |
| xml_etree_process          | 55.0 ms                                                         | 53.5 ms: 1.03x faster                                           |
| django_template            | 37.4 ms                                                         | 36.7 ms: 1.02x faster                                           |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.7 sec: 1.02x faster                                          |
| pickle                     | 7.99 us                                                         | 7.85 us: 1.02x faster                                           |
| pidigits                   | 203 ms                                                          | 199 ms: 1.02x faster                                            |
| telco                      | 5.29 ms                                                         | 5.22 ms: 1.01x faster                                           |
| pickle_list                | 3.27 us                                                         | 3.23 us: 1.01x faster                                           |
| nbody                      | 126 ms                                                          | 125 ms: 1.01x faster                                            |
| xml_etree_parse            | 114 ms                                                          | 113 ms: 1.01x faster                                            |
| sqlite_synth               | 2.15 us                                                         | 2.13 us: 1.01x faster                                           |
| regex_v8                   | 15.2 ms                                                         | 15.3 ms: 1.01x slower                                           |
| bench_mp_pool              | 70.9 ms                                                         | 71.9 ms: 1.01x slower                                           |
| gc_traversal               | 1.38 ms                                                         | 1.41 ms: 1.02x slower                                           |
| xml_etree_generate         | 71.6 ms                                                         | 73.6 ms: 1.03x slower                                           |
| xml_etree_iterparse        | 75.6 ms                                                         | 77.8 ms: 1.03x slower                                           |
| unpickle                   | 9.23 us                                                         | 9.53 us: 1.03x slower                                           |
| json_loads                 | 20.0 us                                                         | 20.9 us: 1.05x slower                                           |
| create_gc_cycles           | 618 us                                                          | 648 us: 1.05x slower                                            |
| regex_dna                  | 122 ms                                                          | 129 ms: 1.06x slower                                            |
| pathlib                    | 79.9 ms                                                         | 85.6 ms: 1.07x slower                                           |
| regex_effbot               | 1.82 ms                                                         | 2.00 ms: 1.10x slower                                           |
| async_generators           | 260 ms                                                          | 313 ms: 1.20x slower                                            |
| Geometric mean             | (ref)                                                           | 1.10x faster                                                    |

Benchmark hidden because not significant (3): unpickle_list, pickle_dict, float
Ignored benchmarks (2) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: unknown