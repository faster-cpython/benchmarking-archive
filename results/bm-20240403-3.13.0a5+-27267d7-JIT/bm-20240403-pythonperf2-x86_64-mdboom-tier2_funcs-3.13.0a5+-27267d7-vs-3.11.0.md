# Results vs. 3.11.0

- fork: mdboom
- ref: tier2_funcs
- machine: linux-x86_64
- commit hash: 27267d7
- commit date: 2024-04-03
- overall geometric mean: 1.04x faster
- HPT reliability: 69.46%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 300 ms: 1.05x slower                                                |
| chameleon      | 7.92 ms                                                      | 7.44 ms: 1.07x faster                                               |
| docutils       | 2.85 sec                                                     | 3.07 sec: 1.08x slower                                              |
| html5lib       | 72.2 ms                                                      | 73.8 ms: 1.02x slower                                               |
| Geometric mean | (ref)                                                        | 1.01x slower                                                        |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none            | 518 ms                                                       | 361 ms: 1.43x faster                                                |
| async_tree_memoization     | 629 ms                                                       | 443 ms: 1.42x faster                                                |
| async_tree_none_tg         | 474 ms                                                       | 341 ms: 1.39x faster                                                |
| async_tree_memoization_tg  | 600 ms                                                       | 439 ms: 1.37x faster                                                |
| async_tree_io              | 1.17 sec                                                     | 889 ms: 1.32x faster                                                |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 579 ms: 1.30x faster                                                |
| async_tree_io_tg           | 1.15 sec                                                     | 904 ms: 1.28x faster                                                |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 598 ms: 1.26x faster                                                |
| Geometric mean             | (ref)                                                        | 1.34x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 74.9 ms                                                      | 77.6 ms: 1.04x slower                                               |
| pidigits       | 251 ms                                                       | 261 ms: 1.04x slower                                                |
| nbody          | 92.9 ms                                                      | 98.4 ms: 1.06x slower                                               |
| Geometric mean | (ref)                                                        | 1.04x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 150 ms: 1.04x faster                                                |
| regex_dna      | 227 ms                                                       | 241 ms: 1.06x slower                                                |
| regex_effbot   | 3.34 ms                                                      | 3.57 ms: 1.07x slower                                               |
| regex_v8       | 24.4 ms                                                      | 26.1 ms: 1.07x slower                                               |
| Geometric mean | (ref)                                                        | 1.04x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|---------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| json_dumps          | 13.3 ms                                                      | 10.7 ms: 1.23x faster                                               |
| json_loads          | 28.9 us                                                      | 25.2 us: 1.15x faster                                               |
| xml_etree_parse     | 155 ms                                                       | 146 ms: 1.06x faster                                                |
| tomli_loads         | 2.25 sec                                                     | 2.15 sec: 1.05x faster                                              |
| pickle_dict         | 32.3 us                                                      | 31.0 us: 1.04x faster                                               |
| pickle_pure_python  | 316 us                                                       | 306 us: 1.03x faster                                                |
| xml_etree_iterparse | 107 ms                                                       | 104 ms: 1.02x faster                                                |
| unpickle_list       | 4.60 us                                                      | 4.55 us: 1.01x faster                                               |
| xml_etree_process   | 55.9 ms                                                      | 58.2 ms: 1.04x slower                                               |
| pickle              | 9.89 us                                                      | 10.5 us: 1.06x slower                                               |
| xml_etree_generate  | 79.7 ms                                                      | 85.2 ms: 1.07x slower                                               |
| pickle_list         | 3.94 us                                                      | 4.46 us: 1.13x slower                                               |
| unpickle            | 13.3 us                                                      | 15.1 us: 1.14x slower                                               |
| Geometric mean      | (ref)                                                        | 1.01x faster                                                        |

