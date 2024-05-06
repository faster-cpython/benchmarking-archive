# Results vs. base

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.00x slower
- HPT reliability: 83.73%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240425-pythonperf2-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                                       | 286 ms: 1.00x slower                                                          |
| chameleon      | 7.22 ms                                                                      | 7.18 ms: 1.01x faster                                                         |
| docutils       | 2.98 sec                                                                     | 3.00 sec: 1.01x slower                                                        |
| Geometric mean | (ref)                                                                        | 1.00x slower                                                                  |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark      | bm-20240425-pythonperf2-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_io  | 900 ms                                                                       | 867 ms: 1.04x faster                                                          |
| Geometric mean | (ref)                                                                        | 1.01x faster                                                                  |

Benchmark hidden because not significant (7): async_tree_io_tg, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_none, async_tree_none_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240425-pythonperf2-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 75.7 ms                                                                      | 77.4 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                                  |

Benchmark hidden because not significant (2): nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240425-pythonperf2-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                                       | 142 ms: 1.00x slower                                                          |
| regex_v8       | 25.3 ms                                                                      | 26.5 ms: 1.05x slower                                                         |
| regex_effbot   | 3.40 ms                                                                      | 3.70 ms: 1.09x slower                                                         |
| Geometric mean | (ref)                                                                        | 1.03x slower                                                                  |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240425-pythonperf2-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|---------------------|:----------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| unpickle            | 15.9 us                                                                      | 15.3 us: 1.04x faster                                                         |
| pickle              | 10.7 us                                                                      | 10.4 us: 1.02x faster                                                         |
| pickle_dict         | 32.9 us                                                                      | 32.2 us: 1.02x faster                                                         |
| unpickle_list       | 4.67 us                                                                      | 4.58 us: 1.02x faster                                                         |
| json_dumps          | 10.5 ms                                                                      | 10.6 ms: 1.00x slower                                                         |
| xml_etree_generate  | 84.2 ms                                                                      | 84.8 ms: 1.01x slower                                                         |
| pickle_list         | 4.48 us                                                                      | 4.52 us: 1.01x slower                                                         |
| xml_etree_iterparse | 104 ms                                                                       | 106 ms: 1.02x slower                                                          |
| tomli_loads         | 2.19 sec                                                                     | 2.23 sec: 1.02x slower                                                        |
| xml_etree_process   | 57.7 ms                                                                      | 59.0 ms: 1.02x slower                                                         |
| xml_etree_parse     | 146 ms                                                                       | 150 ms: 1.02x slower                                                          |
| Geometric mean      | (ref)                                                                        | 1.00x slower                                                                  |

Benchmark hidden because not significant (3): json_loads, unpickle_pure_python, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240425-pythonperf2-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:----------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 8.82 ms                                                                      | 8.81 ms: 1.00x faster                                                         |
| Geometric mean         | (ref)                                                                        | 1.00x faster                                                                  |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240425-pythonperf2-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:----------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_text     | 25.4 ms                                                                      | 24.8 ms: 1.03x faster                                                         |
| genshi_xml      | 54.3 ms                                                                      | 54.0 ms: 1.01x faster                                                         |
| mako            | 10.0 ms                                                                      | 10.2 ms: 1.01x slower                                                         |
| django_template | 37.6 ms                                                                      | 38.7 ms: 1.03x slower                                                         |
| Geometric mean  | (ref)                                                                        | 1.00x slower                                                                  |

All benchmarks:
===============

