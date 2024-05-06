# Results vs. 3.12.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: windows-x86
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.12x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 250 ms: 1.12x faster                                                            |
| chameleon      | 7.75 ms                                                         | 5.70 ms: 1.36x faster                                                           |
| docutils       | 1.98 sec                                                        | 1.95 sec: 1.02x faster                                                          |
| tornado_http   | 105 ms                                                          | 107 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                           | 1.11x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 350 ms                                                          | 260 ms: 1.35x faster                                                            |
| async_tree_none_tg         | 278 ms                                                          | 210 ms: 1.32x faster                                                            |
| async_tree_memoization     | 364 ms                                                          | 277 ms: 1.31x faster                                                            |
| async_tree_none            | 298 ms                                                          | 229 ms: 1.30x faster                                                            |
| async_tree_io              | 693 ms                                                          | 534 ms: 1.30x faster                                                            |
| async_tree_io_tg           | 677 ms                                                          | 537 ms: 1.26x faster                                                            |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 451 ms: 1.21x faster                                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 483 ms: 1.17x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.28x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 127 ms                                                          | 79.1 ms: 1.61x faster                                                           |
| float          | 76.7 ms                                                         | 57.4 ms: 1.34x faster                                                           |
| pidigits       | 199 ms                                                          | 198 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                           | 1.29x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 121 ms: 1.07x faster                                                            |
| regex_effbot   | 2.04 ms                                                         | 1.93 ms: 1.06x faster                                                           |
| regex_dna      | 127 ms                                                          | 120 ms: 1.05x faster                                                            |
| regex_v8       | 15.0 ms                                                         | 16.3 ms: 1.08x slower                                                           |
| Geometric mean | (ref)                                                           | 1.03x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| tomli_loads          | 2.20 sec                                                        | 1.60 sec: 1.37x faster                                                          |
| pickle_pure_python   | 286 us                                                          | 224 us: 1.28x faster                                                            |
| xml_etree_process    | 53.2 ms                                                         | 43.2 ms: 1.23x faster                                                           |
| unpickle_pure_python | 210 us                                                          | 174 us: 1.21x faster                                                            |
| xml_etree_generate   | 72.1 ms                                                         | 60.7 ms: 1.19x faster                                                           |
| xml_etree_iterparse  | 77.6 ms                                                         | 67.0 ms: 1.16x faster                                                           |
| xml_etree_parse      | 113 ms                                                          | 104 ms: 1.09x faster                                                            |
| json_dumps           | 7.40 ms                                                         | 6.89 ms: 1.07x faster                                                           |
| pickle_list          | 3.37 us                                                         | 3.32 us: 1.02x faster                                                           |
| json_loads           | 20.4 us                                                         | 20.5 us: 1.01x slower                                                           |
| unpickle             | 9.71 us                                                         | 9.90 us: 1.02x slower                                                           |
| unpickle_list        | 2.95 us                                                         | 3.02 us: 1.03x slower                                                           |
| pickle_dict          | 19.9 us                                                         | 20.5 us: 1.03x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.10x faster                                                                    |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 19.1 ms                                                         | 18.8 ms: 1.02x faster                                                           |
| Geometric mean         | (ref)                                                           | 1.01x faster                                                                    |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 9.96 ms                                                         | 7.76 ms: 1.28x faster                                                           |
| django_template | 36.9 ms                                                         | 32.0 ms: 1.15x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.22x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| logging_silent             | 101 ns                                                          | 61.0 ns: 1.66x faster                                                           |
| generators                 | 38.5 ms                                                         | 23.8 ms: 1.62x faster                                                           |
| nbody                      | 127 ms                                                          | 79.1 ms: 1.61x faster                                                           |
| deepcopy_memo              | 38.4 us                                                         | 25.8 us: 1.49x faster                                                           |
| raytrace                   | 308 ms                                                          | 214 ms: 1.44x faster                                                            |
| scimark_sor                | 130 ms                                                          | 93.2 ms: 1.39x faster                                                           |
| tomli_loads                | 2.20 sec                                                        | 1.60 sec: 1.37x faster                                                          |
| comprehensions             | 19.2 us                                                         | 14.1 us: 1.36x faster                                                           |
| chameleon                  | 7.75 ms                                                         | 5.70 ms: 1.36x faster                                                           |
| async_tree_memoization_tg  | 350 ms                                                          | 260 ms: 1.35x faster                                                            |
| float                      | 76.7 ms                                                         | 57.4 ms: 1.34x faster                                                           |
| deltablue                  | 3.58 ms                                                         | 2.68 ms: 1.33x faster                                                           |
| richards_super             | 46.5 ms                                                         | 34.9 ms: 1.33x faster                                                           |
| richards                   | 41.3 ms                                                         | 31.2 ms: 1.32x faster                                                           |
| coroutines                 | 20.9 ms                                                         | 15.8 ms: 1.32x faster                                                           |
| async_tree_none_tg         | 278 ms                                                          | 210 ms: 1.32x faster                                                            |
| async_tree_memoization     | 364 ms                                                          | 277 ms: 1.31x faster                                                            |
| spectral_norm              | 104 ms                                                          | 79.5 ms: 1.31x faster                                                           |
| async_tree_none            | 298 ms                                                          | 229 ms: 1.30x faster                                                            |
| async_tree_io              | 693 ms                                                          | 534 ms: 1.30x faster                                                            |
| chaos                      | 69.4 ms                                                         | 53.8 ms: 1.29x faster                                                           |
| sqlglot_parse              | 1.25 ms                                                         | 972 us: 1.28x faster                                                            |
| mako                       | 9.96 ms                                                         | 7.76 ms: 1.28x faster                                                           |
| pickle_pure_python         | 286 us                                                          | 224 us: 1.28x faster                                                            |
| scimark_monte_carlo        | 66.4 ms                                                         | 52.4 ms: 1.27x faster                                                           |
| sqlglot_transpile          | 1.53 ms                                                         | 1.21 ms: 1.27x faster                                                           |
| scimark_fft                | 271 ms                                                          | 214 ms: 1.26x faster                                                            |
| async_tree_io_tg           | 677 ms                                                          | 537 ms: 1.26x faster                                                            |
| deepcopy                   | 360 us                                                          | 291 us: 1.24x faster                                                            |
| deepcopy_reduce            | 3.23 us                                                         | 2.61 us: 1.24x faster                                                           |
| fannkuch                   | 354 ms                                                          | 286 ms: 1.24x faster                                                            |
| logging_simple             | 9.75 us                                                         | 7.90 us: 1.23x faster                                                           |
| pyflate                    | 424 ms                                                          | 344 ms: 1.23x faster                                                            |
| xml_etree_process          | 53.2 ms                                                         | 43.2 ms: 1.23x faster                                                           |
| logging_format             | 10.4 us                                                         | 8.47 us: 1.23x faster                                                           |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 451 ms: 1.21x faster                                                            |
| pprint_pformat             | 1.50 sec                                                        | 1.24 sec: 1.21x faster                                                          |
| unpickle_pure_python       | 210 us                                                          | 174 us: 1.21x faster                                                            |
| crypto_pyaes               | 69.2 ms                                                         | 57.6 ms: 1.20x faster                                                           |
| hexiom                     | 6.82 ms                                                         | 5.68 ms: 1.20x faster                                                           |
| nqueens                    | 93.7 ms                                                         | 78.4 ms: 1.19x faster                                                           |
| pprint_safe_repr           | 721 ms                                                          | 605 ms: 1.19x faster                                                            |
| xml_etree_generate         | 72.1 ms                                                         | 60.7 ms: 1.19x faster                                                           |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 3.26 ms: 1.18x faster                                                           |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 483 ms: 1.17x faster                                                            |
| go                         | 137 ms                                                          | 118 ms: 1.16x faster                                                            |
| pycparser                  | 978 ms                                                          | 843 ms: 1.16x faster                                                            |
| xml_etree_iterparse        | 77.6 ms                                                         | 67.0 ms: 1.16x faster                                                           |
| django_template            | 36.9 ms                                                         | 32.0 ms: 1.15x faster                                                           |
| mdp                        | 1.91 sec                                                        | 1.67 sec: 1.15x faster                                                          |
| scimark_lu                 | 93.2 ms                                                         | 82.1 ms: 1.14x faster                                                           |
| sqlglot_optimize           | 48.5 ms                                                         | 43.0 ms: 1.13x faster                                                           |
| 2to3                       | 280 ms                                                          | 250 ms: 1.12x faster                                                            |
| meteor_contest             | 86.9 ms                                                         | 78.9 ms: 1.10x faster                                                           |
| sympy_integrate            | 17.5 ms                                                         | 16.0 ms: 1.10x faster                                                           |
| xml_etree_parse            | 113 ms                                                          | 104 ms: 1.09x faster                                                            |
| sympy_sum                  | 123 ms                                                          | 113 ms: 1.09x faster                                                            |
| bench_thread_pool          | 1.10 ms                                                         | 1.02 ms: 1.08x faster                                                           |
| sympy_str                  | 240 ms                                                          | 223 ms: 1.08x faster                                                            |
| json_dumps                 | 7.40 ms                                                         | 6.89 ms: 1.07x faster                                                           |
| regex_compile              | 129 ms                                                          | 121 ms: 1.07x faster                                                            |
| regex_effbot               | 2.04 ms                                                         | 1.93 ms: 1.06x faster                                                           |
| async_generators           | 313 ms                                                          | 297 ms: 1.06x faster                                                            |
| regex_dna                  | 127 ms                                                          | 120 ms: 1.05x faster                                                            |
| bench_mp_pool              | 75.4 ms                                                         | 71.7 ms: 1.05x faster                                                           |
| sqlite_synth               | 2.07 us                                                         | 2.01 us: 1.03x faster                                                           |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 17.3 sec: 1.02x faster                                                          |
| pathlib                    | 91.4 ms                                                         | 89.7 ms: 1.02x faster                                                           |
| docutils                   | 1.98 sec                                                        | 1.95 sec: 1.02x faster                                                          |
| python_startup_no_site     | 19.1 ms                                                         | 18.8 ms: 1.02x faster                                                           |
| pickle_list                | 3.37 us                                                         | 3.32 us: 1.02x faster                                                           |
| sympy_expand               | 398 ms                                                          | 393 ms: 1.01x faster                                                            |
| pidigits                   | 199 ms                                                          | 198 ms: 1.01x faster                                                            |
| json_loads                 | 20.4 us                                                         | 20.5 us: 1.01x slower                                                           |
| gc_traversal               | 1.44 ms                                                         | 1.45 ms: 1.01x slower                                                           |
| unpickle                   | 9.71 us                                                         | 9.90 us: 1.02x slower                                                           |
| tornado_http               | 105 ms                                                          | 107 ms: 1.02x slower                                                            |
| unpickle_list              | 2.95 us                                                         | 3.02 us: 1.03x slower                                                           |
| pickle_dict                | 19.9 us                                                         | 20.5 us: 1.03x slower                                                           |
| telco                      | 5.51 ms                                                         | 5.67 ms: 1.03x slower                                                           |
| json                       | 4.15 ms                                                         | 4.27 ms: 1.03x slower                                                           |
| regex_v8                   | 15.0 ms                                                         | 16.3 ms: 1.08x slower                                                           |
| create_gc_cycles           | 652 us                                                          | 750 us: 1.15x slower                                                            |
| typing_runtime_protocols   | 126 us                                                          | 147 us: 1.17x slower                                                            |
| asyncio_tcp                | 662 ms                                                          | 807 ms: 1.22x slower                                                            |
| sqlglot_normalize          | 100 ms                                                          | 220 ms: 2.19x slower                                                            |
| coverage                   | 48.4 ms                                                         | 418 ms: 8.62x slower                                                            |
| Geometric mean             | (ref)                                                           | 1.12x faster                                                                    |

Benchmark hidden because not significant (2): pickle, python_startup
Ignored benchmarks (7) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240427-3.13.0a6+-51aefc5-PYTHON_UOPS/bm-20240427-pythonperf1_win32-x86-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.14x
- 95% likely to have a speedup of 1.13x
- 99% likely to have a speedup of 1.11x

# Memory
- memory change: unknown