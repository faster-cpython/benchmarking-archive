# Results vs. 3.12.0

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-x86
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.21x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 226 ms: 1.24x faster                                                            |
| chameleon      | 7.75 ms                                                         | 5.65 ms: 1.37x faster                                                           |
| docutils       | 1.98 sec                                                        | 1.79 sec: 1.11x faster                                                          |
| tornado_http   | 105 ms                                                          | 92.5 ms: 1.14x faster                                                           |
| Geometric mean | (ref)                                                           | 1.21x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 350 ms                                                          | 249 ms: 1.41x faster                                                            |
| async_tree_memoization     | 364 ms                                                          | 265 ms: 1.37x faster                                                            |
| async_tree_none_tg         | 278 ms                                                          | 204 ms: 1.36x faster                                                            |
| async_tree_none            | 298 ms                                                          | 222 ms: 1.34x faster                                                            |
| async_tree_io              | 693 ms                                                          | 519 ms: 1.34x faster                                                            |
| async_tree_io_tg           | 677 ms                                                          | 522 ms: 1.30x faster                                                            |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 449 ms: 1.22x faster                                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 464 ms: 1.22x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.32x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 127 ms                                                          | 78.4 ms: 1.62x faster                                                           |
| float          | 76.7 ms                                                         | 53.4 ms: 1.44x faster                                                           |
| pidigits       | 199 ms                                                          | 197 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                           | 1.33x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 95.9 ms: 1.35x faster                                                           |
| regex_dna      | 127 ms                                                          | 117 ms: 1.09x faster                                                            |
| regex_effbot   | 2.04 ms                                                         | 1.88 ms: 1.08x faster                                                           |
| regex_v8       | 15.0 ms                                                         | 16.0 ms: 1.06x slower                                                           |
| Geometric mean | (ref)                                                           | 1.11x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 210 us                                                          | 137 us: 1.54x faster                                                            |
| pickle_pure_python   | 286 us                                                          | 203 us: 1.41x faster                                                            |
| tomli_loads          | 2.20 sec                                                        | 1.58 sec: 1.39x faster                                                          |
| xml_etree_process    | 53.2 ms                                                         | 42.6 ms: 1.25x faster                                                           |
| xml_etree_iterparse  | 77.6 ms                                                         | 65.9 ms: 1.18x faster                                                           |
| xml_etree_generate   | 72.1 ms                                                         | 62.0 ms: 1.16x faster                                                           |
| json_dumps           | 7.40 ms                                                         | 6.60 ms: 1.12x faster                                                           |
| unpickle_list        | 2.95 us                                                         | 2.78 us: 1.06x faster                                                           |
| xml_etree_parse      | 113 ms                                                          | 108 ms: 1.05x faster                                                            |
| pickle_list          | 3.37 us                                                         | 3.24 us: 1.04x faster                                                           |
| json_loads           | 20.4 us                                                         | 20.1 us: 1.01x faster                                                           |
| pickle               | 7.79 us                                                         | 8.02 us: 1.03x slower                                                           |
| unpickle             | 9.71 us                                                         | 10.1 us: 1.04x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.14x faster                                                                    |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 19.1 ms                                                         | 18.0 ms: 1.06x faster                                                           |
| python_startup         | 22.4 ms                                                         | 21.9 ms: 1.02x faster                                                           |
| Geometric mean         | (ref)                                                           | 1.04x faster                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|-----------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako      | 9.96 ms                                                         | 6.74 ms: 1.48x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| generators                 | 38.5 ms                                                         | 22.2 ms: 1.74x faster                                                           |
| raytrace                   | 308 ms                                                          | 180 ms: 1.71x faster                                                            |
| deltablue                  | 3.58 ms                                                         | 2.12 ms: 1.69x faster                                                           |
| deepcopy_memo              | 38.4 us                                                         | 22.7 us: 1.69x faster                                                           |
| scimark_sor                | 130 ms                                                          | 77.9 ms: 1.67x faster                                                           |
| logging_silent             | 101 ns                                                          | 61.7 ns: 1.64x faster                                                           |
| comprehensions             | 19.2 us                                                         | 11.7 us: 1.63x faster                                                           |
| hexiom                     | 6.82 ms                                                         | 4.19 ms: 1.63x faster                                                           |
| nbody                      | 127 ms                                                          | 78.4 ms: 1.62x faster                                                           |
| unpickle_pure_python       | 210 us                                                          | 137 us: 1.54x faster                                                            |
| chaos                      | 69.4 ms                                                         | 45.3 ms: 1.53x faster                                                           |
| spectral_norm              | 104 ms                                                          | 68.5 ms: 1.52x faster                                                           |
| scimark_lu                 | 93.2 ms                                                         | 61.9 ms: 1.51x faster                                                           |
| mako                       | 9.96 ms                                                         | 6.74 ms: 1.48x faster                                                           |
| coroutines                 | 20.9 ms                                                         | 14.3 ms: 1.46x faster                                                           |
| sqlglot_parse              | 1.25 ms                                                         | 862 us: 1.45x faster                                                            |
| scimark_monte_carlo        | 66.4 ms                                                         | 46.0 ms: 1.45x faster                                                           |
| float                      | 76.7 ms                                                         | 53.4 ms: 1.44x faster                                                           |
| richards                   | 41.3 ms                                                         | 29.0 ms: 1.42x faster                                                           |
| go                         | 137 ms                                                          | 96.6 ms: 1.42x faster                                                           |
| richards_super             | 46.5 ms                                                         | 32.8 ms: 1.42x faster                                                           |
| async_tree_memoization_tg  | 350 ms                                                          | 249 ms: 1.41x faster                                                            |
| pickle_pure_python         | 286 us                                                          | 203 us: 1.41x faster                                                            |
| sqlglot_transpile          | 1.53 ms                                                         | 1.09 ms: 1.41x faster                                                           |
| tomli_loads                | 2.20 sec                                                        | 1.58 sec: 1.39x faster                                                          |
| async_tree_memoization     | 364 ms                                                          | 265 ms: 1.37x faster                                                            |
| chameleon                  | 7.75 ms                                                         | 5.65 ms: 1.37x faster                                                           |
| pyflate                    | 424 ms                                                          | 309 ms: 1.37x faster                                                            |
| async_tree_none_tg         | 278 ms                                                          | 204 ms: 1.36x faster                                                            |
| typing_runtime_protocols   | 126 us                                                          | 93.0 us: 1.36x faster                                                           |
| nqueens                    | 93.7 ms                                                         | 69.3 ms: 1.35x faster                                                           |
| regex_compile              | 129 ms                                                          | 95.9 ms: 1.35x faster                                                           |
| async_tree_none            | 298 ms                                                          | 222 ms: 1.34x faster                                                            |
| deepcopy                   | 360 us                                                          | 269 us: 1.34x faster                                                            |
| async_tree_io              | 693 ms                                                          | 519 ms: 1.34x faster                                                            |
| fannkuch                   | 354 ms                                                          | 266 ms: 1.33x faster                                                            |
| pprint_pformat             | 1.50 sec                                                        | 1.14 sec: 1.32x faster                                                          |
| deepcopy_reduce            | 3.23 us                                                         | 2.48 us: 1.30x faster                                                           |
| logging_simple             | 9.75 us                                                         | 7.49 us: 1.30x faster                                                           |
| async_tree_io_tg           | 677 ms                                                          | 522 ms: 1.30x faster                                                            |
| logging_format             | 10.4 us                                                         | 8.04 us: 1.29x faster                                                           |
| pprint_safe_repr           | 721 ms                                                          | 558 ms: 1.29x faster                                                            |
| pycparser                  | 978 ms                                                          | 760 ms: 1.29x faster                                                            |
| scimark_fft                | 271 ms                                                          | 211 ms: 1.28x faster                                                            |
| sqlglot_optimize           | 48.5 ms                                                         | 38.4 ms: 1.26x faster                                                           |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 3.07 ms: 1.26x faster                                                           |
| crypto_pyaes               | 69.2 ms                                                         | 55.1 ms: 1.26x faster                                                           |
| xml_etree_process          | 53.2 ms                                                         | 42.6 ms: 1.25x faster                                                           |
| 2to3                       | 280 ms                                                          | 226 ms: 1.24x faster                                                            |
| sympy_integrate            | 17.5 ms                                                         | 14.2 ms: 1.24x faster                                                           |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 449 ms: 1.22x faster                                                            |
| mdp                        | 1.91 sec                                                        | 1.57 sec: 1.22x faster                                                          |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 464 ms: 1.22x faster                                                            |
| sympy_sum                  | 123 ms                                                          | 101 ms: 1.21x faster                                                            |
| sympy_str                  | 240 ms                                                          | 199 ms: 1.20x faster                                                            |
| xml_etree_iterparse        | 77.6 ms                                                         | 65.9 ms: 1.18x faster                                                           |
| xml_etree_generate         | 72.1 ms                                                         | 62.0 ms: 1.16x faster                                                           |
| sympy_expand               | 398 ms                                                          | 349 ms: 1.14x faster                                                            |
| tornado_http               | 105 ms                                                          | 92.5 ms: 1.14x faster                                                           |
| meteor_contest             | 86.9 ms                                                         | 76.7 ms: 1.13x faster                                                           |
| json_dumps                 | 7.40 ms                                                         | 6.60 ms: 1.12x faster                                                           |
| bench_thread_pool          | 1.10 ms                                                         | 986 us: 1.12x faster                                                            |
| bench_mp_pool              | 75.4 ms                                                         | 67.9 ms: 1.11x faster                                                           |
| docutils                   | 1.98 sec                                                        | 1.79 sec: 1.11x faster                                                          |
| pathlib                    | 91.4 ms                                                         | 83.4 ms: 1.10x faster                                                           |
| async_generators           | 313 ms                                                          | 287 ms: 1.09x faster                                                            |
| regex_dna                  | 127 ms                                                          | 117 ms: 1.09x faster                                                            |
| regex_effbot               | 2.04 ms                                                         | 1.88 ms: 1.08x faster                                                           |
| sqlite_synth               | 2.07 us                                                         | 1.91 us: 1.08x faster                                                           |
| unpickle_list              | 2.95 us                                                         | 2.78 us: 1.06x faster                                                           |
| python_startup_no_site     | 19.1 ms                                                         | 18.0 ms: 1.06x faster                                                           |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 16.8 sec: 1.05x faster                                                          |
| xml_etree_parse            | 113 ms                                                          | 108 ms: 1.05x faster                                                            |
| pickle_list                | 3.37 us                                                         | 3.24 us: 1.04x faster                                                           |
| asyncio_tcp                | 662 ms                                                          | 639 ms: 1.04x faster                                                            |
| json                       | 4.15 ms                                                         | 4.04 ms: 1.03x faster                                                           |
| python_startup             | 22.4 ms                                                         | 21.9 ms: 1.02x faster                                                           |
| json_loads                 | 20.4 us                                                         | 20.1 us: 1.01x faster                                                           |
| gc_traversal               | 1.44 ms                                                         | 1.42 ms: 1.01x faster                                                           |
| pidigits                   | 199 ms                                                          | 197 ms: 1.01x faster                                                            |
| pickle                     | 7.79 us                                                         | 8.02 us: 1.03x slower                                                           |
| unpickle                   | 9.71 us                                                         | 10.1 us: 1.04x slower                                                           |
| regex_v8                   | 15.0 ms                                                         | 16.0 ms: 1.06x slower                                                           |
| telco                      | 5.51 ms                                                         | 5.93 ms: 1.08x slower                                                           |
| create_gc_cycles           | 652 us                                                          | 723 us: 1.11x slower                                                            |
| sqlglot_normalize          | 100 ms                                                          | 200 ms: 1.99x slower                                                            |
| coverage                   | 48.4 ms                                                         | 503 ms: 10.38x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.21x faster                                                                    |

Benchmark hidden because not significant (1): pickle_dict
Ignored benchmarks (8) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, django_template, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240414-3.13.0a6+-a74f117/bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.23x
- 95% likely to have a speedup of 1.22x
- 99% likely to have a speedup of 1.20x

# Memory
- memory change: unknown