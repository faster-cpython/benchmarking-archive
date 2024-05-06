# Results vs. base

- fork: mdboom
- ref: aa_test2
- machine: linux-aarch64
- commit hash: fa824fe
- commit date: 2024-05-03
- overall geometric mean: 1.00x slower
- HPT reliability: 94.62%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240503-arminc-aarch64-python-13245027526bf1b21fae-3.13.0a6+-1324502 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------:|
| chameleon      | 9.14 ms                                                                  | 9.17 ms: 1.00x slower                                        |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                 |

Benchmark hidden because not significant (4): 2to3, docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

Benchmark hidden because not significant (8): async_tree_memoization, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_none, async_tree_none_tg, async_tree_io_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240503-arminc-aarch64-python-13245027526bf1b21fae-3.13.0a6+-1324502 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------:|
| float          | 91.3 ms                                                                  | 91.0 ms: 1.00x faster                                        |
| nbody          | 111 ms                                                                   | 111 ms: 1.00x slower                                         |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240503-arminc-aarch64-python-13245027526bf1b21fae-3.13.0a6+-1324502 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 129 ms                                                                   | 128 ms: 1.01x faster                                         |
| regex_effbot   | 4.86 ms                                                                  | 4.88 ms: 1.00x slower                                        |
| regex_v8       | 31.0 ms                                                                  | 31.1 ms: 1.01x slower                                        |
| regex_dna      | 246 ms                                                                   | 249 ms: 1.01x slower                                         |
| Geometric mean | (ref)                                                                    | 1.00x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240503-arminc-aarch64-python-13245027526bf1b21fae-3.13.0a6+-1324502 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------:|
| unpickle             | 20.3 us                                                                  | 19.9 us: 1.02x faster                                        |
| unpickle_pure_python | 250 us                                                                   | 248 us: 1.01x faster                                         |
| tomli_loads          | 2.55 sec                                                                 | 2.53 sec: 1.01x faster                                       |
| pickle_dict          | 37.5 us                                                                  | 37.6 us: 1.00x slower                                        |
| json_loads           | 32.1 us                                                                  | 32.2 us: 1.00x slower                                        |
| pickle_list          | 5.33 us                                                                  | 5.36 us: 1.01x slower                                        |
| xml_etree_iterparse  | 147 ms                                                                   | 148 ms: 1.01x slower                                         |
| pickle               | 13.4 us                                                                  | 13.5 us: 1.01x slower                                        |
| json_dumps           | 13.0 ms                                                                  | 13.1 ms: 1.01x slower                                        |
| pickle_pure_python   | 356 us                                                                   | 363 us: 1.02x slower                                         |
| Geometric mean       | (ref)                                                                    | 1.00x slower                                                 |

Benchmark hidden because not significant (4): unpickle_list, xml_etree_process, xml_etree_parse, xml_etree_generate

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup, python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240503-arminc-aarch64-python-13245027526bf1b21fae-3.13.0a6+-1324502 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|-----------------|:------------------------------------------------------------------------:|:------------------------------------------------------------:|
| django_template | 41.7 ms                                                                  | 41.9 ms: 1.01x slower                                        |
| Geometric mean  | (ref)                                                                    | 1.00x slower                                                 |

Benchmark hidden because not significant (3): genshi_text, genshi_xml, mako

All benchmarks:
===============

