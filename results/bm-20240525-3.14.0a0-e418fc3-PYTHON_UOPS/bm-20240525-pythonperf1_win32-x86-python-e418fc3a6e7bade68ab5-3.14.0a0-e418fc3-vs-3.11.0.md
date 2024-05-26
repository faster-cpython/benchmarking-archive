# Results vs. 3.11.0

- fork: python
- ref: e418fc3a6e7bade68ab5
- machine: windows-x86
- commit hash: e418fc3
- commit date: 2024-05-25
- overall geometric mean: 1.24x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 254 ms: 1.11x faster                                                           |
| chameleon      | 8.08 ms                                                         | 6.16 ms: 1.31x faster                                                          |
| docutils       | 2.10 sec                                                        | 2.03 sec: 1.04x faster                                                         |
| html5lib       | 54.3 ms                                                         | 50.2 ms: 1.08x faster                                                          |
| tornado_http   | 118 ms                                                          | 100 ms: 1.18x faster                                                           |
| Geometric mean | (ref)                                                           | 1.14x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 236 ms: 1.46x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 284 ms: 1.44x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 263 ms: 1.43x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 210 ms: 1.43x faster                                                           |
| async_tree_io              | 754 ms                                                          | 546 ms: 1.38x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 545 ms: 1.37x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 461 ms: 1.25x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 488 ms: 1.21x faster                                                           |
| Geometric mean             | (ref)                                                           | 1.37x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 75.6 ms: 1.67x faster                                                          |
| float          | 76.1 ms                                                         | 51.7 ms: 1.47x faster                                                          |
| pidigits       | 203 ms                                                          | 198 ms: 1.03x faster                                                           |
| Geometric mean | (ref)                                                           | 1.36x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 128 ms: 1.15x faster                                                           |
| regex_dna      | 122 ms                                                          | 117 ms: 1.04x faster                                                           |
| regex_effbot   | 1.82 ms                                                         | 1.89 ms: 1.04x slower                                                          |
| regex_v8       | 15.2 ms                                                         | 16.1 ms: 1.06x slower                                                          |
| Geometric mean | (ref)                                                           | 1.02x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| tomli_loads          | 2.31 sec                                                        | 1.63 sec: 1.42x faster                                                         |
| json_dumps           | 9.80 ms                                                         | 6.97 ms: 1.41x faster                                                          |
| unpickle_pure_python | 231 us                                                          | 170 us: 1.36x faster                                                           |
| pickle_pure_python   | 309 us                                                          | 243 us: 1.27x faster                                                           |
| xml_etree_process    | 55.0 ms                                                         | 43.4 ms: 1.27x faster                                                          |
| xml_etree_generate   | 71.6 ms                                                         | 60.9 ms: 1.18x faster                                                          |
| xml_etree_iterparse  | 75.6 ms                                                         | 64.4 ms: 1.17x faster                                                          |
| xml_etree_parse      | 114 ms                                                          | 104 ms: 1.10x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 3.17 us: 1.03x faster                                                          |
| json_loads           | 20.0 us                                                         | 20.3 us: 1.01x slower                                                          |
| pickle_dict          | 20.1 us                                                         | 20.6 us: 1.03x slower                                                          |
| pickle               | 7.99 us                                                         | 8.36 us: 1.05x slower                                                          |
| pickle_list          | 3.27 us                                                         | 3.54 us: 1.08x slower                                                          |
| unpickle             | 9.23 us                                                         | 10.3 us: 1.11x slower                                                          |
| Geometric mean       | (ref)                                                           | 1.13x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 18.4 ms: 1.02x faster                                                          |
| python_startup         | 22.0 ms                                                         | 22.7 ms: 1.03x slower                                                          |
| Geometric mean         | (ref)                                                           | 1.01x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|-----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 7.12 ms: 1.44x faster                                                          |
| genshi_xml      | 61.2 ms                                                         | 48.6 ms: 1.26x faster                                                          |
| genshi_text     | 26.8 ms                                                         | 21.8 ms: 1.23x faster                                                          |
| django_template | 37.4 ms                                                         | 32.6 ms: 1.15x faster                                                          |
| Geometric mean  | (ref)                                                           | 1.26x faster                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 143 us: 3.35x faster                                                           |
| generators                 | 52.2 ms                                                         | 23.0 ms: 2.27x faster                                                          |
| pylint                     | 418 ms                                                          | 243 ms: 1.72x faster                                                           |
| spectral_norm              | 122 ms                                                          | 70.9 ms: 1.72x faster                                                          |
| richards_super             | 58.7 ms                                                         | 34.7 ms: 1.69x faster                                                          |
| nbody                      | 126 ms                                                          | 75.6 ms: 1.67x faster                                                          |
| chaos                      | 84.4 ms                                                         | 51.0 ms: 1.66x faster                                                          |
| comprehensions             | 22.1 us                                                         | 13.5 us: 1.63x faster                                                          |
| logging_silent             | 119 ns                                                          | 73.4 ns: 1.62x faster                                                          |
| richards                   | 48.8 ms                                                         | 30.4 ms: 1.60x faster                                                          |
| raytrace                   | 327 ms                                                          | 210 ms: 1.56x faster                                                           |
| coroutines                 | 23.7 ms                                                         | 15.8 ms: 1.50x faster                                                          |
| nqueens                    | 111 ms                                                          | 74.4 ms: 1.50x faster                                                          |
| sqlglot_parse              | 1.49 ms                                                         | 997 us: 1.50x faster                                                           |
| deepcopy_memo              | 40.0 us                                                         | 27.2 us: 1.47x faster                                                          |
| float                      | 76.1 ms                                                         | 51.7 ms: 1.47x faster                                                          |
| async_tree_none            | 343 ms                                                          | 236 ms: 1.46x faster                                                           |
| fannkuch                   | 399 ms                                                          | 275 ms: 1.45x faster                                                           |
| deltablue                  | 4.10 ms                                                         | 2.83 ms: 1.45x faster                                                          |
| mako                       | 10.3 ms                                                         | 7.12 ms: 1.44x faster                                                          |
| async_tree_memoization     | 408 ms                                                          | 284 ms: 1.44x faster                                                           |
| scimark_monte_carlo        | 70.8 ms                                                         | 49.4 ms: 1.43x faster                                                          |
| async_tree_memoization_tg  | 378 ms                                                          | 263 ms: 1.43x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 210 ms: 1.43x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.63 sec: 1.42x faster                                                         |
| sqlglot_transpile          | 1.78 ms                                                         | 1.26 ms: 1.42x faster                                                          |
| json_dumps                 | 9.80 ms                                                         | 6.97 ms: 1.41x faster                                                          |
| logging_simple             | 10.8 us                                                         | 7.68 us: 1.41x faster                                                          |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.01 ms: 1.40x faster                                                          |
| scimark_sor                | 135 ms                                                          | 97.0 ms: 1.39x faster                                                          |
| async_tree_io              | 754 ms                                                          | 546 ms: 1.38x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 545 ms: 1.37x faster                                                           |
| scimark_fft                | 291 ms                                                          | 213 ms: 1.37x faster                                                           |
| logging_format             | 11.5 us                                                         | 8.37 us: 1.37x faster                                                          |
| unpickle_pure_python       | 231 us                                                          | 170 us: 1.36x faster                                                           |
| crypto_pyaes               | 79.4 ms                                                         | 58.2 ms: 1.36x faster                                                          |
| pprint_pformat             | 1.70 sec                                                        | 1.25 sec: 1.36x faster                                                         |
| pprint_safe_repr           | 819 ms                                                          | 607 ms: 1.35x faster                                                           |
| hexiom                     | 7.51 ms                                                         | 5.58 ms: 1.35x faster                                                          |
| chameleon                  | 8.08 ms                                                         | 6.16 ms: 1.31x faster                                                          |
| scimark_lu                 | 102 ms                                                          | 78.4 ms: 1.30x faster                                                          |
| asyncio_tcp                | 787 ms                                                          | 606 ms: 1.30x faster                                                           |
| go                         | 147 ms                                                          | 115 ms: 1.28x faster                                                           |
| pyflate                    | 471 ms                                                          | 369 ms: 1.28x faster                                                           |
| pickle_pure_python         | 309 us                                                          | 243 us: 1.27x faster                                                           |
| sympy_sum                  | 149 ms                                                          | 118 ms: 1.27x faster                                                           |
| xml_etree_process          | 55.0 ms                                                         | 43.4 ms: 1.27x faster                                                          |
| genshi_xml                 | 61.2 ms                                                         | 48.6 ms: 1.26x faster                                                          |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 461 ms: 1.25x faster                                                           |
| deepcopy                   | 381 us                                                          | 305 us: 1.25x faster                                                           |
| mdp                        | 2.07 sec                                                        | 1.67 sec: 1.24x faster                                                         |
| genshi_text                | 26.8 ms                                                         | 21.8 ms: 1.23x faster                                                          |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 488 ms: 1.21x faster                                                           |
| sympy_integrate            | 19.9 ms                                                         | 16.5 ms: 1.20x faster                                                          |
| pycparser                  | 1.04 sec                                                        | 874 ms: 1.19x faster                                                           |
| sympy_str                  | 283 ms                                                          | 237 ms: 1.19x faster                                                           |
| tornado_http               | 118 ms                                                          | 100 ms: 1.18x faster                                                           |
| xml_etree_generate         | 71.6 ms                                                         | 60.9 ms: 1.18x faster                                                          |
| xml_etree_iterparse        | 75.6 ms                                                         | 64.4 ms: 1.17x faster                                                          |
| meteor_contest             | 90.9 ms                                                         | 77.7 ms: 1.17x faster                                                          |
| sqlglot_optimize           | 51.8 ms                                                         | 44.3 ms: 1.17x faster                                                          |
| coverage                   | 58.0 ms                                                         | 49.7 ms: 1.17x faster                                                          |
| json                       | 4.78 ms                                                         | 4.11 ms: 1.16x faster                                                          |
| regex_compile              | 148 ms                                                          | 128 ms: 1.15x faster                                                           |
| django_template            | 37.4 ms                                                         | 32.6 ms: 1.15x faster                                                          |
| deepcopy_reduce            | 3.32 us                                                         | 2.91 us: 1.14x faster                                                          |
| bench_thread_pool          | 1.14 ms                                                         | 1.02 ms: 1.11x faster                                                          |
| sqlite_synth               | 2.15 us                                                         | 1.93 us: 1.11x faster                                                          |
| 2to3                       | 282 ms                                                          | 254 ms: 1.11x faster                                                           |
| xml_etree_parse            | 114 ms                                                          | 104 ms: 1.10x faster                                                           |
| html5lib                   | 54.3 ms                                                         | 50.2 ms: 1.08x faster                                                          |
| sympy_expand               | 462 ms                                                          | 428 ms: 1.08x faster                                                           |
| thrift                     | 801 us                                                          | 743 us: 1.08x faster                                                           |
| regex_dna                  | 122 ms                                                          | 117 ms: 1.04x faster                                                           |
| docutils                   | 2.10 sec                                                        | 2.03 sec: 1.04x faster                                                         |
| unpickle_list              | 3.28 us                                                         | 3.17 us: 1.03x faster                                                          |
| pidigits                   | 203 ms                                                          | 198 ms: 1.03x faster                                                           |
| python_startup_no_site     | 18.8 ms                                                         | 18.4 ms: 1.02x faster                                                          |
| flaskblogging              | 2.03 sec                                                        | 2.03 sec: 1.00x slower                                                         |
| json_loads                 | 20.0 us                                                         | 20.3 us: 1.01x slower                                                          |
| pickle_dict                | 20.1 us                                                         | 20.6 us: 1.03x slower                                                          |
| bench_mp_pool              | 70.9 ms                                                         | 73.1 ms: 1.03x slower                                                          |
| python_startup             | 22.0 ms                                                         | 22.7 ms: 1.03x slower                                                          |
| regex_effbot               | 1.82 ms                                                         | 1.89 ms: 1.04x slower                                                          |
| gc_traversal               | 1.38 ms                                                         | 1.44 ms: 1.04x slower                                                          |
| pickle                     | 7.99 us                                                         | 8.36 us: 1.05x slower                                                          |
| regex_v8                   | 15.2 ms                                                         | 16.1 ms: 1.06x slower                                                          |
| pickle_list                | 3.27 us                                                         | 3.54 us: 1.08x slower                                                          |
| pathlib                    | 79.9 ms                                                         | 87.3 ms: 1.09x slower                                                          |
| unpickle                   | 9.23 us                                                         | 10.3 us: 1.11x slower                                                          |
| telco                      | 5.29 ms                                                         | 5.93 ms: 1.12x slower                                                          |
| async_generators           | 260 ms                                                          | 293 ms: 1.13x slower                                                           |
| create_gc_cycles           | 618 us                                                          | 768 us: 1.24x slower                                                           |
| sqlglot_normalize          | 113 ms                                                          | 226 ms: 2.00x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.24x faster                                                                   |

Benchmark hidden because not significant (1): asyncio_tcp_ssl
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.21x
- 95% likely to have a speedup of 1.19x
- 99% likely to have a speedup of 1.18x

# Memory
- memory change: unknown