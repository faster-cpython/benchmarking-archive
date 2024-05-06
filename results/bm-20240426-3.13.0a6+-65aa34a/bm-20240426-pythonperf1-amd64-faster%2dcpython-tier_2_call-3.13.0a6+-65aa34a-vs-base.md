# Results vs. base

- fork: faster-cpython
- ref: tier_2_call
- machine: windows-amd64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.00x slower
- HPT reliability: 96.61%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240425-pythonperf1-amd64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:---------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 215 ms                                                                      | 217 ms: 1.01x slower                                                         |
| chameleon      | 4.87 ms                                                                     | 5.05 ms: 1.04x slower                                                        |
| docutils       | 1.67 sec                                                                    | 1.65 sec: 1.01x faster                                                       |
| html5lib       | 35.4 ms                                                                     | 36.5 ms: 1.03x slower                                                        |
| tornado_http   | 92.0 ms                                                                     | 90.9 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                                       | 1.01x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_none_tg, async_tree_io, async_tree_none, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240425-pythonperf1-amd64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:---------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 74.8 ms                                                                     | 72.9 ms: 1.03x faster                                                        |
| float          | 50.9 ms                                                                     | 51.5 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                                       | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240425-pythonperf1-amd64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:---------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 16.4 ms                                                                     | 14.6 ms: 1.12x faster                                                        |
| regex_compile  | 80.7 ms                                                                     | 79.4 ms: 1.02x faster                                                        |
| regex_dna      | 115 ms                                                                      | 114 ms: 1.01x faster                                                         |
| regex_effbot   | 1.56 ms                                                                     | 1.57 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                                       | 1.03x faster                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240425-pythonperf1-amd64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:---------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_dict          | 19.9 us                                                                     | 18.4 us: 1.08x faster                                                        |
| unpickle_list        | 2.87 us                                                                     | 2.78 us: 1.03x faster                                                        |
| pickle_pure_python   | 179 us                                                                      | 176 us: 1.02x faster                                                         |
| json_loads           | 13.9 us                                                                     | 13.7 us: 1.02x faster                                                        |
| pickle               | 7.38 us                                                                     | 7.27 us: 1.02x faster                                                        |
| xml_etree_process    | 38.0 ms                                                                     | 37.6 ms: 1.01x faster                                                        |
| json_dumps           | 5.77 ms                                                                     | 5.83 ms: 1.01x slower                                                        |
| tomli_loads          | 1.41 sec                                                                    | 1.45 sec: 1.03x slower                                                       |
| unpickle_pure_python | 129 us                                                                      | 133 us: 1.03x slower                                                         |
| Geometric mean       | (ref)                                                                       | 1.01x faster                                                                 |

Benchmark hidden because not significant (5): xml_etree_parse, pickle_list, xml_etree_iterparse, xml_etree_generate, unpickle

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240425-pythonperf1-amd64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:---------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 22.9 ms                                                                     | 22.4 ms: 1.02x faster                                                        |
| genshi_xml      | 33.1 ms                                                                     | 34.4 ms: 1.04x slower                                                        |
| Geometric mean  | (ref)                                                                       | 1.01x slower                                                                 |

Benchmark hidden because not significant (2): genshi_text, mako

All benchmarks:
===============

