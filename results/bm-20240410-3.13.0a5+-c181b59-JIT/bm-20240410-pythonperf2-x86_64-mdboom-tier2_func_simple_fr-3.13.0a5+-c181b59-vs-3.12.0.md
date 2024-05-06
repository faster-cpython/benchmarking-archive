# Results vs. 3.12.0

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: linux-x86_64
- commit hash: c181b59
- commit date: 2024-04-10
- overall geometric mean: 1.02x slower
- HPT reliability: 99.70%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 300 ms: 1.05x slower                                                         |
| chameleon      | 7.23 ms                                                      | 7.65 ms: 1.06x slower                                                        |
| docutils       | 2.87 sec                                                     | 3.10 sec: 1.08x slower                                                       |
| Geometric mean | (ref)                                                        | 1.05x slower                                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 333 ms: 1.29x faster                                                         |
| async_tree_memoization_tg  | 540 ms                                                       | 425 ms: 1.27x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 446 ms: 1.22x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 868 ms: 1.21x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 871 ms: 1.20x faster                                                         |
| async_tree_none            | 452 ms                                                       | 378 ms: 1.19x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 591 ms: 1.18x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 609 ms: 1.14x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 261 ms: 1.01x faster                                                         |
| float          | 76.6 ms                                                      | 76.1 ms: 1.01x faster                                                        |
| nbody          | 88.0 ms                                                      | 96.2 ms: 1.09x slower                                                        |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 239 ms                                                       | 245 ms: 1.03x slower                                                         |
| regex_compile  | 144 ms                                                       | 148 ms: 1.03x slower                                                         |
| regex_effbot   | 3.57 ms                                                      | 3.71 ms: 1.04x slower                                                        |
| regex_v8       | 23.6 ms                                                      | 25.5 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                        | 1.04x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 318 us                                                       | 311 us: 1.02x faster                                                         |
| xml_etree_generate   | 86.1 ms                                                      | 84.6 ms: 1.02x faster                                                        |
| tomli_loads          | 2.16 sec                                                     | 2.13 sec: 1.01x faster                                                       |
| pickle_list          | 4.43 us                                                      | 4.39 us: 1.01x faster                                                        |
| xml_etree_iterparse  | 103 ms                                                       | 102 ms: 1.01x faster                                                         |
| pickle_dict          | 32.5 us                                                      | 32.6 us: 1.00x slower                                                        |
| pickle               | 10.5 us                                                      | 10.6 us: 1.01x slower                                                        |
| xml_etree_process    | 58.4 ms                                                      | 59.0 ms: 1.01x slower                                                        |
| unpickle             | 14.8 us                                                      | 15.0 us: 1.01x slower                                                        |
| json_dumps           | 10.2 ms                                                      | 10.4 ms: 1.02x slower                                                        |
| xml_etree_parse      | 144 ms                                                       | 148 ms: 1.03x slower                                                         |
| json_loads           | 24.4 us                                                      | 25.5 us: 1.05x slower                                                        |
| unpickle_pure_python | 210 us                                                       | 232 us: 1.11x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                                 |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 13.4 ms: 1.16x slower                                                        |
| python_startup_no_site | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.25x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|-----------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako      | 10.0 ms                                                      | 10.1 ms: 1.01x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 333 ms: 1.29x faster                                                         |
| async_tree_memoization_tg  | 540 ms                                                       | 425 ms: 1.27x faster                                                         |
| typing_runtime_protocols   | 152 us                                                       | 124 us: 1.22x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 446 ms: 1.22x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 868 ms: 1.21x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 871 ms: 1.20x faster                                                         |
| async_tree_none            | 452 ms                                                       | 378 ms: 1.19x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 591 ms: 1.18x faster                                                         |
| comprehensions             | 21.9 us                                                      | 19.1 us: 1.15x faster                                                        |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 609 ms: 1.14x faster                                                         |
| generators                 | 37.4 ms                                                      | 33.2 ms: 1.13x faster                                                        |
| raytrace                   | 298 ms                                                       | 272 ms: 1.10x faster                                                         |
| logging_format             | 7.48 us                                                      | 6.95 us: 1.08x faster                                                        |
| logging_simple             | 6.71 us                                                      | 6.27 us: 1.07x faster                                                        |
| crypto_pyaes               | 80.3 ms                                                      | 76.9 ms: 1.05x faster                                                        |
| coroutines                 | 23.0 ms                                                      | 22.1 ms: 1.04x faster                                                        |
| pickle_pure_python         | 318 us                                                       | 311 us: 1.02x faster                                                         |
| sqlite_synth               | 2.77 us                                                      | 2.71 us: 1.02x faster                                                        |
| bench_thread_pool          | 950 us                                                       | 930 us: 1.02x faster                                                         |
| xml_etree_generate         | 86.1 ms                                                      | 84.6 ms: 1.02x faster                                                        |
| async_generators           | 390 ms                                                       | 384 ms: 1.02x faster                                                         |
| pidigits                   | 265 ms                                                       | 261 ms: 1.01x faster                                                         |
| tomli_loads                | 2.16 sec                                                     | 2.13 sec: 1.01x faster                                                       |
| asyncio_tcp                | 378 ms                                                       | 374 ms: 1.01x faster                                                         |
| pickle_list                | 4.43 us                                                      | 4.39 us: 1.01x faster                                                        |
| xml_etree_iterparse        | 103 ms                                                       | 102 ms: 1.01x faster                                                         |
| float                      | 76.6 ms                                                      | 76.1 ms: 1.01x faster                                                        |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.18 ms: 1.01x faster                                                        |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.00x faster                                                       |
| pickle_dict                | 32.5 us                                                      | 32.6 us: 1.00x slower                                                        |
| pickle                     | 10.5 us                                                      | 10.6 us: 1.01x slower                                                        |
| mako                       | 10.0 ms                                                      | 10.1 ms: 1.01x slower                                                        |
| sympy_sum                  | 162 ms                                                       | 164 ms: 1.01x slower                                                         |
| mdp                        | 2.57 sec                                                     | 2.59 sec: 1.01x slower                                                       |
| xml_etree_process          | 58.4 ms                                                      | 59.0 ms: 1.01x slower                                                        |
| asyncio_websockets         | 387 ms                                                       | 391 ms: 1.01x slower                                                         |
| unpickle                   | 14.8 us                                                      | 15.0 us: 1.01x slower                                                        |
| chaos                      | 64.0 ms                                                      | 64.8 ms: 1.01x slower                                                        |
| json_dumps                 | 10.2 ms                                                      | 10.4 ms: 1.02x slower                                                        |
| dask                       | 392 ms                                                       | 400 ms: 1.02x slower                                                         |
| richards                   | 45.7 ms                                                      | 46.7 ms: 1.02x slower                                                        |
| sympy_str                  | 302 ms                                                       | 309 ms: 1.02x slower                                                         |
| spectral_norm              | 91.6 ms                                                      | 93.8 ms: 1.02x slower                                                        |
| pprint_safe_repr           | 807 ms                                                       | 827 ms: 1.02x slower                                                         |
| sqlglot_transpile          | 1.78 ms                                                      | 1.82 ms: 1.02x slower                                                        |
| regex_dna                  | 239 ms                                                       | 245 ms: 1.03x slower                                                         |
| xml_etree_parse            | 144 ms                                                       | 148 ms: 1.03x slower                                                         |
| regex_compile              | 144 ms                                                       | 148 ms: 1.03x slower                                                         |
| meteor_contest             | 128 ms                                                       | 132 ms: 1.03x slower                                                         |
| pycparser                  | 1.23 sec                                                     | 1.27 sec: 1.03x slower                                                       |
| sqlglot_parse              | 1.38 ms                                                      | 1.42 ms: 1.03x slower                                                        |
| pathlib                    | 18.9 ms                                                      | 19.6 ms: 1.04x slower                                                        |
| regex_effbot               | 3.57 ms                                                      | 3.71 ms: 1.04x slower                                                        |
| pprint_pformat             | 1.65 sec                                                     | 1.72 sec: 1.04x slower                                                       |
| dulwich_log                | 65.4 ms                                                      | 68.2 ms: 1.04x slower                                                        |
| scimark_monte_carlo        | 69.0 ms                                                      | 72.0 ms: 1.04x slower                                                        |
| richards_super             | 51.3 ms                                                      | 53.7 ms: 1.05x slower                                                        |
| logging_silent             | 94.4 ns                                                      | 98.9 ns: 1.05x slower                                                        |
| json_loads                 | 24.4 us                                                      | 25.5 us: 1.05x slower                                                        |
| sympy_integrate            | 23.9 ms                                                      | 25.1 ms: 1.05x slower                                                        |
| 2to3                       | 285 ms                                                       | 300 ms: 1.05x slower                                                         |
| scimark_fft                | 301 ms                                                       | 317 ms: 1.05x slower                                                         |
| json                       | 5.12 ms                                                      | 5.40 ms: 1.05x slower                                                        |
| deepcopy_memo              | 36.8 us                                                      | 38.8 us: 1.05x slower                                                        |
| chameleon                  | 7.23 ms                                                      | 7.65 ms: 1.06x slower                                                        |
| sqlglot_normalize          | 116 ms                                                       | 124 ms: 1.07x slower                                                         |
| sympy_expand               | 484 ms                                                       | 518 ms: 1.07x slower                                                         |
| regex_v8                   | 23.6 ms                                                      | 25.5 ms: 1.08x slower                                                        |
| docutils                   | 2.87 sec                                                     | 3.10 sec: 1.08x slower                                                       |
| deepcopy                   | 368 us                                                       | 401 us: 1.09x slower                                                         |
| nbody                      | 88.0 ms                                                      | 96.2 ms: 1.09x slower                                                        |
| sqlglot_optimize           | 57.5 ms                                                      | 62.9 ms: 1.09x slower                                                        |
| gunicorn                   | 1.00 ms                                                      | 1.10 ms: 1.10x slower                                                        |
| pyflate                    | 439 ms                                                       | 483 ms: 1.10x slower                                                         |
| deepcopy_reduce            | 3.37 us                                                      | 3.72 us: 1.10x slower                                                        |
| unpickle_pure_python       | 210 us                                                       | 232 us: 1.11x slower                                                         |
| nqueens                    | 89.9 ms                                                      | 99.8 ms: 1.11x slower                                                        |
| fannkuch                   | 350 ms                                                       | 389 ms: 1.11x slower                                                         |
| aiohttp                    | 1.02 ms                                                      | 1.15 ms: 1.12x slower                                                        |
| python_startup             | 11.6 ms                                                      | 13.4 ms: 1.16x slower                                                        |
| go                         | 150 ms                                                       | 175 ms: 1.17x slower                                                         |
| deltablue                  | 3.24 ms                                                      | 3.80 ms: 1.17x slower                                                        |
| create_gc_cycles           | 1.59 ms                                                      | 1.87 ms: 1.18x slower                                                        |
| coverage                   | 66.7 ms                                                      | 78.8 ms: 1.18x slower                                                        |
| telco                      | 6.96 ms                                                      | 8.29 ms: 1.19x slower                                                        |
| hexiom                     | 5.96 ms                                                      | 7.17 ms: 1.20x slower                                                        |
| scimark_lu                 | 98.8 ms                                                      | 121 ms: 1.23x slower                                                         |
| gc_traversal               | 3.48 ms                                                      | 4.38 ms: 1.26x slower                                                        |
| python_startup_no_site     | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                        |
| scimark_sor                | 109 ms                                                       | 152 ms: 1.39x slower                                                         |
| Geometric mean             | (ref)                                                        | 1.02x slower                                                                 |

Benchmark hidden because not significant (4): bench_mp_pool, mypy2, unpickle_list, tornado_http
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240410-3.13.0a5+-c181b59-JIT/bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.70% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x