# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_align
- machine: windows-x86
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.17x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 252 ms: 1.12x faster                                                          |
| chameleon      | 8.08 ms                                                         | 6.20 ms: 1.30x faster                                                         |
| docutils       | 2.10 sec                                                        | 1.93 sec: 1.09x faster                                                        |
| html5lib       | 54.3 ms                                                         | 45.5 ms: 1.19x faster                                                         |
| tornado_http   | 118 ms                                                          | 96.9 ms: 1.22x faster                                                         |
| Geometric mean | (ref)                                                           | 1.18x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 234 ms: 1.46x faster                                                          |
| async_tree_none_tg         | 301 ms                                                          | 209 ms: 1.44x faster                                                          |
| async_tree_memoization     | 408 ms                                                          | 285 ms: 1.43x faster                                                          |
| async_tree_memoization_tg  | 378 ms                                                          | 264 ms: 1.43x faster                                                          |
| async_tree_io              | 754 ms                                                          | 548 ms: 1.38x faster                                                          |
| async_tree_io_tg           | 746 ms                                                          | 547 ms: 1.36x faster                                                          |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 450 ms: 1.28x faster                                                          |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 473 ms: 1.25x faster                                                          |
| Geometric mean             | (ref)                                                           | 1.38x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 76.1 ms                                                         | 53.6 ms: 1.42x faster                                                         |
| nbody          | 126 ms                                                          | 92.1 ms: 1.37x faster                                                         |
| pidigits       | 203 ms                                                          | 202 ms: 1.00x faster                                                          |
| Geometric mean | (ref)                                                           | 1.25x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 115 ms: 1.28x faster                                                          |
| regex_dna      | 122 ms                                                          | 119 ms: 1.02x faster                                                          |
| regex_effbot   | 1.82 ms                                                         | 1.92 ms: 1.05x slower                                                         |
| regex_v8       | 15.2 ms                                                         | 16.2 ms: 1.07x slower                                                         |
| Geometric mean | (ref)                                                           | 1.04x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 9.80 ms                                                         | 6.70 ms: 1.46x faster                                                         |
| pickle_pure_python   | 309 us                                                          | 221 us: 1.40x faster                                                          |
| unpickle_pure_python | 231 us                                                          | 166 us: 1.39x faster                                                          |
| tomli_loads          | 2.31 sec                                                        | 1.67 sec: 1.39x faster                                                        |
| xml_etree_process    | 55.0 ms                                                         | 42.6 ms: 1.29x faster                                                         |
| xml_etree_generate   | 71.6 ms                                                         | 60.8 ms: 1.18x faster                                                         |
| xml_etree_iterparse  | 75.6 ms                                                         | 64.8 ms: 1.17x faster                                                         |
| unpickle_list        | 3.28 us                                                         | 2.90 us: 1.13x faster                                                         |
| xml_etree_parse      | 114 ms                                                          | 108 ms: 1.06x faster                                                          |
| pickle_list          | 3.27 us                                                         | 3.18 us: 1.03x faster                                                         |
| pickle_dict          | 20.1 us                                                         | 19.6 us: 1.02x faster                                                         |
| json_loads           | 20.0 us                                                         | 20.1 us: 1.00x slower                                                         |
| pickle               | 7.99 us                                                         | 8.04 us: 1.01x slower                                                         |
| unpickle             | 9.23 us                                                         | 9.81 us: 1.06x slower                                                         |
| Geometric mean       | (ref)                                                           | 1.16x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                         | 24.2 ms: 1.10x slower                                                         |
| python_startup_no_site | 18.8 ms                                                         | 21.8 ms: 1.16x slower                                                         |
| Geometric mean         | (ref)                                                           | 1.13x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 7.05 ms: 1.46x faster                                                         |
| genshi_xml      | 61.2 ms                                                         | 47.0 ms: 1.30x faster                                                         |
| genshi_text     | 26.8 ms                                                         | 20.8 ms: 1.29x faster                                                         |
| django_template | 37.4 ms                                                         | 33.0 ms: 1.13x faster                                                         |
| Geometric mean  | (ref)                                                           | 1.29x faster                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 95.3 us: 5.02x faster                                                         |
| generators                 | 52.2 ms                                                         | 23.2 ms: 2.25x faster                                                         |
| logging_silent             | 119 ns                                                          | 60.7 ns: 1.96x faster                                                         |
| pylint                     | 418 ms                                                          | 222 ms: 1.88x faster                                                          |
| spectral_norm              | 122 ms                                                          | 70.4 ms: 1.73x faster                                                         |
| deltablue                  | 4.10 ms                                                         | 2.55 ms: 1.61x faster                                                         |
| coroutines                 | 23.7 ms                                                         | 14.9 ms: 1.59x faster                                                         |
| deepcopy_memo              | 40.0 us                                                         | 25.5 us: 1.57x faster                                                         |
| sqlglot_parse              | 1.49 ms                                                         | 983 us: 1.52x faster                                                          |
| async_tree_none            | 343 ms                                                          | 234 ms: 1.46x faster                                                          |
| json_dumps                 | 9.80 ms                                                         | 6.70 ms: 1.46x faster                                                         |
| comprehensions             | 22.1 us                                                         | 15.1 us: 1.46x faster                                                         |
| mako                       | 10.3 ms                                                         | 7.05 ms: 1.46x faster                                                         |
| sqlglot_transpile          | 1.78 ms                                                         | 1.24 ms: 1.44x faster                                                         |
| async_tree_none_tg         | 301 ms                                                          | 209 ms: 1.44x faster                                                          |
| async_tree_memoization     | 408 ms                                                          | 285 ms: 1.43x faster                                                          |
| async_tree_memoization_tg  | 378 ms                                                          | 264 ms: 1.43x faster                                                          |
| unpack_sequence            | 65.2 ns                                                         | 45.9 ns: 1.42x faster                                                         |
| float                      | 76.1 ms                                                         | 53.6 ms: 1.42x faster                                                         |
| scimark_sor                | 135 ms                                                          | 95.6 ms: 1.41x faster                                                         |
| pickle_pure_python         | 309 us                                                          | 221 us: 1.40x faster                                                          |
| richards_super             | 58.7 ms                                                         | 42.1 ms: 1.39x faster                                                         |
| unpickle_pure_python       | 231 us                                                          | 166 us: 1.39x faster                                                          |
| tomli_loads                | 2.31 sec                                                        | 1.67 sec: 1.39x faster                                                        |
| async_tree_io              | 754 ms                                                          | 548 ms: 1.38x faster                                                          |
| nbody                      | 126 ms                                                          | 92.1 ms: 1.37x faster                                                         |
| chaos                      | 84.4 ms                                                         | 61.8 ms: 1.37x faster                                                         |
| sympy_sum                  | 149 ms                                                          | 109 ms: 1.37x faster                                                          |
| async_tree_io_tg           | 746 ms                                                          | 547 ms: 1.36x faster                                                          |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 3.12 ms: 1.36x faster                                                         |
| richards                   | 48.8 ms                                                         | 37.0 ms: 1.32x faster                                                         |
| sympy_str                  | 283 ms                                                          | 216 ms: 1.31x faster                                                          |
| genshi_xml                 | 61.2 ms                                                         | 47.0 ms: 1.30x faster                                                         |
| chameleon                  | 8.08 ms                                                         | 6.20 ms: 1.30x faster                                                         |
| deepcopy                   | 381 us                                                          | 294 us: 1.30x faster                                                          |
| logging_simple             | 10.8 us                                                         | 8.34 us: 1.30x faster                                                         |
| pyflate                    | 471 ms                                                          | 364 ms: 1.29x faster                                                          |
| xml_etree_process          | 55.0 ms                                                         | 42.6 ms: 1.29x faster                                                         |
| genshi_text                | 26.8 ms                                                         | 20.8 ms: 1.29x faster                                                         |
| logging_format             | 11.5 us                                                         | 8.92 us: 1.28x faster                                                         |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 450 ms: 1.28x faster                                                          |
| regex_compile              | 148 ms                                                          | 115 ms: 1.28x faster                                                          |
| deepcopy_reduce            | 3.32 us                                                         | 2.62 us: 1.26x faster                                                         |
| asyncio_tcp                | 787 ms                                                          | 623 ms: 1.26x faster                                                          |
| fannkuch                   | 399 ms                                                          | 317 ms: 1.26x faster                                                          |
| crypto_pyaes               | 79.4 ms                                                         | 63.2 ms: 1.26x faster                                                         |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 473 ms: 1.25x faster                                                          |
| raytrace                   | 327 ms                                                          | 265 ms: 1.24x faster                                                          |
| scimark_fft                | 291 ms                                                          | 236 ms: 1.23x faster                                                          |
| nqueens                    | 111 ms                                                          | 90.5 ms: 1.23x faster                                                         |
| sympy_integrate            | 19.9 ms                                                         | 16.2 ms: 1.23x faster                                                         |
| sympy_expand               | 462 ms                                                          | 377 ms: 1.23x faster                                                          |
| tornado_http               | 118 ms                                                          | 96.9 ms: 1.22x faster                                                         |
| go                         | 147 ms                                                          | 121 ms: 1.22x faster                                                          |
| pycparser                  | 1.04 sec                                                        | 865 ms: 1.21x faster                                                          |
| html5lib                   | 54.3 ms                                                         | 45.5 ms: 1.19x faster                                                         |
| scimark_lu                 | 102 ms                                                          | 86.1 ms: 1.19x faster                                                         |
| hexiom                     | 7.51 ms                                                         | 6.36 ms: 1.18x faster                                                         |
| xml_etree_generate         | 71.6 ms                                                         | 60.8 ms: 1.18x faster                                                         |
| mdp                        | 2.07 sec                                                        | 1.76 sec: 1.17x faster                                                        |
| xml_etree_iterparse        | 75.6 ms                                                         | 64.8 ms: 1.17x faster                                                         |
| pprint_pformat             | 1.70 sec                                                        | 1.48 sec: 1.14x faster                                                        |
| json                       | 4.78 ms                                                         | 4.19 ms: 1.14x faster                                                         |
| sqlglot_optimize           | 51.8 ms                                                         | 45.7 ms: 1.14x faster                                                         |
| scimark_monte_carlo        | 70.8 ms                                                         | 62.5 ms: 1.13x faster                                                         |
| django_template            | 37.4 ms                                                         | 33.0 ms: 1.13x faster                                                         |
| unpickle_list              | 3.28 us                                                         | 2.90 us: 1.13x faster                                                         |
| bench_thread_pool          | 1.14 ms                                                         | 1.01 ms: 1.13x faster                                                         |
| pprint_safe_repr           | 819 ms                                                          | 727 ms: 1.13x faster                                                          |
| sqlite_synth               | 2.15 us                                                         | 1.92 us: 1.12x faster                                                         |
| 2to3                       | 282 ms                                                          | 252 ms: 1.12x faster                                                          |
| meteor_contest             | 90.9 ms                                                         | 81.6 ms: 1.11x faster                                                         |
| docutils                   | 2.10 sec                                                        | 1.93 sec: 1.09x faster                                                        |
| xml_etree_parse            | 114 ms                                                          | 108 ms: 1.06x faster                                                          |
| pickle_list                | 3.27 us                                                         | 3.18 us: 1.03x faster                                                         |
| pickle_dict                | 20.1 us                                                         | 19.6 us: 1.02x faster                                                         |
| regex_dna                  | 122 ms                                                          | 119 ms: 1.02x faster                                                          |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.8 sec: 1.02x faster                                                        |
| pidigits                   | 203 ms                                                          | 202 ms: 1.00x faster                                                          |
| json_loads                 | 20.0 us                                                         | 20.1 us: 1.00x slower                                                         |
| pickle                     | 7.99 us                                                         | 8.04 us: 1.01x slower                                                         |
| bench_mp_pool              | 70.9 ms                                                         | 72.1 ms: 1.02x slower                                                         |
| gc_traversal               | 1.38 ms                                                         | 1.44 ms: 1.05x slower                                                         |
| regex_effbot               | 1.82 ms                                                         | 1.92 ms: 1.05x slower                                                         |
| unpickle                   | 9.23 us                                                         | 9.81 us: 1.06x slower                                                         |
| regex_v8                   | 15.2 ms                                                         | 16.2 ms: 1.07x slower                                                         |
| pathlib                    | 79.9 ms                                                         | 86.7 ms: 1.09x slower                                                         |
| python_startup             | 22.0 ms                                                         | 24.2 ms: 1.10x slower                                                         |
| async_generators           | 260 ms                                                          | 294 ms: 1.13x slower                                                          |
| python_startup_no_site     | 18.8 ms                                                         | 21.8 ms: 1.16x slower                                                         |
| create_gc_cycles           | 618 us                                                          | 738 us: 1.19x slower                                                          |
| telco                      | 5.29 ms                                                         | 6.41 ms: 1.21x slower                                                         |
| sqlglot_normalize          | 113 ms                                                          | 238 ms: 2.10x slower                                                          |
| coverage                   | 58.0 ms                                                         | 477 ms: 8.22x slower                                                          |
| thrift                     | 801 us                                                          | 11.2 ms: 14.03x slower                                                        |
| Geometric mean             | (ref)                                                           | 1.17x faster                                                                  |
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.20x
- 95% likely to have a speedup of 1.19x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: unknown