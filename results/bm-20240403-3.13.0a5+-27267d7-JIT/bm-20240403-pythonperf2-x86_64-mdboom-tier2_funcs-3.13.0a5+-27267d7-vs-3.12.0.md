# Results vs. 3.12.0

- fork: mdboom
- ref: tier2_funcs
- machine: linux-x86_64
- commit hash: 27267d7
- commit date: 2024-04-03
- overall geometric mean: 1.03x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 300 ms: 1.05x slower                                                |
| chameleon      | 7.23 ms                                                      | 7.44 ms: 1.03x slower                                               |
| docutils       | 2.87 sec                                                     | 3.07 sec: 1.07x slower                                              |
| tornado_http   | 121 ms                                                       | 123 ms: 1.02x slower                                                |
| Geometric mean | (ref)                                                        | 1.04x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 341 ms: 1.26x faster                                                |
| async_tree_none            | 452 ms                                                       | 361 ms: 1.25x faster                                                |
| async_tree_memoization_tg  | 540 ms                                                       | 439 ms: 1.23x faster                                                |
| async_tree_memoization     | 544 ms                                                       | 443 ms: 1.23x faster                                                |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 579 ms: 1.21x faster                                                |
| async_tree_io              | 1.04 sec                                                     | 889 ms: 1.17x faster                                                |
| async_tree_io_tg           | 1.05 sec                                                     | 904 ms: 1.17x faster                                                |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 598 ms: 1.16x faster                                                |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 261 ms: 1.01x faster                                                |
| float          | 76.6 ms                                                      | 77.6 ms: 1.01x slower                                               |
| nbody          | 88.0 ms                                                      | 98.4 ms: 1.12x slower                                               |
| Geometric mean | (ref)                                                        | 1.04x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_dna      | 239 ms                                                       | 241 ms: 1.01x slower                                                |
| regex_compile  | 144 ms                                                       | 150 ms: 1.04x slower                                                |
| regex_v8       | 23.6 ms                                                      | 26.1 ms: 1.11x slower                                               |
| Geometric mean | (ref)                                                        | 1.04x slower                                                        |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 31.0 us: 1.05x faster                                               |
| pickle_pure_python   | 318 us                                                       | 306 us: 1.04x faster                                                |
| unpickle_list        | 4.66 us                                                      | 4.55 us: 1.02x faster                                               |
| xml_etree_generate   | 86.1 ms                                                      | 85.2 ms: 1.01x faster                                               |
| tomli_loads          | 2.16 sec                                                     | 2.15 sec: 1.01x faster                                              |
| pickle_list          | 4.43 us                                                      | 4.46 us: 1.01x slower                                               |
| xml_etree_iterparse  | 103 ms                                                       | 104 ms: 1.01x slower                                                |
| xml_etree_parse      | 144 ms                                                       | 146 ms: 1.01x slower                                                |
| unpickle             | 14.8 us                                                      | 15.1 us: 1.02x slower                                               |
| json_loads           | 24.4 us                                                      | 25.2 us: 1.03x slower                                               |
| json_dumps           | 10.2 ms                                                      | 10.7 ms: 1.05x slower                                               |
| unpickle_pure_python | 210 us                                                       | 240 us: 1.14x slower                                                |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                        |

Benchmark hidden because not significant (2): xml_etree_process, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                               |
| python_startup_no_site | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                               |
| Geometric mean         | (ref)                                                        | 1.26x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 10.0 ms                                                      | 10.1 ms: 1.01x slower                                               |
| django_template | 38.2 ms                                                      | 40.1 ms: 1.05x slower                                               |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 341 ms: 1.26x faster                                                |
| async_tree_none            | 452 ms                                                       | 361 ms: 1.25x faster                                                |
| typing_runtime_protocols   | 152 us                                                       | 121 us: 1.25x faster                                                |
| async_tree_memoization_tg  | 540 ms                                                       | 439 ms: 1.23x faster                                                |
| async_tree_memoization     | 544 ms                                                       | 443 ms: 1.23x faster                                                |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 579 ms: 1.21x faster                                                |
| async_tree_io              | 1.04 sec                                                     | 889 ms: 1.17x faster                                                |
| async_tree_io_tg           | 1.05 sec                                                     | 904 ms: 1.17x faster                                                |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 598 ms: 1.16x faster                                                |
| generators                 | 37.4 ms                                                      | 33.3 ms: 1.12x faster                                               |
| comprehensions             | 21.9 us                                                      | 20.0 us: 1.10x faster                                               |
| pickle_dict                | 32.5 us                                                      | 31.0 us: 1.05x faster                                               |
| pickle_pure_python         | 318 us                                                       | 306 us: 1.04x faster                                                |
| sqlite_synth               | 2.77 us                                                      | 2.69 us: 1.03x faster                                               |
| crypto_pyaes               | 80.3 ms                                                      | 77.9 ms: 1.03x faster                                               |
| unpickle_list              | 4.66 us                                                      | 4.55 us: 1.02x faster                                               |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.13 ms: 1.02x faster                                               |
| asyncio_tcp                | 378 ms                                                       | 371 ms: 1.02x faster                                                |
| logging_format             | 7.48 us                                                      | 7.37 us: 1.02x faster                                               |
| pidigits                   | 265 ms                                                       | 261 ms: 1.01x faster                                                |
| xml_etree_generate         | 86.1 ms                                                      | 85.2 ms: 1.01x faster                                               |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.01x faster                                              |
| tomli_loads                | 2.16 sec                                                     | 2.15 sec: 1.01x faster                                              |
| mako                       | 10.0 ms                                                      | 10.1 ms: 1.01x slower                                               |
| pickle_list                | 4.43 us                                                      | 4.46 us: 1.01x slower                                               |
| regex_dna                  | 239 ms                                                       | 241 ms: 1.01x slower                                                |
| float                      | 76.6 ms                                                      | 77.6 ms: 1.01x slower                                               |
| raytrace                   | 298 ms                                                       | 302 ms: 1.01x slower                                                |
| sqlglot_transpile          | 1.78 ms                                                      | 1.80 ms: 1.01x slower                                               |
| xml_etree_iterparse        | 103 ms                                                       | 104 ms: 1.01x slower                                                |
| xml_etree_parse            | 144 ms                                                       | 146 ms: 1.01x slower                                                |
| sqlglot_parse              | 1.38 ms                                                      | 1.40 ms: 1.02x slower                                               |
| tornado_http               | 121 ms                                                       | 123 ms: 1.02x slower                                                |
| logging_simple             | 6.71 us                                                      | 6.82 us: 1.02x slower                                               |
| mdp                        | 2.57 sec                                                     | 2.62 sec: 1.02x slower                                              |
| unpickle                   | 14.8 us                                                      | 15.1 us: 1.02x slower                                               |
| pycparser                  | 1.23 sec                                                     | 1.26 sec: 1.02x slower                                              |
| pprint_safe_repr           | 807 ms                                                       | 827 ms: 1.02x slower                                                |
| dask                       | 392 ms                                                       | 403 ms: 1.03x slower                                                |
| chameleon                  | 7.23 ms                                                      | 7.44 ms: 1.03x slower                                               |
| logging_silent             | 94.4 ns                                                      | 97.2 ns: 1.03x slower                                               |
| json_loads                 | 24.4 us                                                      | 25.2 us: 1.03x slower                                               |
| meteor_contest             | 128 ms                                                       | 132 ms: 1.03x slower                                                |
| regex_compile              | 144 ms                                                       | 150 ms: 1.04x slower                                                |
| chaos                      | 64.0 ms                                                      | 66.8 ms: 1.04x slower                                               |
| spectral_norm              | 91.6 ms                                                      | 95.7 ms: 1.04x slower                                               |
| pathlib                    | 18.9 ms                                                      | 19.8 ms: 1.05x slower                                               |
| deepcopy_memo              | 36.8 us                                                      | 38.5 us: 1.05x slower                                               |
| pprint_pformat             | 1.65 sec                                                     | 1.73 sec: 1.05x slower                                              |
| json_dumps                 | 10.2 ms                                                      | 10.7 ms: 1.05x slower                                               |
| scimark_fft                | 301 ms                                                       | 316 ms: 1.05x slower                                                |
| json                       | 5.12 ms                                                      | 5.38 ms: 1.05x slower                                               |
| deepcopy                   | 368 us                                                       | 388 us: 1.05x slower                                                |
| django_template            | 38.2 ms                                                      | 40.1 ms: 1.05x slower                                               |
| sympy_expand               | 484 ms                                                       | 510 ms: 1.05x slower                                                |
| 2to3                       | 285 ms                                                       | 300 ms: 1.05x slower                                                |
| sympy_integrate            | 23.9 ms                                                      | 25.3 ms: 1.06x slower                                               |
| bench_mp_pool              | 4.76 ms                                                      | 5.04 ms: 1.06x slower                                               |
| dulwich_log                | 65.4 ms                                                      | 69.2 ms: 1.06x slower                                               |
| sqlglot_normalize          | 116 ms                                                       | 123 ms: 1.06x slower                                                |
| docutils                   | 2.87 sec                                                     | 3.07 sec: 1.07x slower                                              |
| scimark_monte_carlo        | 69.0 ms                                                      | 74.4 ms: 1.08x slower                                               |
| fannkuch                   | 350 ms                                                       | 378 ms: 1.08x slower                                                |
| gunicorn                   | 1.00 ms                                                      | 1.09 ms: 1.09x slower                                               |
| sqlglot_optimize           | 57.5 ms                                                      | 62.6 ms: 1.09x slower                                               |
| aiohttp                    | 1.02 ms                                                      | 1.13 ms: 1.11x slower                                               |
| regex_v8                   | 23.6 ms                                                      | 26.1 ms: 1.11x slower                                               |
| nbody                      | 88.0 ms                                                      | 98.4 ms: 1.12x slower                                               |
| unpickle_pure_python       | 210 us                                                       | 240 us: 1.14x slower                                                |
| pyflate                    | 439 ms                                                       | 502 ms: 1.15x slower                                                |
| create_gc_cycles           | 1.59 ms                                                      | 1.82 ms: 1.15x slower                                               |
| deltablue                  | 3.24 ms                                                      | 3.73 ms: 1.15x slower                                               |
| richards                   | 45.7 ms                                                      | 52.9 ms: 1.16x slower                                               |
| richards_super             | 51.3 ms                                                      | 59.4 ms: 1.16x slower                                               |
| nqueens                    | 89.9 ms                                                      | 104 ms: 1.16x slower                                                |
| go                         | 150 ms                                                       | 174 ms: 1.16x slower                                                |
| python_startup             | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                               |
| telco                      | 6.96 ms                                                      | 8.18 ms: 1.17x slower                                               |
| bench_thread_pool          | 950 us                                                       | 1.12 ms: 1.18x slower                                               |
| coverage                   | 66.7 ms                                                      | 83.6 ms: 1.25x slower                                               |
| scimark_lu                 | 98.8 ms                                                      | 125 ms: 1.27x slower                                                |
| hexiom                     | 5.96 ms                                                      | 7.56 ms: 1.27x slower                                               |
| python_startup_no_site     | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                               |
| gc_traversal               | 3.48 ms                                                      | 4.80 ms: 1.38x slower                                               |
| scimark_sor                | 109 ms                                                       | 155 ms: 1.42x slower                                                |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                        |

Benchmark hidden because not significant (10): mypy2, xml_etree_process, coroutines, regex_effbot, deepcopy_reduce, pickle, sympy_str, async_generators, sympy_sum, asyncio_websockets
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240403-3.13.0a5+-27267d7-JIT/bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 0.98x