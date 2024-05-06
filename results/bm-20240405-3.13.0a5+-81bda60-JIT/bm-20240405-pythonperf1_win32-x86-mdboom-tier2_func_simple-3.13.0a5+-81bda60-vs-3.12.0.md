# Results vs. 3.12.0

- fork: mdboom
- ref: tier2_func_simple
- machine: windows-x86
- commit hash: 81bda60
- commit date: 2024-04-05
- overall geometric mean: 1.10x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 255 ms: 1.10x faster                                                         |
| chameleon      | 7.75 ms                                                         | 6.16 ms: 1.26x faster                                                        |
| docutils       | 1.98 sec                                                        | 1.94 sec: 1.02x faster                                                       |
| tornado_http   | 105 ms                                                          | 96.6 ms: 1.09x faster                                                        |
| Geometric mean | (ref)                                                           | 1.11x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 350 ms                                                          | 265 ms: 1.32x faster                                                         |
| async_tree_none_tg         | 278 ms                                                          | 216 ms: 1.29x faster                                                         |
| async_tree_io              | 693 ms                                                          | 542 ms: 1.28x faster                                                         |
| async_tree_memoization     | 364 ms                                                          | 286 ms: 1.27x faster                                                         |
| async_tree_io_tg           | 677 ms                                                          | 542 ms: 1.25x faster                                                         |
| async_tree_none            | 298 ms                                                          | 238 ms: 1.25x faster                                                         |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 461 ms: 1.18x faster                                                         |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 486 ms: 1.16x faster                                                         |
| Geometric mean             | (ref)                                                           | 1.25x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 76.7 ms                                                         | 54.0 ms: 1.42x faster                                                        |
| nbody          | 127 ms                                                          | 96.4 ms: 1.32x faster                                                        |
| pidigits       | 199 ms                                                          | 198 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                           | 1.24x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 112 ms: 1.15x faster                                                         |
| regex_effbot   | 2.04 ms                                                         | 1.90 ms: 1.07x faster                                                        |
| regex_dna      | 127 ms                                                          | 124 ms: 1.03x faster                                                         |
| regex_v8       | 15.0 ms                                                         | 16.2 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                           | 1.04x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 286 us                                                          | 221 us: 1.29x faster                                                         |
| tomli_loads          | 2.20 sec                                                        | 1.75 sec: 1.26x faster                                                       |
| xml_etree_process    | 53.2 ms                                                         | 43.2 ms: 1.23x faster                                                        |
| unpickle_pure_python | 210 us                                                          | 173 us: 1.21x faster                                                         |
| xml_etree_generate   | 72.1 ms                                                         | 60.4 ms: 1.19x faster                                                        |
| xml_etree_iterparse  | 77.6 ms                                                         | 65.4 ms: 1.19x faster                                                        |
| json_dumps           | 7.40 ms                                                         | 6.76 ms: 1.10x faster                                                        |
| unpickle_list        | 2.95 us                                                         | 2.75 us: 1.07x faster                                                        |
| pickle_list          | 3.37 us                                                         | 3.17 us: 1.06x faster                                                        |
| xml_etree_parse      | 113 ms                                                          | 107 ms: 1.06x faster                                                         |
| json_loads           | 20.4 us                                                         | 20.1 us: 1.01x faster                                                        |
| pickle_dict          | 19.9 us                                                         | 19.8 us: 1.01x faster                                                        |
| pickle               | 7.79 us                                                         | 7.95 us: 1.02x slower                                                        |
| unpickle             | 9.71 us                                                         | 9.95 us: 1.03x slower                                                        |
| Geometric mean       | (ref)                                                           | 1.11x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                         | 24.1 ms: 1.08x slower                                                        |
| python_startup_no_site | 19.1 ms                                                         | 21.7 ms: 1.14x slower                                                        |
| Geometric mean         | (ref)                                                           | 1.11x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|-----------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako      | 9.96 ms                                                         | 7.14 ms: 1.39x faster                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------------|:---------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| generators                 | 38.5 ms                                                         | 22.4 ms: 1.72x faster                                                        |
| logging_silent             | 101 ns                                                          | 60.0 ns: 1.68x faster                                                        |
| deepcopy_memo              | 38.4 us                                                         | 25.3 us: 1.52x faster                                                        |
| spectral_norm              | 104 ms                                                          | 72.3 ms: 1.44x faster                                                        |
| float                      | 76.7 ms                                                         | 54.0 ms: 1.42x faster                                                        |
| coroutines                 | 20.9 ms                                                         | 14.9 ms: 1.40x faster                                                        |
| mako                       | 9.96 ms                                                         | 7.14 ms: 1.39x faster                                                        |
| raytrace                   | 308 ms                                                          | 222 ms: 1.39x faster                                                         |
| scimark_sor                | 130 ms                                                          | 97.3 ms: 1.33x faster                                                        |
| async_tree_memoization_tg  | 350 ms                                                          | 265 ms: 1.32x faster                                                         |
| nbody                      | 127 ms                                                          | 96.4 ms: 1.32x faster                                                        |
| deltablue                  | 3.58 ms                                                         | 2.74 ms: 1.31x faster                                                        |
| pickle_pure_python         | 286 us                                                          | 221 us: 1.29x faster                                                         |
| async_tree_none_tg         | 278 ms                                                          | 216 ms: 1.29x faster                                                         |
| typing_runtime_protocols   | 126 us                                                          | 98.7 us: 1.28x faster                                                        |
| async_tree_io              | 693 ms                                                          | 542 ms: 1.28x faster                                                         |
| async_tree_memoization     | 364 ms                                                          | 286 ms: 1.27x faster                                                         |
| chameleon                  | 7.75 ms                                                         | 6.16 ms: 1.26x faster                                                        |
| tomli_loads                | 2.20 sec                                                        | 1.75 sec: 1.26x faster                                                       |
| async_tree_io_tg           | 677 ms                                                          | 542 ms: 1.25x faster                                                         |
| async_tree_none            | 298 ms                                                          | 238 ms: 1.25x faster                                                         |
| sqlglot_parse              | 1.25 ms                                                         | 1.00 ms: 1.24x faster                                                        |
| sqlglot_transpile          | 1.53 ms                                                         | 1.24 ms: 1.24x faster                                                        |
| xml_etree_process          | 53.2 ms                                                         | 43.2 ms: 1.23x faster                                                        |
| deepcopy_reduce            | 3.23 us                                                         | 2.62 us: 1.23x faster                                                        |
| comprehensions             | 19.2 us                                                         | 15.7 us: 1.22x faster                                                        |
| deepcopy                   | 360 us                                                          | 294 us: 1.22x faster                                                         |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 3.18 ms: 1.21x faster                                                        |
| unpickle_pure_python       | 210 us                                                          | 173 us: 1.21x faster                                                         |
| logging_simple             | 9.75 us                                                         | 8.06 us: 1.21x faster                                                        |
| xml_etree_generate         | 72.1 ms                                                         | 60.4 ms: 1.19x faster                                                        |
| logging_format             | 10.4 us                                                         | 8.73 us: 1.19x faster                                                        |
| xml_etree_iterparse        | 77.6 ms                                                         | 65.4 ms: 1.19x faster                                                        |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 461 ms: 1.18x faster                                                         |
| chaos                      | 69.4 ms                                                         | 58.8 ms: 1.18x faster                                                        |
| richards                   | 41.3 ms                                                         | 35.1 ms: 1.18x faster                                                        |
| pycparser                  | 978 ms                                                          | 841 ms: 1.16x faster                                                         |
| richards_super             | 46.5 ms                                                         | 40.0 ms: 1.16x faster                                                        |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 486 ms: 1.16x faster                                                         |
| pyflate                    | 424 ms                                                          | 368 ms: 1.15x faster                                                         |
| regex_compile              | 129 ms                                                          | 112 ms: 1.15x faster                                                         |
| scimark_fft                | 271 ms                                                          | 237 ms: 1.14x faster                                                         |
| go                         | 137 ms                                                          | 121 ms: 1.13x faster                                                         |
| sympy_sum                  | 123 ms                                                          | 109 ms: 1.13x faster                                                         |
| bench_thread_pool          | 1.10 ms                                                         | 985 us: 1.12x faster                                                         |
| hexiom                     | 6.82 ms                                                         | 6.14 ms: 1.11x faster                                                        |
| async_generators           | 313 ms                                                          | 283 ms: 1.11x faster                                                         |
| sympy_str                  | 240 ms                                                          | 217 ms: 1.10x faster                                                         |
| 2to3                       | 280 ms                                                          | 255 ms: 1.10x faster                                                         |
| json_dumps                 | 7.40 ms                                                         | 6.76 ms: 1.10x faster                                                        |
| sqlite_synth               | 2.07 us                                                         | 1.90 us: 1.09x faster                                                        |
| crypto_pyaes               | 69.2 ms                                                         | 63.4 ms: 1.09x faster                                                        |
| tornado_http               | 105 ms                                                          | 96.6 ms: 1.09x faster                                                        |
| scimark_monte_carlo        | 66.4 ms                                                         | 61.2 ms: 1.09x faster                                                        |
| mdp                        | 1.91 sec                                                        | 1.76 sec: 1.08x faster                                                       |
| scimark_lu                 | 93.2 ms                                                         | 86.1 ms: 1.08x faster                                                        |
| sympy_integrate            | 17.5 ms                                                         | 16.2 ms: 1.08x faster                                                        |
| fannkuch                   | 354 ms                                                          | 327 ms: 1.08x faster                                                         |
| sympy_expand               | 398 ms                                                          | 368 ms: 1.08x faster                                                         |
| unpickle_list              | 2.95 us                                                         | 2.75 us: 1.07x faster                                                        |
| regex_effbot               | 2.04 ms                                                         | 1.90 ms: 1.07x faster                                                        |
| pickle_list                | 3.37 us                                                         | 3.17 us: 1.06x faster                                                        |
| xml_etree_parse            | 113 ms                                                          | 107 ms: 1.06x faster                                                         |
| asyncio_tcp                | 662 ms                                                          | 628 ms: 1.05x faster                                                         |
| pathlib                    | 91.4 ms                                                         | 86.7 ms: 1.05x faster                                                        |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 16.9 sec: 1.05x faster                                                       |
| sqlglot_optimize           | 48.5 ms                                                         | 46.4 ms: 1.04x faster                                                        |
| meteor_contest             | 86.9 ms                                                         | 83.4 ms: 1.04x faster                                                        |
| bench_mp_pool              | 75.4 ms                                                         | 72.5 ms: 1.04x faster                                                        |
| json                       | 4.15 ms                                                         | 4.04 ms: 1.03x faster                                                        |
| regex_dna                  | 127 ms                                                          | 124 ms: 1.03x faster                                                         |
| docutils                   | 1.98 sec                                                        | 1.94 sec: 1.02x faster                                                       |
| json_loads                 | 20.4 us                                                         | 20.1 us: 1.01x faster                                                        |
| pidigits                   | 199 ms                                                          | 198 ms: 1.01x faster                                                         |
| nqueens                    | 93.7 ms                                                         | 93.0 ms: 1.01x faster                                                        |
| pickle_dict                | 19.9 us                                                         | 19.8 us: 1.01x faster                                                        |
| gc_traversal               | 1.44 ms                                                         | 1.45 ms: 1.01x slower                                                        |
| pickle                     | 7.79 us                                                         | 7.95 us: 1.02x slower                                                        |
| unpickle                   | 9.71 us                                                         | 9.95 us: 1.03x slower                                                        |
| pprint_pformat             | 1.50 sec                                                        | 1.54 sec: 1.03x slower                                                       |
| pprint_safe_repr           | 721 ms                                                          | 757 ms: 1.05x slower                                                         |
| python_startup             | 22.4 ms                                                         | 24.1 ms: 1.08x slower                                                        |
| regex_v8                   | 15.0 ms                                                         | 16.2 ms: 1.08x slower                                                        |
| create_gc_cycles           | 652 us                                                          | 738 us: 1.13x slower                                                         |
| python_startup_no_site     | 19.1 ms                                                         | 21.7 ms: 1.14x slower                                                        |
| telco                      | 5.51 ms                                                         | 6.42 ms: 1.16x slower                                                        |
| sqlglot_normalize          | 100 ms                                                          | 235 ms: 2.35x slower                                                         |
| coverage                   | 48.4 ms                                                         | 505 ms: 10.43x slower                                                        |
| Geometric mean             | (ref)                                                           | 1.10x faster                                                                 |
Ignored benchmarks (8) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, django_template, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240405-3.13.0a5+-81bda60-JIT/bm-20240405-pythonperf1_win32-x86-mdboom-tier2_func_simple-3.13.0a5+-81bda60.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: unknown