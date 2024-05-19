# Results vs. 3.11.0

- fork: python
- ref: caf6064a1bc15ac344af
- machine: windows-x86
- commit hash: caf6064
- commit date: 2024-05-18
- overall geometric mean: 1.21x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 257 ms: 1.10x faster                                                           |
| chameleon      | 8.08 ms                                                         | 6.62 ms: 1.22x faster                                                          |
| docutils       | 2.10 sec                                                        | 2.02 sec: 1.04x faster                                                         |
| html5lib       | 54.3 ms                                                         | 50.5 ms: 1.07x faster                                                          |
| tornado_http   | 118 ms                                                          | 99.4 ms: 1.19x faster                                                          |
| Geometric mean | (ref)                                                           | 1.12x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 236 ms: 1.45x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 284 ms: 1.44x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 210 ms: 1.43x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 263 ms: 1.43x faster                                                           |
| async_tree_io              | 754 ms                                                          | 545 ms: 1.38x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 544 ms: 1.37x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 468 ms: 1.23x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 498 ms: 1.19x faster                                                           |
| Geometric mean             | (ref)                                                           | 1.36x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 80.5 ms: 1.56x faster                                                          |
| float          | 76.1 ms                                                         | 56.6 ms: 1.34x faster                                                          |
| pidigits       | 203 ms                                                          | 198 ms: 1.02x faster                                                           |
| Geometric mean | (ref)                                                           | 1.29x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 127 ms: 1.17x faster                                                           |
| regex_dna      | 122 ms                                                          | 125 ms: 1.03x slower                                                           |
| regex_effbot   | 1.82 ms                                                         | 1.92 ms: 1.05x slower                                                          |
| regex_v8       | 15.2 ms                                                         | 16.2 ms: 1.07x slower                                                          |
| Geometric mean | (ref)                                                           | 1.00x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| json_dumps           | 9.80 ms                                                         | 7.00 ms: 1.40x faster                                                          |
| tomli_loads          | 2.31 sec                                                        | 1.67 sec: 1.38x faster                                                         |
| unpickle_pure_python | 231 us                                                          | 181 us: 1.28x faster                                                           |
| xml_etree_process    | 55.0 ms                                                         | 44.6 ms: 1.23x faster                                                          |
| pickle_pure_python   | 309 us                                                          | 254 us: 1.22x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 61.5 ms: 1.16x faster                                                          |
| xml_etree_iterparse  | 75.6 ms                                                         | 66.9 ms: 1.13x faster                                                          |
| xml_etree_parse      | 114 ms                                                          | 104 ms: 1.10x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 3.11 us: 1.05x faster                                                          |
| pickle               | 7.99 us                                                         | 8.10 us: 1.01x slower                                                          |
| pickle_dict          | 20.1 us                                                         | 20.6 us: 1.02x slower                                                          |
| json_loads           | 20.0 us                                                         | 20.7 us: 1.04x slower                                                          |
| pickle_list          | 3.27 us                                                         | 3.59 us: 1.10x slower                                                          |
| unpickle             | 9.23 us                                                         | 10.2 us: 1.11x slower                                                          |
| Geometric mean       | (ref)                                                           | 1.11x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup | 22.0 ms                                                         | 22.2 ms: 1.01x slower                                                          |
| Geometric mean | (ref)                                                           | 1.00x slower                                                                   |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|-----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 7.84 ms: 1.31x faster                                                          |
| genshi_xml      | 61.2 ms                                                         | 48.0 ms: 1.27x faster                                                          |
| genshi_text     | 26.8 ms                                                         | 22.1 ms: 1.21x faster                                                          |
| django_template | 37.4 ms                                                         | 33.6 ms: 1.11x faster                                                          |
| Geometric mean  | (ref)                                                           | 1.22x faster                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 149 us: 3.22x faster                                                           |
| generators                 | 52.2 ms                                                         | 23.7 ms: 2.20x faster                                                          |
| pylint                     | 418 ms                                                          | 245 ms: 1.70x faster                                                           |
| richards_super             | 58.7 ms                                                         | 37.3 ms: 1.57x faster                                                          |
| nbody                      | 126 ms                                                          | 80.5 ms: 1.56x faster                                                          |
| chaos                      | 84.4 ms                                                         | 54.3 ms: 1.55x faster                                                          |
| spectral_norm              | 122 ms                                                          | 78.4 ms: 1.55x faster                                                          |
| raytrace                   | 327 ms                                                          | 214 ms: 1.53x faster                                                           |
| comprehensions             | 22.1 us                                                         | 14.5 us: 1.53x faster                                                          |
| logging_silent             | 119 ns                                                          | 80.1 ns: 1.49x faster                                                          |
| richards                   | 48.8 ms                                                         | 32.9 ms: 1.48x faster                                                          |
| async_tree_none            | 343 ms                                                          | 236 ms: 1.45x faster                                                           |
| coroutines                 | 23.7 ms                                                         | 16.3 ms: 1.45x faster                                                          |
| async_tree_memoization     | 408 ms                                                          | 284 ms: 1.44x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 210 ms: 1.43x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 263 ms: 1.43x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 1.04 ms: 1.43x faster                                                          |
| nqueens                    | 111 ms                                                          | 79.1 ms: 1.41x faster                                                          |
| logging_simple             | 10.8 us                                                         | 7.71 us: 1.40x faster                                                          |
| json_dumps                 | 9.80 ms                                                         | 7.00 ms: 1.40x faster                                                          |
| deltablue                  | 4.10 ms                                                         | 2.96 ms: 1.39x faster                                                          |
| scimark_sor                | 135 ms                                                          | 97.7 ms: 1.38x faster                                                          |
| async_tree_io              | 754 ms                                                          | 545 ms: 1.38x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.67 sec: 1.38x faster                                                         |
| sqlglot_transpile          | 1.78 ms                                                         | 1.30 ms: 1.38x faster                                                          |
| logging_format             | 11.5 us                                                         | 8.34 us: 1.37x faster                                                          |
| scimark_fft                | 291 ms                                                          | 212 ms: 1.37x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 544 ms: 1.37x faster                                                           |
| fannkuch                   | 399 ms                                                          | 294 ms: 1.36x faster                                                           |
| float                      | 76.1 ms                                                         | 56.6 ms: 1.34x faster                                                          |
| crypto_pyaes               | 79.4 ms                                                         | 59.3 ms: 1.34x faster                                                          |
| mako                       | 10.3 ms                                                         | 7.84 ms: 1.31x faster                                                          |
| deepcopy_memo              | 40.0 us                                                         | 30.7 us: 1.30x faster                                                          |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.26 ms: 1.30x faster                                                          |
| scimark_monte_carlo        | 70.8 ms                                                         | 55.3 ms: 1.28x faster                                                          |
| unpickle_pure_python       | 231 us                                                          | 181 us: 1.28x faster                                                           |
| genshi_xml                 | 61.2 ms                                                         | 48.0 ms: 1.27x faster                                                          |
| pprint_pformat             | 1.70 sec                                                        | 1.34 sec: 1.27x faster                                                         |
| sympy_sum                  | 149 ms                                                          | 118 ms: 1.26x faster                                                           |
| pprint_safe_repr           | 819 ms                                                          | 651 ms: 1.26x faster                                                           |
| asyncio_tcp                | 787 ms                                                          | 634 ms: 1.24x faster                                                           |
| go                         | 147 ms                                                          | 119 ms: 1.24x faster                                                           |
| xml_etree_process          | 55.0 ms                                                         | 44.6 ms: 1.23x faster                                                          |
| mdp                        | 2.07 sec                                                        | 1.68 sec: 1.23x faster                                                         |
| scimark_lu                 | 102 ms                                                          | 83.0 ms: 1.23x faster                                                          |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 468 ms: 1.23x faster                                                           |
| pyflate                    | 471 ms                                                          | 385 ms: 1.22x faster                                                           |
| chameleon                  | 8.08 ms                                                         | 6.62 ms: 1.22x faster                                                          |
| pickle_pure_python         | 309 us                                                          | 254 us: 1.22x faster                                                           |
| deepcopy                   | 381 us                                                          | 314 us: 1.21x faster                                                           |
| genshi_text                | 26.8 ms                                                         | 22.1 ms: 1.21x faster                                                          |
| hexiom                     | 7.51 ms                                                         | 6.23 ms: 1.21x faster                                                          |
| tornado_http               | 118 ms                                                          | 99.4 ms: 1.19x faster                                                          |
| sympy_integrate            | 19.9 ms                                                         | 16.7 ms: 1.19x faster                                                          |
| pycparser                  | 1.04 sec                                                        | 878 ms: 1.19x faster                                                           |
| sympy_str                  | 283 ms                                                          | 239 ms: 1.19x faster                                                           |
| coverage                   | 58.0 ms                                                         | 48.9 ms: 1.19x faster                                                          |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 498 ms: 1.19x faster                                                           |
| deepcopy_reduce            | 3.32 us                                                         | 2.81 us: 1.18x faster                                                          |
| regex_compile              | 148 ms                                                          | 127 ms: 1.17x faster                                                           |
| xml_etree_generate         | 71.6 ms                                                         | 61.5 ms: 1.16x faster                                                          |
| sqlglot_optimize           | 51.8 ms                                                         | 44.8 ms: 1.16x faster                                                          |
| meteor_contest             | 90.9 ms                                                         | 80.2 ms: 1.13x faster                                                          |
| sqlite_synth               | 2.15 us                                                         | 1.90 us: 1.13x faster                                                          |
| bench_thread_pool          | 1.14 ms                                                         | 1.01 ms: 1.13x faster                                                          |
| xml_etree_iterparse        | 75.6 ms                                                         | 66.9 ms: 1.13x faster                                                          |
| django_template            | 37.4 ms                                                         | 33.6 ms: 1.11x faster                                                          |
| thrift                     | 801 us                                                          | 727 us: 1.10x faster                                                           |
| 2to3                       | 282 ms                                                          | 257 ms: 1.10x faster                                                           |
| xml_etree_parse            | 114 ms                                                          | 104 ms: 1.10x faster                                                           |
| sympy_expand               | 462 ms                                                          | 421 ms: 1.10x faster                                                           |
| html5lib                   | 54.3 ms                                                         | 50.5 ms: 1.07x faster                                                          |
| unpickle_list              | 3.28 us                                                         | 3.11 us: 1.05x faster                                                          |
| docutils                   | 2.10 sec                                                        | 2.02 sec: 1.04x faster                                                         |
| pidigits                   | 203 ms                                                          | 198 ms: 1.02x faster                                                           |
| python_startup             | 22.0 ms                                                         | 22.2 ms: 1.01x slower                                                          |
| pickle                     | 7.99 us                                                         | 8.10 us: 1.01x slower                                                          |
| bench_mp_pool              | 70.9 ms                                                         | 72.1 ms: 1.02x slower                                                          |
| pickle_dict                | 20.1 us                                                         | 20.6 us: 1.02x slower                                                          |
| regex_dna                  | 122 ms                                                          | 125 ms: 1.03x slower                                                           |
| json_loads                 | 20.0 us                                                         | 20.7 us: 1.04x slower                                                          |
| regex_effbot               | 1.82 ms                                                         | 1.92 ms: 1.05x slower                                                          |
| gc_traversal               | 1.38 ms                                                         | 1.46 ms: 1.06x slower                                                          |
| regex_v8                   | 15.2 ms                                                         | 16.2 ms: 1.07x slower                                                          |
| pathlib                    | 79.9 ms                                                         | 86.0 ms: 1.08x slower                                                          |
| pickle_list                | 3.27 us                                                         | 3.59 us: 1.10x slower                                                          |
| unpickle                   | 9.23 us                                                         | 10.2 us: 1.11x slower                                                          |
| async_generators           | 260 ms                                                          | 306 ms: 1.18x slower                                                           |
| telco                      | 5.29 ms                                                         | 6.46 ms: 1.22x slower                                                          |
| create_gc_cycles           | 618 us                                                          | 757 us: 1.23x slower                                                           |
| sqlglot_normalize          | 113 ms                                                          | 233 ms: 2.06x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.21x faster                                                                   |

Benchmark hidden because not significant (4): json, python_startup_no_site, asyncio_tcp_ssl, flaskblogging
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.18x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: unknown