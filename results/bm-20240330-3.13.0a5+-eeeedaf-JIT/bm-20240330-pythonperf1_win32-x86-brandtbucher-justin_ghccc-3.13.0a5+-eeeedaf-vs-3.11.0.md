# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_ghccc
- machine: windows-x86
- commit hash: eeeedaf
- commit date: 2024-03-30
- overall geometric mean: 1.27x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 282 ms                                                          | 242 ms: 1.17x faster                                                          |
| chameleon      | 8.08 ms                                                         | 5.89 ms: 1.37x faster                                                         |
| docutils       | 2.10 sec                                                        | 1.84 sec: 1.14x faster                                                        |
| html5lib       | 54.3 ms                                                         | 44.1 ms: 1.23x faster                                                         |
| tornado_http   | 118 ms                                                          | 95.7 ms: 1.24x faster                                                         |
| Geometric mean | (ref)                                                           | 1.23x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none            | 343 ms                                                          | 219 ms: 1.56x faster                                                          |
| async_tree_none_tg         | 301 ms                                                          | 198 ms: 1.52x faster                                                          |
| async_tree_memoization     | 408 ms                                                          | 271 ms: 1.50x faster                                                          |
| async_tree_memoization_tg  | 378 ms                                                          | 253 ms: 1.49x faster                                                          |
| async_tree_io              | 754 ms                                                          | 523 ms: 1.44x faster                                                          |
| async_tree_io_tg           | 746 ms                                                          | 523 ms: 1.43x faster                                                          |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 459 ms: 1.29x faster                                                          |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 450 ms: 1.28x faster                                                          |
| Geometric mean             | (ref)                                                           | 1.44x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 126 ms                                                          | 53.7 ms: 2.35x faster                                                         |
| float          | 76.1 ms                                                         | 43.4 ms: 1.75x faster                                                         |
| pidigits       | 203 ms                                                          | 196 ms: 1.03x faster                                                          |
| Geometric mean | (ref)                                                           | 1.62x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                          | 98.7 ms: 1.49x faster                                                         |
| regex_dna      | 122 ms                                                          | 118 ms: 1.03x faster                                                          |
| regex_effbot   | 1.82 ms                                                         | 1.91 ms: 1.04x slower                                                         |
| regex_v8       | 15.2 ms                                                         | 16.0 ms: 1.05x slower                                                         |
| Geometric mean | (ref)                                                           | 1.09x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| unpickle_pure_python | 231 us                                                          | 139 us: 1.66x faster                                                          |
| tomli_loads          | 2.31 sec                                                        | 1.45 sec: 1.60x faster                                                        |
| json_dumps           | 9.80 ms                                                         | 6.72 ms: 1.46x faster                                                         |
| pickle_pure_python   | 309 us                                                          | 218 us: 1.42x faster                                                          |
| xml_etree_process    | 55.0 ms                                                         | 41.7 ms: 1.32x faster                                                         |
| xml_etree_generate   | 71.6 ms                                                         | 58.4 ms: 1.23x faster                                                         |
| xml_etree_iterparse  | 75.6 ms                                                         | 62.1 ms: 1.22x faster                                                         |
| unpickle_list        | 3.28 us                                                         | 2.97 us: 1.10x faster                                                         |
| xml_etree_parse      | 114 ms                                                          | 107 ms: 1.07x faster                                                          |
| pickle               | 7.99 us                                                         | 7.67 us: 1.04x faster                                                         |
| pickle_dict          | 20.1 us                                                         | 19.7 us: 1.02x faster                                                         |
| pickle_list          | 3.27 us                                                         | 3.20 us: 1.02x faster                                                         |
| json_loads           | 20.0 us                                                         | 20.4 us: 1.02x slower                                                         |
| unpickle             | 9.23 us                                                         | 9.80 us: 1.06x slower                                                         |
| Geometric mean       | (ref)                                                           | 1.20x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                         | 24.3 ms: 1.10x slower                                                         |
| python_startup_no_site | 18.8 ms                                                         | 21.8 ms: 1.16x slower                                                         |
| Geometric mean         | (ref)                                                           | 1.13x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 10.3 ms                                                         | 5.42 ms: 1.90x faster                                                         |
| genshi_xml      | 61.2 ms                                                         | 45.6 ms: 1.34x faster                                                         |
| genshi_text     | 26.8 ms                                                         | 20.1 ms: 1.33x faster                                                         |
| django_template | 37.4 ms                                                         | 31.3 ms: 1.20x faster                                                         |
| Geometric mean  | (ref)                                                           | 1.42x faster                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 478 us                                                          | 90.3 us: 5.30x faster                                                         |
| spectral_norm              | 122 ms                                                          | 50.4 ms: 2.41x faster                                                         |
| nbody                      | 126 ms                                                          | 53.7 ms: 2.35x faster                                                         |
| generators                 | 52.2 ms                                                         | 23.1 ms: 2.26x faster                                                         |
| logging_silent             | 119 ns                                                          | 59.4 ns: 2.01x faster                                                         |
| comprehensions             | 22.1 us                                                         | 11.2 us: 1.97x faster                                                         |
| pylint                     | 418 ms                                                          | 215 ms: 1.94x faster                                                          |
| mako                       | 10.3 ms                                                         | 5.42 ms: 1.90x faster                                                         |
| fannkuch                   | 399 ms                                                          | 223 ms: 1.79x faster                                                          |
| scimark_monte_carlo        | 70.8 ms                                                         | 39.8 ms: 1.78x faster                                                         |
| float                      | 76.1 ms                                                         | 43.4 ms: 1.75x faster                                                         |
| deltablue                  | 4.10 ms                                                         | 2.38 ms: 1.72x faster                                                         |
| scimark_fft                | 291 ms                                                          | 171 ms: 1.70x faster                                                          |
| pyflate                    | 471 ms                                                          | 280 ms: 1.68x faster                                                          |
| scimark_sparse_mat_mult    | 4.23 ms                                                         | 2.54 ms: 1.67x faster                                                         |
| crypto_pyaes               | 79.4 ms                                                         | 47.7 ms: 1.67x faster                                                         |
| unpickle_pure_python       | 231 us                                                          | 139 us: 1.66x faster                                                          |
| deepcopy_memo              | 40.0 us                                                         | 24.5 us: 1.64x faster                                                         |
| hexiom                     | 7.51 ms                                                         | 4.61 ms: 1.63x faster                                                         |
| sqlglot_parse              | 1.49 ms                                                         | 923 us: 1.62x faster                                                          |
| coroutines                 | 23.7 ms                                                         | 14.7 ms: 1.61x faster                                                         |
| tomli_loads                | 2.31 sec                                                        | 1.45 sec: 1.60x faster                                                        |
| chaos                      | 84.4 ms                                                         | 53.1 ms: 1.59x faster                                                         |
| scimark_sor                | 135 ms                                                          | 85.6 ms: 1.58x faster                                                         |
| async_tree_none            | 343 ms                                                          | 219 ms: 1.56x faster                                                          |
| nqueens                    | 111 ms                                                          | 71.7 ms: 1.55x faster                                                         |
| richards_super             | 58.7 ms                                                         | 37.8 ms: 1.55x faster                                                         |
| sqlglot_transpile          | 1.78 ms                                                         | 1.17 ms: 1.53x faster                                                         |
| async_tree_none_tg         | 301 ms                                                          | 198 ms: 1.52x faster                                                          |
| async_tree_memoization     | 408 ms                                                          | 271 ms: 1.50x faster                                                          |
| regex_compile              | 148 ms                                                          | 98.7 ms: 1.49x faster                                                         |
| async_tree_memoization_tg  | 378 ms                                                          | 253 ms: 1.49x faster                                                          |
| raytrace                   | 327 ms                                                          | 220 ms: 1.49x faster                                                          |
| pprint_pformat             | 1.70 sec                                                        | 1.16 sec: 1.46x faster                                                        |
| json_dumps                 | 9.80 ms                                                         | 6.72 ms: 1.46x faster                                                         |
| async_tree_io              | 754 ms                                                          | 523 ms: 1.44x faster                                                          |
| pprint_safe_repr           | 819 ms                                                          | 569 ms: 1.44x faster                                                          |
| richards                   | 48.8 ms                                                         | 34.0 ms: 1.43x faster                                                         |
| sympy_sum                  | 149 ms                                                          | 104 ms: 1.43x faster                                                          |
| async_tree_io_tg           | 746 ms                                                          | 523 ms: 1.43x faster                                                          |
| pickle_pure_python         | 309 us                                                          | 218 us: 1.42x faster                                                          |
| sympy_str                  | 283 ms                                                          | 203 ms: 1.39x faster                                                          |
| logging_simple             | 10.8 us                                                         | 7.81 us: 1.38x faster                                                         |
| chameleon                  | 8.08 ms                                                         | 5.89 ms: 1.37x faster                                                         |
| scimark_lu                 | 102 ms                                                          | 75.2 ms: 1.36x faster                                                         |
| logging_format             | 11.5 us                                                         | 8.43 us: 1.36x faster                                                         |
| genshi_xml                 | 61.2 ms                                                         | 45.6 ms: 1.34x faster                                                         |
| go                         | 147 ms                                                          | 110 ms: 1.34x faster                                                          |
| genshi_text                | 26.8 ms                                                         | 20.1 ms: 1.33x faster                                                         |
| sympy_integrate            | 19.9 ms                                                         | 15.0 ms: 1.32x faster                                                         |
| deepcopy                   | 381 us                                                          | 288 us: 1.32x faster                                                          |
| xml_etree_process          | 55.0 ms                                                         | 41.7 ms: 1.32x faster                                                         |
| pycparser                  | 1.04 sec                                                        | 799 ms: 1.31x faster                                                          |
| deepcopy_reduce            | 3.32 us                                                         | 2.54 us: 1.31x faster                                                         |
| async_tree_cpu_io_mixed    | 590 ms                                                          | 459 ms: 1.29x faster                                                          |
| sympy_expand               | 462 ms                                                          | 359 ms: 1.29x faster                                                          |
| async_tree_cpu_io_mixed_tg | 577 ms                                                          | 450 ms: 1.28x faster                                                          |
| mdp                        | 2.07 sec                                                        | 1.62 sec: 1.27x faster                                                        |
| asyncio_tcp                | 787 ms                                                          | 619 ms: 1.27x faster                                                          |
| sqlglot_optimize           | 51.8 ms                                                         | 41.6 ms: 1.25x faster                                                         |
| tornado_http               | 118 ms                                                          | 95.7 ms: 1.24x faster                                                         |
| html5lib                   | 54.3 ms                                                         | 44.1 ms: 1.23x faster                                                         |
| meteor_contest             | 90.9 ms                                                         | 73.8 ms: 1.23x faster                                                         |
| xml_etree_generate         | 71.6 ms                                                         | 58.4 ms: 1.23x faster                                                         |
| xml_etree_iterparse        | 75.6 ms                                                         | 62.1 ms: 1.22x faster                                                         |
| django_template            | 37.4 ms                                                         | 31.3 ms: 1.20x faster                                                         |
| 2to3                       | 282 ms                                                          | 242 ms: 1.17x faster                                                          |
| bench_thread_pool          | 1.14 ms                                                         | 990 us: 1.15x faster                                                          |
| sqlite_synth               | 2.15 us                                                         | 1.87 us: 1.15x faster                                                         |
| docutils                   | 2.10 sec                                                        | 1.84 sec: 1.14x faster                                                        |
| unpickle_list              | 3.28 us                                                         | 2.97 us: 1.10x faster                                                         |
| json                       | 4.78 ms                                                         | 4.37 ms: 1.10x faster                                                         |
| xml_etree_parse            | 114 ms                                                          | 107 ms: 1.07x faster                                                          |
| pickle                     | 7.99 us                                                         | 7.67 us: 1.04x faster                                                         |
| pidigits                   | 203 ms                                                          | 196 ms: 1.03x faster                                                          |
| regex_dna                  | 122 ms                                                          | 118 ms: 1.03x faster                                                          |
| pickle_dict                | 20.1 us                                                         | 19.7 us: 1.02x faster                                                         |
| pickle_list                | 3.27 us                                                         | 3.20 us: 1.02x faster                                                         |
| asyncio_tcp_ssl            | 17.1 sec                                                        | 16.8 sec: 1.02x faster                                                        |
| bench_mp_pool              | 70.9 ms                                                         | 71.7 ms: 1.01x slower                                                         |
| json_loads                 | 20.0 us                                                         | 20.4 us: 1.02x slower                                                         |
| regex_effbot               | 1.82 ms                                                         | 1.91 ms: 1.04x slower                                                         |
| regex_v8                   | 15.2 ms                                                         | 16.0 ms: 1.05x slower                                                         |
| gc_traversal               | 1.38 ms                                                         | 1.45 ms: 1.06x slower                                                         |
| unpickle                   | 9.23 us                                                         | 9.80 us: 1.06x slower                                                         |
| pathlib                    | 79.9 ms                                                         | 85.8 ms: 1.07x slower                                                         |
| unpack_sequence            | 65.2 ns                                                         | 70.2 ns: 1.08x slower                                                         |
| async_generators           | 260 ms                                                          | 283 ms: 1.09x slower                                                          |
| python_startup             | 22.0 ms                                                         | 24.3 ms: 1.10x slower                                                         |
| telco                      | 5.29 ms                                                         | 5.87 ms: 1.11x slower                                                         |
| python_startup_no_site     | 18.8 ms                                                         | 21.8 ms: 1.16x slower                                                         |
| create_gc_cycles           | 618 us                                                          | 734 us: 1.19x slower                                                          |
| sqlglot_normalize          | 113 ms                                                          | 215 ms: 1.90x slower                                                          |
| coverage                   | 58.0 ms                                                         | 486 ms: 8.37x slower                                                          |
| thrift                     | 801 us                                                          | 10.6 ms: 13.28x slower                                                        |
| Geometric mean             | (ref)                                                           | 1.27x faster                                                                  |
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1_win32-x86-python-v3.11.0-3.11.0-deaf509.json: aiohttp, dask, dulwich_log, flaskblogging, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.31x
- 95% likely to have a speedup of 1.30x
- 99% likely to have a speedup of 1.27x

# Memory
- memory change: unknown