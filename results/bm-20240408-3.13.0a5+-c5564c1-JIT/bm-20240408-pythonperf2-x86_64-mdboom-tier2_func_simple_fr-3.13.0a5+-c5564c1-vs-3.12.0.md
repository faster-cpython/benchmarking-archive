# Results vs. 3.12.0

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: linux-x86_64
- commit hash: c5564c1
- commit date: 2024-04-08
- overall geometric mean: 1.02x slower
- HPT reliability: 99.70%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 298 ms: 1.05x slower                                                         |
| chameleon      | 7.23 ms                                                      | 7.70 ms: 1.06x slower                                                        |
| docutils       | 2.87 sec                                                     | 3.09 sec: 1.08x slower                                                       |
| Geometric mean | (ref)                                                        | 1.05x slower                                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 333 ms: 1.29x faster                                                         |
| async_tree_memoization_tg  | 540 ms                                                       | 422 ms: 1.28x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 441 ms: 1.23x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 855 ms: 1.23x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 847 ms: 1.23x faster                                                         |
| async_tree_none            | 452 ms                                                       | 375 ms: 1.20x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 590 ms: 1.18x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 606 ms: 1.15x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.22x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 262 ms: 1.01x faster                                                         |
| nbody          | 88.0 ms                                                      | 96.2 ms: 1.09x slower                                                        |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                 |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 144 ms                                                       | 148 ms: 1.02x slower                                                         |
| regex_v8       | 23.6 ms                                                      | 25.3 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                 |

Benchmark hidden because not significant (2): regex_dna, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 318 us                                                       | 310 us: 1.03x faster                                                         |
| xml_etree_iterparse  | 103 ms                                                       | 101 ms: 1.02x faster                                                         |
| unpickle             | 14.8 us                                                      | 14.6 us: 1.01x faster                                                        |
| xml_etree_parse      | 144 ms                                                       | 143 ms: 1.01x faster                                                         |
| tomli_loads          | 2.16 sec                                                     | 2.18 sec: 1.01x slower                                                       |
| xml_etree_process    | 58.4 ms                                                      | 59.2 ms: 1.01x slower                                                        |
| pickle               | 10.5 us                                                      | 10.7 us: 1.02x slower                                                        |
| json_dumps           | 10.2 ms                                                      | 10.5 ms: 1.03x slower                                                        |
| json_loads           | 24.4 us                                                      | 25.4 us: 1.04x slower                                                        |
| pickle_dict          | 32.5 us                                                      | 34.6 us: 1.06x slower                                                        |
| unpickle_pure_python | 210 us                                                       | 233 us: 1.11x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.02x slower                                                                 |

Benchmark hidden because not significant (3): xml_etree_generate, pickle_list, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 13.4 ms: 1.16x slower                                                        |
| python_startup_no_site | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.25x slower                                                                 |

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 333 ms: 1.29x faster                                                         |
| async_tree_memoization_tg  | 540 ms                                                       | 422 ms: 1.28x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 441 ms: 1.23x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 855 ms: 1.23x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 847 ms: 1.23x faster                                                         |
| typing_runtime_protocols   | 152 us                                                       | 123 us: 1.23x faster                                                         |
| async_tree_none            | 452 ms                                                       | 375 ms: 1.20x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 590 ms: 1.18x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 606 ms: 1.15x faster                                                         |
| comprehensions             | 21.9 us                                                      | 19.2 us: 1.14x faster                                                        |
| generators                 | 37.4 ms                                                      | 33.2 ms: 1.13x faster                                                        |
| raytrace                   | 298 ms                                                       | 271 ms: 1.10x faster                                                         |
| logging_simple             | 6.71 us                                                      | 6.30 us: 1.07x faster                                                        |
| logging_format             | 7.48 us                                                      | 7.08 us: 1.06x faster                                                        |
| coroutines                 | 23.0 ms                                                      | 22.2 ms: 1.04x faster                                                        |
| crypto_pyaes               | 80.3 ms                                                      | 77.8 ms: 1.03x faster                                                        |
| pickle_pure_python         | 318 us                                                       | 310 us: 1.03x faster                                                         |
| async_generators           | 390 ms                                                       | 382 ms: 1.02x faster                                                         |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.13 ms: 1.02x faster                                                        |
| sqlite_synth               | 2.77 us                                                      | 2.73 us: 1.02x faster                                                        |
| xml_etree_iterparse        | 103 ms                                                       | 101 ms: 1.02x faster                                                         |
| unpickle                   | 14.8 us                                                      | 14.6 us: 1.01x faster                                                        |
| pidigits                   | 265 ms                                                       | 262 ms: 1.01x faster                                                         |
| asyncio_tcp                | 378 ms                                                       | 373 ms: 1.01x faster                                                         |
| xml_etree_parse            | 144 ms                                                       | 143 ms: 1.01x faster                                                         |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.00x faster                                                       |
| tomli_loads                | 2.16 sec                                                     | 2.18 sec: 1.01x slower                                                       |
| asyncio_websockets         | 387 ms                                                       | 392 ms: 1.01x slower                                                         |
| xml_etree_process          | 58.4 ms                                                      | 59.2 ms: 1.01x slower                                                        |
| sympy_sum                  | 162 ms                                                       | 164 ms: 1.01x slower                                                         |
| richards_super             | 51.3 ms                                                      | 52.1 ms: 1.01x slower                                                        |
| mdp                        | 2.57 sec                                                     | 2.61 sec: 1.01x slower                                                       |
| pickle                     | 10.5 us                                                      | 10.7 us: 1.02x slower                                                        |
| spectral_norm              | 91.6 ms                                                      | 93.3 ms: 1.02x slower                                                        |
| sympy_str                  | 302 ms                                                       | 308 ms: 1.02x slower                                                         |
| sqlglot_transpile          | 1.78 ms                                                      | 1.81 ms: 1.02x slower                                                        |
| regex_compile              | 144 ms                                                       | 148 ms: 1.02x slower                                                         |
| meteor_contest             | 128 ms                                                       | 132 ms: 1.03x slower                                                         |
| pycparser                  | 1.23 sec                                                     | 1.27 sec: 1.03x slower                                                       |
| sqlglot_parse              | 1.38 ms                                                      | 1.41 ms: 1.03x slower                                                        |
| dask                       | 392 ms                                                       | 403 ms: 1.03x slower                                                         |
| scimark_monte_carlo        | 69.0 ms                                                      | 70.8 ms: 1.03x slower                                                        |
| pprint_pformat             | 1.65 sec                                                     | 1.70 sec: 1.03x slower                                                       |
| pprint_safe_repr           | 807 ms                                                       | 831 ms: 1.03x slower                                                         |
| json_dumps                 | 10.2 ms                                                      | 10.5 ms: 1.03x slower                                                        |
| pathlib                    | 18.9 ms                                                      | 19.5 ms: 1.03x slower                                                        |
| dulwich_log                | 65.4 ms                                                      | 67.7 ms: 1.04x slower                                                        |
| deepcopy_reduce            | 3.37 us                                                      | 3.50 us: 1.04x slower                                                        |
| logging_silent             | 94.4 ns                                                      | 98.1 ns: 1.04x slower                                                        |
| json_loads                 | 24.4 us                                                      | 25.4 us: 1.04x slower                                                        |
| 2to3                       | 285 ms                                                       | 298 ms: 1.05x slower                                                         |
| sqlglot_normalize          | 116 ms                                                       | 121 ms: 1.05x slower                                                         |
| sympy_integrate            | 23.9 ms                                                      | 25.3 ms: 1.06x slower                                                        |
| deepcopy_memo              | 36.8 us                                                      | 38.9 us: 1.06x slower                                                        |
| scimark_fft                | 301 ms                                                       | 320 ms: 1.06x slower                                                         |
| pickle_dict                | 32.5 us                                                      | 34.6 us: 1.06x slower                                                        |
| sympy_expand               | 484 ms                                                       | 515 ms: 1.06x slower                                                         |
| chameleon                  | 7.23 ms                                                      | 7.70 ms: 1.06x slower                                                        |
| json                       | 5.12 ms                                                      | 5.45 ms: 1.07x slower                                                        |
| regex_v8                   | 23.6 ms                                                      | 25.3 ms: 1.07x slower                                                        |
| docutils                   | 2.87 sec                                                     | 3.09 sec: 1.08x slower                                                       |
| deepcopy                   | 368 us                                                       | 398 us: 1.08x slower                                                         |
| gunicorn                   | 1.00 ms                                                      | 1.09 ms: 1.09x slower                                                        |
| sqlglot_optimize           | 57.5 ms                                                      | 62.7 ms: 1.09x slower                                                        |
| nbody                      | 88.0 ms                                                      | 96.2 ms: 1.09x slower                                                        |
| pyflate                    | 439 ms                                                       | 481 ms: 1.10x slower                                                         |
| nqueens                    | 89.9 ms                                                      | 99.7 ms: 1.11x slower                                                        |
| unpickle_pure_python       | 210 us                                                       | 233 us: 1.11x slower                                                         |
| aiohttp                    | 1.02 ms                                                      | 1.13 ms: 1.11x slower                                                        |
| fannkuch                   | 350 ms                                                       | 398 ms: 1.14x slower                                                         |
| python_startup             | 11.6 ms                                                      | 13.4 ms: 1.16x slower                                                        |
| telco                      | 6.96 ms                                                      | 8.05 ms: 1.16x slower                                                        |
| deltablue                  | 3.24 ms                                                      | 3.76 ms: 1.16x slower                                                        |
| create_gc_cycles           | 1.59 ms                                                      | 1.87 ms: 1.18x slower                                                        |
| hexiom                     | 5.96 ms                                                      | 7.17 ms: 1.20x slower                                                        |
| go                         | 150 ms                                                       | 180 ms: 1.20x slower                                                         |
| coverage                   | 66.7 ms                                                      | 83.9 ms: 1.26x slower                                                        |
| gc_traversal               | 3.48 ms                                                      | 4.38 ms: 1.26x slower                                                        |
| scimark_lu                 | 98.8 ms                                                      | 128 ms: 1.30x slower                                                         |
| python_startup_no_site     | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                        |
| scimark_sor                | 109 ms                                                       | 156 ms: 1.43x slower                                                         |
| Geometric mean             | (ref)                                                        | 1.02x slower                                                                 |

Benchmark hidden because not significant (13): bench_thread_pool, mypy2, bench_mp_pool, float, xml_etree_generate, regex_dna, richards, regex_effbot, pickle_list, unpickle_list, mako, chaos, tornado_http
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240408-3.13.0a5+-c5564c1-JIT/bm-20240408-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.70% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x