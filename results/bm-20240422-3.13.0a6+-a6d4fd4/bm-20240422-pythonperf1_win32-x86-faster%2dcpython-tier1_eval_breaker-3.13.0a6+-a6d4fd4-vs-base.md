# Results vs. base

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: windows-x86
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.01x slower
- HPT reliability: 99.17%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240422-pythonperf1_win32-x86-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| 2to3           | 229 ms                                                                          | 232 ms: 1.01x slower                                                                    |
| docutils       | 1.80 sec                                                                        | 1.80 sec: 1.00x faster                                                                  |
| html5lib       | 43.5 ms                                                                         | 42.8 ms: 1.02x faster                                                                   |
| tornado_http   | 92.7 ms                                                                         | 94.0 ms: 1.01x slower                                                                   |
| Geometric mean | (ref)                                                                           | 1.00x slower                                                                            |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_memoization_tg, async_tree_none_tg, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_io, async_tree_none

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240422-pythonperf1_win32-x86-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| nbody          | 78.3 ms                                                                         | 76.4 ms: 1.03x faster                                                                   |
| pidigits       | 200 ms                                                                          | 197 ms: 1.01x faster                                                                    |
| Geometric mean | (ref)                                                                           | 1.01x faster                                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240422-pythonperf1_win32-x86-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| regex_v8       | 15.9 ms                                                                         | 16.1 ms: 1.02x slower                                                                   |
| regex_dna      | 116 ms                                                                          | 121 ms: 1.04x slower                                                                    |
| Geometric mean | (ref)                                                                           | 1.01x slower                                                                            |

Benchmark hidden because not significant (2): regex_compile, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240422-pythonperf1_win32-x86-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| xml_etree_generate   | 60.9 ms                                                                         | 60.0 ms: 1.02x faster                                                                   |
| unpickle             | 9.93 us                                                                         | 9.81 us: 1.01x faster                                                                   |
| xml_etree_process    | 42.7 ms                                                                         | 42.3 ms: 1.01x faster                                                                   |
| xml_etree_iterparse  | 65.3 ms                                                                         | 65.0 ms: 1.00x faster                                                                   |
| xml_etree_parse      | 106 ms                                                                          | 107 ms: 1.01x slower                                                                    |
| pickle_pure_python   | 207 us                                                                          | 209 us: 1.01x slower                                                                    |
| pickle_dict          | 20.1 us                                                                         | 20.4 us: 1.02x slower                                                                   |
| unpickle_pure_python | 138 us                                                                          | 140 us: 1.02x slower                                                                    |
| unpickle_list        | 2.81 us                                                                         | 2.86 us: 1.02x slower                                                                   |
| pickle_list          | 3.24 us                                                                         | 3.29 us: 1.02x slower                                                                   |
| json_dumps           | 6.77 ms                                                                         | 6.92 ms: 1.02x slower                                                                   |
| pickle               | 7.80 us                                                                         | 7.97 us: 1.02x slower                                                                   |
| tomli_loads          | 1.59 sec                                                                        | 1.63 sec: 1.02x slower                                                                  |
| json_loads           | 19.9 us                                                                         | 20.6 us: 1.03x slower                                                                   |
| Geometric mean       | (ref)                                                                           | 1.01x slower                                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240422-pythonperf1_win32-x86-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|------------------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| python_startup         | 21.8 ms                                                                         | 22.0 ms: 1.01x slower                                                                   |
| python_startup_no_site | 18.0 ms                                                                         | 18.3 ms: 1.02x slower                                                                   |
| Geometric mean         | (ref)                                                                           | 1.01x slower                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20240422-pythonperf1_win32-x86-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| genshi_text    | 19.0 ms                                                                         | 18.8 ms: 1.01x faster                                                                   |
| genshi_xml     | 43.1 ms                                                                         | 42.7 ms: 1.01x faster                                                                   |
| Geometric mean | (ref)                                                                           | 1.01x faster                                                                            |

Benchmark hidden because not significant (2): mako, django_template

