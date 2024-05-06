# Results vs. base

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: darwin-arm64
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.02x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240422-darwin-arm64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 159 ms                                                                 | 162 ms: 1.02x slower                                                           |
| chameleon      | 4.48 ms                                                                | 4.62 ms: 1.03x slower                                                          |
| docutils       | 1.45 sec                                                               | 1.48 sec: 1.02x slower                                                         |
| html5lib       | 31.7 ms                                                                | 32.1 ms: 1.01x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                                   |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                        | bm-20240422-darwin-arm64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_eager_tg              | 44.0 ms                                                                | 43.5 ms: 1.01x faster                                                          |
| async_tree_eager_cpu_io_mixed_tg | 335 ms                                                                 | 336 ms: 1.00x slower                                                           |
| async_tree_io                    | 566 ms                                                                 | 576 ms: 1.02x slower                                                           |
| async_tree_none_tg               | 196 ms                                                                 | 200 ms: 1.02x slower                                                           |
| async_tree_io_tg                 | 558 ms                                                                 | 571 ms: 1.02x slower                                                           |
| async_tree_eager                 | 62.5 ms                                                                | 64.4 ms: 1.03x slower                                                          |
| Geometric mean                   | (ref)                                                                  | 1.01x slower                                                                   |

Benchmark hidden because not significant (10): async_tree_eager_memoization, async_tree_eager_cpu_io_mixed, async_tree_eager_memoization_tg, async_tree_eager_io, async_tree_memoization_tg, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_none, async_tree_memoization, async_tree_eager_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240422-darwin-arm64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 65.2 ms                                                                | 65.7 ms: 1.01x slower                                                          |
| float          | 50.7 ms                                                                | 52.2 ms: 1.03x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                   |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240422-darwin-arm64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_effbot   | 2.64 ms                                                                | 2.59 ms: 1.02x faster                                                          |
| regex_v8       | 17.4 ms                                                                | 17.5 ms: 1.00x slower                                                          |
| regex_dna      | 149 ms                                                                 | 150 ms: 1.01x slower                                                           |
| regex_compile  | 69.2 ms                                                                | 70.9 ms: 1.02x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240422-darwin-arm64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| unpickle_list        | 2.92 us                                                                | 2.90 us: 1.01x faster                                                          |
| pickle               | 7.42 us                                                                | 7.39 us: 1.01x faster                                                          |
| json_loads           | 17.1 us                                                                | 17.0 us: 1.00x faster                                                          |
| pickle_dict          | 18.3 us                                                                | 18.3 us: 1.00x slower                                                          |
| xml_etree_iterparse  | 68.1 ms                                                                | 68.5 ms: 1.01x slower                                                          |
| tomli_loads          | 1.50 sec                                                               | 1.51 sec: 1.01x slower                                                         |
| xml_etree_generate   | 54.5 ms                                                                | 55.1 ms: 1.01x slower                                                          |
| unpickle             | 9.21 us                                                                | 9.32 us: 1.01x slower                                                          |
| unpickle_pure_python | 142 us                                                                 | 145 us: 1.02x slower                                                           |
| pickle_pure_python   | 183 us                                                                 | 188 us: 1.03x slower                                                           |
| xml_etree_process    | 37.3 ms                                                                | 38.4 ms: 1.03x slower                                                          |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                                   |

Benchmark hidden because not significant (3): json_dumps, xml_etree_parse, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240422-darwin-arm64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                                | 11.9 ms: 1.03x slower                                                          |
| python_startup_no_site | 8.83 ms                                                                | 9.15 ms: 1.04x slower                                                          |
| Geometric mean         | (ref)                                                                  | 1.03x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240422-darwin-arm64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| django_template | 20.1 ms                                                                | 20.6 ms: 1.03x slower                                                          |
| mako            | 7.09 ms                                                                | 7.32 ms: 1.03x slower                                                          |
| Geometric mean  | (ref)                                                                  | 1.02x slower                                                                   |

