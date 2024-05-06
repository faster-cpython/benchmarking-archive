# Results vs. base

- fork: faster-cpython
- ref: tier_2_call
- machine: darwin-arm64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.00x slower
- HPT reliability: 97.65%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240425-darwin-arm64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| chameleon      | 4.50 ms                                                                | 4.45 ms: 1.01x faster                                                   |
| html5lib       | 31.4 ms                                                                | 31.7 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (3): 2to3, docutils, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                     | bm-20240425-darwin-arm64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-------------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_tg           | 44.2 ms                                                                | 42.4 ms: 1.04x faster                                                   |
| async_tree_eager_memoization  | 157 ms                                                                 | 151 ms: 1.04x faster                                                    |
| async_tree_eager_cpu_io_mixed | 367 ms                                                                 | 362 ms: 1.01x faster                                                    |
| Geometric mean                | (ref)                                                                  | 1.00x faster                                                            |

Benchmark hidden because not significant (13): async_tree_eager, async_tree_eager_memoization_tg, async_tree_eager_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_eager_io_tg, async_tree_eager_io, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_memoization, async_tree_none_tg, async_tree_none, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240425-darwin-arm64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 51.5 ms                                                                | 51.1 ms: 1.01x faster                                                   |
| pidigits       | 282 ms                                                                 | 282 ms: 1.00x faster                                                    |
| nbody          | 69.6 ms                                                                | 69.9 ms: 1.00x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240425-darwin-arm64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 17.4 ms                                                                | 17.4 ms: 1.00x faster                                                   |
| regex_compile  | 69.0 ms                                                                | 69.1 ms: 1.00x slower                                                   |
| regex_effbot   | 2.56 ms                                                                | 2.62 ms: 1.02x slower                                                   |
| regex_dna      | 149 ms                                                                 | 153 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240425-darwin-arm64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_parse      | 106 ms                                                                 | 104 ms: 1.02x faster                                                    |
| pickle_pure_python   | 182 us                                                                 | 180 us: 1.01x faster                                                    |
| json_dumps           | 6.24 ms                                                                | 6.19 ms: 1.01x faster                                                   |
| unpickle_pure_python | 142 us                                                                 | 141 us: 1.00x faster                                                    |
| xml_etree_generate   | 54.4 ms                                                                | 54.5 ms: 1.00x slower                                                   |
| pickle               | 7.45 us                                                                | 7.48 us: 1.00x slower                                                   |
| xml_etree_iterparse  | 72.0 ms                                                                | 72.5 ms: 1.01x slower                                                   |
| xml_etree_process    | 37.3 ms                                                                | 37.8 ms: 1.01x slower                                                   |
| tomli_loads          | 1.49 sec                                                               | 1.51 sec: 1.02x slower                                                  |
| unpickle_list        | 2.94 us                                                                | 2.98 us: 1.02x slower                                                   |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (4): unpickle, pickle_list, pickle_dict, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240425-darwin-arm64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 10.5 ms                                                                | 10.2 ms: 1.03x faster                                                   |
| python_startup         | 13.3 ms                                                                | 13.0 ms: 1.02x faster                                                   |
| Geometric mean         | (ref)                                                                  | 1.03x faster                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240425-darwin-arm64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 7.17 ms                                                                | 7.12 ms: 1.01x faster                                                   |
| django_template | 19.9 ms                                                                | 20.1 ms: 1.01x slower                                                   |
| genshi_text     | 14.4 ms                                                                | 14.5 ms: 1.01x slower                                                   |
| genshi_xml      | 31.2 ms                                                                | 31.5 ms: 1.01x slower                                                   |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                     | bm-20240425-darwin-arm64-python-2c451489122d539080c8-3.13.0a6+-2c45148 | bm-20240426-darwin-arm64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-------------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_eager_tg           | 44.2 ms                                                                | 42.4 ms: 1.04x faster                                                   |
| async_tree_eager_memoization  | 157 ms                                                                 | 151 ms: 1.04x faster                                                    |
| python_startup_no_site        | 10.5 ms                                                                | 10.2 ms: 1.03x faster                                                   |
| logging_silent                | 63.8 ns                                                                | 62.3 ns: 1.02x faster                                                   |
| python_startup                | 13.3 ms                                                                | 13.0 ms: 1.02x faster                                                   |
| xml_etree_parse               | 106 ms                                                                 | 104 ms: 1.02x faster                                                    |
| coverage                      | 47.0 ms                                                                | 46.2 ms: 1.02x faster                                                   |
| async_tree_eager_cpu_io_mixed | 367 ms                                                                 | 362 ms: 1.01x faster                                                    |
| deepcopy_memo                 | 23.5 us                                                                | 23.2 us: 1.01x faster                                                   |
| chameleon                     | 4.50 ms                                                                | 4.45 ms: 1.01x faster                                                   |
| scimark_monte_carlo           | 44.7 ms                                                                | 44.3 ms: 1.01x faster                                                   |
| fannkuch                      | 258 ms                                                                 | 256 ms: 1.01x faster                                                    |
| async_generators              | 287 ms                                                                 | 285 ms: 1.01x faster                                                    |
| mako                          | 7.17 ms                                                                | 7.12 ms: 1.01x faster                                                   |
| pickle_pure_python            | 182 us                                                                 | 180 us: 1.01x faster                                                    |
| float                         | 51.5 ms                                                                | 51.1 ms: 1.01x faster                                                   |
| json_dumps                    | 6.24 ms                                                                | 6.19 ms: 1.01x faster                                                   |
| deepcopy                      | 210 us                                                                 | 209 us: 1.01x faster                                                    |
| sqlglot_transpile             | 911 us                                                                 | 906 us: 1.01x faster                                                    |
| scimark_sparse_mat_mult       | 2.99 ms                                                                | 2.97 ms: 1.00x faster                                                   |
| go                            | 101 ms                                                                 | 101 ms: 1.00x faster                                                    |
| pprint_safe_repr              | 472 ms                                                                 | 470 ms: 1.00x faster                                                    |
| sqlglot_parse                 | 750 us                                                                 | 747 us: 1.00x faster                                                    |
| unpickle_pure_python          | 142 us                                                                 | 141 us: 1.00x faster                                                    |
| regex_v8                      | 17.4 ms                                                                | 17.4 ms: 1.00x faster                                                   |
| richards_super                | 34.9 ms                                                                | 34.8 ms: 1.00x faster                                                   |
| sqlite_synth                  | 1.56 us                                                                | 1.55 us: 1.00x faster                                                   |
| pidigits                      | 282 ms                                                                 | 282 ms: 1.00x faster                                                    |
| xml_etree_generate            | 54.4 ms                                                                | 54.5 ms: 1.00x slower                                                   |
| regex_compile                 | 69.0 ms                                                                | 69.1 ms: 1.00x slower                                                   |
| chaos                         | 36.3 ms                                                                | 36.4 ms: 1.00x slower                                                   |
| deltablue                     | 2.19 ms                                                                | 2.19 ms: 1.00x slower                                                   |
| meteor_contest                | 71.1 ms                                                                | 71.3 ms: 1.00x slower                                                   |
| pickle                        | 7.45 us                                                                | 7.48 us: 1.00x slower                                                   |
| nbody                         | 69.6 ms                                                                | 69.9 ms: 1.00x slower                                                   |
| sqlglot_normalize             | 168 ms                                                                 | 169 ms: 1.00x slower                                                    |
| bench_thread_pool             | 469 us                                                                 | 471 us: 1.00x slower                                                    |
| sqlglot_optimize              | 31.4 ms                                                                | 31.6 ms: 1.01x slower                                                   |
| mdp                           | 1.52 sec                                                               | 1.53 sec: 1.01x slower                                                  |
| comprehensions                | 10.4 us                                                                | 10.5 us: 1.01x slower                                                   |
| xml_etree_iterparse           | 72.0 ms                                                                | 72.5 ms: 1.01x slower                                                   |
| logging_format                | 3.44 us                                                                | 3.46 us: 1.01x slower                                                   |
| django_template               | 19.9 ms                                                                | 20.1 ms: 1.01x slower                                                   |
| hexiom                        | 4.19 ms                                                                | 4.22 ms: 1.01x slower                                                   |
| create_gc_cycles              | 888 us                                                                 | 895 us: 1.01x slower                                                    |
| raytrace                      | 154 ms                                                                 | 155 ms: 1.01x slower                                                    |
| spectral_norm                 | 71.5 ms                                                                | 72.1 ms: 1.01x slower                                                   |
| html5lib                      | 31.4 ms                                                                | 31.7 ms: 1.01x slower                                                   |
| sympy_str                     | 133 ms                                                                 | 134 ms: 1.01x slower                                                    |
| deepcopy_reduce               | 1.87 us                                                                | 1.89 us: 1.01x slower                                                   |
| thrift                        | 443 us                                                                 | 448 us: 1.01x slower                                                    |
| genshi_text                   | 14.4 ms                                                                | 14.5 ms: 1.01x slower                                                   |
| genshi_xml                    | 31.2 ms                                                                | 31.5 ms: 1.01x slower                                                   |
| scimark_lu                    | 67.5 ms                                                                | 68.4 ms: 1.01x slower                                                   |
| xml_etree_process             | 37.3 ms                                                                | 37.8 ms: 1.01x slower                                                   |
| nqueens                       | 55.1 ms                                                                | 55.9 ms: 1.01x slower                                                   |
| tomli_loads                   | 1.49 sec                                                               | 1.51 sec: 1.02x slower                                                  |
| unpickle_list                 | 2.94 us                                                                | 2.98 us: 1.02x slower                                                   |
| sympy_expand                  | 227 ms                                                                 | 231 ms: 1.02x slower                                                    |
| coroutines                    | 16.4 ms                                                                | 16.8 ms: 1.02x slower                                                   |
| regex_effbot                  | 2.56 ms                                                                | 2.62 ms: 1.02x slower                                                   |
| pathlib                       | 23.5 ms                                                                | 24.0 ms: 1.02x slower                                                   |
| regex_dna                     | 149 ms                                                                 | 153 ms: 1.03x slower                                                    |
| generators                    | 27.3 ms                                                                | 28.9 ms: 1.06x slower                                                   |
| Geometric mean                | (ref)                                                                  | 1.00x slower                                                            |

Benchmark hidden because not significant (44): asyncio_tcp, bench_mp_pool, gunicorn, unpickle, async_tree_eager, 2to3, pycparser, pickle_list, telco, pickle_dict, pprint_pformat, logging_simple, json_loads, pyflate, crypto_pyaes, asyncio_tcp_ssl, richards, typing_runtime_protocols, async_tree_eager_memoization_tg, dulwich_log, gc_traversal, scimark_sor, asyncio_websockets, async_tree_eager_cpu_io_mixed_tg, scimark_fft, sympy_integrate, docutils, async_tree_memoization_tg, sympy_sum, async_tree_eager_io_tg, json, async_tree_eager_io, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, pylint, async_tree_io_tg, async_tree_memoization, async_tree_none_tg, async_tree_none, mypy2, dask, async_tree_io, tornado_http, aiohttp

# HPT report

- Reliability score: 97.65% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x