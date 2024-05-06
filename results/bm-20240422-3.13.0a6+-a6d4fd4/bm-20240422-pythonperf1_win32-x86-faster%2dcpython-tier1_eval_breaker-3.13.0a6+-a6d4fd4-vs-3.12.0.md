# Results vs. 3.12.0

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: windows-x86
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.20x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 232 ms: 1.20x faster                                                                    |
| chameleon      | 7.75 ms                                                         | 5.61 ms: 1.38x faster                                                                   |
| docutils       | 1.98 sec                                                        | 1.80 sec: 1.11x faster                                                                  |
| tornado_http   | 105 ms                                                          | 94.0 ms: 1.12x faster                                                                   |
| Geometric mean | (ref)                                                           | 1.20x faster                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 350 ms                                                          | 253 ms: 1.39x faster                                                                    |
| async_tree_none_tg         | 278 ms                                                          | 205 ms: 1.35x faster                                                                    |
| async_tree_memoization     | 364 ms                                                          | 270 ms: 1.34x faster                                                                    |
| async_tree_none            | 298 ms                                                          | 226 ms: 1.32x faster                                                                    |
| async_tree_io              | 693 ms                                                          | 529 ms: 1.31x faster                                                                    |
| async_tree_io_tg           | 677 ms                                                          | 527 ms: 1.28x faster                                                                    |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 453 ms: 1.20x faster                                                                    |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 468 ms: 1.20x faster                                                                    |
| Geometric mean             | (ref)                                                           | 1.30x faster                                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| nbody          | 127 ms                                                          | 76.4 ms: 1.66x faster                                                                   |
| float          | 76.7 ms                                                         | 53.4 ms: 1.44x faster                                                                   |
| pidigits       | 199 ms                                                          | 197 ms: 1.01x faster                                                                    |
| Geometric mean | (ref)                                                           | 1.34x faster                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 97.4 ms: 1.33x faster                                                                   |
| regex_effbot   | 2.04 ms                                                         | 1.90 ms: 1.07x faster                                                                   |
| regex_dna      | 127 ms                                                          | 121 ms: 1.05x faster                                                                    |
| regex_v8       | 15.0 ms                                                         | 16.1 ms: 1.07x slower                                                                   |
| Geometric mean | (ref)                                                           | 1.09x faster                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| unpickle_pure_python | 210 us                                                          | 140 us: 1.49x faster                                                                    |
| pickle_pure_python   | 286 us                                                          | 209 us: 1.37x faster                                                                    |
| tomli_loads          | 2.20 sec                                                        | 1.63 sec: 1.35x faster                                                                  |
| xml_etree_process    | 53.2 ms                                                         | 42.3 ms: 1.26x faster                                                                   |
| xml_etree_generate   | 72.1 ms                                                         | 60.0 ms: 1.20x faster                                                                   |
| xml_etree_iterparse  | 77.6 ms                                                         | 65.0 ms: 1.19x faster                                                                   |
| json_dumps           | 7.40 ms                                                         | 6.92 ms: 1.07x faster                                                                   |
| xml_etree_parse      | 113 ms                                                          | 107 ms: 1.06x faster                                                                    |
| unpickle_list        | 2.95 us                                                         | 2.86 us: 1.03x faster                                                                   |
| pickle_list          | 3.37 us                                                         | 3.29 us: 1.02x faster                                                                   |
| unpickle             | 9.71 us                                                         | 9.81 us: 1.01x slower                                                                   |
| json_loads           | 20.4 us                                                         | 20.6 us: 1.01x slower                                                                   |
| pickle               | 7.79 us                                                         | 7.97 us: 1.02x slower                                                                   |
| pickle_dict          | 19.9 us                                                         | 20.4 us: 1.03x slower                                                                   |
| Geometric mean       | (ref)                                                           | 1.13x faster                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| python_startup_no_site | 19.1 ms                                                         | 18.3 ms: 1.04x faster                                                                   |
| python_startup         | 22.4 ms                                                         | 22.0 ms: 1.01x faster                                                                   |
| Geometric mean         | (ref)                                                           | 1.03x faster                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-----------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| mako            | 9.96 ms                                                         | 6.87 ms: 1.45x faster                                                                   |
| django_template | 36.9 ms                                                         | 29.5 ms: 1.25x faster                                                                   |
| Geometric mean  | (ref)                                                           | 1.35x faster                                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------|:---------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| logging_silent             | 101 ns                                                          | 59.8 ns: 1.69x faster                                                                   |
| deepcopy_memo              | 38.4 us                                                         | 22.9 us: 1.68x faster                                                                   |
| generators                 | 38.5 ms                                                         | 23.0 ms: 1.67x faster                                                                   |
| nbody                      | 127 ms                                                          | 76.4 ms: 1.66x faster                                                                   |
| comprehensions             | 19.2 us                                                         | 11.7 us: 1.64x faster                                                                   |
| raytrace                   | 308 ms                                                          | 189 ms: 1.63x faster                                                                    |
| deltablue                  | 3.58 ms                                                         | 2.20 ms: 1.63x faster                                                                   |
| scimark_sor                | 130 ms                                                          | 80.9 ms: 1.60x faster                                                                   |
| hexiom                     | 6.82 ms                                                         | 4.32 ms: 1.58x faster                                                                   |
| scimark_lu                 | 93.2 ms                                                         | 61.4 ms: 1.52x faster                                                                   |
| unpickle_pure_python       | 210 us                                                          | 140 us: 1.49x faster                                                                    |
| spectral_norm              | 104 ms                                                          | 71.0 ms: 1.46x faster                                                                   |
| mako                       | 9.96 ms                                                         | 6.87 ms: 1.45x faster                                                                   |
| float                      | 76.7 ms                                                         | 53.4 ms: 1.44x faster                                                                   |
| scimark_monte_carlo        | 66.4 ms                                                         | 46.7 ms: 1.42x faster                                                                   |
| sqlglot_parse              | 1.25 ms                                                         | 878 us: 1.42x faster                                                                    |
| coroutines                 | 20.9 ms                                                         | 14.7 ms: 1.42x faster                                                                   |
| chaos                      | 69.4 ms                                                         | 49.1 ms: 1.41x faster                                                                   |
| go                         | 137 ms                                                          | 98.3 ms: 1.40x faster                                                                   |
| typing_runtime_protocols   | 126 us                                                          | 90.7 us: 1.39x faster                                                                   |
| sqlglot_transpile          | 1.53 ms                                                         | 1.10 ms: 1.39x faster                                                                   |
| async_tree_memoization_tg  | 350 ms                                                          | 253 ms: 1.39x faster                                                                    |
| chameleon                  | 7.75 ms                                                         | 5.61 ms: 1.38x faster                                                                   |
| pickle_pure_python         | 286 us                                                          | 209 us: 1.37x faster                                                                    |
| richards                   | 41.3 ms                                                         | 30.3 ms: 1.37x faster                                                                   |
| deepcopy                   | 360 us                                                          | 264 us: 1.37x faster                                                                    |
| deepcopy_reduce            | 3.23 us                                                         | 2.36 us: 1.37x faster                                                                   |
| richards_super             | 46.5 ms                                                         | 34.2 ms: 1.36x faster                                                                   |
| tomli_loads                | 2.20 sec                                                        | 1.63 sec: 1.35x faster                                                                  |
| async_tree_none_tg         | 278 ms                                                          | 205 ms: 1.35x faster                                                                    |
| async_tree_memoization     | 364 ms                                                          | 270 ms: 1.34x faster                                                                    |
| pyflate                    | 424 ms                                                          | 316 ms: 1.34x faster                                                                    |
| regex_compile              | 129 ms                                                          | 97.4 ms: 1.33x faster                                                                   |
| nqueens                    | 93.7 ms                                                         | 70.6 ms: 1.33x faster                                                                   |
| async_tree_none            | 298 ms                                                          | 226 ms: 1.32x faster                                                                    |
| async_tree_io              | 693 ms                                                          | 529 ms: 1.31x faster                                                                    |
| pprint_pformat             | 1.50 sec                                                        | 1.15 sec: 1.31x faster                                                                  |
| logging_simple             | 9.75 us                                                         | 7.47 us: 1.30x faster                                                                   |
| logging_format             | 10.4 us                                                         | 8.01 us: 1.30x faster                                                                   |
| pprint_safe_repr           | 721 ms                                                          | 558 ms: 1.29x faster                                                                    |
| async_tree_io_tg           | 677 ms                                                          | 527 ms: 1.28x faster                                                                    |
| scimark_fft                | 271 ms                                                          | 212 ms: 1.28x faster                                                                    |
| fannkuch                   | 354 ms                                                          | 279 ms: 1.27x faster                                                                    |
| pycparser                  | 978 ms                                                          | 772 ms: 1.27x faster                                                                    |
| xml_etree_process          | 53.2 ms                                                         | 42.3 ms: 1.26x faster                                                                   |
| django_template            | 36.9 ms                                                         | 29.5 ms: 1.25x faster                                                                   |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 3.11 ms: 1.24x faster                                                                   |
| sqlglot_optimize           | 48.5 ms                                                         | 39.5 ms: 1.23x faster                                                                   |
| crypto_pyaes               | 69.2 ms                                                         | 56.5 ms: 1.22x faster                                                                   |
| sympy_integrate            | 17.5 ms                                                         | 14.5 ms: 1.21x faster                                                                   |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 453 ms: 1.20x faster                                                                    |
| 2to3                       | 280 ms                                                          | 232 ms: 1.20x faster                                                                    |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 468 ms: 1.20x faster                                                                    |
| xml_etree_generate         | 72.1 ms                                                         | 60.0 ms: 1.20x faster                                                                   |
| xml_etree_iterparse        | 77.6 ms                                                         | 65.0 ms: 1.19x faster                                                                   |
| sympy_sum                  | 123 ms                                                          | 104 ms: 1.18x faster                                                                    |
| sympy_str                  | 240 ms                                                          | 205 ms: 1.17x faster                                                                    |
| mdp                        | 1.91 sec                                                        | 1.64 sec: 1.17x faster                                                                  |
| meteor_contest             | 86.9 ms                                                         | 75.2 ms: 1.16x faster                                                                   |
| bench_thread_pool          | 1.10 ms                                                         | 977 us: 1.13x faster                                                                    |
| async_generators           | 313 ms                                                          | 280 ms: 1.12x faster                                                                    |
| tornado_http               | 105 ms                                                          | 94.0 ms: 1.12x faster                                                                   |
| bench_mp_pool              | 75.4 ms                                                         | 68.1 ms: 1.11x faster                                                                   |
| sympy_expand               | 398 ms                                                          | 359 ms: 1.11x faster                                                                    |
| docutils                   | 1.98 sec                                                        | 1.80 sec: 1.11x faster                                                                  |
| pathlib                    | 91.4 ms                                                         | 84.8 ms: 1.08x faster                                                                   |
| regex_effbot               | 2.04 ms                                                         | 1.90 ms: 1.07x faster                                                                   |
| json_dumps                 | 7.40 ms                                                         | 6.92 ms: 1.07x faster                                                                   |
| xml_etree_parse            | 113 ms                                                          | 107 ms: 1.06x faster                                                                    |
| sqlite_synth               | 2.07 us                                                         | 1.97 us: 1.05x faster                                                                   |
| regex_dna                  | 127 ms                                                          | 121 ms: 1.05x faster                                                                    |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 16.8 sec: 1.05x faster                                                                  |
| python_startup_no_site     | 19.1 ms                                                         | 18.3 ms: 1.04x faster                                                                   |
| unpickle_list              | 2.95 us                                                         | 2.86 us: 1.03x faster                                                                   |
| pickle_list                | 3.37 us                                                         | 3.29 us: 1.02x faster                                                                   |
| gc_traversal               | 1.44 ms                                                         | 1.42 ms: 1.02x faster                                                                   |
| python_startup             | 22.4 ms                                                         | 22.0 ms: 1.01x faster                                                                   |
| pidigits                   | 199 ms                                                          | 197 ms: 1.01x faster                                                                    |
| json                       | 4.15 ms                                                         | 4.12 ms: 1.01x faster                                                                   |
| unpickle                   | 9.71 us                                                         | 9.81 us: 1.01x slower                                                                   |
| json_loads                 | 20.4 us                                                         | 20.6 us: 1.01x slower                                                                   |
| pickle                     | 7.79 us                                                         | 7.97 us: 1.02x slower                                                                   |
| pickle_dict                | 19.9 us                                                         | 20.4 us: 1.03x slower                                                                   |
| telco                      | 5.51 ms                                                         | 5.90 ms: 1.07x slower                                                                   |
| regex_v8                   | 15.0 ms                                                         | 16.1 ms: 1.07x slower                                                                   |
| create_gc_cycles           | 652 us                                                          | 732 us: 1.12x slower                                                                    |
| sqlglot_normalize          | 100 ms                                                          | 203 ms: 2.02x slower                                                                    |
| coverage                   | 48.4 ms                                                         | 506 ms: 10.44x slower                                                                   |
| Geometric mean             | (ref)                                                           | 1.20x faster                                                                            |

Benchmark hidden because not significant (1): asyncio_tcp
Ignored benchmarks (7) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240422-3.13.0a6+-a6d4fd4/bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.21x
- 95% likely to have a speedup of 1.20x
- 99% likely to have a speedup of 1.18x

# Memory
- memory change: unknown