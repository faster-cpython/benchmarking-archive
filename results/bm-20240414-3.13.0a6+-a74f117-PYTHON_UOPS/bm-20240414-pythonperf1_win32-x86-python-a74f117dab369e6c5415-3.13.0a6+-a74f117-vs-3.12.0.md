# Results vs. 3.12.0

- fork: python
- ref: a74f117dab369e6c5415
- machine: windows-x86
- commit hash: a74f117
- commit date: 2024-04-14
- overall geometric mean: 1.13x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 245 ms: 1.14x faster                                                            |
| chameleon      | 7.75 ms                                                         | 5.70 ms: 1.36x faster                                                           |
| docutils       | 1.98 sec                                                        | 1.91 sec: 1.04x faster                                                          |
| tornado_http   | 105 ms                                                          | 97.7 ms: 1.07x faster                                                           |
| Geometric mean | (ref)                                                           | 1.15x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 350 ms                                                          | 255 ms: 1.37x faster                                                            |
| async_tree_none_tg         | 278 ms                                                          | 206 ms: 1.35x faster                                                            |
| async_tree_memoization     | 364 ms                                                          | 274 ms: 1.33x faster                                                            |
| async_tree_none            | 298 ms                                                          | 226 ms: 1.32x faster                                                            |
| async_tree_io              | 693 ms                                                          | 531 ms: 1.30x faster                                                            |
| async_tree_io_tg           | 677 ms                                                          | 529 ms: 1.28x faster                                                            |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 451 ms: 1.21x faster                                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 472 ms: 1.19x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.29x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 127 ms                                                          | 82.9 ms: 1.53x faster                                                           |
| float          | 76.7 ms                                                         | 61.1 ms: 1.25x faster                                                           |
| pidigits       | 199 ms                                                          | 197 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                           | 1.25x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_effbot   | 2.04 ms                                                         | 1.90 ms: 1.07x faster                                                           |
| regex_compile  | 129 ms                                                          | 125 ms: 1.03x faster                                                            |
| regex_dna      | 127 ms                                                          | 123 ms: 1.03x faster                                                            |
| regex_v8       | 15.0 ms                                                         | 16.2 ms: 1.07x slower                                                           |
| Geometric mean | (ref)                                                           | 1.02x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_pure_python   | 286 us                                                          | 211 us: 1.36x faster                                                            |
| tomli_loads          | 2.20 sec                                                        | 1.63 sec: 1.35x faster                                                          |
| xml_etree_process    | 53.2 ms                                                         | 42.8 ms: 1.24x faster                                                           |
| unpickle_pure_python | 210 us                                                          | 176 us: 1.19x faster                                                            |
| xml_etree_generate   | 72.1 ms                                                         | 61.0 ms: 1.18x faster                                                           |
| xml_etree_iterparse  | 77.6 ms                                                         | 67.9 ms: 1.14x faster                                                           |
| json_dumps           | 7.40 ms                                                         | 6.64 ms: 1.11x faster                                                           |
| unpickle_list        | 2.95 us                                                         | 2.79 us: 1.05x faster                                                           |
| xml_etree_parse      | 113 ms                                                          | 108 ms: 1.04x faster                                                            |
| pickle_list          | 3.37 us                                                         | 3.29 us: 1.02x faster                                                           |
| json_loads           | 20.4 us                                                         | 20.1 us: 1.01x faster                                                           |
| unpickle             | 9.71 us                                                         | 9.84 us: 1.01x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.12x faster                                                                    |

