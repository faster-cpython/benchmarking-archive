# Results vs. 3.12.0

- fork: savannahostrowski
- ref: llvm_18
- machine: windows-x86
- commit hash: fe17f68
- commit date: 2024-04-26
- overall geometric mean: 1.09x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 270 ms: 1.04x faster                                                          |
| chameleon      | 7.75 ms                                                         | 6.48 ms: 1.20x faster                                                         |
| tornado_http   | 105 ms                                                          | 107 ms: 1.02x slower                                                          |
| Geometric mean | (ref)                                                           | 1.05x faster                                                                  |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 350 ms                                                          | 276 ms: 1.27x faster                                                          |
| async_tree_none_tg         | 278 ms                                                          | 224 ms: 1.24x faster                                                          |
| async_tree_io              | 693 ms                                                          | 562 ms: 1.23x faster                                                          |
| async_tree_memoization     | 364 ms                                                          | 301 ms: 1.21x faster                                                          |
| async_tree_io_tg           | 677 ms                                                          | 561 ms: 1.21x faster                                                          |
| async_tree_none            | 298 ms                                                          | 248 ms: 1.20x faster                                                          |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 469 ms: 1.17x faster                                                          |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 502 ms: 1.12x faster                                                          |
| Geometric mean             | (ref)                                                           | 1.20x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 76.7 ms                                                         | 53.7 ms: 1.43x faster                                                         |
| nbody          | 127 ms                                                          | 96.2 ms: 1.32x faster                                                         |
| Geometric mean | (ref)                                                           | 1.24x faster                                                                  |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 109 ms: 1.18x faster                                                          |
| regex_dna      | 127 ms                                                          | 128 ms: 1.01x slower                                                          |
| regex_v8       | 15.0 ms                                                         | 16.1 ms: 1.07x slower                                                         |
| Geometric mean | (ref)                                                           | 1.03x faster                                                                  |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_pure_python   | 286 us                                                          | 224 us: 1.28x faster                                                          |
| unpickle_pure_python | 210 us                                                          | 165 us: 1.27x faster                                                          |
| tomli_loads          | 2.20 sec                                                        | 1.75 sec: 1.25x faster                                                        |
| xml_etree_iterparse  | 77.6 ms                                                         | 65.7 ms: 1.18x faster                                                         |
| xml_etree_process    | 53.2 ms                                                         | 45.4 ms: 1.17x faster                                                         |
| xml_etree_generate   | 72.1 ms                                                         | 62.9 ms: 1.15x faster                                                         |
| xml_etree_parse      | 113 ms                                                          | 104 ms: 1.09x faster                                                          |
| json_dumps           | 7.40 ms                                                         | 6.90 ms: 1.07x faster                                                         |
| unpickle_list        | 2.95 us                                                         | 2.80 us: 1.05x faster                                                         |
| pickle_list          | 3.37 us                                                         | 3.28 us: 1.03x faster                                                         |
| json_loads           | 20.4 us                                                         | 20.5 us: 1.01x slower                                                         |
| pickle_dict          | 19.9 us                                                         | 20.3 us: 1.02x slower                                                         |
| pickle               | 7.79 us                                                         | 8.09 us: 1.04x slower                                                         |
| unpickle             | 9.71 us                                                         | 10.2 us: 1.05x slower                                                         |
| Geometric mean       | (ref)                                                           | 1.10x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 19.1 ms                                                         | 20.6 ms: 1.08x slower                                                         |
| python_startup         | 22.4 ms                                                         | 24.6 ms: 1.10x slower                                                         |
| Geometric mean         | (ref)                                                           | 1.09x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|-----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 9.96 ms                                                         | 7.09 ms: 1.40x faster                                                         |
| django_template | 36.9 ms                                                         | 33.8 ms: 1.09x faster                                                         |
| Geometric mean  | (ref)                                                           | 1.24x faster                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68 |
|----------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| generators                 | 38.5 ms                                                         | 23.0 ms: 1.67x faster                                                         |
| logging_silent             | 101 ns                                                          | 60.8 ns: 1.66x faster                                                         |
| spectral_norm              | 104 ms                                                          | 68.0 ms: 1.53x faster                                                         |
| deepcopy_memo              | 38.4 us                                                         | 25.1 us: 1.53x faster                                                         |
| float                      | 76.7 ms                                                         | 53.7 ms: 1.43x faster                                                         |
| mako                       | 9.96 ms                                                         | 7.09 ms: 1.40x faster                                                         |
| raytrace                   | 308 ms                                                          | 223 ms: 1.38x faster                                                          |
| nbody                      | 127 ms                                                          | 96.2 ms: 1.32x faster                                                         |
| scimark_sor                | 130 ms                                                          | 99.3 ms: 1.31x faster                                                         |
| deltablue                  | 3.58 ms                                                         | 2.79 ms: 1.28x faster                                                         |
| coroutines                 | 20.9 ms                                                         | 16.4 ms: 1.28x faster                                                         |
| pickle_pure_python         | 286 us                                                          | 224 us: 1.28x faster                                                          |
| unpickle_pure_python       | 210 us                                                          | 165 us: 1.27x faster                                                          |
| async_tree_memoization_tg  | 350 ms                                                          | 276 ms: 1.27x faster                                                          |
| tomli_loads                | 2.20 sec                                                        | 1.75 sec: 1.25x faster                                                        |
| async_tree_none_tg         | 278 ms                                                          | 224 ms: 1.24x faster                                                          |
| async_tree_io              | 693 ms                                                          | 562 ms: 1.23x faster                                                          |
| deepcopy_reduce            | 3.23 us                                                         | 2.64 us: 1.22x faster                                                         |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 3.17 ms: 1.22x faster                                                         |
| richards                   | 41.3 ms                                                         | 34.0 ms: 1.22x faster                                                         |
| sqlglot_parse              | 1.25 ms                                                         | 1.03 ms: 1.21x faster                                                         |
| async_tree_memoization     | 364 ms                                                          | 301 ms: 1.21x faster                                                          |
| async_tree_io_tg           | 677 ms                                                          | 561 ms: 1.21x faster                                                          |
| logging_simple             | 9.75 us                                                         | 8.11 us: 1.20x faster                                                         |
| async_tree_none            | 298 ms                                                          | 248 ms: 1.20x faster                                                          |
| chameleon                  | 7.75 ms                                                         | 6.48 ms: 1.20x faster                                                         |
| richards_super             | 46.5 ms                                                         | 38.9 ms: 1.19x faster                                                         |
| logging_format             | 10.4 us                                                         | 8.72 us: 1.19x faster                                                         |
| comprehensions             | 19.2 us                                                         | 16.1 us: 1.19x faster                                                         |
| regex_compile              | 129 ms                                                          | 109 ms: 1.18x faster                                                          |
| xml_etree_iterparse        | 77.6 ms                                                         | 65.7 ms: 1.18x faster                                                         |
| sqlglot_transpile          | 1.53 ms                                                         | 1.30 ms: 1.18x faster                                                         |
| deepcopy                   | 360 us                                                          | 305 us: 1.18x faster                                                          |
| xml_etree_process          | 53.2 ms                                                         | 45.4 ms: 1.17x faster                                                         |
| pyflate                    | 424 ms                                                          | 362 ms: 1.17x faster                                                          |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 469 ms: 1.17x faster                                                          |
| scimark_fft                | 271 ms                                                          | 235 ms: 1.15x faster                                                          |
| pycparser                  | 978 ms                                                          | 851 ms: 1.15x faster                                                          |
| xml_etree_generate         | 72.1 ms                                                         | 62.9 ms: 1.15x faster                                                         |
| chaos                      | 69.4 ms                                                         | 60.9 ms: 1.14x faster                                                         |
| fannkuch                   | 354 ms                                                          | 314 ms: 1.13x faster                                                          |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 502 ms: 1.12x faster                                                          |
| scimark_monte_carlo        | 66.4 ms                                                         | 59.3 ms: 1.12x faster                                                         |
| crypto_pyaes               | 69.2 ms                                                         | 62.2 ms: 1.11x faster                                                         |
| go                         | 137 ms                                                          | 124 ms: 1.10x faster                                                          |
| django_template            | 36.9 ms                                                         | 33.8 ms: 1.09x faster                                                         |
| sympy_sum                  | 123 ms                                                          | 113 ms: 1.09x faster                                                          |
| xml_etree_parse            | 113 ms                                                          | 104 ms: 1.09x faster                                                          |
| hexiom                     | 6.82 ms                                                         | 6.30 ms: 1.08x faster                                                         |
| bench_thread_pool          | 1.10 ms                                                         | 1.02 ms: 1.08x faster                                                         |
| sympy_str                  | 240 ms                                                          | 223 ms: 1.07x faster                                                          |
| json_dumps                 | 7.40 ms                                                         | 6.90 ms: 1.07x faster                                                         |
| unpickle_list              | 2.95 us                                                         | 2.80 us: 1.05x faster                                                         |
| sympy_integrate            | 17.5 ms                                                         | 16.7 ms: 1.05x faster                                                         |
| mdp                        | 1.91 sec                                                        | 1.83 sec: 1.04x faster                                                        |
| sqlite_synth               | 2.07 us                                                         | 1.98 us: 1.04x faster                                                         |
| 2to3                       | 280 ms                                                          | 270 ms: 1.04x faster                                                          |
| async_generators           | 313 ms                                                          | 302 ms: 1.04x faster                                                          |
| sympy_expand               | 398 ms                                                          | 385 ms: 1.03x faster                                                          |
| scimark_lu                 | 93.2 ms                                                         | 90.3 ms: 1.03x faster                                                         |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 17.1 sec: 1.03x faster                                                        |
| pathlib                    | 91.4 ms                                                         | 88.8 ms: 1.03x faster                                                         |
| pickle_list                | 3.37 us                                                         | 3.28 us: 1.03x faster                                                         |
| bench_mp_pool              | 75.4 ms                                                         | 74.1 ms: 1.02x faster                                                         |
| meteor_contest             | 86.9 ms                                                         | 86.0 ms: 1.01x faster                                                         |
| sqlglot_optimize           | 48.5 ms                                                         | 48.2 ms: 1.01x faster                                                         |
| pprint_pformat             | 1.50 sec                                                        | 1.49 sec: 1.01x faster                                                        |
| pprint_safe_repr           | 721 ms                                                          | 727 ms: 1.01x slower                                                          |
| json_loads                 | 20.4 us                                                         | 20.5 us: 1.01x slower                                                         |
| regex_dna                  | 127 ms                                                          | 128 ms: 1.01x slower                                                          |
| sqlglot_normalize          | 100 ms                                                          | 101 ms: 1.01x slower                                                          |
| json                       | 4.15 ms                                                         | 4.22 ms: 1.02x slower                                                         |
| pickle_dict                | 19.9 us                                                         | 20.3 us: 1.02x slower                                                         |
| tornado_http               | 105 ms                                                          | 107 ms: 1.02x slower                                                          |
| gc_traversal               | 1.44 ms                                                         | 1.47 ms: 1.02x slower                                                         |
| pickle                     | 7.79 us                                                         | 8.09 us: 1.04x slower                                                         |
| unpickle                   | 9.71 us                                                         | 10.2 us: 1.05x slower                                                         |
| regex_v8                   | 15.0 ms                                                         | 16.1 ms: 1.07x slower                                                         |
| python_startup_no_site     | 19.1 ms                                                         | 20.6 ms: 1.08x slower                                                         |
| python_startup             | 22.4 ms                                                         | 24.6 ms: 1.10x slower                                                         |
| create_gc_cycles           | 652 us                                                          | 737 us: 1.13x slower                                                          |
| asyncio_tcp                | 662 ms                                                          | 764 ms: 1.15x slower                                                          |
| telco                      | 5.51 ms                                                         | 6.41 ms: 1.16x slower                                                         |
| typing_runtime_protocols   | 126 us                                                          | 154 us: 1.22x slower                                                          |
| coverage                   | 48.4 ms                                                         | 420 ms: 8.66x slower                                                          |
| Geometric mean             | (ref)                                                           | 1.09x faster                                                                  |

Benchmark hidden because not significant (4): regex_effbot, nqueens, pidigits, docutils
Ignored benchmarks (7) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240426-3.13.0a6+-fe17f68-JIT/bm-20240426-pythonperf1_win32-x86-savannahostrowski-llvm_18-3.13.0a6+-fe17f68.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: unknown