Benchmark hidden because not significant (1): unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                               |
| python_startup_no_site | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                               |
| Geometric mean         | (ref)                                                        | 1.39x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 10.1 ms: 1.09x faster                                               |
| django_template | 39.3 ms                                                      | 40.1 ms: 1.02x slower                                               |
| genshi_xml      | 57.1 ms                                                      | 58.8 ms: 1.03x slower                                               |
| genshi_text     | 25.5 ms                                                      | 27.2 ms: 1.07x slower                                               |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-tier2_funcs-3.13.0a5+-27267d7 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 121 us: 4.38x faster                                                |
| asyncio_tcp                | 747 ms                                                       | 371 ms: 2.01x faster                                                |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                              |
| generators                 | 54.6 ms                                                      | 33.3 ms: 1.64x faster                                               |
| async_tree_none            | 518 ms                                                       | 361 ms: 1.43x faster                                                |
| async_tree_memoization     | 629 ms                                                       | 443 ms: 1.42x faster                                                |
| pylint                     | 514 ms                                                       | 366 ms: 1.41x faster                                                |
| async_tree_none_tg         | 474 ms                                                       | 341 ms: 1.39x faster                                                |
| async_tree_memoization_tg  | 600 ms                                                       | 439 ms: 1.37x faster                                                |
| async_tree_io              | 1.17 sec                                                     | 889 ms: 1.32x faster                                                |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 579 ms: 1.30x faster                                                |
| async_tree_io_tg           | 1.15 sec                                                     | 904 ms: 1.28x faster                                                |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 598 ms: 1.26x faster                                                |
| comprehensions             | 25.1 us                                                      | 20.0 us: 1.25x faster                                               |
| json_dumps                 | 13.3 ms                                                      | 10.7 ms: 1.23x faster                                               |
| coroutines                 | 27.8 ms                                                      | 22.9 ms: 1.21x faster                                               |
| json_loads                 | 28.9 us                                                      | 25.2 us: 1.15x faster                                               |
| sympy_sum                  | 186 ms                                                       | 162 ms: 1.14x faster                                                |
| chaos                      | 74.9 ms                                                      | 66.8 ms: 1.12x faster                                               |
| sympy_str                  | 337 ms                                                       | 302 ms: 1.11x faster                                                |
| fannkuch                   | 416 ms                                                       | 378 ms: 1.10x faster                                                |
| mako                       | 11.0 ms                                                      | 10.1 ms: 1.09x faster                                               |
| sympy_expand               | 553 ms                                                       | 510 ms: 1.08x faster                                                |
| sqlglot_parse              | 1.51 ms                                                      | 1.40 ms: 1.08x faster                                               |
| richards_super             | 63.6 ms                                                      | 59.4 ms: 1.07x faster                                               |
| crypto_pyaes               | 83.3 ms                                                      | 77.9 ms: 1.07x faster                                               |
| chameleon                  | 7.92 ms                                                      | 7.44 ms: 1.07x faster                                               |
| deltablue                  | 3.97 ms                                                      | 3.73 ms: 1.06x faster                                               |
| sqlglot_transpile          | 1.91 ms                                                      | 1.80 ms: 1.06x faster                                               |
| logging_simple             | 7.24 us                                                      | 6.82 us: 1.06x faster                                               |
| xml_etree_parse            | 155 ms                                                       | 146 ms: 1.06x faster                                                |
| mdp                        | 2.77 sec                                                     | 2.62 sec: 1.06x faster                                              |
| thrift                     | 931 us                                                       | 887 us: 1.05x faster                                                |
| tomli_loads                | 2.25 sec                                                     | 2.15 sec: 1.05x faster                                              |
| logging_format             | 7.71 us                                                      | 7.37 us: 1.05x faster                                               |
| pickle_dict                | 32.3 us                                                      | 31.0 us: 1.04x faster                                               |
| regex_compile              | 156 ms                                                       | 150 ms: 1.04x faster                                                |
| json                       | 5.58 ms                                                      | 5.38 ms: 1.04x faster                                               |
| pycparser                  | 1.31 sec                                                     | 1.26 sec: 1.04x faster                                              |
| logging_silent             | 100 ns                                                       | 97.2 ns: 1.03x faster                                               |
| pickle_pure_python         | 316 us                                                       | 306 us: 1.03x faster                                                |
| raytrace                   | 309 ms                                                       | 302 ms: 1.03x faster                                                |
| xml_etree_iterparse        | 107 ms                                                       | 104 ms: 1.02x faster                                                |
| sympy_integrate            | 25.8 ms                                                      | 25.3 ms: 1.02x faster                                               |
| dask                       | 410 ms                                                       | 403 ms: 1.02x faster                                                |
| unpickle_list              | 4.60 us                                                      | 4.55 us: 1.01x faster                                               |
| deepcopy                   | 391 us                                                       | 388 us: 1.01x faster                                                |
| deepcopy_reduce            | 3.40 us                                                      | 3.37 us: 1.01x faster                                               |
| spectral_norm              | 95.1 ms                                                      | 95.7 ms: 1.01x slower                                               |
| sqlglot_normalize          | 122 ms                                                       | 123 ms: 1.01x slower                                                |
| meteor_contest             | 131 ms                                                       | 132 ms: 1.01x slower                                                |
| nqueens                    | 103 ms                                                       | 104 ms: 1.02x slower                                                |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.13 ms: 1.02x slower                                               |
| django_template            | 39.3 ms                                                      | 40.1 ms: 1.02x slower                                               |
| html5lib                   | 72.2 ms                                                      | 73.8 ms: 1.02x slower                                               |
| deepcopy_memo              | 37.5 us                                                      | 38.5 us: 1.02x slower                                               |
| dulwich_log                | 67.4 ms                                                      | 69.2 ms: 1.03x slower                                               |
| pprint_safe_repr           | 805 ms                                                       | 827 ms: 1.03x slower                                                |
| genshi_xml                 | 57.1 ms                                                      | 58.8 ms: 1.03x slower                                               |
| float                      | 74.9 ms                                                      | 77.6 ms: 1.04x slower                                               |
| pprint_pformat             | 1.67 sec                                                     | 1.73 sec: 1.04x slower                                              |
| pidigits                   | 251 ms                                                       | 261 ms: 1.04x slower                                                |
| xml_etree_process          | 55.9 ms                                                      | 58.2 ms: 1.04x slower                                               |
| pathlib                    | 18.9 ms                                                      | 19.8 ms: 1.04x slower                                               |
| 2to3                       | 287 ms                                                       | 300 ms: 1.05x slower                                                |
| nbody                      | 92.9 ms                                                      | 98.4 ms: 1.06x slower                                               |
| regex_dna                  | 227 ms                                                       | 241 ms: 1.06x slower                                                |
| sqlglot_optimize           | 59.0 ms                                                      | 62.6 ms: 1.06x slower                                               |
| sqlite_synth               | 2.52 us                                                      | 2.69 us: 1.06x slower                                               |
| pickle                     | 9.89 us                                                      | 10.5 us: 1.06x slower                                               |
| scimark_monte_carlo        | 69.8 ms                                                      | 74.4 ms: 1.07x slower                                               |
| richards                   | 49.7 ms                                                      | 52.9 ms: 1.07x slower                                               |
| genshi_text                | 25.5 ms                                                      | 27.2 ms: 1.07x slower                                               |
| regex_effbot               | 3.34 ms                                                      | 3.57 ms: 1.07x slower                                               |
| xml_etree_generate         | 79.7 ms                                                      | 85.2 ms: 1.07x slower                                               |
| regex_v8                   | 24.4 ms                                                      | 26.1 ms: 1.07x slower                                               |
| bench_mp_pool              | 4.70 ms                                                      | 5.04 ms: 1.07x slower                                               |
| docutils                   | 2.85 sec                                                     | 3.07 sec: 1.08x slower                                              |
| hexiom                     | 6.98 ms                                                      | 7.56 ms: 1.08x slower                                               |
| mypy2                      | 762 ms                                                       | 826 ms: 1.08x slower                                                |
| scimark_lu                 | 114 ms                                                       | 125 ms: 1.10x slower                                                |
| go                         | 158 ms                                                       | 174 ms: 1.10x slower                                                |
| pyflate                    | 449 ms                                                       | 502 ms: 1.12x slower                                                |
| bench_thread_pool          | 1.00 ms                                                      | 1.12 ms: 1.12x slower                                               |
| scimark_fft                | 281 ms                                                       | 316 ms: 1.13x slower                                                |
| gunicorn                   | 966 us                                                       | 1.09 ms: 1.13x slower                                               |
| pickle_list                | 3.94 us                                                      | 4.46 us: 1.13x slower                                               |
| unpickle                   | 13.3 us                                                      | 15.1 us: 1.14x slower                                               |
| aiohttp                    | 986 us                                                       | 1.13 ms: 1.14x slower                                               |
| create_gc_cycles           | 1.58 ms                                                      | 1.82 ms: 1.16x slower                                               |
| gc_traversal               | 4.15 ms                                                      | 4.80 ms: 1.16x slower                                               |
| telco                      | 6.81 ms                                                      | 8.18 ms: 1.20x slower                                               |
| async_generators           | 322 ms                                                       | 391 ms: 1.22x slower                                                |
| python_startup             | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                               |
| coverage                   | 66.1 ms                                                      | 83.6 ms: 1.26x slower                                               |
| scimark_sor                | 110 ms                                                       | 155 ms: 1.41x slower                                                |
| python_startup_no_site     | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                               |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                        |

Benchmark hidden because not significant (3): tornado_http, asyncio_websockets, unpickle_pure_python
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 69.46% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x