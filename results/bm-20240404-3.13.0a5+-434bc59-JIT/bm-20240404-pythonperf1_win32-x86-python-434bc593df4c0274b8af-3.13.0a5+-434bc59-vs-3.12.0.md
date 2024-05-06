# Results vs. 3.12.0

- fork: python
- ref: 434bc593df4c0274b8af
- machine: windows-x86
- commit hash: 434bc59
- commit date: 2024-04-04
- overall geometric mean: 1.10x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 258 ms: 1.08x faster                                                            |
| chameleon      | 7.75 ms                                                         | 6.05 ms: 1.28x faster                                                           |
| docutils       | 1.98 sec                                                        | 1.91 sec: 1.04x faster                                                          |
| tornado_http   | 105 ms                                                          | 95.3 ms: 1.10x faster                                                           |
| Geometric mean | (ref)                                                           | 1.12x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 350 ms                                                          | 265 ms: 1.32x faster                                                            |
| async_tree_none_tg         | 278 ms                                                          | 215 ms: 1.29x faster                                                            |
| async_tree_io              | 693 ms                                                          | 539 ms: 1.29x faster                                                            |
| async_tree_memoization     | 364 ms                                                          | 286 ms: 1.27x faster                                                            |
| async_tree_none            | 298 ms                                                          | 238 ms: 1.25x faster                                                            |
| async_tree_io_tg           | 677 ms                                                          | 543 ms: 1.25x faster                                                            |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 454 ms: 1.20x faster                                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 483 ms: 1.17x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.25x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 76.7 ms                                                         | 53.3 ms: 1.44x faster                                                           |
| nbody          | 127 ms                                                          | 101 ms: 1.26x faster                                                            |
| pidigits       | 199 ms                                                          | 199 ms: 1.00x faster                                                            |
| Geometric mean | (ref)                                                           | 1.22x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 112 ms: 1.16x faster                                                            |
| regex_dna      | 127 ms                                                          | 118 ms: 1.07x faster                                                            |
| regex_effbot   | 2.04 ms                                                         | 1.90 ms: 1.07x faster                                                           |
| regex_v8       | 15.0 ms                                                         | 16.3 ms: 1.08x slower                                                           |
| Geometric mean | (ref)                                                           | 1.05x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_pure_python   | 286 us                                                          | 223 us: 1.28x faster                                                            |
| tomli_loads          | 2.20 sec                                                        | 1.75 sec: 1.25x faster                                                          |
| xml_etree_process    | 53.2 ms                                                         | 43.0 ms: 1.24x faster                                                           |
| unpickle_pure_python | 210 us                                                          | 170 us: 1.23x faster                                                            |
| xml_etree_generate   | 72.1 ms                                                         | 60.7 ms: 1.19x faster                                                           |
| xml_etree_iterparse  | 77.6 ms                                                         | 65.4 ms: 1.19x faster                                                           |
| json_dumps           | 7.40 ms                                                         | 6.82 ms: 1.09x faster                                                           |
| pickle_list          | 3.37 us                                                         | 3.17 us: 1.06x faster                                                           |
| xml_etree_parse      | 113 ms                                                          | 108 ms: 1.05x faster                                                            |
| json_loads           | 20.4 us                                                         | 19.8 us: 1.03x faster                                                           |
| unpickle_list        | 2.95 us                                                         | 2.91 us: 1.01x faster                                                           |
| pickle               | 7.79 us                                                         | 7.87 us: 1.01x slower                                                           |
| unpickle             | 9.71 us                                                         | 9.86 us: 1.02x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.11x faster                                                                    |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                         | 24.6 ms: 1.10x slower                                                           |
| python_startup_no_site | 19.1 ms                                                         | 22.4 ms: 1.18x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.14x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|-----------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako      | 9.96 ms                                                         | 7.13 ms: 1.40x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| generators                 | 38.5 ms                                                         | 22.8 ms: 1.69x faster                                                           |
| logging_silent             | 101 ns                                                          | 60.1 ns: 1.68x faster                                                           |
| deepcopy_memo              | 38.4 us                                                         | 24.9 us: 1.54x faster                                                           |
| spectral_norm              | 104 ms                                                          | 71.5 ms: 1.45x faster                                                           |
| float                      | 76.7 ms                                                         | 53.3 ms: 1.44x faster                                                           |
| mako                       | 9.96 ms                                                         | 7.13 ms: 1.40x faster                                                           |
| coroutines                 | 20.9 ms                                                         | 15.0 ms: 1.39x faster                                                           |
| raytrace                   | 308 ms                                                          | 222 ms: 1.39x faster                                                            |
| deltablue                  | 3.58 ms                                                         | 2.70 ms: 1.33x faster                                                           |
| async_tree_memoization_tg  | 350 ms                                                          | 265 ms: 1.32x faster                                                            |
| async_tree_none_tg         | 278 ms                                                          | 215 ms: 1.29x faster                                                            |
| async_tree_io              | 693 ms                                                          | 539 ms: 1.29x faster                                                            |
| pickle_pure_python         | 286 us                                                          | 223 us: 1.28x faster                                                            |
| chameleon                  | 7.75 ms                                                         | 6.05 ms: 1.28x faster                                                           |
| async_tree_memoization     | 364 ms                                                          | 286 ms: 1.27x faster                                                            |
| typing_runtime_protocols   | 126 us                                                          | 99.8 us: 1.27x faster                                                           |
| scimark_sor                | 130 ms                                                          | 103 ms: 1.26x faster                                                            |
| sqlglot_parse              | 1.25 ms                                                         | 990 us: 1.26x faster                                                            |
| nbody                      | 127 ms                                                          | 101 ms: 1.26x faster                                                            |
| tomli_loads                | 2.20 sec                                                        | 1.75 sec: 1.25x faster                                                          |
| async_tree_none            | 298 ms                                                          | 238 ms: 1.25x faster                                                            |
| async_tree_io_tg           | 677 ms                                                          | 543 ms: 1.25x faster                                                            |
| deepcopy                   | 360 us                                                          | 290 us: 1.24x faster                                                            |
| xml_etree_process          | 53.2 ms                                                         | 43.0 ms: 1.24x faster                                                           |
| richards                   | 41.3 ms                                                         | 33.4 ms: 1.24x faster                                                           |
| unpickle_pure_python       | 210 us                                                          | 170 us: 1.23x faster                                                            |
| sqlglot_transpile          | 1.53 ms                                                         | 1.24 ms: 1.23x faster                                                           |
| comprehensions             | 19.2 us                                                         | 15.6 us: 1.23x faster                                                           |
| richards_super             | 46.5 ms                                                         | 38.2 ms: 1.22x faster                                                           |
| logging_simple             | 9.75 us                                                         | 8.02 us: 1.22x faster                                                           |
| deepcopy_reduce            | 3.23 us                                                         | 2.68 us: 1.20x faster                                                           |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 454 ms: 1.20x faster                                                            |
| logging_format             | 10.4 us                                                         | 8.65 us: 1.20x faster                                                           |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 3.22 ms: 1.20x faster                                                           |
| xml_etree_generate         | 72.1 ms                                                         | 60.7 ms: 1.19x faster                                                           |
| xml_etree_iterparse        | 77.6 ms                                                         | 65.4 ms: 1.19x faster                                                           |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 483 ms: 1.17x faster                                                            |
| pycparser                  | 978 ms                                                          | 839 ms: 1.17x faster                                                            |
| pyflate                    | 424 ms                                                          | 364 ms: 1.16x faster                                                            |
| regex_compile              | 129 ms                                                          | 112 ms: 1.16x faster                                                            |
| go                         | 137 ms                                                          | 119 ms: 1.15x faster                                                            |
| chaos                      | 69.4 ms                                                         | 60.2 ms: 1.15x faster                                                           |
| hexiom                     | 6.82 ms                                                         | 6.09 ms: 1.12x faster                                                           |
| scimark_fft                | 271 ms                                                          | 244 ms: 1.11x faster                                                            |
| tornado_http               | 105 ms                                                          | 95.3 ms: 1.10x faster                                                           |
| sympy_sum                  | 123 ms                                                          | 112 ms: 1.10x faster                                                            |
| async_generators           | 313 ms                                                          | 287 ms: 1.09x faster                                                            |
| scimark_monte_carlo        | 66.4 ms                                                         | 60.9 ms: 1.09x faster                                                           |
| crypto_pyaes               | 69.2 ms                                                         | 63.6 ms: 1.09x faster                                                           |
| bench_thread_pool          | 1.10 ms                                                         | 1.01 ms: 1.09x faster                                                           |
| json_dumps                 | 7.40 ms                                                         | 6.82 ms: 1.09x faster                                                           |
| 2to3                       | 280 ms                                                          | 258 ms: 1.08x faster                                                            |
| mdp                        | 1.91 sec                                                        | 1.77 sec: 1.08x faster                                                          |
| fannkuch                   | 354 ms                                                          | 327 ms: 1.08x faster                                                            |
| sympy_str                  | 240 ms                                                          | 222 ms: 1.08x faster                                                            |
| regex_dna                  | 127 ms                                                          | 118 ms: 1.07x faster                                                            |
| regex_effbot               | 2.04 ms                                                         | 1.90 ms: 1.07x faster                                                           |
| sympy_integrate            | 17.5 ms                                                         | 16.4 ms: 1.07x faster                                                           |
| sqlite_synth               | 2.07 us                                                         | 1.94 us: 1.07x faster                                                           |
| pathlib                    | 91.4 ms                                                         | 85.9 ms: 1.06x faster                                                           |
| pickle_list                | 3.37 us                                                         | 3.17 us: 1.06x faster                                                           |
| asyncio_tcp                | 662 ms                                                          | 626 ms: 1.06x faster                                                            |
| meteor_contest             | 86.9 ms                                                         | 82.5 ms: 1.05x faster                                                           |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 16.8 sec: 1.05x faster                                                          |
| scimark_lu                 | 93.2 ms                                                         | 88.9 ms: 1.05x faster                                                           |
| xml_etree_parse            | 113 ms                                                          | 108 ms: 1.05x faster                                                            |
| docutils                   | 1.98 sec                                                        | 1.91 sec: 1.04x faster                                                          |
| bench_mp_pool              | 75.4 ms                                                         | 72.5 ms: 1.04x faster                                                           |
| sympy_expand               | 398 ms                                                          | 383 ms: 1.04x faster                                                            |
| sqlglot_optimize           | 48.5 ms                                                         | 46.8 ms: 1.04x faster                                                           |
| json                       | 4.15 ms                                                         | 4.01 ms: 1.04x faster                                                           |
| json_loads                 | 20.4 us                                                         | 19.8 us: 1.03x faster                                                           |
| nqueens                    | 93.7 ms                                                         | 92.2 ms: 1.02x faster                                                           |
| unpickle_list              | 2.95 us                                                         | 2.91 us: 1.01x faster                                                           |
| pidigits                   | 199 ms                                                          | 199 ms: 1.00x faster                                                            |
| pickle                     | 7.79 us                                                         | 7.87 us: 1.01x slower                                                           |
| gc_traversal               | 1.44 ms                                                         | 1.46 ms: 1.01x slower                                                           |
| unpickle                   | 9.71 us                                                         | 9.86 us: 1.02x slower                                                           |
| pprint_safe_repr           | 721 ms                                                          | 732 ms: 1.02x slower                                                            |
| regex_v8                   | 15.0 ms                                                         | 16.3 ms: 1.08x slower                                                           |
| python_startup             | 22.4 ms                                                         | 24.6 ms: 1.10x slower                                                           |
| create_gc_cycles           | 652 us                                                          | 740 us: 1.14x slower                                                            |
| telco                      | 5.51 ms                                                         | 6.40 ms: 1.16x slower                                                           |
| python_startup_no_site     | 19.1 ms                                                         | 22.4 ms: 1.18x slower                                                           |
| sqlglot_normalize          | 100 ms                                                          | 235 ms: 2.35x slower                                                            |
| coverage                   | 48.4 ms                                                         | 514 ms: 10.60x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.10x faster                                                                    |

Benchmark hidden because not significant (2): pickle_dict, pprint_pformat
Ignored benchmarks (8) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, django_template, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240404-3.13.0a5+-434bc59-JIT/bm-20240404-pythonperf1_win32-x86-python-434bc593df4c0274b8af-3.13.0a5+-434bc59.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: unknown