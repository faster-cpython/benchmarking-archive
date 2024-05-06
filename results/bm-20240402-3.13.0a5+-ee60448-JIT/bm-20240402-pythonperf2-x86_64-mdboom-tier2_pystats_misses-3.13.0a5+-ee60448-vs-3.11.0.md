# Results vs. 3.11.0

- fork: mdboom
- ref: tier2_pystats_misses
- machine: linux-x86_64
- commit hash: ee60448
- commit date: 2024-04-02
- overall geometric mean: 1.04x faster
- HPT reliability: 71.41%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 300 ms: 1.05x slower                                                         |
| chameleon      | 7.92 ms                                                      | 7.54 ms: 1.05x faster                                                        |
| docutils       | 2.85 sec                                                     | 3.11 sec: 1.09x slower                                                       |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                 |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization     | 629 ms                                                       | 440 ms: 1.43x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 333 ms: 1.42x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 423 ms: 1.42x faster                                                         |
| async_tree_none            | 518 ms                                                       | 377 ms: 1.37x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 858 ms: 1.36x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 858 ms: 1.35x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 588 ms: 1.28x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 602 ms: 1.25x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.36x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 74.9 ms                                                      | 76.6 ms: 1.02x slower                                                        |
| nbody          | 92.9 ms                                                      | 95.6 ms: 1.03x slower                                                        |
| pidigits       | 251 ms                                                       | 261 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 150 ms: 1.04x faster                                                         |
| regex_effbot   | 3.34 ms                                                      | 3.51 ms: 1.05x slower                                                        |
| regex_v8       | 24.4 ms                                                      | 25.9 ms: 1.06x slower                                                        |
| regex_dna      | 227 ms                                                       | 249 ms: 1.09x slower                                                         |
| Geometric mean | (ref)                                                        | 1.04x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.5 ms: 1.26x faster                                                        |
| json_loads           | 28.9 us                                                      | 25.4 us: 1.14x faster                                                        |
| xml_etree_parse      | 155 ms                                                       | 145 ms: 1.07x faster                                                         |
| tomli_loads          | 2.25 sec                                                     | 2.13 sec: 1.06x faster                                                       |
| xml_etree_iterparse  | 107 ms                                                       | 102 ms: 1.05x faster                                                         |
| unpickle_pure_python | 238 us                                                       | 232 us: 1.03x faster                                                         |
| pickle_pure_python   | 316 us                                                       | 311 us: 1.02x faster                                                         |
| pickle_dict          | 32.3 us                                                      | 32.8 us: 1.01x slower                                                        |
| unpickle_list        | 4.60 us                                                      | 4.69 us: 1.02x slower                                                        |
| xml_etree_process    | 55.9 ms                                                      | 58.8 ms: 1.05x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 84.9 ms: 1.07x slower                                                        |
| pickle               | 9.89 us                                                      | 10.7 us: 1.08x slower                                                        |
| unpickle             | 13.3 us                                                      | 14.5 us: 1.10x slower                                                        |
| pickle_list          | 3.94 us                                                      | 4.40 us: 1.12x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 13.7 ms: 1.27x slower                                                        |
| python_startup_no_site | 7.73 ms                                                      | 11.9 ms: 1.54x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.40x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 11.0 ms                                                      | 9.96 ms: 1.11x faster                                                        |
| genshi_xml     | 57.1 ms                                                      | 61.8 ms: 1.08x slower                                                        |
| genshi_text    | 25.5 ms                                                      | 28.5 ms: 1.12x slower                                                        |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-mdboom-tier2_pystats_misses-3.13.0a5+-ee60448 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 124 us: 4.30x faster                                                         |
| asyncio_tcp                | 747 ms                                                       | 376 ms: 1.99x faster                                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                       |
| generators                 | 54.6 ms                                                      | 33.2 ms: 1.64x faster                                                        |
| pylint                     | 514 ms                                                       | 340 ms: 1.51x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 440 ms: 1.43x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 333 ms: 1.42x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 423 ms: 1.42x faster                                                         |
| async_tree_none            | 518 ms                                                       | 377 ms: 1.37x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 858 ms: 1.36x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 858 ms: 1.35x faster                                                         |
| comprehensions             | 25.1 us                                                      | 19.2 us: 1.30x faster                                                        |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 588 ms: 1.28x faster                                                         |
| json_dumps                 | 13.3 ms                                                      | 10.5 ms: 1.26x faster                                                        |
| coroutines                 | 27.8 ms                                                      | 22.1 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 602 ms: 1.25x faster                                                         |
| chaos                      | 74.9 ms                                                      | 64.1 ms: 1.17x faster                                                        |
| json_loads                 | 28.9 us                                                      | 25.4 us: 1.14x faster                                                        |
| logging_simple             | 7.24 us                                                      | 6.43 us: 1.13x faster                                                        |
| sympy_sum                  | 186 ms                                                       | 167 ms: 1.11x faster                                                         |
| deltablue                  | 3.97 ms                                                      | 3.58 ms: 1.11x faster                                                        |
| mako                       | 11.0 ms                                                      | 9.96 ms: 1.11x faster                                                        |
| richards_super             | 63.6 ms                                                      | 58.3 ms: 1.09x faster                                                        |
| logging_format             | 7.71 us                                                      | 7.10 us: 1.09x faster                                                        |
| crypto_pyaes               | 83.3 ms                                                      | 76.9 ms: 1.08x faster                                                        |
| sympy_str                  | 337 ms                                                       | 312 ms: 1.08x faster                                                         |
| raytrace                   | 309 ms                                                       | 287 ms: 1.08x faster                                                         |
| fannkuch                   | 416 ms                                                       | 386 ms: 1.08x faster                                                         |
| thrift                     | 931 us                                                       | 871 us: 1.07x faster                                                         |
| xml_etree_parse            | 155 ms                                                       | 145 ms: 1.07x faster                                                         |
| sympy_expand               | 553 ms                                                       | 518 ms: 1.07x faster                                                         |
| mdp                        | 2.77 sec                                                     | 2.60 sec: 1.06x faster                                                       |
| sqlglot_parse              | 1.51 ms                                                      | 1.43 ms: 1.06x faster                                                        |
| tomli_loads                | 2.25 sec                                                     | 2.13 sec: 1.06x faster                                                       |
| chameleon                  | 7.92 ms                                                      | 7.54 ms: 1.05x faster                                                        |
| logging_silent             | 100 ns                                                       | 95.7 ns: 1.05x faster                                                        |
| xml_etree_iterparse        | 107 ms                                                       | 102 ms: 1.05x faster                                                         |
| regex_compile              | 156 ms                                                       | 150 ms: 1.04x faster                                                         |
| sqlglot_transpile          | 1.91 ms                                                      | 1.84 ms: 1.04x faster                                                        |
| unpickle_pure_python       | 238 us                                                       | 232 us: 1.03x faster                                                         |
| spectral_norm              | 95.1 ms                                                      | 92.6 ms: 1.03x faster                                                        |
| pycparser                  | 1.31 sec                                                     | 1.28 sec: 1.02x faster                                                       |
| json                       | 5.58 ms                                                      | 5.48 ms: 1.02x faster                                                        |
| pickle_pure_python         | 316 us                                                       | 311 us: 1.02x faster                                                         |
| dask                       | 410 ms                                                       | 405 ms: 1.01x faster                                                         |
| sympy_integrate            | 25.8 ms                                                      | 25.9 ms: 1.00x slower                                                        |
| scimark_monte_carlo        | 69.8 ms                                                      | 70.6 ms: 1.01x slower                                                        |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.11 ms: 1.01x slower                                                        |
| deepcopy                   | 391 us                                                       | 395 us: 1.01x slower                                                         |
| asyncio_websockets         | 390 ms                                                       | 395 ms: 1.01x slower                                                         |
| pickle_dict                | 32.3 us                                                      | 32.8 us: 1.01x slower                                                        |
| richards                   | 49.7 ms                                                      | 50.6 ms: 1.02x slower                                                        |
| unpickle_list              | 4.60 us                                                      | 4.69 us: 1.02x slower                                                        |
| float                      | 74.9 ms                                                      | 76.6 ms: 1.02x slower                                                        |
| nqueens                    | 103 ms                                                       | 105 ms: 1.02x slower                                                         |
| nbody                      | 92.9 ms                                                      | 95.6 ms: 1.03x slower                                                        |
| meteor_contest             | 131 ms                                                       | 134 ms: 1.03x slower                                                         |
| deepcopy_reduce            | 3.40 us                                                      | 3.51 us: 1.03x slower                                                        |
| pathlib                    | 18.9 ms                                                      | 19.7 ms: 1.04x slower                                                        |
| pidigits                   | 251 ms                                                       | 261 ms: 1.04x slower                                                         |
| 2to3                       | 287 ms                                                       | 300 ms: 1.05x slower                                                         |
| deepcopy_memo              | 37.5 us                                                      | 39.4 us: 1.05x slower                                                        |
| regex_effbot               | 3.34 ms                                                      | 3.51 ms: 1.05x slower                                                        |
| hexiom                     | 6.98 ms                                                      | 7.33 ms: 1.05x slower                                                        |
| xml_etree_process          | 55.9 ms                                                      | 58.8 ms: 1.05x slower                                                        |
| pprint_pformat             | 1.67 sec                                                     | 1.76 sec: 1.06x slower                                                       |
| sqlglot_optimize           | 59.0 ms                                                      | 62.4 ms: 1.06x slower                                                        |
| pprint_safe_repr           | 805 ms                                                       | 852 ms: 1.06x slower                                                         |
| regex_v8                   | 24.4 ms                                                      | 25.9 ms: 1.06x slower                                                        |
| sqlite_synth               | 2.52 us                                                      | 2.68 us: 1.06x slower                                                        |
| dulwich_log                | 67.4 ms                                                      | 71.7 ms: 1.06x slower                                                        |
| xml_etree_generate         | 79.7 ms                                                      | 84.9 ms: 1.07x slower                                                        |
| pyflate                    | 449 ms                                                       | 485 ms: 1.08x slower                                                         |
| pickle                     | 9.89 us                                                      | 10.7 us: 1.08x slower                                                        |
| genshi_xml                 | 57.1 ms                                                      | 61.8 ms: 1.08x slower                                                        |
| docutils                   | 2.85 sec                                                     | 3.11 sec: 1.09x slower                                                       |
| regex_dna                  | 227 ms                                                       | 249 ms: 1.09x slower                                                         |
| mypy2                      | 762 ms                                                       | 834 ms: 1.10x slower                                                         |
| unpickle                   | 13.3 us                                                      | 14.5 us: 1.10x slower                                                        |
| bench_mp_pool              | 4.70 ms                                                      | 5.17 ms: 1.10x slower                                                        |
| scimark_lu                 | 114 ms                                                       | 126 ms: 1.11x slower                                                         |
| bench_thread_pool          | 1.00 ms                                                      | 1.11 ms: 1.11x slower                                                        |
| scimark_fft                | 281 ms                                                       | 313 ms: 1.12x slower                                                         |
| pickle_list                | 3.94 us                                                      | 4.40 us: 1.12x slower                                                        |
| genshi_text                | 25.5 ms                                                      | 28.5 ms: 1.12x slower                                                        |
| go                         | 158 ms                                                       | 177 ms: 1.12x slower                                                         |
| aiohttp                    | 986 us                                                       | 1.14 ms: 1.16x slower                                                        |
| gunicorn                   | 966 us                                                       | 1.12 ms: 1.16x slower                                                        |
| gc_traversal               | 4.15 ms                                                      | 4.84 ms: 1.17x slower                                                        |
| telco                      | 6.81 ms                                                      | 8.01 ms: 1.18x slower                                                        |
| create_gc_cycles           | 1.58 ms                                                      | 1.88 ms: 1.19x slower                                                        |
| async_generators           | 322 ms                                                       | 393 ms: 1.22x slower                                                         |
| coverage                   | 66.1 ms                                                      | 82.9 ms: 1.25x slower                                                        |
| python_startup             | 10.7 ms                                                      | 13.7 ms: 1.27x slower                                                        |
| scimark_sor                | 110 ms                                                       | 152 ms: 1.39x slower                                                         |
| python_startup_no_site     | 7.73 ms                                                      | 11.9 ms: 1.54x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                                 |

Benchmark hidden because not significant (3): sqlglot_normalize, tornado_http, html5lib
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 71.41% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x