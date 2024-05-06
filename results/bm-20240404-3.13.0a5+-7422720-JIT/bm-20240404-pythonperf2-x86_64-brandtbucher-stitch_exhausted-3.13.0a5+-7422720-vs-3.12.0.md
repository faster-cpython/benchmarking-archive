# Results vs. 3.12.0

- fork: brandtbucher
- ref: stitch_exhausted
- machine: linux-x86_64
- commit hash: 7422720
- commit date: 2024-04-04
- overall geometric mean: 1.02x slower
- HPT reliability: 99.38%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 302 ms: 1.06x slower                                                           |
| chameleon      | 7.23 ms                                                      | 7.46 ms: 1.03x slower                                                          |
| docutils       | 2.87 sec                                                     | 3.12 sec: 1.09x slower                                                         |
| tornado_http   | 121 ms                                                       | 123 ms: 1.01x slower                                                           |
| Geometric mean | (ref)                                                        | 1.05x slower                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 338 ms: 1.28x faster                                                           |
| async_tree_memoization_tg  | 540 ms                                                       | 426 ms: 1.27x faster                                                           |
| async_tree_memoization     | 544 ms                                                       | 446 ms: 1.22x faster                                                           |
| async_tree_io              | 1.04 sec                                                     | 854 ms: 1.22x faster                                                           |
| async_tree_io_tg           | 1.05 sec                                                     | 866 ms: 1.22x faster                                                           |
| async_tree_none            | 452 ms                                                       | 380 ms: 1.19x faster                                                           |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 596 ms: 1.17x faster                                                           |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 613 ms: 1.14x faster                                                           |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 261 ms: 1.01x faster                                                           |
| float          | 76.6 ms                                                      | 75.9 ms: 1.01x faster                                                          |
| nbody          | 88.0 ms                                                      | 97.1 ms: 1.10x slower                                                          |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.50 ms: 1.02x faster                                                          |
| regex_dna      | 239 ms                                                       | 238 ms: 1.00x faster                                                           |
| regex_v8       | 23.6 ms                                                      | 25.4 ms: 1.08x slower                                                          |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                   |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pickle_pure_python   | 318 us                                                       | 307 us: 1.04x faster                                                           |
| tomli_loads          | 2.16 sec                                                     | 2.13 sec: 1.02x faster                                                         |
| unpickle_list        | 4.66 us                                                      | 4.61 us: 1.01x faster                                                          |
| xml_etree_iterparse  | 103 ms                                                       | 102 ms: 1.01x faster                                                           |
| xml_etree_generate   | 86.1 ms                                                      | 85.8 ms: 1.00x faster                                                          |
| xml_etree_process    | 58.4 ms                                                      | 59.2 ms: 1.01x slower                                                          |
| pickle               | 10.5 us                                                      | 10.7 us: 1.02x slower                                                          |
| xml_etree_parse      | 144 ms                                                       | 147 ms: 1.02x slower                                                           |
| unpickle             | 14.8 us                                                      | 15.2 us: 1.03x slower                                                          |
| json_dumps           | 10.2 ms                                                      | 10.6 ms: 1.03x slower                                                          |
| pickle_dict          | 32.5 us                                                      | 33.7 us: 1.04x slower                                                          |
| json_loads           | 24.4 us                                                      | 25.3 us: 1.04x slower                                                          |
| unpickle_pure_python | 210 us                                                       | 227 us: 1.08x slower                                                           |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                                   |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                          |
| python_startup_no_site | 8.64 ms                                                      | 11.8 ms: 1.37x slower                                                          |
| Geometric mean         | (ref)                                                        | 1.26x slower                                                                   |

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 338 ms: 1.28x faster                                                           |
| async_tree_memoization_tg  | 540 ms                                                       | 426 ms: 1.27x faster                                                           |
| typing_runtime_protocols   | 152 us                                                       | 121 us: 1.25x faster                                                           |
| async_tree_memoization     | 544 ms                                                       | 446 ms: 1.22x faster                                                           |
| async_tree_io              | 1.04 sec                                                     | 854 ms: 1.22x faster                                                           |
| async_tree_io_tg           | 1.05 sec                                                     | 866 ms: 1.22x faster                                                           |
| async_tree_none            | 452 ms                                                       | 380 ms: 1.19x faster                                                           |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 596 ms: 1.17x faster                                                           |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 613 ms: 1.14x faster                                                           |
| generators                 | 37.4 ms                                                      | 33.0 ms: 1.13x faster                                                          |
| comprehensions             | 21.9 us                                                      | 19.7 us: 1.11x faster                                                          |
| raytrace                   | 298 ms                                                       | 275 ms: 1.08x faster                                                           |
| logging_format             | 7.48 us                                                      | 7.12 us: 1.05x faster                                                          |
| logging_simple             | 6.71 us                                                      | 6.43 us: 1.04x faster                                                          |
| pickle_pure_python         | 318 us                                                       | 307 us: 1.04x faster                                                           |
| crypto_pyaes               | 80.3 ms                                                      | 77.6 ms: 1.04x faster                                                          |
| sqlite_synth               | 2.77 us                                                      | 2.68 us: 1.03x faster                                                          |
| coroutines                 | 23.0 ms                                                      | 22.2 ms: 1.03x faster                                                          |
| async_generators           | 390 ms                                                       | 379 ms: 1.03x faster                                                           |
| regex_effbot               | 3.57 ms                                                      | 3.50 ms: 1.02x faster                                                          |
| asyncio_tcp                | 378 ms                                                       | 372 ms: 1.02x faster                                                           |
| tomli_loads                | 2.16 sec                                                     | 2.13 sec: 1.02x faster                                                         |
| pidigits                   | 265 ms                                                       | 261 ms: 1.01x faster                                                           |
| unpickle_list              | 4.66 us                                                      | 4.61 us: 1.01x faster                                                          |
| xml_etree_iterparse        | 103 ms                                                       | 102 ms: 1.01x faster                                                           |
| richards                   | 45.7 ms                                                      | 45.3 ms: 1.01x faster                                                          |
| float                      | 76.6 ms                                                      | 75.9 ms: 1.01x faster                                                          |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.01x faster                                                         |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.18 ms: 1.01x faster                                                          |
| xml_etree_generate         | 86.1 ms                                                      | 85.8 ms: 1.00x faster                                                          |
| regex_dna                  | 239 ms                                                       | 238 ms: 1.00x faster                                                           |
| deepcopy_memo              | 36.8 us                                                      | 37.0 us: 1.01x slower                                                          |
| richards_super             | 51.3 ms                                                      | 51.9 ms: 1.01x slower                                                          |
| tornado_http               | 121 ms                                                       | 123 ms: 1.01x slower                                                           |
| spectral_norm              | 91.6 ms                                                      | 92.8 ms: 1.01x slower                                                          |
| xml_etree_process          | 58.4 ms                                                      | 59.2 ms: 1.01x slower                                                          |
| pickle                     | 10.5 us                                                      | 10.7 us: 1.02x slower                                                          |
| xml_etree_parse            | 144 ms                                                       | 147 ms: 1.02x slower                                                           |
| sympy_sum                  | 162 ms                                                       | 165 ms: 1.02x slower                                                           |
| sqlglot_transpile          | 1.78 ms                                                      | 1.81 ms: 1.02x slower                                                          |
| sqlglot_parse              | 1.38 ms                                                      | 1.41 ms: 1.02x slower                                                          |
| deepcopy_reduce            | 3.37 us                                                      | 3.45 us: 1.02x slower                                                          |
| mdp                        | 2.57 sec                                                     | 2.63 sec: 1.02x slower                                                         |
| unpickle                   | 14.8 us                                                      | 15.2 us: 1.03x slower                                                          |
| sympy_str                  | 302 ms                                                       | 311 ms: 1.03x slower                                                           |
| chameleon                  | 7.23 ms                                                      | 7.46 ms: 1.03x slower                                                          |
| json_dumps                 | 10.2 ms                                                      | 10.6 ms: 1.03x slower                                                          |
| chaos                      | 64.0 ms                                                      | 66.1 ms: 1.03x slower                                                          |
| pickle_dict                | 32.5 us                                                      | 33.7 us: 1.04x slower                                                          |
| dask                       | 392 ms                                                       | 407 ms: 1.04x slower                                                           |
| json_loads                 | 24.4 us                                                      | 25.3 us: 1.04x slower                                                          |
| pprint_pformat             | 1.65 sec                                                     | 1.72 sec: 1.04x slower                                                         |
| logging_silent             | 94.4 ns                                                      | 98.2 ns: 1.04x slower                                                          |
| pprint_safe_repr           | 807 ms                                                       | 841 ms: 1.04x slower                                                           |
| dulwich_log                | 65.4 ms                                                      | 68.2 ms: 1.04x slower                                                          |
| pathlib                    | 18.9 ms                                                      | 19.7 ms: 1.04x slower                                                          |
| scimark_monte_carlo        | 69.0 ms                                                      | 72.1 ms: 1.05x slower                                                          |
| json                       | 5.12 ms                                                      | 5.41 ms: 1.06x slower                                                          |
| meteor_contest             | 128 ms                                                       | 136 ms: 1.06x slower                                                           |
| deepcopy                   | 368 us                                                       | 390 us: 1.06x slower                                                           |
| 2to3                       | 285 ms                                                       | 302 ms: 1.06x slower                                                           |
| scimark_fft                | 301 ms                                                       | 322 ms: 1.07x slower                                                           |
| sympy_integrate            | 23.9 ms                                                      | 25.7 ms: 1.07x slower                                                          |
| regex_v8                   | 23.6 ms                                                      | 25.4 ms: 1.08x slower                                                          |
| sympy_expand               | 484 ms                                                       | 522 ms: 1.08x slower                                                           |
| unpickle_pure_python       | 210 us                                                       | 227 us: 1.08x slower                                                           |
| docutils                   | 2.87 sec                                                     | 3.12 sec: 1.09x slower                                                         |
| fannkuch                   | 350 ms                                                       | 381 ms: 1.09x slower                                                           |
| sqlglot_normalize          | 116 ms                                                       | 126 ms: 1.09x slower                                                           |
| nbody                      | 88.0 ms                                                      | 97.1 ms: 1.10x slower                                                          |
| pyflate                    | 439 ms                                                       | 486 ms: 1.11x slower                                                           |
| gunicorn                   | 1.00 ms                                                      | 1.11 ms: 1.11x slower                                                          |
| sqlglot_optimize           | 57.5 ms                                                      | 64.5 ms: 1.12x slower                                                          |
| aiohttp                    | 1.02 ms                                                      | 1.14 ms: 1.12x slower                                                          |
| nqueens                    | 89.9 ms                                                      | 101 ms: 1.13x slower                                                           |
| go                         | 150 ms                                                       | 172 ms: 1.15x slower                                                           |
| python_startup             | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                          |
| scimark_lu                 | 98.8 ms                                                      | 115 ms: 1.17x slower                                                           |
| deltablue                  | 3.24 ms                                                      | 3.78 ms: 1.17x slower                                                          |
| create_gc_cycles           | 1.59 ms                                                      | 1.87 ms: 1.18x slower                                                          |
| telco                      | 6.96 ms                                                      | 8.32 ms: 1.20x slower                                                          |
| hexiom                     | 5.96 ms                                                      | 7.30 ms: 1.22x slower                                                          |
| coverage                   | 66.7 ms                                                      | 86.4 ms: 1.30x slower                                                          |
| gc_traversal               | 3.48 ms                                                      | 4.66 ms: 1.34x slower                                                          |
| python_startup_no_site     | 8.64 ms                                                      | 11.8 ms: 1.37x slower                                                          |
| scimark_sor                | 109 ms                                                       | 150 ms: 1.38x slower                                                           |
| Geometric mean             | (ref)                                                        | 1.02x slower                                                                   |

Benchmark hidden because not significant (8): bench_mp_pool, mako, pickle_list, bench_thread_pool, regex_compile, asyncio_websockets, pycparser, mypy2
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240404-3.13.0a5+-7422720-JIT/bm-20240404-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-7422720.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.38% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x