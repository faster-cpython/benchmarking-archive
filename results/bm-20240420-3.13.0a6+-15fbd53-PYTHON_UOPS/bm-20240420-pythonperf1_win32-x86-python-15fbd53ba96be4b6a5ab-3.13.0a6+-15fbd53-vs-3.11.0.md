# Results vs. 3.11.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: windows-x86
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.21x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 242 ms: 1.17x faster                                                            |
| chameleon      | 8.08 ms                                                         | 5.74 ms: 1.41x faster                                                           |
| docutils       | 2.10 sec                                                        | 1.90 sec: 1.10x faster                                                          |
| html5lib       | 54.3 ms                                                         | 44.8 ms: 1.21x faster                                                           |
| tornado_http   | 118 ms                                                          | 96.6 ms: 1.23x faster                                                           |
| Geometric mean | (ref)                                                           | 1.22x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 231 ms: 1.49x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 278 ms: 1.47x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 259 ms: 1.46x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 210 ms: 1.43x faster                                                            |
| async_tree_io              | 754 ms                                                          | 535 ms: 1.41x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 533 ms: 1.40x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 446 ms: 1.29x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 473 ms: 1.25x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.40x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 79.1 ms: 1.59x faster                                                           |
| float          | 76.1 ms                                                         | 55.1 ms: 1.38x faster                                                           |
| pidigits       | 203 ms                                                          | 200 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                           | 1.31x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 119 ms: 1.24x faster                                                            |
| regex_dna      | 122 ms                                                          | 120 ms: 1.01x faster                                                            |
| regex_effbot   | 1.82 ms                                                         | 1.90 ms: 1.04x slower                                                           |
| regex_v8       | 15.2 ms                                                         | 16.1 ms: 1.06x slower                                                           |
| Geometric mean | (ref)                                                           | 1.03x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| tomli_loads          | 2.31 sec                                                        | 1.63 sec: 1.42x faster                                                          |
| pickle_pure_python   | 309 us                                                          | 218 us: 1.42x faster                                                            |
| unpickle_pure_python | 231 us                                                          | 164 us: 1.41x faster                                                            |
| json_dumps           | 9.80 ms                                                         | 7.02 ms: 1.40x faster                                                           |
| xml_etree_process    | 55.0 ms                                                         | 43.4 ms: 1.27x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 2.70 us: 1.21x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 60.1 ms: 1.19x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 67.1 ms: 1.13x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 106 ms: 1.07x faster                                                            |
| pickle               | 7.99 us                                                         | 7.76 us: 1.03x faster                                                           |
| pickle_dict          | 20.1 us                                                         | 20.3 us: 1.01x slower                                                           |
| json_loads           | 20.0 us                                                         | 20.3 us: 1.01x slower                                                           |
| pickle_list          | 3.27 us                                                         | 3.33 us: 1.02x slower                                                           |
| unpickle             | 9.23 us                                                         | 9.94 us: 1.08x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.16x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 18.1 ms: 1.04x faster                                                           |
| Geometric mean         | (ref)                                                           | 1.02x faster                                                                    |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 7.01 ms: 1.47x faster                                                           |
| genshi_xml      | 61.2 ms                                                         | 46.8 ms: 1.31x faster                                                           |
| genshi_text     | 26.8 ms                                                         | 20.9 ms: 1.28x faster                                                           |
| django_template | 37.4 ms                                                         | 31.9 ms: 1.17x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.30x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf1_win32-x86-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 92.9 us: 5.15x faster                                                           |
| generators                 | 52.2 ms                                                         | 23.4 ms: 2.24x faster                                                           |
| logging_silent             | 119 ns                                                          | 59.7 ns: 2.00x faster                                                           |
| pylint                     | 418 ms                                                          | 230 ms: 1.82x faster                                                            |
| richards_super             | 58.7 ms                                                         | 33.7 ms: 1.74x faster                                                           |
| richards                   | 48.8 ms                                                         | 29.7 ms: 1.64x faster                                                           |
| comprehensions             | 22.1 us                                                         | 13.7 us: 1.61x faster                                                           |
| raytrace                   | 327 ms                                                          | 203 ms: 1.61x faster                                                            |
| chaos                      | 84.4 ms                                                         | 52.6 ms: 1.61x faster                                                           |
| deepcopy_memo              | 40.0 us                                                         | 25.0 us: 1.60x faster                                                           |
| nbody                      | 126 ms                                                          | 79.1 ms: 1.59x faster                                                           |
| deltablue                  | 4.10 ms                                                         | 2.58 ms: 1.59x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 955 us: 1.56x faster                                                            |
| coroutines                 | 23.7 ms                                                         | 15.2 ms: 1.56x faster                                                           |
| spectral_norm              | 122 ms                                                          | 79.5 ms: 1.53x faster                                                           |
| sqlglot_transpile          | 1.78 ms                                                         | 1.20 ms: 1.49x faster                                                           |
| async_tree_none            | 343 ms                                                          | 231 ms: 1.49x faster                                                            |
| mako                       | 10.3 ms                                                         | 7.01 ms: 1.47x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 278 ms: 1.47x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 259 ms: 1.46x faster                                                            |
| nqueens                    | 111 ms                                                          | 77.3 ms: 1.44x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 210 ms: 1.43x faster                                                            |
| tomli_loads                | 2.31 sec                                                        | 1.63 sec: 1.42x faster                                                          |
| pyflate                    | 471 ms                                                          | 332 ms: 1.42x faster                                                            |
| scimark_sor                | 135 ms                                                          | 95.3 ms: 1.42x faster                                                           |
| pickle_pure_python         | 309 us                                                          | 218 us: 1.42x faster                                                            |
| fannkuch                   | 399 ms                                                          | 282 ms: 1.42x faster                                                            |
| async_tree_io              | 754 ms                                                          | 535 ms: 1.41x faster                                                            |
| unpickle_pure_python       | 231 us                                                          | 164 us: 1.41x faster                                                            |
| chameleon                  | 8.08 ms                                                         | 5.74 ms: 1.41x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 533 ms: 1.40x faster                                                            |
| json_dumps                 | 9.80 ms                                                         | 7.02 ms: 1.40x faster                                                           |
| hexiom                     | 7.51 ms                                                         | 5.39 ms: 1.39x faster                                                           |
| scimark_monte_carlo        | 70.8 ms                                                         | 50.8 ms: 1.39x faster                                                           |
| scimark_fft                | 291 ms                                                          | 209 ms: 1.39x faster                                                            |
| float                      | 76.1 ms                                                         | 55.1 ms: 1.38x faster                                                           |
| pprint_pformat             | 1.70 sec                                                        | 1.23 sec: 1.37x faster                                                          |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.10 ms: 1.37x faster                                                           |
| logging_simple             | 10.8 us                                                         | 7.92 us: 1.36x faster                                                           |
| crypto_pyaes               | 79.4 ms                                                         | 58.4 ms: 1.36x faster                                                           |
| pprint_safe_repr           | 819 ms                                                          | 603 ms: 1.36x faster                                                            |
| deepcopy                   | 381 us                                                          | 281 us: 1.36x faster                                                            |
| logging_format             | 11.5 us                                                         | 8.60 us: 1.33x faster                                                           |
| sympy_sum                  | 149 ms                                                          | 113 ms: 1.32x faster                                                            |
| genshi_xml                 | 61.2 ms                                                         | 46.8 ms: 1.31x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 446 ms: 1.29x faster                                                            |
| deepcopy_reduce            | 3.32 us                                                         | 2.57 us: 1.29x faster                                                           |
| genshi_text                | 26.8 ms                                                         | 20.9 ms: 1.28x faster                                                           |
| xml_etree_process          | 55.0 ms                                                         | 43.4 ms: 1.27x faster                                                           |
| scimark_lu                 | 102 ms                                                          | 80.9 ms: 1.26x faster                                                           |
| sympy_integrate            | 19.9 ms                                                         | 15.8 ms: 1.26x faster                                                           |
| go                         | 147 ms                                                          | 116 ms: 1.26x faster                                                            |
| sympy_str                  | 283 ms                                                          | 224 ms: 1.26x faster                                                            |
| asyncio_tcp                | 787 ms                                                          | 627 ms: 1.25x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 473 ms: 1.25x faster                                                            |
| pycparser                  | 1.04 sec                                                        | 842 ms: 1.24x faster                                                            |
| regex_compile              | 148 ms                                                          | 119 ms: 1.24x faster                                                            |
| tornado_http               | 118 ms                                                          | 96.6 ms: 1.23x faster                                                           |
| unpickle_list              | 3.28 us                                                         | 2.70 us: 1.21x faster                                                           |
| html5lib                   | 54.3 ms                                                         | 44.8 ms: 1.21x faster                                                           |
| sqlglot_optimize           | 51.8 ms                                                         | 42.9 ms: 1.21x faster                                                           |
| mdp                        | 2.07 sec                                                        | 1.72 sec: 1.20x faster                                                          |
| xml_etree_generate         | 71.6 ms                                                         | 60.1 ms: 1.19x faster                                                           |
| meteor_contest             | 90.9 ms                                                         | 77.5 ms: 1.17x faster                                                           |
| django_template            | 37.4 ms                                                         | 31.9 ms: 1.17x faster                                                           |
| sympy_expand               | 462 ms                                                          | 394 ms: 1.17x faster                                                            |
| 2to3                       | 282 ms                                                          | 242 ms: 1.17x faster                                                            |
| json                       | 4.78 ms                                                         | 4.13 ms: 1.16x faster                                                           |
| bench_thread_pool          | 1.14 ms                                                         | 1.00 ms: 1.13x faster                                                           |
| xml_etree_iterparse        | 75.6 ms                                                         | 67.1 ms: 1.13x faster                                                           |
| sqlite_synth               | 2.15 us                                                         | 1.93 us: 1.12x faster                                                           |
| docutils                   | 2.10 sec                                                        | 1.90 sec: 1.10x faster                                                          |
| xml_etree_parse            | 114 ms                                                          | 106 ms: 1.07x faster                                                            |
| python_startup_no_site     | 18.8 ms                                                         | 18.1 ms: 1.04x faster                                                           |
| pickle                     | 7.99 us                                                         | 7.76 us: 1.03x faster                                                           |
| bench_mp_pool              | 70.9 ms                                                         | 69.3 ms: 1.02x faster                                                           |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.7 sec: 1.02x faster                                                          |
| pidigits                   | 203 ms                                                          | 200 ms: 1.01x faster                                                            |
| regex_dna                  | 122 ms                                                          | 120 ms: 1.01x faster                                                            |
| pickle_dict                | 20.1 us                                                         | 20.3 us: 1.01x slower                                                           |
| json_loads                 | 20.0 us                                                         | 20.3 us: 1.01x slower                                                           |
| pickle_list                | 3.27 us                                                         | 3.33 us: 1.02x slower                                                           |
| gc_traversal               | 1.38 ms                                                         | 1.43 ms: 1.04x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.90 ms: 1.04x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 84.4 ms: 1.06x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 16.1 ms: 1.06x slower                                                           |
| unpickle                   | 9.23 us                                                         | 9.94 us: 1.08x slower                                                           |
| async_generators           | 260 ms                                                          | 291 ms: 1.12x slower                                                            |
| telco                      | 5.29 ms                                                         | 6.08 ms: 1.15x slower                                                           |
| create_gc_cycles           | 618 us                                                          | 731 us: 1.18x slower                                                            |
| sqlglot_normalize          | 113 ms                                                          | 224 ms: 1.98x slower                                                            |
| coverage                   | 58.0 ms                                                         | 512 ms: 8.82x slower                                                            |
| thrift                     | 801 us                                                          | 11.0 ms: 13.77x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.21x faster                                                                    |

Benchmark hidden because not significant (1): python_startup
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.25x
- 95% likely to have a speedup of 1.23x
- 99% likely to have a speedup of 1.22x

# Memory
- memory change: unknown