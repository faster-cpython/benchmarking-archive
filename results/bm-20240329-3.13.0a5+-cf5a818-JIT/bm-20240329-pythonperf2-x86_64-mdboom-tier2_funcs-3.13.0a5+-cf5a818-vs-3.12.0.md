# Results vs. 3.12.0

- fork: mdboom
- ref: tier2_funcs
- machine: linux-x86_64
- commit hash: cf5a818
- commit date: 2024-03-29
- overall geometric mean: 1.03x slower
- HPT reliability: 99.69%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 300 ms: 1.05x slower                                                |
| chameleon      | 7.23 ms                                                      | 7.54 ms: 1.04x slower                                               |
| docutils       | 2.87 sec                                                     | 3.06 sec: 1.07x slower                                              |
| tornado_http   | 121 ms                                                       | 124 ms: 1.02x slower                                                |
| Geometric mean | (ref)                                                        | 1.05x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 339 ms: 1.27x faster                                                |
| async_tree_none            | 452 ms                                                       | 358 ms: 1.26x faster                                                |
| async_tree_memoization     | 544 ms                                                       | 441 ms: 1.23x faster                                                |
| async_tree_memoization_tg  | 540 ms                                                       | 441 ms: 1.23x faster                                                |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 578 ms: 1.21x faster                                                |
| async_tree_io              | 1.04 sec                                                     | 886 ms: 1.18x faster                                                |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 594 ms: 1.17x faster                                                |
| async_tree_io_tg           | 1.05 sec                                                     | 908 ms: 1.16x faster                                                |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 261 ms: 1.01x faster                                                |
| nbody          | 88.0 ms                                                      | 96.2 ms: 1.09x slower                                               |
| Geometric mean | (ref)                                                        | 1.03x slower                                                        |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.61 ms: 1.01x slower                                               |
| regex_dna      | 239 ms                                                       | 241 ms: 1.01x slower                                                |
| regex_compile  | 144 ms                                                       | 149 ms: 1.03x slower                                                |
| regex_v8       | 23.6 ms                                                      | 25.4 ms: 1.08x slower                                               |
| Geometric mean | (ref)                                                        | 1.03x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 30.7 us: 1.06x faster                                               |
| xml_etree_generate   | 86.1 ms                                                      | 84.7 ms: 1.02x faster                                               |
| pickle_pure_python   | 318 us                                                       | 313 us: 1.02x faster                                                |
| pickle_list          | 4.43 us                                                      | 4.37 us: 1.01x faster                                               |
| xml_etree_parse      | 144 ms                                                       | 143 ms: 1.01x faster                                                |
| xml_etree_process    | 58.4 ms                                                      | 58.0 ms: 1.01x faster                                               |
| pickle               | 10.5 us                                                      | 10.6 us: 1.01x slower                                               |
| tomli_loads          | 2.16 sec                                                     | 2.19 sec: 1.01x slower                                              |
| unpickle             | 14.8 us                                                      | 15.1 us: 1.02x slower                                               |
| json_dumps           | 10.2 ms                                                      | 10.6 ms: 1.03x slower                                               |
| json_loads           | 24.4 us                                                      | 25.3 us: 1.04x slower                                               |
| unpickle_pure_python | 210 us                                                       | 232 us: 1.11x slower                                                |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                        |

