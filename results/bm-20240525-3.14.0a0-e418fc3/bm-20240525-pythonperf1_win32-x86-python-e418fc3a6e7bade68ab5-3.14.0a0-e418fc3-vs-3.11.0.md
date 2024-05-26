# Results vs. 3.11.0

- fork: python
- ref: e418fc3a6e7bade68ab5
- machine: windows-x86
- commit hash: e418fc3
- commit date: 2024-05-25
- overall geometric mean: 1.32x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 233 ms: 1.21x faster                                                           |
| chameleon      | 8.08 ms                                                         | 5.72 ms: 1.41x faster                                                          |
| docutils       | 2.10 sec                                                        | 1.81 sec: 1.16x faster                                                         |
| html5lib       | 54.3 ms                                                         | 45.0 ms: 1.21x faster                                                          |
| tornado_http   | 118 ms                                                          | 94.8 ms: 1.25x faster                                                          |
| Geometric mean | (ref)                                                           | 1.24x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 227 ms: 1.51x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 276 ms: 1.48x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 204 ms: 1.47x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 257 ms: 1.47x faster                                                           |
| async_tree_io              | 754 ms                                                          | 528 ms: 1.43x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 534 ms: 1.40x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 453 ms: 1.27x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 476 ms: 1.24x faster                                                           |
| Geometric mean             | (ref)                                                           | 1.41x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 76.4 ms: 1.65x faster                                                          |
| float          | 76.1 ms                                                         | 52.6 ms: 1.45x faster                                                          |
| pidigits       | 203 ms                                                          | 199 ms: 1.02x faster                                                           |
| Geometric mean | (ref)                                                           | 1.34x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 98.9 ms: 1.49x faster                                                          |
| regex_dna      | 122 ms                                                          | 116 ms: 1.05x faster                                                           |
| regex_effbot   | 1.82 ms                                                         | 1.89 ms: 1.04x slower                                                          |
| regex_v8       | 15.2 ms                                                         | 15.9 ms: 1.05x slower                                                          |
| Geometric mean | (ref)                                                           | 1.10x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 148 us: 1.56x faster                                                           |
| tomli_loads          | 2.31 sec                                                        | 1.60 sec: 1.44x faster                                                         |
| json_dumps           | 9.80 ms                                                         | 6.95 ms: 1.41x faster                                                          |
| pickle_pure_python   | 309 us                                                          | 221 us: 1.40x faster                                                           |
| xml_etree_process    | 55.0 ms                                                         | 42.9 ms: 1.28x faster                                                          |
| xml_etree_generate   | 71.6 ms                                                         | 60.0 ms: 1.19x faster                                                          |
| xml_etree_iterparse  | 75.6 ms                                                         | 63.8 ms: 1.18x faster                                                          |
| unpickle_list        | 3.28 us                                                         | 2.97 us: 1.10x faster                                                          |
| xml_etree_parse      | 114 ms                                                          | 105 ms: 1.08x faster                                                           |
| pickle               | 7.99 us                                                         | 8.15 us: 1.02x slower                                                          |
| pickle_dict          | 20.1 us                                                         | 20.9 us: 1.04x slower                                                          |
| json_loads           | 20.0 us                                                         | 20.9 us: 1.04x slower                                                          |
| pickle_list          | 3.27 us                                                         | 3.63 us: 1.11x slower                                                          |
| unpickle             | 9.23 us                                                         | 10.4 us: 1.12x slower                                                          |
| Geometric mean       | (ref)                                                           | 1.15x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 18.6 ms: 1.01x faster                                                          |
| python_startup         | 22.0 ms                                                         | 22.8 ms: 1.04x slower                                                          |
| Geometric mean         | (ref)                                                           | 1.01x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|-----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 6.94 ms: 1.48x faster                                                          |
| genshi_text     | 26.8 ms                                                         | 19.1 ms: 1.40x faster                                                          |
| genshi_xml      | 61.2 ms                                                         | 44.2 ms: 1.39x faster                                                          |
| django_template | 37.4 ms                                                         | 30.4 ms: 1.23x faster                                                          |
| Geometric mean  | (ref)                                                           | 1.37x faster                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 133 us: 3.60x faster                                                           |
| generators                 | 52.2 ms                                                         | 21.5 ms: 2.43x faster                                                          |
| logging_silent             | 119 ns                                                          | 57.7 ns: 2.07x faster                                                          |
| pylint                     | 418 ms                                                          | 218 ms: 1.92x faster                                                           |
| comprehensions             | 22.1 us                                                         | 11.9 us: 1.85x faster                                                          |
| spectral_norm              | 122 ms                                                          | 66.2 ms: 1.84x faster                                                          |
| deltablue                  | 4.10 ms                                                         | 2.26 ms: 1.81x faster                                                          |
| chaos                      | 84.4 ms                                                         | 46.7 ms: 1.81x faster                                                          |
| raytrace                   | 327 ms                                                          | 185 ms: 1.77x faster                                                           |
| scimark_lu                 | 102 ms                                                          | 58.3 ms: 1.75x faster                                                          |
| hexiom                     | 7.51 ms                                                         | 4.33 ms: 1.73x faster                                                          |
| richards_super             | 58.7 ms                                                         | 34.2 ms: 1.71x faster                                                          |
| deepcopy_memo              | 40.0 us                                                         | 23.5 us: 1.70x faster                                                          |
| nqueens                    | 111 ms                                                          | 66.5 ms: 1.68x faster                                                          |
| nbody                      | 126 ms                                                          | 76.4 ms: 1.65x faster                                                          |
| richards                   | 48.8 ms                                                         | 30.5 ms: 1.60x faster                                                          |
| scimark_sor                | 135 ms                                                          | 85.0 ms: 1.59x faster                                                          |
| unpickle_pure_python       | 231 us                                                          | 148 us: 1.56x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 965 us: 1.54x faster                                                           |
| scimark_monte_carlo        | 70.8 ms                                                         | 46.3 ms: 1.53x faster                                                          |
| pyflate                    | 471 ms                                                          | 311 ms: 1.51x faster                                                           |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.80 ms: 1.51x faster                                                          |
| async_tree_none            | 343 ms                                                          | 227 ms: 1.51x faster                                                           |
| sqlglot_transpile          | 1.78 ms                                                         | 1.19 ms: 1.50x faster                                                          |
| coroutines                 | 23.7 ms                                                         | 15.9 ms: 1.50x faster                                                          |
| regex_compile              | 148 ms                                                          | 98.9 ms: 1.49x faster                                                          |
| fannkuch                   | 399 ms                                                          | 269 ms: 1.48x faster                                                           |
| mako                       | 10.3 ms                                                         | 6.94 ms: 1.48x faster                                                          |
| async_tree_memoization     | 408 ms                                                          | 276 ms: 1.48x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 204 ms: 1.47x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 257 ms: 1.47x faster                                                           |
| crypto_pyaes               | 79.4 ms                                                         | 54.4 ms: 1.46x faster                                                          |
| logging_simple             | 10.8 us                                                         | 7.47 us: 1.45x faster                                                          |
| float                      | 76.1 ms                                                         | 52.6 ms: 1.45x faster                                                          |
| tomli_loads                | 2.31 sec                                                        | 1.60 sec: 1.44x faster                                                         |
| sympy_sum                  | 149 ms                                                          | 104 ms: 1.44x faster                                                           |
| scimark_fft                | 291 ms                                                          | 203 ms: 1.43x faster                                                           |
| async_tree_io              | 754 ms                                                          | 528 ms: 1.43x faster                                                           |
| chameleon                  | 8.08 ms                                                         | 5.72 ms: 1.41x faster                                                          |
| go                         | 147 ms                                                          | 104 ms: 1.41x faster                                                           |
| json_dumps                 | 9.80 ms                                                         | 6.95 ms: 1.41x faster                                                          |
| genshi_text                | 26.8 ms                                                         | 19.1 ms: 1.40x faster                                                          |
| async_tree_io_tg           | 746 ms                                                          | 534 ms: 1.40x faster                                                           |
| logging_format             | 11.5 us                                                         | 8.19 us: 1.40x faster                                                          |
| pickle_pure_python         | 309 us                                                          | 221 us: 1.40x faster                                                           |
| genshi_xml                 | 61.2 ms                                                         | 44.2 ms: 1.39x faster                                                          |
| sympy_str                  | 283 ms                                                          | 206 ms: 1.38x faster                                                           |
| sympy_integrate            | 19.9 ms                                                         | 14.6 ms: 1.36x faster                                                          |
| pprint_pformat             | 1.70 sec                                                        | 1.25 sec: 1.36x faster                                                         |
| pprint_safe_repr           | 819 ms                                                          | 607 ms: 1.35x faster                                                           |
| deepcopy                   | 381 us                                                          | 283 us: 1.35x faster                                                           |
| pycparser                  | 1.04 sec                                                        | 788 ms: 1.32x faster                                                           |
| sqlglot_optimize           | 51.8 ms                                                         | 39.6 ms: 1.31x faster                                                          |
| xml_etree_process          | 55.0 ms                                                         | 42.9 ms: 1.28x faster                                                          |
| sympy_expand               | 462 ms                                                          | 361 ms: 1.28x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 453 ms: 1.27x faster                                                           |
| mdp                        | 2.07 sec                                                        | 1.63 sec: 1.26x faster                                                         |
| tornado_http               | 118 ms                                                          | 94.8 ms: 1.25x faster                                                          |
| deepcopy_reduce            | 3.32 us                                                         | 2.66 us: 1.25x faster                                                          |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 476 ms: 1.24x faster                                                           |
| django_template            | 37.4 ms                                                         | 30.4 ms: 1.23x faster                                                          |
| meteor_contest             | 90.9 ms                                                         | 74.4 ms: 1.22x faster                                                          |
| 2to3                       | 282 ms                                                          | 233 ms: 1.21x faster                                                           |
| html5lib                   | 54.3 ms                                                         | 45.0 ms: 1.21x faster                                                          |
| coverage                   | 58.0 ms                                                         | 48.4 ms: 1.20x faster                                                          |
| xml_etree_generate         | 71.6 ms                                                         | 60.0 ms: 1.19x faster                                                          |
| xml_etree_iterparse        | 75.6 ms                                                         | 63.8 ms: 1.18x faster                                                          |
| thrift                     | 801 us                                                          | 682 us: 1.17x faster                                                           |
| asyncio_tcp                | 787 ms                                                          | 674 ms: 1.17x faster                                                           |
| bench_thread_pool          | 1.14 ms                                                         | 975 us: 1.17x faster                                                           |
| docutils                   | 2.10 sec                                                        | 1.81 sec: 1.16x faster                                                         |
| json                       | 4.78 ms                                                         | 4.27 ms: 1.12x faster                                                          |
| sqlite_synth               | 2.15 us                                                         | 1.94 us: 1.11x faster                                                          |
| unpickle_list              | 3.28 us                                                         | 2.97 us: 1.10x faster                                                          |
| xml_etree_parse            | 114 ms                                                          | 105 ms: 1.08x faster                                                           |
| regex_dna                  | 122 ms                                                          | 116 ms: 1.05x faster                                                           |
| pidigits                   | 203 ms                                                          | 199 ms: 1.02x faster                                                           |
| python_startup_no_site     | 18.8 ms                                                         | 18.6 ms: 1.01x faster                                                          |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.9 sec: 1.01x faster                                                         |
| bench_mp_pool              | 70.9 ms                                                         | 71.2 ms: 1.00x slower                                                          |
| pickle                     | 7.99 us                                                         | 8.15 us: 1.02x slower                                                          |
| regex_effbot               | 1.82 ms                                                         | 1.89 ms: 1.04x slower                                                          |
| pickle_dict                | 20.1 us                                                         | 20.9 us: 1.04x slower                                                          |
| python_startup             | 22.0 ms                                                         | 22.8 ms: 1.04x slower                                                          |
| json_loads                 | 20.0 us                                                         | 20.9 us: 1.04x slower                                                          |
| async_generators           | 260 ms                                                          | 271 ms: 1.04x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 15.9 ms: 1.05x slower                                                          |
| gc_traversal               | 1.38 ms                                                         | 1.44 ms: 1.05x slower                                                          |
| pathlib                    | 79.9 ms                                                         | 87.5 ms: 1.09x slower                                                          |
| pickle_list                | 3.27 us                                                         | 3.63 us: 1.11x slower                                                          |
| unpickle                   | 9.23 us                                                         | 10.4 us: 1.12x slower                                                          |
| telco                      | 5.29 ms                                                         | 6.20 ms: 1.17x slower                                                          |
| create_gc_cycles           | 618 us                                                          | 750 us: 1.21x slower                                                           |
| sqlglot_normalize          | 113 ms                                                          | 204 ms: 1.80x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.32x faster                                                                   |

Benchmark hidden because not significant (1): flaskblogging
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.31x
- 95% likely to have a speedup of 1.29x
- 99% likely to have a speedup of 1.26x

# Memory
- memory change: unknown