Benchmark hidden because not significant (2): genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                        | bm-20240422-darwin-arm64-python-550483b7e6c54b2a25d4-3.13.0a6+-550483b | bm-20240422-darwin-arm64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_effbot                     | 2.64 ms                                                                | 2.59 ms: 1.02x faster                                                          |
| generators                       | 27.6 ms                                                                | 27.2 ms: 1.01x faster                                                          |
| async_tree_eager_tg              | 44.0 ms                                                                | 43.5 ms: 1.01x faster                                                          |
| unpickle_list                    | 2.92 us                                                                | 2.90 us: 1.01x faster                                                          |
| pickle                           | 7.42 us                                                                | 7.39 us: 1.01x faster                                                          |
| json_loads                       | 17.1 us                                                                | 17.0 us: 1.00x faster                                                          |
| nqueens                          | 55.4 ms                                                                | 55.2 ms: 1.00x faster                                                          |
| fannkuch                         | 257 ms                                                                 | 257 ms: 1.00x faster                                                           |
| mdp                              | 1.53 sec                                                               | 1.54 sec: 1.00x slower                                                         |
| scimark_sparse_mat_mult          | 3.01 ms                                                                | 3.02 ms: 1.00x slower                                                          |
| regex_v8                         | 17.4 ms                                                                | 17.5 ms: 1.00x slower                                                          |
| async_tree_eager_cpu_io_mixed_tg | 335 ms                                                                 | 336 ms: 1.00x slower                                                           |
| scimark_fft                      | 195 ms                                                                 | 195 ms: 1.00x slower                                                           |
| gc_traversal                     | 2.45 ms                                                                | 2.46 ms: 1.00x slower                                                          |
| pickle_dict                      | 18.3 us                                                                | 18.3 us: 1.00x slower                                                          |
| meteor_contest                   | 71.1 ms                                                                | 71.4 ms: 1.01x slower                                                          |
| bench_thread_pool                | 470 us                                                                 | 473 us: 1.01x slower                                                           |
| regex_dna                        | 149 ms                                                                 | 150 ms: 1.01x slower                                                           |
| xml_etree_iterparse              | 68.1 ms                                                                | 68.5 ms: 1.01x slower                                                          |
| sqlite_synth                     | 1.55 us                                                                | 1.56 us: 1.01x slower                                                          |
| sympy_integrate                  | 10.4 ms                                                                | 10.5 ms: 1.01x slower                                                          |
| nbody                            | 65.2 ms                                                                | 65.7 ms: 1.01x slower                                                          |
| deepcopy                         | 212 us                                                                 | 215 us: 1.01x slower                                                           |
| telco                            | 4.58 ms                                                                | 4.63 ms: 1.01x slower                                                          |
| dulwich_log                      | 27.8 ms                                                                | 28.1 ms: 1.01x slower                                                          |
| tomli_loads                      | 1.50 sec                                                               | 1.51 sec: 1.01x slower                                                         |
| scimark_monte_carlo              | 44.4 ms                                                                | 44.8 ms: 1.01x slower                                                          |
| thrift                           | 439 us                                                                 | 444 us: 1.01x slower                                                           |
| xml_etree_generate               | 54.5 ms                                                                | 55.1 ms: 1.01x slower                                                          |
| pathlib                          | 23.5 ms                                                                | 23.7 ms: 1.01x slower                                                          |
| html5lib                         | 31.7 ms                                                                | 32.1 ms: 1.01x slower                                                          |
| unpickle                         | 9.21 us                                                                | 9.32 us: 1.01x slower                                                          |
| async_generators                 | 286 ms                                                                 | 290 ms: 1.01x slower                                                           |
| logging_format                   | 3.43 us                                                                | 3.48 us: 1.01x slower                                                          |
| scimark_sor                      | 98.6 ms                                                                | 100 ms: 1.01x slower                                                           |
| crypto_pyaes                     | 46.6 ms                                                                | 47.4 ms: 1.02x slower                                                          |
| logging_simple                   | 3.15 us                                                                | 3.21 us: 1.02x slower                                                          |
| scimark_lu                       | 68.5 ms                                                                | 69.6 ms: 1.02x slower                                                          |
| pprint_pformat                   | 973 ms                                                                 | 989 ms: 1.02x slower                                                           |
| chaos                            | 36.3 ms                                                                | 36.9 ms: 1.02x slower                                                          |
| 2to3                             | 159 ms                                                                 | 162 ms: 1.02x slower                                                           |
| pprint_safe_repr                 | 478 ms                                                                 | 487 ms: 1.02x slower                                                           |
| async_tree_io                    | 566 ms                                                                 | 576 ms: 1.02x slower                                                           |
| coverage                         | 45.7 ms                                                                | 46.6 ms: 1.02x slower                                                          |
| go                               | 101 ms                                                                 | 102 ms: 1.02x slower                                                           |
| sympy_sum                        | 70.3 ms                                                                | 71.7 ms: 1.02x slower                                                          |
| docutils                         | 1.45 sec                                                               | 1.48 sec: 1.02x slower                                                         |
| sympy_expand                     | 227 ms                                                                 | 231 ms: 1.02x slower                                                           |
| sympy_str                        | 133 ms                                                                 | 136 ms: 1.02x slower                                                           |
| hexiom                           | 4.19 ms                                                                | 4.27 ms: 1.02x slower                                                          |
| pycparser                        | 639 ms                                                                 | 654 ms: 1.02x slower                                                           |
| deepcopy_reduce                  | 1.87 us                                                                | 1.91 us: 1.02x slower                                                          |
| async_tree_none_tg               | 196 ms                                                                 | 200 ms: 1.02x slower                                                           |
| async_tree_io_tg                 | 558 ms                                                                 | 571 ms: 1.02x slower                                                           |
| unpickle_pure_python             | 142 us                                                                 | 145 us: 1.02x slower                                                           |
| deepcopy_memo                    | 23.7 us                                                                | 24.3 us: 1.02x slower                                                          |
| regex_compile                    | 69.2 ms                                                                | 70.9 ms: 1.02x slower                                                          |
| coroutines                       | 17.0 ms                                                                | 17.4 ms: 1.02x slower                                                          |
| sqlglot_optimize                 | 31.3 ms                                                                | 32.1 ms: 1.03x slower                                                          |
| django_template                  | 20.1 ms                                                                | 20.6 ms: 1.03x slower                                                          |
| sqlglot_normalize                | 167 ms                                                                 | 172 ms: 1.03x slower                                                           |
| python_startup                   | 11.6 ms                                                                | 11.9 ms: 1.03x slower                                                          |
| typing_runtime_protocols         | 67.7 us                                                                | 69.5 us: 1.03x slower                                                          |
| pyflate                          | 322 ms                                                                 | 330 ms: 1.03x slower                                                           |
| create_gc_cycles                 | 873 us                                                                 | 897 us: 1.03x slower                                                           |
| pickle_pure_python               | 183 us                                                                 | 188 us: 1.03x slower                                                           |
| xml_etree_process                | 37.3 ms                                                                | 38.4 ms: 1.03x slower                                                          |
| float                            | 50.7 ms                                                                | 52.2 ms: 1.03x slower                                                          |
| async_tree_eager                 | 62.5 ms                                                                | 64.4 ms: 1.03x slower                                                          |
| raytrace                         | 152 ms                                                                 | 157 ms: 1.03x slower                                                           |
| chameleon                        | 4.48 ms                                                                | 4.62 ms: 1.03x slower                                                          |
| sqlglot_transpile                | 903 us                                                                 | 932 us: 1.03x slower                                                           |
| mako                             | 7.09 ms                                                                | 7.32 ms: 1.03x slower                                                          |
| logging_silent                   | 64.2 ns                                                                | 66.4 ns: 1.03x slower                                                          |
| sqlglot_parse                    | 747 us                                                                 | 772 us: 1.03x slower                                                           |
| python_startup_no_site           | 8.83 ms                                                                | 9.15 ms: 1.04x slower                                                          |
| richards_super                   | 34.2 ms                                                                | 35.8 ms: 1.05x slower                                                          |
| deltablue                        | 2.17 ms                                                                | 2.28 ms: 1.05x slower                                                          |
| richards                         | 30.8 ms                                                                | 32.4 ms: 1.05x slower                                                          |
| comprehensions                   | 10.5 us                                                                | 11.2 us: 1.07x slower                                                          |
| asyncio_tcp                      | 400 ms                                                                 | 430 ms: 1.07x slower                                                           |
| Geometric mean                   | (ref)                                                                  | 1.02x slower                                                                   |

Benchmark hidden because not significant (27): async_tree_eager_memoization, async_tree_eager_cpu_io_mixed, asyncio_tcp_ssl, pidigits, spectral_norm, asyncio_websockets, genshi_text, json_dumps, xml_etree_parse, genshi_xml, pickle_list, async_tree_eager_memoization_tg, json, dask, async_tree_eager_io, async_tree_memoization_tg, bench_mp_pool, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_none, pylint, async_tree_memoization, mypy2, gunicorn, async_tree_eager_io_tg, aiohttp, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.01x