# Results vs. 3.11.0

- fork: brandtbucher
- ref: stitch_exhausted
- machine: linux-x86_64
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.03x faster
- HPT reliability: 55.59%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 306 ms: 1.07x slower                                                           |
| chameleon      | 7.92 ms                                                      | 7.57 ms: 1.05x faster                                                          |
| docutils       | 2.85 sec                                                     | 3.13 sec: 1.10x slower                                                         |
| html5lib       | 72.2 ms                                                      | 74.3 ms: 1.03x slower                                                          |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                   |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none            | 518 ms                                                       | 362 ms: 1.43x faster                                                           |
| async_tree_memoization     | 629 ms                                                       | 445 ms: 1.41x faster                                                           |
| async_tree_none_tg         | 474 ms                                                       | 340 ms: 1.40x faster                                                           |
| async_tree_memoization_tg  | 600 ms                                                       | 437 ms: 1.37x faster                                                           |
| async_tree_io              | 1.17 sec                                                     | 891 ms: 1.31x faster                                                           |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 579 ms: 1.29x faster                                                           |
| async_tree_io_tg           | 1.15 sec                                                     | 910 ms: 1.27x faster                                                           |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 601 ms: 1.25x faster                                                           |
| Geometric mean             | (ref)                                                        | 1.34x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 261 ms: 1.04x slower                                                           |
| nbody          | 92.9 ms                                                      | 96.8 ms: 1.04x slower                                                          |
| float          | 74.9 ms                                                      | 79.0 ms: 1.05x slower                                                          |
| Geometric mean | (ref)                                                        | 1.05x slower                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 146 ms: 1.07x faster                                                           |
| regex_v8       | 24.4 ms                                                      | 25.7 ms: 1.05x slower                                                          |
| regex_dna      | 227 ms                                                       | 240 ms: 1.06x slower                                                           |
| regex_effbot   | 3.34 ms                                                      | 3.60 ms: 1.08x slower                                                          |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.7 ms: 1.23x faster                                                          |
| json_loads           | 28.9 us                                                      | 25.4 us: 1.14x faster                                                          |
| xml_etree_parse      | 155 ms                                                       | 142 ms: 1.09x faster                                                           |
| xml_etree_iterparse  | 107 ms                                                       | 102 ms: 1.05x faster                                                           |
| tomli_loads          | 2.25 sec                                                     | 2.16 sec: 1.04x faster                                                         |
| unpickle_pure_python | 238 us                                                       | 230 us: 1.04x faster                                                           |
| pickle_pure_python   | 316 us                                                       | 308 us: 1.03x faster                                                           |
| pickle_dict          | 32.3 us                                                      | 33.0 us: 1.02x slower                                                          |
| xml_etree_generate   | 79.7 ms                                                      | 82.7 ms: 1.04x slower                                                          |
| xml_etree_process    | 55.9 ms                                                      | 58.2 ms: 1.04x slower                                                          |
| pickle               | 9.89 us                                                      | 11.0 us: 1.12x slower                                                          |
| unpickle             | 13.3 us                                                      | 15.1 us: 1.14x slower                                                          |
| pickle_list          | 3.94 us                                                      | 4.50 us: 1.14x slower                                                          |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                                   |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                                          |
| python_startup_no_site | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                                          |
| Geometric mean         | (ref)                                                        | 1.39x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 9.90 ms: 1.11x faster                                                          |
| django_template | 39.3 ms                                                      | 40.9 ms: 1.04x slower                                                          |
| genshi_xml      | 57.1 ms                                                      | 59.9 ms: 1.05x slower                                                          |
| genshi_text     | 25.5 ms                                                      | 28.0 ms: 1.10x slower                                                          |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 123 us: 4.34x faster                                                           |
| asyncio_tcp                | 747 ms                                                       | 375 ms: 1.99x faster                                                           |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                         |
| generators                 | 54.6 ms                                                      | 33.5 ms: 1.63x faster                                                          |
| pylint                     | 514 ms                                                       | 345 ms: 1.49x faster                                                           |
| async_tree_none            | 518 ms                                                       | 362 ms: 1.43x faster                                                           |
| async_tree_memoization     | 629 ms                                                       | 445 ms: 1.41x faster                                                           |
| async_tree_none_tg         | 474 ms                                                       | 340 ms: 1.40x faster                                                           |
| async_tree_memoization_tg  | 600 ms                                                       | 437 ms: 1.37x faster                                                           |
| async_tree_io              | 1.17 sec                                                     | 891 ms: 1.31x faster                                                           |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 579 ms: 1.29x faster                                                           |
| async_tree_io_tg           | 1.15 sec                                                     | 910 ms: 1.27x faster                                                           |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 601 ms: 1.25x faster                                                           |
| coroutines                 | 27.8 ms                                                      | 22.2 ms: 1.25x faster                                                          |
| comprehensions             | 25.1 us                                                      | 20.2 us: 1.24x faster                                                          |
| json_dumps                 | 13.3 ms                                                      | 10.7 ms: 1.23x faster                                                          |
| json_loads                 | 28.9 us                                                      | 25.4 us: 1.14x faster                                                          |
| sympy_sum                  | 186 ms                                                       | 165 ms: 1.13x faster                                                           |
| mako                       | 11.0 ms                                                      | 9.90 ms: 1.11x faster                                                          |
| richards_super             | 63.6 ms                                                      | 57.6 ms: 1.10x faster                                                          |
| logging_simple             | 7.24 us                                                      | 6.63 us: 1.09x faster                                                          |
| sympy_str                  | 337 ms                                                       | 310 ms: 1.09x faster                                                           |
| xml_etree_parse            | 155 ms                                                       | 142 ms: 1.09x faster                                                           |
| chaos                      | 74.9 ms                                                      | 69.0 ms: 1.09x faster                                                          |
| fannkuch                   | 416 ms                                                       | 383 ms: 1.09x faster                                                           |
| regex_compile              | 156 ms                                                       | 146 ms: 1.07x faster                                                           |
| thrift                     | 931 us                                                       | 878 us: 1.06x faster                                                           |
| sqlglot_parse              | 1.51 ms                                                      | 1.43 ms: 1.06x faster                                                          |
| logging_format             | 7.71 us                                                      | 7.32 us: 1.05x faster                                                          |
| crypto_pyaes               | 83.3 ms                                                      | 79.1 ms: 1.05x faster                                                          |
| sympy_expand               | 553 ms                                                       | 526 ms: 1.05x faster                                                           |
| xml_etree_iterparse        | 107 ms                                                       | 102 ms: 1.05x faster                                                           |
| chameleon                  | 7.92 ms                                                      | 7.57 ms: 1.05x faster                                                          |
| deltablue                  | 3.97 ms                                                      | 3.79 ms: 1.05x faster                                                          |
| mdp                        | 2.77 sec                                                     | 2.65 sec: 1.05x faster                                                         |
| sqlglot_transpile          | 1.91 ms                                                      | 1.84 ms: 1.04x faster                                                          |
| tomli_loads                | 2.25 sec                                                     | 2.16 sec: 1.04x faster                                                         |
| unpickle_pure_python       | 238 us                                                       | 230 us: 1.04x faster                                                           |
| logging_silent             | 100 ns                                                       | 97.7 ns: 1.03x faster                                                          |
| pickle_pure_python         | 316 us                                                       | 308 us: 1.03x faster                                                           |
| asyncio_websockets         | 390 ms                                                       | 384 ms: 1.02x faster                                                           |
| json                       | 5.58 ms                                                      | 5.51 ms: 1.01x faster                                                          |
| spectral_norm              | 95.1 ms                                                      | 94.0 ms: 1.01x faster                                                          |
| pycparser                  | 1.31 sec                                                     | 1.29 sec: 1.01x faster                                                         |
| sympy_integrate            | 25.8 ms                                                      | 26.1 ms: 1.01x slower                                                          |
| richards                   | 49.7 ms                                                      | 50.5 ms: 1.02x slower                                                          |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.14 ms: 1.02x slower                                                          |
| raytrace                   | 309 ms                                                       | 316 ms: 1.02x slower                                                           |
| pickle_dict                | 32.3 us                                                      | 33.0 us: 1.02x slower                                                          |
| deepcopy_memo              | 37.5 us                                                      | 38.4 us: 1.02x slower                                                          |
| dulwich_log                | 67.4 ms                                                      | 68.9 ms: 1.02x slower                                                          |
| deepcopy                   | 391 us                                                       | 401 us: 1.03x slower                                                           |
| html5lib                   | 72.2 ms                                                      | 74.3 ms: 1.03x slower                                                          |
| meteor_contest             | 131 ms                                                       | 135 ms: 1.03x slower                                                           |
| nqueens                    | 103 ms                                                       | 106 ms: 1.03x slower                                                           |
| pprint_pformat             | 1.67 sec                                                     | 1.73 sec: 1.04x slower                                                         |
| deepcopy_reduce            | 3.40 us                                                      | 3.52 us: 1.04x slower                                                          |
| xml_etree_generate         | 79.7 ms                                                      | 82.7 ms: 1.04x slower                                                          |
| pprint_safe_repr           | 805 ms                                                       | 836 ms: 1.04x slower                                                           |
| pidigits                   | 251 ms                                                       | 261 ms: 1.04x slower                                                           |
| django_template            | 39.3 ms                                                      | 40.9 ms: 1.04x slower                                                          |
| nbody                      | 92.9 ms                                                      | 96.8 ms: 1.04x slower                                                          |
| xml_etree_process          | 55.9 ms                                                      | 58.2 ms: 1.04x slower                                                          |
| sqlglot_normalize          | 122 ms                                                       | 127 ms: 1.04x slower                                                           |
| pathlib                    | 18.9 ms                                                      | 19.8 ms: 1.05x slower                                                          |
| scimark_lu                 | 114 ms                                                       | 119 ms: 1.05x slower                                                           |
| genshi_xml                 | 57.1 ms                                                      | 59.9 ms: 1.05x slower                                                          |
| gc_traversal               | 4.15 ms                                                      | 4.35 ms: 1.05x slower                                                          |
| regex_v8                   | 24.4 ms                                                      | 25.7 ms: 1.05x slower                                                          |
| float                      | 74.9 ms                                                      | 79.0 ms: 1.05x slower                                                          |
| regex_dna                  | 227 ms                                                       | 240 ms: 1.06x slower                                                           |
| 2to3                       | 287 ms                                                       | 306 ms: 1.07x slower                                                           |
| bench_mp_pool              | 4.70 ms                                                      | 5.01 ms: 1.07x slower                                                          |
| sqlite_synth               | 2.52 us                                                      | 2.70 us: 1.07x slower                                                          |
| regex_effbot               | 3.34 ms                                                      | 3.60 ms: 1.08x slower                                                          |
| scimark_monte_carlo        | 69.8 ms                                                      | 75.9 ms: 1.09x slower                                                          |
| sqlglot_optimize           | 59.0 ms                                                      | 64.7 ms: 1.10x slower                                                          |
| docutils                   | 2.85 sec                                                     | 3.13 sec: 1.10x slower                                                         |
| genshi_text                | 25.5 ms                                                      | 28.0 ms: 1.10x slower                                                          |
| hexiom                     | 6.98 ms                                                      | 7.73 ms: 1.11x slower                                                          |
| pickle                     | 9.89 us                                                      | 11.0 us: 1.12x slower                                                          |
| mypy2                      | 762 ms                                                       | 852 ms: 1.12x slower                                                           |
| go                         | 158 ms                                                       | 177 ms: 1.12x slower                                                           |
| scimark_fft                | 281 ms                                                       | 317 ms: 1.13x slower                                                           |
| bench_thread_pool          | 1.00 ms                                                      | 1.13 ms: 1.13x slower                                                          |
| unpickle                   | 13.3 us                                                      | 15.1 us: 1.14x slower                                                          |
| pickle_list                | 3.94 us                                                      | 4.50 us: 1.14x slower                                                          |
| create_gc_cycles           | 1.58 ms                                                      | 1.81 ms: 1.15x slower                                                          |
| gunicorn                   | 966 us                                                       | 1.12 ms: 1.16x slower                                                          |
| aiohttp                    | 986 us                                                       | 1.15 ms: 1.16x slower                                                          |
| pyflate                    | 449 ms                                                       | 528 ms: 1.17x slower                                                           |
| telco                      | 6.81 ms                                                      | 8.11 ms: 1.19x slower                                                          |
| async_generators           | 322 ms                                                       | 393 ms: 1.22x slower                                                           |
| python_startup             | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                                          |
| coverage                   | 66.1 ms                                                      | 84.3 ms: 1.27x slower                                                          |
| unpack_sequence            | 45.7 ns                                                      | 59.5 ns: 1.30x slower                                                          |
| scimark_sor                | 110 ms                                                       | 156 ms: 1.42x slower                                                           |
| python_startup_no_site     | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                                          |
| Geometric mean             | (ref)                                                        | 1.03x faster                                                                   |

Benchmark hidden because not significant (3): dask, tornado_http, unpickle_list
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 55.59% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.11x