| Benchmark                | bm-20240425-pythonperf1-amd64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-pythonperf1-amd64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|--------------------------|:---------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8                 | 16.4 ms                                                                     | 14.6 ms: 1.12x faster                                                        |
| pickle_dict              | 19.9 us                                                                     | 18.4 us: 1.08x faster                                                        |
| unpickle_list            | 2.87 us                                                                     | 2.78 us: 1.03x faster                                                        |
| scimark_sor              | 79.8 ms                                                                     | 77.7 ms: 1.03x faster                                                        |
| nbody                    | 74.8 ms                                                                     | 72.9 ms: 1.03x faster                                                        |
| django_template          | 22.9 ms                                                                     | 22.4 ms: 1.02x faster                                                        |
| create_gc_cycles         | 919 us                                                                      | 901 us: 1.02x faster                                                         |
| nqueens                  | 61.8 ms                                                                     | 60.6 ms: 1.02x faster                                                        |
| pickle_pure_python       | 179 us                                                                      | 176 us: 1.02x faster                                                         |
| pyflate                  | 293 ms                                                                      | 288 ms: 1.02x faster                                                         |
| json_loads               | 13.9 us                                                                     | 13.7 us: 1.02x faster                                                        |
| regex_compile            | 80.7 ms                                                                     | 79.4 ms: 1.02x faster                                                        |
| hexiom                   | 3.95 ms                                                                     | 3.88 ms: 1.02x faster                                                        |
| pickle                   | 7.38 us                                                                     | 7.27 us: 1.02x faster                                                        |
| sympy_integrate          | 12.7 ms                                                                     | 12.5 ms: 1.01x faster                                                        |
| dulwich_log              | 40.5 ms                                                                     | 39.9 ms: 1.01x faster                                                        |
| crypto_pyaes             | 46.1 ms                                                                     | 45.4 ms: 1.01x faster                                                        |
| chaos                    | 39.6 ms                                                                     | 39.1 ms: 1.01x faster                                                        |
| tornado_http             | 92.0 ms                                                                     | 90.9 ms: 1.01x faster                                                        |
| xml_etree_process        | 38.0 ms                                                                     | 37.6 ms: 1.01x faster                                                        |
| docutils                 | 1.67 sec                                                                    | 1.65 sec: 1.01x faster                                                       |
| pprint_safe_repr         | 496 ms                                                                      | 492 ms: 1.01x faster                                                         |
| logging_simple           | 6.10 us                                                                     | 6.05 us: 1.01x faster                                                        |
| comprehensions           | 10.8 us                                                                     | 10.7 us: 1.01x faster                                                        |
| sympy_str                | 163 ms                                                                      | 162 ms: 1.01x faster                                                         |
| gc_traversal             | 1.57 ms                                                                     | 1.56 ms: 1.01x faster                                                        |
| deepcopy                 | 222 us                                                                      | 221 us: 1.01x faster                                                         |
| regex_dna                | 115 ms                                                                      | 114 ms: 1.01x faster                                                         |
| pprint_pformat           | 1.00 sec                                                                    | 999 ms: 1.00x faster                                                         |
| scimark_fft              | 196 ms                                                                      | 197 ms: 1.00x slower                                                         |
| deepcopy_memo            | 22.7 us                                                                     | 22.9 us: 1.01x slower                                                        |
| regex_effbot             | 1.56 ms                                                                     | 1.57 ms: 1.01x slower                                                        |
| sqlglot_parse            | 776 us                                                                      | 781 us: 1.01x slower                                                         |
| 2to3                     | 215 ms                                                                      | 217 ms: 1.01x slower                                                         |
| logging_format           | 6.48 us                                                                     | 6.53 us: 1.01x slower                                                        |
| json_dumps               | 5.77 ms                                                                     | 5.83 ms: 1.01x slower                                                        |
| sqlglot_transpile        | 983 us                                                                      | 994 us: 1.01x slower                                                         |
| sqlite_synth             | 1.65 us                                                                     | 1.67 us: 1.01x slower                                                        |
| pathlib                  | 81.3 ms                                                                     | 82.3 ms: 1.01x slower                                                        |
| float                    | 50.9 ms                                                                     | 51.5 ms: 1.01x slower                                                        |
| deltablue                | 2.02 ms                                                                     | 2.05 ms: 1.01x slower                                                        |
| spectral_norm            | 64.6 ms                                                                     | 65.5 ms: 1.01x slower                                                        |
| deepcopy_reduce          | 2.02 us                                                                     | 2.05 us: 1.01x slower                                                        |
| sqlglot_optimize         | 33.5 ms                                                                     | 34.2 ms: 1.02x slower                                                        |
| typing_runtime_protocols | 106 us                                                                      | 109 us: 1.02x slower                                                         |
| raytrace                 | 162 ms                                                                      | 166 ms: 1.03x slower                                                         |
| tomli_loads              | 1.41 sec                                                                    | 1.45 sec: 1.03x slower                                                       |
| mdp                      | 1.39 sec                                                                    | 1.43 sec: 1.03x slower                                                       |
| sqlglot_normalize        | 176 ms                                                                      | 181 ms: 1.03x slower                                                         |
| richards_super           | 31.5 ms                                                                     | 32.4 ms: 1.03x slower                                                        |
| unpickle_pure_python     | 129 us                                                                      | 133 us: 1.03x slower                                                         |
| html5lib                 | 35.4 ms                                                                     | 36.5 ms: 1.03x slower                                                        |
| async_generators         | 235 ms                                                                      | 242 ms: 1.03x slower                                                         |
| generators               | 21.5 ms                                                                     | 22.3 ms: 1.04x slower                                                        |
| chameleon                | 4.87 ms                                                                     | 5.05 ms: 1.04x slower                                                        |
| thrift                   | 8.12 ms                                                                     | 8.42 ms: 1.04x slower                                                        |
| scimark_sparse_mat_mult  | 2.77 ms                                                                     | 2.88 ms: 1.04x slower                                                        |
| genshi_xml               | 33.1 ms                                                                     | 34.4 ms: 1.04x slower                                                        |
| richards                 | 27.6 ms                                                                     | 28.7 ms: 1.04x slower                                                        |
| go                       | 86.0 ms                                                                     | 90.7 ms: 1.05x slower                                                        |
| asyncio_tcp              | 625 ms                                                                      | 664 ms: 1.06x slower                                                         |
| coverage                 | 46.8 ms                                                                     | 50.6 ms: 1.08x slower                                                        |
| Geometric mean           | (ref)                                                                       | 1.00x slower                                                                 |

Benchmark hidden because not significant (35): pycparser, asyncio_tcp_ssl, json, xml_etree_parse, async_tree_cpu_io_mixed_tg, scimark_monte_carlo, aiohttp, telco, pickle_list, pidigits, coroutines, async_tree_cpu_io_mixed, bench_mp_pool, logging_silent, xml_etree_iterparse, sympy_expand, meteor_contest, async_tree_io_tg, genshi_text, pylint, fannkuch, bench_thread_pool, xml_etree_generate, mypy2, sympy_sum, scimark_lu, python_startup_no_site, unpickle, mako, python_startup, async_tree_none_tg, async_tree_io, async_tree_none, async_tree_memoization, async_tree_memoization_tg

# HPT report

- Reliability score: 96.61% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown