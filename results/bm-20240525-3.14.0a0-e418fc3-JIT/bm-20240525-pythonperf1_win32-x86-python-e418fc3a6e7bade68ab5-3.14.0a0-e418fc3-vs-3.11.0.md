# Results vs. 3.11.0

- fork: python
- ref: e418fc3a6e7bade68ab5
- machine: windows-x86
- commit hash: e418fc3
- commit date: 2024-05-25
- overall geometric mean: 1.33x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 248 ms: 1.14x faster                                                           |
| chameleon      | 8.08 ms                                                         | 6.16 ms: 1.31x faster                                                          |
| docutils       | 2.10 sec                                                        | 1.88 sec: 1.11x faster                                                         |
| html5lib       | 54.3 ms                                                         | 45.1 ms: 1.20x faster                                                          |
| tornado_http   | 118 ms                                                          | 96.9 ms: 1.22x faster                                                          |
| Geometric mean | (ref)                                                           | 1.20x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 226 ms: 1.51x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 203 ms: 1.48x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 276 ms: 1.48x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 257 ms: 1.47x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 531 ms: 1.41x faster                                                           |
| async_tree_io              | 754 ms                                                          | 539 ms: 1.40x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 457 ms: 1.26x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 475 ms: 1.24x faster                                                           |
| Geometric mean             | (ref)                                                           | 1.40x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 52.6 ms: 2.39x faster                                                          |
| float          | 76.1 ms                                                         | 41.8 ms: 1.82x faster                                                          |
| pidigits       | 203 ms                                                          | 195 ms: 1.04x faster                                                           |
| Geometric mean | (ref)                                                           | 1.66x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 98.3 ms: 1.50x faster                                                          |
| regex_dna      | 122 ms                                                          | 118 ms: 1.03x faster                                                           |
| regex_v8       | 15.2 ms                                                         | 15.9 ms: 1.05x slower                                                          |
| regex_effbot   | 1.82 ms                                                         | 1.98 ms: 1.09x slower                                                          |
| Geometric mean | (ref)                                                           | 1.08x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 135 us: 1.72x faster                                                           |
| tomli_loads          | 2.31 sec                                                        | 1.41 sec: 1.64x faster                                                         |
| pickle_pure_python   | 309 us                                                          | 201 us: 1.54x faster                                                           |
| json_dumps           | 9.80 ms                                                         | 6.76 ms: 1.45x faster                                                          |
| xml_etree_process    | 55.0 ms                                                         | 41.1 ms: 1.34x faster                                                          |
| xml_etree_generate   | 71.6 ms                                                         | 55.7 ms: 1.29x faster                                                          |
| xml_etree_iterparse  | 75.6 ms                                                         | 61.0 ms: 1.24x faster                                                          |
| unpickle_list        | 3.28 us                                                         | 2.88 us: 1.14x faster                                                          |
| xml_etree_parse      | 114 ms                                                          | 103 ms: 1.10x faster                                                           |
| pickle               | 7.99 us                                                         | 8.10 us: 1.01x slower                                                          |
| pickle_dict          | 20.1 us                                                         | 20.5 us: 1.02x slower                                                          |
| json_loads           | 20.0 us                                                         | 20.8 us: 1.04x slower                                                          |
| pickle_list          | 3.27 us                                                         | 3.57 us: 1.09x slower                                                          |
| unpickle             | 9.23 us                                                         | 10.3 us: 1.11x slower                                                          |
| Geometric mean       | (ref)                                                           | 1.20x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 20.5 ms: 1.09x slower                                                          |
| python_startup         | 22.0 ms                                                         | 24.8 ms: 1.13x slower                                                          |
| Geometric mean         | (ref)                                                           | 1.11x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|-----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 5.29 ms: 1.94x faster                                                          |
| genshi_text     | 26.8 ms                                                         | 21.4 ms: 1.25x faster                                                          |
| genshi_xml      | 61.2 ms                                                         | 51.3 ms: 1.19x faster                                                          |
| django_template | 37.4 ms                                                         | 32.3 ms: 1.16x faster                                                          |
| Geometric mean  | (ref)                                                           | 1.35x faster                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240525-pythonperf1_win32-x86-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 137 us: 3.48x faster                                                           |
| spectral_norm              | 122 ms                                                          | 47.6 ms: 2.56x faster                                                          |
| nbody                      | 126 ms                                                          | 52.6 ms: 2.39x faster                                                          |
| generators                 | 52.2 ms                                                         | 23.4 ms: 2.23x faster                                                          |
| logging_silent             | 119 ns                                                          | 57.3 ns: 2.08x faster                                                          |
| comprehensions             | 22.1 us                                                         | 11.1 us: 2.00x faster                                                          |
| mako                       | 10.3 ms                                                         | 5.29 ms: 1.94x faster                                                          |
| deepcopy_memo              | 40.0 us                                                         | 20.6 us: 1.94x faster                                                          |
| float                      | 76.1 ms                                                         | 41.8 ms: 1.82x faster                                                          |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.36 ms: 1.80x faster                                                          |
| fannkuch                   | 399 ms                                                          | 225 ms: 1.78x faster                                                           |
| pylint                     | 418 ms                                                          | 241 ms: 1.73x faster                                                           |
| scimark_monte_carlo        | 70.8 ms                                                         | 40.9 ms: 1.73x faster                                                          |
| unpickle_pure_python       | 231 us                                                          | 135 us: 1.72x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 908 us: 1.64x faster                                                           |
| chaos                      | 84.4 ms                                                         | 51.4 ms: 1.64x faster                                                          |
| tomli_loads                | 2.31 sec                                                        | 1.41 sec: 1.64x faster                                                         |
| hexiom                     | 7.51 ms                                                         | 4.58 ms: 1.64x faster                                                          |
| richards_super             | 58.7 ms                                                         | 35.9 ms: 1.64x faster                                                          |
| nqueens                    | 111 ms                                                          | 69.6 ms: 1.60x faster                                                          |
| crypto_pyaes               | 79.4 ms                                                         | 49.7 ms: 1.60x faster                                                          |
| deltablue                  | 4.10 ms                                                         | 2.57 ms: 1.60x faster                                                          |
| scimark_fft                | 291 ms                                                          | 185 ms: 1.58x faster                                                           |
| raytrace                   | 327 ms                                                          | 211 ms: 1.55x faster                                                           |
| pickle_pure_python         | 309 us                                                          | 201 us: 1.54x faster                                                           |
| richards                   | 48.8 ms                                                         | 31.9 ms: 1.53x faster                                                          |
| sqlglot_transpile          | 1.78 ms                                                         | 1.17 ms: 1.52x faster                                                          |
| async_tree_none            | 343 ms                                                          | 226 ms: 1.51x faster                                                           |
| pyflate                    | 471 ms                                                          | 313 ms: 1.51x faster                                                           |
| regex_compile              | 148 ms                                                          | 98.3 ms: 1.50x faster                                                          |
| scimark_sor                | 135 ms                                                          | 90.3 ms: 1.50x faster                                                          |
| async_tree_none_tg         | 301 ms                                                          | 203 ms: 1.48x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 276 ms: 1.48x faster                                                           |
| pprint_pformat             | 1.70 sec                                                        | 1.15 sec: 1.47x faster                                                         |
| async_tree_memoization_tg  | 378 ms                                                          | 257 ms: 1.47x faster                                                           |
| logging_simple             | 10.8 us                                                         | 7.35 us: 1.47x faster                                                          |
| coroutines                 | 23.7 ms                                                         | 16.2 ms: 1.47x faster                                                          |
| pprint_safe_repr           | 819 ms                                                          | 562 ms: 1.46x faster                                                           |
| json_dumps                 | 9.80 ms                                                         | 6.76 ms: 1.45x faster                                                          |
| logging_format             | 11.5 us                                                         | 7.93 us: 1.44x faster                                                          |
| scimark_lu                 | 102 ms                                                          | 72.1 ms: 1.42x faster                                                          |
| async_tree_io_tg           | 746 ms                                                          | 531 ms: 1.41x faster                                                           |
| async_tree_io              | 754 ms                                                          | 539 ms: 1.40x faster                                                           |
| sympy_sum                  | 149 ms                                                          | 108 ms: 1.38x faster                                                           |
| xml_etree_process          | 55.0 ms                                                         | 41.1 ms: 1.34x faster                                                          |
| sympy_str                  | 283 ms                                                          | 212 ms: 1.33x faster                                                           |
| chameleon                  | 8.08 ms                                                         | 6.16 ms: 1.31x faster                                                          |
| go                         | 147 ms                                                          | 113 ms: 1.30x faster                                                           |
| asyncio_tcp                | 787 ms                                                          | 608 ms: 1.29x faster                                                           |
| xml_etree_generate         | 71.6 ms                                                         | 55.7 ms: 1.29x faster                                                          |
| pycparser                  | 1.04 sec                                                        | 811 ms: 1.29x faster                                                           |
| sympy_integrate            | 19.9 ms                                                         | 15.6 ms: 1.27x faster                                                          |
| mdp                        | 2.07 sec                                                        | 1.63 sec: 1.26x faster                                                         |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 457 ms: 1.26x faster                                                           |
| genshi_text                | 26.8 ms                                                         | 21.4 ms: 1.25x faster                                                          |
| meteor_contest             | 90.9 ms                                                         | 72.9 ms: 1.25x faster                                                          |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 475 ms: 1.24x faster                                                           |
| xml_etree_iterparse        | 75.6 ms                                                         | 61.0 ms: 1.24x faster                                                          |
| deepcopy                   | 381 us                                                          | 310 us: 1.23x faster                                                           |
| tornado_http               | 118 ms                                                          | 96.9 ms: 1.22x faster                                                          |
| sqlglot_optimize           | 51.8 ms                                                         | 42.5 ms: 1.22x faster                                                          |
| sympy_expand               | 462 ms                                                          | 379 ms: 1.22x faster                                                           |
| html5lib                   | 54.3 ms                                                         | 45.1 ms: 1.20x faster                                                          |
| genshi_xml                 | 61.2 ms                                                         | 51.3 ms: 1.19x faster                                                          |
| deepcopy_reduce            | 3.32 us                                                         | 2.84 us: 1.17x faster                                                          |
| coverage                   | 58.0 ms                                                         | 49.9 ms: 1.16x faster                                                          |
| bench_thread_pool          | 1.14 ms                                                         | 981 us: 1.16x faster                                                           |
| django_template            | 37.4 ms                                                         | 32.3 ms: 1.16x faster                                                          |
| sqlite_synth               | 2.15 us                                                         | 1.87 us: 1.15x faster                                                          |
| unpickle_list              | 3.28 us                                                         | 2.88 us: 1.14x faster                                                          |
| 2to3                       | 282 ms                                                          | 248 ms: 1.14x faster                                                           |
| json                       | 4.78 ms                                                         | 4.21 ms: 1.13x faster                                                          |
| thrift                     | 801 us                                                          | 710 us: 1.13x faster                                                           |
| docutils                   | 2.10 sec                                                        | 1.88 sec: 1.11x faster                                                         |
| xml_etree_parse            | 114 ms                                                          | 103 ms: 1.10x faster                                                           |
| pidigits                   | 203 ms                                                          | 195 ms: 1.04x faster                                                           |
| regex_dna                  | 122 ms                                                          | 118 ms: 1.03x faster                                                           |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.9 sec: 1.01x faster                                                         |
| flaskblogging              | 2.03 sec                                                        | 2.03 sec: 1.00x slower                                                         |
| pickle                     | 7.99 us                                                         | 8.10 us: 1.01x slower                                                          |
| pickle_dict                | 20.1 us                                                         | 20.5 us: 1.02x slower                                                          |
| json_loads                 | 20.0 us                                                         | 20.8 us: 1.04x slower                                                          |
| telco                      | 5.29 ms                                                         | 5.51 ms: 1.04x slower                                                          |
| regex_v8                   | 15.2 ms                                                         | 15.9 ms: 1.05x slower                                                          |
| bench_mp_pool              | 70.9 ms                                                         | 75.4 ms: 1.06x slower                                                          |
| gc_traversal               | 1.38 ms                                                         | 1.47 ms: 1.06x slower                                                          |
| pathlib                    | 79.9 ms                                                         | 86.4 ms: 1.08x slower                                                          |
| regex_effbot               | 1.82 ms                                                         | 1.98 ms: 1.09x slower                                                          |
| python_startup_no_site     | 18.8 ms                                                         | 20.5 ms: 1.09x slower                                                          |
| pickle_list                | 3.27 us                                                         | 3.57 us: 1.09x slower                                                          |
| unpickle                   | 9.23 us                                                         | 10.3 us: 1.11x slower                                                          |
| python_startup             | 22.0 ms                                                         | 24.8 ms: 1.13x slower                                                          |
| async_generators           | 260 ms                                                          | 296 ms: 1.14x slower                                                           |
| create_gc_cycles           | 618 us                                                          | 765 us: 1.24x slower                                                           |
| sqlglot_normalize          | 113 ms                                                          | 222 ms: 1.97x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.33x faster                                                                   |
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.28x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: unknown