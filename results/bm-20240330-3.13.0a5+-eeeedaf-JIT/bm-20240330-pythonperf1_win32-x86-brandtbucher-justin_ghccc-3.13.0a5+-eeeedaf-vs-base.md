# Results vs. base

- fork: brandtbucher
- ref: justin_ghccc
- machine: windows-x86
- commit hash: eeeedaf
- commit date: 2024-03-30
- overall geometric mean: 1.09x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                          | 242 ms: 1.06x faster                                                          |
| chameleon      | 6.13 ms                                                                         | 5.89 ms: 1.04x faster                                                         |
| docutils       | 1.94 sec                                                                        | 1.84 sec: 1.05x faster                                                        |
| html5lib       | 46.3 ms                                                                         | 44.1 ms: 1.05x faster                                                         |
| tornado_http   | 96.6 ms                                                                         | 95.7 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                                           | 1.04x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|---------------------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none_tg        | 208 ms                                                                          | 198 ms: 1.05x faster                                                          |
| async_tree_io_tg          | 550 ms                                                                          | 523 ms: 1.05x faster                                                          |
| async_tree_none           | 230 ms                                                                          | 219 ms: 1.05x faster                                                          |
| async_tree_io             | 548 ms                                                                          | 523 ms: 1.05x faster                                                          |
| async_tree_memoization    | 284 ms                                                                          | 271 ms: 1.05x faster                                                          |
| async_tree_memoization_tg | 264 ms                                                                          | 253 ms: 1.04x faster                                                          |
| async_tree_cpu_io_mixed   | 469 ms                                                                          | 459 ms: 1.02x faster                                                          |
| Geometric mean            | (ref)                                                                           | 1.04x faster                                                                  |

Benchmark hidden because not significant (1): async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 95.6 ms                                                                         | 53.7 ms: 1.78x faster                                                         |
| float          | 53.2 ms                                                                         | 43.4 ms: 1.22x faster                                                         |
| pidigits       | 197 ms                                                                          | 196 ms: 1.00x faster                                                          |
| Geometric mean | (ref)                                                                           | 1.30x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 114 ms                                                                          | 98.7 ms: 1.16x faster                                                         |
| regex_dna      | 121 ms                                                                          | 118 ms: 1.02x faster                                                          |
| regex_v8       | 16.2 ms                                                                         | 16.0 ms: 1.02x faster                                                         |
| regex_effbot   | 1.93 ms                                                                         | 1.91 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                                           | 1.05x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| unpickle_pure_python | 167 us                                                                          | 139 us: 1.20x faster                                                          |
| tomli_loads          | 1.69 sec                                                                        | 1.45 sec: 1.17x faster                                                        |
| xml_etree_iterparse  | 66.4 ms                                                                         | 62.1 ms: 1.07x faster                                                         |
| xml_etree_generate   | 60.8 ms                                                                         | 58.4 ms: 1.04x faster                                                         |
| pickle               | 7.96 us                                                                         | 7.67 us: 1.04x faster                                                         |
| pickle_list          | 3.30 us                                                                         | 3.20 us: 1.03x faster                                                         |
| xml_etree_process    | 42.8 ms                                                                         | 41.7 ms: 1.03x faster                                                         |
| xml_etree_parse      | 109 ms                                                                          | 107 ms: 1.02x faster                                                          |
| json_dumps           | 6.84 ms                                                                         | 6.72 ms: 1.02x faster                                                         |
| pickle_dict          | 19.9 us                                                                         | 19.7 us: 1.01x faster                                                         |
| unpickle             | 9.88 us                                                                         | 9.80 us: 1.01x faster                                                         |
| pickle_pure_python   | 217 us                                                                          | 218 us: 1.00x slower                                                          |
| unpickle_list        | 2.85 us                                                                         | 2.97 us: 1.04x slower                                                         |
| Geometric mean       | (ref)                                                                           | 1.04x faster                                                                  |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|----------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup | 24.1 ms                                                                         | 24.3 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                                           | 1.00x slower                                                                  |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|-----------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 7.15 ms                                                                         | 5.42 ms: 1.32x faster                                                         |
| django_template | 34.1 ms                                                                         | 31.3 ms: 1.09x faster                                                         |
| genshi_text     | 21.1 ms                                                                         | 20.1 ms: 1.05x faster                                                         |
| genshi_xml      | 47.8 ms                                                                         | 45.6 ms: 1.05x faster                                                         |
| Geometric mean  | (ref)                                                                           | 1.12x faster                                                                  |

All benchmarks:
===============

