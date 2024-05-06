# Results vs. base

- fork: brandtbucher
- ref: stitch_exhausted
- machine: windows-x86
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.01x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                          | 264 ms: 1.04x slower                                                              |
| chameleon      | 6.11 ms                                                                         | 6.24 ms: 1.02x slower                                                             |
| docutils       | 1.94 sec                                                                        | 1.98 sec: 1.02x slower                                                            |
| tornado_http   | 96.5 ms                                                                         | 97.6 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                                           | 1.02x slower                                                                      |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|--------------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| async_tree_none_tg | 209 ms                                                                          | 212 ms: 1.01x slower                                                              |
| async_tree_io_tg   | 545 ms                                                                          | 552 ms: 1.01x slower                                                              |
| async_tree_none    | 232 ms                                                                          | 237 ms: 1.02x slower                                                              |
| Geometric mean     | (ref)                                                                           | 1.01x slower                                                                      |

Benchmark hidden because not significant (5): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_memoization, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| pidigits       | 202 ms                                                                          | 198 ms: 1.02x faster                                                              |
| float          | 53.0 ms                                                                         | 53.7 ms: 1.01x slower                                                             |
| nbody          | 96.2 ms                                                                         | 98.7 ms: 1.03x slower                                                             |
| Geometric mean | (ref)                                                                           | 1.01x slower                                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| regex_dna      | 125 ms                                                                          | 122 ms: 1.02x faster                                                              |
| regex_effbot   | 1.92 ms                                                                         | 1.89 ms: 1.02x faster                                                             |
| regex_compile  | 114 ms                                                                          | 115 ms: 1.01x slower                                                              |
| regex_v8       | 16.1 ms                                                                         | 16.3 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                                           | 1.01x faster                                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| unpickle_list        | 2.97 us                                                                         | 2.76 us: 1.08x faster                                                             |
| json_dumps           | 7.10 ms                                                                         | 6.91 ms: 1.03x faster                                                             |
| json_loads           | 20.0 us                                                                         | 19.8 us: 1.01x faster                                                             |
| xml_etree_iterparse  | 67.0 ms                                                                         | 66.6 ms: 1.01x faster                                                             |
| unpickle             | 9.81 us                                                                         | 9.89 us: 1.01x slower                                                             |
| pickle_list          | 3.23 us                                                                         | 3.26 us: 1.01x slower                                                             |
| pickle_pure_python   | 222 us                                                                          | 224 us: 1.01x slower                                                              |
| pickle_dict          | 19.8 us                                                                         | 20.1 us: 1.01x slower                                                             |
| xml_etree_parse      | 108 ms                                                                          | 110 ms: 1.01x slower                                                              |
| unpickle_pure_python | 175 us                                                                          | 178 us: 1.02x slower                                                              |
| pickle               | 8.06 us                                                                         | 8.24 us: 1.02x slower                                                             |
| tomli_loads          | 1.70 sec                                                                        | 1.75 sec: 1.03x slower                                                            |
| xml_etree_generate   | 61.8 ms                                                                         | 64.4 ms: 1.04x slower                                                             |
| xml_etree_process    | 43.4 ms                                                                         | 46.0 ms: 1.06x slower                                                             |
| Geometric mean       | (ref)                                                                           | 1.01x slower                                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| python_startup         | 24.8 ms                                                                         | 24.2 ms: 1.02x faster                                                             |
| python_startup_no_site | 22.4 ms                                                                         | 22.0 ms: 1.02x faster                                                             |
| Geometric mean         | (ref)                                                                           | 1.02x faster                                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| mako            | 7.08 ms                                                                         | 7.18 ms: 1.01x slower                                                             |
| django_template | 33.9 ms                                                                         | 35.3 ms: 1.04x slower                                                             |
| genshi_xml      | 47.9 ms                                                                         | 49.9 ms: 1.04x slower                                                             |
| genshi_text     | 21.7 ms                                                                         | 23.3 ms: 1.07x slower                                                             |
| Geometric mean  | (ref)                                                                           | 1.04x slower                                                                      |

All benchmarks:
===============

