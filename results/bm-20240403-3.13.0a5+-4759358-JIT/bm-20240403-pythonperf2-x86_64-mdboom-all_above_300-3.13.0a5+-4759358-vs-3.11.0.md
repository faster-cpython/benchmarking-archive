# Results vs. 3.11.0

- fork: mdboom
- ref: all_above_300
- machine: linux-x86_64
- commit hash: 4759358
- commit date: 2024-04-03
- overall geometric mean: 1.04x faster
- HPT reliability: 62.80%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 301 ms: 1.05x slower                                                  |
| chameleon      | 7.92 ms                                                      | 7.23 ms: 1.10x faster                                                 |
| docutils       | 2.85 sec                                                     | 3.05 sec: 1.07x slower                                                |
| html5lib       | 72.2 ms                                                      | 73.5 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                        | 1.01x slower                                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 432 ms: 1.39x faster                                                  |
| async_tree_none_tg         | 474 ms                                                       | 343 ms: 1.38x faster                                                  |
| async_tree_memoization     | 629 ms                                                       | 455 ms: 1.38x faster                                                  |
| async_tree_none            | 518 ms                                                       | 380 ms: 1.36x faster                                                  |
| async_tree_io_tg           | 1.15 sec                                                     | 886 ms: 1.30x faster                                                  |
| async_tree_io              | 1.17 sec                                                     | 909 ms: 1.29x faster                                                  |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 593 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 600 ms: 1.25x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 95.4 ms: 1.03x slower                                                 |
| pidigits       | 251 ms                                                       | 261 ms: 1.04x slower                                                  |
| float          | 74.9 ms                                                      | 79.5 ms: 1.06x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 149 ms: 1.05x faster                                                  |
| regex_effbot   | 3.34 ms                                                      | 3.50 ms: 1.05x slower                                                 |
| regex_v8       | 24.4 ms                                                      | 25.9 ms: 1.06x slower                                                 |
| regex_dna      | 227 ms                                                       | 246 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.8 ms: 1.23x faster                                                 |
| json_loads           | 28.9 us                                                      | 25.3 us: 1.15x faster                                                 |
| xml_etree_parse      | 155 ms                                                       | 142 ms: 1.09x faster                                                  |
| xml_etree_iterparse  | 107 ms                                                       | 102 ms: 1.05x faster                                                  |
| pickle_pure_python   | 316 us                                                       | 308 us: 1.03x faster                                                  |
| tomli_loads          | 2.25 sec                                                     | 2.21 sec: 1.02x faster                                                |
| unpickle_pure_python | 238 us                                                       | 241 us: 1.01x slower                                                  |
| pickle_dict          | 32.3 us                                                      | 32.7 us: 1.01x slower                                                 |
| unpickle_list        | 4.60 us                                                      | 4.71 us: 1.02x slower                                                 |
| xml_etree_process    | 55.9 ms                                                      | 58.0 ms: 1.04x slower                                                 |
| xml_etree_generate   | 79.7 ms                                                      | 84.3 ms: 1.06x slower                                                 |
| pickle               | 9.89 us                                                      | 10.8 us: 1.09x slower                                                 |
| pickle_list          | 3.94 us                                                      | 4.38 us: 1.11x slower                                                 |
| unpickle             | 13.3 us                                                      | 14.9 us: 1.13x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                                 |
| python_startup_no_site | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 9.92 ms: 1.11x faster                                                 |
| django_template | 39.3 ms                                                      | 40.2 ms: 1.02x slower                                                 |
| genshi_text     | 25.5 ms                                                      | 26.7 ms: 1.05x slower                                                 |
| genshi_xml      | 57.1 ms                                                      | 60.3 ms: 1.06x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 120 us: 4.45x faster                                                  |
| asyncio_tcp                | 747 ms                                                       | 370 ms: 2.02x faster                                                  |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                |
| generators                 | 54.6 ms                                                      | 33.4 ms: 1.63x faster                                                 |
| pylint                     | 514 ms                                                       | 365 ms: 1.41x faster                                                  |
| async_tree_memoization_tg  | 600 ms                                                       | 432 ms: 1.39x faster                                                  |
| async_tree_none_tg         | 474 ms                                                       | 343 ms: 1.38x faster                                                  |
| async_tree_memoization     | 629 ms                                                       | 455 ms: 1.38x faster                                                  |
| async_tree_none            | 518 ms                                                       | 380 ms: 1.36x faster                                                  |
| async_tree_io_tg           | 1.15 sec                                                     | 886 ms: 1.30x faster                                                  |
| async_tree_io              | 1.17 sec                                                     | 909 ms: 1.29x faster                                                  |
| comprehensions             | 25.1 us                                                      | 19.8 us: 1.27x faster                                                 |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 593 ms: 1.27x faster                                                  |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 600 ms: 1.25x faster                                                  |
| coroutines                 | 27.8 ms                                                      | 22.6 ms: 1.23x faster                                                 |
| json_dumps                 | 13.3 ms                                                      | 10.8 ms: 1.23x faster                                                 |
| json_loads                 | 28.9 us                                                      | 25.3 us: 1.15x faster                                                 |
| sympy_sum                  | 186 ms                                                       | 163 ms: 1.14x faster                                                  |
| mako                       | 11.0 ms                                                      | 9.92 ms: 1.11x faster                                                 |
| chaos                      | 74.9 ms                                                      | 67.9 ms: 1.10x faster                                                 |
| sympy_str                  | 337 ms                                                       | 305 ms: 1.10x faster                                                  |
| chameleon                  | 7.92 ms                                                      | 7.23 ms: 1.10x faster                                                 |
| richards_super             | 63.6 ms                                                      | 58.3 ms: 1.09x faster                                                 |
| xml_etree_parse            | 155 ms                                                       | 142 ms: 1.09x faster                                                  |
| logging_simple             | 7.24 us                                                      | 6.66 us: 1.09x faster                                                 |
| sympy_expand               | 553 ms                                                       | 513 ms: 1.08x faster                                                  |
| logging_format             | 7.71 us                                                      | 7.15 us: 1.08x faster                                                 |
| crypto_pyaes               | 83.3 ms                                                      | 78.7 ms: 1.06x faster                                                 |
| mdp                        | 2.77 sec                                                     | 2.62 sec: 1.06x faster                                                |
| sqlglot_parse              | 1.51 ms                                                      | 1.43 ms: 1.06x faster                                                 |
| fannkuch                   | 416 ms                                                       | 393 ms: 1.06x faster                                                  |
| deltablue                  | 3.97 ms                                                      | 3.76 ms: 1.05x faster                                                 |
| xml_etree_iterparse        | 107 ms                                                       | 102 ms: 1.05x faster                                                  |
| regex_compile              | 156 ms                                                       | 149 ms: 1.05x faster                                                  |
| sqlglot_transpile          | 1.91 ms                                                      | 1.83 ms: 1.05x faster                                                 |
| thrift                     | 931 us                                                       | 893 us: 1.04x faster                                                  |
| json                       | 5.58 ms                                                      | 5.36 ms: 1.04x faster                                                 |
| logging_silent             | 100 ns                                                       | 97.7 ns: 1.03x faster                                                 |
| pickle_pure_python         | 316 us                                                       | 308 us: 1.03x faster                                                  |
| sympy_integrate            | 25.8 ms                                                      | 25.3 ms: 1.02x faster                                                 |
| tomli_loads                | 2.25 sec                                                     | 2.21 sec: 1.02x faster                                                |
| pycparser                  | 1.31 sec                                                     | 1.29 sec: 1.02x faster                                                |
| dask                       | 410 ms                                                       | 403 ms: 1.02x faster                                                  |
| raytrace                   | 309 ms                                                       | 306 ms: 1.01x faster                                                  |
| unpickle_pure_python       | 238 us                                                       | 241 us: 1.01x slower                                                  |
| pickle_dict                | 32.3 us                                                      | 32.7 us: 1.01x slower                                                 |
| sqlglot_normalize          | 122 ms                                                       | 123 ms: 1.01x slower                                                  |
| html5lib                   | 72.2 ms                                                      | 73.5 ms: 1.02x slower                                                 |
| spectral_norm              | 95.1 ms                                                      | 96.8 ms: 1.02x slower                                                 |
| deepcopy_memo              | 37.5 us                                                      | 38.4 us: 1.02x slower                                                 |
| unpickle_list              | 4.60 us                                                      | 4.71 us: 1.02x slower                                                 |
| django_template            | 39.3 ms                                                      | 40.2 ms: 1.02x slower                                                 |
| pathlib                    | 18.9 ms                                                      | 19.4 ms: 1.03x slower                                                 |
| nbody                      | 92.9 ms                                                      | 95.4 ms: 1.03x slower                                                 |
| dulwich_log                | 67.4 ms                                                      | 69.4 ms: 1.03x slower                                                 |
| meteor_contest             | 131 ms                                                       | 135 ms: 1.03x slower                                                  |
| xml_etree_process          | 55.9 ms                                                      | 58.0 ms: 1.04x slower                                                 |
| pidigits                   | 251 ms                                                       | 261 ms: 1.04x slower                                                  |
| nqueens                    | 103 ms                                                       | 107 ms: 1.04x slower                                                  |
| richards                   | 49.7 ms                                                      | 51.9 ms: 1.04x slower                                                 |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.25 ms: 1.05x slower                                                 |
| regex_effbot               | 3.34 ms                                                      | 3.50 ms: 1.05x slower                                                 |
| genshi_text                | 25.5 ms                                                      | 26.7 ms: 1.05x slower                                                 |
| pprint_pformat             | 1.67 sec                                                     | 1.75 sec: 1.05x slower                                                |
| 2to3                       | 287 ms                                                       | 301 ms: 1.05x slower                                                  |
| gc_traversal               | 4.15 ms                                                      | 4.37 ms: 1.05x slower                                                 |
| genshi_xml                 | 57.1 ms                                                      | 60.3 ms: 1.06x slower                                                 |
| xml_etree_generate         | 79.7 ms                                                      | 84.3 ms: 1.06x slower                                                 |
| regex_v8                   | 24.4 ms                                                      | 25.9 ms: 1.06x slower                                                 |
| float                      | 74.9 ms                                                      | 79.5 ms: 1.06x slower                                                 |
| pprint_safe_repr           | 805 ms                                                       | 858 ms: 1.07x slower                                                  |
| sqlite_synth               | 2.52 us                                                      | 2.70 us: 1.07x slower                                                 |
| docutils                   | 2.85 sec                                                     | 3.05 sec: 1.07x slower                                                |
| scimark_monte_carlo        | 69.8 ms                                                      | 74.8 ms: 1.07x slower                                                 |
| sqlglot_optimize           | 59.0 ms                                                      | 63.2 ms: 1.07x slower                                                 |
| regex_dna                  | 227 ms                                                       | 246 ms: 1.08x slower                                                  |
| mypy2                      | 762 ms                                                       | 828 ms: 1.09x slower                                                  |
| pickle                     | 9.89 us                                                      | 10.8 us: 1.09x slower                                                 |
| scimark_lu                 | 114 ms                                                       | 126 ms: 1.10x slower                                                  |
| hexiom                     | 6.98 ms                                                      | 7.75 ms: 1.11x slower                                                 |
| bench_mp_pool              | 4.70 ms                                                      | 5.22 ms: 1.11x slower                                                 |
| pickle_list                | 3.94 us                                                      | 4.38 us: 1.11x slower                                                 |
| unpickle                   | 13.3 us                                                      | 14.9 us: 1.13x slower                                                 |
| bench_thread_pool          | 1.00 ms                                                      | 1.13 ms: 1.13x slower                                                 |
| aiohttp                    | 986 us                                                       | 1.12 ms: 1.13x slower                                                 |
| gunicorn                   | 966 us                                                       | 1.09 ms: 1.13x slower                                                 |
| create_gc_cycles           | 1.58 ms                                                      | 1.80 ms: 1.14x slower                                                 |
| go                         | 158 ms                                                       | 180 ms: 1.14x slower                                                  |
| scimark_fft                | 281 ms                                                       | 320 ms: 1.14x slower                                                  |
| pyflate                    | 449 ms                                                       | 525 ms: 1.17x slower                                                  |
| telco                      | 6.81 ms                                                      | 8.03 ms: 1.18x slower                                                 |
| async_generators           | 322 ms                                                       | 394 ms: 1.23x slower                                                  |
| python_startup             | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                                 |
| coverage                   | 66.1 ms                                                      | 88.1 ms: 1.33x slower                                                 |
| scimark_sor                | 110 ms                                                       | 155 ms: 1.42x slower                                                  |
| python_startup_no_site     | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                          |

Benchmark hidden because not significant (4): deepcopy_reduce, deepcopy, asyncio_websockets, tornado_http
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 62.80% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x