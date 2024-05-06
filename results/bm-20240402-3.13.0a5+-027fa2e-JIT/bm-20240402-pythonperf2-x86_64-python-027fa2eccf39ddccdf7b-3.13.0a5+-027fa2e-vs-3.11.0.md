# Results vs. 3.11.0

- fork: python
- ref: 027fa2eccf39ddccdf7b
- machine: linux-x86_64
- commit hash: 027fa2e
- commit date: 2024-04-02
- overall geometric mean: 1.05x faster
- HPT reliability: 73.39%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 297 ms: 1.04x slower                                                         |
| chameleon      | 7.92 ms                                                      | 7.41 ms: 1.07x faster                                                        |
| docutils       | 2.85 sec                                                     | 3.09 sec: 1.09x slower                                                       |
| tornado_http   | 124 ms                                                       | 122 ms: 1.02x faster                                                         |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                 |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 474 ms                                                       | 335 ms: 1.42x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 444 ms: 1.42x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 427 ms: 1.41x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 849 ms: 1.38x faster                                                         |
| async_tree_none            | 518 ms                                                       | 380 ms: 1.36x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 861 ms: 1.34x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 592 ms: 1.27x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 608 ms: 1.24x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.35x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 74.9 ms                                                      | 75.9 ms: 1.01x slower                                                        |
| pidigits       | 251 ms                                                       | 262 ms: 1.04x slower                                                         |
| nbody          | 92.9 ms                                                      | 101 ms: 1.09x slower                                                         |
| Geometric mean | (ref)                                                        | 1.05x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 148 ms: 1.06x faster                                                         |
| regex_effbot   | 3.34 ms                                                      | 3.45 ms: 1.03x slower                                                        |
| regex_v8       | 24.4 ms                                                      | 26.0 ms: 1.06x slower                                                        |
| regex_dna      | 227 ms                                                       | 247 ms: 1.08x slower                                                         |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|---------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps          | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                        |
| json_loads          | 28.9 us                                                      | 25.4 us: 1.14x faster                                                        |
| tomli_loads         | 2.25 sec                                                     | 2.15 sec: 1.05x faster                                                       |
| xml_etree_parse     | 155 ms                                                       | 149 ms: 1.04x faster                                                         |
| xml_etree_iterparse | 107 ms                                                       | 104 ms: 1.03x faster                                                         |
| pickle_pure_python  | 316 us                                                       | 309 us: 1.02x faster                                                         |
| pickle_dict         | 32.3 us                                                      | 33.7 us: 1.04x slower                                                        |
| xml_etree_process   | 55.9 ms                                                      | 58.6 ms: 1.05x slower                                                        |
| xml_etree_generate  | 79.7 ms                                                      | 84.0 ms: 1.05x slower                                                        |
| pickle              | 9.89 us                                                      | 10.7 us: 1.08x slower                                                        |
| pickle_list         | 3.94 us                                                      | 4.42 us: 1.12x slower                                                        |
| unpickle            | 13.3 us                                                      | 15.1 us: 1.14x slower                                                        |
| Geometric mean      | (ref)                                                        | 1.00x faster                                                                 |

