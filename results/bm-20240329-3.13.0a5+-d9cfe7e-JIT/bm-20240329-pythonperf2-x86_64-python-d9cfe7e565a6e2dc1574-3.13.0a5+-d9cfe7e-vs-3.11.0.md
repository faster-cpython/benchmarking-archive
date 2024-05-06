# Results vs. 3.11.0

- fork: python
- ref: d9cfe7e565a6e2dc1574
- machine: linux-x86_64
- commit hash: d9cfe7e
- commit date: 2024-03-29
- overall geometric mean: 1.04x faster
- HPT reliability: 66.46%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 300 ms: 1.05x slower                                                         |
| chameleon      | 7.92 ms                                                      | 7.43 ms: 1.07x faster                                                        |
| docutils       | 2.85 sec                                                     | 3.07 sec: 1.08x slower                                                       |
| html5lib       | 72.2 ms                                                      | 73.4 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 431 ms: 1.39x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 341 ms: 1.39x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 454 ms: 1.39x faster                                                         |
| async_tree_none            | 518 ms                                                       | 377 ms: 1.37x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 880 ms: 1.31x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 907 ms: 1.29x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 596 ms: 1.26x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 600 ms: 1.25x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 261 ms: 1.04x slower                                                         |
| nbody          | 92.9 ms                                                      | 98.3 ms: 1.06x slower                                                        |
| float          | 74.9 ms                                                      | 79.5 ms: 1.06x slower                                                        |
| Geometric mean | (ref)                                                        | 1.05x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 148 ms: 1.05x faster                                                         |
| regex_effbot   | 3.34 ms                                                      | 3.42 ms: 1.02x slower                                                        |
| regex_v8       | 24.4 ms                                                      | 26.1 ms: 1.07x slower                                                        |
| regex_dna      | 227 ms                                                       | 244 ms: 1.07x slower                                                         |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.5 ms: 1.26x faster                                                        |
| json_loads           | 28.9 us                                                      | 25.8 us: 1.12x faster                                                        |
| xml_etree_parse      | 155 ms                                                       | 144 ms: 1.08x faster                                                         |
| tomli_loads          | 2.25 sec                                                     | 2.16 sec: 1.04x faster                                                       |
| xml_etree_iterparse  | 107 ms                                                       | 104 ms: 1.03x faster                                                         |
| unpickle_pure_python | 238 us                                                       | 235 us: 1.01x faster                                                         |
| pickle_dict          | 32.3 us                                                      | 33.0 us: 1.02x slower                                                        |
| xml_etree_process    | 55.9 ms                                                      | 58.5 ms: 1.05x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 83.9 ms: 1.05x slower                                                        |
| pickle               | 9.89 us                                                      | 10.9 us: 1.10x slower                                                        |
| pickle_list          | 3.94 us                                                      | 4.38 us: 1.11x slower                                                        |
| unpickle             | 13.3 us                                                      | 15.5 us: 1.17x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                                 |

Benchmark hidden because not significant (2): pickle_pure_python, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                                        |
| python_startup_no_site | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 10.0 ms: 1.10x faster                                                        |
| genshi_xml      | 57.1 ms                                                      | 59.1 ms: 1.04x slower                                                        |
| django_template | 39.3 ms                                                      | 41.2 ms: 1.05x slower                                                        |
| genshi_text     | 25.5 ms                                                      | 26.8 ms: 1.05x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 122 us: 4.36x faster                                                         |
| asyncio_tcp                | 747 ms                                                       | 372 ms: 2.01x faster                                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.95x faster                                                       |
| generators                 | 54.6 ms                                                      | 34.6 ms: 1.58x faster                                                        |
| pylint                     | 514 ms                                                       | 364 ms: 1.41x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 431 ms: 1.39x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 341 ms: 1.39x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 454 ms: 1.39x faster                                                         |
| async_tree_none            | 518 ms                                                       | 377 ms: 1.37x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 880 ms: 1.31x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 907 ms: 1.29x faster                                                         |
| comprehensions             | 25.1 us                                                      | 19.7 us: 1.27x faster                                                        |
| json_dumps                 | 13.3 ms                                                      | 10.5 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 596 ms: 1.26x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 600 ms: 1.25x faster                                                         |
| coroutines                 | 27.8 ms                                                      | 22.5 ms: 1.24x faster                                                        |
| sympy_sum                  | 186 ms                                                       | 163 ms: 1.14x faster                                                         |
| json_loads                 | 28.9 us                                                      | 25.8 us: 1.12x faster                                                        |
| chaos                      | 74.9 ms                                                      | 67.5 ms: 1.11x faster                                                        |
| sympy_str                  | 337 ms                                                       | 304 ms: 1.11x faster                                                         |
| mako                       | 11.0 ms                                                      | 10.0 ms: 1.10x faster                                                        |
| richards_super             | 63.6 ms                                                      | 58.0 ms: 1.10x faster                                                        |
| fannkuch                   | 416 ms                                                       | 379 ms: 1.10x faster                                                         |
| sympy_expand               | 553 ms                                                       | 512 ms: 1.08x faster                                                         |
| xml_etree_parse            | 155 ms                                                       | 144 ms: 1.08x faster                                                         |
| crypto_pyaes               | 83.3 ms                                                      | 77.5 ms: 1.08x faster                                                        |
| chameleon                  | 7.92 ms                                                      | 7.43 ms: 1.07x faster                                                        |
| logging_simple             | 7.24 us                                                      | 6.80 us: 1.07x faster                                                        |
| mdp                        | 2.77 sec                                                     | 2.62 sec: 1.06x faster                                                       |
| thrift                     | 931 us                                                       | 882 us: 1.06x faster                                                         |
| regex_compile              | 156 ms                                                       | 148 ms: 1.05x faster                                                         |
| logging_format             | 7.71 us                                                      | 7.33 us: 1.05x faster                                                        |
| sqlglot_parse              | 1.51 ms                                                      | 1.45 ms: 1.05x faster                                                        |
| tomli_loads                | 2.25 sec                                                     | 2.16 sec: 1.04x faster                                                       |
| sqlglot_transpile          | 1.91 ms                                                      | 1.84 ms: 1.04x faster                                                        |
| json                       | 5.58 ms                                                      | 5.41 ms: 1.03x faster                                                        |
| logging_silent             | 100 ns                                                       | 97.2 ns: 1.03x faster                                                        |
| deltablue                  | 3.97 ms                                                      | 3.85 ms: 1.03x faster                                                        |
| xml_etree_iterparse        | 107 ms                                                       | 104 ms: 1.03x faster                                                         |
| spectral_norm              | 95.1 ms                                                      | 93.2 ms: 1.02x faster                                                        |
| sympy_integrate            | 25.8 ms                                                      | 25.3 ms: 1.02x faster                                                        |
| pycparser                  | 1.31 sec                                                     | 1.29 sec: 1.01x faster                                                       |
| unpickle_pure_python       | 238 us                                                       | 235 us: 1.01x faster                                                         |
| deepcopy                   | 391 us                                                       | 388 us: 1.01x faster                                                         |
| html5lib                   | 72.2 ms                                                      | 73.4 ms: 1.02x slower                                                        |
| deepcopy_memo              | 37.5 us                                                      | 38.3 us: 1.02x slower                                                        |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.15 ms: 1.02x slower                                                        |
| pickle_dict                | 32.3 us                                                      | 33.0 us: 1.02x slower                                                        |
| regex_effbot               | 3.34 ms                                                      | 3.42 ms: 1.02x slower                                                        |
| sqlglot_normalize          | 122 ms                                                       | 125 ms: 1.03x slower                                                         |
| pathlib                    | 18.9 ms                                                      | 19.4 ms: 1.03x slower                                                        |
| pprint_pformat             | 1.67 sec                                                     | 1.72 sec: 1.03x slower                                                       |
| genshi_xml                 | 57.1 ms                                                      | 59.1 ms: 1.04x slower                                                        |
| dulwich_log                | 67.4 ms                                                      | 69.8 ms: 1.04x slower                                                        |
| pidigits                   | 251 ms                                                       | 261 ms: 1.04x slower                                                         |
| scimark_monte_carlo        | 69.8 ms                                                      | 72.9 ms: 1.04x slower                                                        |
| pprint_safe_repr           | 805 ms                                                       | 841 ms: 1.05x slower                                                         |
| richards                   | 49.7 ms                                                      | 51.9 ms: 1.05x slower                                                        |
| 2to3                       | 287 ms                                                       | 300 ms: 1.05x slower                                                         |
| xml_etree_process          | 55.9 ms                                                      | 58.5 ms: 1.05x slower                                                        |
| django_template            | 39.3 ms                                                      | 41.2 ms: 1.05x slower                                                        |
| genshi_text                | 25.5 ms                                                      | 26.8 ms: 1.05x slower                                                        |
| scimark_lu                 | 114 ms                                                       | 120 ms: 1.05x slower                                                         |
| xml_etree_generate         | 79.7 ms                                                      | 83.9 ms: 1.05x slower                                                        |
| gc_traversal               | 4.15 ms                                                      | 4.38 ms: 1.06x slower                                                        |
| nbody                      | 92.9 ms                                                      | 98.3 ms: 1.06x slower                                                        |
| float                      | 74.9 ms                                                      | 79.5 ms: 1.06x slower                                                        |
| regex_v8                   | 24.4 ms                                                      | 26.1 ms: 1.07x slower                                                        |
| regex_dna                  | 227 ms                                                       | 244 ms: 1.07x slower                                                         |
| sqlite_synth               | 2.52 us                                                      | 2.71 us: 1.08x slower                                                        |
| sqlglot_optimize           | 59.0 ms                                                      | 63.6 ms: 1.08x slower                                                        |
| docutils                   | 2.85 sec                                                     | 3.07 sec: 1.08x slower                                                       |
| hexiom                     | 6.98 ms                                                      | 7.57 ms: 1.08x slower                                                        |
| mypy2                      | 762 ms                                                       | 833 ms: 1.09x slower                                                         |
| pickle                     | 9.89 us                                                      | 10.9 us: 1.10x slower                                                        |
| bench_mp_pool              | 4.70 ms                                                      | 5.16 ms: 1.10x slower                                                        |
| scimark_fft                | 281 ms                                                       | 312 ms: 1.11x slower                                                         |
| pickle_list                | 3.94 us                                                      | 4.38 us: 1.11x slower                                                        |
| bench_thread_pool          | 1.00 ms                                                      | 1.12 ms: 1.12x slower                                                        |
| create_gc_cycles           | 1.58 ms                                                      | 1.79 ms: 1.13x slower                                                        |
| gunicorn                   | 966 us                                                       | 1.10 ms: 1.14x slower                                                        |
| aiohttp                    | 986 us                                                       | 1.12 ms: 1.14x slower                                                        |
| go                         | 158 ms                                                       | 180 ms: 1.14x slower                                                         |
| pyflate                    | 449 ms                                                       | 519 ms: 1.16x slower                                                         |
| unpickle                   | 13.3 us                                                      | 15.5 us: 1.17x slower                                                        |
| telco                      | 6.81 ms                                                      | 7.97 ms: 1.17x slower                                                        |
| async_generators           | 322 ms                                                       | 390 ms: 1.21x slower                                                         |
| coverage                   | 66.1 ms                                                      | 83.0 ms: 1.26x slower                                                        |
| python_startup             | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                                        |
| unpack_sequence            | 45.7 ns                                                      | 58.5 ns: 1.28x slower                                                        |
| scimark_sor                | 110 ms                                                       | 154 ms: 1.40x slower                                                         |
| python_startup_no_site     | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                                 |

Benchmark hidden because not significant (9): asyncio_websockets, dask, raytrace, pickle_pure_python, deepcopy_reduce, tornado_http, meteor_contest, nqueens, unpickle_list
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 66.46% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x