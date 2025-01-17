# Results vs. 3.11.0

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: linux-x86_64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.04x faster
- HPT reliability: 72.84%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 300 ms: 1.05x slower                                                         |
| chameleon      | 7.92 ms                                                      | 7.58 ms: 1.05x faster                                                        |
| docutils       | 2.85 sec                                                     | 3.08 sec: 1.08x slower                                                       |
| html5lib       | 72.2 ms                                                      | 74.4 ms: 1.03x slower                                                        |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 518 ms                                                       | 358 ms: 1.45x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 440 ms: 1.43x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 338 ms: 1.41x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 435 ms: 1.38x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 882 ms: 1.33x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 577 ms: 1.30x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 904 ms: 1.28x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 592 ms: 1.27x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.35x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 94.9 ms: 1.02x slower                                                        |
| pidigits       | 251 ms                                                       | 261 ms: 1.04x slower                                                         |
| float          | 74.9 ms                                                      | 78.5 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                        | 1.04x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 148 ms: 1.05x faster                                                         |
| regex_v8       | 24.4 ms                                                      | 25.6 ms: 1.05x slower                                                        |
| regex_dna      | 227 ms                                                       | 242 ms: 1.07x slower                                                         |
| regex_effbot   | 3.34 ms                                                      | 3.70 ms: 1.11x slower                                                        |
| Geometric mean | (ref)                                                        | 1.04x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.5 ms: 1.26x faster                                                        |
| json_loads           | 28.9 us                                                      | 25.3 us: 1.14x faster                                                        |
| xml_etree_parse      | 155 ms                                                       | 143 ms: 1.08x faster                                                         |
| xml_etree_iterparse  | 107 ms                                                       | 102 ms: 1.04x faster                                                         |
| tomli_loads          | 2.25 sec                                                     | 2.17 sec: 1.04x faster                                                       |
| pickle_pure_python   | 316 us                                                       | 311 us: 1.02x faster                                                         |
| unpickle_pure_python | 238 us                                                       | 235 us: 1.01x faster                                                         |
| pickle_dict          | 32.3 us                                                      | 33.1 us: 1.03x slower                                                        |
| xml_etree_process    | 55.9 ms                                                      | 58.3 ms: 1.04x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 84.1 ms: 1.05x slower                                                        |
| pickle               | 9.89 us                                                      | 10.9 us: 1.10x slower                                                        |
| pickle_list          | 3.94 us                                                      | 4.42 us: 1.12x slower                                                        |
| unpickle             | 13.3 us                                                      | 15.2 us: 1.14x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                                 |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 13.6 ms: 1.26x slower                                                        |
| python_startup_no_site | 7.73 ms                                                      | 11.8 ms: 1.53x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.39x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 10.0 ms: 1.10x faster                                                        |
| django_template | 39.3 ms                                                      | 40.1 ms: 1.02x slower                                                        |
| genshi_xml      | 57.1 ms                                                      | 59.4 ms: 1.04x slower                                                        |
| genshi_text     | 25.5 ms                                                      | 27.4 ms: 1.08x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 128 us: 4.17x faster                                                         |
| asyncio_tcp                | 747 ms                                                       | 371 ms: 2.01x faster                                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                       |
| generators                 | 54.6 ms                                                      | 33.6 ms: 1.62x faster                                                        |
| pylint                     | 514 ms                                                       | 339 ms: 1.52x faster                                                         |
| async_tree_none            | 518 ms                                                       | 358 ms: 1.45x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 440 ms: 1.43x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 338 ms: 1.41x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 435 ms: 1.38x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 882 ms: 1.33x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 577 ms: 1.30x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 904 ms: 1.28x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 592 ms: 1.27x faster                                                         |
| json_dumps                 | 13.3 ms                                                      | 10.5 ms: 1.26x faster                                                        |
| comprehensions             | 25.1 us                                                      | 20.1 us: 1.25x faster                                                        |
| coroutines                 | 27.8 ms                                                      | 22.7 ms: 1.22x faster                                                        |
| sympy_sum                  | 186 ms                                                       | 161 ms: 1.15x faster                                                         |
| json_loads                 | 28.9 us                                                      | 25.3 us: 1.14x faster                                                        |
| sympy_str                  | 337 ms                                                       | 304 ms: 1.11x faster                                                         |
| chaos                      | 74.9 ms                                                      | 67.9 ms: 1.10x faster                                                        |
| mako                       | 11.0 ms                                                      | 10.0 ms: 1.10x faster                                                        |
| fannkuch                   | 416 ms                                                       | 379 ms: 1.10x faster                                                         |
| logging_simple             | 7.24 us                                                      | 6.61 us: 1.10x faster                                                        |
| richards_super             | 63.6 ms                                                      | 58.4 ms: 1.09x faster                                                        |
| crypto_pyaes               | 83.3 ms                                                      | 77.1 ms: 1.08x faster                                                        |
| xml_etree_parse            | 155 ms                                                       | 143 ms: 1.08x faster                                                         |
| sympy_expand               | 553 ms                                                       | 513 ms: 1.08x faster                                                         |
| logging_format             | 7.71 us                                                      | 7.24 us: 1.06x faster                                                        |
| thrift                     | 931 us                                                       | 878 us: 1.06x faster                                                         |
| sqlglot_parse              | 1.51 ms                                                      | 1.43 ms: 1.06x faster                                                        |
| mdp                        | 2.77 sec                                                     | 2.62 sec: 1.06x faster                                                       |
| deltablue                  | 3.97 ms                                                      | 3.75 ms: 1.06x faster                                                        |
| regex_compile              | 156 ms                                                       | 148 ms: 1.05x faster                                                         |
| chameleon                  | 7.92 ms                                                      | 7.58 ms: 1.05x faster                                                        |
| xml_etree_iterparse        | 107 ms                                                       | 102 ms: 1.04x faster                                                         |
| sqlglot_transpile          | 1.91 ms                                                      | 1.83 ms: 1.04x faster                                                        |
| tomli_loads                | 2.25 sec                                                     | 2.17 sec: 1.04x faster                                                       |
| pycparser                  | 1.31 sec                                                     | 1.26 sec: 1.03x faster                                                       |
| json                       | 5.58 ms                                                      | 5.44 ms: 1.03x faster                                                        |
| logging_silent             | 100 ns                                                       | 98.3 ns: 1.02x faster                                                        |
| dask                       | 410 ms                                                       | 402 ms: 1.02x faster                                                         |
| sympy_integrate            | 25.8 ms                                                      | 25.3 ms: 1.02x faster                                                        |
| spectral_norm              | 95.1 ms                                                      | 93.2 ms: 1.02x faster                                                        |
| raytrace                   | 309 ms                                                       | 304 ms: 1.02x faster                                                         |
| pickle_pure_python         | 316 us                                                       | 311 us: 1.02x faster                                                         |
| unpickle_pure_python       | 238 us                                                       | 235 us: 1.01x faster                                                         |
| asyncio_websockets         | 390 ms                                                       | 387 ms: 1.01x faster                                                         |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.11 ms: 1.01x slower                                                        |
| deepcopy                   | 391 us                                                       | 398 us: 1.02x slower                                                         |
| django_template            | 39.3 ms                                                      | 40.1 ms: 1.02x slower                                                        |
| nbody                      | 92.9 ms                                                      | 94.9 ms: 1.02x slower                                                        |
| pickle_dict                | 32.3 us                                                      | 33.1 us: 1.03x slower                                                        |
| deepcopy_reduce            | 3.40 us                                                      | 3.48 us: 1.03x slower                                                        |
| dulwich_log                | 67.4 ms                                                      | 69.2 ms: 1.03x slower                                                        |
| sqlglot_normalize          | 122 ms                                                       | 125 ms: 1.03x slower                                                         |
| pprint_pformat             | 1.67 sec                                                     | 1.71 sec: 1.03x slower                                                       |
| meteor_contest             | 131 ms                                                       | 134 ms: 1.03x slower                                                         |
| html5lib                   | 72.2 ms                                                      | 74.4 ms: 1.03x slower                                                        |
| richards                   | 49.7 ms                                                      | 51.3 ms: 1.03x slower                                                        |
| pidigits                   | 251 ms                                                       | 261 ms: 1.04x slower                                                         |
| pprint_safe_repr           | 805 ms                                                       | 836 ms: 1.04x slower                                                         |
| genshi_xml                 | 57.1 ms                                                      | 59.4 ms: 1.04x slower                                                        |
| pathlib                    | 18.9 ms                                                      | 19.8 ms: 1.04x slower                                                        |
| xml_etree_process          | 55.9 ms                                                      | 58.3 ms: 1.04x slower                                                        |
| scimark_monte_carlo        | 69.8 ms                                                      | 72.9 ms: 1.04x slower                                                        |
| 2to3                       | 287 ms                                                       | 300 ms: 1.05x slower                                                         |
| float                      | 74.9 ms                                                      | 78.5 ms: 1.05x slower                                                        |
| regex_v8                   | 24.4 ms                                                      | 25.6 ms: 1.05x slower                                                        |
| xml_etree_generate         | 79.7 ms                                                      | 84.1 ms: 1.05x slower                                                        |
| bench_mp_pool              | 4.70 ms                                                      | 4.97 ms: 1.06x slower                                                        |
| deepcopy_memo              | 37.5 us                                                      | 39.9 us: 1.06x slower                                                        |
| regex_dna                  | 227 ms                                                       | 242 ms: 1.07x slower                                                         |
| sqlite_synth               | 2.52 us                                                      | 2.70 us: 1.07x slower                                                        |
| sqlglot_optimize           | 59.0 ms                                                      | 63.1 ms: 1.07x slower                                                        |
| genshi_text                | 25.5 ms                                                      | 27.4 ms: 1.08x slower                                                        |
| docutils                   | 2.85 sec                                                     | 3.08 sec: 1.08x slower                                                       |
| hexiom                     | 6.98 ms                                                      | 7.59 ms: 1.09x slower                                                        |
| mypy2                      | 762 ms                                                       | 830 ms: 1.09x slower                                                         |
| pickle                     | 9.89 us                                                      | 10.9 us: 1.10x slower                                                        |
| gc_traversal               | 4.15 ms                                                      | 4.57 ms: 1.10x slower                                                        |
| regex_effbot               | 3.34 ms                                                      | 3.70 ms: 1.11x slower                                                        |
| scimark_lu                 | 114 ms                                                       | 127 ms: 1.11x slower                                                         |
| go                         | 158 ms                                                       | 175 ms: 1.11x slower                                                         |
| pickle_list                | 3.94 us                                                      | 4.42 us: 1.12x slower                                                        |
| gunicorn                   | 966 us                                                       | 1.09 ms: 1.13x slower                                                        |
| bench_thread_pool          | 1.00 ms                                                      | 1.13 ms: 1.13x slower                                                        |
| scimark_fft                | 281 ms                                                       | 318 ms: 1.13x slower                                                         |
| aiohttp                    | 986 us                                                       | 1.12 ms: 1.14x slower                                                        |
| create_gc_cycles           | 1.58 ms                                                      | 1.80 ms: 1.14x slower                                                        |
| pyflate                    | 449 ms                                                       | 514 ms: 1.14x slower                                                         |
| unpickle                   | 13.3 us                                                      | 15.2 us: 1.14x slower                                                        |
| telco                      | 6.81 ms                                                      | 8.00 ms: 1.17x slower                                                        |
| async_generators           | 322 ms                                                       | 395 ms: 1.23x slower                                                         |
| coverage                   | 66.1 ms                                                      | 82.4 ms: 1.25x slower                                                        |
| python_startup             | 10.7 ms                                                      | 13.6 ms: 1.26x slower                                                        |
| unpack_sequence            | 45.7 ns                                                      | 58.9 ns: 1.29x slower                                                        |
| scimark_sor                | 110 ms                                                       | 154 ms: 1.40x slower                                                         |
| python_startup_no_site     | 7.73 ms                                                      | 11.8 ms: 1.53x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.04x faster                                                                 |

Benchmark hidden because not significant (3): tornado_http, nqueens, unpickle_list
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 72.84% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x