# Results vs. base

- fork: brandtbucher
- ref: justin_align
- machine: windows-x86
- commit hash: 790b1f8
- commit date: 2024-03-30
- overall geometric mean: 1.01x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                          | 252 ms: 1.02x faster                                                          |
| html5lib       | 46.5 ms                                                                         | 45.5 ms: 1.02x faster                                                         |
| tornado_http   | 96.1 ms                                                                         | 96.9 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                                           | 1.01x faster                                                                  |

Benchmark hidden because not significant (2): chameleon, docutils

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_memoization, async_tree_io_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_io, async_tree_cpu_io_mixed, async_tree_none_tg, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 95.8 ms                                                                         | 92.1 ms: 1.04x faster                                                         |
| pidigits       | 199 ms                                                                          | 202 ms: 1.01x slower                                                          |
| Geometric mean | (ref)                                                                           | 1.01x faster                                                                  |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 114 ms                                                                          | 115 ms: 1.01x slower                                                          |
| Geometric mean | (ref)                                                                           | 1.00x slower                                                                  |

Benchmark hidden because not significant (3): regex_effbot, regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|----------------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| unpickle_pure_python | 180 us                                                                          | 166 us: 1.08x faster                                                          |
| json_dumps           | 6.93 ms                                                                         | 6.70 ms: 1.03x faster                                                         |
| tomli_loads          | 1.73 sec                                                                        | 1.67 sec: 1.03x faster                                                        |
| xml_etree_generate   | 62.4 ms                                                                         | 60.8 ms: 1.03x faster                                                         |
| xml_etree_process    | 43.7 ms                                                                         | 42.6 ms: 1.03x faster                                                         |
| unpickle             | 10.0 us                                                                         | 9.81 us: 1.02x faster                                                         |
| pickle_list          | 3.25 us                                                                         | 3.18 us: 1.02x faster                                                         |
| pickle_dict          | 19.9 us                                                                         | 19.6 us: 1.01x faster                                                         |
| xml_etree_iterparse  | 65.4 ms                                                                         | 64.8 ms: 1.01x faster                                                         |
| pickle_pure_python   | 220 us                                                                          | 221 us: 1.01x slower                                                          |
| xml_etree_parse      | 107 ms                                                                          | 108 ms: 1.01x slower                                                          |
| pickle               | 7.98 us                                                                         | 8.04 us: 1.01x slower                                                         |
| json_loads           | 19.9 us                                                                         | 20.1 us: 1.01x slower                                                         |
| unpickle_list        | 2.85 us                                                                         | 2.90 us: 1.02x slower                                                         |
| Geometric mean       | (ref)                                                                           | 1.02x faster                                                                  |

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|-----------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_xml      | 48.6 ms                                                                         | 47.0 ms: 1.04x faster                                                         |
| genshi_text     | 21.2 ms                                                                         | 20.8 ms: 1.02x faster                                                         |
| django_template | 33.4 ms                                                                         | 33.0 ms: 1.01x faster                                                         |
| mako            | 7.10 ms                                                                         | 7.05 ms: 1.01x faster                                                         |
| Geometric mean  | (ref)                                                                           | 1.02x faster                                                                  |

All benchmarks:
===============

