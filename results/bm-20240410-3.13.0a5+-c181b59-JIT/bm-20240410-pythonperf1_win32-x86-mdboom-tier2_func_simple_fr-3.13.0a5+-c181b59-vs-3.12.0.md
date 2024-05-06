# Results vs. 3.12.0

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: windows-x86
- commit hash: c181b59
- commit date: 2024-04-10
- overall geometric mean: 1.10x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 255 ms: 1.10x faster                                                            |
| chameleon      | 7.75 ms                                                         | 6.27 ms: 1.23x faster                                                           |
| docutils       | 1.98 sec                                                        | 1.93 sec: 1.03x faster                                                          |
| tornado_http   | 105 ms                                                          | 95.5 ms: 1.10x faster                                                           |
| Geometric mean | (ref)                                                           | 1.11x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 350 ms                                                          | 267 ms: 1.31x faster                                                            |
| async_tree_none_tg         | 278 ms                                                          | 217 ms: 1.28x faster                                                            |
| async_tree_memoization     | 364 ms                                                          | 287 ms: 1.27x faster                                                            |
| async_tree_io              | 693 ms                                                          | 553 ms: 1.25x faster                                                            |
| async_tree_none            | 298 ms                                                          | 238 ms: 1.25x faster                                                            |
| async_tree_io_tg           | 677 ms                                                          | 547 ms: 1.24x faster                                                            |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 461 ms: 1.19x faster                                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 491 ms: 1.15x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.24x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 76.7 ms                                                         | 53.2 ms: 1.44x faster                                                           |
| nbody          | 127 ms                                                          | 96.9 ms: 1.31x faster                                                           |
| pidigits       | 199 ms                                                          | 197 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                           | 1.24x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 110 ms: 1.17x faster                                                            |
| regex_effbot   | 2.04 ms                                                         | 1.91 ms: 1.06x faster                                                           |
| regex_dna      | 127 ms                                                          | 122 ms: 1.04x faster                                                            |
| regex_v8       | 15.0 ms                                                         | 16.1 ms: 1.07x slower                                                           |
| Geometric mean | (ref)                                                           | 1.05x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_pure_python   | 286 us                                                          | 216 us: 1.32x faster                                                            |
| tomli_loads          | 2.20 sec                                                        | 1.71 sec: 1.29x faster                                                          |
| xml_etree_process    | 53.2 ms                                                         | 43.0 ms: 1.24x faster                                                           |
| unpickle_pure_python | 210 us                                                          | 174 us: 1.21x faster                                                            |
| xml_etree_generate   | 72.1 ms                                                         | 60.7 ms: 1.19x faster                                                           |
| xml_etree_iterparse  | 77.6 ms                                                         | 65.7 ms: 1.18x faster                                                           |
| json_dumps           | 7.40 ms                                                         | 6.84 ms: 1.08x faster                                                           |
| pickle_list          | 3.37 us                                                         | 3.17 us: 1.06x faster                                                           |
| xml_etree_parse      | 113 ms                                                          | 108 ms: 1.05x faster                                                            |
| unpickle_list        | 2.95 us                                                         | 2.82 us: 1.05x faster                                                           |
| json_loads           | 20.4 us                                                         | 20.1 us: 1.01x faster                                                           |
| pickle_dict          | 19.9 us                                                         | 19.8 us: 1.00x faster                                                           |
| pickle               | 7.79 us                                                         | 7.94 us: 1.02x slower                                                           |
| unpickle             | 9.71 us                                                         | 10.2 us: 1.05x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.11x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                         | 23.9 ms: 1.07x slower                                                           |
| python_startup_no_site | 19.1 ms                                                         | 21.8 ms: 1.14x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.11x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|-----------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako      | 9.96 ms                                                         | 7.13 ms: 1.40x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| generators                 | 38.5 ms                                                         | 22.3 ms: 1.73x faster                                                           |
| logging_silent             | 101 ns                                                          | 59.4 ns: 1.70x faster                                                           |
| deepcopy_memo              | 38.4 us                                                         | 25.3 us: 1.51x faster                                                           |
| spectral_norm              | 104 ms                                                          | 71.0 ms: 1.46x faster                                                           |
| float                      | 76.7 ms                                                         | 53.2 ms: 1.44x faster                                                           |
| raytrace                   | 308 ms                                                          | 220 ms: 1.40x faster                                                            |
| mako                       | 9.96 ms                                                         | 7.13 ms: 1.40x faster                                                           |
| coroutines                 | 20.9 ms                                                         | 15.1 ms: 1.39x faster                                                           |
| scimark_sor                | 130 ms                                                          | 97.4 ms: 1.33x faster                                                           |
| pickle_pure_python         | 286 us                                                          | 216 us: 1.32x faster                                                            |
| deltablue                  | 3.58 ms                                                         | 2.72 ms: 1.32x faster                                                           |
| typing_runtime_protocols   | 126 us                                                          | 96.1 us: 1.31x faster                                                           |
| async_tree_memoization_tg  | 350 ms                                                          | 267 ms: 1.31x faster                                                            |
| nbody                      | 127 ms                                                          | 96.9 ms: 1.31x faster                                                           |
| tomli_loads                | 2.20 sec                                                        | 1.71 sec: 1.29x faster                                                          |
| async_tree_none_tg         | 278 ms                                                          | 217 ms: 1.28x faster                                                            |
| async_tree_memoization     | 364 ms                                                          | 287 ms: 1.27x faster                                                            |
| sqlglot_parse              | 1.25 ms                                                         | 988 us: 1.26x faster                                                            |
| async_tree_io              | 693 ms                                                          | 553 ms: 1.25x faster                                                            |
| async_tree_none            | 298 ms                                                          | 238 ms: 1.25x faster                                                            |
| async_tree_io_tg           | 677 ms                                                          | 547 ms: 1.24x faster                                                            |
| xml_etree_process          | 53.2 ms                                                         | 43.0 ms: 1.24x faster                                                           |
| chameleon                  | 7.75 ms                                                         | 6.27 ms: 1.23x faster                                                           |
| sqlglot_transpile          | 1.53 ms                                                         | 1.24 ms: 1.23x faster                                                           |
| logging_simple             | 9.75 us                                                         | 7.93 us: 1.23x faster                                                           |
| comprehensions             | 19.2 us                                                         | 15.6 us: 1.23x faster                                                           |
| deepcopy                   | 360 us                                                          | 294 us: 1.23x faster                                                            |
| logging_format             | 10.4 us                                                         | 8.53 us: 1.22x faster                                                           |
| unpickle_pure_python       | 210 us                                                          | 174 us: 1.21x faster                                                            |
| deepcopy_reduce            | 3.23 us                                                         | 2.69 us: 1.20x faster                                                           |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 3.23 ms: 1.19x faster                                                           |
| richards                   | 41.3 ms                                                         | 34.8 ms: 1.19x faster                                                           |
| xml_etree_generate         | 72.1 ms                                                         | 60.7 ms: 1.19x faster                                                           |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 461 ms: 1.19x faster                                                            |
| xml_etree_iterparse        | 77.6 ms                                                         | 65.7 ms: 1.18x faster                                                           |
| richards_super             | 46.5 ms                                                         | 39.5 ms: 1.18x faster                                                           |
| pyflate                    | 424 ms                                                          | 361 ms: 1.17x faster                                                            |
| regex_compile              | 129 ms                                                          | 110 ms: 1.17x faster                                                            |
| pycparser                  | 978 ms                                                          | 841 ms: 1.16x faster                                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 491 ms: 1.15x faster                                                            |
| bench_thread_pool          | 1.10 ms                                                         | 981 us: 1.12x faster                                                            |
| chaos                      | 69.4 ms                                                         | 61.9 ms: 1.12x faster                                                           |
| scimark_monte_carlo        | 66.4 ms                                                         | 59.4 ms: 1.12x faster                                                           |
| go                         | 137 ms                                                          | 123 ms: 1.12x faster                                                            |
| sympy_sum                  | 123 ms                                                          | 110 ms: 1.12x faster                                                            |
| hexiom                     | 6.82 ms                                                         | 6.12 ms: 1.11x faster                                                           |
| scimark_fft                | 271 ms                                                          | 245 ms: 1.11x faster                                                            |
| mdp                        | 1.91 sec                                                        | 1.73 sec: 1.11x faster                                                          |
| sympy_str                  | 240 ms                                                          | 217 ms: 1.10x faster                                                            |
| tornado_http               | 105 ms                                                          | 95.5 ms: 1.10x faster                                                           |
| 2to3                       | 280 ms                                                          | 255 ms: 1.10x faster                                                            |
| async_generators           | 313 ms                                                          | 286 ms: 1.10x faster                                                            |
| asyncio_tcp                | 662 ms                                                          | 607 ms: 1.09x faster                                                            |
| crypto_pyaes               | 69.2 ms                                                         | 63.5 ms: 1.09x faster                                                           |
| json_dumps                 | 7.40 ms                                                         | 6.84 ms: 1.08x faster                                                           |
| pathlib                    | 91.4 ms                                                         | 84.6 ms: 1.08x faster                                                           |
| fannkuch                   | 354 ms                                                          | 329 ms: 1.07x faster                                                            |
| sympy_integrate            | 17.5 ms                                                         | 16.4 ms: 1.07x faster                                                           |
| sympy_expand               | 398 ms                                                          | 373 ms: 1.07x faster                                                            |
| sqlglot_optimize           | 48.5 ms                                                         | 45.4 ms: 1.07x faster                                                           |
| sqlite_synth               | 2.07 us                                                         | 1.95 us: 1.07x faster                                                           |
| scimark_lu                 | 93.2 ms                                                         | 87.5 ms: 1.06x faster                                                           |
| regex_effbot               | 2.04 ms                                                         | 1.91 ms: 1.06x faster                                                           |
| pickle_list                | 3.37 us                                                         | 3.17 us: 1.06x faster                                                           |
| meteor_contest             | 86.9 ms                                                         | 82.0 ms: 1.06x faster                                                           |
| bench_mp_pool              | 75.4 ms                                                         | 71.8 ms: 1.05x faster                                                           |
| xml_etree_parse            | 113 ms                                                          | 108 ms: 1.05x faster                                                            |
| unpickle_list              | 2.95 us                                                         | 2.82 us: 1.05x faster                                                           |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 16.9 sec: 1.05x faster                                                          |
| regex_dna                  | 127 ms                                                          | 122 ms: 1.04x faster                                                            |
| docutils                   | 1.98 sec                                                        | 1.93 sec: 1.03x faster                                                          |
| json_loads                 | 20.4 us                                                         | 20.1 us: 1.01x faster                                                           |
| pidigits                   | 199 ms                                                          | 197 ms: 1.01x faster                                                            |
| json                       | 4.15 ms                                                         | 4.12 ms: 1.01x faster                                                           |
| nqueens                    | 93.7 ms                                                         | 92.9 ms: 1.01x faster                                                           |
| pickle_dict                | 19.9 us                                                         | 19.8 us: 1.00x faster                                                           |
| pickle                     | 7.79 us                                                         | 7.94 us: 1.02x slower                                                           |
| pprint_pformat             | 1.50 sec                                                        | 1.53 sec: 1.02x slower                                                          |
| pprint_safe_repr           | 721 ms                                                          | 749 ms: 1.04x slower                                                            |
| unpickle                   | 9.71 us                                                         | 10.2 us: 1.05x slower                                                           |
| python_startup             | 22.4 ms                                                         | 23.9 ms: 1.07x slower                                                           |
| regex_v8                   | 15.0 ms                                                         | 16.1 ms: 1.07x slower                                                           |
| python_startup_no_site     | 19.1 ms                                                         | 21.8 ms: 1.14x slower                                                           |
| create_gc_cycles           | 652 us                                                          | 749 us: 1.15x slower                                                            |
| telco                      | 5.51 ms                                                         | 6.84 ms: 1.24x slower                                                           |
| sqlglot_normalize          | 100 ms                                                          | 232 ms: 2.31x slower                                                            |
| coverage                   | 48.4 ms                                                         | 499 ms: 10.29x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.10x faster                                                                    |

Benchmark hidden because not significant (1): gc_traversal
Ignored benchmarks (8) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, django_template, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240410-3.13.0a5+-c181b59-JIT/bm-20240410-pythonperf1_win32-x86-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: unknown