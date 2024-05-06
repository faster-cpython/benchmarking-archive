# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_align
- machine: windows-x86
- commit hash: d1a7b3a
- commit date: 2024-03-30
- overall geometric mean: 1.17x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.16x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 254 ms: 1.11x faster                                                          |
| chameleon      | 8.08 ms                                                         | 6.36 ms: 1.27x faster                                                         |
| docutils       | 2.10 sec                                                        | 1.91 sec: 1.10x faster                                                        |
| html5lib       | 54.3 ms                                                         | 45.4 ms: 1.20x faster                                                         |
| tornado_http   | 118 ms                                                          | 96.1 ms: 1.23x faster                                                         |
| Geometric mean | (ref)                                                           | 1.18x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 231 ms: 1.48x faster                                                          |
| async_tree_none_tg         | 301 ms                                                          | 206 ms: 1.46x faster                                                          |
| async_tree_memoization_tg  | 378 ms                                                          | 262 ms: 1.44x faster                                                          |
| async_tree_memoization     | 408 ms                                                          | 284 ms: 1.44x faster                                                          |
| async_tree_io              | 754 ms                                                          | 545 ms: 1.38x faster                                                          |
| async_tree_io_tg           | 746 ms                                                          | 544 ms: 1.37x faster                                                          |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 451 ms: 1.28x faster                                                          |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 474 ms: 1.25x faster                                                          |
| Geometric mean             | (ref)                                                           | 1.39x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 76.1 ms                                                         | 54.0 ms: 1.41x faster                                                         |
| nbody          | 126 ms                                                          | 96.5 ms: 1.31x faster                                                         |
| pidigits       | 203 ms                                                          | 197 ms: 1.03x faster                                                          |
| Geometric mean | (ref)                                                           | 1.24x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 113 ms: 1.31x faster                                                          |
| regex_effbot   | 1.82 ms                                                         | 1.90 ms: 1.04x slower                                                         |
| regex_v8       | 15.2 ms                                                         | 16.3 ms: 1.08x slower                                                         |
| Geometric mean | (ref)                                                           | 1.04x faster                                                                  |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 9.80 ms                                                         | 6.93 ms: 1.41x faster                                                         |
| pickle_pure_python   | 309 us                                                          | 223 us: 1.39x faster                                                          |
| unpickle_pure_python | 231 us                                                          | 171 us: 1.35x faster                                                          |
| tomli_loads          | 2.31 sec                                                        | 1.74 sec: 1.33x faster                                                        |
| xml_etree_process    | 55.0 ms                                                         | 43.8 ms: 1.26x faster                                                         |
| unpickle_list        | 3.28 us                                                         | 2.80 us: 1.17x faster                                                         |
| xml_etree_iterparse  | 75.6 ms                                                         | 65.4 ms: 1.16x faster                                                         |
| xml_etree_generate   | 71.6 ms                                                         | 62.0 ms: 1.15x faster                                                         |
| xml_etree_parse      | 114 ms                                                          | 107 ms: 1.07x faster                                                          |
| pickle_dict          | 20.1 us                                                         | 19.8 us: 1.01x faster                                                         |
| pickle               | 7.99 us                                                         | 7.90 us: 1.01x faster                                                         |
| pickle_list          | 3.27 us                                                         | 3.23 us: 1.01x faster                                                         |
| json_loads           | 20.0 us                                                         | 20.2 us: 1.01x slower                                                         |
| unpickle             | 9.23 us                                                         | 10.0 us: 1.09x slower                                                         |
| Geometric mean       | (ref)                                                           | 1.15x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                         | 24.4 ms: 1.11x slower                                                         |
| python_startup_no_site | 18.8 ms                                                         | 21.8 ms: 1.16x slower                                                         |
| Geometric mean         | (ref)                                                           | 1.13x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 7.07 ms: 1.45x faster                                                         |
| genshi_text     | 26.8 ms                                                         | 20.7 ms: 1.29x faster                                                         |
| genshi_xml      | 61.2 ms                                                         | 48.8 ms: 1.26x faster                                                         |
| django_template | 37.4 ms                                                         | 33.6 ms: 1.11x faster                                                         |
| Geometric mean  | (ref)                                                           | 1.27x faster                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 94.1 us: 5.08x faster                                                         |
| generators                 | 52.2 ms                                                         | 23.1 ms: 2.26x faster                                                         |
| logging_silent             | 119 ns                                                          | 61.3 ns: 1.94x faster                                                         |
| pylint                     | 418 ms                                                          | 221 ms: 1.89x faster                                                          |
| spectral_norm              | 122 ms                                                          | 72.1 ms: 1.69x faster                                                         |
| coroutines                 | 23.7 ms                                                         | 14.9 ms: 1.59x faster                                                         |
| deltablue                  | 4.10 ms                                                         | 2.61 ms: 1.57x faster                                                         |
| deepcopy_memo              | 40.0 us                                                         | 26.1 us: 1.53x faster                                                         |
| sqlglot_parse              | 1.49 ms                                                         | 1.00 ms: 1.49x faster                                                         |
| async_tree_none            | 343 ms                                                          | 231 ms: 1.48x faster                                                          |
| async_tree_none_tg         | 301 ms                                                          | 206 ms: 1.46x faster                                                          |
| mako                       | 10.3 ms                                                         | 7.07 ms: 1.45x faster                                                         |
| async_tree_memoization_tg  | 378 ms                                                          | 262 ms: 1.44x faster                                                          |
| async_tree_memoization     | 408 ms                                                          | 284 ms: 1.44x faster                                                          |
| richards_super             | 58.7 ms                                                         | 40.8 ms: 1.44x faster                                                         |
| comprehensions             | 22.1 us                                                         | 15.4 us: 1.43x faster                                                         |
| unpack_sequence            | 65.2 ns                                                         | 45.7 ns: 1.43x faster                                                         |
| sqlglot_transpile          | 1.78 ms                                                         | 1.25 ms: 1.42x faster                                                         |
| json_dumps                 | 9.80 ms                                                         | 6.93 ms: 1.41x faster                                                         |
| float                      | 76.1 ms                                                         | 54.0 ms: 1.41x faster                                                         |
| chaos                      | 84.4 ms                                                         | 60.7 ms: 1.39x faster                                                         |
| pickle_pure_python         | 309 us                                                          | 223 us: 1.39x faster                                                          |
| async_tree_io              | 754 ms                                                          | 545 ms: 1.38x faster                                                          |
| sympy_sum                  | 149 ms                                                          | 108 ms: 1.38x faster                                                          |
| async_tree_io_tg           | 746 ms                                                          | 544 ms: 1.37x faster                                                          |
| scimark_sor                | 135 ms                                                          | 99.9 ms: 1.35x faster                                                         |
| unpickle_pure_python       | 231 us                                                          | 171 us: 1.35x faster                                                          |
| richards                   | 48.8 ms                                                         | 36.2 ms: 1.35x faster                                                         |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.15 ms: 1.34x faster                                                         |
| tomli_loads                | 2.31 sec                                                        | 1.74 sec: 1.33x faster                                                        |
| sympy_str                  | 283 ms                                                          | 213 ms: 1.33x faster                                                          |
| deepcopy_reduce            | 3.32 us                                                         | 2.51 us: 1.32x faster                                                         |
| deepcopy                   | 381 us                                                          | 291 us: 1.31x faster                                                          |
| nbody                      | 126 ms                                                          | 96.5 ms: 1.31x faster                                                         |
| regex_compile              | 148 ms                                                          | 113 ms: 1.31x faster                                                          |
| genshi_text                | 26.8 ms                                                         | 20.7 ms: 1.29x faster                                                         |
| pyflate                    | 471 ms                                                          | 365 ms: 1.29x faster                                                          |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 451 ms: 1.28x faster                                                          |
| chameleon                  | 8.08 ms                                                         | 6.36 ms: 1.27x faster                                                         |
| logging_simple             | 10.8 us                                                         | 8.55 us: 1.26x faster                                                         |
| logging_format             | 11.5 us                                                         | 9.11 us: 1.26x faster                                                         |
| xml_etree_process          | 55.0 ms                                                         | 43.8 ms: 1.26x faster                                                         |
| genshi_xml                 | 61.2 ms                                                         | 48.8 ms: 1.26x faster                                                         |
| asyncio_tcp                | 787 ms                                                          | 627 ms: 1.25x faster                                                          |
| raytrace                   | 327 ms                                                          | 262 ms: 1.25x faster                                                          |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 474 ms: 1.25x faster                                                          |
| sympy_expand               | 462 ms                                                          | 371 ms: 1.25x faster                                                          |
| crypto_pyaes               | 79.4 ms                                                         | 63.7 ms: 1.25x faster                                                         |
| sympy_integrate            | 19.9 ms                                                         | 16.0 ms: 1.24x faster                                                         |
| fannkuch                   | 399 ms                                                          | 323 ms: 1.24x faster                                                          |
| tornado_http               | 118 ms                                                          | 96.1 ms: 1.23x faster                                                         |
| scimark_fft                | 291 ms                                                          | 238 ms: 1.23x faster                                                          |
| pycparser                  | 1.04 sec                                                        | 857 ms: 1.22x faster                                                          |
| html5lib                   | 54.3 ms                                                         | 45.4 ms: 1.20x faster                                                         |
| go                         | 147 ms                                                          | 123 ms: 1.20x faster                                                          |
| nqueens                    | 111 ms                                                          | 93.5 ms: 1.19x faster                                                         |
| hexiom                     | 7.51 ms                                                         | 6.30 ms: 1.19x faster                                                         |
| mdp                        | 2.07 sec                                                        | 1.74 sec: 1.19x faster                                                        |
| unpickle_list              | 3.28 us                                                         | 2.80 us: 1.17x faster                                                         |
| xml_etree_iterparse        | 75.6 ms                                                         | 65.4 ms: 1.16x faster                                                         |
| xml_etree_generate         | 71.6 ms                                                         | 62.0 ms: 1.15x faster                                                         |
| scimark_monte_carlo        | 70.8 ms                                                         | 62.0 ms: 1.14x faster                                                         |
| pprint_pformat             | 1.70 sec                                                        | 1.49 sec: 1.14x faster                                                        |
| sqlglot_optimize           | 51.8 ms                                                         | 45.6 ms: 1.14x faster                                                         |
| json                       | 4.78 ms                                                         | 4.26 ms: 1.12x faster                                                         |
| sqlite_synth               | 2.15 us                                                         | 1.92 us: 1.12x faster                                                         |
| pprint_safe_repr           | 819 ms                                                          | 735 ms: 1.12x faster                                                          |
| django_template            | 37.4 ms                                                         | 33.6 ms: 1.11x faster                                                         |
| 2to3                       | 282 ms                                                          | 254 ms: 1.11x faster                                                          |
| meteor_contest             | 90.9 ms                                                         | 82.0 ms: 1.11x faster                                                         |
| bench_thread_pool          | 1.14 ms                                                         | 1.03 ms: 1.10x faster                                                         |
| docutils                   | 2.10 sec                                                        | 1.91 sec: 1.10x faster                                                        |
| scimark_lu                 | 102 ms                                                          | 94.8 ms: 1.08x faster                                                         |
| xml_etree_parse            | 114 ms                                                          | 107 ms: 1.07x faster                                                          |
| pidigits                   | 203 ms                                                          | 197 ms: 1.03x faster                                                          |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.7 sec: 1.02x faster                                                        |
| pickle_dict                | 20.1 us                                                         | 19.8 us: 1.01x faster                                                         |
| pickle                     | 7.99 us                                                         | 7.90 us: 1.01x faster                                                         |
| pickle_list                | 3.27 us                                                         | 3.23 us: 1.01x faster                                                         |
| json_loads                 | 20.0 us                                                         | 20.2 us: 1.01x slower                                                         |
| bench_mp_pool              | 70.9 ms                                                         | 72.3 ms: 1.02x slower                                                         |
| gc_traversal               | 1.38 ms                                                         | 1.43 ms: 1.04x slower                                                         |
| regex_effbot               | 1.82 ms                                                         | 1.90 ms: 1.04x slower                                                         |
| regex_v8                   | 15.2 ms                                                         | 16.3 ms: 1.08x slower                                                         |
| pathlib                    | 79.9 ms                                                         | 86.3 ms: 1.08x slower                                                         |
| unpickle                   | 9.23 us                                                         | 10.0 us: 1.09x slower                                                         |
| async_generators           | 260 ms                                                          | 286 ms: 1.10x slower                                                          |
| python_startup             | 22.0 ms                                                         | 24.4 ms: 1.11x slower                                                         |
| python_startup_no_site     | 18.8 ms                                                         | 21.8 ms: 1.16x slower                                                         |
| create_gc_cycles           | 618 us                                                          | 738 us: 1.19x slower                                                          |
| telco                      | 5.29 ms                                                         | 6.58 ms: 1.24x slower                                                         |
| sqlglot_normalize          | 113 ms                                                          | 241 ms: 2.13x slower                                                          |
| coverage                   | 58.0 ms                                                         | 489 ms: 8.43x slower                                                          |
| thrift                     | 801 us                                                          | 11.1 ms: 13.87x slower                                                        |
| Geometric mean             | (ref)                                                           | 1.17x faster                                                                  |

Benchmark hidden because not significant (1): regex_dna
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.19x
- 95% likely to have a speedup of 1.19x
- 99% likely to have a speedup of 1.16x

# Memory
- memory change: unknown