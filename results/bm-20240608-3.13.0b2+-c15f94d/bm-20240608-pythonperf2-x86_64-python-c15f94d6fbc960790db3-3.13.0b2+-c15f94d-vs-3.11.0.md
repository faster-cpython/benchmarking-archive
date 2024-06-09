# Results vs. 3.11.0

- fork: python
- ref: c15f94d6fbc960790db3
- machine: linux-x86_64
- commit hash: c15f94d
- commit date: 2024-06-08
- overall geometric mean: 1.07x faster
- HPT reliability: 99.69%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 291 ms: 1.02x slower                                                         |
| chameleon      | 7.92 ms                                                      | 7.40 ms: 1.07x faster                                                        |
| docutils       | 2.85 sec                                                     | 2.99 sec: 1.05x slower                                                       |
| html5lib       | 72.2 ms                                                      | 75.3 ms: 1.04x slower                                                        |
| tornado_http   | 124 ms                                                       | 119 ms: 1.04x faster                                                         |
| Geometric mean | (ref)                                                        | 1.00x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 518 ms                                                       | 371 ms: 1.40x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 432 ms: 1.39x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 345 ms: 1.37x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 465 ms: 1.35x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 884 ms: 1.33x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 580 ms: 1.29x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 904 ms: 1.28x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 614 ms: 1.23x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 89.4 ms: 1.04x faster                                                        |
| pidigits       | 251 ms                                                       | 253 ms: 1.01x slower                                                         |
| float          | 74.9 ms                                                      | 80.8 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 145 ms: 1.08x faster                                                         |
| regex_v8       | 24.4 ms                                                      | 26.4 ms: 1.08x slower                                                        |
| regex_dna      | 227 ms                                                       | 248 ms: 1.09x slower                                                         |
| regex_effbot   | 3.34 ms                                                      | 3.72 ms: 1.11x slower                                                        |
| Geometric mean | (ref)                                                        | 1.05x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 11.1 ms: 1.20x faster                                                        |
| json_loads           | 28.9 us                                                      | 24.8 us: 1.17x faster                                                        |
| xml_etree_parse      | 155 ms                                                       | 143 ms: 1.08x faster                                                         |
| unpickle_pure_python | 238 us                                                       | 226 us: 1.06x faster                                                         |
| xml_etree_iterparse  | 107 ms                                                       | 102 ms: 1.05x faster                                                         |
| pickle_pure_python   | 316 us                                                       | 309 us: 1.02x faster                                                         |
| pickle_dict          | 32.3 us                                                      | 33.3 us: 1.03x slower                                                        |
| unpickle_list        | 4.60 us                                                      | 4.80 us: 1.04x slower                                                        |
| xml_etree_process    | 55.9 ms                                                      | 59.3 ms: 1.06x slower                                                        |
| tomli_loads          | 2.25 sec                                                     | 2.39 sec: 1.06x slower                                                       |
| xml_etree_generate   | 79.7 ms                                                      | 85.2 ms: 1.07x slower                                                        |
| pickle               | 9.89 us                                                      | 10.6 us: 1.07x slower                                                        |
| pickle_list          | 3.94 us                                                      | 4.46 us: 1.13x slower                                                        |
| unpickle             | 13.3 us                                                      | 15.7 us: 1.19x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 8.84 ms: 1.14x slower                                                        |
| python_startup         | 10.7 ms                                                      | 13.2 ms: 1.23x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.19x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 11.0 ms                                                      | 10.3 ms: 1.06x faster                                                        |
| genshi_xml     | 57.1 ms                                                      | 55.5 ms: 1.03x faster                                                        |
| genshi_text    | 25.5 ms                                                      | 25.0 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                        | 1.03x faster                                                                 |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-pythonperf2-x86_64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 173 us: 3.07x faster                                                         |
| asyncio_tcp                | 747 ms                                                       | 378 ms: 1.98x faster                                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                       |
| generators                 | 54.6 ms                                                      | 33.4 ms: 1.64x faster                                                        |
| pylint                     | 514 ms                                                       | 340 ms: 1.51x faster                                                         |
| comprehensions             | 25.1 us                                                      | 17.1 us: 1.47x faster                                                        |
| async_tree_none            | 518 ms                                                       | 371 ms: 1.40x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 432 ms: 1.39x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 345 ms: 1.37x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 465 ms: 1.35x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 884 ms: 1.33x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 580 ms: 1.29x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 904 ms: 1.28x faster                                                         |
| coroutines                 | 27.8 ms                                                      | 22.0 ms: 1.26x faster                                                        |
| chaos                      | 74.9 ms                                                      | 60.5 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 614 ms: 1.23x faster                                                         |
| sympy_sum                  | 186 ms                                                       | 155 ms: 1.20x faster                                                         |
| json_dumps                 | 13.3 ms                                                      | 11.1 ms: 1.20x faster                                                        |
| deltablue                  | 3.97 ms                                                      | 3.36 ms: 1.18x faster                                                        |
| json_loads                 | 28.9 us                                                      | 24.8 us: 1.17x faster                                                        |
| scimark_lu                 | 114 ms                                                       | 97.9 ms: 1.16x faster                                                        |
| fannkuch                   | 416 ms                                                       | 358 ms: 1.16x faster                                                         |
| raytrace                   | 309 ms                                                       | 268 ms: 1.16x faster                                                         |
| nqueens                    | 103 ms                                                       | 88.8 ms: 1.16x faster                                                        |
| sympy_str                  | 337 ms                                                       | 295 ms: 1.14x faster                                                         |
| logging_simple             | 7.24 us                                                      | 6.40 us: 1.13x faster                                                        |
| crypto_pyaes               | 83.3 ms                                                      | 73.9 ms: 1.13x faster                                                        |
| sympy_integrate            | 25.8 ms                                                      | 23.4 ms: 1.10x faster                                                        |
| sympy_expand               | 553 ms                                                       | 501 ms: 1.10x faster                                                         |
| logging_format             | 7.71 us                                                      | 7.02 us: 1.10x faster                                                        |
| pathlib                    | 18.9 ms                                                      | 17.3 ms: 1.10x faster                                                        |
| hexiom                     | 6.98 ms                                                      | 6.37 ms: 1.09x faster                                                        |
| mdp                        | 2.77 sec                                                     | 2.53 sec: 1.09x faster                                                       |
| bench_thread_pool          | 1.00 ms                                                      | 918 us: 1.09x faster                                                         |
| xml_etree_parse            | 155 ms                                                       | 143 ms: 1.08x faster                                                         |
| sqlglot_parse              | 1.51 ms                                                      | 1.40 ms: 1.08x faster                                                        |
| regex_compile              | 156 ms                                                       | 145 ms: 1.08x faster                                                         |
| sqlglot_transpile          | 1.91 ms                                                      | 1.78 ms: 1.07x faster                                                        |
| chameleon                  | 7.92 ms                                                      | 7.40 ms: 1.07x faster                                                        |
| scimark_monte_carlo        | 69.8 ms                                                      | 65.5 ms: 1.07x faster                                                        |
| mako                       | 11.0 ms                                                      | 10.3 ms: 1.06x faster                                                        |
| pycparser                  | 1.31 sec                                                     | 1.23 sec: 1.06x faster                                                       |
| json                       | 5.58 ms                                                      | 5.28 ms: 1.06x faster                                                        |
| unpickle_pure_python       | 238 us                                                       | 226 us: 1.06x faster                                                         |
| richards_super             | 63.6 ms                                                      | 60.3 ms: 1.05x faster                                                        |
| xml_etree_iterparse        | 107 ms                                                       | 102 ms: 1.05x faster                                                         |
| tornado_http               | 124 ms                                                       | 119 ms: 1.04x faster                                                         |
| logging_silent             | 100 ns                                                       | 96.3 ns: 1.04x faster                                                        |
| thrift                     | 931 us                                                       | 894 us: 1.04x faster                                                         |
| nbody                      | 92.9 ms                                                      | 89.4 ms: 1.04x faster                                                        |
| dask                       | 410 ms                                                       | 396 ms: 1.03x faster                                                         |
| genshi_xml                 | 57.1 ms                                                      | 55.5 ms: 1.03x faster                                                        |
| deepcopy                   | 391 us                                                       | 381 us: 1.03x faster                                                         |
| pickle_pure_python         | 316 us                                                       | 309 us: 1.02x faster                                                         |
| sqlglot_normalize          | 122 ms                                                       | 119 ms: 1.02x faster                                                         |
| genshi_text                | 25.5 ms                                                      | 25.0 ms: 1.02x faster                                                        |
| meteor_contest             | 131 ms                                                       | 128 ms: 1.02x faster                                                         |
| deepcopy_reduce            | 3.40 us                                                      | 3.37 us: 1.01x faster                                                        |
| pprint_pformat             | 1.67 sec                                                     | 1.66 sec: 1.00x faster                                                       |
| deepcopy_memo              | 37.5 us                                                      | 37.8 us: 1.01x slower                                                        |
| pidigits                   | 251 ms                                                       | 253 ms: 1.01x slower                                                         |
| pprint_safe_repr           | 805 ms                                                       | 814 ms: 1.01x slower                                                         |
| 2to3                       | 287 ms                                                       | 291 ms: 1.02x slower                                                         |
| spectral_norm              | 95.1 ms                                                      | 97.2 ms: 1.02x slower                                                        |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.18 ms: 1.03x slower                                                        |
| pickle_dict                | 32.3 us                                                      | 33.3 us: 1.03x slower                                                        |
| go                         | 158 ms                                                       | 163 ms: 1.04x slower                                                         |
| html5lib                   | 72.2 ms                                                      | 75.3 ms: 1.04x slower                                                        |
| unpickle_list              | 4.60 us                                                      | 4.80 us: 1.04x slower                                                        |
| docutils                   | 2.85 sec                                                     | 2.99 sec: 1.05x slower                                                       |
| gc_traversal               | 4.15 ms                                                      | 4.38 ms: 1.06x slower                                                        |
| xml_etree_process          | 55.9 ms                                                      | 59.3 ms: 1.06x slower                                                        |
| tomli_loads                | 2.25 sec                                                     | 2.39 sec: 1.06x slower                                                       |
| xml_etree_generate         | 79.7 ms                                                      | 85.2 ms: 1.07x slower                                                        |
| scimark_sor                | 110 ms                                                       | 117 ms: 1.07x slower                                                         |
| pickle                     | 9.89 us                                                      | 10.6 us: 1.07x slower                                                        |
| richards                   | 49.7 ms                                                      | 53.5 ms: 1.08x slower                                                        |
| gunicorn                   | 966 us                                                       | 1.04 ms: 1.08x slower                                                        |
| pyflate                    | 449 ms                                                       | 484 ms: 1.08x slower                                                         |
| float                      | 74.9 ms                                                      | 80.8 ms: 1.08x slower                                                        |
| regex_v8                   | 24.4 ms                                                      | 26.4 ms: 1.08x slower                                                        |
| aiohttp                    | 986 us                                                       | 1.07 ms: 1.09x slower                                                        |
| regex_dna                  | 227 ms                                                       | 248 ms: 1.09x slower                                                         |
| scimark_fft                | 281 ms                                                       | 308 ms: 1.10x slower                                                         |
| sqlite_synth               | 2.52 us                                                      | 2.80 us: 1.11x slower                                                        |
| regex_effbot               | 3.34 ms                                                      | 3.72 ms: 1.11x slower                                                        |
| pickle_list                | 3.94 us                                                      | 4.46 us: 1.13x slower                                                        |
| python_startup_no_site     | 7.73 ms                                                      | 8.84 ms: 1.14x slower                                                        |
| async_generators           | 322 ms                                                       | 370 ms: 1.15x slower                                                         |
| unpickle                   | 13.3 us                                                      | 15.7 us: 1.19x slower                                                        |
| flaskblogging              | 3.88 ms                                                      | 4.66 ms: 1.20x slower                                                        |
| python_startup             | 10.7 ms                                                      | 13.2 ms: 1.23x slower                                                        |
| telco                      | 6.81 ms                                                      | 8.41 ms: 1.24x slower                                                        |
| coverage                   | 66.1 ms                                                      | 84.1 ms: 1.27x slower                                                        |
| create_gc_cycles           | 1.58 ms                                                      | 2.04 ms: 1.29x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.07x faster                                                                 |

Benchmark hidden because not significant (6): django_template, dulwich_log, sqlglot_optimize, asyncio_websockets, mypy2, bench_mp_pool
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.69% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x