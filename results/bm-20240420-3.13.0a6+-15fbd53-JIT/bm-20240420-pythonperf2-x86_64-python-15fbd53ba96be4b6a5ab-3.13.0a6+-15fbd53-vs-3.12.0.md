# Results vs. 3.12.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.01x slower
- HPT reliability: 97.77%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 298 ms: 1.04x slower                                                         |
| chameleon      | 7.23 ms                                                      | 7.57 ms: 1.05x slower                                                        |
| docutils       | 2.87 sec                                                     | 3.05 sec: 1.06x slower                                                       |
| Geometric mean | (ref)                                                        | 1.04x slower                                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 540 ms                                                       | 426 ms: 1.27x faster                                                         |
| async_tree_none_tg         | 431 ms                                                       | 341 ms: 1.26x faster                                                         |
| async_tree_none            | 452 ms                                                       | 372 ms: 1.21x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 881 ms: 1.20x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 595 ms: 1.17x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 467 ms: 1.16x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 903 ms: 1.15x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 617 ms: 1.13x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.19x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 261 ms: 1.02x faster                                                         |
| float          | 76.6 ms                                                      | 75.6 ms: 1.01x faster                                                        |
| nbody          | 88.0 ms                                                      | 98.2 ms: 1.12x slower                                                        |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.47 ms: 1.03x faster                                                        |
| regex_compile  | 144 ms                                                       | 145 ms: 1.01x slower                                                         |
| regex_dna      | 239 ms                                                       | 241 ms: 1.01x slower                                                         |
| regex_v8       | 23.6 ms                                                      | 26.2 ms: 1.11x slower                                                        |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| xml_etree_generate   | 86.1 ms                                                      | 83.7 ms: 1.03x faster                                                        |
| pickle_pure_python   | 318 us                                                       | 311 us: 1.02x faster                                                         |
| xml_etree_iterparse  | 103 ms                                                       | 101 ms: 1.02x faster                                                         |
| xml_etree_process    | 58.4 ms                                                      | 57.6 ms: 1.01x faster                                                        |
| unpickle_list        | 4.66 us                                                      | 4.60 us: 1.01x faster                                                        |
| tomli_loads          | 2.16 sec                                                     | 2.14 sec: 1.01x faster                                                       |
| pickle_dict          | 32.5 us                                                      | 32.5 us: 1.00x faster                                                        |
| json_loads           | 24.4 us                                                      | 24.8 us: 1.02x slower                                                        |
| pickle               | 10.5 us                                                      | 10.8 us: 1.03x slower                                                        |
| unpickle             | 14.8 us                                                      | 15.3 us: 1.03x slower                                                        |
| unpickle_pure_python | 210 us                                                       | 219 us: 1.05x slower                                                         |
| json_dumps           | 10.2 ms                                                      | 10.8 ms: 1.05x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                                 |

