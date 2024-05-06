# Results vs. 3.12.0

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: windows-x86
- commit hash: 4675ce8
- commit date: 2024-04-08
- overall geometric mean: 1.21x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 230 ms: 1.22x faster                                                                      |
| chameleon      | 7.75 ms                                                         | 5.67 ms: 1.37x faster                                                                     |
| docutils       | 1.98 sec                                                        | 1.77 sec: 1.12x faster                                                                    |
| tornado_http   | 105 ms                                                          | 91.6 ms: 1.15x faster                                                                     |
| Geometric mean | (ref)                                                           | 1.21x faster                                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 350 ms                                                          | 244 ms: 1.43x faster                                                                      |
| async_tree_none_tg         | 278 ms                                                          | 199 ms: 1.40x faster                                                                      |
| async_tree_memoization     | 364 ms                                                          | 262 ms: 1.39x faster                                                                      |
| async_tree_none            | 298 ms                                                          | 216 ms: 1.37x faster                                                                      |
| async_tree_io              | 693 ms                                                          | 510 ms: 1.36x faster                                                                      |
| async_tree_io_tg           | 677 ms                                                          | 514 ms: 1.32x faster                                                                      |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 439 ms: 1.24x faster                                                                      |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 457 ms: 1.23x faster                                                                      |
| Geometric mean             | (ref)                                                           | 1.34x faster                                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| nbody          | 127 ms                                                          | 75.1 ms: 1.69x faster                                                                     |
| float          | 76.7 ms                                                         | 52.7 ms: 1.46x faster                                                                     |
| pidigits       | 199 ms                                                          | 196 ms: 1.02x faster                                                                      |
| Geometric mean | (ref)                                                           | 1.36x faster                                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 96.3 ms: 1.34x faster                                                                     |
| regex_dna      | 127 ms                                                          | 117 ms: 1.09x faster                                                                      |
| regex_effbot   | 2.04 ms                                                         | 1.88 ms: 1.08x faster                                                                     |
| regex_v8       | 15.0 ms                                                         | 16.1 ms: 1.07x slower                                                                     |
| Geometric mean | (ref)                                                           | 1.10x faster                                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| unpickle_pure_python | 210 us                                                          | 145 us: 1.45x faster                                                                      |
| pickle_pure_python   | 286 us                                                          | 206 us: 1.39x faster                                                                      |
| tomli_loads          | 2.20 sec                                                        | 1.59 sec: 1.39x faster                                                                    |
| xml_etree_process    | 53.2 ms                                                         | 42.9 ms: 1.24x faster                                                                     |
| xml_etree_generate   | 72.1 ms                                                         | 60.1 ms: 1.20x faster                                                                     |
| xml_etree_iterparse  | 77.6 ms                                                         | 65.1 ms: 1.19x faster                                                                     |
| json_dumps           | 7.40 ms                                                         | 6.55 ms: 1.13x faster                                                                     |
| xml_etree_parse      | 113 ms                                                          | 106 ms: 1.06x faster                                                                      |
| pickle_list          | 3.37 us                                                         | 3.21 us: 1.05x faster                                                                     |
| json_loads           | 20.4 us                                                         | 20.1 us: 1.01x faster                                                                     |
| pickle_dict          | 19.9 us                                                         | 20.1 us: 1.01x slower                                                                     |
| pickle               | 7.79 us                                                         | 7.88 us: 1.01x slower                                                                     |
| unpickle             | 9.71 us                                                         | 9.87 us: 1.02x slower                                                                     |
| unpickle_list        | 2.95 us                                                         | 3.00 us: 1.02x slower                                                                     |
| Geometric mean       | (ref)                                                           | 1.14x faster                                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                         | 22.2 ms: 1.01x faster                                                                     |
| python_startup_no_site | 19.1 ms                                                         | 19.8 ms: 1.04x slower                                                                     |
| Geometric mean         | (ref)                                                           | 1.02x slower                                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|-----------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| mako      | 9.96 ms                                                         | 6.76 ms: 1.47x faster                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------------------:|
| logging_silent             | 101 ns                                                          | 57.5 ns: 1.76x faster                                                                     |
| generators                 | 38.5 ms                                                         | 22.5 ms: 1.71x faster                                                                     |
| nbody                      | 127 ms                                                          | 75.1 ms: 1.69x faster                                                                     |
| deepcopy_memo              | 38.4 us                                                         | 22.8 us: 1.69x faster                                                                     |
| deltablue                  | 3.58 ms                                                         | 2.14 ms: 1.67x faster                                                                     |
| scimark_sor                | 130 ms                                                          | 79.0 ms: 1.64x faster                                                                     |
| raytrace                   | 308 ms                                                          | 188 ms: 1.64x faster                                                                      |
| comprehensions             | 19.2 us                                                         | 11.8 us: 1.62x faster                                                                     |
| hexiom                     | 6.82 ms                                                         | 4.22 ms: 1.62x faster                                                                     |
| scimark_lu                 | 93.2 ms                                                         | 59.7 ms: 1.56x faster                                                                     |
| spectral_norm              | 104 ms                                                          | 68.7 ms: 1.51x faster                                                                     |
| chaos                      | 69.4 ms                                                         | 46.8 ms: 1.48x faster                                                                     |
| mako                       | 9.96 ms                                                         | 6.76 ms: 1.47x faster                                                                     |
| coroutines                 | 20.9 ms                                                         | 14.2 ms: 1.47x faster                                                                     |
| scimark_monte_carlo        | 66.4 ms                                                         | 45.5 ms: 1.46x faster                                                                     |
| float                      | 76.7 ms                                                         | 52.7 ms: 1.46x faster                                                                     |
| unpickle_pure_python       | 210 us                                                          | 145 us: 1.45x faster                                                                      |
| async_tree_memoization_tg  | 350 ms                                                          | 244 ms: 1.43x faster                                                                      |
| go                         | 137 ms                                                          | 96.6 ms: 1.42x faster                                                                     |
| sqlglot_parse              | 1.25 ms                                                         | 878 us: 1.42x faster                                                                      |
| async_tree_none_tg         | 278 ms                                                          | 199 ms: 1.40x faster                                                                      |
| richards                   | 41.3 ms                                                         | 29.7 ms: 1.39x faster                                                                     |
| pyflate                    | 424 ms                                                          | 304 ms: 1.39x faster                                                                      |
| pickle_pure_python         | 286 us                                                          | 206 us: 1.39x faster                                                                      |
| sqlglot_transpile          | 1.53 ms                                                         | 1.10 ms: 1.39x faster                                                                     |
| async_tree_memoization     | 364 ms                                                          | 262 ms: 1.39x faster                                                                      |
| tomli_loads                | 2.20 sec                                                        | 1.59 sec: 1.39x faster                                                                    |
| richards_super             | 46.5 ms                                                         | 33.6 ms: 1.38x faster                                                                     |
| async_tree_none            | 298 ms                                                          | 216 ms: 1.37x faster                                                                      |
| chameleon                  | 7.75 ms                                                         | 5.67 ms: 1.37x faster                                                                     |
| typing_runtime_protocols   | 126 us                                                          | 92.8 us: 1.36x faster                                                                     |
| async_tree_io              | 693 ms                                                          | 510 ms: 1.36x faster                                                                      |
| regex_compile              | 129 ms                                                          | 96.3 ms: 1.34x faster                                                                     |
| scimark_fft                | 271 ms                                                          | 204 ms: 1.33x faster                                                                      |
| deepcopy_reduce            | 3.23 us                                                         | 2.43 us: 1.33x faster                                                                     |
| deepcopy                   | 360 us                                                          | 272 us: 1.33x faster                                                                      |
| nqueens                    | 93.7 ms                                                         | 70.9 ms: 1.32x faster                                                                     |
| pprint_pformat             | 1.50 sec                                                        | 1.14 sec: 1.32x faster                                                                    |
| async_tree_io_tg           | 677 ms                                                          | 514 ms: 1.32x faster                                                                      |
| logging_simple             | 9.75 us                                                         | 7.54 us: 1.29x faster                                                                     |
| pprint_safe_repr           | 721 ms                                                          | 558 ms: 1.29x faster                                                                      |
| fannkuch                   | 354 ms                                                          | 275 ms: 1.29x faster                                                                      |
| crypto_pyaes               | 69.2 ms                                                         | 53.9 ms: 1.28x faster                                                                     |
| logging_format             | 10.4 us                                                         | 8.12 us: 1.28x faster                                                                     |
| pycparser                  | 978 ms                                                          | 767 ms: 1.28x faster                                                                      |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 3.03 ms: 1.27x faster                                                                     |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 439 ms: 1.24x faster                                                                      |
| xml_etree_process          | 53.2 ms                                                         | 42.9 ms: 1.24x faster                                                                     |
| sympy_integrate            | 17.5 ms                                                         | 14.2 ms: 1.24x faster                                                                     |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 457 ms: 1.23x faster                                                                      |
| sqlglot_optimize           | 48.5 ms                                                         | 39.6 ms: 1.22x faster                                                                     |
| sympy_sum                  | 123 ms                                                          | 101 ms: 1.22x faster                                                                      |
| 2to3                       | 280 ms                                                          | 230 ms: 1.22x faster                                                                      |
| xml_etree_generate         | 72.1 ms                                                         | 60.1 ms: 1.20x faster                                                                     |
| sympy_str                  | 240 ms                                                          | 200 ms: 1.20x faster                                                                      |
| xml_etree_iterparse        | 77.6 ms                                                         | 65.1 ms: 1.19x faster                                                                     |
| mdp                        | 1.91 sec                                                        | 1.62 sec: 1.18x faster                                                                    |
| meteor_contest             | 86.9 ms                                                         | 75.5 ms: 1.15x faster                                                                     |
| tornado_http               | 105 ms                                                          | 91.6 ms: 1.15x faster                                                                     |
| sympy_expand               | 398 ms                                                          | 349 ms: 1.14x faster                                                                      |
| json_dumps                 | 7.40 ms                                                         | 6.55 ms: 1.13x faster                                                                     |
| async_generators           | 313 ms                                                          | 278 ms: 1.13x faster                                                                      |
| bench_thread_pool          | 1.10 ms                                                         | 979 us: 1.13x faster                                                                      |
| docutils                   | 1.98 sec                                                        | 1.77 sec: 1.12x faster                                                                    |
| bench_mp_pool              | 75.4 ms                                                         | 68.0 ms: 1.11x faster                                                                     |
| sqlite_synth               | 2.07 us                                                         | 1.90 us: 1.09x faster                                                                     |
| regex_dna                  | 127 ms                                                          | 117 ms: 1.09x faster                                                                      |
| regex_effbot               | 2.04 ms                                                         | 1.88 ms: 1.08x faster                                                                     |
| pathlib                    | 91.4 ms                                                         | 85.6 ms: 1.07x faster                                                                     |
| xml_etree_parse            | 113 ms                                                          | 106 ms: 1.06x faster                                                                      |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 16.8 sec: 1.05x faster                                                                    |
| pickle_list                | 3.37 us                                                         | 3.21 us: 1.05x faster                                                                     |
| json                       | 4.15 ms                                                         | 4.04 ms: 1.03x faster                                                                     |
| pidigits                   | 199 ms                                                          | 196 ms: 1.02x faster                                                                      |
| gc_traversal               | 1.44 ms                                                         | 1.42 ms: 1.01x faster                                                                     |
| json_loads                 | 20.4 us                                                         | 20.1 us: 1.01x faster                                                                     |
| python_startup             | 22.4 ms                                                         | 22.2 ms: 1.01x faster                                                                     |
| pickle_dict                | 19.9 us                                                         | 20.1 us: 1.01x slower                                                                     |
| pickle                     | 7.79 us                                                         | 7.88 us: 1.01x slower                                                                     |
| unpickle                   | 9.71 us                                                         | 9.87 us: 1.02x slower                                                                     |
| unpickle_list              | 2.95 us                                                         | 3.00 us: 1.02x slower                                                                     |
| python_startup_no_site     | 19.1 ms                                                         | 19.8 ms: 1.04x slower                                                                     |
| regex_v8                   | 15.0 ms                                                         | 16.1 ms: 1.07x slower                                                                     |
| telco                      | 5.51 ms                                                         | 6.00 ms: 1.09x slower                                                                     |
| create_gc_cycles           | 652 us                                                          | 733 us: 1.13x slower                                                                      |
| sqlglot_normalize          | 100 ms                                                          | 206 ms: 2.06x slower                                                                      |
| coverage                   | 48.4 ms                                                         | 507 ms: 10.47x slower                                                                     |
| Geometric mean             | (ref)                                                           | 1.21x faster                                                                              |

Benchmark hidden because not significant (1): asyncio_tcp
Ignored benchmarks (8) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, django_template, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240408-3.13.0a5+-4675ce8/bm-20240408-pythonperf1_win32-x86-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.22x
- 95% likely to have a speedup of 1.22x
- 99% likely to have a speedup of 1.20x

# Memory
- memory change: unknown