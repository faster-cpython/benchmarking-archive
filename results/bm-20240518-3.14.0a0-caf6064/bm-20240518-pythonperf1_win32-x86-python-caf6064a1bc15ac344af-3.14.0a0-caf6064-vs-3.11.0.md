# Results vs. 3.11.0

- fork: python
- ref: caf6064a1bc15ac344af
- machine: windows-x86
- commit hash: caf6064
- commit date: 2024-05-18
- overall geometric mean: 1.31x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 235 ms: 1.20x faster                                                           |
| chameleon      | 8.08 ms                                                         | 5.69 ms: 1.42x faster                                                          |
| docutils       | 2.10 sec                                                        | 1.80 sec: 1.16x faster                                                         |
| html5lib       | 54.3 ms                                                         | 44.7 ms: 1.22x faster                                                          |
| tornado_http   | 118 ms                                                          | 94.0 ms: 1.26x faster                                                          |
| Geometric mean | (ref)                                                           | 1.25x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 228 ms: 1.50x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 203 ms: 1.48x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 256 ms: 1.47x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 277 ms: 1.47x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 527 ms: 1.42x faster                                                           |
| async_tree_io              | 754 ms                                                          | 533 ms: 1.42x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 475 ms: 1.21x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 496 ms: 1.19x faster                                                           |
| Geometric mean             | (ref)                                                           | 1.39x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 78.9 ms: 1.60x faster                                                          |
| float          | 76.1 ms                                                         | 53.5 ms: 1.42x faster                                                          |
| pidigits       | 203 ms                                                          | 197 ms: 1.03x faster                                                           |
| Geometric mean | (ref)                                                           | 1.33x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 97.6 ms: 1.51x faster                                                          |
| regex_dna      | 122 ms                                                          | 117 ms: 1.04x faster                                                           |
| regex_v8       | 15.2 ms                                                         | 15.8 ms: 1.04x slower                                                          |
| regex_effbot   | 1.82 ms                                                         | 1.90 ms: 1.04x slower                                                          |
| Geometric mean | (ref)                                                           | 1.10x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 150 us: 1.54x faster                                                           |
| tomli_loads          | 2.31 sec                                                        | 1.64 sec: 1.41x faster                                                         |
| json_dumps           | 9.80 ms                                                         | 7.04 ms: 1.39x faster                                                          |
| pickle_pure_python   | 309 us                                                          | 223 us: 1.39x faster                                                           |
| xml_etree_process    | 55.0 ms                                                         | 42.5 ms: 1.29x faster                                                          |
| xml_etree_generate   | 71.6 ms                                                         | 60.0 ms: 1.19x faster                                                          |
| xml_etree_iterparse  | 75.6 ms                                                         | 63.5 ms: 1.19x faster                                                          |
| xml_etree_parse      | 114 ms                                                          | 103 ms: 1.11x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 3.03 us: 1.08x faster                                                          |
| json_loads           | 20.0 us                                                         | 20.5 us: 1.02x slower                                                          |
| pickle_dict          | 20.1 us                                                         | 20.7 us: 1.03x slower                                                          |
| pickle_list          | 3.27 us                                                         | 3.51 us: 1.07x slower                                                          |
| unpickle             | 9.23 us                                                         | 10.2 us: 1.11x slower                                                          |
| Geometric mean       | (ref)                                                           | 1.15x faster                                                                   |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 19.0 ms: 1.01x slower                                                          |
| python_startup         | 22.0 ms                                                         | 22.6 ms: 1.03x slower                                                          |
| Geometric mean         | (ref)                                                           | 1.02x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|-----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 7.12 ms: 1.44x faster                                                          |
| genshi_text     | 26.8 ms                                                         | 19.3 ms: 1.39x faster                                                          |
| genshi_xml      | 61.2 ms                                                         | 44.4 ms: 1.38x faster                                                          |
| django_template | 37.4 ms                                                         | 29.4 ms: 1.27x faster                                                          |
| Geometric mean  | (ref)                                                           | 1.37x faster                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240518-pythonperf1_win32-x86-python-caf6064a1bc15ac344af-3.14.0a0-caf6064 |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 133 us: 3.60x faster                                                           |
| generators                 | 52.2 ms                                                         | 21.7 ms: 2.41x faster                                                          |
| logging_silent             | 119 ns                                                          | 57.8 ns: 2.06x faster                                                          |
| pylint                     | 418 ms                                                          | 218 ms: 1.92x faster                                                           |
| comprehensions             | 22.1 us                                                         | 11.8 us: 1.87x faster                                                          |
| deltablue                  | 4.10 ms                                                         | 2.22 ms: 1.84x faster                                                          |
| chaos                      | 84.4 ms                                                         | 46.6 ms: 1.81x faster                                                          |
| raytrace                   | 327 ms                                                          | 183 ms: 1.78x faster                                                           |
| spectral_norm              | 122 ms                                                          | 68.4 ms: 1.78x faster                                                          |
| hexiom                     | 7.51 ms                                                         | 4.38 ms: 1.71x faster                                                          |
| scimark_lu                 | 102 ms                                                          | 61.0 ms: 1.68x faster                                                          |
| richards_super             | 58.7 ms                                                         | 35.4 ms: 1.66x faster                                                          |
| nqueens                    | 111 ms                                                          | 68.5 ms: 1.63x faster                                                          |
| deepcopy_memo              | 40.0 us                                                         | 24.6 us: 1.62x faster                                                          |
| nbody                      | 126 ms                                                          | 78.9 ms: 1.60x faster                                                          |
| sqlglot_parse              | 1.49 ms                                                         | 954 us: 1.56x faster                                                           |
| richards                   | 48.8 ms                                                         | 31.5 ms: 1.55x faster                                                          |
| unpickle_pure_python       | 231 us                                                          | 150 us: 1.54x faster                                                           |
| pyflate                    | 471 ms                                                          | 310 ms: 1.52x faster                                                           |
| regex_compile              | 148 ms                                                          | 97.6 ms: 1.51x faster                                                          |
| async_tree_none            | 343 ms                                                          | 228 ms: 1.50x faster                                                           |
| sqlglot_transpile          | 1.78 ms                                                         | 1.19 ms: 1.50x faster                                                          |
| async_tree_none_tg         | 301 ms                                                          | 203 ms: 1.48x faster                                                           |
| scimark_sor                | 135 ms                                                          | 91.4 ms: 1.48x faster                                                          |
| async_tree_memoization_tg  | 378 ms                                                          | 256 ms: 1.47x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 277 ms: 1.47x faster                                                           |
| coroutines                 | 23.7 ms                                                         | 16.1 ms: 1.47x faster                                                          |
| scimark_monte_carlo        | 70.8 ms                                                         | 48.3 ms: 1.47x faster                                                          |
| crypto_pyaes               | 79.4 ms                                                         | 54.6 ms: 1.45x faster                                                          |
| mako                       | 10.3 ms                                                         | 7.12 ms: 1.44x faster                                                          |
| go                         | 147 ms                                                          | 102 ms: 1.44x faster                                                           |
| sympy_sum                  | 149 ms                                                          | 104 ms: 1.44x faster                                                           |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.95 ms: 1.43x faster                                                          |
| float                      | 76.1 ms                                                         | 53.5 ms: 1.42x faster                                                          |
| chameleon                  | 8.08 ms                                                         | 5.69 ms: 1.42x faster                                                          |
| async_tree_io_tg           | 746 ms                                                          | 527 ms: 1.42x faster                                                           |
| async_tree_io              | 754 ms                                                          | 533 ms: 1.42x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.64 sec: 1.41x faster                                                         |
| logging_simple             | 10.8 us                                                         | 7.66 us: 1.41x faster                                                          |
| scimark_fft                | 291 ms                                                          | 207 ms: 1.41x faster                                                           |
| json_dumps                 | 9.80 ms                                                         | 7.04 ms: 1.39x faster                                                          |
| pprint_pformat             | 1.70 sec                                                        | 1.22 sec: 1.39x faster                                                         |
| genshi_text                | 26.8 ms                                                         | 19.3 ms: 1.39x faster                                                          |
| pickle_pure_python         | 309 us                                                          | 223 us: 1.39x faster                                                           |
| fannkuch                   | 399 ms                                                          | 288 ms: 1.39x faster                                                           |
| sympy_str                  | 283 ms                                                          | 205 ms: 1.38x faster                                                           |
| genshi_xml                 | 61.2 ms                                                         | 44.4 ms: 1.38x faster                                                          |
| logging_format             | 11.5 us                                                         | 8.31 us: 1.38x faster                                                          |
| pprint_safe_repr           | 819 ms                                                          | 599 ms: 1.37x faster                                                           |
| sympy_integrate            | 19.9 ms                                                         | 14.6 ms: 1.37x faster                                                          |
| pycparser                  | 1.04 sec                                                        | 795 ms: 1.31x faster                                                           |
| sqlglot_optimize           | 51.8 ms                                                         | 39.6 ms: 1.31x faster                                                          |
| deepcopy                   | 381 us                                                          | 292 us: 1.30x faster                                                           |
| xml_etree_process          | 55.0 ms                                                         | 42.5 ms: 1.29x faster                                                          |
| mdp                        | 2.07 sec                                                        | 1.61 sec: 1.28x faster                                                         |
| django_template            | 37.4 ms                                                         | 29.4 ms: 1.27x faster                                                          |
| sympy_expand               | 462 ms                                                          | 365 ms: 1.27x faster                                                           |
| tornado_http               | 118 ms                                                          | 94.0 ms: 1.26x faster                                                          |
| deepcopy_reduce            | 3.32 us                                                         | 2.66 us: 1.24x faster                                                          |
| html5lib                   | 54.3 ms                                                         | 44.7 ms: 1.22x faster                                                          |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 475 ms: 1.21x faster                                                           |
| asyncio_tcp                | 787 ms                                                          | 651 ms: 1.21x faster                                                           |
| meteor_contest             | 90.9 ms                                                         | 75.3 ms: 1.21x faster                                                          |
| 2to3                       | 282 ms                                                          | 235 ms: 1.20x faster                                                           |
| xml_etree_generate         | 71.6 ms                                                         | 60.0 ms: 1.19x faster                                                          |
| xml_etree_iterparse        | 75.6 ms                                                         | 63.5 ms: 1.19x faster                                                          |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 496 ms: 1.19x faster                                                           |
| bench_thread_pool          | 1.14 ms                                                         | 969 us: 1.17x faster                                                           |
| docutils                   | 2.10 sec                                                        | 1.80 sec: 1.16x faster                                                         |
| json                       | 4.78 ms                                                         | 4.16 ms: 1.15x faster                                                          |
| coverage                   | 58.0 ms                                                         | 50.9 ms: 1.14x faster                                                          |
| thrift                     | 801 us                                                          | 709 us: 1.13x faster                                                           |
| xml_etree_parse            | 114 ms                                                          | 103 ms: 1.11x faster                                                           |
| sqlite_synth               | 2.15 us                                                         | 1.93 us: 1.11x faster                                                          |
| unpickle_list              | 3.28 us                                                         | 3.03 us: 1.08x faster                                                          |
| regex_dna                  | 122 ms                                                          | 117 ms: 1.04x faster                                                           |
| pidigits                   | 203 ms                                                          | 197 ms: 1.03x faster                                                           |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.8 sec: 1.01x faster                                                         |
| python_startup_no_site     | 18.8 ms                                                         | 19.0 ms: 1.01x slower                                                          |
| bench_mp_pool              | 70.9 ms                                                         | 71.9 ms: 1.01x slower                                                          |
| json_loads                 | 20.0 us                                                         | 20.5 us: 1.02x slower                                                          |
| pickle_dict                | 20.1 us                                                         | 20.7 us: 1.03x slower                                                          |
| python_startup             | 22.0 ms                                                         | 22.6 ms: 1.03x slower                                                          |
| gc_traversal               | 1.38 ms                                                         | 1.43 ms: 1.04x slower                                                          |
| regex_v8                   | 15.2 ms                                                         | 15.8 ms: 1.04x slower                                                          |
| regex_effbot               | 1.82 ms                                                         | 1.90 ms: 1.04x slower                                                          |
| async_generators           | 260 ms                                                          | 276 ms: 1.06x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 85.8 ms: 1.07x slower                                                          |
| pickle_list                | 3.27 us                                                         | 3.51 us: 1.07x slower                                                          |
| unpickle                   | 9.23 us                                                         | 10.2 us: 1.11x slower                                                          |
| create_gc_cycles           | 618 us                                                          | 732 us: 1.19x slower                                                           |
| telco                      | 5.29 ms                                                         | 6.28 ms: 1.19x slower                                                          |
| sqlglot_normalize          | 113 ms                                                          | 204 ms: 1.81x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.31x faster                                                                   |

Benchmark hidden because not significant (2): pickle, flaskblogging
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.29x
- 95% likely to have a speedup of 1.28x
- 99% likely to have a speedup of 1.27x

# Memory
- memory change: unknown