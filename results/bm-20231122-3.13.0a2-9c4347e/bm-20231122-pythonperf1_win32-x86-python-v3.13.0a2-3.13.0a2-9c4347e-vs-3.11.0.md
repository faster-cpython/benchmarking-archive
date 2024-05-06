# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a2
- machine: windows-x86
- commit hash: 9c4347e
- commit date: 2023-11-22
- overall geometric mean: 1.19x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20231122-pythonperf1_win32-x86-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 246 ms: 1.15x faster                                                |
| chameleon      | 8.08 ms                                                         | 5.96 ms: 1.36x faster                                               |
| docutils       | 2.10 sec                                                        | 1.78 sec: 1.18x faster                                              |
| html5lib       | 54.3 ms                                                         | 45.7 ms: 1.19x faster                                               |
| tornado_http   | 118 ms                                                          | 98.2 ms: 1.21x faster                                               |
| Geometric mean | (ref)                                                           | 1.21x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20231122-pythonperf1_win32-x86-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 254 ms: 1.35x faster                                                |
| async_tree_memoization     | 408 ms                                                          | 317 ms: 1.29x faster                                                |
| async_tree_none_tg         | 301 ms                                                          | 248 ms: 1.21x faster                                                |
| async_tree_io              | 754 ms                                                          | 623 ms: 1.21x faster                                                |
| async_tree_memoization_tg  | 378 ms                                                          | 312 ms: 1.21x faster                                                |
| async_tree_io_tg           | 746 ms                                                          | 619 ms: 1.21x faster                                                |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 511 ms: 1.16x faster                                                |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 506 ms: 1.14x faster                                                |
| Geometric mean             | (ref)                                                           | 1.22x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20231122-pythonperf1_win32-x86-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 88.9 ms: 1.42x faster                                               |
| float          | 76.1 ms                                                         | 59.8 ms: 1.27x faster                                               |
| pidigits       | 203 ms                                                          | 200 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                           | 1.22x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20231122-pythonperf1_win32-x86-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 106 ms: 1.40x faster                                                |
| regex_dna      | 122 ms                                                          | 120 ms: 1.01x faster                                                |
| regex_effbot   | 1.82 ms                                                         | 1.92 ms: 1.05x slower                                               |
| regex_v8       | 15.2 ms                                                         | 16.2 ms: 1.07x slower                                               |
| Geometric mean | (ref)                                                           | 1.06x faster                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20231122-pythonperf1_win32-x86-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 156 us: 1.48x faster                                                |
| json_dumps           | 9.80 ms                                                         | 6.96 ms: 1.41x faster                                               |
| pickle_pure_python   | 309 us                                                          | 231 us: 1.34x faster                                                |
| tomli_loads          | 2.31 sec                                                        | 1.81 sec: 1.28x faster                                              |
| xml_etree_process    | 55.0 ms                                                         | 45.8 ms: 1.20x faster                                               |
| xml_etree_generate   | 71.6 ms                                                         | 62.8 ms: 1.14x faster                                               |
| unpickle_list        | 3.28 us                                                         | 2.94 us: 1.11x faster                                               |
| xml_etree_iterparse  | 75.6 ms                                                         | 69.5 ms: 1.09x faster                                               |
| xml_etree_parse      | 114 ms                                                          | 108 ms: 1.06x faster                                                |
| pickle               | 7.99 us                                                         | 7.57 us: 1.06x faster                                               |
| pickle_list          | 3.27 us                                                         | 3.17 us: 1.03x faster                                               |
| json_loads           | 20.0 us                                                         | 19.8 us: 1.01x faster                                               |
| pickle_dict          | 20.1 us                                                         | 19.8 us: 1.01x faster                                               |
| unpickle             | 9.23 us                                                         | 9.58 us: 1.04x slower                                               |
| Geometric mean       | (ref)                                                           | 1.15x faster                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20231122-pythonperf1_win32-x86-python-v3.13.0a2-3.13.0a2-9c4347e |
|------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                         | 22.2 ms: 1.01x slower                                               |
| python_startup_no_site | 18.8 ms                                                         | 20.0 ms: 1.06x slower                                               |
| Geometric mean         | (ref)                                                           | 1.04x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20231122-pythonperf1_win32-x86-python-v3.13.0a2-3.13.0a2-9c4347e |
|-----------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 7.72 ms: 1.33x faster                                               |
| genshi_xml      | 61.2 ms                                                         | 48.4 ms: 1.27x faster                                               |
| genshi_text     | 26.8 ms                                                         | 21.7 ms: 1.23x faster                                               |
| django_template | 37.4 ms                                                         | 31.2 ms: 1.20x faster                                               |
| Geometric mean  | (ref)                                                           | 1.26x faster                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20231122-pythonperf1_win32-x86-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------------------|:---------------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 98.7 us: 4.85x faster                                               |
| generators                 | 52.2 ms                                                         | 27.0 ms: 1.94x faster                                               |
| pylint                     | 418 ms                                                          | 226 ms: 1.85x faster                                                |
| comprehensions             | 22.1 us                                                         | 12.6 us: 1.76x faster                                               |
| logging_silent             | 119 ns                                                          | 70.3 ns: 1.70x faster                                               |
| chaos                      | 84.4 ms                                                         | 51.8 ms: 1.63x faster                                               |
| spectral_norm              | 122 ms                                                          | 75.0 ms: 1.62x faster                                               |
| deltablue                  | 4.10 ms                                                         | 2.55 ms: 1.61x faster                                               |
| sqlglot_parse              | 1.49 ms                                                         | 953 us: 1.56x faster                                                |
| richards_super             | 58.7 ms                                                         | 38.0 ms: 1.54x faster                                               |
| hexiom                     | 7.51 ms                                                         | 4.97 ms: 1.51x faster                                               |
| deepcopy_memo              | 40.0 us                                                         | 26.6 us: 1.50x faster                                               |
| scimark_lu                 | 102 ms                                                          | 69.0 ms: 1.48x faster                                               |
| unpickle_pure_python       | 231 us                                                          | 156 us: 1.48x faster                                                |
| sqlglot_transpile          | 1.78 ms                                                         | 1.21 ms: 1.48x faster                                               |
| raytrace                   | 327 ms                                                          | 223 ms: 1.47x faster                                                |
| richards                   | 48.8 ms                                                         | 33.7 ms: 1.45x faster                                               |
| sympy_sum                  | 149 ms                                                          | 104 ms: 1.44x faster                                                |
| crypto_pyaes               | 79.4 ms                                                         | 55.4 ms: 1.43x faster                                               |
| coroutines                 | 23.7 ms                                                         | 16.7 ms: 1.42x faster                                               |
| nbody                      | 126 ms                                                          | 88.9 ms: 1.42x faster                                               |
| json_dumps                 | 9.80 ms                                                         | 6.96 ms: 1.41x faster                                               |
| pyflate                    | 471 ms                                                          | 335 ms: 1.40x faster                                                |
| scimark_monte_carlo        | 70.8 ms                                                         | 50.6 ms: 1.40x faster                                               |
| regex_compile              | 148 ms                                                          | 106 ms: 1.40x faster                                                |
| nqueens                    | 111 ms                                                          | 80.1 ms: 1.39x faster                                               |
| scimark_sor                | 135 ms                                                          | 97.7 ms: 1.38x faster                                               |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.07 ms: 1.38x faster                                               |
| go                         | 147 ms                                                          | 108 ms: 1.37x faster                                                |
| sympy_str                  | 283 ms                                                          | 207 ms: 1.37x faster                                                |
| chameleon                  | 8.08 ms                                                         | 5.96 ms: 1.36x faster                                               |
| async_tree_none            | 343 ms                                                          | 254 ms: 1.35x faster                                                |
| pickle_pure_python         | 309 us                                                          | 231 us: 1.34x faster                                                |
| sympy_integrate            | 19.9 ms                                                         | 14.9 ms: 1.34x faster                                               |
| mako                       | 10.3 ms                                                         | 7.72 ms: 1.33x faster                                               |
| pprint_pformat             | 1.70 sec                                                        | 1.28 sec: 1.33x faster                                              |
| scimark_fft                | 291 ms                                                          | 220 ms: 1.33x faster                                                |
| fannkuch                   | 399 ms                                                          | 302 ms: 1.32x faster                                                |
| pprint_safe_repr           | 819 ms                                                          | 621 ms: 1.32x faster                                                |
| logging_simple             | 10.8 us                                                         | 8.35 us: 1.29x faster                                               |
| deepcopy                   | 381 us                                                          | 295 us: 1.29x faster                                                |
| async_tree_memoization     | 408 ms                                                          | 317 ms: 1.29x faster                                                |
| logging_format             | 11.5 us                                                         | 8.90 us: 1.29x faster                                               |
| tomli_loads                | 2.31 sec                                                        | 1.81 sec: 1.28x faster                                              |
| sympy_expand               | 462 ms                                                          | 362 ms: 1.28x faster                                                |
| float                      | 76.1 ms                                                         | 59.8 ms: 1.27x faster                                               |
| genshi_xml                 | 61.2 ms                                                         | 48.4 ms: 1.27x faster                                               |
| deepcopy_reduce            | 3.32 us                                                         | 2.63 us: 1.26x faster                                               |
| sqlglot_optimize           | 51.8 ms                                                         | 41.5 ms: 1.25x faster                                               |
| genshi_text                | 26.8 ms                                                         | 21.7 ms: 1.23x faster                                               |
| mdp                        | 2.07 sec                                                        | 1.70 sec: 1.21x faster                                              |
| async_tree_none_tg         | 301 ms                                                          | 248 ms: 1.21x faster                                                |
| pycparser                  | 1.04 sec                                                        | 862 ms: 1.21x faster                                                |
| async_tree_io              | 754 ms                                                          | 623 ms: 1.21x faster                                                |
| async_tree_memoization_tg  | 378 ms                                                          | 312 ms: 1.21x faster                                                |
| tornado_http               | 118 ms                                                          | 98.2 ms: 1.21x faster                                               |
| async_tree_io_tg           | 746 ms                                                          | 619 ms: 1.21x faster                                                |
| asyncio_tcp                | 787 ms                                                          | 654 ms: 1.20x faster                                                |
| django_template            | 37.4 ms                                                         | 31.2 ms: 1.20x faster                                               |
| xml_etree_process          | 55.0 ms                                                         | 45.8 ms: 1.20x faster                                               |
| html5lib                   | 54.3 ms                                                         | 45.7 ms: 1.19x faster                                               |
| docutils                   | 2.10 sec                                                        | 1.78 sec: 1.18x faster                                              |
| sqlite_synth               | 2.15 us                                                         | 1.84 us: 1.17x faster                                               |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 511 ms: 1.16x faster                                                |
| json                       | 4.78 ms                                                         | 4.14 ms: 1.15x faster                                               |
| 2to3                       | 282 ms                                                          | 246 ms: 1.15x faster                                                |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 506 ms: 1.14x faster                                                |
| xml_etree_generate         | 71.6 ms                                                         | 62.8 ms: 1.14x faster                                               |
| meteor_contest             | 90.9 ms                                                         | 80.4 ms: 1.13x faster                                               |
| unpickle_list              | 3.28 us                                                         | 2.94 us: 1.11x faster                                               |
| bench_thread_pool          | 1.14 ms                                                         | 1.05 ms: 1.09x faster                                               |
| xml_etree_iterparse        | 75.6 ms                                                         | 69.5 ms: 1.09x faster                                               |
| xml_etree_parse            | 114 ms                                                          | 108 ms: 1.06x faster                                                |
| pickle                     | 7.99 us                                                         | 7.57 us: 1.06x faster                                               |
| pickle_list                | 3.27 us                                                         | 3.17 us: 1.03x faster                                               |
| bench_mp_pool              | 70.9 ms                                                         | 69.3 ms: 1.02x faster                                               |
| pidigits                   | 203 ms                                                          | 200 ms: 1.01x faster                                                |
| json_loads                 | 20.0 us                                                         | 19.8 us: 1.01x faster                                               |
| pickle_dict                | 20.1 us                                                         | 19.8 us: 1.01x faster                                               |
| regex_dna                  | 122 ms                                                          | 120 ms: 1.01x faster                                                |
| gc_traversal               | 1.38 ms                                                         | 1.39 ms: 1.01x slower                                               |
| python_startup             | 22.0 ms                                                         | 22.2 ms: 1.01x slower                                               |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 17.2 sec: 1.01x slower                                              |
| unpickle                   | 9.23 us                                                         | 9.58 us: 1.04x slower                                               |
| create_gc_cycles           | 618 us                                                          | 645 us: 1.04x slower                                                |
| regex_effbot               | 1.82 ms                                                         | 1.92 ms: 1.05x slower                                               |
| python_startup_no_site     | 18.8 ms                                                         | 20.0 ms: 1.06x slower                                               |
| async_generators           | 260 ms                                                          | 278 ms: 1.07x slower                                                |
| regex_v8                   | 15.2 ms                                                         | 16.2 ms: 1.07x slower                                               |
| pathlib                    | 79.9 ms                                                         | 89.7 ms: 1.12x slower                                               |
| telco                      | 5.29 ms                                                         | 6.08 ms: 1.15x slower                                               |
| sqlglot_normalize          | 113 ms                                                          | 212 ms: 1.87x slower                                                |
| coverage                   | 58.0 ms                                                         | 512 ms: 8.83x slower                                                |
| thrift                     | 801 us                                                          | 10.7 ms: 13.35x slower                                              |
| Geometric mean             | (ref)                                                           | 1.19x faster                                                        |

Benchmark hidden because not significant (1): flaskblogging
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.21x
- 95% likely to have a speedup of 1.21x
- 99% likely to have a speedup of 1.20x

# Memory
- memory change: unknown