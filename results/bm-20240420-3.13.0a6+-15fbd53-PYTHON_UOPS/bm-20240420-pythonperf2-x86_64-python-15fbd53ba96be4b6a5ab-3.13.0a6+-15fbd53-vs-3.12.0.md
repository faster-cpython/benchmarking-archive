# Results vs. 3.12.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.09x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 0.93x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 314 ms: 1.10x slower                                                         |
| chameleon      | 7.23 ms                                                      | 8.34 ms: 1.15x slower                                                        |
| docutils       | 2.87 sec                                                     | 3.24 sec: 1.13x slower                                                       |
| tornado_http   | 121 ms                                                       | 127 ms: 1.05x slower                                                         |
| Geometric mean | (ref)                                                        | 1.11x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 540 ms                                                       | 438 ms: 1.23x faster                                                         |
| async_tree_none_tg         | 431 ms                                                       | 352 ms: 1.23x faster                                                         |
| async_tree_none            | 452 ms                                                       | 384 ms: 1.18x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 900 ms: 1.17x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 604 ms: 1.15x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 478 ms: 1.14x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 919 ms: 1.13x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 631 ms: 1.10x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.17x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 263 ms: 1.01x faster                                                         |
| float          | 76.6 ms                                                      | 84.7 ms: 1.11x slower                                                        |
| nbody          | 88.0 ms                                                      | 110 ms: 1.25x slower                                                         |
| Geometric mean | (ref)                                                        | 1.11x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 239 ms                                                       | 242 ms: 1.01x slower                                                         |
| regex_effbot   | 3.57 ms                                                      | 3.63 ms: 1.02x slower                                                        |
| regex_v8       | 23.6 ms                                                      | 25.6 ms: 1.08x slower                                                        |
| regex_compile  | 144 ms                                                       | 194 ms: 1.35x slower                                                         |
| Geometric mean | (ref)                                                        | 1.11x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 30.6 us: 1.06x faster                                                        |
| unpickle_list        | 4.66 us                                                      | 4.58 us: 1.02x faster                                                        |
| pickle               | 10.5 us                                                      | 10.4 us: 1.01x faster                                                        |
| pickle_pure_python   | 318 us                                                       | 320 us: 1.01x slower                                                         |
| json_loads           | 24.4 us                                                      | 24.5 us: 1.01x slower                                                        |
| pickle_list          | 4.43 us                                                      | 4.52 us: 1.02x slower                                                        |
| xml_etree_generate   | 86.1 ms                                                      | 88.5 ms: 1.03x slower                                                        |
| unpickle             | 14.8 us                                                      | 15.3 us: 1.03x slower                                                        |
| xml_etree_parse      | 144 ms                                                       | 149 ms: 1.03x slower                                                         |
| json_dumps           | 10.2 ms                                                      | 10.7 ms: 1.05x slower                                                        |
| xml_etree_process    | 58.4 ms                                                      | 61.2 ms: 1.05x slower                                                        |
| xml_etree_iterparse  | 103 ms                                                       | 110 ms: 1.07x slower                                                         |
| tomli_loads          | 2.16 sec                                                     | 2.73 sec: 1.27x slower                                                       |
| unpickle_pure_python | 210 us                                                       | 283 us: 1.35x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.05x slower                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 8.64 ms                                                      | 8.90 ms: 1.03x slower                                                        |
| python_startup         | 11.6 ms                                                      | 12.9 ms: 1.11x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 38.2 ms                                                      | 41.5 ms: 1.09x slower                                                        |
| mako            | 10.0 ms                                                      | 13.0 ms: 1.30x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.19x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 540 ms                                                       | 438 ms: 1.23x faster                                                         |
| async_tree_none_tg         | 431 ms                                                       | 352 ms: 1.23x faster                                                         |
| typing_runtime_protocols   | 152 us                                                       | 126 us: 1.21x faster                                                         |
| async_tree_none            | 452 ms                                                       | 384 ms: 1.18x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 900 ms: 1.17x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 604 ms: 1.15x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 478 ms: 1.14x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 919 ms: 1.13x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 631 ms: 1.10x faster                                                         |
| generators                 | 37.4 ms                                                      | 34.0 ms: 1.10x faster                                                        |
| pickle_dict                | 32.5 us                                                      | 30.6 us: 1.06x faster                                                        |
| pathlib                    | 18.9 ms                                                      | 17.8 ms: 1.06x faster                                                        |
| coroutines                 | 23.0 ms                                                      | 22.2 ms: 1.04x faster                                                        |
| unpickle_list              | 4.66 us                                                      | 4.58 us: 1.02x faster                                                        |
| pickle                     | 10.5 us                                                      | 10.4 us: 1.01x faster                                                        |
| pidigits                   | 265 ms                                                       | 263 ms: 1.01x faster                                                         |
| pickle_pure_python         | 318 us                                                       | 320 us: 1.01x slower                                                         |
| async_generators           | 390 ms                                                       | 392 ms: 1.01x slower                                                         |
| json_loads                 | 24.4 us                                                      | 24.5 us: 1.01x slower                                                        |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.60 sec: 1.01x slower                                                       |
| asyncio_websockets         | 387 ms                                                       | 390 ms: 1.01x slower                                                         |
| logging_format             | 7.48 us                                                      | 7.55 us: 1.01x slower                                                        |
| regex_dna                  | 239 ms                                                       | 242 ms: 1.01x slower                                                         |
| regex_effbot               | 3.57 ms                                                      | 3.63 ms: 1.02x slower                                                        |
| sqlite_synth               | 2.77 us                                                      | 2.82 us: 1.02x slower                                                        |
| pickle_list                | 4.43 us                                                      | 4.52 us: 1.02x slower                                                        |
| logging_simple             | 6.71 us                                                      | 6.86 us: 1.02x slower                                                        |
| mdp                        | 2.57 sec                                                     | 2.63 sec: 1.02x slower                                                       |
| xml_etree_generate         | 86.1 ms                                                      | 88.5 ms: 1.03x slower                                                        |
| deepcopy_reduce            | 3.37 us                                                      | 3.47 us: 1.03x slower                                                        |
| python_startup_no_site     | 8.64 ms                                                      | 8.90 ms: 1.03x slower                                                        |
| unpickle                   | 14.8 us                                                      | 15.3 us: 1.03x slower                                                        |
| xml_etree_parse            | 144 ms                                                       | 149 ms: 1.03x slower                                                         |
| logging_silent             | 94.4 ns                                                      | 98.1 ns: 1.04x slower                                                        |
| dask                       | 392 ms                                                       | 410 ms: 1.05x slower                                                         |
| tornado_http               | 121 ms                                                       | 127 ms: 1.05x slower                                                         |
| json_dumps                 | 10.2 ms                                                      | 10.7 ms: 1.05x slower                                                        |
| xml_etree_process          | 58.4 ms                                                      | 61.2 ms: 1.05x slower                                                        |
| json                       | 5.12 ms                                                      | 5.39 ms: 1.05x slower                                                        |
| crypto_pyaes               | 80.3 ms                                                      | 85.5 ms: 1.06x slower                                                        |
| xml_etree_iterparse        | 103 ms                                                       | 110 ms: 1.07x slower                                                         |
| meteor_contest             | 128 ms                                                       | 137 ms: 1.07x slower                                                         |
| regex_v8                   | 23.6 ms                                                      | 25.6 ms: 1.08x slower                                                        |
| pycparser                  | 1.23 sec                                                     | 1.34 sec: 1.09x slower                                                       |
| django_template            | 38.2 ms                                                      | 41.5 ms: 1.09x slower                                                        |
| comprehensions             | 21.9 us                                                      | 23.9 us: 1.09x slower                                                        |
| deepcopy                   | 368 us                                                       | 404 us: 1.10x slower                                                         |
| sqlglot_transpile          | 1.78 ms                                                      | 1.95 ms: 1.10x slower                                                        |
| sympy_integrate            | 23.9 ms                                                      | 26.2 ms: 1.10x slower                                                        |
| sqlglot_normalize          | 116 ms                                                       | 127 ms: 1.10x slower                                                         |
| sympy_sum                  | 162 ms                                                       | 178 ms: 1.10x slower                                                         |
| 2to3                       | 285 ms                                                       | 314 ms: 1.10x slower                                                         |
| float                      | 76.6 ms                                                      | 84.7 ms: 1.11x slower                                                        |
| aiohttp                    | 1.02 ms                                                      | 1.13 ms: 1.11x slower                                                        |
| python_startup             | 11.6 ms                                                      | 12.9 ms: 1.11x slower                                                        |
| gunicorn                   | 1.00 ms                                                      | 1.12 ms: 1.12x slower                                                        |
| deepcopy_memo              | 36.8 us                                                      | 41.4 us: 1.13x slower                                                        |
| sqlglot_parse              | 1.38 ms                                                      | 1.55 ms: 1.13x slower                                                        |
| docutils                   | 2.87 sec                                                     | 3.24 sec: 1.13x slower                                                       |
| sympy_str                  | 302 ms                                                       | 343 ms: 1.14x slower                                                         |
| dulwich_log                | 65.4 ms                                                      | 74.8 ms: 1.14x slower                                                        |
| chaos                      | 64.0 ms                                                      | 73.3 ms: 1.15x slower                                                        |
| chameleon                  | 7.23 ms                                                      | 8.34 ms: 1.15x slower                                                        |
| sqlglot_optimize           | 57.5 ms                                                      | 66.5 ms: 1.16x slower                                                        |
| richards_super             | 51.3 ms                                                      | 59.6 ms: 1.16x slower                                                        |
| richards                   | 45.7 ms                                                      | 53.3 ms: 1.16x slower                                                        |
| sympy_expand               | 484 ms                                                       | 573 ms: 1.18x slower                                                         |
| pprint_pformat             | 1.65 sec                                                     | 2.01 sec: 1.21x slower                                                       |
| pprint_safe_repr           | 807 ms                                                       | 981 ms: 1.22x slower                                                         |
| create_gc_cycles           | 1.59 ms                                                      | 1.94 ms: 1.22x slower                                                        |
| coverage                   | 66.7 ms                                                      | 81.8 ms: 1.23x slower                                                        |
| nqueens                    | 89.9 ms                                                      | 111 ms: 1.24x slower                                                         |
| telco                      | 6.96 ms                                                      | 8.67 ms: 1.25x slower                                                        |
| nbody                      | 88.0 ms                                                      | 110 ms: 1.25x slower                                                         |
| tomli_loads                | 2.16 sec                                                     | 2.73 sec: 1.27x slower                                                       |
| deltablue                  | 3.24 ms                                                      | 4.12 ms: 1.27x slower                                                        |
| gc_traversal               | 3.48 ms                                                      | 4.44 ms: 1.28x slower                                                        |
| mako                       | 10.0 ms                                                      | 13.0 ms: 1.30x slower                                                        |
| scimark_monte_carlo        | 69.0 ms                                                      | 90.3 ms: 1.31x slower                                                        |
| fannkuch                   | 350 ms                                                       | 459 ms: 1.31x slower                                                         |
| scimark_fft                | 301 ms                                                       | 396 ms: 1.32x slower                                                         |
| pyflate                    | 439 ms                                                       | 587 ms: 1.34x slower                                                         |
| regex_compile              | 144 ms                                                       | 194 ms: 1.35x slower                                                         |
| unpickle_pure_python       | 210 us                                                       | 283 us: 1.35x slower                                                         |
| go                         | 150 ms                                                       | 204 ms: 1.36x slower                                                         |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 5.95 ms: 1.41x slower                                                        |
| scimark_lu                 | 98.8 ms                                                      | 140 ms: 1.42x slower                                                         |
| scimark_sor                | 109 ms                                                       | 159 ms: 1.46x slower                                                         |
| spectral_norm              | 91.6 ms                                                      | 140 ms: 1.53x slower                                                         |
| hexiom                     | 5.96 ms                                                      | 9.39 ms: 1.58x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.09x slower                                                                 |

Benchmark hidden because not significant (5): bench_mp_pool, asyncio_tcp, raytrace, bench_thread_pool, mypy2
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240420-3.13.0a6+-15fbd53-PYTHON_UOPS/bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 0.93x