# Results vs. 3.11.0

- fork: python
- ref: 5b941e57c71d7d0ab983
- machine: windows-x86
- commit hash: 5b941e5
- commit date: 2024-05-11
- overall geometric mean: 1.33x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 249 ms: 1.14x faster                                                           |
| chameleon      | 8.08 ms                                                         | 6.16 ms: 1.31x faster                                                          |
| docutils       | 2.10 sec                                                        | 1.88 sec: 1.12x faster                                                         |
| html5lib       | 54.3 ms                                                         | 45.5 ms: 1.19x faster                                                          |
| tornado_http   | 118 ms                                                          | 97.0 ms: 1.22x faster                                                          |
| Geometric mean | (ref)                                                           | 1.19x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 228 ms: 1.51x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 278 ms: 1.47x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 205 ms: 1.46x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 260 ms: 1.45x faster                                                           |
| async_tree_io              | 754 ms                                                          | 534 ms: 1.41x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 533 ms: 1.40x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 463 ms: 1.25x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 479 ms: 1.23x faster                                                           |
| Geometric mean             | (ref)                                                           | 1.39x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 55.2 ms: 2.28x faster                                                          |
| float          | 76.1 ms                                                         | 41.1 ms: 1.85x faster                                                          |
| pidigits       | 203 ms                                                          | 197 ms: 1.03x faster                                                           |
| Geometric mean | (ref)                                                           | 1.63x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 92.2 ms: 1.60x faster                                                          |
| regex_dna      | 122 ms                                                          | 118 ms: 1.03x faster                                                           |
| regex_v8       | 15.2 ms                                                         | 15.6 ms: 1.03x slower                                                          |
| regex_effbot   | 1.82 ms                                                         | 1.99 ms: 1.09x slower                                                          |
| Geometric mean | (ref)                                                           | 1.10x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 137 us: 1.69x faster                                                           |
| tomli_loads          | 2.31 sec                                                        | 1.39 sec: 1.66x faster                                                         |
| pickle_pure_python   | 309 us                                                          | 202 us: 1.53x faster                                                           |
| json_dumps           | 9.80 ms                                                         | 6.53 ms: 1.50x faster                                                          |
| xml_etree_process    | 55.0 ms                                                         | 40.2 ms: 1.37x faster                                                          |
| xml_etree_generate   | 71.6 ms                                                         | 55.3 ms: 1.30x faster                                                          |
| xml_etree_iterparse  | 75.6 ms                                                         | 61.8 ms: 1.22x faster                                                          |
| unpickle_list        | 3.28 us                                                         | 2.73 us: 1.20x faster                                                          |
| xml_etree_parse      | 114 ms                                                          | 105 ms: 1.09x faster                                                           |
| pickle               | 7.99 us                                                         | 8.19 us: 1.03x slower                                                          |
| pickle_dict          | 20.1 us                                                         | 20.7 us: 1.03x slower                                                          |
| json_loads           | 20.0 us                                                         | 21.0 us: 1.05x slower                                                          |
| pickle_list          | 3.27 us                                                         | 3.54 us: 1.08x slower                                                          |
| unpickle             | 9.23 us                                                         | 10.4 us: 1.13x slower                                                          |
| Geometric mean       | (ref)                                                           | 1.20x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 20.5 ms: 1.09x slower                                                          |
| python_startup         | 22.0 ms                                                         | 24.4 ms: 1.11x slower                                                          |
| Geometric mean         | (ref)                                                           | 1.10x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|-----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 5.31 ms: 1.94x faster                                                          |
| genshi_text     | 26.8 ms                                                         | 22.2 ms: 1.20x faster                                                          |
| genshi_xml      | 61.2 ms                                                         | 52.3 ms: 1.17x faster                                                          |
| django_template | 37.4 ms                                                         | 32.0 ms: 1.17x faster                                                          |
| Geometric mean  | (ref)                                                           | 1.34x faster                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240511-pythonperf1_win32-x86-python-5b941e57c71d7d0ab983-3.14.0a0-5b941e5 |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 140 us: 3.41x faster                                                           |
| spectral_norm              | 122 ms                                                          | 47.2 ms: 2.58x faster                                                          |
| nbody                      | 126 ms                                                          | 55.2 ms: 2.28x faster                                                          |
| generators                 | 52.2 ms                                                         | 23.2 ms: 2.25x faster                                                          |
| logging_silent             | 119 ns                                                          | 54.7 ns: 2.18x faster                                                          |
| comprehensions             | 22.1 us                                                         | 10.8 us: 2.05x faster                                                          |
| mako                       | 10.3 ms                                                         | 5.31 ms: 1.94x faster                                                          |
| deepcopy_memo              | 40.0 us                                                         | 20.8 us: 1.93x faster                                                          |
| float                      | 76.1 ms                                                         | 41.1 ms: 1.85x faster                                                          |
| fannkuch                   | 399 ms                                                          | 220 ms: 1.82x faster                                                           |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.34 ms: 1.81x faster                                                          |
| pylint                     | 418 ms                                                          | 240 ms: 1.74x faster                                                           |
| scimark_fft                | 291 ms                                                          | 168 ms: 1.73x faster                                                           |
| scimark_monte_carlo        | 70.8 ms                                                         | 41.2 ms: 1.72x faster                                                          |
| unpickle_pure_python       | 231 us                                                          | 137 us: 1.69x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.39 sec: 1.66x faster                                                         |
| crypto_pyaes               | 79.4 ms                                                         | 47.9 ms: 1.66x faster                                                          |
| hexiom                     | 7.51 ms                                                         | 4.53 ms: 1.66x faster                                                          |
| sqlglot_parse              | 1.49 ms                                                         | 903 us: 1.65x faster                                                           |
| richards_super             | 58.7 ms                                                         | 35.7 ms: 1.64x faster                                                          |
| chaos                      | 84.4 ms                                                         | 51.5 ms: 1.64x faster                                                          |
| deltablue                  | 4.10 ms                                                         | 2.53 ms: 1.62x faster                                                          |
| nqueens                    | 111 ms                                                          | 69.2 ms: 1.61x faster                                                          |
| regex_compile              | 148 ms                                                          | 92.2 ms: 1.60x faster                                                          |
| raytrace                   | 327 ms                                                          | 208 ms: 1.57x faster                                                           |
| richards                   | 48.8 ms                                                         | 31.3 ms: 1.56x faster                                                          |
| pyflate                    | 471 ms                                                          | 306 ms: 1.54x faster                                                           |
| sqlglot_transpile          | 1.78 ms                                                         | 1.16 ms: 1.53x faster                                                          |
| pickle_pure_python         | 309 us                                                          | 202 us: 1.53x faster                                                           |
| scimark_sor                | 135 ms                                                          | 89.6 ms: 1.51x faster                                                          |
| async_tree_none            | 343 ms                                                          | 228 ms: 1.51x faster                                                           |
| json_dumps                 | 9.80 ms                                                         | 6.53 ms: 1.50x faster                                                          |
| async_tree_memoization     | 408 ms                                                          | 278 ms: 1.47x faster                                                           |
| logging_simple             | 10.8 us                                                         | 7.37 us: 1.47x faster                                                          |
| async_tree_none_tg         | 301 ms                                                          | 205 ms: 1.46x faster                                                           |
| pprint_safe_repr           | 819 ms                                                          | 560 ms: 1.46x faster                                                           |
| pprint_pformat             | 1.70 sec                                                        | 1.16 sec: 1.46x faster                                                         |
| async_tree_memoization_tg  | 378 ms                                                          | 260 ms: 1.45x faster                                                           |
| coroutines                 | 23.7 ms                                                         | 16.5 ms: 1.44x faster                                                          |
| logging_format             | 11.5 us                                                         | 8.03 us: 1.43x faster                                                          |
| async_tree_io              | 754 ms                                                          | 534 ms: 1.41x faster                                                           |
| sympy_sum                  | 149 ms                                                          | 106 ms: 1.40x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 533 ms: 1.40x faster                                                           |
| go                         | 147 ms                                                          | 106 ms: 1.39x faster                                                           |
| xml_etree_process          | 55.0 ms                                                         | 40.2 ms: 1.37x faster                                                          |
| sympy_str                  | 283 ms                                                          | 208 ms: 1.36x faster                                                           |
| scimark_lu                 | 102 ms                                                          | 76.0 ms: 1.35x faster                                                          |
| pycparser                  | 1.04 sec                                                        | 781 ms: 1.34x faster                                                           |
| chameleon                  | 8.08 ms                                                         | 6.16 ms: 1.31x faster                                                          |
| xml_etree_generate         | 71.6 ms                                                         | 55.3 ms: 1.30x faster                                                          |
| sympy_integrate            | 19.9 ms                                                         | 15.5 ms: 1.29x faster                                                          |
| mdp                        | 2.07 sec                                                        | 1.63 sec: 1.27x faster                                                         |
| deepcopy                   | 381 us                                                          | 302 us: 1.26x faster                                                           |
| sympy_expand               | 462 ms                                                          | 369 ms: 1.25x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 463 ms: 1.25x faster                                                           |
| sqlglot_optimize           | 51.8 ms                                                         | 41.7 ms: 1.24x faster                                                          |
| deepcopy_reduce            | 3.32 us                                                         | 2.67 us: 1.24x faster                                                          |
| meteor_contest             | 90.9 ms                                                         | 73.3 ms: 1.24x faster                                                          |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 479 ms: 1.23x faster                                                           |
| xml_etree_iterparse        | 75.6 ms                                                         | 61.8 ms: 1.22x faster                                                          |
| tornado_http               | 118 ms                                                          | 97.0 ms: 1.22x faster                                                          |
| genshi_text                | 26.8 ms                                                         | 22.2 ms: 1.20x faster                                                          |
| unpickle_list              | 3.28 us                                                         | 2.73 us: 1.20x faster                                                          |
| html5lib                   | 54.3 ms                                                         | 45.5 ms: 1.19x faster                                                          |
| genshi_xml                 | 61.2 ms                                                         | 52.3 ms: 1.17x faster                                                          |
| django_template            | 37.4 ms                                                         | 32.0 ms: 1.17x faster                                                          |
| bench_thread_pool          | 1.14 ms                                                         | 991 us: 1.15x faster                                                           |
| sqlite_synth               | 2.15 us                                                         | 1.88 us: 1.14x faster                                                          |
| 2to3                       | 282 ms                                                          | 249 ms: 1.14x faster                                                           |
| coverage                   | 58.0 ms                                                         | 51.2 ms: 1.13x faster                                                          |
| docutils                   | 2.10 sec                                                        | 1.88 sec: 1.12x faster                                                         |
| asyncio_tcp                | 787 ms                                                          | 711 ms: 1.11x faster                                                           |
| json                       | 4.78 ms                                                         | 4.34 ms: 1.10x faster                                                          |
| xml_etree_parse            | 114 ms                                                          | 105 ms: 1.09x faster                                                           |
| thrift                     | 801 us                                                          | 734 us: 1.09x faster                                                           |
| regex_dna                  | 122 ms                                                          | 118 ms: 1.03x faster                                                           |
| pidigits                   | 203 ms                                                          | 197 ms: 1.03x faster                                                           |
| pickle                     | 7.99 us                                                         | 8.19 us: 1.03x slower                                                          |
| pickle_dict                | 20.1 us                                                         | 20.7 us: 1.03x slower                                                          |
| regex_v8                   | 15.2 ms                                                         | 15.6 ms: 1.03x slower                                                          |
| gc_traversal               | 1.38 ms                                                         | 1.44 ms: 1.05x slower                                                          |
| json_loads                 | 20.0 us                                                         | 21.0 us: 1.05x slower                                                          |
| bench_mp_pool              | 70.9 ms                                                         | 75.1 ms: 1.06x slower                                                          |
| telco                      | 5.29 ms                                                         | 5.72 ms: 1.08x slower                                                          |
| pickle_list                | 3.27 us                                                         | 3.54 us: 1.08x slower                                                          |
| regex_effbot               | 1.82 ms                                                         | 1.99 ms: 1.09x slower                                                          |
| python_startup_no_site     | 18.8 ms                                                         | 20.5 ms: 1.09x slower                                                          |
| async_generators           | 260 ms                                                          | 285 ms: 1.10x slower                                                           |
| pathlib                    | 79.9 ms                                                         | 87.9 ms: 1.10x slower                                                          |
| python_startup             | 22.0 ms                                                         | 24.4 ms: 1.11x slower                                                          |
| unpickle                   | 9.23 us                                                         | 10.4 us: 1.13x slower                                                          |
| create_gc_cycles           | 618 us                                                          | 751 us: 1.22x slower                                                           |
| sqlglot_normalize          | 113 ms                                                          | 220 ms: 1.95x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.33x faster                                                                   |

Benchmark hidden because not significant (2): asyncio_tcp_ssl, flaskblogging
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.28x
- 95% likely to have a speedup of 1.27x
- 99% likely to have a speedup of 1.24x

# Memory
- memory change: unknown