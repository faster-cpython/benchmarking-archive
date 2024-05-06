# Results vs. base

- fork: brandtbucher
- ref: stitch_exhausted
- machine: windows-amd64
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.00x slower
- HPT reliability: 99.92%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| chameleon      | 4.87 ms                                                                     | 4.75 ms: 1.03x faster                                                         |
| docutils       | 1.69 sec                                                                    | 1.73 sec: 1.02x slower                                                        |
| html5lib       | 36.2 ms                                                                     | 36.8 ms: 1.02x slower                                                         |
| tornado_http   | 84.2 ms                                                                     | 85.2 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                                       | 1.01x slower                                                                  |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark              | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none_tg     | 203 ms                                                                      | 206 ms: 1.02x slower                                                          |
| async_tree_memoization | 268 ms                                                                      | 273 ms: 1.02x slower                                                          |
| async_tree_none        | 215 ms                                                                      | 220 ms: 1.03x slower                                                          |
| Geometric mean         | (ref)                                                                       | 1.01x slower                                                                  |

Benchmark hidden because not significant (5): async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 59.4 ms                                                                     | 57.4 ms: 1.04x faster                                                         |
| float          | 47.7 ms                                                                     | 46.6 ms: 1.02x faster                                                         |
| Geometric mean | (ref)                                                                       | 1.02x faster                                                                  |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_dna      | 117 ms                                                                      | 116 ms: 1.00x faster                                                          |
| regex_compile  | 83.0 ms                                                                     | 87.5 ms: 1.05x slower                                                         |
| Geometric mean | (ref)                                                                       | 1.00x faster                                                                  |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 5.64 ms                                                                     | 5.51 ms: 1.02x faster                                                         |
| unpickle             | 8.68 us                                                                     | 8.48 us: 1.02x faster                                                         |
| tomli_loads          | 1.22 sec                                                                    | 1.21 sec: 1.01x faster                                                        |
| json_loads           | 13.8 us                                                                     | 13.7 us: 1.01x faster                                                         |
| unpickle_pure_python | 130 us                                                                      | 131 us: 1.01x slower                                                          |
| pickle               | 7.34 us                                                                     | 7.40 us: 1.01x slower                                                         |
| xml_etree_process    | 36.8 ms                                                                     | 37.1 ms: 1.01x slower                                                         |
| pickle_pure_python   | 175 us                                                                      | 178 us: 1.02x slower                                                          |
| xml_etree_parse      | 90.2 ms                                                                     | 92.1 ms: 1.02x slower                                                         |
| xml_etree_generate   | 53.7 ms                                                                     | 55.0 ms: 1.02x slower                                                         |
| unpickle_list        | 2.77 us                                                                     | 2.84 us: 1.03x slower                                                         |
| xml_etree_iterparse  | 62.4 ms                                                                     | 64.1 ms: 1.03x slower                                                         |
| pickle_list          | 2.90 us                                                                     | 3.17 us: 1.09x slower                                                         |
| Geometric mean       | (ref)                                                                       | 1.01x slower                                                                  |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 20.4 ms                                                                     | 19.6 ms: 1.04x faster                                                         |
| python_startup         | 22.4 ms                                                                     | 21.9 ms: 1.02x faster                                                         |
| Geometric mean         | (ref)                                                                       | 1.03x faster                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_text     | 15.5 ms                                                                     | 15.6 ms: 1.01x slower                                                         |
| mako            | 5.63 ms                                                                     | 5.71 ms: 1.01x slower                                                         |
| genshi_xml      | 33.8 ms                                                                     | 34.6 ms: 1.02x slower                                                         |
| django_template | 23.0 ms                                                                     | 24.3 ms: 1.06x slower                                                         |
| Geometric mean  | (ref)                                                                       | 1.03x slower                                                                  |

All benchmarks:
===============

