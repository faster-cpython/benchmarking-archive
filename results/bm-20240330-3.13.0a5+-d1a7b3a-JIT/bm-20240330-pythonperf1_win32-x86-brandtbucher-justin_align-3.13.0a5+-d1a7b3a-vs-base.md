# Results vs. base

- fork: brandtbucher
- ref: justin_align
- machine: windows-x86
- commit hash: d1a7b3a
- commit date: 2024-03-30
- overall geometric mean: 1.00x slower
- HPT reliability: 97.43%
- HPT 99th percentile: 1.00x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                          | 254 ms: 1.01x faster                                                          |
| chameleon      | 6.13 ms                                                                         | 6.36 ms: 1.04x slower                                                         |
| docutils       | 1.94 sec                                                                        | 1.91 sec: 1.01x faster                                                        |
| html5lib       | 46.3 ms                                                                         | 45.4 ms: 1.02x faster                                                         |
| Geometric mean | (ref)                                                                           | 1.00x faster                                                                  |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-------------------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none_tg      | 208 ms                                                                          | 206 ms: 1.01x faster                                                          |
| async_tree_io_tg        | 550 ms                                                                          | 544 ms: 1.01x faster                                                          |
| async_tree_cpu_io_mixed | 469 ms                                                                          | 474 ms: 1.01x slower                                                          |
| Geometric mean          | (ref)                                                                           | 1.00x faster                                                                  |

Benchmark hidden because not significant (5): async_tree_memoization_tg, async_tree_io, async_tree_memoization, async_tree_none, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 197 ms                                                                          | 197 ms: 1.00x faster                                                          |
| nbody          | 95.6 ms                                                                         | 96.5 ms: 1.01x slower                                                         |
| float          | 53.2 ms                                                                         | 54.0 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                                           | 1.01x slower                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 114 ms                                                                          | 113 ms: 1.01x faster                                                          |
| regex_effbot   | 1.93 ms                                                                         | 1.90 ms: 1.01x faster                                                         |
| regex_dna      | 121 ms                                                                          | 121 ms: 1.01x slower                                                          |
| regex_v8       | 16.2 ms                                                                         | 16.3 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                                           | 1.00x faster                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_list          | 3.30 us                                                                         | 3.23 us: 1.02x faster                                                         |
| unpickle_list        | 2.85 us                                                                         | 2.80 us: 1.02x faster                                                         |
| xml_etree_parse      | 109 ms                                                                          | 107 ms: 1.02x faster                                                          |
| xml_etree_iterparse  | 66.4 ms                                                                         | 65.4 ms: 1.01x faster                                                         |
| pickle               | 7.96 us                                                                         | 7.90 us: 1.01x faster                                                         |
| pickle_dict          | 19.9 us                                                                         | 19.8 us: 1.01x faster                                                         |
| json_loads           | 20.3 us                                                                         | 20.2 us: 1.00x faster                                                         |
| json_dumps           | 6.84 ms                                                                         | 6.93 ms: 1.01x slower                                                         |
| unpickle             | 9.88 us                                                                         | 10.0 us: 1.02x slower                                                         |
| xml_etree_generate   | 60.8 ms                                                                         | 62.0 ms: 1.02x slower                                                         |
| unpickle_pure_python | 167 us                                                                          | 171 us: 1.02x slower                                                          |
| tomli_loads          | 1.69 sec                                                                        | 1.74 sec: 1.02x slower                                                        |
| xml_etree_process    | 42.8 ms                                                                         | 43.8 ms: 1.02x slower                                                         |
| pickle_pure_python   | 217 us                                                                          | 223 us: 1.03x slower                                                          |
| Geometric mean       | (ref)                                                                           | 1.00x slower                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|----------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup | 24.1 ms                                                                         | 24.4 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                                           | 1.00x slower                                                                  |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|-----------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_text     | 21.1 ms                                                                         | 20.7 ms: 1.02x faster                                                         |
| django_template | 34.1 ms                                                                         | 33.6 ms: 1.01x faster                                                         |
| mako            | 7.15 ms                                                                         | 7.07 ms: 1.01x faster                                                         |
| genshi_xml      | 47.8 ms                                                                         | 48.8 ms: 1.02x slower                                                         |
| Geometric mean  | (ref)                                                                           | 1.00x faster                                                                  |

All benchmarks:
===============

