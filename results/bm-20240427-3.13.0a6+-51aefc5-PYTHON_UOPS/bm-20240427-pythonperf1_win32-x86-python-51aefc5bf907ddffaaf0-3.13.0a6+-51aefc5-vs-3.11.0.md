# Results vs. 3.11.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: windows-x86
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.19x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 250 ms: 1.13x faster                                                            |
| chameleon      | 8.08 ms                                                         | 5.70 ms: 1.42x faster                                                           |
| docutils       | 2.10 sec                                                        | 1.95 sec: 1.08x faster                                                          |
| html5lib       | 54.3 ms                                                         | 46.3 ms: 1.17x faster                                                           |
| tornado_http   | 118 ms                                                          | 107 ms: 1.11x faster                                                            |
| Geometric mean | (ref)                                                           | 1.17x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 229 ms: 1.50x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 277 ms: 1.47x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 260 ms: 1.45x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 210 ms: 1.44x faster                                                            |
| async_tree_io              | 754 ms                                                          | 534 ms: 1.41x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 537 ms: 1.39x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 451 ms: 1.28x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 483 ms: 1.22x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.39x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 79.1 ms: 1.59x faster                                                           |
| float          | 76.1 ms                                                         | 57.4 ms: 1.33x faster                                                           |
| pidigits       | 203 ms                                                          | 198 ms: 1.03x faster                                                            |
| Geometric mean | (ref)                                                           | 1.29x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 121 ms: 1.22x faster                                                            |
| regex_dna      | 122 ms                                                          | 120 ms: 1.01x faster                                                            |
| regex_effbot   | 1.82 ms                                                         | 1.93 ms: 1.06x slower                                                           |
| regex_v8       | 15.2 ms                                                         | 16.3 ms: 1.07x slower                                                           |
| Geometric mean | (ref)                                                           | 1.02x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| tomli_loads          | 2.31 sec                                                        | 1.60 sec: 1.44x faster                                                          |
| json_dumps           | 9.80 ms                                                         | 6.89 ms: 1.42x faster                                                           |
| pickle_pure_python   | 309 us                                                          | 224 us: 1.38x faster                                                            |
| unpickle_pure_python | 231 us                                                          | 174 us: 1.33x faster                                                            |
| xml_etree_process    | 55.0 ms                                                         | 43.2 ms: 1.27x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 60.7 ms: 1.18x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 67.0 ms: 1.13x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 104 ms: 1.10x faster                                                            |
| unpickle_list        | 3.28 us                                                         | 3.02 us: 1.08x faster                                                           |
| pickle               | 7.99 us                                                         | 7.76 us: 1.03x faster                                                           |
| pickle_list          | 3.27 us                                                         | 3.32 us: 1.02x slower                                                           |
| pickle_dict          | 20.1 us                                                         | 20.5 us: 1.02x slower                                                           |
| json_loads           | 20.0 us                                                         | 20.5 us: 1.02x slower                                                           |
| unpickle             | 9.23 us                                                         | 9.90 us: 1.07x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.15x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup | 22.0 ms                                                         | 22.5 ms: 1.02x slower                                                           |
| Geometric mean | (ref)                                                           | 1.01x slower                                                                    |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 7.76 ms: 1.32x faster                                                           |
| genshi_text     | 26.8 ms                                                         | 20.5 ms: 1.31x faster                                                           |
| genshi_xml      | 61.2 ms                                                         | 47.3 ms: 1.29x faster                                                           |
| django_template | 37.4 ms                                                         | 32.0 ms: 1.17x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.27x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 147 us: 3.25x faster                                                            |
| generators                 | 52.2 ms                                                         | 23.8 ms: 2.20x faster                                                           |
| logging_silent             | 119 ns                                                          | 61.0 ns: 1.95x faster                                                           |
| pylint                     | 418 ms                                                          | 236 ms: 1.77x faster                                                            |
| richards_super             | 58.7 ms                                                         | 34.9 ms: 1.68x faster                                                           |
| nbody                      | 126 ms                                                          | 79.1 ms: 1.59x faster                                                           |
| chaos                      | 84.4 ms                                                         | 53.8 ms: 1.57x faster                                                           |
| comprehensions             | 22.1 us                                                         | 14.1 us: 1.57x faster                                                           |
| richards                   | 48.8 ms                                                         | 31.2 ms: 1.56x faster                                                           |
| deepcopy_memo              | 40.0 us                                                         | 25.8 us: 1.55x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 972 us: 1.53x faster                                                            |
| raytrace                   | 327 ms                                                          | 214 ms: 1.53x faster                                                            |
| spectral_norm              | 122 ms                                                          | 79.5 ms: 1.53x faster                                                           |
| deltablue                  | 4.10 ms                                                         | 2.68 ms: 1.53x faster                                                           |
| coroutines                 | 23.7 ms                                                         | 15.8 ms: 1.51x faster                                                           |
| async_tree_none            | 343 ms                                                          | 229 ms: 1.50x faster                                                            |
| sqlglot_transpile          | 1.78 ms                                                         | 1.21 ms: 1.48x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 277 ms: 1.47x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 260 ms: 1.45x faster                                                            |
| scimark_sor                | 135 ms                                                          | 93.2 ms: 1.45x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.60 sec: 1.44x faster                                                          |
| async_tree_none_tg         | 301 ms                                                          | 210 ms: 1.44x faster                                                            |
| json_dumps                 | 9.80 ms                                                         | 6.89 ms: 1.42x faster                                                           |
| nqueens                    | 111 ms                                                          | 78.4 ms: 1.42x faster                                                           |
| chameleon                  | 8.08 ms                                                         | 5.70 ms: 1.42x faster                                                           |
| async_tree_io              | 754 ms                                                          | 534 ms: 1.41x faster                                                            |
| fannkuch                   | 399 ms                                                          | 286 ms: 1.40x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 537 ms: 1.39x faster                                                            |
| crypto_pyaes               | 79.4 ms                                                         | 57.6 ms: 1.38x faster                                                           |
| pickle_pure_python         | 309 us                                                          | 224 us: 1.38x faster                                                            |
| pyflate                    | 471 ms                                                          | 344 ms: 1.37x faster                                                            |
| pprint_pformat             | 1.70 sec                                                        | 1.24 sec: 1.37x faster                                                          |
| logging_simple             | 10.8 us                                                         | 7.90 us: 1.37x faster                                                           |
| scimark_fft                | 291 ms                                                          | 214 ms: 1.36x faster                                                            |
| pprint_safe_repr           | 819 ms                                                          | 605 ms: 1.35x faster                                                            |
| logging_format             | 11.5 us                                                         | 8.47 us: 1.35x faster                                                           |
| scimark_monte_carlo        | 70.8 ms                                                         | 52.4 ms: 1.35x faster                                                           |
| unpickle_pure_python       | 231 us                                                          | 174 us: 1.33x faster                                                            |
| float                      | 76.1 ms                                                         | 57.4 ms: 1.33x faster                                                           |
| mako                       | 10.3 ms                                                         | 7.76 ms: 1.32x faster                                                           |
| hexiom                     | 7.51 ms                                                         | 5.68 ms: 1.32x faster                                                           |
| sympy_sum                  | 149 ms                                                          | 113 ms: 1.32x faster                                                            |
| deepcopy                   | 381 us                                                          | 291 us: 1.31x faster                                                            |
| genshi_text                | 26.8 ms                                                         | 20.5 ms: 1.31x faster                                                           |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.26 ms: 1.30x faster                                                           |
| genshi_xml                 | 61.2 ms                                                         | 47.3 ms: 1.29x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 451 ms: 1.28x faster                                                            |
| sympy_str                  | 283 ms                                                          | 223 ms: 1.27x faster                                                            |
| xml_etree_process          | 55.0 ms                                                         | 43.2 ms: 1.27x faster                                                           |
| deepcopy_reduce            | 3.32 us                                                         | 2.61 us: 1.27x faster                                                           |
| sympy_integrate            | 19.9 ms                                                         | 16.0 ms: 1.25x faster                                                           |
| scimark_lu                 | 102 ms                                                          | 82.1 ms: 1.25x faster                                                           |
| go                         | 147 ms                                                          | 118 ms: 1.24x faster                                                            |
| mdp                        | 2.07 sec                                                        | 1.67 sec: 1.24x faster                                                          |
| pycparser                  | 1.04 sec                                                        | 843 ms: 1.24x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 483 ms: 1.22x faster                                                            |
| regex_compile              | 148 ms                                                          | 121 ms: 1.22x faster                                                            |
| sqlglot_optimize           | 51.8 ms                                                         | 43.0 ms: 1.21x faster                                                           |
| xml_etree_generate         | 71.6 ms                                                         | 60.7 ms: 1.18x faster                                                           |
| sympy_expand               | 462 ms                                                          | 393 ms: 1.18x faster                                                            |
| html5lib                   | 54.3 ms                                                         | 46.3 ms: 1.17x faster                                                           |
| django_template            | 37.4 ms                                                         | 32.0 ms: 1.17x faster                                                           |
| meteor_contest             | 90.9 ms                                                         | 78.9 ms: 1.15x faster                                                           |
| xml_etree_iterparse        | 75.6 ms                                                         | 67.0 ms: 1.13x faster                                                           |
| 2to3                       | 282 ms                                                          | 250 ms: 1.13x faster                                                            |
| json                       | 4.78 ms                                                         | 4.27 ms: 1.12x faster                                                           |
| bench_thread_pool          | 1.14 ms                                                         | 1.02 ms: 1.11x faster                                                           |
| tornado_http               | 118 ms                                                          | 107 ms: 1.11x faster                                                            |
| xml_etree_parse            | 114 ms                                                          | 104 ms: 1.10x faster                                                            |
| unpickle_list              | 3.28 us                                                         | 3.02 us: 1.08x faster                                                           |
| docutils                   | 2.10 sec                                                        | 1.95 sec: 1.08x faster                                                          |
| sqlite_synth               | 2.15 us                                                         | 2.01 us: 1.07x faster                                                           |
| pickle                     | 7.99 us                                                         | 7.76 us: 1.03x faster                                                           |
| pidigits                   | 203 ms                                                          | 198 ms: 1.03x faster                                                            |
| regex_dna                  | 122 ms                                                          | 120 ms: 1.01x faster                                                            |
| bench_mp_pool              | 70.9 ms                                                         | 71.7 ms: 1.01x slower                                                           |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 17.3 sec: 1.01x slower                                                          |
| pickle_list                | 3.27 us                                                         | 3.32 us: 1.02x slower                                                           |
| pickle_dict                | 20.1 us                                                         | 20.5 us: 1.02x slower                                                           |
| python_startup             | 22.0 ms                                                         | 22.5 ms: 1.02x slower                                                           |
| json_loads                 | 20.0 us                                                         | 20.5 us: 1.02x slower                                                           |
| gc_traversal               | 1.38 ms                                                         | 1.45 ms: 1.05x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.93 ms: 1.06x slower                                                           |
| telco                      | 5.29 ms                                                         | 5.67 ms: 1.07x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 16.3 ms: 1.07x slower                                                           |
| unpickle                   | 9.23 us                                                         | 9.90 us: 1.07x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 89.7 ms: 1.12x slower                                                           |
| async_generators           | 260 ms                                                          | 297 ms: 1.14x slower                                                            |
| create_gc_cycles           | 618 us                                                          | 750 us: 1.21x slower                                                            |
| sqlglot_normalize          | 113 ms                                                          | 220 ms: 1.94x slower                                                            |
| coverage                   | 58.0 ms                                                         | 418 ms: 7.20x slower                                                            |
| thrift                     | 801 us                                                          | 11.6 ms: 14.44x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.19x faster                                                                    |

Benchmark hidden because not significant (2): python_startup_no_site, asyncio_tcp
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.23x
- 95% likely to have a speedup of 1.22x
- 99% likely to have a speedup of 1.20x

# Memory
- memory change: unknown