| Benchmark                | bm-20240425-pythonperf2-x86_64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|--------------------------|:----------------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| gc_traversal             | 4.89 ms                                                                      | 4.42 ms: 1.11x faster                                                         |
| unpickle                 | 15.9 us                                                                      | 15.3 us: 1.04x faster                                                         |
| async_tree_io            | 900 ms                                                                       | 867 ms: 1.04x faster                                                          |
| genshi_text              | 25.4 ms                                                                      | 24.8 ms: 1.03x faster                                                         |
| pickle                   | 10.7 us                                                                      | 10.4 us: 1.02x faster                                                         |
| crypto_pyaes             | 73.0 ms                                                                      | 71.3 ms: 1.02x faster                                                         |
| scimark_lu               | 97.5 ms                                                                      | 95.4 ms: 1.02x faster                                                         |
| logging_silent           | 95.9 ns                                                                      | 93.9 ns: 1.02x faster                                                         |
| pickle_dict              | 32.9 us                                                                      | 32.2 us: 1.02x faster                                                         |
| unpickle_list            | 4.67 us                                                                      | 4.58 us: 1.02x faster                                                         |
| aiohttp                  | 1.09 ms                                                                      | 1.07 ms: 1.02x faster                                                         |
| create_gc_cycles         | 1.98 ms                                                                      | 1.95 ms: 1.02x faster                                                         |
| json                     | 5.46 ms                                                                      | 5.38 ms: 1.02x faster                                                         |
| spectral_norm            | 99.1 ms                                                                      | 97.8 ms: 1.01x faster                                                         |
| dulwich_log              | 67.1 ms                                                                      | 66.4 ms: 1.01x faster                                                         |
| pyflate                  | 459 ms                                                                       | 454 ms: 1.01x faster                                                          |
| asyncio_tcp              | 371 ms                                                                       | 367 ms: 1.01x faster                                                          |
| sympy_str                | 296 ms                                                                       | 294 ms: 1.01x faster                                                          |
| deltablue                | 3.24 ms                                                                      | 3.22 ms: 1.01x faster                                                         |
| genshi_xml               | 54.3 ms                                                                      | 54.0 ms: 1.01x faster                                                         |
| scimark_fft              | 302 ms                                                                       | 301 ms: 1.01x faster                                                          |
| chameleon                | 7.22 ms                                                                      | 7.18 ms: 1.01x faster                                                         |
| python_startup_no_site   | 8.82 ms                                                                      | 8.81 ms: 1.00x faster                                                         |
| pprint_safe_repr         | 796 ms                                                                       | 798 ms: 1.00x slower                                                          |
| 2to3                     | 285 ms                                                                       | 286 ms: 1.00x slower                                                          |
| hexiom                   | 5.97 ms                                                                      | 5.99 ms: 1.00x slower                                                         |
| json_dumps               | 10.5 ms                                                                      | 10.6 ms: 1.00x slower                                                         |
| sqlglot_transpile        | 1.76 ms                                                                      | 1.77 ms: 1.00x slower                                                         |
| regex_compile            | 141 ms                                                                       | 142 ms: 1.00x slower                                                          |
| sympy_integrate          | 23.1 ms                                                                      | 23.3 ms: 1.01x slower                                                         |
| fannkuch                 | 354 ms                                                                       | 356 ms: 1.01x slower                                                          |
| docutils                 | 2.98 sec                                                                     | 3.00 sec: 1.01x slower                                                        |
| xml_etree_generate       | 84.2 ms                                                                      | 84.8 ms: 1.01x slower                                                         |
| generators               | 33.1 ms                                                                      | 33.4 ms: 1.01x slower                                                         |
| pprint_pformat           | 1.62 sec                                                                     | 1.63 sec: 1.01x slower                                                        |
| sqlglot_optimize         | 58.4 ms                                                                      | 58.9 ms: 1.01x slower                                                         |
| pickle_list              | 4.48 us                                                                      | 4.52 us: 1.01x slower                                                         |
| mako                     | 10.0 ms                                                                      | 10.2 ms: 1.01x slower                                                         |
| meteor_contest           | 126 ms                                                                       | 128 ms: 1.01x slower                                                          |
| deepcopy_reduce          | 3.52 us                                                                      | 3.56 us: 1.01x slower                                                         |
| nqueens                  | 86.4 ms                                                                      | 87.6 ms: 1.01x slower                                                         |
| gunicorn                 | 1.04 ms                                                                      | 1.06 ms: 1.02x slower                                                         |
| richards_super           | 57.4 ms                                                                      | 58.4 ms: 1.02x slower                                                         |
| telco                    | 7.84 ms                                                                      | 7.97 ms: 1.02x slower                                                         |
| xml_etree_iterparse      | 104 ms                                                                       | 106 ms: 1.02x slower                                                          |
| tomli_loads              | 2.19 sec                                                                     | 2.23 sec: 1.02x slower                                                        |
| richards                 | 51.1 ms                                                                      | 52.0 ms: 1.02x slower                                                         |
| typing_runtime_protocols | 170 us                                                                       | 173 us: 1.02x slower                                                          |
| xml_etree_process        | 57.7 ms                                                                      | 59.0 ms: 1.02x slower                                                         |
| float                    | 75.7 ms                                                                      | 77.4 ms: 1.02x slower                                                         |
| scimark_sor              | 121 ms                                                                       | 123 ms: 1.02x slower                                                          |
| raytrace                 | 251 ms                                                                       | 257 ms: 1.02x slower                                                          |
| deepcopy_memo            | 38.0 us                                                                      | 38.9 us: 1.02x slower                                                         |
| xml_etree_parse          | 146 ms                                                                       | 150 ms: 1.02x slower                                                          |
| django_template          | 37.6 ms                                                                      | 38.7 ms: 1.03x slower                                                         |
| scimark_sparse_mat_mult  | 4.23 ms                                                                      | 4.36 ms: 1.03x slower                                                         |
| pycparser                | 1.22 sec                                                                     | 1.26 sec: 1.03x slower                                                        |
| coverage                 | 82.5 ms                                                                      | 85.3 ms: 1.03x slower                                                         |
| logging_format           | 6.77 us                                                                      | 7.03 us: 1.04x slower                                                         |
| go                       | 153 ms                                                                       | 160 ms: 1.04x slower                                                          |
| logging_simple           | 6.15 us                                                                      | 6.41 us: 1.04x slower                                                         |
| regex_v8                 | 25.3 ms                                                                      | 26.5 ms: 1.05x slower                                                         |
| regex_effbot             | 3.40 ms                                                                      | 3.70 ms: 1.09x slower                                                         |
| Geometric mean           | (ref)                                                                        | 1.00x slower                                                                  |

Benchmark hidden because not significant (37): bench_thread_pool, async_tree_io_tg, html5lib, coroutines, async_tree_memoization, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, scimark_monte_carlo, async_tree_none, nbody, bench_mp_pool, mdp, chaos, thrift, json_loads, asyncio_websockets, sqlglot_parse, sympy_sum, pidigits, sympy_expand, async_tree_none_tg, asyncio_tcp_ssl, regex_dna, python_startup, pathlib, async_tree_memoization_tg, async_generators, sqlglot_normalize, deepcopy, sqlite_synth, unpickle_pure_python, pickle_pure_python, comprehensions, pylint, tornado_http, mypy2, dask

# HPT report

- Reliability score: 83.73% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x