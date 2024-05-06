# Results vs. base

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: linux-x86_64
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.00x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240422-pythonperf2-x86_64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                                       | 287 ms: 1.01x slower                                                                 |
| chameleon      | 7.15 ms                                                                      | 7.29 ms: 1.02x slower                                                                |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                                         |

Benchmark hidden because not significant (3): docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_memoization_tg, async_tree_none_tg, async_tree_io, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_none, async_tree_io_tg, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240422-pythonperf2-x86_64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| float          | 75.4 ms                                                                      | 77.2 ms: 1.02x slower                                                                |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                                         |

Benchmark hidden because not significant (2): pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240422-pythonperf2-x86_64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| regex_effbot   | 3.46 ms                                                                      | 3.47 ms: 1.00x slower                                                                |
| regex_dna      | 236 ms                                                                       | 238 ms: 1.01x slower                                                                 |
| regex_v8       | 25.5 ms                                                                      | 26.0 ms: 1.02x slower                                                                |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                                         |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240422-pythonperf2-x86_64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| unpickle             | 15.6 us                                                                      | 14.8 us: 1.06x faster                                                                |
| unpickle_pure_python | 214 us                                                                       | 204 us: 1.05x faster                                                                 |
| xml_etree_iterparse  | 106 ms                                                                       | 104 ms: 1.03x faster                                                                 |
| xml_etree_parse      | 149 ms                                                                       | 146 ms: 1.02x faster                                                                 |
| pickle_list          | 4.53 us                                                                      | 4.44 us: 1.02x faster                                                                |
| unpickle_list        | 4.65 us                                                                      | 4.56 us: 1.02x faster                                                                |
| pickle_dict          | 33.5 us                                                                      | 33.3 us: 1.01x faster                                                                |
| xml_etree_generate   | 84.8 ms                                                                      | 85.1 ms: 1.00x slower                                                                |
| json_loads           | 24.7 us                                                                      | 24.8 us: 1.00x slower                                                                |
| json_dumps           | 10.5 ms                                                                      | 10.6 ms: 1.01x slower                                                                |
| xml_etree_process    | 58.8 ms                                                                      | 59.6 ms: 1.01x slower                                                                |
| pickle_pure_python   | 305 us                                                                       | 310 us: 1.02x slower                                                                 |
| Geometric mean       | (ref)                                                                        | 1.01x faster                                                                         |

Benchmark hidden because not significant (2): tomli_loads, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240422-pythonperf2-x86_64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|------------------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| python_startup         | 12.9 ms                                                                      | 12.9 ms: 1.00x faster                                                                |
| python_startup_no_site | 8.83 ms                                                                      | 8.84 ms: 1.00x slower                                                                |
| Geometric mean         | (ref)                                                                        | 1.00x faster                                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240422-pythonperf2-x86_64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-----------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| django_template | 38.0 ms                                                                      | 38.8 ms: 1.02x slower                                                                |
| genshi_xml      | 55.1 ms                                                                      | 56.2 ms: 1.02x slower                                                                |
| mako            | 10.1 ms                                                                      | 10.5 ms: 1.03x slower                                                                |
| genshi_text     | 25.0 ms                                                                      | 26.4 ms: 1.06x slower                                                                |
| Geometric mean  | (ref)                                                                        | 1.03x slower                                                                         |

All benchmarks:
===============

