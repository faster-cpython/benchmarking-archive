# Results vs. 3.11.0

- fork: brandtbucher
- ref: no_cold_exits
- machine: windows-x86
- commit hash: f837cc6
- commit date: 2024-06-10
- overall geometric mean: 1.35x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf1_win32-x86-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 244 ms: 1.16x faster                                                          |
| docutils       | 2.10 sec                                                        | 1.87 sec: 1.12x faster                                                        |
| html5lib       | 54.3 ms                                                         | 45.9 ms: 1.18x faster                                                         |
| tornado_http   | 118 ms                                                          | 97.0 ms: 1.22x faster                                                         |
| Geometric mean | (ref)                                                           | 1.17x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf1_win32-x86-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 228 ms: 1.50x faster                                                          |
| async_tree_memoization     | 408 ms                                                          | 278 ms: 1.47x faster                                                          |
| async_tree_none_tg         | 301 ms                                                          | 206 ms: 1.46x faster                                                          |
| async_tree_memoization_tg  | 378 ms                                                          | 261 ms: 1.45x faster                                                          |
| async_tree_io              | 754 ms                                                          | 527 ms: 1.43x faster                                                          |
| async_tree_io_tg           | 746 ms                                                          | 533 ms: 1.40x faster                                                          |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 464 ms: 1.24x faster                                                          |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 479 ms: 1.23x faster                                                          |
| Geometric mean             | (ref)                                                           | 1.39x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf1_win32-x86-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 52.6 ms: 2.40x faster                                                         |
| float          | 76.1 ms                                                         | 41.6 ms: 1.83x faster                                                         |
| pidigits       | 203 ms                                                          | 195 ms: 1.04x faster                                                          |
| Geometric mean | (ref)                                                           | 1.66x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf1_win32-x86-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 96.3 ms: 1.53x faster                                                         |
| regex_dna      | 122 ms                                                          | 124 ms: 1.02x slower                                                          |
| regex_v8       | 15.2 ms                                                         | 15.9 ms: 1.05x slower                                                         |
| regex_effbot   | 1.82 ms                                                         | 1.99 ms: 1.09x slower                                                         |
| Geometric mean | (ref)                                                           | 1.07x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf1_win32-x86-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 135 us: 1.72x faster                                                          |
| tomli_loads          | 2.31 sec                                                        | 1.39 sec: 1.66x faster                                                        |
| pickle_pure_python   | 309 us                                                          | 201 us: 1.54x faster                                                          |
| json_dumps           | 9.80 ms                                                         | 6.66 ms: 1.47x faster                                                         |
| xml_etree_process    | 55.0 ms                                                         | 40.2 ms: 1.37x faster                                                         |
| xml_etree_generate   | 71.6 ms                                                         | 54.5 ms: 1.32x faster                                                         |
| xml_etree_iterparse  | 75.6 ms                                                         | 61.1 ms: 1.24x faster                                                         |
| unpickle_list        | 3.28 us                                                         | 2.76 us: 1.19x faster                                                         |
| xml_etree_parse      | 114 ms                                                          | 99.5 ms: 1.15x faster                                                         |
| pickle               | 7.99 us                                                         | 8.24 us: 1.03x slower                                                         |
| json_loads           | 20.0 us                                                         | 20.7 us: 1.03x slower                                                         |
| pickle_dict          | 20.1 us                                                         | 20.9 us: 1.04x slower                                                         |
| pickle_list          | 3.27 us                                                         | 3.58 us: 1.10x slower                                                         |
| unpickle             | 9.23 us                                                         | 10.3 us: 1.11x slower                                                         |
| Geometric mean       | (ref)                                                           | 1.21x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf1_win32-x86-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 18.5 ms: 1.02x faster                                                         |
| python_startup         | 22.0 ms                                                         | 22.9 ms: 1.04x slower                                                         |
| Geometric mean         | (ref)                                                           | 1.01x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf1_win32-x86-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|-----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 5.33 ms: 1.93x faster                                                         |
| genshi_text     | 26.8 ms                                                         | 21.0 ms: 1.27x faster                                                         |
| genshi_xml      | 61.2 ms                                                         | 50.7 ms: 1.21x faster                                                         |
| django_template | 37.4 ms                                                         | 31.7 ms: 1.18x faster                                                         |
| Geometric mean  | (ref)                                                           | 1.37x faster                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240610-pythonperf1_win32-x86-brandtbucher-no_cold_exits-3.14.0a0-f837cc6 |
|----------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 146 us: 3.29x faster                                                          |
| spectral_norm              | 122 ms                                                          | 47.9 ms: 2.54x faster                                                         |
| nbody                      | 126 ms                                                          | 52.6 ms: 2.40x faster                                                         |
| generators                 | 52.2 ms                                                         | 23.5 ms: 2.22x faster                                                         |
| logging_silent             | 119 ns                                                          | 54.8 ns: 2.18x faster                                                         |
| deepcopy_memo              | 40.0 us                                                         | 20.0 us: 2.00x faster                                                         |
| comprehensions             | 22.1 us                                                         | 11.3 us: 1.95x faster                                                         |
| mako                       | 10.3 ms                                                         | 5.33 ms: 1.93x faster                                                         |
| fannkuch                   | 399 ms                                                          | 211 ms: 1.89x faster                                                          |
| float                      | 76.1 ms                                                         | 41.6 ms: 1.83x faster                                                         |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.34 ms: 1.81x faster                                                         |
| scimark_fft                | 291 ms                                                          | 163 ms: 1.79x faster                                                          |
| scimark_monte_carlo        | 70.8 ms                                                         | 39.9 ms: 1.77x faster                                                         |
| pylint                     | 418 ms                                                          | 236 ms: 1.77x faster                                                          |
| richards_super             | 58.7 ms                                                         | 33.3 ms: 1.76x faster                                                         |
| pyflate                    | 471 ms                                                          | 270 ms: 1.75x faster                                                          |
| unpickle_pure_python       | 231 us                                                          | 135 us: 1.72x faster                                                          |
| hexiom                     | 7.51 ms                                                         | 4.45 ms: 1.69x faster                                                         |
| richards                   | 48.8 ms                                                         | 29.2 ms: 1.67x faster                                                         |
| tomli_loads                | 2.31 sec                                                        | 1.39 sec: 1.66x faster                                                        |
| sqlglot_parse              | 1.49 ms                                                         | 899 us: 1.66x faster                                                          |
| nqueens                    | 111 ms                                                          | 67.4 ms: 1.65x faster                                                         |
| chaos                      | 84.4 ms                                                         | 51.3 ms: 1.65x faster                                                         |
| crypto_pyaes               | 79.4 ms                                                         | 48.5 ms: 1.64x faster                                                         |
| deltablue                  | 4.10 ms                                                         | 2.51 ms: 1.63x faster                                                         |
| scimark_sor                | 135 ms                                                          | 87.6 ms: 1.54x faster                                                         |
| sqlglot_transpile          | 1.78 ms                                                         | 1.16 ms: 1.54x faster                                                         |
| pickle_pure_python         | 309 us                                                          | 201 us: 1.54x faster                                                          |
| raytrace                   | 327 ms                                                          | 213 ms: 1.54x faster                                                          |
| regex_compile              | 148 ms                                                          | 96.3 ms: 1.53x faster                                                         |
| coroutines                 | 23.7 ms                                                         | 15.6 ms: 1.53x faster                                                         |
| async_tree_none            | 343 ms                                                          | 228 ms: 1.50x faster                                                          |
| logging_simple             | 10.8 us                                                         | 7.21 us: 1.50x faster                                                         |
| pprint_pformat             | 1.70 sec                                                        | 1.13 sec: 1.50x faster                                                        |
| pprint_safe_repr           | 819 ms                                                          | 550 ms: 1.49x faster                                                          |
| json_dumps                 | 9.80 ms                                                         | 6.66 ms: 1.47x faster                                                         |
| async_tree_memoization     | 408 ms                                                          | 278 ms: 1.47x faster                                                          |
| logging_format             | 11.5 us                                                         | 7.82 us: 1.46x faster                                                         |
| async_tree_none_tg         | 301 ms                                                          | 206 ms: 1.46x faster                                                          |
| async_tree_memoization_tg  | 378 ms                                                          | 261 ms: 1.45x faster                                                          |
| scimark_lu                 | 102 ms                                                          | 71.1 ms: 1.44x faster                                                         |
| async_tree_io              | 754 ms                                                          | 527 ms: 1.43x faster                                                          |
| async_tree_io_tg           | 746 ms                                                          | 533 ms: 1.40x faster                                                          |
| sympy_sum                  | 149 ms                                                          | 108 ms: 1.39x faster                                                          |
| xml_etree_process          | 55.0 ms                                                         | 40.2 ms: 1.37x faster                                                         |
| sympy_str                  | 283 ms                                                          | 211 ms: 1.34x faster                                                          |
| go                         | 147 ms                                                          | 111 ms: 1.33x faster                                                          |
| xml_etree_generate         | 71.6 ms                                                         | 54.5 ms: 1.32x faster                                                         |
| pycparser                  | 1.04 sec                                                        | 795 ms: 1.31x faster                                                          |
| mdp                        | 2.07 sec                                                        | 1.59 sec: 1.30x faster                                                        |
| sympy_integrate            | 19.9 ms                                                         | 15.5 ms: 1.29x faster                                                         |
| deepcopy                   | 381 us                                                          | 300 us: 1.27x faster                                                          |
| genshi_text                | 26.8 ms                                                         | 21.0 ms: 1.27x faster                                                         |
| meteor_contest             | 90.9 ms                                                         | 72.3 ms: 1.26x faster                                                         |
| asyncio_tcp                | 787 ms                                                          | 626 ms: 1.26x faster                                                          |
| sqlglot_optimize           | 51.8 ms                                                         | 41.7 ms: 1.24x faster                                                         |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 464 ms: 1.24x faster                                                          |
| xml_etree_iterparse        | 75.6 ms                                                         | 61.1 ms: 1.24x faster                                                         |
| sympy_expand               | 462 ms                                                          | 374 ms: 1.23x faster                                                          |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 479 ms: 1.23x faster                                                          |
| tornado_http               | 118 ms                                                          | 97.0 ms: 1.22x faster                                                         |
| deepcopy_reduce            | 3.32 us                                                         | 2.74 us: 1.21x faster                                                         |
| genshi_xml                 | 61.2 ms                                                         | 50.7 ms: 1.21x faster                                                         |
| coverage                   | 58.0 ms                                                         | 48.6 ms: 1.19x faster                                                         |
| unpickle_list              | 3.28 us                                                         | 2.76 us: 1.19x faster                                                         |
| html5lib                   | 54.3 ms                                                         | 45.9 ms: 1.18x faster                                                         |
| django_template            | 37.4 ms                                                         | 31.7 ms: 1.18x faster                                                         |
| bench_thread_pool          | 1.14 ms                                                         | 976 us: 1.17x faster                                                          |
| 2to3                       | 282 ms                                                          | 244 ms: 1.16x faster                                                          |
| xml_etree_parse            | 114 ms                                                          | 99.5 ms: 1.15x faster                                                         |
| thrift                     | 801 us                                                          | 712 us: 1.12x faster                                                          |
| docutils                   | 2.10 sec                                                        | 1.87 sec: 1.12x faster                                                        |
| sqlite_synth               | 2.15 us                                                         | 1.92 us: 1.12x faster                                                         |
| json                       | 4.78 ms                                                         | 4.30 ms: 1.11x faster                                                         |
| pidigits                   | 203 ms                                                          | 195 ms: 1.04x faster                                                          |
| python_startup_no_site     | 18.8 ms                                                         | 18.5 ms: 1.02x faster                                                         |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.8 sec: 1.01x faster                                                        |
| telco                      | 5.29 ms                                                         | 5.23 ms: 1.01x faster                                                         |
| regex_dna                  | 122 ms                                                          | 124 ms: 1.02x slower                                                          |
| bench_mp_pool              | 70.9 ms                                                         | 73.0 ms: 1.03x slower                                                         |
| pickle                     | 7.99 us                                                         | 8.24 us: 1.03x slower                                                         |
| json_loads                 | 20.0 us                                                         | 20.7 us: 1.03x slower                                                         |
| pathlib                    | 79.9 ms                                                         | 82.7 ms: 1.03x slower                                                         |
| pickle_dict                | 20.1 us                                                         | 20.9 us: 1.04x slower                                                         |
| python_startup             | 22.0 ms                                                         | 22.9 ms: 1.04x slower                                                         |
| regex_v8                   | 15.2 ms                                                         | 15.9 ms: 1.05x slower                                                         |
| gc_traversal               | 1.38 ms                                                         | 1.46 ms: 1.06x slower                                                         |
| regex_effbot               | 1.82 ms                                                         | 1.99 ms: 1.09x slower                                                         |
| pickle_list                | 3.27 us                                                         | 3.58 us: 1.10x slower                                                         |
| unpickle                   | 9.23 us                                                         | 10.3 us: 1.11x slower                                                         |
| async_generators           | 260 ms                                                          | 301 ms: 1.16x slower                                                          |
| create_gc_cycles           | 618 us                                                          | 755 us: 1.22x slower                                                          |
| sqlglot_normalize          | 113 ms                                                          | 219 ms: 1.93x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.35x faster                                                                  |
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.30x
- 95% likely to have a speedup of 1.30x
- 99% likely to have a speedup of 1.27x

# Memory
- memory change: unknown