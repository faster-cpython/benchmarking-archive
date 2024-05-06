# Results vs. 3.12.0

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: windows-x86
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.10x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 255 ms: 1.10x faster                                                            |
| chameleon      | 7.75 ms                                                         | 6.13 ms: 1.26x faster                                                           |
| docutils       | 1.98 sec                                                        | 1.95 sec: 1.02x faster                                                          |
| tornado_http   | 105 ms                                                          | 96.4 ms: 1.09x faster                                                           |
| Geometric mean | (ref)                                                           | 1.11x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none_tg         | 278 ms                                                          | 209 ms: 1.33x faster                                                            |
| async_tree_memoization_tg  | 350 ms                                                          | 265 ms: 1.32x faster                                                            |
| async_tree_memoization     | 364 ms                                                          | 282 ms: 1.29x faster                                                            |
| async_tree_none            | 298 ms                                                          | 231 ms: 1.29x faster                                                            |
| async_tree_io              | 693 ms                                                          | 544 ms: 1.27x faster                                                            |
| async_tree_io_tg           | 677 ms                                                          | 547 ms: 1.24x faster                                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 481 ms: 1.17x faster                                                            |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 468 ms: 1.17x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.26x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 76.7 ms                                                         | 53.3 ms: 1.44x faster                                                           |
| nbody          | 127 ms                                                          | 98.8 ms: 1.29x faster                                                           |
| pidigits       | 199 ms                                                          | 198 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                           | 1.23x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 113 ms: 1.14x faster                                                            |
| regex_effbot   | 2.04 ms                                                         | 1.93 ms: 1.06x faster                                                           |
| regex_dna      | 127 ms                                                          | 125 ms: 1.02x faster                                                            |
| regex_v8       | 15.0 ms                                                         | 16.2 ms: 1.08x slower                                                           |
| Geometric mean | (ref)                                                           | 1.03x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| tomli_loads          | 2.20 sec                                                        | 1.72 sec: 1.28x faster                                                          |
| pickle_pure_python   | 286 us                                                          | 227 us: 1.26x faster                                                            |
| unpickle_pure_python | 210 us                                                          | 171 us: 1.23x faster                                                            |
| xml_etree_process    | 53.2 ms                                                         | 43.4 ms: 1.23x faster                                                           |
| xml_etree_iterparse  | 77.6 ms                                                         | 65.4 ms: 1.19x faster                                                           |
| xml_etree_generate   | 72.1 ms                                                         | 61.7 ms: 1.17x faster                                                           |
| json_dumps           | 7.40 ms                                                         | 6.78 ms: 1.09x faster                                                           |
| unpickle_list        | 2.95 us                                                         | 2.80 us: 1.05x faster                                                           |
| xml_etree_parse      | 113 ms                                                          | 108 ms: 1.05x faster                                                            |
| pickle_list          | 3.37 us                                                         | 3.25 us: 1.04x faster                                                           |
| pickle_dict          | 19.9 us                                                         | 19.9 us: 1.00x faster                                                           |
| unpickle             | 9.71 us                                                         | 9.88 us: 1.02x slower                                                           |
| pickle               | 7.79 us                                                         | 8.18 us: 1.05x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.10x faster                                                                    |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                         | 24.4 ms: 1.09x slower                                                           |
| python_startup_no_site | 19.1 ms                                                         | 21.9 ms: 1.15x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.12x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 9.96 ms                                                         | 7.24 ms: 1.38x faster                                                           |
| django_template | 36.9 ms                                                         | 33.2 ms: 1.11x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.24x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| generators                 | 38.5 ms                                                         | 23.0 ms: 1.68x faster                                                           |
| logging_silent             | 101 ns                                                          | 60.7 ns: 1.66x faster                                                           |
| spectral_norm              | 104 ms                                                          | 71.3 ms: 1.46x faster                                                           |
| deepcopy_memo              | 38.4 us                                                         | 26.5 us: 1.45x faster                                                           |
| float                      | 76.7 ms                                                         | 53.3 ms: 1.44x faster                                                           |
| unpack_sequence            | 62.5 ns                                                         | 44.0 ns: 1.42x faster                                                           |
| coroutines                 | 20.9 ms                                                         | 14.8 ms: 1.41x faster                                                           |
| deltablue                  | 3.58 ms                                                         | 2.59 ms: 1.38x faster                                                           |
| mako                       | 9.96 ms                                                         | 7.24 ms: 1.38x faster                                                           |
| async_tree_none_tg         | 278 ms                                                          | 209 ms: 1.33x faster                                                            |
| async_tree_memoization_tg  | 350 ms                                                          | 265 ms: 1.32x faster                                                            |
| scimark_sor                | 130 ms                                                          | 99.1 ms: 1.31x faster                                                           |
| async_tree_memoization     | 364 ms                                                          | 282 ms: 1.29x faster                                                            |
| async_tree_none            | 298 ms                                                          | 231 ms: 1.29x faster                                                            |
| typing_runtime_protocols   | 126 us                                                          | 98.2 us: 1.29x faster                                                           |
| nbody                      | 127 ms                                                          | 98.8 ms: 1.29x faster                                                           |
| tomli_loads                | 2.20 sec                                                        | 1.72 sec: 1.28x faster                                                          |
| async_tree_io              | 693 ms                                                          | 544 ms: 1.27x faster                                                            |
| chameleon                  | 7.75 ms                                                         | 6.13 ms: 1.26x faster                                                           |
| pickle_pure_python         | 286 us                                                          | 227 us: 1.26x faster                                                            |
| sqlglot_parse              | 1.25 ms                                                         | 996 us: 1.25x faster                                                            |
| comprehensions             | 19.2 us                                                         | 15.3 us: 1.25x faster                                                           |
| async_tree_io_tg           | 677 ms                                                          | 547 ms: 1.24x faster                                                            |
| unpickle_pure_python       | 210 us                                                          | 171 us: 1.23x faster                                                            |
| deepcopy_reduce            | 3.23 us                                                         | 2.63 us: 1.23x faster                                                           |
| xml_etree_process          | 53.2 ms                                                         | 43.4 ms: 1.23x faster                                                           |
| deepcopy                   | 360 us                                                          | 295 us: 1.22x faster                                                            |
| sqlglot_transpile          | 1.53 ms                                                         | 1.26 ms: 1.21x faster                                                           |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 3.18 ms: 1.21x faster                                                           |
| xml_etree_iterparse        | 77.6 ms                                                         | 65.4 ms: 1.19x faster                                                           |
| raytrace                   | 308 ms                                                          | 260 ms: 1.19x faster                                                            |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 481 ms: 1.17x faster                                                            |
| xml_etree_generate         | 72.1 ms                                                         | 61.7 ms: 1.17x faster                                                           |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 468 ms: 1.17x faster                                                            |
| logging_format             | 10.4 us                                                         | 9.05 us: 1.15x faster                                                           |
| logging_simple             | 9.75 us                                                         | 8.50 us: 1.15x faster                                                           |
| pyflate                    | 424 ms                                                          | 369 ms: 1.15x faster                                                            |
| richards                   | 41.3 ms                                                         | 36.1 ms: 1.14x faster                                                           |
| richards_super             | 46.5 ms                                                         | 40.6 ms: 1.14x faster                                                           |
| regex_compile              | 129 ms                                                          | 113 ms: 1.14x faster                                                            |
| fannkuch                   | 354 ms                                                          | 313 ms: 1.13x faster                                                            |
| go                         | 137 ms                                                          | 122 ms: 1.12x faster                                                            |
| chaos                      | 69.4 ms                                                         | 61.8 ms: 1.12x faster                                                           |
| pycparser                  | 978 ms                                                          | 871 ms: 1.12x faster                                                            |
| sympy_sum                  | 123 ms                                                          | 109 ms: 1.12x faster                                                            |
| crypto_pyaes               | 69.2 ms                                                         | 62.0 ms: 1.12x faster                                                           |
| django_template            | 36.9 ms                                                         | 33.2 ms: 1.11x faster                                                           |
| sympy_str                  | 240 ms                                                          | 217 ms: 1.10x faster                                                            |
| 2to3                       | 280 ms                                                          | 255 ms: 1.10x faster                                                            |
| scimark_fft                | 271 ms                                                          | 247 ms: 1.09x faster                                                            |
| hexiom                     | 6.82 ms                                                         | 6.24 ms: 1.09x faster                                                           |
| json_dumps                 | 7.40 ms                                                         | 6.78 ms: 1.09x faster                                                           |
| tornado_http               | 105 ms                                                          | 96.4 ms: 1.09x faster                                                           |
| bench_thread_pool          | 1.10 ms                                                         | 1.01 ms: 1.09x faster                                                           |
| sympy_integrate            | 17.5 ms                                                         | 16.3 ms: 1.08x faster                                                           |
| mdp                        | 1.91 sec                                                        | 1.78 sec: 1.08x faster                                                          |
| meteor_contest             | 86.9 ms                                                         | 81.2 ms: 1.07x faster                                                           |
| scimark_monte_carlo        | 66.4 ms                                                         | 62.4 ms: 1.06x faster                                                           |
| sqlite_synth               | 2.07 us                                                         | 1.95 us: 1.06x faster                                                           |
| pathlib                    | 91.4 ms                                                         | 86.0 ms: 1.06x faster                                                           |
| async_generators           | 313 ms                                                          | 295 ms: 1.06x faster                                                            |
| regex_effbot               | 2.04 ms                                                         | 1.93 ms: 1.06x faster                                                           |
| sympy_expand               | 398 ms                                                          | 378 ms: 1.05x faster                                                            |
| unpickle_list              | 2.95 us                                                         | 2.80 us: 1.05x faster                                                           |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 16.8 sec: 1.05x faster                                                          |
| sqlglot_optimize           | 48.5 ms                                                         | 46.3 ms: 1.05x faster                                                           |
| asyncio_tcp                | 662 ms                                                          | 632 ms: 1.05x faster                                                            |
| xml_etree_parse            | 113 ms                                                          | 108 ms: 1.05x faster                                                            |
| bench_mp_pool              | 75.4 ms                                                         | 72.3 ms: 1.04x faster                                                           |
| pickle_list                | 3.37 us                                                         | 3.25 us: 1.04x faster                                                           |
| docutils                   | 1.98 sec                                                        | 1.95 sec: 1.02x faster                                                          |
| regex_dna                  | 127 ms                                                          | 125 ms: 1.02x faster                                                            |
| gc_traversal               | 1.44 ms                                                         | 1.42 ms: 1.01x faster                                                           |
| pidigits                   | 199 ms                                                          | 198 ms: 1.01x faster                                                            |
| nqueens                    | 93.7 ms                                                         | 93.0 ms: 1.01x faster                                                           |
| pprint_pformat             | 1.50 sec                                                        | 1.49 sec: 1.00x faster                                                          |
| pickle_dict                | 19.9 us                                                         | 19.9 us: 1.00x faster                                                           |
| unpickle                   | 9.71 us                                                         | 9.88 us: 1.02x slower                                                           |
| pprint_safe_repr           | 721 ms                                                          | 741 ms: 1.03x slower                                                            |
| scimark_lu                 | 93.2 ms                                                         | 96.7 ms: 1.04x slower                                                           |
| pickle                     | 7.79 us                                                         | 8.18 us: 1.05x slower                                                           |
| regex_v8                   | 15.0 ms                                                         | 16.2 ms: 1.08x slower                                                           |
| json                       | 4.15 ms                                                         | 4.50 ms: 1.08x slower                                                           |
| python_startup             | 22.4 ms                                                         | 24.4 ms: 1.09x slower                                                           |
| create_gc_cycles           | 652 us                                                          | 740 us: 1.13x slower                                                            |
| telco                      | 5.51 ms                                                         | 6.33 ms: 1.15x slower                                                           |
| python_startup_no_site     | 19.1 ms                                                         | 21.9 ms: 1.15x slower                                                           |
| sqlglot_normalize          | 100 ms                                                          | 238 ms: 2.38x slower                                                            |
| coverage                   | 48.4 ms                                                         | 482 ms: 9.95x slower                                                            |
| Geometric mean             | (ref)                                                           | 1.10x faster                                                                    |

Benchmark hidden because not significant (1): json_loads
Ignored benchmarks (6) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240329-3.13.0a5+-bfc57d4-JIT/bm-20240329-pythonperf1_win32-x86-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.07x

# Memory
- memory change: unknown