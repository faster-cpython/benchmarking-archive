# Results vs. 3.11.0

- fork: python
- ref: d472b4f9fa4fb6061588
- machine: windows-x86
- commit hash: d472b4f
- commit date: 2024-05-22
- overall geometric mean: 1.33x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.26x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240522-pythonperf1_win32-x86-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 248 ms: 1.14x faster                                                           |
| chameleon      | 8.08 ms                                                         | 6.12 ms: 1.32x faster                                                          |
| docutils       | 2.10 sec                                                        | 1.87 sec: 1.12x faster                                                         |
| html5lib       | 54.3 ms                                                         | 45.0 ms: 1.21x faster                                                          |
| tornado_http   | 118 ms                                                          | 96.8 ms: 1.22x faster                                                          |
| Geometric mean | (ref)                                                           | 1.20x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240522-pythonperf1_win32-x86-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 228 ms: 1.51x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 206 ms: 1.46x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 280 ms: 1.46x faster                                                           |
| async_tree_memoization_tg  | 378 ms                                                          | 261 ms: 1.45x faster                                                           |
| async_tree_io              | 754 ms                                                          | 540 ms: 1.39x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 539 ms: 1.38x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 454 ms: 1.27x faster                                                           |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 472 ms: 1.25x faster                                                           |
| Geometric mean             | (ref)                                                           | 1.39x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240522-pythonperf1_win32-x86-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 52.1 ms: 2.42x faster                                                          |
| float          | 76.1 ms                                                         | 41.5 ms: 1.83x faster                                                          |
| pidigits       | 203 ms                                                          | 194 ms: 1.04x faster                                                           |
| Geometric mean | (ref)                                                           | 1.67x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240522-pythonperf1_win32-x86-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 96.8 ms: 1.52x faster                                                          |
| regex_dna      | 122 ms                                                          | 120 ms: 1.02x faster                                                           |
| regex_v8       | 15.2 ms                                                         | 16.0 ms: 1.05x slower                                                          |
| regex_effbot   | 1.82 ms                                                         | 1.94 ms: 1.06x slower                                                          |
| Geometric mean | (ref)                                                           | 1.08x faster                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240522-pythonperf1_win32-x86-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|----------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 138 us: 1.68x faster                                                           |
| tomli_loads          | 2.31 sec                                                        | 1.38 sec: 1.67x faster                                                         |
| pickle_pure_python   | 309 us                                                          | 196 us: 1.57x faster                                                           |
| json_dumps           | 9.80 ms                                                         | 6.74 ms: 1.45x faster                                                          |
| xml_etree_process    | 55.0 ms                                                         | 41.2 ms: 1.34x faster                                                          |
| xml_etree_generate   | 71.6 ms                                                         | 55.3 ms: 1.30x faster                                                          |
| xml_etree_iterparse  | 75.6 ms                                                         | 60.0 ms: 1.26x faster                                                          |
| xml_etree_parse      | 114 ms                                                          | 102 ms: 1.12x faster                                                           |
| unpickle_list        | 3.28 us                                                         | 3.06 us: 1.07x faster                                                          |
| pickle_dict          | 20.1 us                                                         | 20.7 us: 1.03x slower                                                          |
| json_loads           | 20.0 us                                                         | 21.0 us: 1.05x slower                                                          |
| pickle               | 7.99 us                                                         | 8.51 us: 1.07x slower                                                          |
| pickle_list          | 3.27 us                                                         | 3.53 us: 1.08x slower                                                          |
| unpickle             | 9.23 us                                                         | 10.2 us: 1.10x slower                                                          |
| Geometric mean       | (ref)                                                           | 1.20x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240522-pythonperf1_win32-x86-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 20.4 ms: 1.09x slower                                                          |
| python_startup         | 22.0 ms                                                         | 24.2 ms: 1.10x slower                                                          |
| Geometric mean         | (ref)                                                           | 1.09x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240522-pythonperf1_win32-x86-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|-----------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 5.25 ms: 1.96x faster                                                          |
| genshi_text     | 26.8 ms                                                         | 21.6 ms: 1.24x faster                                                          |
| django_template | 37.4 ms                                                         | 31.2 ms: 1.20x faster                                                          |
| genshi_xml      | 61.2 ms                                                         | 51.1 ms: 1.20x faster                                                          |
| Geometric mean  | (ref)                                                           | 1.37x faster                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240522-pythonperf1_win32-x86-python-d472b4f9fa4fb6061588-3.14.0a0-d472b4f |
|----------------------------|:---------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 147 us: 3.25x faster                                                           |
| spectral_norm              | 122 ms                                                          | 47.3 ms: 2.57x faster                                                          |
| nbody                      | 126 ms                                                          | 52.1 ms: 2.42x faster                                                          |
| generators                 | 52.2 ms                                                         | 23.6 ms: 2.21x faster                                                          |
| logging_silent             | 119 ns                                                          | 54.8 ns: 2.17x faster                                                          |
| comprehensions             | 22.1 us                                                         | 11.2 us: 1.96x faster                                                          |
| mako                       | 10.3 ms                                                         | 5.25 ms: 1.96x faster                                                          |
| deepcopy_memo              | 40.0 us                                                         | 20.5 us: 1.95x faster                                                          |
| float                      | 76.1 ms                                                         | 41.5 ms: 1.83x faster                                                          |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.34 ms: 1.81x faster                                                          |
| fannkuch                   | 399 ms                                                          | 224 ms: 1.79x faster                                                           |
| pylint                     | 418 ms                                                          | 239 ms: 1.75x faster                                                           |
| scimark_fft                | 291 ms                                                          | 171 ms: 1.70x faster                                                           |
| scimark_monte_carlo        | 70.8 ms                                                         | 41.6 ms: 1.70x faster                                                          |
| hexiom                     | 7.51 ms                                                         | 4.43 ms: 1.69x faster                                                          |
| unpickle_pure_python       | 231 us                                                          | 138 us: 1.68x faster                                                           |
| sqlglot_parse              | 1.49 ms                                                         | 891 us: 1.67x faster                                                           |
| tomli_loads                | 2.31 sec                                                        | 1.38 sec: 1.67x faster                                                         |
| richards_super             | 58.7 ms                                                         | 35.3 ms: 1.66x faster                                                          |
| crypto_pyaes               | 79.4 ms                                                         | 48.5 ms: 1.64x faster                                                          |
| chaos                      | 84.4 ms                                                         | 52.0 ms: 1.62x faster                                                          |
| pyflate                    | 471 ms                                                          | 292 ms: 1.61x faster                                                           |
| deltablue                  | 4.10 ms                                                         | 2.54 ms: 1.61x faster                                                          |
| richards                   | 48.8 ms                                                         | 30.9 ms: 1.58x faster                                                          |
| raytrace                   | 327 ms                                                          | 208 ms: 1.58x faster                                                           |
| pickle_pure_python         | 309 us                                                          | 196 us: 1.57x faster                                                           |
| nqueens                    | 111 ms                                                          | 71.0 ms: 1.57x faster                                                          |
| sqlglot_transpile          | 1.78 ms                                                         | 1.15 ms: 1.55x faster                                                          |
| regex_compile              | 148 ms                                                          | 96.8 ms: 1.52x faster                                                          |
| scimark_sor                | 135 ms                                                          | 89.5 ms: 1.51x faster                                                          |
| async_tree_none            | 343 ms                                                          | 228 ms: 1.51x faster                                                           |
| pprint_pformat             | 1.70 sec                                                        | 1.14 sec: 1.49x faster                                                         |
| pprint_safe_repr           | 819 ms                                                          | 551 ms: 1.49x faster                                                           |
| async_tree_none_tg         | 301 ms                                                          | 206 ms: 1.46x faster                                                           |
| async_tree_memoization     | 408 ms                                                          | 280 ms: 1.46x faster                                                           |
| json_dumps                 | 9.80 ms                                                         | 6.74 ms: 1.45x faster                                                          |
| logging_simple             | 10.8 us                                                         | 7.44 us: 1.45x faster                                                          |
| scimark_lu                 | 102 ms                                                          | 70.5 ms: 1.45x faster                                                          |
| async_tree_memoization_tg  | 378 ms                                                          | 261 ms: 1.45x faster                                                           |
| coroutines                 | 23.7 ms                                                         | 16.5 ms: 1.44x faster                                                          |
| logging_format             | 11.5 us                                                         | 8.09 us: 1.42x faster                                                          |
| sympy_sum                  | 149 ms                                                          | 105 ms: 1.42x faster                                                           |
| async_tree_io              | 754 ms                                                          | 540 ms: 1.39x faster                                                           |
| async_tree_io_tg           | 746 ms                                                          | 539 ms: 1.38x faster                                                           |
| sympy_str                  | 283 ms                                                          | 209 ms: 1.36x faster                                                           |
| xml_etree_process          | 55.0 ms                                                         | 41.2 ms: 1.34x faster                                                          |
| go                         | 147 ms                                                          | 111 ms: 1.32x faster                                                           |
| chameleon                  | 8.08 ms                                                         | 6.12 ms: 1.32x faster                                                          |
| pycparser                  | 1.04 sec                                                        | 794 ms: 1.31x faster                                                           |
| asyncio_tcp                | 787 ms                                                          | 599 ms: 1.31x faster                                                           |
| xml_etree_generate         | 71.6 ms                                                         | 55.3 ms: 1.30x faster                                                          |
| mdp                        | 2.07 sec                                                        | 1.60 sec: 1.29x faster                                                         |
| sympy_integrate            | 19.9 ms                                                         | 15.5 ms: 1.29x faster                                                          |
| deepcopy                   | 381 us                                                          | 298 us: 1.28x faster                                                           |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 454 ms: 1.27x faster                                                           |
| xml_etree_iterparse        | 75.6 ms                                                         | 60.0 ms: 1.26x faster                                                          |
| meteor_contest             | 90.9 ms                                                         | 72.2 ms: 1.26x faster                                                          |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 472 ms: 1.25x faster                                                           |
| genshi_text                | 26.8 ms                                                         | 21.6 ms: 1.24x faster                                                          |
| sqlglot_optimize           | 51.8 ms                                                         | 42.0 ms: 1.23x faster                                                          |
| sympy_expand               | 462 ms                                                          | 374 ms: 1.23x faster                                                           |
| deepcopy_reduce            | 3.32 us                                                         | 2.69 us: 1.23x faster                                                          |
| tornado_http               | 118 ms                                                          | 96.8 ms: 1.22x faster                                                          |
| html5lib                   | 54.3 ms                                                         | 45.0 ms: 1.21x faster                                                          |
| django_template            | 37.4 ms                                                         | 31.2 ms: 1.20x faster                                                          |
| genshi_xml                 | 61.2 ms                                                         | 51.1 ms: 1.20x faster                                                          |
| coverage                   | 58.0 ms                                                         | 50.2 ms: 1.16x faster                                                          |
| bench_thread_pool          | 1.14 ms                                                         | 987 us: 1.15x faster                                                           |
| sqlite_synth               | 2.15 us                                                         | 1.88 us: 1.14x faster                                                          |
| 2to3                       | 282 ms                                                          | 248 ms: 1.14x faster                                                           |
| thrift                     | 801 us                                                          | 705 us: 1.14x faster                                                           |
| docutils                   | 2.10 sec                                                        | 1.87 sec: 1.12x faster                                                         |
| xml_etree_parse            | 114 ms                                                          | 102 ms: 1.12x faster                                                           |
| json                       | 4.78 ms                                                         | 4.37 ms: 1.09x faster                                                          |
| unpickle_list              | 3.28 us                                                         | 3.06 us: 1.07x faster                                                          |
| pidigits                   | 203 ms                                                          | 194 ms: 1.04x faster                                                           |
| regex_dna                  | 122 ms                                                          | 120 ms: 1.02x faster                                                           |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.9 sec: 1.01x faster                                                         |
| telco                      | 5.29 ms                                                         | 5.45 ms: 1.03x slower                                                          |
| pickle_dict                | 20.1 us                                                         | 20.7 us: 1.03x slower                                                          |
| json_loads                 | 20.0 us                                                         | 21.0 us: 1.05x slower                                                          |
| regex_v8                   | 15.2 ms                                                         | 16.0 ms: 1.05x slower                                                          |
| bench_mp_pool              | 70.9 ms                                                         | 74.9 ms: 1.06x slower                                                          |
| regex_effbot               | 1.82 ms                                                         | 1.94 ms: 1.06x slower                                                          |
| gc_traversal               | 1.38 ms                                                         | 1.47 ms: 1.07x slower                                                          |
| pickle                     | 7.99 us                                                         | 8.51 us: 1.07x slower                                                          |
| pathlib                    | 79.9 ms                                                         | 85.8 ms: 1.07x slower                                                          |
| pickle_list                | 3.27 us                                                         | 3.53 us: 1.08x slower                                                          |
| python_startup_no_site     | 18.8 ms                                                         | 20.4 ms: 1.09x slower                                                          |
| python_startup             | 22.0 ms                                                         | 24.2 ms: 1.10x slower                                                          |
| unpickle                   | 9.23 us                                                         | 10.2 us: 1.10x slower                                                          |
| async_generators           | 260 ms                                                          | 292 ms: 1.12x slower                                                           |
| create_gc_cycles           | 618 us                                                          | 749 us: 1.21x slower                                                           |
| sqlglot_normalize          | 113 ms                                                          | 220 ms: 1.95x slower                                                           |
| Geometric mean             | (ref)                                                           | 1.33x faster                                                                   |

Benchmark hidden because not significant (1): flaskblogging
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.30x
- 95% likely to have a speedup of 1.29x
- 99% likely to have a speedup of 1.26x

# Memory
- memory change: unknown