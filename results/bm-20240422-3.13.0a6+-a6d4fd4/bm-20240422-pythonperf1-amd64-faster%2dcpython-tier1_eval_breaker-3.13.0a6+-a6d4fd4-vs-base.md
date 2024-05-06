# Results vs. base

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: windows-amd64
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.01x slower
- HPT reliability: 99.87%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| 2to3           | 211 ms                                                                      | 213 ms: 1.01x slower                                                                |
| chameleon      | 4.69 ms                                                                     | 4.97 ms: 1.06x slower                                                               |
| docutils       | 1.66 sec                                                                    | 1.65 sec: 1.00x faster                                                              |
| Geometric mean | (ref)                                                                       | 1.01x slower                                                                        |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_none_tg, async_tree_none, async_tree_io_tg, async_tree_cpu_io_mixed, async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): float, pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| regex_compile  | 77.8 ms                                                                     | 80.5 ms: 1.03x slower                                                               |
| regex_effbot   | 1.56 ms                                                                     | 1.61 ms: 1.04x slower                                                               |
| regex_dna      | 115 ms                                                                      | 121 ms: 1.05x slower                                                                |
| Geometric mean | (ref)                                                                       | 1.04x slower                                                                        |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| pickle_list          | 3.06 us                                                                     | 2.92 us: 1.05x faster                                                               |
| xml_etree_parse      | 91.7 ms                                                                     | 90.2 ms: 1.02x faster                                                               |
| xml_etree_process    | 37.6 ms                                                                     | 37.9 ms: 1.01x slower                                                               |
| pickle               | 7.17 us                                                                     | 7.24 us: 1.01x slower                                                               |
| pickle_dict          | 18.5 us                                                                     | 18.8 us: 1.02x slower                                                               |
| unpickle             | 8.24 us                                                                     | 8.49 us: 1.03x slower                                                               |
| pickle_pure_python   | 179 us                                                                      | 184 us: 1.03x slower                                                                |
| unpickle_pure_python | 128 us                                                                      | 133 us: 1.04x slower                                                                |
| Geometric mean       | (ref)                                                                       | 1.01x slower                                                                        |

Benchmark hidden because not significant (6): unpickle_list, tomli_loads, xml_etree_generate, json_dumps, xml_etree_iterparse, json_loads

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-----------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| django_template | 21.9 ms                                                                     | 22.5 ms: 1.03x slower                                                               |
| mako            | 6.30 ms                                                                     | 6.56 ms: 1.04x slower                                                               |
| Geometric mean  | (ref)                                                                       | 1.01x slower                                                                        |

Benchmark hidden because not significant (2): genshi_xml, genshi_text

All benchmarks:
===============

