# Results vs. 3.12.0

- fork: python
- ref: 027fa2eccf39ddccdf7b
- machine: linux-x86_64
- commit hash: 027fa2e
- commit date: 2024-04-02
- overall geometric mean: 1.03x slower
- HPT reliability: 99.79%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 297 ms: 1.04x slower                                                         |
| chameleon      | 7.23 ms                                                      | 7.41 ms: 1.02x slower                                                        |
| docutils       | 2.87 sec                                                     | 3.09 sec: 1.08x slower                                                       |
| Geometric mean | (ref)                                                        | 1.04x slower                                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 335 ms: 1.29x faster                                                         |
| async_tree_memoization_tg  | 540 ms                                                       | 427 ms: 1.27x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 849 ms: 1.23x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 444 ms: 1.23x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 861 ms: 1.22x faster                                                         |
| async_tree_none            | 452 ms                                                       | 380 ms: 1.19x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 592 ms: 1.18x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 608 ms: 1.15x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.22x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 262 ms: 1.01x faster                                                         |
| float          | 76.6 ms                                                      | 75.9 ms: 1.01x faster                                                        |
| nbody          | 88.0 ms                                                      | 101 ms: 1.15x slower                                                         |
| Geometric mean | (ref)                                                        | 1.04x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.45 ms: 1.03x faster                                                        |
| regex_compile  | 144 ms                                                       | 148 ms: 1.03x slower                                                         |
| regex_dna      | 239 ms                                                       | 247 ms: 1.03x slower                                                         |
| regex_v8       | 23.6 ms                                                      | 26.0 ms: 1.10x slower                                                        |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 318 us                                                       | 309 us: 1.03x faster                                                         |
| xml_etree_generate   | 86.1 ms                                                      | 84.0 ms: 1.03x faster                                                        |
| unpickle_list        | 4.66 us                                                      | 4.58 us: 1.02x faster                                                        |
| tomli_loads          | 2.16 sec                                                     | 2.15 sec: 1.01x faster                                                       |
| pickle               | 10.5 us                                                      | 10.7 us: 1.02x slower                                                        |
| unpickle             | 14.8 us                                                      | 15.1 us: 1.02x slower                                                        |
| json_dumps           | 10.2 ms                                                      | 10.6 ms: 1.04x slower                                                        |
| pickle_dict          | 32.5 us                                                      | 33.7 us: 1.04x slower                                                        |
| xml_etree_parse      | 144 ms                                                       | 149 ms: 1.04x slower                                                         |
| json_loads           | 24.4 us                                                      | 25.4 us: 1.04x slower                                                        |
| unpickle_pure_python | 210 us                                                       | 239 us: 1.14x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.02x slower                                                                 |

Benchmark hidden because not significant (3): pickle_list, xml_etree_process, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                        |
| python_startup_no_site | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.26x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|-----------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako      | 10.0 ms                                                      | 9.91 ms: 1.01x faster                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 335 ms: 1.29x faster                                                         |
| typing_runtime_protocols   | 152 us                                                       | 119 us: 1.28x faster                                                         |
| async_tree_memoization_tg  | 540 ms                                                       | 427 ms: 1.27x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 849 ms: 1.23x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 444 ms: 1.23x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 861 ms: 1.22x faster                                                         |
| async_tree_none            | 452 ms                                                       | 380 ms: 1.19x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 592 ms: 1.18x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 608 ms: 1.15x faster                                                         |
| comprehensions             | 21.9 us                                                      | 19.5 us: 1.12x faster                                                        |
| generators                 | 37.4 ms                                                      | 33.3 ms: 1.12x faster                                                        |
| raytrace                   | 298 ms                                                       | 285 ms: 1.05x faster                                                         |
| coroutines                 | 23.0 ms                                                      | 22.0 ms: 1.04x faster                                                        |
| crypto_pyaes               | 80.3 ms                                                      | 77.1 ms: 1.04x faster                                                        |
| logging_format             | 7.48 us                                                      | 7.21 us: 1.04x faster                                                        |
| sqlite_synth               | 2.77 us                                                      | 2.68 us: 1.03x faster                                                        |
| regex_effbot               | 3.57 ms                                                      | 3.45 ms: 1.03x faster                                                        |
| pickle_pure_python         | 318 us                                                       | 309 us: 1.03x faster                                                         |
| logging_simple             | 6.71 us                                                      | 6.54 us: 1.03x faster                                                        |
| xml_etree_generate         | 86.1 ms                                                      | 84.0 ms: 1.03x faster                                                        |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.13 ms: 1.02x faster                                                        |
| unpickle_list              | 4.66 us                                                      | 4.58 us: 1.02x faster                                                        |
| asyncio_tcp                | 378 ms                                                       | 373 ms: 1.01x faster                                                         |
| pidigits                   | 265 ms                                                       | 262 ms: 1.01x faster                                                         |
| float                      | 76.6 ms                                                      | 75.9 ms: 1.01x faster                                                        |
| mako                       | 10.0 ms                                                      | 9.91 ms: 1.01x faster                                                        |
| tomli_loads                | 2.16 sec                                                     | 2.15 sec: 1.01x faster                                                       |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.00x faster                                                       |
| sympy_sum                  | 162 ms                                                       | 164 ms: 1.01x slower                                                         |
| sympy_str                  | 302 ms                                                       | 306 ms: 1.01x slower                                                         |
| asyncio_websockets         | 387 ms                                                       | 392 ms: 1.01x slower                                                         |
| deepcopy_reduce            | 3.37 us                                                      | 3.42 us: 1.01x slower                                                        |
| logging_silent             | 94.4 ns                                                      | 95.9 ns: 1.02x slower                                                        |
| pickle                     | 10.5 us                                                      | 10.7 us: 1.02x slower                                                        |
| spectral_norm              | 91.6 ms                                                      | 93.2 ms: 1.02x slower                                                        |
| unpickle                   | 14.8 us                                                      | 15.1 us: 1.02x slower                                                        |
| meteor_contest             | 128 ms                                                       | 131 ms: 1.02x slower                                                         |
| sqlglot_parse              | 1.38 ms                                                      | 1.41 ms: 1.02x slower                                                        |
| sqlglot_transpile          | 1.78 ms                                                      | 1.82 ms: 1.02x slower                                                        |
| chameleon                  | 7.23 ms                                                      | 7.41 ms: 1.02x slower                                                        |
| regex_compile              | 144 ms                                                       | 148 ms: 1.03x slower                                                         |
| mdp                        | 2.57 sec                                                     | 2.64 sec: 1.03x slower                                                       |
| pathlib                    | 18.9 ms                                                      | 19.4 ms: 1.03x slower                                                        |
| dask                       | 392 ms                                                       | 404 ms: 1.03x slower                                                         |
| regex_dna                  | 239 ms                                                       | 247 ms: 1.03x slower                                                         |
| json_dumps                 | 10.2 ms                                                      | 10.6 ms: 1.04x slower                                                        |
| pycparser                  | 1.23 sec                                                     | 1.28 sec: 1.04x slower                                                       |
| pickle_dict                | 32.5 us                                                      | 33.7 us: 1.04x slower                                                        |
| scimark_monte_carlo        | 69.0 ms                                                      | 71.5 ms: 1.04x slower                                                        |
| xml_etree_parse            | 144 ms                                                       | 149 ms: 1.04x slower                                                         |
| 2to3                       | 285 ms                                                       | 297 ms: 1.04x slower                                                         |
| scimark_fft                | 301 ms                                                       | 314 ms: 1.04x slower                                                         |
| json_loads                 | 24.4 us                                                      | 25.4 us: 1.04x slower                                                        |
| pprint_pformat             | 1.65 sec                                                     | 1.74 sec: 1.05x slower                                                       |
| deepcopy_memo              | 36.8 us                                                      | 38.6 us: 1.05x slower                                                        |
| pprint_safe_repr           | 807 ms                                                       | 851 ms: 1.05x slower                                                         |
| sqlglot_normalize          | 116 ms                                                       | 122 ms: 1.06x slower                                                         |
| sympy_expand               | 484 ms                                                       | 514 ms: 1.06x slower                                                         |
| sympy_integrate            | 23.9 ms                                                      | 25.5 ms: 1.07x slower                                                        |
| dulwich_log                | 65.4 ms                                                      | 69.8 ms: 1.07x slower                                                        |
| deepcopy                   | 368 us                                                       | 394 us: 1.07x slower                                                         |
| json                       | 5.12 ms                                                      | 5.51 ms: 1.08x slower                                                        |
| docutils                   | 2.87 sec                                                     | 3.09 sec: 1.08x slower                                                       |
| bench_mp_pool              | 4.76 ms                                                      | 5.15 ms: 1.08x slower                                                        |
| sqlglot_optimize           | 57.5 ms                                                      | 62.3 ms: 1.08x slower                                                        |
| gunicorn                   | 1.00 ms                                                      | 1.09 ms: 1.09x slower                                                        |
| regex_v8                   | 23.6 ms                                                      | 26.0 ms: 1.10x slower                                                        |
| pyflate                    | 439 ms                                                       | 482 ms: 1.10x slower                                                         |
| fannkuch                   | 350 ms                                                       | 385 ms: 1.10x slower                                                         |
| deltablue                  | 3.24 ms                                                      | 3.58 ms: 1.11x slower                                                        |
| richards                   | 45.7 ms                                                      | 50.6 ms: 1.11x slower                                                        |
| richards_super             | 51.3 ms                                                      | 56.8 ms: 1.11x slower                                                        |
| aiohttp                    | 1.02 ms                                                      | 1.13 ms: 1.11x slower                                                        |
| unpickle_pure_python       | 210 us                                                       | 239 us: 1.14x slower                                                         |
| telco                      | 6.96 ms                                                      | 7.98 ms: 1.15x slower                                                        |
| nbody                      | 88.0 ms                                                      | 101 ms: 1.15x slower                                                         |
| create_gc_cycles           | 1.59 ms                                                      | 1.84 ms: 1.16x slower                                                        |
| python_startup             | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                        |
| bench_thread_pool          | 950 us                                                       | 1.11 ms: 1.16x slower                                                        |
| nqueens                    | 89.9 ms                                                      | 105 ms: 1.17x slower                                                         |
| go                         | 150 ms                                                       | 177 ms: 1.18x slower                                                         |
| scimark_lu                 | 98.8 ms                                                      | 121 ms: 1.22x slower                                                         |
| coverage                   | 66.7 ms                                                      | 81.8 ms: 1.23x slower                                                        |
| hexiom                     | 5.96 ms                                                      | 7.39 ms: 1.24x slower                                                        |
| gc_traversal               | 3.48 ms                                                      | 4.54 ms: 1.30x slower                                                        |
| python_startup_no_site     | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                        |
| scimark_sor                | 109 ms                                                       | 154 ms: 1.41x slower                                                         |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                                 |

Benchmark hidden because not significant (7): async_generators, mypy2, pickle_list, chaos, xml_etree_process, tornado_http, xml_etree_iterparse
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240402-3.13.0a5+-027fa2e-JIT/bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.79% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x