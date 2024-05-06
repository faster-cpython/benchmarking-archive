# Results vs. 3.12.0

- fork: mdboom
- ref: tier2_pystats_misses
- machine: linux-x86_64
- commit hash: ee60448
- commit date: 2024-04-02
- overall geometric mean: 1.03x slower
- HPT reliability: 99.88%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 300 ms: 1.05x slower                                                         |
| chameleon      | 7.23 ms                                                      | 7.54 ms: 1.04x slower                                                        |
| docutils       | 2.87 sec                                                     | 3.11 sec: 1.08x slower                                                       |
| tornado_http   | 121 ms                                                       | 125 ms: 1.03x slower                                                         |
| Geometric mean | (ref)                                                        | 1.05x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 333 ms: 1.29x faster                                                         |
| async_tree_memoization_tg  | 540 ms                                                       | 423 ms: 1.28x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 440 ms: 1.24x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 858 ms: 1.23x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 858 ms: 1.21x faster                                                         |
| async_tree_none            | 452 ms                                                       | 377 ms: 1.20x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 588 ms: 1.19x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 602 ms: 1.16x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.22x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 261 ms: 1.01x faster                                                         |
| nbody          | 88.0 ms                                                      | 95.6 ms: 1.09x slower                                                        |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                 |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.51 ms: 1.02x faster                                                        |
| regex_compile  | 144 ms                                                       | 150 ms: 1.04x slower                                                         |
| regex_dna      | 239 ms                                                       | 249 ms: 1.04x slower                                                         |
| regex_v8       | 23.6 ms                                                      | 25.9 ms: 1.09x slower                                                        |
| Geometric mean | (ref)                                                        | 1.04x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_pure_python   | 318 us                                                       | 311 us: 1.02x faster                                                         |
| unpickle             | 14.8 us                                                      | 14.5 us: 1.02x faster                                                        |
| xml_etree_generate   | 86.1 ms                                                      | 84.9 ms: 1.01x faster                                                        |
| tomli_loads          | 2.16 sec                                                     | 2.13 sec: 1.01x faster                                                       |
| xml_etree_iterparse  | 103 ms                                                       | 102 ms: 1.01x faster                                                         |
| xml_etree_process    | 58.4 ms                                                      | 58.8 ms: 1.01x slower                                                        |
| xml_etree_parse      | 144 ms                                                       | 145 ms: 1.01x slower                                                         |
| pickle_dict          | 32.5 us                                                      | 32.8 us: 1.01x slower                                                        |
| unpickle_list        | 4.66 us                                                      | 4.69 us: 1.01x slower                                                        |
| pickle               | 10.5 us                                                      | 10.7 us: 1.02x slower                                                        |
| json_dumps           | 10.2 ms                                                      | 10.5 ms: 1.03x slower                                                        |
| json_loads           | 24.4 us                                                      | 25.4 us: 1.04x slower                                                        |
| unpickle_pure_python | 210 us                                                       | 232 us: 1.11x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                                 |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 13.7 ms: 1.18x slower                                                        |
| python_startup_no_site | 8.64 ms                                                      | 11.9 ms: 1.38x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.27x slower                                                                 |

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 333 ms: 1.29x faster                                                         |
| async_tree_memoization_tg  | 540 ms                                                       | 423 ms: 1.28x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 440 ms: 1.24x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 858 ms: 1.23x faster                                                         |
| typing_runtime_protocols   | 152 us                                                       | 124 us: 1.23x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 858 ms: 1.21x faster                                                         |
| async_tree_none            | 452 ms                                                       | 377 ms: 1.20x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 588 ms: 1.19x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 602 ms: 1.16x faster                                                         |
| comprehensions             | 21.9 us                                                      | 19.2 us: 1.14x faster                                                        |
| generators                 | 37.4 ms                                                      | 33.2 ms: 1.13x faster                                                        |
| logging_format             | 7.48 us                                                      | 7.10 us: 1.05x faster                                                        |
| crypto_pyaes               | 80.3 ms                                                      | 76.9 ms: 1.04x faster                                                        |
| logging_simple             | 6.71 us                                                      | 6.43 us: 1.04x faster                                                        |
| coroutines                 | 23.0 ms                                                      | 22.1 ms: 1.04x faster                                                        |
| raytrace                   | 298 ms                                                       | 287 ms: 1.04x faster                                                         |
| sqlite_synth               | 2.77 us                                                      | 2.68 us: 1.04x faster                                                        |
| pickle_pure_python         | 318 us                                                       | 311 us: 1.02x faster                                                         |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.11 ms: 1.02x faster                                                        |
| unpickle                   | 14.8 us                                                      | 14.5 us: 1.02x faster                                                        |
| regex_effbot               | 3.57 ms                                                      | 3.51 ms: 1.02x faster                                                        |
| xml_etree_generate         | 86.1 ms                                                      | 84.9 ms: 1.01x faster                                                        |
| tomli_loads                | 2.16 sec                                                     | 2.13 sec: 1.01x faster                                                       |
| pidigits                   | 265 ms                                                       | 261 ms: 1.01x faster                                                         |
| xml_etree_iterparse        | 103 ms                                                       | 102 ms: 1.01x faster                                                         |
| asyncio_tcp                | 378 ms                                                       | 376 ms: 1.01x faster                                                         |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.01x faster                                                       |
| xml_etree_process          | 58.4 ms                                                      | 58.8 ms: 1.01x slower                                                        |
| async_generators           | 390 ms                                                       | 393 ms: 1.01x slower                                                         |
| xml_etree_parse            | 144 ms                                                       | 145 ms: 1.01x slower                                                         |
| pickle_dict                | 32.5 us                                                      | 32.8 us: 1.01x slower                                                        |
| unpickle_list              | 4.66 us                                                      | 4.69 us: 1.01x slower                                                        |
| spectral_norm              | 91.6 ms                                                      | 92.6 ms: 1.01x slower                                                        |
| mdp                        | 2.57 sec                                                     | 2.60 sec: 1.01x slower                                                       |
| logging_silent             | 94.4 ns                                                      | 95.7 ns: 1.01x slower                                                        |
| pickle                     | 10.5 us                                                      | 10.7 us: 1.02x slower                                                        |
| asyncio_websockets         | 387 ms                                                       | 395 ms: 1.02x slower                                                         |
| scimark_monte_carlo        | 69.0 ms                                                      | 70.6 ms: 1.02x slower                                                        |
| json_dumps                 | 10.2 ms                                                      | 10.5 ms: 1.03x slower                                                        |
| tornado_http               | 121 ms                                                       | 125 ms: 1.03x slower                                                         |
| sympy_sum                  | 162 ms                                                       | 167 ms: 1.03x slower                                                         |
| dask                       | 392 ms                                                       | 405 ms: 1.03x slower                                                         |
| sympy_str                  | 302 ms                                                       | 312 ms: 1.03x slower                                                         |
| pycparser                  | 1.23 sec                                                     | 1.28 sec: 1.03x slower                                                       |
| sqlglot_transpile          | 1.78 ms                                                      | 1.84 ms: 1.03x slower                                                        |
| sqlglot_parse              | 1.38 ms                                                      | 1.43 ms: 1.04x slower                                                        |
| regex_compile              | 144 ms                                                       | 150 ms: 1.04x slower                                                         |
| scimark_fft                | 301 ms                                                       | 313 ms: 1.04x slower                                                         |
| pathlib                    | 18.9 ms                                                      | 19.7 ms: 1.04x slower                                                        |
| deepcopy_reduce            | 3.37 us                                                      | 3.51 us: 1.04x slower                                                        |
| chameleon                  | 7.23 ms                                                      | 7.54 ms: 1.04x slower                                                        |
| regex_dna                  | 239 ms                                                       | 249 ms: 1.04x slower                                                         |
| json_loads                 | 24.4 us                                                      | 25.4 us: 1.04x slower                                                        |
| meteor_contest             | 128 ms                                                       | 134 ms: 1.05x slower                                                         |
| sqlglot_normalize          | 116 ms                                                       | 122 ms: 1.05x slower                                                         |
| 2to3                       | 285 ms                                                       | 300 ms: 1.05x slower                                                         |
| pprint_safe_repr           | 807 ms                                                       | 852 ms: 1.06x slower                                                         |
| pprint_pformat             | 1.65 sec                                                     | 1.76 sec: 1.06x slower                                                       |
| deepcopy_memo              | 36.8 us                                                      | 39.4 us: 1.07x slower                                                        |
| json                       | 5.12 ms                                                      | 5.48 ms: 1.07x slower                                                        |
| sympy_expand               | 484 ms                                                       | 518 ms: 1.07x slower                                                         |
| deepcopy                   | 368 us                                                       | 395 us: 1.07x slower                                                         |
| sympy_integrate            | 23.9 ms                                                      | 25.9 ms: 1.08x slower                                                        |
| docutils                   | 2.87 sec                                                     | 3.11 sec: 1.08x slower                                                       |
| bench_mp_pool              | 4.76 ms                                                      | 5.17 ms: 1.08x slower                                                        |
| sqlglot_optimize           | 57.5 ms                                                      | 62.4 ms: 1.09x slower                                                        |
| nbody                      | 88.0 ms                                                      | 95.6 ms: 1.09x slower                                                        |
| regex_v8                   | 23.6 ms                                                      | 25.9 ms: 1.09x slower                                                        |
| dulwich_log                | 65.4 ms                                                      | 71.7 ms: 1.10x slower                                                        |
| fannkuch                   | 350 ms                                                       | 386 ms: 1.10x slower                                                         |
| pyflate                    | 439 ms                                                       | 485 ms: 1.11x slower                                                         |
| unpickle_pure_python       | 210 us                                                       | 232 us: 1.11x slower                                                         |
| richards                   | 45.7 ms                                                      | 50.6 ms: 1.11x slower                                                        |
| deltablue                  | 3.24 ms                                                      | 3.58 ms: 1.11x slower                                                        |
| gunicorn                   | 1.00 ms                                                      | 1.12 ms: 1.12x slower                                                        |
| aiohttp                    | 1.02 ms                                                      | 1.14 ms: 1.12x slower                                                        |
| richards_super             | 51.3 ms                                                      | 58.3 ms: 1.13x slower                                                        |
| telco                      | 6.96 ms                                                      | 8.01 ms: 1.15x slower                                                        |
| nqueens                    | 89.9 ms                                                      | 105 ms: 1.17x slower                                                         |
| bench_thread_pool          | 950 us                                                       | 1.11 ms: 1.17x slower                                                        |
| python_startup             | 11.6 ms                                                      | 13.7 ms: 1.18x slower                                                        |
| create_gc_cycles           | 1.59 ms                                                      | 1.88 ms: 1.18x slower                                                        |
| go                         | 150 ms                                                       | 177 ms: 1.18x slower                                                         |
| hexiom                     | 5.96 ms                                                      | 7.33 ms: 1.23x slower                                                        |
| coverage                   | 66.7 ms                                                      | 82.9 ms: 1.24x slower                                                        |
| scimark_lu                 | 98.8 ms                                                      | 126 ms: 1.28x slower                                                         |
| python_startup_no_site     | 8.64 ms                                                      | 11.9 ms: 1.38x slower                                                        |
| gc_traversal               | 3.48 ms                                                      | 4.84 ms: 1.39x slower                                                        |
| scimark_sor                | 109 ms                                                       | 152 ms: 1.40x slower                                                         |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                                 |

Benchmark hidden because not significant (5): pickle_list, mako, float, chaos, mypy2
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240402-3.13.0a5+-ee60448-JIT/bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.88% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x