| Benchmark               | bm-20240422-pythonperf1-amd64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-pythonperf1-amd64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-------------------------|:---------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| mdp                     | 1.46 sec                                                                    | 1.34 sec: 1.09x faster                                                              |
| json                    | 3.03 ms                                                                     | 2.87 ms: 1.06x faster                                                               |
| generators              | 22.1 ms                                                                     | 21.0 ms: 1.05x faster                                                               |
| pickle_list             | 3.06 us                                                                     | 2.92 us: 1.05x faster                                                               |
| logging_silent          | 59.1 ns                                                                     | 56.4 ns: 1.05x faster                                                               |
| richards                | 27.7 ms                                                                     | 26.7 ms: 1.04x faster                                                               |
| richards_super          | 31.5 ms                                                                     | 30.5 ms: 1.03x faster                                                               |
| xml_etree_parse         | 91.7 ms                                                                     | 90.2 ms: 1.02x faster                                                               |
| logging_format          | 6.41 us                                                                     | 6.35 us: 1.01x faster                                                               |
| pprint_pformat          | 994 ms                                                                      | 986 ms: 1.01x faster                                                                |
| raytrace                | 161 ms                                                                      | 160 ms: 1.01x faster                                                                |
| sqlglot_normalize       | 179 ms                                                                      | 177 ms: 1.01x faster                                                                |
| pprint_safe_repr        | 489 ms                                                                      | 486 ms: 1.01x faster                                                                |
| docutils                | 1.66 sec                                                                    | 1.65 sec: 1.00x faster                                                              |
| spectral_norm           | 63.8 ms                                                                     | 64.1 ms: 1.00x slower                                                               |
| scimark_sparse_mat_mult | 2.70 ms                                                                     | 2.72 ms: 1.00x slower                                                               |
| sqlglot_optimize        | 33.6 ms                                                                     | 33.8 ms: 1.01x slower                                                               |
| 2to3                    | 211 ms                                                                      | 213 ms: 1.01x slower                                                                |
| xml_etree_process       | 37.6 ms                                                                     | 37.9 ms: 1.01x slower                                                               |
| chaos                   | 38.7 ms                                                                     | 39.0 ms: 1.01x slower                                                               |
| deepcopy                | 222 us                                                                      | 223 us: 1.01x slower                                                                |
| aiohttp                 | 874 us                                                                      | 882 us: 1.01x slower                                                                |
| pickle                  | 7.17 us                                                                     | 7.24 us: 1.01x slower                                                               |
| deltablue               | 1.98 ms                                                                     | 2.00 ms: 1.01x slower                                                               |
| sympy_integrate         | 12.5 ms                                                                     | 12.6 ms: 1.01x slower                                                               |
| mypy2                   | 418 ms                                                                      | 424 ms: 1.02x slower                                                                |
| deepcopy_reduce         | 2.01 us                                                                     | 2.04 us: 1.02x slower                                                               |
| pickle_dict             | 18.5 us                                                                     | 18.8 us: 1.02x slower                                                               |
| hexiom                  | 3.84 ms                                                                     | 3.90 ms: 1.02x slower                                                               |
| meteor_contest          | 73.0 ms                                                                     | 74.3 ms: 1.02x slower                                                               |
| crypto_pyaes            | 45.4 ms                                                                     | 46.2 ms: 1.02x slower                                                               |
| fannkuch                | 255 ms                                                                      | 259 ms: 1.02x slower                                                                |
| sympy_str               | 161 ms                                                                      | 165 ms: 1.02x slower                                                                |
| dulwich_log             | 39.6 ms                                                                     | 40.5 ms: 1.02x slower                                                               |
| scimark_lu              | 56.5 ms                                                                     | 57.9 ms: 1.02x slower                                                               |
| nqueens                 | 58.5 ms                                                                     | 60.0 ms: 1.03x slower                                                               |
| django_template         | 21.9 ms                                                                     | 22.5 ms: 1.03x slower                                                               |
| sqlite_synth            | 1.62 us                                                                     | 1.66 us: 1.03x slower                                                               |
| sympy_expand            | 273 ms                                                                      | 281 ms: 1.03x slower                                                                |
| unpickle                | 8.24 us                                                                     | 8.49 us: 1.03x slower                                                               |
| pickle_pure_python      | 179 us                                                                      | 184 us: 1.03x slower                                                                |
| comprehensions          | 10.8 us                                                                     | 11.2 us: 1.03x slower                                                               |
| regex_compile           | 77.8 ms                                                                     | 80.5 ms: 1.03x slower                                                               |
| regex_effbot            | 1.56 ms                                                                     | 1.61 ms: 1.04x slower                                                               |
| scimark_fft             | 182 ms                                                                      | 189 ms: 1.04x slower                                                                |
| thrift                  | 8.01 ms                                                                     | 8.32 ms: 1.04x slower                                                               |
| mako                    | 6.30 ms                                                                     | 6.56 ms: 1.04x slower                                                               |
| scimark_sor             | 74.2 ms                                                                     | 77.5 ms: 1.04x slower                                                               |
| unpickle_pure_python    | 128 us                                                                      | 133 us: 1.04x slower                                                                |
| async_generators        | 230 ms                                                                      | 240 ms: 1.05x slower                                                                |
| coverage                | 46.0 ms                                                                     | 48.1 ms: 1.05x slower                                                               |
| regex_dna               | 115 ms                                                                      | 121 ms: 1.05x slower                                                                |
| telco                   | 4.89 ms                                                                     | 5.18 ms: 1.06x slower                                                               |
| chameleon               | 4.69 ms                                                                     | 4.97 ms: 1.06x slower                                                               |
| deepcopy_memo           | 21.7 us                                                                     | 23.0 us: 1.06x slower                                                               |
| scimark_monte_carlo     | 40.0 ms                                                                     | 44.1 ms: 1.10x slower                                                               |
| Geometric mean          | (ref)                                                                       | 1.01x slower                                                                        |

Benchmark hidden because not significant (41): pycparser, asyncio_tcp_ssl, create_gc_cycles, async_tree_none_tg, async_tree_none, unpickle_list, async_tree_io_tg, genshi_xml, tomli_loads, sqlglot_transpile, coroutines, float, genshi_text, go, html5lib, logging_simple, bench_thread_pool, sqlglot_parse, async_tree_cpu_io_mixed, xml_etree_generate, async_tree_io, pathlib, tornado_http, pidigits, nbody, gc_traversal, json_dumps, sympy_sum, bench_mp_pool, async_tree_cpu_io_mixed_tg, xml_etree_iterparse, json_loads, async_tree_memoization, async_tree_memoization_tg, asyncio_tcp, python_startup_no_site, python_startup, pylint, typing_runtime_protocols, pyflate, regex_v8

# HPT report

- Reliability score: 99.87% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown