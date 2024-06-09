# Results vs. 3.11.0

- fork: python
- ref: c15f94d6fbc960790db3
- machine: windows-x86
- commit hash: c15f94d
- commit date: 2024-06-08
- overall geometric mean: 1.28x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 246 ms: 1.15x faster                                                            |
| chameleon      | 8.08 ms                                                         | 6.01 ms: 1.34x faster                                                           |
| docutils       | 2.10 sec                                                        | 1.88 sec: 1.12x faster                                                          |
| html5lib       | 54.3 ms                                                         | 46.1 ms: 1.18x faster                                                           |
| tornado_http   | 118 ms                                                          | 97.1 ms: 1.22x faster                                                           |
| Geometric mean | (ref)                                                           | 1.20x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 227 ms: 1.51x faster                                                            |
| async_tree_none_tg         | 301 ms                                                          | 206 ms: 1.46x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 259 ms: 1.46x faster                                                            |
| async_tree_memoization     | 408 ms                                                          | 287 ms: 1.42x faster                                                            |
| async_tree_io              | 754 ms                                                          | 531 ms: 1.42x faster                                                            |
| async_tree_io_tg           | 746 ms                                                          | 535 ms: 1.39x faster                                                            |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 452 ms: 1.28x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 469 ms: 1.26x faster                                                            |
| Geometric mean             | (ref)                                                           | 1.40x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 53.4 ms: 2.36x faster                                                           |
| float          | 76.1 ms                                                         | 41.9 ms: 1.82x faster                                                           |
| pidigits       | 203 ms                                                          | 196 ms: 1.04x faster                                                            |
| Geometric mean | (ref)                                                           | 1.64x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 92.1 ms: 1.60x faster                                                           |
| regex_dna      | 122 ms                                                          | 123 ms: 1.01x slower                                                            |
| regex_v8       | 15.2 ms                                                         | 16.0 ms: 1.05x slower                                                           |
| regex_effbot   | 1.82 ms                                                         | 1.95 ms: 1.07x slower                                                           |
| Geometric mean | (ref)                                                           | 1.09x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 134 us: 1.72x faster                                                            |
| tomli_loads          | 2.31 sec                                                        | 1.40 sec: 1.65x faster                                                          |
| pickle_pure_python   | 309 us                                                          | 198 us: 1.56x faster                                                            |
| json_dumps           | 9.80 ms                                                         | 6.54 ms: 1.50x faster                                                           |
| xml_etree_process    | 55.0 ms                                                         | 40.9 ms: 1.35x faster                                                           |
| xml_etree_generate   | 71.6 ms                                                         | 55.6 ms: 1.29x faster                                                           |
| xml_etree_iterparse  | 75.6 ms                                                         | 60.4 ms: 1.25x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 2.80 us: 1.17x faster                                                           |
| xml_etree_parse      | 114 ms                                                          | 103 ms: 1.11x faster                                                            |
| json_loads           | 20.0 us                                                         | 20.5 us: 1.02x slower                                                           |
| pickle_dict          | 20.1 us                                                         | 20.8 us: 1.03x slower                                                           |
| pickle               | 7.99 us                                                         | 8.32 us: 1.04x slower                                                           |
| pickle_list          | 3.27 us                                                         | 3.58 us: 1.10x slower                                                           |
| unpickle             | 9.23 us                                                         | 10.5 us: 1.13x slower                                                           |
| Geometric mean       | (ref)                                                           | 1.21x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 20.9 ms: 1.11x slower                                                           |
| python_startup         | 22.0 ms                                                         | 24.8 ms: 1.13x slower                                                           |
| Geometric mean         | (ref)                                                           | 1.12x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 5.34 ms: 1.92x faster                                                           |
| genshi_text     | 26.8 ms                                                         | 20.9 ms: 1.28x faster                                                           |
| genshi_xml      | 61.2 ms                                                         | 50.0 ms: 1.23x faster                                                           |
| django_template | 37.4 ms                                                         | 30.8 ms: 1.22x faster                                                           |
| Geometric mean  | (ref)                                                           | 1.38x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf1_win32-x86-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 141 us: 3.40x faster                                                            |
| spectral_norm              | 122 ms                                                          | 47.5 ms: 2.56x faster                                                           |
| nbody                      | 126 ms                                                          | 53.4 ms: 2.36x faster                                                           |
| logging_silent             | 119 ns                                                          | 54.2 ns: 2.20x faster                                                           |
| generators                 | 52.2 ms                                                         | 23.9 ms: 2.18x faster                                                           |
| comprehensions             | 22.1 us                                                         | 10.8 us: 2.04x faster                                                           |
| deepcopy_memo              | 40.0 us                                                         | 20.1 us: 1.99x faster                                                           |
| mako                       | 10.3 ms                                                         | 5.34 ms: 1.92x faster                                                           |
| fannkuch                   | 399 ms                                                          | 216 ms: 1.85x faster                                                            |
| float                      | 76.1 ms                                                         | 41.9 ms: 1.82x faster                                                           |
| scimark_monte_carlo        | 70.8 ms                                                         | 39.6 ms: 1.79x faster                                                           |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.39 ms: 1.77x faster                                                           |
| scimark_fft                | 291 ms                                                          | 165 ms: 1.77x faster                                                            |
| pylint                     | 418 ms                                                          | 237 ms: 1.76x faster                                                            |
| unpickle_pure_python       | 231 us                                                          | 134 us: 1.72x faster                                                            |
| chaos                      | 84.4 ms                                                         | 50.1 ms: 1.69x faster                                                           |
| richards_super             | 58.7 ms                                                         | 34.8 ms: 1.68x faster                                                           |
| crypto_pyaes               | 79.4 ms                                                         | 47.1 ms: 1.68x faster                                                           |
| hexiom                     | 7.51 ms                                                         | 4.49 ms: 1.67x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.40 sec: 1.65x faster                                                          |
| sqlglot_parse              | 1.49 ms                                                         | 904 us: 1.65x faster                                                            |
| deltablue                  | 4.10 ms                                                         | 2.51 ms: 1.63x faster                                                           |
| nqueens                    | 111 ms                                                          | 68.9 ms: 1.62x faster                                                           |
| raytrace                   | 327 ms                                                          | 204 ms: 1.61x faster                                                            |
| regex_compile              | 148 ms                                                          | 92.1 ms: 1.60x faster                                                           |
| richards                   | 48.8 ms                                                         | 30.9 ms: 1.58x faster                                                           |
| pickle_pure_python         | 309 us                                                          | 198 us: 1.56x faster                                                            |
| pyflate                    | 471 ms                                                          | 303 ms: 1.55x faster                                                            |
| sqlglot_transpile          | 1.78 ms                                                         | 1.17 ms: 1.53x faster                                                           |
| scimark_sor                | 135 ms                                                          | 88.6 ms: 1.53x faster                                                           |
| coroutines                 | 23.7 ms                                                         | 15.6 ms: 1.52x faster                                                           |
| async_tree_none            | 343 ms                                                          | 227 ms: 1.51x faster                                                            |
| json_dumps                 | 9.80 ms                                                         | 6.54 ms: 1.50x faster                                                           |
| logging_simple             | 10.8 us                                                         | 7.32 us: 1.48x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 206 ms: 1.46x faster                                                            |
| async_tree_memoization_tg  | 378 ms                                                          | 259 ms: 1.46x faster                                                            |
| pprint_pformat             | 1.70 sec                                                        | 1.17 sec: 1.45x faster                                                          |
| pprint_safe_repr           | 819 ms                                                          | 566 ms: 1.45x faster                                                            |
| logging_format             | 11.5 us                                                         | 7.94 us: 1.44x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 287 ms: 1.42x faster                                                            |
| async_tree_io              | 754 ms                                                          | 531 ms: 1.42x faster                                                            |
| scimark_lu                 | 102 ms                                                          | 72.4 ms: 1.41x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 535 ms: 1.39x faster                                                            |
| go                         | 147 ms                                                          | 106 ms: 1.39x faster                                                            |
| sympy_sum                  | 149 ms                                                          | 108 ms: 1.38x faster                                                            |
| xml_etree_process          | 55.0 ms                                                         | 40.9 ms: 1.35x faster                                                           |
| sympy_str                  | 283 ms                                                          | 210 ms: 1.35x faster                                                            |
| chameleon                  | 8.08 ms                                                         | 6.01 ms: 1.34x faster                                                           |
| pycparser                  | 1.04 sec                                                        | 781 ms: 1.34x faster                                                            |
| deepcopy                   | 381 us                                                          | 294 us: 1.30x faster                                                            |
| xml_etree_generate         | 71.6 ms                                                         | 55.6 ms: 1.29x faster                                                           |
| sympy_integrate            | 19.9 ms                                                         | 15.5 ms: 1.28x faster                                                           |
| genshi_text                | 26.8 ms                                                         | 20.9 ms: 1.28x faster                                                           |
| mdp                        | 2.07 sec                                                        | 1.62 sec: 1.28x faster                                                          |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 452 ms: 1.28x faster                                                            |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 469 ms: 1.26x faster                                                            |
| asyncio_tcp                | 787 ms                                                          | 625 ms: 1.26x faster                                                            |
| sqlglot_optimize           | 51.8 ms                                                         | 41.4 ms: 1.25x faster                                                           |
| xml_etree_iterparse        | 75.6 ms                                                         | 60.4 ms: 1.25x faster                                                           |
| meteor_contest             | 90.9 ms                                                         | 73.0 ms: 1.25x faster                                                           |
| sympy_expand               | 462 ms                                                          | 375 ms: 1.23x faster                                                            |
| deepcopy_reduce            | 3.32 us                                                         | 2.70 us: 1.23x faster                                                           |
| genshi_xml                 | 61.2 ms                                                         | 50.0 ms: 1.23x faster                                                           |
| tornado_http               | 118 ms                                                          | 97.1 ms: 1.22x faster                                                           |
| django_template            | 37.4 ms                                                         | 30.8 ms: 1.22x faster                                                           |
| html5lib                   | 54.3 ms                                                         | 46.1 ms: 1.18x faster                                                           |
| json                       | 4.78 ms                                                         | 4.07 ms: 1.17x faster                                                           |
| unpickle_list              | 3.28 us                                                         | 2.80 us: 1.17x faster                                                           |
| sqlite_synth               | 2.15 us                                                         | 1.87 us: 1.15x faster                                                           |
| bench_thread_pool          | 1.14 ms                                                         | 989 us: 1.15x faster                                                            |
| 2to3                       | 282 ms                                                          | 246 ms: 1.15x faster                                                            |
| docutils                   | 2.10 sec                                                        | 1.88 sec: 1.12x faster                                                          |
| xml_etree_parse            | 114 ms                                                          | 103 ms: 1.11x faster                                                            |
| pidigits                   | 203 ms                                                          | 196 ms: 1.04x faster                                                            |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.8 sec: 1.02x faster                                                          |
| flaskblogging              | 2.03 sec                                                        | 2.04 sec: 1.00x slower                                                          |
| regex_dna                  | 122 ms                                                          | 123 ms: 1.01x slower                                                            |
| json_loads                 | 20.0 us                                                         | 20.5 us: 1.02x slower                                                           |
| pickle_dict                | 20.1 us                                                         | 20.8 us: 1.03x slower                                                           |
| pickle                     | 7.99 us                                                         | 8.32 us: 1.04x slower                                                           |
| gc_traversal               | 1.38 ms                                                         | 1.44 ms: 1.04x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 84.0 ms: 1.05x slower                                                           |
| regex_v8                   | 15.2 ms                                                         | 16.0 ms: 1.05x slower                                                           |
| telco                      | 5.29 ms                                                         | 5.63 ms: 1.06x slower                                                           |
| regex_effbot               | 1.82 ms                                                         | 1.95 ms: 1.07x slower                                                           |
| bench_mp_pool              | 70.9 ms                                                         | 76.7 ms: 1.08x slower                                                           |
| pickle_list                | 3.27 us                                                         | 3.58 us: 1.10x slower                                                           |
| python_startup_no_site     | 18.8 ms                                                         | 20.9 ms: 1.11x slower                                                           |
| python_startup             | 22.0 ms                                                         | 24.8 ms: 1.13x slower                                                           |
| unpickle                   | 9.23 us                                                         | 10.5 us: 1.13x slower                                                           |
| async_generators           | 260 ms                                                          | 295 ms: 1.13x slower                                                            |
| create_gc_cycles           | 618 us                                                          | 751 us: 1.22x slower                                                            |
| sqlglot_normalize          | 113 ms                                                          | 218 ms: 1.93x slower                                                            |
| coverage                   | 58.0 ms                                                         | 331 ms: 5.70x slower                                                            |
| thrift                     | 801 us                                                          | 10.2 ms: 12.73x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.28x faster                                                                    |
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.29x
- 95% likely to have a speedup of 1.28x
- 99% likely to have a speedup of 1.25x

# Memory
- memory change: unknown