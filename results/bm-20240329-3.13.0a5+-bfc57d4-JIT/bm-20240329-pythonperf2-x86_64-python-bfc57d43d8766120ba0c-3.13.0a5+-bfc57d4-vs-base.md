# Results vs. base

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: linux-x86_64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.00x slower
- HPT reliability: 92.90%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 302 ms                                                                       | 300 ms: 1.01x faster                                                         |
| chameleon      | 7.39 ms                                                                      | 7.58 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                        | 1.01x slower                                                                 |

Benchmark hidden because not significant (3): docutils, html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 380 ms                                                                       | 358 ms: 1.06x faster                                                         |
| async_tree_memoization     | 455 ms                                                                       | 440 ms: 1.04x faster                                                         |
| async_tree_io              | 907 ms                                                                       | 882 ms: 1.03x faster                                                         |
| async_tree_cpu_io_mixed_tg | 592 ms                                                                       | 577 ms: 1.03x faster                                                         |
| async_tree_cpu_io_mixed    | 600 ms                                                                       | 592 ms: 1.01x faster                                                         |
| async_tree_io_tg           | 885 ms                                                                       | 904 ms: 1.02x slower                                                         |
| Geometric mean             | (ref)                                                                        | 1.02x faster                                                                 |

Benchmark hidden because not significant (2): async_tree_none_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 98.2 ms                                                                      | 94.9 ms: 1.03x faster                                                        |
| float          | 77.1 ms                                                                      | 78.5 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                                        | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 250 ms                                                                       | 242 ms: 1.03x faster                                                         |
| regex_v8       | 26.0 ms                                                                      | 25.6 ms: 1.01x faster                                                        |
| regex_effbot   | 3.49 ms                                                                      | 3.70 ms: 1.06x slower                                                        |
| Geometric mean | (ref)                                                                        | 1.00x slower                                                                 |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| xml_etree_parse      | 148 ms                                                                       | 143 ms: 1.03x faster                                                         |
| xml_etree_iterparse  | 105 ms                                                                       | 102 ms: 1.02x faster                                                         |
| json_dumps           | 10.6 ms                                                                      | 10.5 ms: 1.01x faster                                                        |
| xml_etree_generate   | 84.8 ms                                                                      | 84.1 ms: 1.01x faster                                                        |
| json_loads           | 25.5 us                                                                      | 25.3 us: 1.01x faster                                                        |
| unpickle_list        | 4.64 us                                                                      | 4.62 us: 1.01x faster                                                        |
| pickle_pure_python   | 310 us                                                                       | 311 us: 1.00x slower                                                         |
| pickle_list          | 4.40 us                                                                      | 4.42 us: 1.01x slower                                                        |
| pickle               | 10.8 us                                                                      | 10.9 us: 1.01x slower                                                        |
| pickle_dict          | 32.8 us                                                                      | 33.1 us: 1.01x slower                                                        |
| tomli_loads          | 2.14 sec                                                                     | 2.17 sec: 1.02x slower                                                       |
| unpickle_pure_python | 231 us                                                                       | 235 us: 1.02x slower                                                         |
| Geometric mean       | (ref)                                                                        | 1.00x faster                                                                 |

Benchmark hidden because not significant (2): xml_etree_process, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 11.8 ms                                                                      | 11.8 ms: 1.00x slower                                                        |
| python_startup         | 13.5 ms                                                                      | 13.6 ms: 1.01x slower                                                        |
| Geometric mean         | (ref)                                                                        | 1.00x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 40.4 ms                                                                      | 40.1 ms: 1.01x faster                                                        |
| genshi_xml      | 59.0 ms                                                                      | 59.4 ms: 1.01x slower                                                        |
| mako            | 9.93 ms                                                                      | 10.0 ms: 1.01x slower                                                        |
| genshi_text     | 26.9 ms                                                                      | 27.4 ms: 1.02x slower                                                        |
| Geometric mean  | (ref)                                                                        | 1.01x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240329-pythonperf2-x86_64-python-05e0b67a43c5c1778dc2-3.13.0a5+-05e0b67 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:----------------------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 380 ms                                                                       | 358 ms: 1.06x faster                                                         |
| async_tree_memoization     | 455 ms                                                                       | 440 ms: 1.04x faster                                                         |
| nbody                      | 98.2 ms                                                                      | 94.9 ms: 1.03x faster                                                        |
| xml_etree_parse            | 148 ms                                                                       | 143 ms: 1.03x faster                                                         |
| regex_dna                  | 250 ms                                                                       | 242 ms: 1.03x faster                                                         |
| bench_mp_pool              | 5.12 ms                                                                      | 4.97 ms: 1.03x faster                                                        |
| async_tree_io              | 907 ms                                                                       | 882 ms: 1.03x faster                                                         |
| async_tree_cpu_io_mixed_tg | 592 ms                                                                       | 577 ms: 1.03x faster                                                         |
| nqueens                    | 105 ms                                                                       | 103 ms: 1.03x faster                                                         |
| coverage                   | 84.3 ms                                                                      | 82.4 ms: 1.02x faster                                                        |
| xml_etree_iterparse        | 105 ms                                                                       | 102 ms: 1.02x faster                                                         |
| pathlib                    | 20.2 ms                                                                      | 19.8 ms: 1.02x faster                                                        |
| pprint_pformat             | 1.74 sec                                                                     | 1.71 sec: 1.02x faster                                                       |
| scimark_monte_carlo        | 74.2 ms                                                                      | 72.9 ms: 1.02x faster                                                        |
| raytrace                   | 308 ms                                                                       | 304 ms: 1.01x faster                                                         |
| regex_v8                   | 26.0 ms                                                                      | 25.6 ms: 1.01x faster                                                        |
| async_tree_cpu_io_mixed    | 600 ms                                                                       | 592 ms: 1.01x faster                                                         |
| scimark_sparse_mat_mult    | 4.16 ms                                                                      | 4.11 ms: 1.01x faster                                                        |
| mdp                        | 2.65 sec                                                                     | 2.62 sec: 1.01x faster                                                       |
| telco                      | 8.08 ms                                                                      | 8.00 ms: 1.01x faster                                                        |
| json_dumps                 | 10.6 ms                                                                      | 10.5 ms: 1.01x faster                                                        |
| logging_format             | 7.31 us                                                                      | 7.24 us: 1.01x faster                                                        |
| go                         | 177 ms                                                                       | 175 ms: 1.01x faster                                                         |
| xml_etree_generate         | 84.8 ms                                                                      | 84.1 ms: 1.01x faster                                                        |
| logging_simple             | 6.66 us                                                                      | 6.61 us: 1.01x faster                                                        |
| django_template            | 40.4 ms                                                                      | 40.1 ms: 1.01x faster                                                        |
| create_gc_cycles           | 1.81 ms                                                                      | 1.80 ms: 1.01x faster                                                        |
| crypto_pyaes               | 77.6 ms                                                                      | 77.1 ms: 1.01x faster                                                        |
| 2to3                       | 302 ms                                                                       | 300 ms: 1.01x faster                                                         |
| json_loads                 | 25.5 us                                                                      | 25.3 us: 1.01x faster                                                        |
| unpickle_list              | 4.64 us                                                                      | 4.62 us: 1.01x faster                                                        |
| dulwich_log                | 69.5 ms                                                                      | 69.2 ms: 1.00x faster                                                        |
| scimark_sor                | 154 ms                                                                       | 154 ms: 1.00x faster                                                         |
| spectral_norm              | 93.5 ms                                                                      | 93.2 ms: 1.00x faster                                                        |
| pylint                     | 338 ms                                                                       | 339 ms: 1.00x slower                                                         |
| hexiom                     | 7.57 ms                                                                      | 7.59 ms: 1.00x slower                                                        |
| python_startup_no_site     | 11.8 ms                                                                      | 11.8 ms: 1.00x slower                                                        |
| sympy_integrate            | 25.2 ms                                                                      | 25.3 ms: 1.00x slower                                                        |
| sqlglot_transpile          | 1.83 ms                                                                      | 1.83 ms: 1.00x slower                                                        |
| sympy_str                  | 303 ms                                                                       | 304 ms: 1.00x slower                                                         |
| pickle_pure_python         | 310 us                                                                       | 311 us: 1.00x slower                                                         |
| pickle_list                | 4.40 us                                                                      | 4.42 us: 1.01x slower                                                        |
| python_startup             | 13.5 ms                                                                      | 13.6 ms: 1.01x slower                                                        |
| richards_super             | 58.1 ms                                                                      | 58.4 ms: 1.01x slower                                                        |
| generators                 | 33.4 ms                                                                      | 33.6 ms: 1.01x slower                                                        |
| genshi_xml                 | 59.0 ms                                                                      | 59.4 ms: 1.01x slower                                                        |
| mako                       | 9.93 ms                                                                      | 10.0 ms: 1.01x slower                                                        |
| unpack_sequence            | 58.4 ns                                                                      | 58.9 ns: 1.01x slower                                                        |
| pickle                     | 10.8 us                                                                      | 10.9 us: 1.01x slower                                                        |
| aiohttp                    | 1.11 ms                                                                      | 1.12 ms: 1.01x slower                                                        |
| pickle_dict                | 32.8 us                                                                      | 33.1 us: 1.01x slower                                                        |
| deepcopy                   | 394 us                                                                       | 398 us: 1.01x slower                                                         |
| sqlglot_normalize          | 123 ms                                                                       | 125 ms: 1.01x slower                                                         |
| async_generators           | 389 ms                                                                       | 395 ms: 1.01x slower                                                         |
| tomli_loads                | 2.14 sec                                                                     | 2.17 sec: 1.02x slower                                                       |
| unpickle_pure_python       | 231 us                                                                       | 235 us: 1.02x slower                                                         |
| float                      | 77.1 ms                                                                      | 78.5 ms: 1.02x slower                                                        |
| comprehensions             | 19.7 us                                                                      | 20.1 us: 1.02x slower                                                        |
| meteor_contest             | 132 ms                                                                       | 134 ms: 1.02x slower                                                         |
| genshi_text                | 26.9 ms                                                                      | 27.4 ms: 1.02x slower                                                        |
| async_tree_io_tg           | 885 ms                                                                       | 904 ms: 1.02x slower                                                         |
| chaos                      | 66.3 ms                                                                      | 67.9 ms: 1.02x slower                                                        |
| chameleon                  | 7.39 ms                                                                      | 7.58 ms: 1.02x slower                                                        |
| gc_traversal               | 4.42 ms                                                                      | 4.57 ms: 1.04x slower                                                        |
| deepcopy_reduce            | 3.35 us                                                                      | 3.48 us: 1.04x slower                                                        |
| deepcopy_memo              | 38.3 us                                                                      | 39.9 us: 1.04x slower                                                        |
| scimark_lu                 | 121 ms                                                                       | 127 ms: 1.05x slower                                                         |
| regex_effbot               | 3.49 ms                                                                      | 3.70 ms: 1.06x slower                                                        |
| typing_runtime_protocols   | 120 us                                                                       | 128 us: 1.07x slower                                                         |
| Geometric mean             | (ref)                                                                        | 1.00x slower                                                                 |

Benchmark hidden because not significant (32): async_tree_none_tg, pycparser, asyncio_websockets, dask, deltablue, logging_silent, sympy_expand, richards, asyncio_tcp_ssl, scimark_fft, xml_etree_process, pidigits, pyflate, unpickle, gunicorn, regex_compile, sqlglot_optimize, sqlglot_parse, html5lib, asyncio_tcp, docutils, fannkuch, pprint_safe_repr, sympy_sum, sqlite_synth, json, thrift, mypy2, async_tree_memoization_tg, coroutines, tornado_http, bench_thread_pool

# HPT report

- Reliability score: 92.90% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x