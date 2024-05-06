# Results vs. base

- fork: brandtbucher
- ref: stitch_exhausted
- machine: windows-amd64
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 218 ms                                                                      | 222 ms: 1.02x slower                                                          |
| chameleon      | 4.69 ms                                                                     | 4.81 ms: 1.02x slower                                                         |
| docutils       | 1.69 sec                                                                    | 1.72 sec: 1.02x slower                                                        |
| html5lib       | 35.1 ms                                                                     | 35.6 ms: 1.02x slower                                                         |
| tornado_http   | 82.8 ms                                                                     | 83.6 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                                       | 1.02x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark       | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|-----------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none | 217 ms                                                                      | 222 ms: 1.02x slower                                                          |
| Geometric mean  | (ref)                                                                       | 1.01x slower                                                                  |

Benchmark hidden because not significant (7): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_memoization, async_tree_none_tg, async_tree_io, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 146 ms                                                                      | 147 ms: 1.00x slower                                                          |
| nbody          | 57.0 ms                                                                     | 59.0 ms: 1.03x slower                                                         |
| Geometric mean | (ref)                                                                       | 1.01x slower                                                                  |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_dna      | 119 ms                                                                      | 116 ms: 1.02x faster                                                          |
| regex_v8       | 14.6 ms                                                                     | 14.4 ms: 1.01x faster                                                         |
| regex_effbot   | 1.57 ms                                                                     | 1.56 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                                       | 1.01x faster                                                                  |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| unpickle             | 8.66 us                                                                     | 8.55 us: 1.01x faster                                                         |
| json_dumps           | 5.58 ms                                                                     | 5.53 ms: 1.01x faster                                                         |
| json_loads           | 13.7 us                                                                     | 13.6 us: 1.01x faster                                                         |
| pickle               | 7.33 us                                                                     | 7.29 us: 1.01x faster                                                         |
| pickle_dict          | 18.6 us                                                                     | 18.5 us: 1.00x faster                                                         |
| unpickle_pure_python | 129 us                                                                      | 129 us: 1.00x faster                                                          |
| xml_etree_parse      | 89.5 ms                                                                     | 90.3 ms: 1.01x slower                                                         |
| xml_etree_process    | 36.2 ms                                                                     | 36.6 ms: 1.01x slower                                                         |
| xml_etree_generate   | 52.4 ms                                                                     | 53.1 ms: 1.01x slower                                                         |
| unpickle_list        | 2.77 us                                                                     | 2.82 us: 1.02x slower                                                         |
| xml_etree_iterparse  | 59.7 ms                                                                     | 61.3 ms: 1.03x slower                                                         |
| tomli_loads          | 1.17 sec                                                                    | 1.21 sec: 1.03x slower                                                        |
| pickle_list          | 2.89 us                                                                     | 3.16 us: 1.09x slower                                                         |
| Geometric mean       | (ref)                                                                       | 1.01x slower                                                                  |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako           | 5.73 ms                                                                     | 5.64 ms: 1.02x faster                                                         |
| genshi_text    | 14.8 ms                                                                     | 15.4 ms: 1.04x slower                                                         |
| genshi_xml     | 32.4 ms                                                                     | 35.7 ms: 1.10x slower                                                         |
| Geometric mean | (ref)                                                                       | 1.04x slower                                                                  |

All benchmarks:
===============