Benchmark hidden because not significant (2): xml_etree_iterparse, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                               |
| python_startup_no_site | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                               |
| Geometric mean         | (ref)                                                        | 1.26x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| django_template | 38.2 ms                                                      | 40.0 ms: 1.05x slower                                               |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                        |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 339 ms: 1.27x faster                                                |
| async_tree_none            | 452 ms                                                       | 358 ms: 1.26x faster                                                |
| typing_runtime_protocols   | 152 us                                                       | 121 us: 1.25x faster                                                |
| async_tree_memoization     | 544 ms                                                       | 441 ms: 1.23x faster                                                |
| async_tree_memoization_tg  | 540 ms                                                       | 441 ms: 1.23x faster                                                |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 578 ms: 1.21x faster                                                |
| async_tree_io              | 1.04 sec                                                     | 886 ms: 1.18x faster                                                |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 594 ms: 1.17x faster                                                |
| async_tree_io_tg           | 1.05 sec                                                     | 908 ms: 1.16x faster                                                |
| generators                 | 37.4 ms                                                      | 33.6 ms: 1.11x faster                                               |
| comprehensions             | 21.9 us                                                      | 19.9 us: 1.10x faster                                               |
| pickle_dict                | 32.5 us                                                      | 30.7 us: 1.06x faster                                               |
| logging_format             | 7.48 us                                                      | 7.14 us: 1.05x faster                                               |
| crypto_pyaes               | 80.3 ms                                                      | 77.4 ms: 1.04x faster                                               |
| sqlite_synth               | 2.77 us                                                      | 2.70 us: 1.03x faster                                               |
| logging_simple             | 6.71 us                                                      | 6.56 us: 1.02x faster                                               |
| xml_etree_generate         | 86.1 ms                                                      | 84.7 ms: 1.02x faster                                               |
| pickle_pure_python         | 318 us                                                       | 313 us: 1.02x faster                                                |
| coroutines                 | 23.0 ms                                                      | 22.6 ms: 1.02x faster                                               |
| pidigits                   | 265 ms                                                       | 261 ms: 1.01x faster                                                |
| pickle_list                | 4.43 us                                                      | 4.37 us: 1.01x faster                                               |
| asyncio_tcp                | 378 ms                                                       | 373 ms: 1.01x faster                                                |
| sympy_sum                  | 162 ms                                                       | 161 ms: 1.01x faster                                                |
| xml_etree_parse            | 144 ms                                                       | 143 ms: 1.01x faster                                                |
| async_generators           | 390 ms                                                       | 387 ms: 1.01x faster                                                |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.01x faster                                              |
| xml_etree_process          | 58.4 ms                                                      | 58.0 ms: 1.01x faster                                               |
| pickle                     | 10.5 us                                                      | 10.6 us: 1.01x slower                                               |
| regex_effbot               | 3.57 ms                                                      | 3.61 ms: 1.01x slower                                               |
| regex_dna                  | 239 ms                                                       | 241 ms: 1.01x slower                                                |
| tomli_loads                | 2.16 sec                                                     | 2.19 sec: 1.01x slower                                              |
| mdp                        | 2.57 sec                                                     | 2.61 sec: 1.01x slower                                              |
| unpickle                   | 14.8 us                                                      | 15.1 us: 1.02x slower                                               |
| tornado_http               | 121 ms                                                       | 124 ms: 1.02x slower                                                |
| pprint_safe_repr           | 807 ms                                                       | 823 ms: 1.02x slower                                                |
| sqlglot_transpile          | 1.78 ms                                                      | 1.81 ms: 1.02x slower                                               |
| pathlib                    | 18.9 ms                                                      | 19.3 ms: 1.02x slower                                               |
| sqlglot_parse              | 1.38 ms                                                      | 1.41 ms: 1.02x slower                                               |
| spectral_norm              | 91.6 ms                                                      | 94.0 ms: 1.03x slower                                               |
| pprint_pformat             | 1.65 sec                                                     | 1.70 sec: 1.03x slower                                              |
| meteor_contest             | 128 ms                                                       | 132 ms: 1.03x slower                                                |
| logging_silent             | 94.4 ns                                                      | 97.0 ns: 1.03x slower                                               |
| dask                       | 392 ms                                                       | 404 ms: 1.03x slower                                                |
| regex_compile              | 144 ms                                                       | 149 ms: 1.03x slower                                                |
| json_dumps                 | 10.2 ms                                                      | 10.6 ms: 1.03x slower                                               |
| chaos                      | 64.0 ms                                                      | 66.2 ms: 1.04x slower                                               |
| deepcopy_memo              | 36.8 us                                                      | 38.1 us: 1.04x slower                                               |
| pycparser                  | 1.23 sec                                                     | 1.28 sec: 1.04x slower                                              |
| json_loads                 | 24.4 us                                                      | 25.3 us: 1.04x slower                                               |
| chameleon                  | 7.23 ms                                                      | 7.54 ms: 1.04x slower                                               |
| sympy_integrate            | 23.9 ms                                                      | 25.0 ms: 1.05x slower                                               |
| scimark_fft                | 301 ms                                                       | 315 ms: 1.05x slower                                                |
| django_template            | 38.2 ms                                                      | 40.0 ms: 1.05x slower                                               |
| dulwich_log                | 65.4 ms                                                      | 68.7 ms: 1.05x slower                                               |
| 2to3                       | 285 ms                                                       | 300 ms: 1.05x slower                                                |
| sympy_expand               | 484 ms                                                       | 509 ms: 1.05x slower                                                |
| deepcopy                   | 368 us                                                       | 389 us: 1.05x slower                                                |
| json                       | 5.12 ms                                                      | 5.40 ms: 1.06x slower                                               |
| bench_mp_pool              | 4.76 ms                                                      | 5.05 ms: 1.06x slower                                               |
| scimark_monte_carlo        | 69.0 ms                                                      | 73.5 ms: 1.07x slower                                               |
| docutils                   | 2.87 sec                                                     | 3.06 sec: 1.07x slower                                              |
| gunicorn                   | 1.00 ms                                                      | 1.08 ms: 1.07x slower                                               |
| regex_v8                   | 23.6 ms                                                      | 25.4 ms: 1.08x slower                                               |
| sqlglot_normalize          | 116 ms                                                       | 126 ms: 1.09x slower                                                |
| richards                   | 45.7 ms                                                      | 50.0 ms: 1.09x slower                                               |
| nbody                      | 88.0 ms                                                      | 96.2 ms: 1.09x slower                                               |
| fannkuch                   | 350 ms                                                       | 384 ms: 1.10x slower                                                |
| sqlglot_optimize           | 57.5 ms                                                      | 63.1 ms: 1.10x slower                                               |
| aiohttp                    | 1.02 ms                                                      | 1.12 ms: 1.10x slower                                               |
| unpickle_pure_python       | 210 us                                                       | 232 us: 1.11x slower                                                |
| unpack_sequence            | 53.2 ns                                                      | 59.6 ns: 1.12x slower                                               |
| richards_super             | 51.3 ms                                                      | 57.6 ms: 1.12x slower                                               |
| create_gc_cycles           | 1.59 ms                                                      | 1.80 ms: 1.13x slower                                               |
| nqueens                    | 89.9 ms                                                      | 103 ms: 1.15x slower                                                |
| deltablue                  | 3.24 ms                                                      | 3.74 ms: 1.16x slower                                               |
| python_startup             | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                               |
| bench_thread_pool          | 950 us                                                       | 1.11 ms: 1.16x slower                                               |
| telco                      | 6.96 ms                                                      | 8.15 ms: 1.17x slower                                               |
| pyflate                    | 439 ms                                                       | 516 ms: 1.18x slower                                                |
| go                         | 150 ms                                                       | 179 ms: 1.20x slower                                                |
| scimark_lu                 | 98.8 ms                                                      | 120 ms: 1.22x slower                                                |
| hexiom                     | 5.96 ms                                                      | 7.52 ms: 1.26x slower                                               |
| coverage                   | 66.7 ms                                                      | 86.4 ms: 1.30x slower                                               |
| gc_traversal               | 3.48 ms                                                      | 4.56 ms: 1.31x slower                                               |
| python_startup_no_site     | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                               |
| scimark_sor                | 109 ms                                                       | 154 ms: 1.42x slower                                                |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                        |

Benchmark hidden because not significant (10): scimark_sparse_mat_mult, mako, mypy2, asyncio_websockets, deepcopy_reduce, xml_etree_iterparse, unpickle_list, sympy_str, raytrace, float
Ignored benchmarks (2) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240329-3.13.0a5+-cf5a818-JIT/bm-20240329-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-cf5a818.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.69% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x