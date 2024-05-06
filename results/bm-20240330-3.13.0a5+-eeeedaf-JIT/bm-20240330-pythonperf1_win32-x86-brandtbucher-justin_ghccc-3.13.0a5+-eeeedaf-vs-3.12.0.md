# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_ghccc
- machine: windows-x86
- commit hash: eeeedaf
- commit date: 2024-03-30
- overall geometric mean: 1.20x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.17x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 280 ms                                                          | 242 ms: 1.16x faster                                                          |
| chameleon      | 7.75 ms                                                         | 5.89 ms: 1.32x faster                                                         |
| docutils       | 1.98 sec                                                        | 1.84 sec: 1.08x faster                                                        |
| tornado_http   | 105 ms                                                          | 95.7 ms: 1.10x faster                                                         |
| Geometric mean | (ref)                                                           | 1.16x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none_tg         | 278 ms                                                          | 198 ms: 1.40x faster                                                          |
| async_tree_memoization_tg  | 350 ms                                                          | 253 ms: 1.39x faster                                                          |
| async_tree_none            | 298 ms                                                          | 219 ms: 1.36x faster                                                          |
| async_tree_memoization     | 364 ms                                                          | 271 ms: 1.34x faster                                                          |
| async_tree_io              | 693 ms                                                          | 523 ms: 1.33x faster                                                          |
| async_tree_io_tg           | 677 ms                                                          | 523 ms: 1.29x faster                                                          |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 459 ms: 1.23x faster                                                          |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 450 ms: 1.21x faster                                                          |
| Geometric mean             | (ref)                                                           | 1.32x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 127 ms                                                          | 53.7 ms: 2.36x faster                                                         |
| float          | 76.7 ms                                                         | 43.4 ms: 1.77x faster                                                         |
| pidigits       | 199 ms                                                          | 196 ms: 1.02x faster                                                          |
| Geometric mean | (ref)                                                           | 1.62x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 129 ms                                                          | 98.7 ms: 1.31x faster                                                         |
| regex_dna      | 127 ms                                                          | 118 ms: 1.07x faster                                                          |
| regex_effbot   | 2.04 ms                                                         | 1.91 ms: 1.07x faster                                                         |
| regex_v8       | 15.0 ms                                                         | 16.0 ms: 1.06x slower                                                         |
| Geometric mean | (ref)                                                           | 1.09x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| tomli_loads          | 2.20 sec                                                        | 1.45 sec: 1.52x faster                                                        |
| unpickle_pure_python | 210 us                                                          | 139 us: 1.51x faster                                                          |
| pickle_pure_python   | 286 us                                                          | 218 us: 1.31x faster                                                          |
| xml_etree_process    | 53.2 ms                                                         | 41.7 ms: 1.28x faster                                                         |
| xml_etree_iterparse  | 77.6 ms                                                         | 62.1 ms: 1.25x faster                                                         |
| xml_etree_generate   | 72.1 ms                                                         | 58.4 ms: 1.24x faster                                                         |
| json_dumps           | 7.40 ms                                                         | 6.72 ms: 1.10x faster                                                         |
| xml_etree_parse      | 113 ms                                                          | 107 ms: 1.06x faster                                                          |
| pickle_list          | 3.37 us                                                         | 3.20 us: 1.05x faster                                                         |
| pickle               | 7.79 us                                                         | 7.67 us: 1.02x faster                                                         |
| pickle_dict          | 19.9 us                                                         | 19.7 us: 1.01x faster                                                         |
| unpickle             | 9.71 us                                                         | 9.80 us: 1.01x slower                                                         |
| Geometric mean       | (ref)                                                           | 1.15x faster                                                                  |

