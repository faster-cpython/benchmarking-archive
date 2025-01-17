# Results vs. 3.11.0

- fork: mdboom
- ref: all_above_200
- machine: linux-x86_64
- commit hash: d42ae28
- commit date: 2024-04-03
- overall geometric mean: 1.04x faster
- HPT reliability: 58.44%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 302 ms: 1.05x slower                                                  |
| chameleon      | 7.92 ms                                                      | 7.31 ms: 1.08x faster                                                 |
| docutils       | 2.85 sec                                                     | 3.06 sec: 1.08x slower                                                |
| Geometric mean | (ref)                                                        | 1.01x slower                                                          |

Benchmark hidden because not significant (2): html5lib, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 474 ms                                                       | 339 ms: 1.40x faster                                                  |
| async_tree_memoization_tg  | 600 ms                                                       | 429 ms: 1.40x faster                                                  |
| async_tree_memoization     | 629 ms                                                       | 452 ms: 1.39x faster                                                  |
| async_tree_none            | 518 ms                                                       | 377 ms: 1.37x faster                                                  |
| async_tree_io_tg           | 1.15 sec                                                     | 879 ms: 1.31x faster                                                  |
| async_tree_io              | 1.17 sec                                                     | 906 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 592 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 602 ms: 1.25x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 94.7 ms: 1.02x slower                                                 |
| float          | 74.9 ms                                                      | 77.7 ms: 1.04x slower                                                 |
| pidigits       | 251 ms                                                       | 264 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 150 ms: 1.04x faster                                                  |
| regex_effbot   | 3.34 ms                                                      | 3.50 ms: 1.05x slower                                                 |
| regex_v8       | 24.4 ms                                                      | 25.9 ms: 1.06x slower                                                 |
| regex_dna      | 227 ms                                                       | 247 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                 |
| json_loads           | 28.9 us                                                      | 25.8 us: 1.12x faster                                                 |
| xml_etree_parse      | 155 ms                                                       | 146 ms: 1.06x faster                                                  |
| xml_etree_iterparse  | 107 ms                                                       | 104 ms: 1.03x faster                                                  |
| pickle_pure_python   | 316 us                                                       | 310 us: 1.02x faster                                                  |
| tomli_loads          | 2.25 sec                                                     | 2.21 sec: 1.02x faster                                                |
| unpickle_pure_python | 238 us                                                       | 241 us: 1.01x slower                                                  |
| pickle_dict          | 32.3 us                                                      | 33.1 us: 1.02x slower                                                 |
| xml_etree_process    | 55.9 ms                                                      | 58.9 ms: 1.05x slower                                                 |
| xml_etree_generate   | 79.7 ms                                                      | 85.5 ms: 1.07x slower                                                 |
| unpickle             | 13.3 us                                                      | 14.6 us: 1.10x slower                                                 |
| pickle               | 9.89 us                                                      | 11.1 us: 1.12x slower                                                 |
| pickle_list          | 3.94 us                                                      | 4.45 us: 1.13x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                          |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 13.6 ms: 1.26x slower                                                 |
| python_startup_no_site | 7.73 ms                                                      | 11.8 ms: 1.53x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.39x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 9.84 ms: 1.12x faster                                                 |
| django_template | 39.3 ms                                                      | 40.1 ms: 1.02x slower                                                 |
| genshi_text     | 25.5 ms                                                      | 27.7 ms: 1.09x slower                                                 |
| genshi_xml      | 57.1 ms                                                      | 62.7 ms: 1.10x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 123 us: 4.34x faster                                                  |
| asyncio_tcp                | 747 ms                                                       | 369 ms: 2.02x faster                                                  |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.95x faster                                                |
| generators                 | 54.6 ms                                                      | 34.4 ms: 1.59x faster                                                 |
| pylint                     | 514 ms                                                       | 364 ms: 1.41x faster                                                  |
| async_tree_none_tg         | 474 ms                                                       | 339 ms: 1.40x faster                                                  |
| async_tree_memoization_tg  | 600 ms                                                       | 429 ms: 1.40x faster                                                  |
| async_tree_memoization     | 629 ms                                                       | 452 ms: 1.39x faster                                                  |
| async_tree_none            | 518 ms                                                       | 377 ms: 1.37x faster                                                  |
| async_tree_io_tg           | 1.15 sec                                                     | 879 ms: 1.31x faster                                                  |
| async_tree_io              | 1.17 sec                                                     | 906 ms: 1.29x faster                                                  |
| comprehensions             | 25.1 us                                                      | 19.5 us: 1.28x faster                                                 |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 592 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 602 ms: 1.25x faster                                                  |
| json_dumps                 | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                 |
| coroutines                 | 27.8 ms                                                      | 22.5 ms: 1.24x faster                                                 |
| sympy_sum                  | 186 ms                                                       | 161 ms: 1.15x faster                                                  |
| json_loads                 | 28.9 us                                                      | 25.8 us: 1.12x faster                                                 |
| mako                       | 11.0 ms                                                      | 9.84 ms: 1.12x faster                                                 |
| sympy_str                  | 337 ms                                                       | 304 ms: 1.11x faster                                                  |
| chaos                      | 74.9 ms                                                      | 67.7 ms: 1.11x faster                                                 |
| thrift                     | 931 us                                                       | 845 us: 1.10x faster                                                  |
| chameleon                  | 7.92 ms                                                      | 7.31 ms: 1.08x faster                                                 |
| sympy_expand               | 553 ms                                                       | 512 ms: 1.08x faster                                                  |
| richards_super             | 63.6 ms                                                      | 58.9 ms: 1.08x faster                                                 |
| logging_simple             | 7.24 us                                                      | 6.73 us: 1.08x faster                                                 |
| crypto_pyaes               | 83.3 ms                                                      | 77.9 ms: 1.07x faster                                                 |
| sqlglot_parse              | 1.51 ms                                                      | 1.42 ms: 1.07x faster                                                 |
| xml_etree_parse            | 155 ms                                                       | 146 ms: 1.06x faster                                                  |
| sqlglot_transpile          | 1.91 ms                                                      | 1.81 ms: 1.06x faster                                                 |
| logging_format             | 7.71 us                                                      | 7.31 us: 1.05x faster                                                 |
| mdp                        | 2.77 sec                                                     | 2.63 sec: 1.05x faster                                                |
| deltablue                  | 3.97 ms                                                      | 3.77 ms: 1.05x faster                                                 |
| fannkuch                   | 416 ms                                                       | 396 ms: 1.05x faster                                                  |
| regex_compile              | 156 ms                                                       | 150 ms: 1.04x faster                                                  |
| logging_silent             | 100 ns                                                       | 97.3 ns: 1.03x faster                                                 |
| json                       | 5.58 ms                                                      | 5.42 ms: 1.03x faster                                                 |
| xml_etree_iterparse        | 107 ms                                                       | 104 ms: 1.03x faster                                                  |
| sympy_integrate            | 25.8 ms                                                      | 25.1 ms: 1.03x faster                                                 |
| pycparser                  | 1.31 sec                                                     | 1.28 sec: 1.02x faster                                                |
| pickle_pure_python         | 316 us                                                       | 310 us: 1.02x faster                                                  |
| dask                       | 410 ms                                                       | 403 ms: 1.02x faster                                                  |
| tomli_loads                | 2.25 sec                                                     | 2.21 sec: 1.02x faster                                                |
| unpickle_pure_python       | 238 us                                                       | 241 us: 1.01x slower                                                  |
| spectral_norm              | 95.1 ms                                                      | 96.2 ms: 1.01x slower                                                 |
| sqlglot_normalize          | 122 ms                                                       | 123 ms: 1.01x slower                                                  |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.14 ms: 1.02x slower                                                 |
| nbody                      | 92.9 ms                                                      | 94.7 ms: 1.02x slower                                                 |
| django_template            | 39.3 ms                                                      | 40.1 ms: 1.02x slower                                                 |
| pprint_pformat             | 1.67 sec                                                     | 1.70 sec: 1.02x slower                                                |
| pathlib                    | 18.9 ms                                                      | 19.3 ms: 1.02x slower                                                 |
| nqueens                    | 103 ms                                                       | 105 ms: 1.02x slower                                                  |
| pickle_dict                | 32.3 us                                                      | 33.1 us: 1.02x slower                                                 |
| meteor_contest             | 131 ms                                                       | 134 ms: 1.03x slower                                                  |
| pprint_safe_repr           | 805 ms                                                       | 828 ms: 1.03x slower                                                  |
| richards                   | 49.7 ms                                                      | 51.2 ms: 1.03x slower                                                 |
| float                      | 74.9 ms                                                      | 77.7 ms: 1.04x slower                                                 |
| dulwich_log                | 67.4 ms                                                      | 69.9 ms: 1.04x slower                                                 |
| regex_effbot               | 3.34 ms                                                      | 3.50 ms: 1.05x slower                                                 |
| pidigits                   | 251 ms                                                       | 264 ms: 1.05x slower                                                  |
| scimark_lu                 | 114 ms                                                       | 120 ms: 1.05x slower                                                  |
| 2to3                       | 287 ms                                                       | 302 ms: 1.05x slower                                                  |
| xml_etree_process          | 55.9 ms                                                      | 58.9 ms: 1.05x slower                                                 |
| scimark_monte_carlo        | 69.8 ms                                                      | 73.7 ms: 1.06x slower                                                 |
| deepcopy_memo              | 37.5 us                                                      | 39.6 us: 1.06x slower                                                 |
| bench_mp_pool              | 4.70 ms                                                      | 4.98 ms: 1.06x slower                                                 |
| regex_v8                   | 24.4 ms                                                      | 25.9 ms: 1.06x slower                                                 |
| sqlglot_optimize           | 59.0 ms                                                      | 62.9 ms: 1.07x slower                                                 |
| sqlite_synth               | 2.52 us                                                      | 2.70 us: 1.07x slower                                                 |
| xml_etree_generate         | 79.7 ms                                                      | 85.5 ms: 1.07x slower                                                 |
| docutils                   | 2.85 sec                                                     | 3.06 sec: 1.08x slower                                                |
| mypy2                      | 762 ms                                                       | 826 ms: 1.08x slower                                                  |
| regex_dna                  | 227 ms                                                       | 247 ms: 1.09x slower                                                  |
| genshi_text                | 25.5 ms                                                      | 27.7 ms: 1.09x slower                                                 |
| genshi_xml                 | 57.1 ms                                                      | 62.7 ms: 1.10x slower                                                 |
| unpickle                   | 13.3 us                                                      | 14.6 us: 1.10x slower                                                 |
| hexiom                     | 6.98 ms                                                      | 7.70 ms: 1.10x slower                                                 |
| bench_thread_pool          | 1.00 ms                                                      | 1.12 ms: 1.12x slower                                                 |
| scimark_fft                | 281 ms                                                       | 314 ms: 1.12x slower                                                  |
| pickle                     | 9.89 us                                                      | 11.1 us: 1.12x slower                                                 |
| pyflate                    | 449 ms                                                       | 506 ms: 1.13x slower                                                  |
| aiohttp                    | 986 us                                                       | 1.11 ms: 1.13x slower                                                 |
| pickle_list                | 3.94 us                                                      | 4.45 us: 1.13x slower                                                 |
| go                         | 158 ms                                                       | 178 ms: 1.13x slower                                                  |
| gunicorn                   | 966 us                                                       | 1.10 ms: 1.14x slower                                                 |
| create_gc_cycles           | 1.58 ms                                                      | 1.81 ms: 1.15x slower                                                 |
| gc_traversal               | 4.15 ms                                                      | 4.85 ms: 1.17x slower                                                 |
| telco                      | 6.81 ms                                                      | 8.19 ms: 1.20x slower                                                 |
| coverage                   | 66.1 ms                                                      | 81.6 ms: 1.23x slower                                                 |
| async_generators           | 322 ms                                                       | 398 ms: 1.24x slower                                                  |
| python_startup             | 10.7 ms                                                      | 13.6 ms: 1.26x slower                                                 |
| scimark_sor                | 110 ms                                                       | 153 ms: 1.39x slower                                                  |
| python_startup_no_site     | 7.73 ms                                                      | 11.8 ms: 1.53x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                          |

Benchmark hidden because not significant (7): tornado_http, asyncio_websockets, raytrace, unpickle_list, deepcopy, deepcopy_reduce, html5lib
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 58.44% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x