Benchmark hidden because not significant (2): pickle_list, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 8.64 ms                                                      | 9.45 ms: 1.09x slower                                                        |
| python_startup         | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.13x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.0 ms                                                      | 9.93 ms: 1.01x faster                                                        |
| django_template | 38.2 ms                                                      | 39.4 ms: 1.03x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 540 ms                                                       | 426 ms: 1.27x faster                                                         |
| async_tree_none_tg         | 431 ms                                                       | 341 ms: 1.26x faster                                                         |
| typing_runtime_protocols   | 152 us                                                       | 121 us: 1.25x faster                                                         |
| async_tree_none            | 452 ms                                                       | 372 ms: 1.21x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 881 ms: 1.20x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 595 ms: 1.17x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 467 ms: 1.16x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 903 ms: 1.15x faster                                                         |
| comprehensions             | 21.9 us                                                      | 19.2 us: 1.14x faster                                                        |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 617 ms: 1.13x faster                                                         |
| generators                 | 37.4 ms                                                      | 33.5 ms: 1.12x faster                                                        |
| raytrace                   | 298 ms                                                       | 271 ms: 1.10x faster                                                         |
| logging_format             | 7.48 us                                                      | 6.89 us: 1.09x faster                                                        |
| pathlib                    | 18.9 ms                                                      | 17.5 ms: 1.08x faster                                                        |
| logging_simple             | 6.71 us                                                      | 6.25 us: 1.07x faster                                                        |
| crypto_pyaes               | 80.3 ms                                                      | 77.3 ms: 1.04x faster                                                        |
| coroutines                 | 23.0 ms                                                      | 22.1 ms: 1.04x faster                                                        |
| sqlite_synth               | 2.77 us                                                      | 2.68 us: 1.03x faster                                                        |
| regex_effbot               | 3.57 ms                                                      | 3.47 ms: 1.03x faster                                                        |
| xml_etree_generate         | 86.1 ms                                                      | 83.7 ms: 1.03x faster                                                        |
| bench_thread_pool          | 950 us                                                       | 926 us: 1.03x faster                                                         |
| pickle_pure_python         | 318 us                                                       | 311 us: 1.02x faster                                                         |
| xml_etree_iterparse        | 103 ms                                                       | 101 ms: 1.02x faster                                                         |
| pidigits                   | 265 ms                                                       | 261 ms: 1.02x faster                                                         |
| xml_etree_process          | 58.4 ms                                                      | 57.6 ms: 1.01x faster                                                        |
| float                      | 76.6 ms                                                      | 75.6 ms: 1.01x faster                                                        |
| unpickle_list              | 4.66 us                                                      | 4.60 us: 1.01x faster                                                        |
| asyncio_tcp                | 378 ms                                                       | 374 ms: 1.01x faster                                                         |
| tomli_loads                | 2.16 sec                                                     | 2.14 sec: 1.01x faster                                                       |
| mako                       | 10.0 ms                                                      | 9.93 ms: 1.01x faster                                                        |
| async_generators           | 390 ms                                                       | 388 ms: 1.01x faster                                                         |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.00x faster                                                       |
| pickle_dict                | 32.5 us                                                      | 32.5 us: 1.00x faster                                                        |
| logging_silent             | 94.4 ns                                                      | 94.7 ns: 1.00x slower                                                        |
| mdp                        | 2.57 sec                                                     | 2.59 sec: 1.01x slower                                                       |
| regex_compile              | 144 ms                                                       | 145 ms: 1.01x slower                                                         |
| regex_dna                  | 239 ms                                                       | 241 ms: 1.01x slower                                                         |
| deepcopy_reduce            | 3.37 us                                                      | 3.40 us: 1.01x slower                                                        |
| richards                   | 45.7 ms                                                      | 46.2 ms: 1.01x slower                                                        |
| spectral_norm              | 91.6 ms                                                      | 92.7 ms: 1.01x slower                                                        |
| sympy_str                  | 302 ms                                                       | 306 ms: 1.01x slower                                                         |
| deepcopy_memo              | 36.8 us                                                      | 37.3 us: 1.01x slower                                                        |
| json_loads                 | 24.4 us                                                      | 24.8 us: 1.02x slower                                                        |
| dask                       | 392 ms                                                       | 399 ms: 1.02x slower                                                         |
| richards_super             | 51.3 ms                                                      | 52.2 ms: 1.02x slower                                                        |
| dulwich_log                | 65.4 ms                                                      | 66.6 ms: 1.02x slower                                                        |
| chaos                      | 64.0 ms                                                      | 65.6 ms: 1.02x slower                                                        |
| meteor_contest             | 128 ms                                                       | 131 ms: 1.02x slower                                                         |
| pickle                     | 10.5 us                                                      | 10.8 us: 1.03x slower                                                        |
| pprint_safe_repr           | 807 ms                                                       | 831 ms: 1.03x slower                                                         |
| unpickle                   | 14.8 us                                                      | 15.3 us: 1.03x slower                                                        |
| django_template            | 38.2 ms                                                      | 39.4 ms: 1.03x slower                                                        |
| pprint_pformat             | 1.65 sec                                                     | 1.71 sec: 1.03x slower                                                       |
| sqlglot_transpile          | 1.78 ms                                                      | 1.84 ms: 1.03x slower                                                        |
| deepcopy                   | 368 us                                                       | 382 us: 1.04x slower                                                         |
| 2to3                       | 285 ms                                                       | 298 ms: 1.04x slower                                                         |
| sqlglot_parse              | 1.38 ms                                                      | 1.44 ms: 1.04x slower                                                        |
| json                       | 5.12 ms                                                      | 5.35 ms: 1.04x slower                                                        |
| sympy_integrate            | 23.9 ms                                                      | 25.0 ms: 1.05x slower                                                        |
| unpickle_pure_python       | 210 us                                                       | 219 us: 1.05x slower                                                         |
| chameleon                  | 7.23 ms                                                      | 7.57 ms: 1.05x slower                                                        |
| scimark_fft                | 301 ms                                                       | 316 ms: 1.05x slower                                                         |
| scimark_monte_carlo        | 69.0 ms                                                      | 72.6 ms: 1.05x slower                                                        |
| json_dumps                 | 10.2 ms                                                      | 10.8 ms: 1.05x slower                                                        |
| sympy_expand               | 484 ms                                                       | 510 ms: 1.05x slower                                                         |
| docutils                   | 2.87 sec                                                     | 3.05 sec: 1.06x slower                                                       |
| sqlglot_normalize          | 116 ms                                                       | 123 ms: 1.06x slower                                                         |
| fannkuch                   | 350 ms                                                       | 374 ms: 1.07x slower                                                         |
| sqlglot_optimize           | 57.5 ms                                                      | 62.6 ms: 1.09x slower                                                        |
| gunicorn                   | 1.00 ms                                                      | 1.10 ms: 1.09x slower                                                        |
| python_startup_no_site     | 8.64 ms                                                      | 9.45 ms: 1.09x slower                                                        |
| pyflate                    | 439 ms                                                       | 483 ms: 1.10x slower                                                         |
| aiohttp                    | 1.02 ms                                                      | 1.13 ms: 1.10x slower                                                        |
| regex_v8                   | 23.6 ms                                                      | 26.2 ms: 1.11x slower                                                        |
| nqueens                    | 89.9 ms                                                      | 100 ms: 1.12x slower                                                         |
| nbody                      | 88.0 ms                                                      | 98.2 ms: 1.12x slower                                                        |
| telco                      | 6.96 ms                                                      | 8.06 ms: 1.16x slower                                                        |
| python_startup             | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                        |
| deltablue                  | 3.24 ms                                                      | 3.83 ms: 1.18x slower                                                        |
| create_gc_cycles           | 1.59 ms                                                      | 1.88 ms: 1.18x slower                                                        |
| go                         | 150 ms                                                       | 178 ms: 1.19x slower                                                         |
| coverage                   | 66.7 ms                                                      | 79.5 ms: 1.19x slower                                                        |
| hexiom                     | 5.96 ms                                                      | 7.15 ms: 1.20x slower                                                        |
| gc_traversal               | 3.48 ms                                                      | 4.40 ms: 1.26x slower                                                        |
| scimark_lu                 | 98.8 ms                                                      | 125 ms: 1.27x slower                                                         |
| scimark_sor                | 109 ms                                                       | 152 ms: 1.40x slower                                                         |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                                 |

Benchmark hidden because not significant (9): bench_mp_pool, mypy2, pycparser, pickle_list, scimark_sparse_mat_mult, xml_etree_parse, sympy_sum, asyncio_websockets, tornado_http
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240420-3.13.0a6+-15fbd53-JIT/bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 97.77% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x