Benchmark hidden because not significant (2): json_loads, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 22.4 ms                                                         | 24.3 ms: 1.09x slower                                                         |
| python_startup_no_site | 19.1 ms                                                         | 21.8 ms: 1.14x slower                                                         |
| Geometric mean         | (ref)                                                           | 1.11x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-----------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 9.96 ms                                                         | 5.42 ms: 1.84x faster                                                         |
| django_template | 36.9 ms                                                         | 31.3 ms: 1.18x faster                                                         |
| Geometric mean  | (ref)                                                           | 1.47x faster                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------------|:---------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody                      | 127 ms                                                          | 53.7 ms: 2.36x faster                                                         |
| spectral_norm              | 104 ms                                                          | 50.4 ms: 2.06x faster                                                         |
| mako                       | 9.96 ms                                                         | 5.42 ms: 1.84x faster                                                         |
| float                      | 76.7 ms                                                         | 43.4 ms: 1.77x faster                                                         |
| comprehensions             | 19.2 us                                                         | 11.2 us: 1.71x faster                                                         |
| logging_silent             | 101 ns                                                          | 59.4 ns: 1.70x faster                                                         |
| scimark_monte_carlo        | 66.4 ms                                                         | 39.8 ms: 1.67x faster                                                         |
| generators                 | 38.5 ms                                                         | 23.1 ms: 1.66x faster                                                         |
| fannkuch                   | 354 ms                                                          | 223 ms: 1.58x faster                                                          |
| scimark_fft                | 271 ms                                                          | 171 ms: 1.58x faster                                                          |
| deepcopy_memo              | 38.4 us                                                         | 24.5 us: 1.57x faster                                                         |
| scimark_sparse_mat_mult    | 3.86 ms                                                         | 2.54 ms: 1.52x faster                                                         |
| scimark_sor                | 130 ms                                                          | 85.6 ms: 1.52x faster                                                         |
| tomli_loads                | 2.20 sec                                                        | 1.45 sec: 1.52x faster                                                        |
| pyflate                    | 424 ms                                                          | 280 ms: 1.51x faster                                                          |
| unpickle_pure_python       | 210 us                                                          | 139 us: 1.51x faster                                                          |
| deltablue                  | 3.58 ms                                                         | 2.38 ms: 1.50x faster                                                         |
| hexiom                     | 6.82 ms                                                         | 4.61 ms: 1.48x faster                                                         |
| crypto_pyaes               | 69.2 ms                                                         | 47.7 ms: 1.45x faster                                                         |
| coroutines                 | 20.9 ms                                                         | 14.7 ms: 1.42x faster                                                         |
| raytrace                   | 308 ms                                                          | 220 ms: 1.40x faster                                                          |
| async_tree_none_tg         | 278 ms                                                          | 198 ms: 1.40x faster                                                          |
| typing_runtime_protocols   | 126 us                                                          | 90.3 us: 1.40x faster                                                         |
| async_tree_memoization_tg  | 350 ms                                                          | 253 ms: 1.39x faster                                                          |
| async_tree_none            | 298 ms                                                          | 219 ms: 1.36x faster                                                          |
| sqlglot_parse              | 1.25 ms                                                         | 923 us: 1.35x faster                                                          |
| async_tree_memoization     | 364 ms                                                          | 271 ms: 1.34x faster                                                          |
| async_tree_io              | 693 ms                                                          | 523 ms: 1.33x faster                                                          |
| chameleon                  | 7.75 ms                                                         | 5.89 ms: 1.32x faster                                                         |
| pickle_pure_python         | 286 us                                                          | 218 us: 1.31x faster                                                          |
| sqlglot_transpile          | 1.53 ms                                                         | 1.17 ms: 1.31x faster                                                         |
| regex_compile              | 129 ms                                                          | 98.7 ms: 1.31x faster                                                         |
| nqueens                    | 93.7 ms                                                         | 71.7 ms: 1.31x faster                                                         |
| chaos                      | 69.4 ms                                                         | 53.1 ms: 1.31x faster                                                         |
| pprint_pformat             | 1.50 sec                                                        | 1.16 sec: 1.29x faster                                                        |
| async_tree_io_tg           | 677 ms                                                          | 523 ms: 1.29x faster                                                          |
| xml_etree_process          | 53.2 ms                                                         | 41.7 ms: 1.28x faster                                                         |
| deepcopy_reduce            | 3.23 us                                                         | 2.54 us: 1.27x faster                                                         |
| pprint_safe_repr           | 721 ms                                                          | 569 ms: 1.27x faster                                                          |
| go                         | 137 ms                                                          | 110 ms: 1.25x faster                                                          |
| xml_etree_iterparse        | 77.6 ms                                                         | 62.1 ms: 1.25x faster                                                         |
| deepcopy                   | 360 us                                                          | 288 us: 1.25x faster                                                          |
| logging_simple             | 9.75 us                                                         | 7.81 us: 1.25x faster                                                         |
| scimark_lu                 | 93.2 ms                                                         | 75.2 ms: 1.24x faster                                                         |
| xml_etree_generate         | 72.1 ms                                                         | 58.4 ms: 1.24x faster                                                         |
| logging_format             | 10.4 us                                                         | 8.43 us: 1.23x faster                                                         |
| async_tree_cpu_io_mixed    | 564 ms                                                          | 459 ms: 1.23x faster                                                          |
| richards_super             | 46.5 ms                                                         | 37.8 ms: 1.23x faster                                                         |
| pycparser                  | 978 ms                                                          | 799 ms: 1.22x faster                                                          |
| richards                   | 41.3 ms                                                         | 34.0 ms: 1.22x faster                                                         |
| async_tree_cpu_io_mixed_tg | 546 ms                                                          | 450 ms: 1.21x faster                                                          |
| django_template            | 36.9 ms                                                         | 31.3 ms: 1.18x faster                                                         |
| mdp                        | 1.91 sec                                                        | 1.62 sec: 1.18x faster                                                        |
| sympy_str                  | 240 ms                                                          | 203 ms: 1.18x faster                                                          |
| sympy_sum                  | 123 ms                                                          | 104 ms: 1.18x faster                                                          |
| meteor_contest             | 86.9 ms                                                         | 73.8 ms: 1.18x faster                                                         |
| sympy_integrate            | 17.5 ms                                                         | 15.0 ms: 1.17x faster                                                         |
| sqlglot_optimize           | 48.5 ms                                                         | 41.6 ms: 1.16x faster                                                         |
| 2to3                       | 280 ms                                                          | 242 ms: 1.16x faster                                                          |
| bench_thread_pool          | 1.10 ms                                                         | 990 us: 1.11x faster                                                          |
| sympy_expand               | 398 ms                                                          | 359 ms: 1.11x faster                                                          |
| sqlite_synth               | 2.07 us                                                         | 1.87 us: 1.11x faster                                                         |
| async_generators           | 313 ms                                                          | 283 ms: 1.11x faster                                                          |
| json_dumps                 | 7.40 ms                                                         | 6.72 ms: 1.10x faster                                                         |
| tornado_http               | 105 ms                                                          | 95.7 ms: 1.10x faster                                                         |
| docutils                   | 1.98 sec                                                        | 1.84 sec: 1.08x faster                                                        |
| regex_dna                  | 127 ms                                                          | 118 ms: 1.07x faster                                                          |
| asyncio_tcp                | 662 ms                                                          | 619 ms: 1.07x faster                                                          |
| regex_effbot               | 2.04 ms                                                         | 1.91 ms: 1.07x faster                                                         |
| pathlib                    | 91.4 ms                                                         | 85.8 ms: 1.07x faster                                                         |
| xml_etree_parse            | 113 ms                                                          | 107 ms: 1.06x faster                                                          |
| asyncio_tcp_ssl            | 17.7 sec                                                        | 16.8 sec: 1.05x faster                                                        |
| bench_mp_pool              | 75.4 ms                                                         | 71.7 ms: 1.05x faster                                                         |
| pickle_list                | 3.37 us                                                         | 3.20 us: 1.05x faster                                                         |
| pickle                     | 7.79 us                                                         | 7.67 us: 1.02x faster                                                         |
| pidigits                   | 199 ms                                                          | 196 ms: 1.02x faster                                                          |
| pickle_dict                | 19.9 us                                                         | 19.7 us: 1.01x faster                                                         |
| gc_traversal               | 1.44 ms                                                         | 1.45 ms: 1.01x slower                                                         |
| unpickle                   | 9.71 us                                                         | 9.80 us: 1.01x slower                                                         |
| json                       | 4.15 ms                                                         | 4.37 ms: 1.05x slower                                                         |
| regex_v8                   | 15.0 ms                                                         | 16.0 ms: 1.06x slower                                                         |
| telco                      | 5.51 ms                                                         | 5.87 ms: 1.06x slower                                                         |
| python_startup             | 22.4 ms                                                         | 24.3 ms: 1.09x slower                                                         |
| unpack_sequence            | 62.5 ns                                                         | 70.2 ns: 1.12x slower                                                         |
| create_gc_cycles           | 652 us                                                          | 734 us: 1.13x slower                                                          |
| python_startup_no_site     | 19.1 ms                                                         | 21.8 ms: 1.14x slower                                                         |
| sqlglot_normalize          | 100 ms                                                          | 215 ms: 2.14x slower                                                          |
| coverage                   | 48.4 ms                                                         | 486 ms: 10.03x slower                                                         |
| Geometric mean             | (ref)                                                           | 1.20x faster                                                                  |

Benchmark hidden because not significant (2): json_loads, unpickle_list
Ignored benchmarks (6) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf1_win32-x86-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, dask, dulwich_log, mypy2, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240330-3.13.0a5+-eeeedaf-JIT/bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.21x
- 95% likely to have a speedup of 1.19x
- 99% likely to have a speedup of 1.17x

# Memory
- memory change: unknown