| Benchmark               | bm-20240422-pythonperf2-x86_64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-------------------------|:----------------------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| unpickle                | 15.6 us                                                                      | 14.8 us: 1.06x faster                                                                |
| gc_traversal            | 4.65 ms                                                                      | 4.42 ms: 1.05x faster                                                                |
| unpickle_pure_python    | 214 us                                                                       | 204 us: 1.05x faster                                                                 |
| scimark_fft             | 310 ms                                                                       | 298 ms: 1.04x faster                                                                 |
| bench_thread_pool       | 917 us                                                                       | 884 us: 1.04x faster                                                                 |
| raytrace                | 261 ms                                                                       | 253 ms: 1.03x faster                                                                 |
| xml_etree_iterparse     | 106 ms                                                                       | 104 ms: 1.03x faster                                                                 |
| logging_format          | 7.07 us                                                                      | 6.91 us: 1.02x faster                                                                |
| xml_etree_parse         | 149 ms                                                                       | 146 ms: 1.02x faster                                                                 |
| pickle_list             | 4.53 us                                                                      | 4.44 us: 1.02x faster                                                                |
| chaos                   | 59.7 ms                                                                      | 58.6 ms: 1.02x faster                                                                |
| pathlib                 | 17.4 ms                                                                      | 17.1 ms: 1.02x faster                                                                |
| logging_simple          | 6.44 us                                                                      | 6.32 us: 1.02x faster                                                                |
| unpickle_list           | 4.65 us                                                                      | 4.56 us: 1.02x faster                                                                |
| coroutines              | 21.4 ms                                                                      | 21.2 ms: 1.01x faster                                                                |
| fannkuch                | 365 ms                                                                       | 361 ms: 1.01x faster                                                                 |
| pyflate                 | 473 ms                                                                       | 468 ms: 1.01x faster                                                                 |
| sympy_integrate         | 23.4 ms                                                                      | 23.1 ms: 1.01x faster                                                                |
| thrift                  | 910 us                                                                       | 900 us: 1.01x faster                                                                 |
| scimark_sparse_mat_mult | 4.36 ms                                                                      | 4.32 ms: 1.01x faster                                                                |
| scimark_sor             | 120 ms                                                                       | 119 ms: 1.01x faster                                                                 |
| pickle_dict             | 33.5 us                                                                      | 33.3 us: 1.01x faster                                                                |
| go                      | 156 ms                                                                       | 155 ms: 1.01x faster                                                                 |
| generators              | 33.3 ms                                                                      | 33.1 ms: 1.01x faster                                                                |
| python_startup          | 12.9 ms                                                                      | 12.9 ms: 1.00x faster                                                                |
| python_startup_no_site  | 8.83 ms                                                                      | 8.84 ms: 1.00x slower                                                                |
| xml_etree_generate      | 84.8 ms                                                                      | 85.1 ms: 1.00x slower                                                                |
| regex_effbot            | 3.46 ms                                                                      | 3.47 ms: 1.00x slower                                                                |
| sqlglot_normalize       | 117 ms                                                                       | 117 ms: 1.00x slower                                                                 |
| json_loads              | 24.7 us                                                                      | 24.8 us: 1.00x slower                                                                |
| coverage                | 85.9 ms                                                                      | 86.3 ms: 1.00x slower                                                                |
| meteor_contest          | 127 ms                                                                       | 127 ms: 1.00x slower                                                                 |
| async_generators        | 354 ms                                                                       | 356 ms: 1.00x slower                                                                 |
| regex_dna               | 236 ms                                                                       | 238 ms: 1.01x slower                                                                 |
| deepcopy                | 376 us                                                                       | 379 us: 1.01x slower                                                                 |
| telco                   | 8.00 ms                                                                      | 8.06 ms: 1.01x slower                                                                |
| 2to3                    | 285 ms                                                                       | 287 ms: 1.01x slower                                                                 |
| sympy_str               | 295 ms                                                                       | 298 ms: 1.01x slower                                                                 |
| crypto_pyaes            | 72.0 ms                                                                      | 72.6 ms: 1.01x slower                                                                |
| logging_silent          | 93.8 ns                                                                      | 94.6 ns: 1.01x slower                                                                |
| sqlglot_optimize        | 58.5 ms                                                                      | 59.0 ms: 1.01x slower                                                                |
| pprint_safe_repr        | 793 ms                                                                       | 801 ms: 1.01x slower                                                                 |
| json_dumps              | 10.5 ms                                                                      | 10.6 ms: 1.01x slower                                                                |
| pycparser               | 1.27 sec                                                                     | 1.28 sec: 1.01x slower                                                               |
| richards                | 51.0 ms                                                                      | 51.5 ms: 1.01x slower                                                                |
| sympy_expand            | 498 ms                                                                       | 504 ms: 1.01x slower                                                                 |
| mdp                     | 2.47 sec                                                                     | 2.50 sec: 1.01x slower                                                               |
| xml_etree_process       | 58.8 ms                                                                      | 59.6 ms: 1.01x slower                                                                |
| json                    | 5.39 ms                                                                      | 5.46 ms: 1.01x slower                                                                |
| asyncio_websockets      | 391 ms                                                                       | 396 ms: 1.01x slower                                                                 |
| comprehensions          | 16.6 us                                                                      | 16.8 us: 1.01x slower                                                                |
| pprint_pformat          | 1.61 sec                                                                     | 1.64 sec: 1.02x slower                                                               |
| pickle_pure_python      | 305 us                                                                       | 310 us: 1.02x slower                                                                 |
| regex_v8                | 25.5 ms                                                                      | 26.0 ms: 1.02x slower                                                                |
| chameleon               | 7.15 ms                                                                      | 7.29 ms: 1.02x slower                                                                |
| django_template         | 38.0 ms                                                                      | 38.8 ms: 1.02x slower                                                                |
| genshi_xml              | 55.1 ms                                                                      | 56.2 ms: 1.02x slower                                                                |
| deltablue               | 3.25 ms                                                                      | 3.32 ms: 1.02x slower                                                                |
| float                   | 75.4 ms                                                                      | 77.2 ms: 1.02x slower                                                                |
| hexiom                  | 5.94 ms                                                                      | 6.10 ms: 1.03x slower                                                                |
| dulwich_log             | 65.8 ms                                                                      | 67.7 ms: 1.03x slower                                                                |
| scimark_lu              | 95.6 ms                                                                      | 98.6 ms: 1.03x slower                                                                |
| mako                    | 10.1 ms                                                                      | 10.5 ms: 1.03x slower                                                                |
| deepcopy_memo           | 36.6 us                                                                      | 37.9 us: 1.04x slower                                                                |
| scimark_monte_carlo     | 60.8 ms                                                                      | 63.2 ms: 1.04x slower                                                                |
| genshi_text             | 25.0 ms                                                                      | 26.4 ms: 1.06x slower                                                                |
| Geometric mean          | (ref)                                                                        | 1.00x slower                                                                         |

Benchmark hidden because not significant (34): aiohttp, deepcopy_reduce, sqlglot_parse, richards_super, async_tree_memoization_tg, tomli_loads, sqlglot_transpile, spectral_norm, pidigits, sympy_sum, regex_compile, async_tree_none_tg, dask, nqueens, asyncio_tcp_ssl, asyncio_tcp, pickle, docutils, gunicorn, mypy2, html5lib, async_tree_io, sqlite_synth, typing_runtime_protocols, tornado_http, bench_mp_pool, async_tree_cpu_io_mixed, async_tree_memoization, async_tree_none, pylint, async_tree_io_tg, async_tree_cpu_io_mixed_tg, nbody, create_gc_cycles

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x