| Benchmark                | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-790b1f8 |
|--------------------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| unpickle_pure_python     | 180 us                                                                          | 166 us: 1.08x faster                                                          |
| scimark_lu               | 93.0 ms                                                                         | 86.1 ms: 1.08x faster                                                         |
| json                     | 4.45 ms                                                                         | 4.19 ms: 1.06x faster                                                         |
| scimark_sor              | 100.0 ms                                                                        | 95.6 ms: 1.05x faster                                                         |
| nbody                    | 95.8 ms                                                                         | 92.1 ms: 1.04x faster                                                         |
| comprehensions           | 15.6 us                                                                         | 15.1 us: 1.04x faster                                                         |
| genshi_xml               | 48.6 ms                                                                         | 47.0 ms: 1.04x faster                                                         |
| json_dumps               | 6.93 ms                                                                         | 6.70 ms: 1.03x faster                                                         |
| tomli_loads              | 1.73 sec                                                                        | 1.67 sec: 1.03x faster                                                        |
| deepcopy_memo            | 26.3 us                                                                         | 25.5 us: 1.03x faster                                                         |
| raytrace                 | 273 ms                                                                          | 265 ms: 1.03x faster                                                          |
| deltablue                | 2.62 ms                                                                         | 2.55 ms: 1.03x faster                                                         |
| meteor_contest           | 83.9 ms                                                                         | 81.6 ms: 1.03x faster                                                         |
| xml_etree_generate       | 62.4 ms                                                                         | 60.8 ms: 1.03x faster                                                         |
| xml_etree_process        | 43.7 ms                                                                         | 42.6 ms: 1.03x faster                                                         |
| sqlglot_parse            | 1.01 ms                                                                         | 983 us: 1.02x faster                                                          |
| unpickle                 | 10.0 us                                                                         | 9.81 us: 1.02x faster                                                         |
| scimark_sparse_mat_mult  | 3.19 ms                                                                         | 3.12 ms: 1.02x faster                                                         |
| html5lib                 | 46.5 ms                                                                         | 45.5 ms: 1.02x faster                                                         |
| sqlglot_transpile        | 1.26 ms                                                                         | 1.24 ms: 1.02x faster                                                         |
| pickle_list              | 3.25 us                                                                         | 3.18 us: 1.02x faster                                                         |
| go                       | 123 ms                                                                          | 121 ms: 1.02x faster                                                          |
| chaos                    | 63.1 ms                                                                         | 61.8 ms: 1.02x faster                                                         |
| coverage                 | 487 ms                                                                          | 477 ms: 1.02x faster                                                          |
| genshi_text              | 21.2 ms                                                                         | 20.8 ms: 1.02x faster                                                         |
| deepcopy                 | 300 us                                                                          | 294 us: 1.02x faster                                                          |
| pprint_safe_repr         | 742 ms                                                                          | 727 ms: 1.02x faster                                                          |
| pprint_pformat           | 1.51 sec                                                                        | 1.48 sec: 1.02x faster                                                        |
| 2to3                     | 257 ms                                                                          | 252 ms: 1.02x faster                                                          |
| sqlglot_optimize         | 46.5 ms                                                                         | 45.7 ms: 1.02x faster                                                         |
| nqueens                  | 92.1 ms                                                                         | 90.5 ms: 1.02x faster                                                         |
| unpack_sequence          | 46.6 ns                                                                         | 45.9 ns: 1.02x faster                                                         |
| pyflate                  | 370 ms                                                                          | 364 ms: 1.02x faster                                                          |
| telco                    | 6.50 ms                                                                         | 6.41 ms: 1.01x faster                                                         |
| sqlglot_normalize        | 241 ms                                                                          | 238 ms: 1.01x faster                                                          |
| sqlite_synth             | 1.94 us                                                                         | 1.92 us: 1.01x faster                                                         |
| django_template          | 33.4 ms                                                                         | 33.0 ms: 1.01x faster                                                         |
| spectral_norm            | 71.2 ms                                                                         | 70.4 ms: 1.01x faster                                                         |
| typing_runtime_protocols | 96.5 us                                                                         | 95.3 us: 1.01x faster                                                         |
| sympy_expand             | 381 ms                                                                          | 377 ms: 1.01x faster                                                          |
| sympy_integrate          | 16.4 ms                                                                         | 16.2 ms: 1.01x faster                                                         |
| pickle_dict              | 19.9 us                                                                         | 19.6 us: 1.01x faster                                                         |
| mdp                      | 1.78 sec                                                                        | 1.76 sec: 1.01x faster                                                        |
| xml_etree_iterparse      | 65.4 ms                                                                         | 64.8 ms: 1.01x faster                                                         |
| pycparser                | 872 ms                                                                          | 865 ms: 1.01x faster                                                          |
| sympy_sum                | 110 ms                                                                          | 109 ms: 1.01x faster                                                          |
| deepcopy_reduce          | 2.64 us                                                                         | 2.62 us: 1.01x faster                                                         |
| mako                     | 7.10 ms                                                                         | 7.05 ms: 1.01x faster                                                         |
| fannkuch                 | 319 ms                                                                          | 317 ms: 1.01x faster                                                          |
| sympy_str                | 218 ms                                                                          | 216 ms: 1.01x faster                                                          |
| pathlib                  | 86.3 ms                                                                         | 86.7 ms: 1.01x slower                                                         |
| pickle_pure_python       | 220 us                                                                          | 221 us: 1.01x slower                                                          |
| logging_silent           | 60.3 ns                                                                         | 60.7 ns: 1.01x slower                                                         |
| gc_traversal             | 1.43 ms                                                                         | 1.44 ms: 1.01x slower                                                         |
| xml_etree_parse          | 107 ms                                                                          | 108 ms: 1.01x slower                                                          |
| pickle                   | 7.98 us                                                                         | 8.04 us: 1.01x slower                                                         |
| tornado_http             | 96.1 ms                                                                         | 96.9 ms: 1.01x slower                                                         |
| json_loads               | 19.9 us                                                                         | 20.1 us: 1.01x slower                                                         |
| coroutines               | 14.7 ms                                                                         | 14.9 ms: 1.01x slower                                                         |
| regex_compile            | 114 ms                                                                          | 115 ms: 1.01x slower                                                          |
| logging_simple           | 8.24 us                                                                         | 8.34 us: 1.01x slower                                                         |
| logging_format           | 8.81 us                                                                         | 8.92 us: 1.01x slower                                                         |
| hexiom                   | 6.28 ms                                                                         | 6.36 ms: 1.01x slower                                                         |
| pidigits                 | 199 ms                                                                          | 202 ms: 1.01x slower                                                          |
| scimark_monte_carlo      | 61.5 ms                                                                         | 62.5 ms: 1.02x slower                                                         |
| unpickle_list            | 2.85 us                                                                         | 2.90 us: 1.02x slower                                                         |
| crypto_pyaes             | 61.8 ms                                                                         | 63.2 ms: 1.02x slower                                                         |
| thrift                   | 10.9 ms                                                                         | 11.2 ms: 1.03x slower                                                         |
| async_generators         | 285 ms                                                                          | 294 ms: 1.03x slower                                                          |
| asyncio_tcp              | 604 ms                                                                          | 623 ms: 1.03x slower                                                          |
| richards                 | 35.6 ms                                                                         | 37.0 ms: 1.04x slower                                                         |
| richards_super           | 40.2 ms                                                                         | 42.1 ms: 1.05x slower                                                         |
| Geometric mean           | (ref)                                                                           | 1.01x faster                                                                  |

Benchmark hidden because not significant (23): python_startup_no_site, asyncio_tcp_ssl, async_tree_memoization, regex_effbot, scimark_fft, regex_dna, bench_thread_pool, async_tree_io_tg, async_tree_cpu_io_mixed_tg, bench_mp_pool, regex_v8, python_startup, async_tree_memoization_tg, float, pylint, create_gc_cycles, async_tree_io, async_tree_cpu_io_mixed, docutils, generators, chameleon, async_tree_none_tg, async_tree_none

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown