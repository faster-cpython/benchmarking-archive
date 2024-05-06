# Results vs. 3.12.0

- fork: python
- ref: 434bc593df4c0274b8af
- machine: linux-x86_64
- commit hash: 434bc59
- commit date: 2024-04-04
- overall geometric mean: 1.02x slower
- HPT reliability: 98.14%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 298 ms: 1.05x slower                                                         |
| chameleon      | 7.23 ms                                                      | 7.72 ms: 1.07x slower                                                        |
| docutils       | 2.87 sec                                                     | 3.07 sec: 1.07x slower                                                       |
| Geometric mean | (ref)                                                        | 1.05x slower                                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 332 ms: 1.30x faster                                                         |
| async_tree_memoization_tg  | 540 ms                                                       | 420 ms: 1.29x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 439 ms: 1.24x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 846 ms: 1.23x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 858 ms: 1.23x faster                                                         |
| async_tree_none            | 452 ms                                                       | 374 ms: 1.21x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 588 ms: 1.19x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 602 ms: 1.16x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.23x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 76.6 ms                                                      | 75.3 ms: 1.02x faster                                                        |
| pidigits       | 265 ms                                                       | 261 ms: 1.02x faster                                                         |
| nbody          | 88.0 ms                                                      | 96.3 ms: 1.10x slower                                                        |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 239 ms                                                       | 237 ms: 1.01x faster                                                         |
| regex_effbot   | 3.57 ms                                                      | 3.61 ms: 1.01x slower                                                        |
| regex_compile  | 144 ms                                                       | 147 ms: 1.02x slower                                                         |
| regex_v8       | 23.6 ms                                                      | 25.4 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 30.6 us: 1.06x faster                                                        |
| xml_etree_generate   | 86.1 ms                                                      | 84.7 ms: 1.02x faster                                                        |
| pickle_pure_python   | 318 us                                                       | 313 us: 1.02x faster                                                         |
| pickle               | 10.5 us                                                      | 10.4 us: 1.02x faster                                                        |
| tomli_loads          | 2.16 sec                                                     | 2.13 sec: 1.01x faster                                                       |
| unpickle_list        | 4.66 us                                                      | 4.61 us: 1.01x faster                                                        |
| xml_etree_process    | 58.4 ms                                                      | 58.9 ms: 1.01x slower                                                        |
| unpickle             | 14.8 us                                                      | 15.1 us: 1.02x slower                                                        |
| xml_etree_parse      | 144 ms                                                       | 148 ms: 1.03x slower                                                         |
| json_loads           | 24.4 us                                                      | 25.2 us: 1.03x slower                                                        |
| json_dumps           | 10.2 ms                                                      | 10.6 ms: 1.03x slower                                                        |
| unpickle_pure_python | 210 us                                                       | 225 us: 1.08x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                                 |

Benchmark hidden because not significant (2): xml_etree_iterparse, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 13.4 ms: 1.15x slower                                                        |
| python_startup_no_site | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.25x slower                                                                 |

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 332 ms: 1.30x faster                                                         |
| async_tree_memoization_tg  | 540 ms                                                       | 420 ms: 1.29x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 439 ms: 1.24x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 846 ms: 1.23x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 858 ms: 1.23x faster                                                         |
| async_tree_none            | 452 ms                                                       | 374 ms: 1.21x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 588 ms: 1.19x faster                                                         |
| typing_runtime_protocols   | 152 us                                                       | 128 us: 1.18x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 602 ms: 1.16x faster                                                         |
| comprehensions             | 21.9 us                                                      | 19.1 us: 1.15x faster                                                        |
| generators                 | 37.4 ms                                                      | 33.4 ms: 1.12x faster                                                        |
| raytrace                   | 298 ms                                                       | 272 ms: 1.10x faster                                                         |
| logging_format             | 7.48 us                                                      | 7.00 us: 1.07x faster                                                        |
| pickle_dict                | 32.5 us                                                      | 30.6 us: 1.06x faster                                                        |
| logging_simple             | 6.71 us                                                      | 6.34 us: 1.06x faster                                                        |
| crypto_pyaes               | 80.3 ms                                                      | 77.2 ms: 1.04x faster                                                        |
| coroutines                 | 23.0 ms                                                      | 22.1 ms: 1.04x faster                                                        |
| sqlite_synth               | 2.77 us                                                      | 2.69 us: 1.03x faster                                                        |
| async_generators           | 390 ms                                                       | 380 ms: 1.03x faster                                                         |
| float                      | 76.6 ms                                                      | 75.3 ms: 1.02x faster                                                        |
| xml_etree_generate         | 86.1 ms                                                      | 84.7 ms: 1.02x faster                                                        |
| pickle_pure_python         | 318 us                                                       | 313 us: 1.02x faster                                                         |
| pickle                     | 10.5 us                                                      | 10.4 us: 1.02x faster                                                        |
| pidigits                   | 265 ms                                                       | 261 ms: 1.02x faster                                                         |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.14 ms: 1.02x faster                                                        |
| asyncio_tcp                | 378 ms                                                       | 373 ms: 1.01x faster                                                         |
| tomli_loads                | 2.16 sec                                                     | 2.13 sec: 1.01x faster                                                       |
| unpickle_list              | 4.66 us                                                      | 4.61 us: 1.01x faster                                                        |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.01x faster                                                       |
| regex_dna                  | 239 ms                                                       | 237 ms: 1.01x faster                                                         |
| sympy_str                  | 302 ms                                                       | 305 ms: 1.01x slower                                                         |
| xml_etree_process          | 58.4 ms                                                      | 58.9 ms: 1.01x slower                                                        |
| chaos                      | 64.0 ms                                                      | 64.6 ms: 1.01x slower                                                        |
| asyncio_websockets         | 387 ms                                                       | 391 ms: 1.01x slower                                                         |
| regex_effbot               | 3.57 ms                                                      | 3.61 ms: 1.01x slower                                                        |
| richards_super             | 51.3 ms                                                      | 51.9 ms: 1.01x slower                                                        |
| pycparser                  | 1.23 sec                                                     | 1.25 sec: 1.02x slower                                                       |
| spectral_norm              | 91.6 ms                                                      | 93.2 ms: 1.02x slower                                                        |
| scimark_monte_carlo        | 69.0 ms                                                      | 70.2 ms: 1.02x slower                                                        |
| dask                       | 392 ms                                                       | 400 ms: 1.02x slower                                                         |
| regex_compile              | 144 ms                                                       | 147 ms: 1.02x slower                                                         |
| unpickle                   | 14.8 us                                                      | 15.1 us: 1.02x slower                                                        |
| pathlib                    | 18.9 ms                                                      | 19.3 ms: 1.02x slower                                                        |
| sqlglot_transpile          | 1.78 ms                                                      | 1.82 ms: 1.02x slower                                                        |
| xml_etree_parse            | 144 ms                                                       | 148 ms: 1.03x slower                                                         |
| sqlglot_parse              | 1.38 ms                                                      | 1.42 ms: 1.03x slower                                                        |
| logging_silent             | 94.4 ns                                                      | 97.2 ns: 1.03x slower                                                        |
| pprint_safe_repr           | 807 ms                                                       | 834 ms: 1.03x slower                                                         |
| json_loads                 | 24.4 us                                                      | 25.2 us: 1.03x slower                                                        |
| json_dumps                 | 10.2 ms                                                      | 10.6 ms: 1.03x slower                                                        |
| json                       | 5.12 ms                                                      | 5.30 ms: 1.03x slower                                                        |
| pprint_pformat             | 1.65 sec                                                     | 1.71 sec: 1.04x slower                                                       |
| dulwich_log                | 65.4 ms                                                      | 67.8 ms: 1.04x slower                                                        |
| meteor_contest             | 128 ms                                                       | 133 ms: 1.04x slower                                                         |
| deepcopy_reduce            | 3.37 us                                                      | 3.51 us: 1.04x slower                                                        |
| scimark_fft                | 301 ms                                                       | 314 ms: 1.04x slower                                                         |
| 2to3                       | 285 ms                                                       | 298 ms: 1.05x slower                                                         |
| sympy_expand               | 484 ms                                                       | 507 ms: 1.05x slower                                                         |
| sympy_integrate            | 23.9 ms                                                      | 25.2 ms: 1.05x slower                                                        |
| deepcopy_memo              | 36.8 us                                                      | 38.8 us: 1.05x slower                                                        |
| chameleon                  | 7.23 ms                                                      | 7.72 ms: 1.07x slower                                                        |
| docutils                   | 2.87 sec                                                     | 3.07 sec: 1.07x slower                                                       |
| regex_v8                   | 23.6 ms                                                      | 25.4 ms: 1.07x slower                                                        |
| unpickle_pure_python       | 210 us                                                       | 225 us: 1.08x slower                                                         |
| sqlglot_normalize          | 116 ms                                                       | 125 ms: 1.08x slower                                                         |
| deepcopy                   | 368 us                                                       | 398 us: 1.08x slower                                                         |
| gunicorn                   | 1.00 ms                                                      | 1.10 ms: 1.09x slower                                                        |
| nbody                      | 88.0 ms                                                      | 96.3 ms: 1.10x slower                                                        |
| sqlglot_optimize           | 57.5 ms                                                      | 63.1 ms: 1.10x slower                                                        |
| aiohttp                    | 1.02 ms                                                      | 1.12 ms: 1.10x slower                                                        |
| fannkuch                   | 350 ms                                                       | 388 ms: 1.11x slower                                                         |
| nqueens                    | 89.9 ms                                                      | 102 ms: 1.13x slower                                                         |
| pyflate                    | 439 ms                                                       | 501 ms: 1.14x slower                                                         |
| go                         | 150 ms                                                       | 172 ms: 1.15x slower                                                         |
| python_startup             | 11.6 ms                                                      | 13.4 ms: 1.15x slower                                                        |
| deltablue                  | 3.24 ms                                                      | 3.76 ms: 1.16x slower                                                        |
| create_gc_cycles           | 1.59 ms                                                      | 1.86 ms: 1.17x slower                                                        |
| telco                      | 6.96 ms                                                      | 8.22 ms: 1.18x slower                                                        |
| hexiom                     | 5.96 ms                                                      | 7.15 ms: 1.20x slower                                                        |
| scimark_lu                 | 98.8 ms                                                      | 119 ms: 1.21x slower                                                         |
| coverage                   | 66.7 ms                                                      | 81.6 ms: 1.22x slower                                                        |
| gc_traversal               | 3.48 ms                                                      | 4.58 ms: 1.32x slower                                                        |
| python_startup_no_site     | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                        |
| scimark_sor                | 109 ms                                                       | 151 ms: 1.39x slower                                                         |
| Geometric mean             | (ref)                                                        | 1.02x slower                                                                 |

Benchmark hidden because not significant (10): bench_mp_pool, mypy2, bench_thread_pool, xml_etree_iterparse, richards, mdp, mako, sympy_sum, pickle_list, tornado_http
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240404-3.13.0a5+-434bc59-JIT/bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 98.14% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x