| Benchmark                | bm-20240404-pythonperf1-amd64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 | bm-20240404-pythonperf1-amd64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|--------------------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| go                       | 92.1 ms                                                                     | 89.9 ms: 1.02x faster                                                         |
| regex_dna                | 119 ms                                                                      | 116 ms: 1.02x faster                                                          |
| fannkuch                 | 234 ms                                                                      | 230 ms: 1.02x faster                                                          |
| generators               | 19.6 ms                                                                     | 19.3 ms: 1.02x faster                                                         |
| mako                     | 5.73 ms                                                                     | 5.64 ms: 1.02x faster                                                         |
| create_gc_cycles         | 904 us                                                                      | 891 us: 1.01x faster                                                          |
| regex_v8                 | 14.6 ms                                                                     | 14.4 ms: 1.01x faster                                                         |
| unpickle                 | 8.66 us                                                                     | 8.55 us: 1.01x faster                                                         |
| richards_super           | 30.2 ms                                                                     | 29.9 ms: 1.01x faster                                                         |
| json_dumps               | 5.58 ms                                                                     | 5.53 ms: 1.01x faster                                                         |
| regex_effbot             | 1.57 ms                                                                     | 1.56 ms: 1.01x faster                                                         |
| json_loads               | 13.7 us                                                                     | 13.6 us: 1.01x faster                                                         |
| telco                    | 4.80 ms                                                                     | 4.76 ms: 1.01x faster                                                         |
| richards                 | 26.7 ms                                                                     | 26.5 ms: 1.01x faster                                                         |
| pickle                   | 7.33 us                                                                     | 7.29 us: 1.01x faster                                                         |
| logging_silent           | 53.4 ns                                                                     | 53.1 ns: 1.01x faster                                                         |
| coroutines               | 13.0 ms                                                                     | 12.9 ms: 1.00x faster                                                         |
| sqlite_synth             | 1.57 us                                                                     | 1.56 us: 1.00x faster                                                         |
| pickle_dict              | 18.6 us                                                                     | 18.5 us: 1.00x faster                                                         |
| unpickle_pure_python     | 129 us                                                                      | 129 us: 1.00x faster                                                          |
| pidigits                 | 146 ms                                                                      | 147 ms: 1.00x slower                                                          |
| scimark_fft              | 166 ms                                                                      | 167 ms: 1.01x slower                                                          |
| sqlglot_parse            | 769 us                                                                      | 774 us: 1.01x slower                                                          |
| dulwich_log              | 40.9 ms                                                                     | 41.2 ms: 1.01x slower                                                         |
| xml_etree_parse          | 89.5 ms                                                                     | 90.3 ms: 1.01x slower                                                         |
| json                     | 2.86 ms                                                                     | 2.89 ms: 1.01x slower                                                         |
| tornado_http             | 82.8 ms                                                                     | 83.6 ms: 1.01x slower                                                         |
| scimark_sor              | 80.0 ms                                                                     | 80.9 ms: 1.01x slower                                                         |
| pprint_pformat           | 942 ms                                                                      | 952 ms: 1.01x slower                                                          |
| deepcopy_reduce          | 1.95 us                                                                     | 1.97 us: 1.01x slower                                                         |
| xml_etree_process        | 36.2 ms                                                                     | 36.6 ms: 1.01x slower                                                         |
| sqlglot_transpile        | 985 us                                                                      | 997 us: 1.01x slower                                                          |
| xml_etree_generate       | 52.4 ms                                                                     | 53.1 ms: 1.01x slower                                                         |
| html5lib                 | 35.1 ms                                                                     | 35.6 ms: 1.02x slower                                                         |
| raytrace                 | 164 ms                                                                      | 167 ms: 1.02x slower                                                          |
| pprint_safe_repr         | 463 ms                                                                      | 471 ms: 1.02x slower                                                          |
| scimark_sparse_mat_mult  | 2.22 ms                                                                     | 2.26 ms: 1.02x slower                                                         |
| coverage                 | 46.7 ms                                                                     | 47.5 ms: 1.02x slower                                                         |
| 2to3                     | 218 ms                                                                      | 222 ms: 1.02x slower                                                          |
| scimark_lu               | 69.5 ms                                                                     | 70.7 ms: 1.02x slower                                                         |
| scimark_monte_carlo      | 39.0 ms                                                                     | 39.7 ms: 1.02x slower                                                         |
| unpickle_list            | 2.77 us                                                                     | 2.82 us: 1.02x slower                                                         |
| docutils                 | 1.69 sec                                                                    | 1.72 sec: 1.02x slower                                                        |
| aiohttp                  | 893 us                                                                      | 911 us: 1.02x slower                                                          |
| comprehensions           | 11.1 us                                                                     | 11.3 us: 1.02x slower                                                         |
| async_tree_none          | 217 ms                                                                      | 222 ms: 1.02x slower                                                          |
| chameleon                | 4.69 ms                                                                     | 4.81 ms: 1.02x slower                                                         |
| spectral_norm            | 50.7 ms                                                                     | 51.9 ms: 1.03x slower                                                         |
| xml_etree_iterparse      | 59.7 ms                                                                     | 61.3 ms: 1.03x slower                                                         |
| pylint                   | 193 ms                                                                      | 198 ms: 1.03x slower                                                          |
| logging_format           | 6.10 us                                                                     | 6.27 us: 1.03x slower                                                         |
| logging_simple           | 5.68 us                                                                     | 5.86 us: 1.03x slower                                                         |
| sympy_str                | 166 ms                                                                      | 172 ms: 1.03x slower                                                          |
| tomli_loads              | 1.17 sec                                                                    | 1.21 sec: 1.03x slower                                                        |
| nbody                    | 57.0 ms                                                                     | 59.0 ms: 1.03x slower                                                         |
| sympy_expand             | 283 ms                                                                      | 293 ms: 1.03x slower                                                          |
| sympy_sum                | 87.7 ms                                                                     | 90.9 ms: 1.04x slower                                                         |
| nqueens                  | 61.0 ms                                                                     | 63.3 ms: 1.04x slower                                                         |
| async_generators         | 234 ms                                                                      | 243 ms: 1.04x slower                                                          |
| sqlglot_normalize        | 178 ms                                                                      | 186 ms: 1.04x slower                                                          |
| chaos                    | 38.3 ms                                                                     | 40.0 ms: 1.04x slower                                                         |
| sympy_integrate          | 13.2 ms                                                                     | 13.8 ms: 1.04x slower                                                         |
| genshi_text              | 14.8 ms                                                                     | 15.4 ms: 1.04x slower                                                         |
| deepcopy_memo            | 21.0 us                                                                     | 21.9 us: 1.05x slower                                                         |
| deepcopy                 | 219 us                                                                      | 229 us: 1.05x slower                                                          |
| mypy2                    | 446 ms                                                                      | 467 ms: 1.05x slower                                                          |
| thrift                   | 8.76 ms                                                                     | 9.17 ms: 1.05x slower                                                         |
| sqlglot_optimize         | 34.4 ms                                                                     | 36.0 ms: 1.05x slower                                                         |
| typing_runtime_protocols | 71.8 us                                                                     | 75.2 us: 1.05x slower                                                         |
| meteor_contest           | 71.5 ms                                                                     | 76.1 ms: 1.06x slower                                                         |
| hexiom                   | 4.41 ms                                                                     | 4.81 ms: 1.09x slower                                                         |
| pickle_list              | 2.89 us                                                                     | 3.16 us: 1.09x slower                                                         |
| genshi_xml               | 32.4 ms                                                                     | 35.7 ms: 1.10x slower                                                         |
| mdp                      | 1.38 sec                                                                    | 1.53 sec: 1.11x slower                                                        |
| Geometric mean           | (ref)                                                                       | 1.02x slower                                                                  |

Benchmark hidden because not significant (22): pycparser, bench_thread_pool, pyflate, gc_traversal, python_startup, float, python_startup_no_site, crypto_pyaes, bench_mp_pool, regex_compile, async_tree_cpu_io_mixed_tg, deltablue, async_tree_cpu_io_mixed, pathlib, pickle_pure_python, async_tree_memoization_tg, asyncio_tcp_ssl, asyncio_tcp, async_tree_memoization, async_tree_none_tg, async_tree_io, async_tree_io_tg

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: unknown