| Benchmark                | bm-20240329-pythonperf1_win32-x86-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240330-pythonperf1_win32-x86-brandtbucher-justin_align-3.13.0a5+-d1a7b3a |
|--------------------------|:-------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_generators         | 307 ms                                                                          | 286 ms: 1.07x faster                                                          |
| typing_runtime_protocols | 98.5 us                                                                         | 94.1 us: 1.05x faster                                                         |
| json                     | 4.43 ms                                                                         | 4.26 ms: 1.04x faster                                                         |
| scimark_sparse_mat_mult  | 3.26 ms                                                                         | 3.15 ms: 1.03x faster                                                         |
| sympy_expand             | 380 ms                                                                          | 371 ms: 1.02x faster                                                          |
| scimark_monte_carlo      | 63.2 ms                                                                         | 62.0 ms: 1.02x faster                                                         |
| pickle_list              | 3.30 us                                                                         | 3.23 us: 1.02x faster                                                         |
| sympy_str                | 217 ms                                                                          | 213 ms: 1.02x faster                                                          |
| html5lib                 | 46.3 ms                                                                         | 45.4 ms: 1.02x faster                                                         |
| unpickle_list            | 2.85 us                                                                         | 2.80 us: 1.02x faster                                                         |
| xml_etree_parse          | 109 ms                                                                          | 107 ms: 1.02x faster                                                          |
| mdp                      | 1.77 sec                                                                        | 1.74 sec: 1.02x faster                                                        |
| pprint_pformat           | 1.52 sec                                                                        | 1.49 sec: 1.02x faster                                                        |
| scimark_fft              | 242 ms                                                                          | 238 ms: 1.02x faster                                                          |
| pycparser                | 871 ms                                                                          | 857 ms: 1.02x faster                                                          |
| genshi_text              | 21.1 ms                                                                         | 20.7 ms: 1.02x faster                                                         |
| sympy_sum                | 110 ms                                                                          | 108 ms: 1.02x faster                                                          |
| pyflate                  | 371 ms                                                                          | 365 ms: 1.01x faster                                                          |
| xml_etree_iterparse      | 66.4 ms                                                                         | 65.4 ms: 1.01x faster                                                         |
| docutils                 | 1.94 sec                                                                        | 1.91 sec: 1.01x faster                                                        |
| async_tree_none_tg       | 208 ms                                                                          | 206 ms: 1.01x faster                                                          |
| richards_super           | 41.4 ms                                                                         | 40.8 ms: 1.01x faster                                                         |
| regex_compile            | 114 ms                                                                          | 113 ms: 1.01x faster                                                          |
| django_template          | 34.1 ms                                                                         | 33.6 ms: 1.01x faster                                                         |
| regex_effbot             | 1.93 ms                                                                         | 1.90 ms: 1.01x faster                                                         |
| mako                     | 7.15 ms                                                                         | 7.07 ms: 1.01x faster                                                         |
| meteor_contest           | 83.0 ms                                                                         | 82.0 ms: 1.01x faster                                                         |
| coverage                 | 494 ms                                                                          | 489 ms: 1.01x faster                                                          |
| deltablue                | 2.63 ms                                                                         | 2.61 ms: 1.01x faster                                                         |
| async_tree_io_tg         | 550 ms                                                                          | 544 ms: 1.01x faster                                                          |
| pprint_safe_repr         | 741 ms                                                                          | 735 ms: 1.01x faster                                                          |
| sympy_integrate          | 16.2 ms                                                                         | 16.0 ms: 1.01x faster                                                         |
| raytrace                 | 264 ms                                                                          | 262 ms: 1.01x faster                                                          |
| pickle                   | 7.96 us                                                                         | 7.90 us: 1.01x faster                                                         |
| pylint                   | 222 ms                                                                          | 221 ms: 1.01x faster                                                          |
| asyncio_tcp_ssl          | 16.9 sec                                                                        | 16.7 sec: 1.01x faster                                                        |
| pathlib                  | 86.9 ms                                                                         | 86.3 ms: 1.01x faster                                                         |
| sqlite_synth             | 1.93 us                                                                         | 1.92 us: 1.01x faster                                                         |
| deepcopy_reduce          | 2.53 us                                                                         | 2.51 us: 1.01x faster                                                         |
| generators               | 23.3 ms                                                                         | 23.1 ms: 1.01x faster                                                         |
| richards                 | 36.4 ms                                                                         | 36.2 ms: 1.01x faster                                                         |
| 2to3                     | 256 ms                                                                          | 254 ms: 1.01x faster                                                          |
| pickle_dict              | 19.9 us                                                                         | 19.8 us: 1.01x faster                                                         |
| json_loads               | 20.3 us                                                                         | 20.2 us: 1.00x faster                                                         |
| pidigits                 | 197 ms                                                                          | 197 ms: 1.00x faster                                                          |
| thrift                   | 11.1 ms                                                                         | 11.1 ms: 1.00x slower                                                         |
| deepcopy_memo            | 26.0 us                                                                         | 26.1 us: 1.00x slower                                                         |
| regex_dna                | 121 ms                                                                          | 121 ms: 1.01x slower                                                          |
| comprehensions           | 15.3 us                                                                         | 15.4 us: 1.01x slower                                                         |
| deepcopy                 | 289 us                                                                          | 291 us: 1.01x slower                                                          |
| nbody                    | 95.6 ms                                                                         | 96.5 ms: 1.01x slower                                                         |
| regex_v8                 | 16.2 ms                                                                         | 16.3 ms: 1.01x slower                                                         |
| async_tree_cpu_io_mixed  | 469 ms                                                                          | 474 ms: 1.01x slower                                                          |
| nqueens                  | 92.5 ms                                                                         | 93.5 ms: 1.01x slower                                                         |
| python_startup           | 24.1 ms                                                                         | 24.4 ms: 1.01x slower                                                         |
| fannkuch                 | 319 ms                                                                          | 323 ms: 1.01x slower                                                          |
| json_dumps               | 6.84 ms                                                                         | 6.93 ms: 1.01x slower                                                         |
| sqlglot_normalize        | 238 ms                                                                          | 241 ms: 1.01x slower                                                          |
| sqlglot_transpile        | 1.24 ms                                                                         | 1.25 ms: 1.01x slower                                                         |
| chaos                    | 59.8 ms                                                                         | 60.7 ms: 1.01x slower                                                         |
| float                    | 53.2 ms                                                                         | 54.0 ms: 1.01x slower                                                         |
| logging_silent           | 60.4 ns                                                                         | 61.3 ns: 1.02x slower                                                         |
| unpickle                 | 9.88 us                                                                         | 10.0 us: 1.02x slower                                                         |
| logging_format           | 8.95 us                                                                         | 9.11 us: 1.02x slower                                                         |
| genshi_xml               | 47.8 ms                                                                         | 48.8 ms: 1.02x slower                                                         |
| xml_etree_generate       | 60.8 ms                                                                         | 62.0 ms: 1.02x slower                                                         |
| sqlglot_parse            | 983 us                                                                          | 1.00 ms: 1.02x slower                                                         |
| unpickle_pure_python     | 167 us                                                                          | 171 us: 1.02x slower                                                          |
| coroutines               | 14.6 ms                                                                         | 14.9 ms: 1.02x slower                                                         |
| scimark_sor              | 97.7 ms                                                                         | 99.9 ms: 1.02x slower                                                         |
| crypto_pyaes             | 62.3 ms                                                                         | 63.7 ms: 1.02x slower                                                         |
| spectral_norm            | 70.5 ms                                                                         | 72.1 ms: 1.02x slower                                                         |
| tomli_loads              | 1.69 sec                                                                        | 1.74 sec: 1.02x slower                                                        |
| xml_etree_process        | 42.8 ms                                                                         | 43.8 ms: 1.02x slower                                                         |
| logging_simple           | 8.31 us                                                                         | 8.55 us: 1.03x slower                                                         |
| pickle_pure_python       | 217 us                                                                          | 223 us: 1.03x slower                                                          |
| chameleon                | 6.13 ms                                                                         | 6.36 ms: 1.04x slower                                                         |
| unpack_sequence          | 43.8 ns                                                                         | 45.7 ns: 1.04x slower                                                         |
| telco                    | 6.25 ms                                                                         | 6.58 ms: 1.05x slower                                                         |
| scimark_lu               | 88.4 ms                                                                         | 94.8 ms: 1.07x slower                                                         |
| Geometric mean           | (ref)                                                                           | 1.00x slower                                                                  |

Benchmark hidden because not significant (15): async_tree_memoization_tg, tornado_http, async_tree_io, go, hexiom, python_startup_no_site, gc_traversal, sqlglot_optimize, bench_mp_pool, async_tree_memoization, asyncio_tcp, async_tree_none, create_gc_cycles, async_tree_cpu_io_mixed_tg, bench_thread_pool

# HPT report

- Reliability score: 97.43% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: unknown