| Benchmark                 | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_ghccc-3.13.0a5+-eeeedaf |
|---------------------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody                     | 95.6 ms                                                                         | 53.7 ms: 1.78x faster                                                         |
| scimark_monte_carlo       | 63.2 ms                                                                         | 39.8 ms: 1.59x faster                                                         |
| fannkuch                  | 319 ms                                                                          | 223 ms: 1.43x faster                                                          |
| scimark_fft               | 242 ms                                                                          | 171 ms: 1.41x faster                                                          |
| spectral_norm             | 70.5 ms                                                                         | 50.4 ms: 1.40x faster                                                         |
| hexiom                    | 6.31 ms                                                                         | 4.61 ms: 1.37x faster                                                         |
| comprehensions            | 15.3 us                                                                         | 11.2 us: 1.37x faster                                                         |
| pyflate                   | 371 ms                                                                          | 280 ms: 1.32x faster                                                          |
| mako                      | 7.15 ms                                                                         | 5.42 ms: 1.32x faster                                                         |
| pprint_pformat            | 1.52 sec                                                                        | 1.16 sec: 1.31x faster                                                        |
| crypto_pyaes              | 62.3 ms                                                                         | 47.7 ms: 1.31x faster                                                         |
| pprint_safe_repr          | 741 ms                                                                          | 569 ms: 1.30x faster                                                          |
| nqueens                   | 92.5 ms                                                                         | 71.7 ms: 1.29x faster                                                         |
| scimark_sparse_mat_mult   | 3.26 ms                                                                         | 2.54 ms: 1.29x faster                                                         |
| float                     | 53.2 ms                                                                         | 43.4 ms: 1.22x faster                                                         |
| unpickle_pure_python      | 167 us                                                                          | 139 us: 1.20x faster                                                          |
| raytrace                  | 264 ms                                                                          | 220 ms: 1.20x faster                                                          |
| scimark_lu                | 88.4 ms                                                                         | 75.2 ms: 1.18x faster                                                         |
| tomli_loads               | 1.69 sec                                                                        | 1.45 sec: 1.17x faster                                                        |
| regex_compile             | 114 ms                                                                          | 98.7 ms: 1.16x faster                                                         |
| scimark_sor               | 97.7 ms                                                                         | 85.6 ms: 1.14x faster                                                         |
| chaos                     | 59.8 ms                                                                         | 53.1 ms: 1.13x faster                                                         |
| go                        | 123 ms                                                                          | 110 ms: 1.12x faster                                                          |
| meteor_contest            | 83.0 ms                                                                         | 73.8 ms: 1.12x faster                                                         |
| sqlglot_normalize         | 238 ms                                                                          | 215 ms: 1.11x faster                                                          |
| deltablue                 | 2.63 ms                                                                         | 2.38 ms: 1.10x faster                                                         |
| sqlglot_optimize          | 45.7 ms                                                                         | 41.6 ms: 1.10x faster                                                         |
| richards_super            | 41.4 ms                                                                         | 37.8 ms: 1.09x faster                                                         |
| typing_runtime_protocols  | 98.5 us                                                                         | 90.3 us: 1.09x faster                                                         |
| mdp                       | 1.77 sec                                                                        | 1.62 sec: 1.09x faster                                                        |
| pycparser                 | 871 ms                                                                          | 799 ms: 1.09x faster                                                          |
| django_template           | 34.1 ms                                                                         | 31.3 ms: 1.09x faster                                                         |
| async_generators          | 307 ms                                                                          | 283 ms: 1.08x faster                                                          |
| sympy_integrate           | 16.2 ms                                                                         | 15.0 ms: 1.08x faster                                                         |
| richards                  | 36.4 ms                                                                         | 34.0 ms: 1.07x faster                                                         |
| xml_etree_iterparse       | 66.4 ms                                                                         | 62.1 ms: 1.07x faster                                                         |
| sympy_str                 | 217 ms                                                                          | 203 ms: 1.07x faster                                                          |
| telco                     | 6.25 ms                                                                         | 5.87 ms: 1.06x faster                                                         |
| sqlglot_parse             | 983 us                                                                          | 923 us: 1.06x faster                                                          |
| logging_simple            | 8.31 us                                                                         | 7.81 us: 1.06x faster                                                         |
| logging_format            | 8.95 us                                                                         | 8.43 us: 1.06x faster                                                         |
| deepcopy_memo             | 26.0 us                                                                         | 24.5 us: 1.06x faster                                                         |
| sqlglot_transpile         | 1.24 ms                                                                         | 1.17 ms: 1.06x faster                                                         |
| sympy_expand              | 380 ms                                                                          | 359 ms: 1.06x faster                                                          |
| 2to3                      | 256 ms                                                                          | 242 ms: 1.06x faster                                                          |
| async_tree_none_tg        | 208 ms                                                                          | 198 ms: 1.05x faster                                                          |
| sympy_sum                 | 110 ms                                                                          | 104 ms: 1.05x faster                                                          |
| docutils                  | 1.94 sec                                                                        | 1.84 sec: 1.05x faster                                                        |
| async_tree_io_tg          | 550 ms                                                                          | 523 ms: 1.05x faster                                                          |
| html5lib                  | 46.3 ms                                                                         | 44.1 ms: 1.05x faster                                                         |
| genshi_text               | 21.1 ms                                                                         | 20.1 ms: 1.05x faster                                                         |
| genshi_xml                | 47.8 ms                                                                         | 45.6 ms: 1.05x faster                                                         |
| async_tree_none           | 230 ms                                                                          | 219 ms: 1.05x faster                                                          |
| async_tree_io             | 548 ms                                                                          | 523 ms: 1.05x faster                                                          |
| async_tree_memoization    | 284 ms                                                                          | 271 ms: 1.05x faster                                                          |
| async_tree_memoization_tg | 264 ms                                                                          | 253 ms: 1.04x faster                                                          |
| xml_etree_generate        | 60.8 ms                                                                         | 58.4 ms: 1.04x faster                                                         |
| thrift                    | 11.1 ms                                                                         | 10.6 ms: 1.04x faster                                                         |
| chameleon                 | 6.13 ms                                                                         | 5.89 ms: 1.04x faster                                                         |
| pickle                    | 7.96 us                                                                         | 7.67 us: 1.04x faster                                                         |
| pylint                    | 222 ms                                                                          | 215 ms: 1.04x faster                                                          |
| sqlite_synth              | 1.93 us                                                                         | 1.87 us: 1.03x faster                                                         |
| pickle_list               | 3.30 us                                                                         | 3.20 us: 1.03x faster                                                         |
| bench_thread_pool         | 1.02 ms                                                                         | 990 us: 1.03x faster                                                          |
| xml_etree_process         | 42.8 ms                                                                         | 41.7 ms: 1.03x faster                                                         |
| regex_dna                 | 121 ms                                                                          | 118 ms: 1.02x faster                                                          |
| async_tree_cpu_io_mixed   | 469 ms                                                                          | 459 ms: 1.02x faster                                                          |
| xml_etree_parse           | 109 ms                                                                          | 107 ms: 1.02x faster                                                          |
| coverage                  | 494 ms                                                                          | 486 ms: 1.02x faster                                                          |
| json_dumps                | 6.84 ms                                                                         | 6.72 ms: 1.02x faster                                                         |
| logging_silent            | 60.4 ns                                                                         | 59.4 ns: 1.02x faster                                                         |
| regex_v8                  | 16.2 ms                                                                         | 16.0 ms: 1.02x faster                                                         |
| pathlib                   | 86.9 ms                                                                         | 85.8 ms: 1.01x faster                                                         |
| pickle_dict               | 19.9 us                                                                         | 19.7 us: 1.01x faster                                                         |
| regex_effbot              | 1.93 ms                                                                         | 1.91 ms: 1.01x faster                                                         |
| tornado_http              | 96.6 ms                                                                         | 95.7 ms: 1.01x faster                                                         |
| bench_mp_pool             | 72.3 ms                                                                         | 71.7 ms: 1.01x faster                                                         |
| unpickle                  | 9.88 us                                                                         | 9.80 us: 1.01x faster                                                         |
| generators                | 23.3 ms                                                                         | 23.1 ms: 1.01x faster                                                         |
| pidigits                  | 197 ms                                                                          | 196 ms: 1.00x faster                                                          |
| deepcopy_reduce           | 2.53 us                                                                         | 2.54 us: 1.00x slower                                                         |
| coroutines                | 14.6 ms                                                                         | 14.7 ms: 1.00x slower                                                         |
| pickle_pure_python        | 217 us                                                                          | 218 us: 1.00x slower                                                          |
| python_startup            | 24.1 ms                                                                         | 24.3 ms: 1.01x slower                                                         |
| gc_traversal              | 1.43 ms                                                                         | 1.45 ms: 1.02x slower                                                         |
| unpickle_list             | 2.85 us                                                                         | 2.97 us: 1.04x slower                                                         |
| unpack_sequence           | 43.8 ns                                                                         | 70.2 ns: 1.60x slower                                                         |
| Geometric mean            | (ref)                                                                           | 1.09x faster                                                                  |

Benchmark hidden because not significant (8): json, asyncio_tcp, asyncio_tcp_ssl, deepcopy, python_startup_no_site, create_gc_cycles, json_loads, async_tree_cpu_io_mixed_tg

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: unknown