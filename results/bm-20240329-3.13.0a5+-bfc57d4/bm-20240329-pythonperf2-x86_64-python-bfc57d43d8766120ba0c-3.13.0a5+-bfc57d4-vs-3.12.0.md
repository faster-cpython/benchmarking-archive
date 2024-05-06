# Results vs. 3.12.0

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: linux-x86_64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.00x faster
- HPT reliability: 72.43%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.91x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 292 ms: 1.03x slower                                                         |
| chameleon      | 7.23 ms                                                      | 7.19 ms: 1.00x faster                                                        |
| docutils       | 2.87 sec                                                     | 2.95 sec: 1.03x slower                                                       |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 339 ms: 1.27x faster                                                         |
| async_tree_memoization_tg  | 540 ms                                                       | 427 ms: 1.27x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 854 ms: 1.23x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 451 ms: 1.21x faster                                                         |
| async_tree_none            | 452 ms                                                       | 376 ms: 1.20x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 586 ms: 1.19x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 594 ms: 1.17x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 893 ms: 1.17x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 263 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                        | 1.01x faster                                                                 |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 144 ms                                                       | 142 ms: 1.01x faster                                                         |
| regex_effbot   | 3.57 ms                                                      | 3.55 ms: 1.01x faster                                                        |
| regex_dna      | 239 ms                                                       | 249 ms: 1.04x slower                                                         |
| regex_v8       | 23.6 ms                                                      | 25.7 ms: 1.09x slower                                                        |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 318 us                                                       | 306 us: 1.04x faster                                                         |
| xml_etree_generate   | 86.1 ms                                                      | 84.2 ms: 1.02x faster                                                        |
| unpickle_list        | 4.66 us                                                      | 4.61 us: 1.01x faster                                                        |
| unpickle             | 14.8 us                                                      | 14.7 us: 1.01x faster                                                        |
| pickle_list          | 4.43 us                                                      | 4.47 us: 1.01x slower                                                        |
| unpickle_pure_python | 210 us                                                       | 213 us: 1.02x slower                                                         |
| json_dumps           | 10.2 ms                                                      | 10.5 ms: 1.03x slower                                                        |
| pickle_dict          | 32.5 us                                                      | 33.7 us: 1.03x slower                                                        |
| json_loads           | 24.4 us                                                      | 25.5 us: 1.04x slower                                                        |
| tomli_loads          | 2.16 sec                                                     | 2.30 sec: 1.07x slower                                                       |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                                 |