| Benchmark                | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf1_win32-x86-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|--------------------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------:|
| unpickle_list            | 2.97 us                                                                         | 2.76 us: 1.08x faster                                                             |
| deepcopy_reduce          | 2.72 us                                                                         | 2.57 us: 1.06x faster                                                             |
| json_dumps               | 7.10 ms                                                                         | 6.91 ms: 1.03x faster                                                             |
| logging_silent           | 61.3 ns                                                                         | 59.9 ns: 1.02x faster                                                             |
| regex_dna                | 125 ms                                                                          | 122 ms: 1.02x faster                                                              |
| python_startup           | 24.8 ms                                                                         | 24.2 ms: 1.02x faster                                                             |
| python_startup_no_site   | 22.4 ms                                                                         | 22.0 ms: 1.02x faster                                                             |
| pidigits                 | 202 ms                                                                          | 198 ms: 1.02x faster                                                              |
| pycparser                | 885 ms                                                                          | 869 ms: 1.02x faster                                                              |
| async_generators         | 299 ms                                                                          | 294 ms: 1.02x faster                                                              |
| regex_effbot             | 1.92 ms                                                                         | 1.89 ms: 1.02x faster                                                             |
| scimark_sparse_mat_mult  | 3.18 ms                                                                         | 3.14 ms: 1.01x faster                                                             |
| spectral_norm            | 71.3 ms                                                                         | 70.5 ms: 1.01x faster                                                             |
| thrift                   | 11.1 ms                                                                         | 11.0 ms: 1.01x faster                                                             |
| pprint_pformat           | 1.50 sec                                                                        | 1.48 sec: 1.01x faster                                                            |
| pprint_safe_repr         | 736 ms                                                                          | 732 ms: 1.01x faster                                                              |
| json_loads               | 20.0 us                                                                         | 19.8 us: 1.01x faster                                                             |
| xml_etree_iterparse      | 67.0 ms                                                                         | 66.6 ms: 1.01x faster                                                             |
| deltablue                | 2.63 ms                                                                         | 2.61 ms: 1.00x faster                                                             |
| pyflate                  | 371 ms                                                                          | 372 ms: 1.00x slower                                                              |
| mdp                      | 1.75 sec                                                                        | 1.76 sec: 1.01x slower                                                            |
| unpickle                 | 9.81 us                                                                         | 9.89 us: 1.01x slower                                                             |
| sqlglot_transpile        | 1.25 ms                                                                         | 1.26 ms: 1.01x slower                                                             |
| pickle_list              | 3.23 us                                                                         | 3.26 us: 1.01x slower                                                             |
| regex_compile            | 114 ms                                                                          | 115 ms: 1.01x slower                                                              |
| pickle_pure_python       | 222 us                                                                          | 224 us: 1.01x slower                                                              |
| regex_v8                 | 16.1 ms                                                                         | 16.3 ms: 1.01x slower                                                             |
| fannkuch                 | 321 ms                                                                          | 324 ms: 1.01x slower                                                              |
| sqlglot_parse            | 995 us                                                                          | 1.00 ms: 1.01x slower                                                             |
| pylint                   | 226 ms                                                                          | 228 ms: 1.01x slower                                                              |
| tornado_http             | 96.5 ms                                                                         | 97.6 ms: 1.01x slower                                                             |
| sympy_expand             | 381 ms                                                                          | 386 ms: 1.01x slower                                                              |
| float                    | 53.0 ms                                                                         | 53.7 ms: 1.01x slower                                                             |
| telco                    | 6.25 ms                                                                         | 6.32 ms: 1.01x slower                                                             |
| async_tree_none_tg       | 209 ms                                                                          | 212 ms: 1.01x slower                                                              |
| sqlite_synth             | 1.92 us                                                                         | 1.94 us: 1.01x slower                                                             |
| async_tree_io_tg         | 545 ms                                                                          | 552 ms: 1.01x slower                                                              |
| pickle_dict              | 19.8 us                                                                         | 20.1 us: 1.01x slower                                                             |
| mako                     | 7.08 ms                                                                         | 7.18 ms: 1.01x slower                                                             |
| xml_etree_parse          | 108 ms                                                                          | 110 ms: 1.01x slower                                                              |
| logging_simple           | 8.48 us                                                                         | 8.60 us: 1.01x slower                                                             |
| bench_thread_pool        | 1.01 ms                                                                         | 1.03 ms: 1.02x slower                                                             |
| sympy_sum                | 110 ms                                                                          | 112 ms: 1.02x slower                                                              |
| logging_format           | 9.02 us                                                                         | 9.18 us: 1.02x slower                                                             |
| unpickle_pure_python     | 175 us                                                                          | 178 us: 1.02x slower                                                              |
| coverage                 | 481 ms                                                                          | 490 ms: 1.02x slower                                                              |
| scimark_sor              | 96.1 ms                                                                         | 97.9 ms: 1.02x slower                                                             |
| docutils                 | 1.94 sec                                                                        | 1.98 sec: 1.02x slower                                                            |
| sympy_str                | 217 ms                                                                          | 222 ms: 1.02x slower                                                              |
| scimark_fft              | 236 ms                                                                          | 240 ms: 1.02x slower                                                              |
| chameleon                | 6.11 ms                                                                         | 6.24 ms: 1.02x slower                                                             |
| pickle                   | 8.06 us                                                                         | 8.24 us: 1.02x slower                                                             |
| async_tree_none          | 232 ms                                                                          | 237 ms: 1.02x slower                                                              |
| nbody                    | 96.2 ms                                                                         | 98.7 ms: 1.03x slower                                                             |
| tomli_loads              | 1.70 sec                                                                        | 1.75 sec: 1.03x slower                                                            |
| crypto_pyaes             | 61.1 ms                                                                         | 62.7 ms: 1.03x slower                                                             |
| scimark_monte_carlo      | 60.1 ms                                                                         | 61.7 ms: 1.03x slower                                                             |
| sqlglot_optimize         | 46.2 ms                                                                         | 47.5 ms: 1.03x slower                                                             |
| sympy_integrate          | 16.4 ms                                                                         | 16.9 ms: 1.03x slower                                                             |
| go                       | 126 ms                                                                          | 130 ms: 1.03x slower                                                              |
| unpack_sequence          | 44.0 ns                                                                         | 45.5 ns: 1.03x slower                                                             |
| meteor_contest           | 84.1 ms                                                                         | 87.2 ms: 1.04x slower                                                             |
| comprehensions           | 15.7 us                                                                         | 16.3 us: 1.04x slower                                                             |
| 2to3                     | 255 ms                                                                          | 264 ms: 1.04x slower                                                              |
| raytrace                 | 254 ms                                                                          | 264 ms: 1.04x slower                                                              |
| django_template          | 33.9 ms                                                                         | 35.3 ms: 1.04x slower                                                             |
| sqlglot_normalize        | 237 ms                                                                          | 247 ms: 1.04x slower                                                              |
| genshi_xml               | 47.9 ms                                                                         | 49.9 ms: 1.04x slower                                                             |
| xml_etree_generate       | 61.8 ms                                                                         | 64.4 ms: 1.04x slower                                                             |
| deepcopy                 | 290 us                                                                          | 302 us: 1.04x slower                                                              |
| chaos                    | 59.8 ms                                                                         | 62.5 ms: 1.05x slower                                                             |
| nqueens                  | 92.1 ms                                                                         | 96.7 ms: 1.05x slower                                                             |
| deepcopy_memo            | 25.3 us                                                                         | 26.6 us: 1.05x slower                                                             |
| typing_runtime_protocols | 95.7 us                                                                         | 101 us: 1.06x slower                                                              |
| xml_etree_process        | 43.4 ms                                                                         | 46.0 ms: 1.06x slower                                                             |
| hexiom                   | 6.20 ms                                                                         | 6.65 ms: 1.07x slower                                                             |
| genshi_text              | 21.7 ms                                                                         | 23.3 ms: 1.07x slower                                                             |
| Geometric mean           | (ref)                                                                           | 1.01x slower                                                                      |

Benchmark hidden because not significant (18): json, gc_traversal, richards_super, pathlib, async_tree_cpu_io_mixed_tg, html5lib, richards, create_gc_cycles, asyncio_tcp, generators, coroutines, async_tree_cpu_io_mixed, scimark_lu, bench_mp_pool, asyncio_tcp_ssl, async_tree_memoization_tg, async_tree_memoization, async_tree_io

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown