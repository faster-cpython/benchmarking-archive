# Results vs. 3.11.0

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: linux-x86_64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.08x faster
- HPT reliability: 99.95%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 292 ms: 1.02x slower                                                         |
| chameleon      | 7.92 ms                                                      | 7.19 ms: 1.10x faster                                                        |
| docutils       | 2.85 sec                                                     | 2.95 sec: 1.04x slower                                                       |
| html5lib       | 72.2 ms                                                      | 74.0 ms: 1.02x slower                                                        |
| tornado_http   | 124 ms                                                       | 121 ms: 1.03x faster                                                         |
| Geometric mean | (ref)                                                        | 1.01x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 427 ms: 1.41x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 339 ms: 1.40x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 451 ms: 1.39x faster                                                         |
| async_tree_none            | 518 ms                                                       | 376 ms: 1.38x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 854 ms: 1.35x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 893 ms: 1.31x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 586 ms: 1.28x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 594 ms: 1.27x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.35x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 87.5 ms: 1.06x faster                                                        |
| float          | 74.9 ms                                                      | 76.5 ms: 1.02x slower                                                        |
| pidigits       | 251 ms                                                       | 263 ms: 1.05x slower                                                         |
| Geometric mean | (ref)                                                        | 1.00x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 142 ms: 1.10x faster                                                         |
| regex_v8       | 24.4 ms                                                      | 25.7 ms: 1.05x slower                                                        |
| regex_effbot   | 3.34 ms                                                      | 3.55 ms: 1.06x slower                                                        |
| regex_dna      | 227 ms                                                       | 249 ms: 1.09x slower                                                         |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.5 ms: 1.26x faster                                                        |
| json_loads           | 28.9 us                                                      | 25.5 us: 1.14x faster                                                        |
| unpickle_pure_python | 238 us                                                       | 213 us: 1.12x faster                                                         |
| xml_etree_parse      | 155 ms                                                       | 143 ms: 1.08x faster                                                         |
| xml_etree_iterparse  | 107 ms                                                       | 102 ms: 1.04x faster                                                         |
| pickle_pure_python   | 316 us                                                       | 306 us: 1.03x faster                                                         |
| tomli_loads          | 2.25 sec                                                     | 2.30 sec: 1.02x slower                                                       |
| pickle_dict          | 32.3 us                                                      | 33.7 us: 1.04x slower                                                        |
| xml_etree_process    | 55.9 ms                                                      | 58.4 ms: 1.04x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 84.2 ms: 1.06x slower                                                        |
| pickle               | 9.89 us                                                      | 10.5 us: 1.07x slower                                                        |
| unpickle             | 13.3 us                                                      | 14.7 us: 1.11x slower                                                        |
| pickle_list          | 3.94 us                                                      | 4.47 us: 1.13x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 12.8 ms: 1.20x slower                                                        |
| python_startup_no_site | 7.73 ms                                                      | 11.1 ms: 1.43x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.31x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 10.2 ms: 1.08x faster                                                        |
| genshi_xml      | 57.1 ms                                                      | 53.8 ms: 1.06x faster                                                        |
| genshi_text     | 25.5 ms                                                      | 24.8 ms: 1.03x faster                                                        |
| django_template | 39.3 ms                                                      | 38.5 ms: 1.02x faster                                                        |
| Geometric mean  | (ref)                                                        | 1.05x faster                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 115 us: 4.62x faster                                                         |
| asyncio_tcp                | 747 ms                                                       | 371 ms: 2.02x faster                                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.57 sec: 1.95x faster                                                       |
| generators                 | 54.6 ms                                                      | 33.4 ms: 1.63x faster                                                        |
| pylint                     | 514 ms                                                       | 320 ms: 1.61x faster                                                         |
| comprehensions             | 25.1 us                                                      | 16.9 us: 1.49x faster                                                        |
| async_tree_memoization_tg  | 600 ms                                                       | 427 ms: 1.41x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 339 ms: 1.40x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 451 ms: 1.39x faster                                                         |
| async_tree_none            | 518 ms                                                       | 376 ms: 1.38x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 854 ms: 1.35x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 893 ms: 1.31x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 586 ms: 1.28x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 594 ms: 1.27x faster                                                         |
| json_dumps                 | 13.3 ms                                                      | 10.5 ms: 1.26x faster                                                        |
| chaos                      | 74.9 ms                                                      | 60.0 ms: 1.25x faster                                                        |
| coroutines                 | 27.8 ms                                                      | 22.4 ms: 1.24x faster                                                        |
| sympy_sum                  | 186 ms                                                       | 151 ms: 1.23x faster                                                         |
| scimark_lu                 | 114 ms                                                       | 95.6 ms: 1.19x faster                                                        |
| raytrace                   | 309 ms                                                       | 261 ms: 1.18x faster                                                         |
| nqueens                    | 103 ms                                                       | 87.7 ms: 1.17x faster                                                        |
| sympy_str                  | 337 ms                                                       | 290 ms: 1.16x faster                                                         |
| crypto_pyaes               | 83.3 ms                                                      | 71.7 ms: 1.16x faster                                                        |
| json_loads                 | 28.9 us                                                      | 25.5 us: 1.14x faster                                                        |
| unpickle_pure_python       | 238 us                                                       | 213 us: 1.12x faster                                                         |
| sympy_expand               | 553 ms                                                       | 495 ms: 1.12x faster                                                         |
| sympy_integrate            | 25.8 ms                                                      | 23.2 ms: 1.11x faster                                                        |
| deltablue                  | 3.97 ms                                                      | 3.57 ms: 1.11x faster                                                        |
| logging_simple             | 7.24 us                                                      | 6.53 us: 1.11x faster                                                        |
| bench_thread_pool          | 1.00 ms                                                      | 904 us: 1.11x faster                                                         |
| sqlglot_parse              | 1.51 ms                                                      | 1.37 ms: 1.10x faster                                                        |
| chameleon                  | 7.92 ms                                                      | 7.19 ms: 1.10x faster                                                        |
| mdp                        | 2.77 sec                                                     | 2.52 sec: 1.10x faster                                                       |
| regex_compile              | 156 ms                                                       | 142 ms: 1.10x faster                                                         |
| sqlglot_transpile          | 1.91 ms                                                      | 1.75 ms: 1.09x faster                                                        |
| hexiom                     | 6.98 ms                                                      | 6.41 ms: 1.09x faster                                                        |
| fannkuch                   | 416 ms                                                       | 382 ms: 1.09x faster                                                         |
| logging_format             | 7.71 us                                                      | 7.12 us: 1.08x faster                                                        |
| mako                       | 11.0 ms                                                      | 10.2 ms: 1.08x faster                                                        |
| xml_etree_parse            | 155 ms                                                       | 143 ms: 1.08x faster                                                         |
| thrift                     | 931 us                                                       | 865 us: 1.08x faster                                                         |
| scimark_monte_carlo        | 69.8 ms                                                      | 64.9 ms: 1.08x faster                                                        |
| richards_super             | 63.6 ms                                                      | 59.3 ms: 1.07x faster                                                        |
| nbody                      | 92.9 ms                                                      | 87.5 ms: 1.06x faster                                                        |
| genshi_xml                 | 57.1 ms                                                      | 53.8 ms: 1.06x faster                                                        |
| json                       | 5.58 ms                                                      | 5.33 ms: 1.05x faster                                                        |
| dask                       | 410 ms                                                       | 393 ms: 1.04x faster                                                         |
| xml_etree_iterparse        | 107 ms                                                       | 102 ms: 1.04x faster                                                         |
| sqlglot_normalize          | 122 ms                                                       | 117 ms: 1.04x faster                                                         |
| logging_silent             | 100 ns                                                       | 96.2 ns: 1.04x faster                                                        |
| pprint_pformat             | 1.67 sec                                                     | 1.60 sec: 1.04x faster                                                       |
| meteor_contest             | 131 ms                                                       | 126 ms: 1.03x faster                                                         |
| pickle_pure_python         | 316 us                                                       | 306 us: 1.03x faster                                                         |
| genshi_text                | 25.5 ms                                                      | 24.8 ms: 1.03x faster                                                        |
| deepcopy                   | 391 us                                                       | 381 us: 1.03x faster                                                         |
| tornado_http               | 124 ms                                                       | 121 ms: 1.03x faster                                                         |
| pprint_safe_repr           | 805 ms                                                       | 785 ms: 1.03x faster                                                         |
| spectral_norm              | 95.1 ms                                                      | 92.7 ms: 1.03x faster                                                        |
| deepcopy_memo              | 37.5 us                                                      | 36.7 us: 1.02x faster                                                        |
| django_template            | 39.3 ms                                                      | 38.5 ms: 1.02x faster                                                        |
| pycparser                  | 1.31 sec                                                     | 1.29 sec: 1.02x faster                                                       |
| sqlglot_optimize           | 59.0 ms                                                      | 58.4 ms: 1.01x faster                                                        |
| deepcopy_reduce            | 3.40 us                                                      | 3.37 us: 1.01x faster                                                        |
| dulwich_log                | 67.4 ms                                                      | 68.7 ms: 1.02x slower                                                        |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.14 ms: 1.02x slower                                                        |
| 2to3                       | 287 ms                                                       | 292 ms: 1.02x slower                                                         |
| float                      | 74.9 ms                                                      | 76.5 ms: 1.02x slower                                                        |
| tomli_loads                | 2.25 sec                                                     | 2.30 sec: 1.02x slower                                                       |
| html5lib                   | 72.2 ms                                                      | 74.0 ms: 1.02x slower                                                        |
| pathlib                    | 18.9 ms                                                      | 19.4 ms: 1.03x slower                                                        |
| docutils                   | 2.85 sec                                                     | 2.95 sec: 1.04x slower                                                       |
| pickle_dict                | 32.3 us                                                      | 33.7 us: 1.04x slower                                                        |
| xml_etree_process          | 55.9 ms                                                      | 58.4 ms: 1.04x slower                                                        |
| pidigits                   | 251 ms                                                       | 263 ms: 1.05x slower                                                         |
| regex_v8                   | 24.4 ms                                                      | 25.7 ms: 1.05x slower                                                        |
| scimark_fft                | 281 ms                                                       | 296 ms: 1.06x slower                                                         |
| xml_etree_generate         | 79.7 ms                                                      | 84.2 ms: 1.06x slower                                                        |
| aiohttp                    | 986 us                                                       | 1.05 ms: 1.06x slower                                                        |
| regex_effbot               | 3.34 ms                                                      | 3.55 ms: 1.06x slower                                                        |
| pickle                     | 9.89 us                                                      | 10.5 us: 1.07x slower                                                        |
| richards                   | 49.7 ms                                                      | 53.6 ms: 1.08x slower                                                        |
| gunicorn                   | 966 us                                                       | 1.05 ms: 1.08x slower                                                        |
| sqlite_synth               | 2.52 us                                                      | 2.74 us: 1.09x slower                                                        |
| go                         | 158 ms                                                       | 172 ms: 1.09x slower                                                         |
| regex_dna                  | 227 ms                                                       | 249 ms: 1.09x slower                                                         |
| unpickle                   | 13.3 us                                                      | 14.7 us: 1.11x slower                                                        |
| async_generators           | 322 ms                                                       | 360 ms: 1.12x slower                                                         |
| gc_traversal               | 4.15 ms                                                      | 4.67 ms: 1.13x slower                                                        |
| pickle_list                | 3.94 us                                                      | 4.47 us: 1.13x slower                                                        |
| create_gc_cycles           | 1.58 ms                                                      | 1.81 ms: 1.14x slower                                                        |
| telco                      | 6.81 ms                                                      | 7.91 ms: 1.16x slower                                                        |
| pyflate                    | 449 ms                                                       | 535 ms: 1.19x slower                                                         |
| python_startup             | 10.7 ms                                                      | 12.8 ms: 1.20x slower                                                        |
| unpack_sequence            | 45.7 ns                                                      | 56.3 ns: 1.23x slower                                                        |
| coverage                   | 66.1 ms                                                      | 85.0 ms: 1.29x slower                                                        |
| scimark_sor                | 110 ms                                                       | 144 ms: 1.31x slower                                                         |
| python_startup_no_site     | 7.73 ms                                                      | 11.1 ms: 1.43x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.08x faster                                                                 |

Benchmark hidden because not significant (4): bench_mp_pool, asyncio_websockets, unpickle_list, mypy2
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.95% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.02x