| Benchmark               | bm-20240503-arminc-aarch64-python-13245027526bf1b21fae-3.13.0a6+-1324502 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|-------------------------|:------------------------------------------------------------------------:|:------------------------------------------------------------:|
| richards_super          | 62.3 ms                                                                  | 61.0 ms: 1.02x faster                                        |
| telco                   | 10.3 ms                                                                  | 10.1 ms: 1.02x faster                                        |
| dulwich_log             | 58.4 ms                                                                  | 57.1 ms: 1.02x faster                                        |
| unpickle                | 20.3 us                                                                  | 19.9 us: 1.02x faster                                        |
| pathlib                 | 23.1 ms                                                                  | 22.7 ms: 1.02x faster                                        |
| aiohttp                 | 1.19 ms                                                                  | 1.17 ms: 1.01x faster                                        |
| bench_mp_pool           | 7.23 ms                                                                  | 7.14 ms: 1.01x faster                                        |
| scimark_sparse_mat_mult | 6.59 ms                                                                  | 6.52 ms: 1.01x faster                                        |
| scimark_lu              | 137 ms                                                                   | 136 ms: 1.01x faster                                         |
| gc_traversal            | 5.06 ms                                                                  | 5.01 ms: 1.01x faster                                        |
| unpickle_pure_python    | 250 us                                                                   | 248 us: 1.01x faster                                         |
| tomli_loads             | 2.55 sec                                                                 | 2.53 sec: 1.01x faster                                       |
| json                    | 5.76 ms                                                                  | 5.72 ms: 1.01x faster                                        |
| thrift                  | 948 us                                                                   | 942 us: 1.01x faster                                         |
| regex_compile           | 129 ms                                                                   | 128 ms: 1.01x faster                                         |
| crypto_pyaes            | 81.1 ms                                                                  | 80.7 ms: 1.00x faster                                        |
| generators              | 37.9 ms                                                                  | 37.7 ms: 1.00x faster                                        |
| float                   | 91.3 ms                                                                  | 91.0 ms: 1.00x faster                                        |
| scimark_sor             | 159 ms                                                                   | 159 ms: 1.00x faster                                         |
| richards                | 55.6 ms                                                                  | 55.5 ms: 1.00x faster                                        |
| logging_simple          | 7.08 us                                                                  | 7.09 us: 1.00x slower                                        |
| comprehensions          | 20.4 us                                                                  | 20.5 us: 1.00x slower                                        |
| coroutines              | 28.9 ms                                                                  | 29.0 ms: 1.00x slower                                        |
| pickle_dict             | 37.5 us                                                                  | 37.6 us: 1.00x slower                                        |
| scimark_fft             | 443 ms                                                                   | 445 ms: 1.00x slower                                         |
| pyflate                 | 556 ms                                                                   | 558 ms: 1.00x slower                                         |
| hexiom                  | 7.05 ms                                                                  | 7.07 ms: 1.00x slower                                        |
| sqlglot_transpile       | 1.70 ms                                                                  | 1.71 ms: 1.00x slower                                        |
| json_loads              | 32.1 us                                                                  | 32.2 us: 1.00x slower                                        |
| chameleon               | 9.14 ms                                                                  | 9.17 ms: 1.00x slower                                        |
| regex_effbot            | 4.86 ms                                                                  | 4.88 ms: 1.00x slower                                        |
| logging_silent          | 134 ns                                                                   | 134 ns: 1.00x slower                                         |
| pprint_pformat          | 1.92 sec                                                                 | 1.93 sec: 1.00x slower                                       |
| go                      | 159 ms                                                                   | 160 ms: 1.00x slower                                         |
| nbody                   | 111 ms                                                                   | 111 ms: 1.00x slower                                         |
| meteor_contest          | 113 ms                                                                   | 113 ms: 1.00x slower                                         |
| regex_v8                | 31.0 ms                                                                  | 31.1 ms: 1.01x slower                                        |
| pickle_list             | 5.33 us                                                                  | 5.36 us: 1.01x slower                                        |
| django_template         | 41.7 ms                                                                  | 41.9 ms: 1.01x slower                                        |
| chaos                   | 67.7 ms                                                                  | 68.1 ms: 1.01x slower                                        |
| logging_format          | 7.72 us                                                                  | 7.76 us: 1.01x slower                                        |
| xml_etree_iterparse     | 147 ms                                                                   | 148 ms: 1.01x slower                                         |
| sqlglot_parse           | 1.38 ms                                                                  | 1.38 ms: 1.01x slower                                        |
| pickle                  | 13.4 us                                                                  | 13.5 us: 1.01x slower                                        |
| json_dumps              | 13.0 ms                                                                  | 13.1 ms: 1.01x slower                                        |
| sympy_sum               | 143 ms                                                                   | 145 ms: 1.01x slower                                         |
| raytrace                | 295 ms                                                                   | 297 ms: 1.01x slower                                         |
| sqlite_synth            | 3.84 us                                                                  | 3.88 us: 1.01x slower                                        |
| deepcopy_reduce         | 4.04 us                                                                  | 4.08 us: 1.01x slower                                        |
| nqueens                 | 97.3 ms                                                                  | 98.3 ms: 1.01x slower                                        |
| pycparser               | 1.21 sec                                                                 | 1.22 sec: 1.01x slower                                       |
| regex_dna               | 246 ms                                                                   | 249 ms: 1.01x slower                                         |
| scimark_monte_carlo     | 81.6 ms                                                                  | 82.5 ms: 1.01x slower                                        |
| spectral_norm           | 139 ms                                                                   | 141 ms: 1.01x slower                                         |
| deepcopy_memo           | 48.7 us                                                                  | 49.4 us: 1.01x slower                                        |
| deepcopy                | 438 us                                                                   | 445 us: 1.02x slower                                         |
| pickle_pure_python      | 356 us                                                                   | 363 us: 1.02x slower                                         |
| fannkuch                | 447 ms                                                                   | 456 ms: 1.02x slower                                         |
| Geometric mean          | (ref)                                                                    | 1.00x slower                                                 |

Benchmark hidden because not significant (42): flaskblogging, create_gc_cycles, async_tree_memoization, asyncio_tcp, async_tree_cpu_io_mixed, asyncio_tcp_ssl, mdp, unpickle_list, async_generators, typing_runtime_protocols, genshi_text, sympy_expand, sqlglot_normalize, tornado_http, coverage, pidigits, bench_thread_pool, pylint, asyncio_websockets, sqlglot_optimize, xml_etree_process, python_startup, html5lib, python_startup_no_site, sympy_integrate, 2to3, deltablue, genshi_xml, pprint_safe_repr, sympy_str, mako, async_tree_cpu_io_mixed_tg, async_tree_io, docutils, dask, xml_etree_parse, async_tree_none, gunicorn, xml_etree_generate, async_tree_none_tg, async_tree_io_tg, async_tree_memoization_tg

# HPT report

- Reliability score: 94.62% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x