All benchmarks:
===============

| Benchmark               | bm-20240422-pythonperf1_win32-x86-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-pythonperf1_win32-x86-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-------------------------|:-------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------:|
| deepcopy_reduce         | 2.51 us                                                                         | 2.36 us: 1.06x faster                                                                   |
| pprint_safe_repr        | 575 ms                                                                          | 558 ms: 1.03x faster                                                                    |
| nbody                   | 78.3 ms                                                                         | 76.4 ms: 1.03x faster                                                                   |
| scimark_lu              | 62.7 ms                                                                         | 61.4 ms: 1.02x faster                                                                   |
| pprint_pformat          | 1.17 sec                                                                        | 1.15 sec: 1.02x faster                                                                  |
| sqlglot_normalize       | 207 ms                                                                          | 203 ms: 1.02x faster                                                                    |
| deepcopy                | 268 us                                                                          | 264 us: 1.02x faster                                                                    |
| html5lib                | 43.5 ms                                                                         | 42.8 ms: 1.02x faster                                                                   |
| xml_etree_generate      | 60.9 ms                                                                         | 60.0 ms: 1.02x faster                                                                   |
| pidigits                | 200 ms                                                                          | 197 ms: 1.01x faster                                                                    |
| async_generators        | 284 ms                                                                          | 280 ms: 1.01x faster                                                                    |
| unpickle                | 9.93 us                                                                         | 9.81 us: 1.01x faster                                                                   |
| genshi_text             | 19.0 ms                                                                         | 18.8 ms: 1.01x faster                                                                   |
| genshi_xml              | 43.1 ms                                                                         | 42.7 ms: 1.01x faster                                                                   |
| sqlglot_transpile       | 1.11 ms                                                                         | 1.10 ms: 1.01x faster                                                                   |
| json                    | 4.16 ms                                                                         | 4.12 ms: 1.01x faster                                                                   |
| xml_etree_process       | 42.7 ms                                                                         | 42.3 ms: 1.01x faster                                                                   |
| sqlglot_parse           | 884 us                                                                          | 878 us: 1.01x faster                                                                    |
| sympy_integrate         | 14.6 ms                                                                         | 14.5 ms: 1.01x faster                                                                   |
| sqlglot_optimize        | 39.7 ms                                                                         | 39.5 ms: 1.01x faster                                                                   |
| xml_etree_iterparse     | 65.3 ms                                                                         | 65.0 ms: 1.00x faster                                                                   |
| docutils                | 1.80 sec                                                                        | 1.80 sec: 1.00x faster                                                                  |
| scimark_sparse_mat_mult | 3.10 ms                                                                         | 3.11 ms: 1.00x slower                                                                   |
| deepcopy_memo           | 22.8 us                                                                         | 22.9 us: 1.00x slower                                                                   |
| meteor_contest          | 74.8 ms                                                                         | 75.2 ms: 1.00x slower                                                                   |
| xml_etree_parse         | 106 ms                                                                          | 107 ms: 1.01x slower                                                                    |
| nqueens                 | 70.2 ms                                                                         | 70.6 ms: 1.01x slower                                                                   |
| deltablue               | 2.18 ms                                                                         | 2.20 ms: 1.01x slower                                                                   |
| generators              | 22.8 ms                                                                         | 23.0 ms: 1.01x slower                                                                   |
| pickle_pure_python      | 207 us                                                                          | 209 us: 1.01x slower                                                                    |
| sympy_sum               | 103 ms                                                                          | 104 ms: 1.01x slower                                                                    |
| logging_format          | 7.92 us                                                                         | 8.01 us: 1.01x slower                                                                   |
| sympy_str               | 203 ms                                                                          | 205 ms: 1.01x slower                                                                    |
| sqlite_synth            | 1.94 us                                                                         | 1.97 us: 1.01x slower                                                                   |
| python_startup          | 21.8 ms                                                                         | 22.0 ms: 1.01x slower                                                                   |
| fannkuch                | 276 ms                                                                          | 279 ms: 1.01x slower                                                                    |
| hexiom                  | 4.26 ms                                                                         | 4.32 ms: 1.01x slower                                                                   |
| tornado_http            | 92.7 ms                                                                         | 94.0 ms: 1.01x slower                                                                   |
| 2to3                    | 229 ms                                                                          | 232 ms: 1.01x slower                                                                    |
| mdp                     | 1.62 sec                                                                        | 1.64 sec: 1.01x slower                                                                  |
| logging_simple          | 7.37 us                                                                         | 7.47 us: 1.01x slower                                                                   |
| scimark_sor             | 79.7 ms                                                                         | 80.9 ms: 1.01x slower                                                                   |
| pickle_dict             | 20.1 us                                                                         | 20.4 us: 1.02x slower                                                                   |
| unpickle_pure_python    | 138 us                                                                          | 140 us: 1.02x slower                                                                    |
| regex_v8                | 15.9 ms                                                                         | 16.1 ms: 1.02x slower                                                                   |
| unpickle_list           | 2.81 us                                                                         | 2.86 us: 1.02x slower                                                                   |
| sympy_expand            | 354 ms                                                                          | 359 ms: 1.02x slower                                                                    |
| pickle_list             | 3.24 us                                                                         | 3.29 us: 1.02x slower                                                                   |
| python_startup_no_site  | 18.0 ms                                                                         | 18.3 ms: 1.02x slower                                                                   |
| thrift                  | 9.69 ms                                                                         | 9.88 ms: 1.02x slower                                                                   |
| pyflate                 | 309 ms                                                                          | 316 ms: 1.02x slower                                                                    |
| json_dumps              | 6.77 ms                                                                         | 6.92 ms: 1.02x slower                                                                   |
| coroutines              | 14.4 ms                                                                         | 14.7 ms: 1.02x slower                                                                   |
| pickle                  | 7.80 us                                                                         | 7.97 us: 1.02x slower                                                                   |
| tomli_loads             | 1.59 sec                                                                        | 1.63 sec: 1.02x slower                                                                  |
| raytrace                | 184 ms                                                                          | 189 ms: 1.03x slower                                                                    |
| spectral_norm           | 69.2 ms                                                                         | 71.0 ms: 1.03x slower                                                                   |
| go                      | 95.7 ms                                                                         | 98.3 ms: 1.03x slower                                                                   |
| scimark_monte_carlo     | 45.4 ms                                                                         | 46.7 ms: 1.03x slower                                                                   |
| richards                | 29.3 ms                                                                         | 30.3 ms: 1.03x slower                                                                   |
| logging_silent          | 57.9 ns                                                                         | 59.8 ns: 1.03x slower                                                                   |
| coverage                | 490 ms                                                                          | 506 ms: 1.03x slower                                                                    |
| json_loads              | 19.9 us                                                                         | 20.6 us: 1.03x slower                                                                   |
| regex_dna               | 116 ms                                                                          | 121 ms: 1.04x slower                                                                    |
| richards_super          | 32.5 ms                                                                         | 34.2 ms: 1.05x slower                                                                   |
| chaos                   | 46.1 ms                                                                         | 49.1 ms: 1.07x slower                                                                   |
| Geometric mean          | (ref)                                                                           | 1.01x slower                                                                            |

Benchmark hidden because not significant (28): mako, regex_compile, scimark_fft, crypto_pyaes, async_tree_cpu_io_mixed, comprehensions, async_tree_io_tg, async_tree_memoization_tg, pycparser, float, pathlib, gc_traversal, chameleon, async_tree_none_tg, typing_runtime_protocols, create_gc_cycles, telco, async_tree_cpu_io_mixed_tg, bench_mp_pool, async_tree_memoization, pylint, django_template, regex_effbot, asyncio_tcp_ssl, async_tree_io, bench_thread_pool, async_tree_none, asyncio_tcp

# HPT report

- Reliability score: 99.17% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown