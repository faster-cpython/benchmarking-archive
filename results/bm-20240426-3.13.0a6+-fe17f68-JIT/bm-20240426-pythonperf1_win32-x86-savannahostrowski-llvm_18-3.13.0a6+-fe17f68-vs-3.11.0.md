# Results vs. 3.11.0

- fork: savannahostrowski
- ref: llvm_18
- machine: windows-x86
- commit hash: fe17f68
- commit date: 2024-04-26
- overall geometric mean: 1.15x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 270 ms: 1.05x faster                                                          |
| chameleon      | 8.08 ms                                                         | 6.48 ms: 1.25x faster                                                         |
| docutils       | 2.10 sec                                                        | 1.99 sec: 1.05x faster                                                        |
| html5lib       | 54.3 ms                                                         | 46.1 ms: 1.18x faster                                                         |
| tornado_http   | 118 ms                                                          | 107 ms: 1.11x faster                                                          |
| Geometric mean | (ref)                                                           | 1.12x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 248 ms: 1.38x faster                                                          |
| async_tree_memoization_tg  | 378 ms                                                          | 276 ms: 1.37x faster                                                          |
| async_tree_memoization     | 408 ms                                                          | 301 ms: 1.36x faster                                                          |
| async_tree_none_tg         | 301 ms                                                          | 224 ms: 1.34x faster                                                          |
| async_tree_io              | 754 ms                                                          | 562 ms: 1.34x faster                                                          |
| async_tree_io_tg           | 746 ms                                                          | 561 ms: 1.33x faster                                                          |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 469 ms: 1.23x faster                                                          |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 502 ms: 1.18x faster                                                          |
| Geometric mean             | (ref)                                                           | 1.31x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 76.1 ms                                                         | 53.7 ms: 1.42x faster                                                         |
| nbody          | 126 ms                                                          | 96.2 ms: 1.31x faster                                                         |
| pidigits       | 203 ms                                                          | 199 ms: 1.02x faster                                                          |
| Geometric mean | (ref)                                                           | 1.24x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 109 ms: 1.35x faster                                                          |
| regex_dna      | 122 ms                                                          | 128 ms: 1.06x slower                                                          |
| regex_v8       | 15.2 ms                                                         | 16.1 ms: 1.06x slower                                                         |
| regex_effbot   | 1.82 ms                                                         | 2.00 ms: 1.10x slower                                                         |
| Geometric mean | (ref)                                                           | 1.02x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 9.80 ms                                                         | 6.90 ms: 1.42x faster                                                         |
| unpickle_pure_python | 231 us                                                          | 165 us: 1.40x faster                                                          |
| pickle_pure_python   | 309 us                                                          | 224 us: 1.38x faster                                                          |
| tomli_loads          | 2.31 sec                                                        | 1.75 sec: 1.32x faster                                                        |
| xml_etree_process    | 55.0 ms                                                         | 45.4 ms: 1.21x faster                                                         |
| unpickle_list        | 3.28 us                                                         | 2.80 us: 1.17x faster                                                         |
| xml_etree_iterparse  | 75.6 ms                                                         | 65.7 ms: 1.15x faster                                                         |
| xml_etree_generate   | 71.6 ms                                                         | 62.9 ms: 1.14x faster                                                         |
| xml_etree_parse      | 114 ms                                                          | 104 ms: 1.10x faster                                                          |
| pickle_list          | 3.27 us                                                         | 3.28 us: 1.01x slower                                                         |
| pickle_dict          | 20.1 us                                                         | 20.3 us: 1.01x slower                                                         |
| pickle               | 7.99 us                                                         | 8.09 us: 1.01x slower                                                         |
| json_loads           | 20.0 us                                                         | 20.5 us: 1.03x slower                                                         |
| unpickle             | 9.23 us                                                         | 10.2 us: 1.11x slower                                                         |
| Geometric mean       | (ref)                                                           | 1.14x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 18.8 ms                                                         | 20.6 ms: 1.10x slower                                                         |
| python_startup         | 22.0 ms                                                         | 24.6 ms: 1.12x slower                                                         |
| Geometric mean         | (ref)                                                           | 1.11x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|-----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 7.09 ms: 1.45x faster                                                         |
| genshi_xml      | 61.2 ms                                                         | 52.1 ms: 1.17x faster                                                         |
| django_template | 37.4 ms                                                         | 33.8 ms: 1.11x faster                                                         |
| genshi_text     | 26.8 ms                                                         | 24.3 ms: 1.10x faster                                                         |
| Geometric mean  | (ref)                                                           | 1.20x faster                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 154 us: 3.10x faster                                                          |
| generators                 | 52.2 ms                                                         | 23.0 ms: 2.27x faster                                                         |
| logging_silent             | 119 ns                                                          | 60.8 ns: 1.96x faster                                                         |
| spectral_norm              | 122 ms                                                          | 68.0 ms: 1.79x faster                                                         |
| pylint                     | 418 ms                                                          | 243 ms: 1.72x faster                                                          |
| deepcopy_memo              | 40.0 us                                                         | 25.1 us: 1.59x faster                                                         |
| richards_super             | 58.7 ms                                                         | 38.9 ms: 1.51x faster                                                         |
| raytrace                   | 327 ms                                                          | 223 ms: 1.47x faster                                                          |
| deltablue                  | 4.10 ms                                                         | 2.79 ms: 1.47x faster                                                         |
| coroutines                 | 23.7 ms                                                         | 16.4 ms: 1.45x faster                                                         |
| mako                       | 10.3 ms                                                         | 7.09 ms: 1.45x faster                                                         |
| sqlglot_parse              | 1.49 ms                                                         | 1.03 ms: 1.45x faster                                                         |
| richards                   | 48.8 ms                                                         | 34.0 ms: 1.44x faster                                                         |
| json_dumps                 | 9.80 ms                                                         | 6.90 ms: 1.42x faster                                                         |
| float                      | 76.1 ms                                                         | 53.7 ms: 1.42x faster                                                         |
| unpickle_pure_python       | 231 us                                                          | 165 us: 1.40x faster                                                          |
| chaos                      | 84.4 ms                                                         | 60.9 ms: 1.39x faster                                                         |
| async_tree_none            | 343 ms                                                          | 248 ms: 1.38x faster                                                          |
| pickle_pure_python         | 309 us                                                          | 224 us: 1.38x faster                                                          |
| sqlglot_transpile          | 1.78 ms                                                         | 1.30 ms: 1.38x faster                                                         |
| comprehensions             | 22.1 us                                                         | 16.1 us: 1.37x faster                                                         |
| async_tree_memoization_tg  | 378 ms                                                          | 276 ms: 1.37x faster                                                          |
| scimark_sor                | 135 ms                                                          | 99.3 ms: 1.36x faster                                                         |
| async_tree_memoization     | 408 ms                                                          | 301 ms: 1.36x faster                                                          |
| regex_compile              | 148 ms                                                          | 109 ms: 1.35x faster                                                          |
| async_tree_none_tg         | 301 ms                                                          | 224 ms: 1.34x faster                                                          |
| async_tree_io              | 754 ms                                                          | 562 ms: 1.34x faster                                                          |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.17 ms: 1.34x faster                                                         |
| logging_simple             | 10.8 us                                                         | 8.11 us: 1.33x faster                                                         |
| async_tree_io_tg           | 746 ms                                                          | 561 ms: 1.33x faster                                                          |
| tomli_loads                | 2.31 sec                                                        | 1.75 sec: 1.32x faster                                                        |
| sympy_sum                  | 149 ms                                                          | 113 ms: 1.32x faster                                                          |
| logging_format             | 11.5 us                                                         | 8.72 us: 1.31x faster                                                         |
| nbody                      | 126 ms                                                          | 96.2 ms: 1.31x faster                                                         |
| pyflate                    | 471 ms                                                          | 362 ms: 1.30x faster                                                          |
| crypto_pyaes               | 79.4 ms                                                         | 62.2 ms: 1.28x faster                                                         |
| fannkuch                   | 399 ms                                                          | 314 ms: 1.27x faster                                                          |
| sympy_str                  | 283 ms                                                          | 223 ms: 1.27x faster                                                          |
| deepcopy_reduce            | 3.32 us                                                         | 2.64 us: 1.26x faster                                                         |
| deepcopy                   | 381 us                                                          | 305 us: 1.25x faster                                                          |
| chameleon                  | 8.08 ms                                                         | 6.48 ms: 1.25x faster                                                         |
| scimark_fft                | 291 ms                                                          | 235 ms: 1.24x faster                                                          |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 469 ms: 1.23x faster                                                          |
| pycparser                  | 1.04 sec                                                        | 851 ms: 1.23x faster                                                          |
| xml_etree_process          | 55.0 ms                                                         | 45.4 ms: 1.21x faster                                                         |
| sympy_expand               | 462 ms                                                          | 385 ms: 1.20x faster                                                          |
| nqueens                    | 111 ms                                                          | 93.2 ms: 1.20x faster                                                         |
| scimark_monte_carlo        | 70.8 ms                                                         | 59.3 ms: 1.19x faster                                                         |
| hexiom                     | 7.51 ms                                                         | 6.30 ms: 1.19x faster                                                         |
| sympy_integrate            | 19.9 ms                                                         | 16.7 ms: 1.19x faster                                                         |
| go                         | 147 ms                                                          | 124 ms: 1.18x faster                                                          |
| html5lib                   | 54.3 ms                                                         | 46.1 ms: 1.18x faster                                                         |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 502 ms: 1.18x faster                                                          |
| genshi_xml                 | 61.2 ms                                                         | 52.1 ms: 1.17x faster                                                         |
| unpickle_list              | 3.28 us                                                         | 2.80 us: 1.17x faster                                                         |
| xml_etree_iterparse        | 75.6 ms                                                         | 65.7 ms: 1.15x faster                                                         |
| xml_etree_generate         | 71.6 ms                                                         | 62.9 ms: 1.14x faster                                                         |
| pprint_pformat             | 1.70 sec                                                        | 1.49 sec: 1.14x faster                                                        |
| json                       | 4.78 ms                                                         | 4.22 ms: 1.13x faster                                                         |
| scimark_lu                 | 102 ms                                                          | 90.3 ms: 1.13x faster                                                         |
| mdp                        | 2.07 sec                                                        | 1.83 sec: 1.13x faster                                                        |
| pprint_safe_repr           | 819 ms                                                          | 727 ms: 1.13x faster                                                          |
| sqlglot_normalize          | 113 ms                                                          | 101 ms: 1.12x faster                                                          |
| bench_thread_pool          | 1.14 ms                                                         | 1.02 ms: 1.11x faster                                                         |
| tornado_http               | 118 ms                                                          | 107 ms: 1.11x faster                                                          |
| django_template            | 37.4 ms                                                         | 33.8 ms: 1.11x faster                                                         |
| genshi_text                | 26.8 ms                                                         | 24.3 ms: 1.10x faster                                                         |
| xml_etree_parse            | 114 ms                                                          | 104 ms: 1.10x faster                                                          |
| sqlite_synth               | 2.15 us                                                         | 1.98 us: 1.08x faster                                                         |
| sqlglot_optimize           | 51.8 ms                                                         | 48.2 ms: 1.08x faster                                                         |
| meteor_contest             | 90.9 ms                                                         | 86.0 ms: 1.06x faster                                                         |
| docutils                   | 2.10 sec                                                        | 1.99 sec: 1.05x faster                                                        |
| 2to3                       | 282 ms                                                          | 270 ms: 1.05x faster                                                          |
| pidigits                   | 203 ms                                                          | 199 ms: 1.02x faster                                                          |
| pickle_list                | 3.27 us                                                         | 3.28 us: 1.01x slower                                                         |
| pickle_dict                | 20.1 us                                                         | 20.3 us: 1.01x slower                                                         |
| pickle                     | 7.99 us                                                         | 8.09 us: 1.01x slower                                                         |
| json_loads                 | 20.0 us                                                         | 20.5 us: 1.03x slower                                                         |
| bench_mp_pool              | 70.9 ms                                                         | 74.1 ms: 1.04x slower                                                         |
| regex_dna                  | 122 ms                                                          | 128 ms: 1.06x slower                                                          |
| regex_v8                   | 15.2 ms                                                         | 16.1 ms: 1.06x slower                                                         |
| gc_traversal               | 1.38 ms                                                         | 1.47 ms: 1.07x slower                                                         |
| regex_effbot               | 1.82 ms                                                         | 2.00 ms: 1.10x slower                                                         |
| python_startup_no_site     | 18.8 ms                                                         | 20.6 ms: 1.10x slower                                                         |
| unpickle                   | 9.23 us                                                         | 10.2 us: 1.11x slower                                                         |
| pathlib                    | 79.9 ms                                                         | 88.8 ms: 1.11x slower                                                         |
| python_startup             | 22.0 ms                                                         | 24.6 ms: 1.12x slower                                                         |
| async_generators           | 260 ms                                                          | 302 ms: 1.16x slower                                                          |
| create_gc_cycles           | 618 us                                                          | 737 us: 1.19x slower                                                          |
| telco                      | 5.29 ms                                                         | 6.41 ms: 1.21x slower                                                         |
| coverage                   | 58.0 ms                                                         | 420 ms: 7.23x slower                                                          |
| thrift                     | 801 us                                                          | 10.8 ms: 13.52x slower                                                        |
| Geometric mean             | (ref)                                                           | 1.15x faster                                                                  |

Benchmark hidden because not significant (2): asyncio_tcp, asyncio_tcp_ssl
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.16x
- 95% likely to have a speedup of 1.15x
- 99% likely to have a speedup of 1.13x

# Memory
- memory change: unknown