Benchmark hidden because not significant (2): unpickle_list, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                                        |
| python_startup_no_site | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 11.0 ms                                                      | 9.91 ms: 1.11x faster                                                        |
| genshi_xml     | 57.1 ms                                                      | 58.5 ms: 1.02x slower                                                        |
| genshi_text    | 25.5 ms                                                      | 26.8 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                        | 1.01x faster                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 119 us: 4.47x faster                                                         |
| asyncio_tcp                | 747 ms                                                       | 373 ms: 2.00x faster                                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                       |
| generators                 | 54.6 ms                                                      | 33.3 ms: 1.64x faster                                                        |
| pylint                     | 514 ms                                                       | 336 ms: 1.53x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 335 ms: 1.42x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 444 ms: 1.42x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 427 ms: 1.41x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 849 ms: 1.38x faster                                                         |
| async_tree_none            | 518 ms                                                       | 380 ms: 1.36x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 861 ms: 1.34x faster                                                         |
| comprehensions             | 25.1 us                                                      | 19.5 us: 1.28x faster                                                        |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 592 ms: 1.27x faster                                                         |
| coroutines                 | 27.8 ms                                                      | 22.0 ms: 1.26x faster                                                        |
| json_dumps                 | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 608 ms: 1.24x faster                                                         |
| chaos                      | 74.9 ms                                                      | 64.1 ms: 1.17x faster                                                        |
| json_loads                 | 28.9 us                                                      | 25.4 us: 1.14x faster                                                        |
| sympy_sum                  | 186 ms                                                       | 164 ms: 1.13x faster                                                         |
| richards_super             | 63.6 ms                                                      | 56.8 ms: 1.12x faster                                                        |
| mako                       | 11.0 ms                                                      | 9.91 ms: 1.11x faster                                                        |
| deltablue                  | 3.97 ms                                                      | 3.58 ms: 1.11x faster                                                        |
| logging_simple             | 7.24 us                                                      | 6.54 us: 1.11x faster                                                        |
| sympy_str                  | 337 ms                                                       | 306 ms: 1.10x faster                                                         |
| raytrace                   | 309 ms                                                       | 285 ms: 1.09x faster                                                         |
| fannkuch                   | 416 ms                                                       | 385 ms: 1.08x faster                                                         |
| crypto_pyaes               | 83.3 ms                                                      | 77.1 ms: 1.08x faster                                                        |
| sympy_expand               | 553 ms                                                       | 514 ms: 1.08x faster                                                         |
| sqlglot_parse              | 1.51 ms                                                      | 1.41 ms: 1.08x faster                                                        |
| chameleon                  | 7.92 ms                                                      | 7.41 ms: 1.07x faster                                                        |
| logging_format             | 7.71 us                                                      | 7.21 us: 1.07x faster                                                        |
| regex_compile              | 156 ms                                                       | 148 ms: 1.06x faster                                                         |
| sqlglot_transpile          | 1.91 ms                                                      | 1.82 ms: 1.05x faster                                                        |
| mdp                        | 2.77 sec                                                     | 2.64 sec: 1.05x faster                                                       |
| tomli_loads                | 2.25 sec                                                     | 2.15 sec: 1.05x faster                                                       |
| thrift                     | 931 us                                                       | 890 us: 1.05x faster                                                         |
| logging_silent             | 100 ns                                                       | 95.9 ns: 1.05x faster                                                        |
| xml_etree_parse            | 155 ms                                                       | 149 ms: 1.04x faster                                                         |
| xml_etree_iterparse        | 107 ms                                                       | 104 ms: 1.03x faster                                                         |
| pickle_pure_python         | 316 us                                                       | 309 us: 1.02x faster                                                         |
| pycparser                  | 1.31 sec                                                     | 1.28 sec: 1.02x faster                                                       |
| tornado_http               | 124 ms                                                       | 122 ms: 1.02x faster                                                         |
| spectral_norm              | 95.1 ms                                                      | 93.2 ms: 1.02x faster                                                        |
| dask                       | 410 ms                                                       | 404 ms: 1.01x faster                                                         |
| json                       | 5.58 ms                                                      | 5.51 ms: 1.01x faster                                                        |
| sympy_integrate            | 25.8 ms                                                      | 25.5 ms: 1.01x faster                                                        |
| meteor_contest             | 131 ms                                                       | 131 ms: 1.00x slower                                                         |
| sqlglot_normalize          | 122 ms                                                       | 122 ms: 1.01x slower                                                         |
| deepcopy                   | 391 us                                                       | 394 us: 1.01x slower                                                         |
| float                      | 74.9 ms                                                      | 75.9 ms: 1.01x slower                                                        |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.13 ms: 1.02x slower                                                        |
| richards                   | 49.7 ms                                                      | 50.6 ms: 1.02x slower                                                        |
| scimark_monte_carlo        | 69.8 ms                                                      | 71.5 ms: 1.02x slower                                                        |
| pathlib                    | 18.9 ms                                                      | 19.4 ms: 1.02x slower                                                        |
| genshi_xml                 | 57.1 ms                                                      | 58.5 ms: 1.02x slower                                                        |
| nqueens                    | 103 ms                                                       | 105 ms: 1.03x slower                                                         |
| deepcopy_memo              | 37.5 us                                                      | 38.6 us: 1.03x slower                                                        |
| regex_effbot               | 3.34 ms                                                      | 3.45 ms: 1.03x slower                                                        |
| dulwich_log                | 67.4 ms                                                      | 69.8 ms: 1.04x slower                                                        |
| 2to3                       | 287 ms                                                       | 297 ms: 1.04x slower                                                         |
| pidigits                   | 251 ms                                                       | 262 ms: 1.04x slower                                                         |
| pprint_pformat             | 1.67 sec                                                     | 1.74 sec: 1.04x slower                                                       |
| pickle_dict                | 32.3 us                                                      | 33.7 us: 1.04x slower                                                        |
| xml_etree_process          | 55.9 ms                                                      | 58.6 ms: 1.05x slower                                                        |
| genshi_text                | 25.5 ms                                                      | 26.8 ms: 1.05x slower                                                        |
| xml_etree_generate         | 79.7 ms                                                      | 84.0 ms: 1.05x slower                                                        |
| pprint_safe_repr           | 805 ms                                                       | 851 ms: 1.06x slower                                                         |
| sqlglot_optimize           | 59.0 ms                                                      | 62.3 ms: 1.06x slower                                                        |
| scimark_lu                 | 114 ms                                                       | 121 ms: 1.06x slower                                                         |
| hexiom                     | 6.98 ms                                                      | 7.39 ms: 1.06x slower                                                        |
| sqlite_synth               | 2.52 us                                                      | 2.68 us: 1.06x slower                                                        |
| regex_v8                   | 24.4 ms                                                      | 26.0 ms: 1.06x slower                                                        |
| pyflate                    | 449 ms                                                       | 482 ms: 1.07x slower                                                         |
| pickle                     | 9.89 us                                                      | 10.7 us: 1.08x slower                                                        |
| mypy2                      | 762 ms                                                       | 826 ms: 1.08x slower                                                         |
| regex_dna                  | 227 ms                                                       | 247 ms: 1.08x slower                                                         |
| nbody                      | 92.9 ms                                                      | 101 ms: 1.09x slower                                                         |
| docutils                   | 2.85 sec                                                     | 3.09 sec: 1.09x slower                                                       |
| gc_traversal               | 4.15 ms                                                      | 4.54 ms: 1.09x slower                                                        |
| bench_mp_pool              | 4.70 ms                                                      | 5.15 ms: 1.09x slower                                                        |
| bench_thread_pool          | 1.00 ms                                                      | 1.11 ms: 1.11x slower                                                        |
| scimark_fft                | 281 ms                                                       | 314 ms: 1.12x slower                                                         |
| pickle_list                | 3.94 us                                                      | 4.42 us: 1.12x slower                                                        |
| go                         | 158 ms                                                       | 177 ms: 1.12x slower                                                         |
| gunicorn                   | 966 us                                                       | 1.09 ms: 1.13x slower                                                        |
| unpickle                   | 13.3 us                                                      | 15.1 us: 1.14x slower                                                        |
| aiohttp                    | 986 us                                                       | 1.13 ms: 1.14x slower                                                        |
| create_gc_cycles           | 1.58 ms                                                      | 1.84 ms: 1.17x slower                                                        |
| telco                      | 6.81 ms                                                      | 7.98 ms: 1.17x slower                                                        |
| async_generators           | 322 ms                                                       | 388 ms: 1.21x slower                                                         |
| coverage                   | 66.1 ms                                                      | 81.8 ms: 1.24x slower                                                        |
| python_startup             | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                                        |
| scimark_sor                | 110 ms                                                       | 154 ms: 1.40x slower                                                         |
| python_startup_no_site     | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                                 |

Benchmark hidden because not significant (5): unpickle_list, html5lib, unpickle_pure_python, asyncio_websockets, deepcopy_reduce
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 73.39% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x