| Benchmark                | bm-20240329-pythonperf1-amd64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240402-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|--------------------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json                     | 3.48 ms                                                                     | 2.87 ms: 1.21x faster                                                         |
| asyncio_tcp_ssl          | 1.58 sec                                                                    | 1.44 sec: 1.09x faster                                                        |
| richards_super           | 33.5 ms                                                                     | 31.3 ms: 1.07x faster                                                         |
| richards                 | 30.2 ms                                                                     | 28.2 ms: 1.07x faster                                                         |
| unpack_sequence          | 47.2 ns                                                                     | 44.7 ns: 1.06x faster                                                         |
| bench_mp_pool            | 70.6 ms                                                                     | 67.8 ms: 1.04x faster                                                         |
| python_startup_no_site   | 20.4 ms                                                                     | 19.6 ms: 1.04x faster                                                         |
| nbody                    | 59.4 ms                                                                     | 57.4 ms: 1.04x faster                                                         |
| scimark_lu               | 75.7 ms                                                                     | 73.2 ms: 1.03x faster                                                         |
| chameleon                | 4.87 ms                                                                     | 4.75 ms: 1.03x faster                                                         |
| json_dumps               | 5.64 ms                                                                     | 5.51 ms: 1.02x faster                                                         |
| unpickle                 | 8.68 us                                                                     | 8.48 us: 1.02x faster                                                         |
| python_startup           | 22.4 ms                                                                     | 21.9 ms: 1.02x faster                                                         |
| float                    | 47.7 ms                                                                     | 46.6 ms: 1.02x faster                                                         |
| comprehensions           | 11.3 us                                                                     | 11.1 us: 1.02x faster                                                         |
| scimark_sor              | 81.5 ms                                                                     | 80.0 ms: 1.02x faster                                                         |
| sqlite_synth             | 1.59 us                                                                     | 1.57 us: 1.01x faster                                                         |
| scimark_fft              | 170 ms                                                                      | 168 ms: 1.01x faster                                                          |
| pprint_safe_repr         | 470 ms                                                                      | 465 ms: 1.01x faster                                                          |
| async_generators         | 244 ms                                                                      | 242 ms: 1.01x faster                                                          |
| coverage                 | 46.7 ms                                                                     | 46.3 ms: 1.01x faster                                                         |
| tomli_loads              | 1.22 sec                                                                    | 1.21 sec: 1.01x faster                                                        |
| json_loads               | 13.8 us                                                                     | 13.7 us: 1.01x faster                                                         |
| deepcopy_memo            | 21.6 us                                                                     | 21.5 us: 1.01x faster                                                         |
| regex_dna                | 117 ms                                                                      | 116 ms: 1.00x faster                                                          |
| dulwich_log              | 41.0 ms                                                                     | 40.9 ms: 1.00x faster                                                         |
| sqlglot_parse            | 778 us                                                                      | 780 us: 1.00x slower                                                          |
| scimark_sparse_mat_mult  | 2.29 ms                                                                     | 2.30 ms: 1.00x slower                                                         |
| unpickle_pure_python     | 130 us                                                                      | 131 us: 1.01x slower                                                          |
| logging_format           | 6.31 us                                                                     | 6.36 us: 1.01x slower                                                         |
| sqlglot_transpile        | 1.00 ms                                                                     | 1.01 ms: 1.01x slower                                                         |
| pickle                   | 7.34 us                                                                     | 7.40 us: 1.01x slower                                                         |
| sqlglot_optimize         | 35.6 ms                                                                     | 35.9 ms: 1.01x slower                                                         |
| xml_etree_process        | 36.8 ms                                                                     | 37.1 ms: 1.01x slower                                                         |
| pprint_pformat           | 952 ms                                                                      | 961 ms: 1.01x slower                                                          |
| genshi_text              | 15.5 ms                                                                     | 15.6 ms: 1.01x slower                                                         |
| sqlglot_normalize        | 185 ms                                                                      | 187 ms: 1.01x slower                                                          |
| tornado_http             | 84.2 ms                                                                     | 85.2 ms: 1.01x slower                                                         |
| chaos                    | 39.0 ms                                                                     | 39.5 ms: 1.01x slower                                                         |
| mako                     | 5.63 ms                                                                     | 5.71 ms: 1.01x slower                                                         |
| logging_simple           | 5.84 us                                                                     | 5.92 us: 1.01x slower                                                         |
| mdp                      | 1.47 sec                                                                    | 1.49 sec: 1.02x slower                                                        |
| async_tree_none_tg       | 203 ms                                                                      | 206 ms: 1.02x slower                                                          |
| async_tree_memoization   | 268 ms                                                                      | 273 ms: 1.02x slower                                                          |
| raytrace                 | 182 ms                                                                      | 185 ms: 1.02x slower                                                          |
| html5lib                 | 36.2 ms                                                                     | 36.8 ms: 1.02x slower                                                         |
| pickle_pure_python       | 175 us                                                                      | 178 us: 1.02x slower                                                          |
| xml_etree_parse          | 90.2 ms                                                                     | 92.1 ms: 1.02x slower                                                         |
| docutils                 | 1.69 sec                                                                    | 1.73 sec: 1.02x slower                                                        |
| genshi_xml               | 33.8 ms                                                                     | 34.6 ms: 1.02x slower                                                         |
| xml_etree_generate       | 53.7 ms                                                                     | 55.0 ms: 1.02x slower                                                         |
| crypto_pyaes             | 43.9 ms                                                                     | 45.0 ms: 1.03x slower                                                         |
| async_tree_none          | 215 ms                                                                      | 220 ms: 1.03x slower                                                          |
| unpickle_list            | 2.77 us                                                                     | 2.84 us: 1.03x slower                                                         |
| sympy_integrate          | 13.3 ms                                                                     | 13.6 ms: 1.03x slower                                                         |
| typing_runtime_protocols | 71.1 us                                                                     | 73.0 us: 1.03x slower                                                         |
| xml_etree_iterparse      | 62.4 ms                                                                     | 64.1 ms: 1.03x slower                                                         |
| thrift                   | 8.97 ms                                                                     | 9.22 ms: 1.03x slower                                                         |
| logging_silent           | 53.5 ns                                                                     | 55.0 ns: 1.03x slower                                                         |
| sympy_sum                | 87.6 ms                                                                     | 90.1 ms: 1.03x slower                                                         |
| pylint                   | 195 ms                                                                      | 202 ms: 1.03x slower                                                          |
| fannkuch                 | 224 ms                                                                      | 232 ms: 1.04x slower                                                          |
| sympy_str                | 166 ms                                                                      | 172 ms: 1.04x slower                                                          |
| go                       | 94.1 ms                                                                     | 97.7 ms: 1.04x slower                                                         |
| sympy_expand             | 285 ms                                                                      | 296 ms: 1.04x slower                                                          |
| scimark_monte_carlo      | 39.5 ms                                                                     | 41.1 ms: 1.04x slower                                                         |
| nqueens                  | 60.1 ms                                                                     | 62.5 ms: 1.04x slower                                                         |
| meteor_contest           | 71.7 ms                                                                     | 75.1 ms: 1.05x slower                                                         |
| mypy2                    | 448 ms                                                                      | 471 ms: 1.05x slower                                                          |
| regex_compile            | 83.0 ms                                                                     | 87.5 ms: 1.05x slower                                                         |
| django_template          | 23.0 ms                                                                     | 24.3 ms: 1.06x slower                                                         |
| hexiom                   | 4.54 ms                                                                     | 4.92 ms: 1.08x slower                                                         |
| pickle_list              | 2.90 us                                                                     | 3.17 us: 1.09x slower                                                         |
| Geometric mean           | (ref)                                                                       | 1.00x slower                                                                  |

Benchmark hidden because not significant (25): regex_v8, bench_thread_pool, regex_effbot, async_tree_cpu_io_mixed_tg, create_gc_cycles, spectral_norm, asyncio_tcp, aiohttp, async_tree_io, pyflate, deepcopy, gc_traversal, deltablue, pycparser, deepcopy_reduce, async_tree_io_tg, telco, async_tree_cpu_io_mixed, pidigits, pathlib, generators, pickle_dict, 2to3, coroutines, async_tree_memoization_tg

# HPT report

- Reliability score: 99.92% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown