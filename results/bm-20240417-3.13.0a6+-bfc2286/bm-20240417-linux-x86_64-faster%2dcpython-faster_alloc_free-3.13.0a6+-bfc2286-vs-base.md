# Results vs. base

- fork: faster-cpython
- ref: faster_alloc_free
- machine: linux-x86_64
- commit hash: bfc2286
- commit date: 2024-04-17
- overall geometric mean: 1.00x slower
- HPT reliability: 74.83%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 270 ms                                                                 | 272 ms: 1.01x slower                                                          |
| chameleon      | 6.94 ms                                                                | 7.12 ms: 1.03x slower                                                         |
| docutils       | 2.83 sec                                                               | 2.84 sec: 1.00x slower                                                        |
| html5lib       | 67.3 ms                                                                | 68.6 ms: 1.02x slower                                                         |
| tornado_http   | 93.9 ms                                                                | 94.6 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_memoization, async_tree_none, async_tree_none_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 206 ms                                                                 | 190 ms: 1.09x faster                                                          |
| nbody          | 90.0 ms                                                                | 84.7 ms: 1.06x faster                                                         |
| float          | 78.7 ms                                                                | 77.6 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_effbot   | 3.74 ms                                                                | 3.73 ms: 1.00x faster                                                         |
| regex_compile  | 136 ms                                                                 | 136 ms: 1.01x slower                                                          |
| regex_dna      | 218 ms                                                                 | 224 ms: 1.03x slower                                                          |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                                  |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| xml_etree_generate   | 88.8 ms                                                                | 88.3 ms: 1.00x faster                                                         |
| json_dumps           | 10.5 ms                                                                | 10.6 ms: 1.01x slower                                                         |
| pickle_list          | 5.33 us                                                                | 5.41 us: 1.02x slower                                                         |
| pickle_pure_python   | 299 us                                                                 | 305 us: 1.02x slower                                                          |
| unpickle             | 15.2 us                                                                | 15.5 us: 1.02x slower                                                         |
| unpickle_pure_python | 217 us                                                                 | 222 us: 1.02x slower                                                          |
| pickle               | 11.8 us                                                                | 12.1 us: 1.02x slower                                                         |
| tomli_loads          | 2.17 sec                                                               | 2.24 sec: 1.03x slower                                                        |
| unpickle_list        | 4.99 us                                                                | 5.24 us: 1.05x slower                                                         |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                                  |

Benchmark hidden because not significant (5): xml_etree_parse, xml_etree_iterparse, json_loads, xml_etree_process, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 7.11 ms                                                                | 7.07 ms: 1.01x faster                                                         |
| python_startup         | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                         |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| django_template | 35.8 ms                                                                | 35.1 ms: 1.02x faster                                                         |
| genshi_text     | 23.4 ms                                                                | 23.7 ms: 1.01x slower                                                         |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                                  |

Benchmark hidden because not significant (2): genshi_xml, mako

All benchmarks:
===============