Benchmark hidden because not significant (4): xml_etree_iterparse, xml_etree_parse, xml_etree_process, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 12.8 ms: 1.10x slower                                                        |
| python_startup_no_site | 8.64 ms                                                      | 11.1 ms: 1.28x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.19x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 38.2 ms                                                      | 38.5 ms: 1.01x slower                                                        |
| mako            | 10.0 ms                                                      | 10.2 ms: 1.02x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 152 us                                                       | 115 us: 1.32x faster                                                         |
| comprehensions             | 21.9 us                                                      | 16.9 us: 1.30x faster                                                        |
| async_tree_none_tg         | 431 ms                                                       | 339 ms: 1.27x faster                                                         |
| async_tree_memoization_tg  | 540 ms                                                       | 427 ms: 1.27x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 854 ms: 1.23x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 451 ms: 1.21x faster                                                         |
| async_tree_none            | 452 ms                                                       | 376 ms: 1.20x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 586 ms: 1.19x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 594 ms: 1.17x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 893 ms: 1.17x faster                                                         |
| raytrace                   | 298 ms                                                       | 261 ms: 1.14x faster                                                         |
| crypto_pyaes               | 80.3 ms                                                      | 71.7 ms: 1.12x faster                                                        |
| generators                 | 37.4 ms                                                      | 33.4 ms: 1.12x faster                                                        |
| async_generators           | 390 ms                                                       | 360 ms: 1.09x faster                                                         |
| mypy2                      | 830 ms                                                       | 768 ms: 1.08x faster                                                         |
| sympy_sum                  | 162 ms                                                       | 151 ms: 1.07x faster                                                         |
| chaos                      | 64.0 ms                                                      | 60.0 ms: 1.07x faster                                                        |
| scimark_monte_carlo        | 69.0 ms                                                      | 64.9 ms: 1.06x faster                                                        |
| logging_format             | 7.48 us                                                      | 7.12 us: 1.05x faster                                                        |
| bench_thread_pool          | 950 us                                                       | 904 us: 1.05x faster                                                         |
| sympy_str                  | 302 ms                                                       | 290 ms: 1.04x faster                                                         |
| pickle_pure_python         | 318 us                                                       | 306 us: 1.04x faster                                                         |
| bench_mp_pool              | 4.76 ms                                                      | 4.59 ms: 1.04x faster                                                        |
| scimark_lu                 | 98.8 ms                                                      | 95.6 ms: 1.03x faster                                                        |
| sympy_integrate            | 23.9 ms                                                      | 23.2 ms: 1.03x faster                                                        |
| pprint_pformat             | 1.65 sec                                                     | 1.60 sec: 1.03x faster                                                       |
| pprint_safe_repr           | 807 ms                                                       | 785 ms: 1.03x faster                                                         |
| logging_simple             | 6.71 us                                                      | 6.53 us: 1.03x faster                                                        |
| coroutines                 | 23.0 ms                                                      | 22.4 ms: 1.03x faster                                                        |
| nqueens                    | 89.9 ms                                                      | 87.7 ms: 1.02x faster                                                        |
| xml_etree_generate         | 86.1 ms                                                      | 84.2 ms: 1.02x faster                                                        |
| mdp                        | 2.57 sec                                                     | 2.52 sec: 1.02x faster                                                       |
| asyncio_tcp                | 378 ms                                                       | 371 ms: 1.02x faster                                                         |
| scimark_fft                | 301 ms                                                       | 296 ms: 1.02x faster                                                         |
| sqlglot_transpile          | 1.78 ms                                                      | 1.75 ms: 1.02x faster                                                        |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.14 ms: 1.02x faster                                                        |
| meteor_contest             | 128 ms                                                       | 126 ms: 1.01x faster                                                         |
| sqlite_synth               | 2.77 us                                                      | 2.74 us: 1.01x faster                                                        |
| regex_compile              | 144 ms                                                       | 142 ms: 1.01x faster                                                         |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.57 sec: 1.01x faster                                                       |
| unpickle_list              | 4.66 us                                                      | 4.61 us: 1.01x faster                                                        |
| pidigits                   | 265 ms                                                       | 263 ms: 1.01x faster                                                         |
| regex_effbot               | 3.57 ms                                                      | 3.55 ms: 1.01x faster                                                        |
| unpickle                   | 14.8 us                                                      | 14.7 us: 1.01x faster                                                        |
| chameleon                  | 7.23 ms                                                      | 7.19 ms: 1.00x faster                                                        |
| django_template            | 38.2 ms                                                      | 38.5 ms: 1.01x slower                                                        |
| sqlglot_normalize          | 116 ms                                                       | 117 ms: 1.01x slower                                                         |
| pickle_list                | 4.43 us                                                      | 4.47 us: 1.01x slower                                                        |
| asyncio_websockets         | 387 ms                                                       | 391 ms: 1.01x slower                                                         |
| spectral_norm              | 91.6 ms                                                      | 92.7 ms: 1.01x slower                                                        |
| mako                       | 10.0 ms                                                      | 10.2 ms: 1.02x slower                                                        |
| unpickle_pure_python       | 210 us                                                       | 213 us: 1.02x slower                                                         |
| sqlglot_optimize           | 57.5 ms                                                      | 58.4 ms: 1.02x slower                                                        |
| logging_silent             | 94.4 ns                                                      | 96.2 ns: 1.02x slower                                                        |
| sympy_expand               | 484 ms                                                       | 495 ms: 1.02x slower                                                         |
| 2to3                       | 285 ms                                                       | 292 ms: 1.03x slower                                                         |
| json_dumps                 | 10.2 ms                                                      | 10.5 ms: 1.03x slower                                                        |
| aiohttp                    | 1.02 ms                                                      | 1.05 ms: 1.03x slower                                                        |
| pathlib                    | 18.9 ms                                                      | 19.4 ms: 1.03x slower                                                        |
| docutils                   | 2.87 sec                                                     | 2.95 sec: 1.03x slower                                                       |
| deepcopy                   | 368 us                                                       | 381 us: 1.03x slower                                                         |
| pickle_dict                | 32.5 us                                                      | 33.7 us: 1.03x slower                                                        |
| regex_dna                  | 239 ms                                                       | 249 ms: 1.04x slower                                                         |
| pycparser                  | 1.23 sec                                                     | 1.29 sec: 1.04x slower                                                       |
| json                       | 5.12 ms                                                      | 5.33 ms: 1.04x slower                                                        |
| json_loads                 | 24.4 us                                                      | 25.5 us: 1.04x slower                                                        |
| gunicorn                   | 1.00 ms                                                      | 1.05 ms: 1.05x slower                                                        |
| dulwich_log                | 65.4 ms                                                      | 68.7 ms: 1.05x slower                                                        |
| unpack_sequence            | 53.2 ns                                                      | 56.3 ns: 1.06x slower                                                        |
| tomli_loads                | 2.16 sec                                                     | 2.30 sec: 1.07x slower                                                       |
| hexiom                     | 5.96 ms                                                      | 6.41 ms: 1.08x slower                                                        |
| regex_v8                   | 23.6 ms                                                      | 25.7 ms: 1.09x slower                                                        |
| fannkuch                   | 350 ms                                                       | 382 ms: 1.09x slower                                                         |
| deltablue                  | 3.24 ms                                                      | 3.57 ms: 1.10x slower                                                        |
| python_startup             | 11.6 ms                                                      | 12.8 ms: 1.10x slower                                                        |
| create_gc_cycles           | 1.59 ms                                                      | 1.81 ms: 1.13x slower                                                        |
| telco                      | 6.96 ms                                                      | 7.91 ms: 1.14x slower                                                        |
| go                         | 150 ms                                                       | 172 ms: 1.15x slower                                                         |
| richards_super             | 51.3 ms                                                      | 59.3 ms: 1.16x slower                                                        |
| richards                   | 45.7 ms                                                      | 53.6 ms: 1.17x slower                                                        |
| pyflate                    | 439 ms                                                       | 535 ms: 1.22x slower                                                         |
| coverage                   | 66.7 ms                                                      | 85.0 ms: 1.27x slower                                                        |
| python_startup_no_site     | 8.64 ms                                                      | 11.1 ms: 1.28x slower                                                        |
| scimark_sor                | 109 ms                                                       | 144 ms: 1.32x slower                                                         |
| gc_traversal               | 3.48 ms                                                      | 4.67 ms: 1.34x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.00x faster                                                                 |

Benchmark hidden because not significant (11): nbody, xml_etree_iterparse, xml_etree_parse, sqlglot_parse, float, deepcopy_memo, deepcopy_reduce, xml_etree_process, tornado_http, pickle, dask
Ignored benchmarks (2) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240329-3.13.0a5+-bfc57d4/bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 72.43% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.91x