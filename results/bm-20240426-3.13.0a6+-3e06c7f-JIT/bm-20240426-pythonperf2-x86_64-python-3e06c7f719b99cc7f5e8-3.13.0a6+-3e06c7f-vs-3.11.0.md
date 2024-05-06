# Results vs. 3.11.0

- fork: python
- ref: 3e06c7f719b99cc7f5e8
- machine: linux-x86_64
- commit hash: 3e06c7f
- commit date: 2024-04-26
- overall geometric mean: 1.05x faster
- HPT reliability: 90.72%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 304 ms: 1.06x slower                                                         |
| chameleon      | 7.92 ms                                                      | 7.58 ms: 1.04x faster                                                        |
| docutils       | 2.85 sec                                                     | 3.10 sec: 1.09x slower                                                       |
| html5lib       | 72.2 ms                                                      | 74.0 ms: 1.02x slower                                                        |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 424 ms: 1.41x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 343 ms: 1.38x faster                                                         |
| async_tree_none            | 518 ms                                                       | 376 ms: 1.38x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 472 ms: 1.33x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 881 ms: 1.31x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 909 ms: 1.29x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 595 ms: 1.26x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 622 ms: 1.21x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.32x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 74.9 ms                                                      | 76.2 ms: 1.02x slower                                                        |
| pidigits       | 251 ms                                                       | 261 ms: 1.04x slower                                                         |
| nbody          | 92.9 ms                                                      | 99.1 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                        | 1.04x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 143 ms: 1.09x faster                                                         |
| regex_v8       | 24.4 ms                                                      | 24.9 ms: 1.02x slower                                                        |
| regex_effbot   | 3.34 ms                                                      | 3.44 ms: 1.03x slower                                                        |
| regex_dna      | 227 ms                                                       | 240 ms: 1.06x slower                                                         |
| Geometric mean | (ref)                                                        | 1.00x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                        |
| json_loads           | 28.9 us                                                      | 24.9 us: 1.16x faster                                                        |
| xml_etree_parse      | 155 ms                                                       | 143 ms: 1.08x faster                                                         |
| unpickle_pure_python | 238 us                                                       | 223 us: 1.07x faster                                                         |
| tomli_loads          | 2.25 sec                                                     | 2.12 sec: 1.06x faster                                                       |
| xml_etree_iterparse  | 107 ms                                                       | 101 ms: 1.05x faster                                                         |
| pickle_dict          | 32.3 us                                                      | 30.8 us: 1.05x faster                                                        |
| pickle_pure_python   | 316 us                                                       | 312 us: 1.01x faster                                                         |
| unpickle_list        | 4.60 us                                                      | 4.64 us: 1.01x slower                                                        |
| pickle               | 9.89 us                                                      | 10.3 us: 1.04x slower                                                        |
| xml_etree_process    | 55.9 ms                                                      | 58.6 ms: 1.05x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 83.6 ms: 1.05x slower                                                        |
| unpickle             | 13.3 us                                                      | 15.1 us: 1.14x slower                                                        |
| pickle_list          | 3.94 us                                                      | 4.50 us: 1.14x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 9.44 ms: 1.22x slower                                                        |
| python_startup         | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.24x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 9.84 ms: 1.12x faster                                                        |
| django_template | 39.3 ms                                                      | 41.4 ms: 1.05x slower                                                        |
| genshi_xml      | 57.1 ms                                                      | 63.1 ms: 1.11x slower                                                        |
| genshi_text     | 25.5 ms                                                      | 29.7 ms: 1.17x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.05x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-python-3e06c7f719b99cc7f5e8-3.13.0a6+-3e06c7f |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 186 us: 2.85x faster                                                         |
| asyncio_tcp                | 747 ms                                                       | 376 ms: 1.99x faster                                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                       |
| generators                 | 54.6 ms                                                      | 34.3 ms: 1.59x faster                                                        |
| async_tree_memoization_tg  | 600 ms                                                       | 424 ms: 1.41x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 343 ms: 1.38x faster                                                         |
| pylint                     | 514 ms                                                       | 373 ms: 1.38x faster                                                         |
| async_tree_none            | 518 ms                                                       | 376 ms: 1.38x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 472 ms: 1.33x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 881 ms: 1.31x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 909 ms: 1.29x faster                                                         |
| comprehensions             | 25.1 us                                                      | 19.6 us: 1.28x faster                                                        |
| coroutines                 | 27.8 ms                                                      | 21.9 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 595 ms: 1.26x faster                                                         |
| json_dumps                 | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 622 ms: 1.21x faster                                                         |
| richards_super             | 63.6 ms                                                      | 52.8 ms: 1.20x faster                                                        |
| json_loads                 | 28.9 us                                                      | 24.9 us: 1.16x faster                                                        |
| chaos                      | 74.9 ms                                                      | 65.5 ms: 1.14x faster                                                        |
| logging_simple             | 7.24 us                                                      | 6.42 us: 1.13x faster                                                        |
| raytrace                   | 309 ms                                                       | 275 ms: 1.13x faster                                                         |
| sympy_sum                  | 186 ms                                                       | 165 ms: 1.12x faster                                                         |
| mako                       | 11.0 ms                                                      | 9.84 ms: 1.12x faster                                                        |
| fannkuch                   | 416 ms                                                       | 377 ms: 1.10x faster                                                         |
| logging_format             | 7.71 us                                                      | 7.00 us: 1.10x faster                                                        |
| regex_compile              | 156 ms                                                       | 143 ms: 1.09x faster                                                         |
| xml_etree_parse            | 155 ms                                                       | 143 ms: 1.08x faster                                                         |
| pathlib                    | 18.9 ms                                                      | 17.5 ms: 1.08x faster                                                        |
| sympy_str                  | 337 ms                                                       | 313 ms: 1.08x faster                                                         |
| mdp                        | 2.77 sec                                                     | 2.58 sec: 1.07x faster                                                       |
| unpickle_pure_python       | 238 us                                                       | 223 us: 1.07x faster                                                         |
| crypto_pyaes               | 83.3 ms                                                      | 77.8 ms: 1.07x faster                                                        |
| sqlglot_parse              | 1.51 ms                                                      | 1.42 ms: 1.07x faster                                                        |
| richards                   | 49.7 ms                                                      | 46.6 ms: 1.07x faster                                                        |
| tomli_loads                | 2.25 sec                                                     | 2.12 sec: 1.06x faster                                                       |
| logging_silent             | 100 ns                                                       | 94.8 ns: 1.06x faster                                                        |
| xml_etree_iterparse        | 107 ms                                                       | 101 ms: 1.05x faster                                                         |
| pickle_dict                | 32.3 us                                                      | 30.8 us: 1.05x faster                                                        |
| bench_thread_pool          | 1.00 ms                                                      | 955 us: 1.05x faster                                                         |
| sqlglot_transpile          | 1.91 ms                                                      | 1.82 ms: 1.05x faster                                                        |
| chameleon                  | 7.92 ms                                                      | 7.58 ms: 1.04x faster                                                        |
| sympy_expand               | 553 ms                                                       | 531 ms: 1.04x faster                                                         |
| json                       | 5.58 ms                                                      | 5.36 ms: 1.04x faster                                                        |
| deltablue                  | 3.97 ms                                                      | 3.83 ms: 1.04x faster                                                        |
| spectral_norm              | 95.1 ms                                                      | 92.8 ms: 1.02x faster                                                        |
| pycparser                  | 1.31 sec                                                     | 1.28 sec: 1.02x faster                                                       |
| nqueens                    | 103 ms                                                       | 101 ms: 1.02x faster                                                         |
| thrift                     | 931 us                                                       | 918 us: 1.01x faster                                                         |
| pickle_pure_python         | 316 us                                                       | 312 us: 1.01x faster                                                         |
| scimark_lu                 | 114 ms                                                       | 113 ms: 1.01x faster                                                         |
| sympy_integrate            | 25.8 ms                                                      | 25.7 ms: 1.01x faster                                                        |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.08 ms: 1.00x slower                                                        |
| unpickle_list              | 4.60 us                                                      | 4.64 us: 1.01x slower                                                        |
| scimark_monte_carlo        | 69.8 ms                                                      | 70.5 ms: 1.01x slower                                                        |
| float                      | 74.9 ms                                                      | 76.2 ms: 1.02x slower                                                        |
| regex_v8                   | 24.4 ms                                                      | 24.9 ms: 1.02x slower                                                        |
| pprint_pformat             | 1.67 sec                                                     | 1.70 sec: 1.02x slower                                                       |
| html5lib                   | 72.2 ms                                                      | 74.0 ms: 1.02x slower                                                        |
| deepcopy_reduce            | 3.40 us                                                      | 3.48 us: 1.03x slower                                                        |
| meteor_contest             | 131 ms                                                       | 134 ms: 1.03x slower                                                         |
| deepcopy_memo              | 37.5 us                                                      | 38.6 us: 1.03x slower                                                        |
| asyncio_websockets         | 390 ms                                                       | 401 ms: 1.03x slower                                                         |
| regex_effbot               | 3.34 ms                                                      | 3.44 ms: 1.03x slower                                                        |
| pprint_safe_repr           | 805 ms                                                       | 830 ms: 1.03x slower                                                         |
| pickle                     | 9.89 us                                                      | 10.3 us: 1.04x slower                                                        |
| pidigits                   | 251 ms                                                       | 261 ms: 1.04x slower                                                         |
| deepcopy                   | 391 us                                                       | 408 us: 1.04x slower                                                         |
| bench_mp_pool              | 4.70 ms                                                      | 4.91 ms: 1.05x slower                                                        |
| gc_traversal               | 4.15 ms                                                      | 4.34 ms: 1.05x slower                                                        |
| hexiom                     | 6.98 ms                                                      | 7.31 ms: 1.05x slower                                                        |
| xml_etree_process          | 55.9 ms                                                      | 58.6 ms: 1.05x slower                                                        |
| xml_etree_generate         | 79.7 ms                                                      | 83.6 ms: 1.05x slower                                                        |
| sqlglot_normalize          | 122 ms                                                       | 128 ms: 1.05x slower                                                         |
| django_template            | 39.3 ms                                                      | 41.4 ms: 1.05x slower                                                        |
| regex_dna                  | 227 ms                                                       | 240 ms: 1.06x slower                                                         |
| sqlite_synth               | 2.52 us                                                      | 2.67 us: 1.06x slower                                                        |
| 2to3                       | 287 ms                                                       | 304 ms: 1.06x slower                                                         |
| pyflate                    | 449 ms                                                       | 479 ms: 1.07x slower                                                         |
| nbody                      | 92.9 ms                                                      | 99.1 ms: 1.07x slower                                                        |
| docutils                   | 2.85 sec                                                     | 3.10 sec: 1.09x slower                                                       |
| sqlglot_optimize           | 59.0 ms                                                      | 64.7 ms: 1.10x slower                                                        |
| go                         | 158 ms                                                       | 174 ms: 1.10x slower                                                         |
| scimark_fft                | 281 ms                                                       | 309 ms: 1.10x slower                                                         |
| genshi_xml                 | 57.1 ms                                                      | 63.1 ms: 1.11x slower                                                        |
| mypy2                      | 762 ms                                                       | 855 ms: 1.12x slower                                                         |
| unpickle                   | 13.3 us                                                      | 15.1 us: 1.14x slower                                                        |
| pickle_list                | 3.94 us                                                      | 4.50 us: 1.14x slower                                                        |
| aiohttp                    | 986 us                                                       | 1.13 ms: 1.15x slower                                                        |
| gunicorn                   | 966 us                                                       | 1.11 ms: 1.15x slower                                                        |
| genshi_text                | 25.5 ms                                                      | 29.7 ms: 1.17x slower                                                        |
| telco                      | 6.81 ms                                                      | 8.00 ms: 1.17x slower                                                        |
| coverage                   | 66.1 ms                                                      | 78.0 ms: 1.18x slower                                                        |
| async_generators           | 322 ms                                                       | 382 ms: 1.19x slower                                                         |
| create_gc_cycles           | 1.58 ms                                                      | 1.90 ms: 1.21x slower                                                        |
| python_startup_no_site     | 7.73 ms                                                      | 9.44 ms: 1.22x slower                                                        |
| python_startup             | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                                        |
| scimark_sor                | 110 ms                                                       | 151 ms: 1.38x slower                                                         |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                                 |

Benchmark hidden because not significant (3): dask, dulwich_log, tornado_http
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 90.72% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x