| Benchmark              | bm-20240416-linux-x86_64-python-c520bf9bdf77d43c3d5d-3.13.0a6+-c520bf9 | bm-20240417-linux-x86_64-faster%2dcpython-faster_alloc_free-3.13.0a6+-bfc2286 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits               | 206 ms                                                                 | 190 ms: 1.09x faster                                                          |
| nbody                  | 90.0 ms                                                                | 84.7 ms: 1.06x faster                                                         |
| generators             | 30.9 ms                                                                | 29.5 ms: 1.05x faster                                                         |
| gc_traversal           | 3.87 ms                                                                | 3.76 ms: 1.03x faster                                                         |
| crypto_pyaes           | 76.3 ms                                                                | 74.6 ms: 1.02x faster                                                         |
| django_template        | 35.8 ms                                                                | 35.1 ms: 1.02x faster                                                         |
| scimark_lu             | 117 ms                                                                 | 115 ms: 1.02x faster                                                          |
| float                  | 78.7 ms                                                                | 77.6 ms: 1.01x faster                                                         |
| deltablue              | 3.26 ms                                                                | 3.23 ms: 1.01x faster                                                         |
| thrift                 | 818 us                                                                 | 810 us: 1.01x faster                                                          |
| sqlglot_normalize      | 112 ms                                                                 | 111 ms: 1.01x faster                                                          |
| coverage               | 98.6 ms                                                                | 97.7 ms: 1.01x faster                                                         |
| nqueens                | 81.7 ms                                                                | 81.0 ms: 1.01x faster                                                         |
| hexiom                 | 6.43 ms                                                                | 6.38 ms: 1.01x faster                                                         |
| meteor_contest         | 111 ms                                                                 | 111 ms: 1.01x faster                                                          |
| python_startup_no_site | 7.11 ms                                                                | 7.07 ms: 1.01x faster                                                         |
| xml_etree_generate     | 88.8 ms                                                                | 88.3 ms: 1.00x faster                                                         |
| python_startup         | 10.5 ms                                                                | 10.5 ms: 1.00x faster                                                         |
| regex_effbot           | 3.74 ms                                                                | 3.73 ms: 1.00x faster                                                         |
| create_gc_cycles       | 1.75 ms                                                                | 1.75 ms: 1.00x faster                                                         |
| raytrace               | 264 ms                                                                 | 265 ms: 1.00x slower                                                          |
| pprint_pformat         | 1.53 sec                                                               | 1.54 sec: 1.00x slower                                                        |
| richards               | 47.9 ms                                                                | 48.0 ms: 1.00x slower                                                         |
| dulwich_log            | 66.4 ms                                                                | 66.7 ms: 1.00x slower                                                         |
| docutils               | 2.83 sec                                                               | 2.84 sec: 1.00x slower                                                        |
| richards_super         | 53.7 ms                                                                | 54.0 ms: 1.00x slower                                                         |
| sqlglot_transpile      | 1.60 ms                                                                | 1.60 ms: 1.00x slower                                                         |
| 2to3                   | 270 ms                                                                 | 272 ms: 1.01x slower                                                          |
| regex_compile          | 136 ms                                                                 | 136 ms: 1.01x slower                                                          |
| telco                  | 8.55 ms                                                                | 8.60 ms: 1.01x slower                                                         |
| sympy_str              | 282 ms                                                                 | 283 ms: 1.01x slower                                                          |
| sympy_sum              | 157 ms                                                                 | 157 ms: 1.01x slower                                                          |
| scimark_monte_carlo    | 68.4 ms                                                                | 68.9 ms: 1.01x slower                                                         |
| tornado_http           | 93.9 ms                                                                | 94.6 ms: 1.01x slower                                                         |
| sympy_integrate        | 20.3 ms                                                                | 20.5 ms: 1.01x slower                                                         |
| comprehensions         | 16.9 us                                                                | 17.0 us: 1.01x slower                                                         |
| asyncio_websockets     | 563 ms                                                                 | 569 ms: 1.01x slower                                                          |
| json_dumps             | 10.5 ms                                                                | 10.6 ms: 1.01x slower                                                         |
| logging_format         | 6.40 us                                                                | 6.47 us: 1.01x slower                                                         |
| genshi_text            | 23.4 ms                                                                | 23.7 ms: 1.01x slower                                                         |
| logging_silent         | 104 ns                                                                 | 105 ns: 1.01x slower                                                          |
| deepcopy_memo          | 37.7 us                                                                | 38.3 us: 1.01x slower                                                         |
| scimark_sor            | 123 ms                                                                 | 125 ms: 1.01x slower                                                          |
| pickle_list            | 5.33 us                                                                | 5.41 us: 1.02x slower                                                         |
| scimark_fft            | 369 ms                                                                 | 376 ms: 1.02x slower                                                          |
| json                   | 5.15 ms                                                                | 5.24 ms: 1.02x slower                                                         |
| html5lib               | 67.3 ms                                                                | 68.6 ms: 1.02x slower                                                         |
| pickle_pure_python     | 299 us                                                                 | 305 us: 1.02x slower                                                          |
| unpickle               | 15.2 us                                                                | 15.5 us: 1.02x slower                                                         |
| unpickle_pure_python   | 217 us                                                                 | 222 us: 1.02x slower                                                          |
| pycparser              | 1.15 sec                                                               | 1.17 sec: 1.02x slower                                                        |
| pickle                 | 11.8 us                                                                | 12.1 us: 1.02x slower                                                         |
| chameleon              | 6.94 ms                                                                | 7.12 ms: 1.03x slower                                                         |
| pyflate                | 471 ms                                                                 | 483 ms: 1.03x slower                                                          |
| fannkuch               | 391 ms                                                                 | 401 ms: 1.03x slower                                                          |
| regex_dna              | 218 ms                                                                 | 224 ms: 1.03x slower                                                          |
| tomli_loads            | 2.17 sec                                                               | 2.24 sec: 1.03x slower                                                        |
| unpickle_list          | 4.99 us                                                                | 5.24 us: 1.05x slower                                                         |
| mdp                    | 2.60 sec                                                               | 2.80 sec: 1.08x slower                                                        |
| spectral_norm          | 113 ms                                                                 | 122 ms: 1.08x slower                                                          |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                                  |

Benchmark hidden because not significant (41): async_tree_io, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_io_tg, async_tree_memoization, async_tree_none, async_tree_none_tg, pathlib, bench_mp_pool, xml_etree_parse, xml_etree_iterparse, async_tree_memoization_tg, regex_v8, sqlglot_optimize, bench_thread_pool, pprint_safe_repr, json_loads, typing_runtime_protocols, dask, sqlite_synth, genshi_xml, go, mako, asyncio_tcp_ssl, coroutines, asyncio_tcp, deepcopy, deepcopy_reduce, xml_etree_process, pylint, aiohttp, async_generators, sympy_expand, gunicorn, chaos, logging_simple, mypy2, scimark_sparse_mat_mult, sqlglot_parse, djangocms, pickle_dict

# HPT report

- Reliability score: 74.83% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x