Benchmark hidden because not significant (2): pickle, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 19.1 ms                                                         | 18.8 ms: 1.01x faster                                                           |
| python_startup         | 22.4 ms                                                         | 22.6 ms: 1.01x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.00x faster                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|-----------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako      | 9.96 ms                                                         | 7.60 ms: 1.31x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| generators                 | 38.5 ms                                                         | 22.8 ms: 1.69x faster                                                           |
| logging_silent             | 101 ns                                                          | 60.5 ns: 1.67x faster                                                           |
| nbody                      | 127 ms                                                          | 82.9 ms: 1.53x faster                                                           |
| deepcopy_memo              | 38.4 us                                                         | 25.6 us: 1.50x faster                                                           |
| coroutines                 | 20.9 ms                                                         | 14.5 ms: 1.44x faster                                                           |
| raytrace                   | 308 ms                                                          | 215 ms: 1.44x faster                                                            |
| scimark_sor                | 130 ms                                                          | 94.4 ms: 1.38x faster                                                           |
| async_tree_memoization_tg  | 350 ms                                                          | 255 ms: 1.37x faster                                                            |
| chameleon                  | 7.75 ms                                                         | 5.70 ms: 1.36x faster                                                           |
| pickle_pure_python         | 286 us                                                          | 211 us: 1.36x faster                                                            |
| richards_super             | 46.5 ms                                                         | 34.4 ms: 1.35x faster                                                           |
| tomli_loads                | 2.20 sec                                                        | 1.63 sec: 1.35x faster                                                          |
| async_tree_none_tg         | 278 ms                                                          | 206 ms: 1.35x faster                                                            |
| richards                   | 41.3 ms                                                         | 30.7 ms: 1.34x faster                                                           |
| deltablue                  | 3.58 ms                                                         | 2.67 ms: 1.34x faster                                                           |
| deepcopy_reduce            | 3.23 us                                                         | 2.41 us: 1.34x faster                                                           |
| deepcopy                   | 360 us                                                          | 269 us: 1.34x faster                                                            |
| typing_runtime_protocols   | 126 us                                                          | 94.5 us: 1.34x faster                                                           |
| async_tree_memoization     | 364 ms                                                          | 274 ms: 1.33x faster                                                            |
| comprehensions             | 19.2 us                                                         | 14.5 us: 1.32x faster                                                           |
| async_tree_none            | 298 ms                                                          | 226 ms: 1.32x faster                                                            |
| mako                       | 9.96 ms                                                         | 7.60 ms: 1.31x faster                                                           |
| async_tree_io              | 693 ms                                                          | 531 ms: 1.30x faster                                                            |
| chaos                      | 69.4 ms                                                         | 53.4 ms: 1.30x faster                                                           |
| sqlglot_parse              | 1.25 ms                                                         | 965 us: 1.29x faster                                                            |
| async_tree_io_tg           | 677 ms                                                          | 529 ms: 1.28x faster                                                            |
| sqlglot_transpile          | 1.53 ms                                                         | 1.20 ms: 1.27x faster                                                           |
| logging_simple             | 9.75 us                                                         | 7.75 us: 1.26x faster                                                           |
| float                      | 76.7 ms                                                         | 61.1 ms: 1.25x faster                                                           |
| xml_etree_process          | 53.2 ms                                                         | 42.8 ms: 1.24x faster                                                           |
| logging_format             | 10.4 us                                                         | 8.40 us: 1.24x faster                                                           |
| scimark_monte_carlo        | 66.4 ms                                                         | 53.8 ms: 1.23x faster                                                           |
| scimark_fft                | 271 ms                                                          | 223 ms: 1.22x faster                                                            |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 451 ms: 1.21x faster                                                            |
| nqueens                    | 93.7 ms                                                         | 78.2 ms: 1.20x faster                                                           |
| fannkuch                   | 354 ms                                                          | 295 ms: 1.20x faster                                                            |
| spectral_norm              | 104 ms                                                          | 86.7 ms: 1.20x faster                                                           |
| unpickle_pure_python       | 210 us                                                          | 176 us: 1.19x faster                                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 472 ms: 1.19x faster                                                            |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 3.23 ms: 1.19x faster                                                           |
| pyflate                    | 424 ms                                                          | 355 ms: 1.19x faster                                                            |
| xml_etree_generate         | 72.1 ms                                                         | 61.0 ms: 1.18x faster                                                           |
| pycparser                  | 978 ms                                                          | 827 ms: 1.18x faster                                                            |
| crypto_pyaes               | 69.2 ms                                                         | 59.0 ms: 1.17x faster                                                           |
| mdp                        | 1.91 sec                                                        | 1.63 sec: 1.17x faster                                                          |
| hexiom                     | 6.82 ms                                                         | 5.89 ms: 1.16x faster                                                           |
| go                         | 137 ms                                                          | 120 ms: 1.15x faster                                                            |
| pprint_pformat             | 1.50 sec                                                        | 1.31 sec: 1.15x faster                                                          |
| 2to3                       | 280 ms                                                          | 245 ms: 1.14x faster                                                            |
| xml_etree_iterparse        | 77.6 ms                                                         | 67.9 ms: 1.14x faster                                                           |
| pprint_safe_repr           | 721 ms                                                          | 635 ms: 1.13x faster                                                            |
| sqlglot_optimize           | 48.5 ms                                                         | 43.3 ms: 1.12x faster                                                           |
| json_dumps                 | 7.40 ms                                                         | 6.64 ms: 1.11x faster                                                           |
| bench_thread_pool          | 1.10 ms                                                         | 1.00 ms: 1.10x faster                                                           |
| sympy_integrate            | 17.5 ms                                                         | 16.0 ms: 1.10x faster                                                           |
| meteor_contest             | 86.9 ms                                                         | 79.2 ms: 1.10x faster                                                           |
| scimark_lu                 | 93.2 ms                                                         | 85.1 ms: 1.10x faster                                                           |
| pathlib                    | 91.4 ms                                                         | 83.6 ms: 1.09x faster                                                           |
| sympy_sum                  | 123 ms                                                          | 113 ms: 1.09x faster                                                            |
| tornado_http               | 105 ms                                                          | 97.7 ms: 1.07x faster                                                           |
| regex_effbot               | 2.04 ms                                                         | 1.90 ms: 1.07x faster                                                           |
| sympy_str                  | 240 ms                                                          | 224 ms: 1.07x faster                                                            |
| sqlite_synth               | 2.07 us                                                         | 1.94 us: 1.07x faster                                                           |
| unpickle_list              | 2.95 us                                                         | 2.79 us: 1.05x faster                                                           |
| asyncio_tcp                | 662 ms                                                          | 628 ms: 1.05x faster                                                            |
| bench_mp_pool              | 75.4 ms                                                         | 71.6 ms: 1.05x faster                                                           |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 16.9 sec: 1.05x faster                                                          |
| xml_etree_parse            | 113 ms                                                          | 108 ms: 1.04x faster                                                            |
| async_generators           | 313 ms                                                          | 301 ms: 1.04x faster                                                            |
| docutils                   | 1.98 sec                                                        | 1.91 sec: 1.04x faster                                                          |
| regex_compile              | 129 ms                                                          | 125 ms: 1.03x faster                                                            |
| regex_dna                  | 127 ms                                                          | 123 ms: 1.03x faster                                                            |
| pickle_list                | 3.37 us                                                         | 3.29 us: 1.02x faster                                                           |
| sympy_expand               | 398 ms                                                          | 390 ms: 1.02x faster                                                            |
| json_loads                 | 20.4 us                                                         | 20.1 us: 1.01x faster                                                           |
| pidigits                   | 199 ms                                                          | 197 ms: 1.01x faster                                                            |
| python_startup_no_site     | 19.1 ms                                                         | 18.8 ms: 1.01x faster                                                           |
| json                       | 4.15 ms                                                         | 4.12 ms: 1.01x faster                                                           |
| gc_traversal               | 1.44 ms                                                         | 1.43 ms: 1.01x faster                                                           |
| python_startup             | 22.4 ms                                                         | 22.6 ms: 1.01x slower                                                           |
| unpickle                   | 9.71 us                                                         | 9.84 us: 1.01x slower                                                           |
| regex_v8                   | 15.0 ms                                                         | 16.2 ms: 1.07x slower                                                           |
| create_gc_cycles           | 652 us                                                          | 735 us: 1.13x slower                                                            |
| telco                      | 5.51 ms                                                         | 6.34 ms: 1.15x slower                                                           |
| sqlglot_normalize          | 100 ms                                                          | 225 ms: 2.24x slower                                                            |
| coverage                   | 48.4 ms                                                         | 507 ms: 10.47x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.13x faster                                                                    |

Benchmark hidden because not significant (2): pickle, pickle_dict
Ignored benchmarks (8) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, django_template, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240414-3.13.0a6+-a74f117-PYTHON_UOPS/bm-20240414-pythonperf1_win32-x86-python-a74f117dab369e6c5415-3.13.0a6+-a74f117.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.14x
- 95% likely to have a speedup of 1.13x
- 99% likely to have a speedup of 1.11x

# Memory
- memory change: unknown