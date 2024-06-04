# Results vs. 3.11.0

- fork: Fidget-Spinner
- ref: stackref_all
- machine: linux-x86_64
- commit hash: c73f8ac
- commit date: 2024-06-04
- overall geometric mean: 1.06x faster
- HPT reliability: 99.73%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-c73f8ac |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 308 ms: 1.07x slower                                                          |
| docutils       | 2.85 sec                                                     | 3.14 sec: 1.10x slower                                                        |
| html5lib       | 72.2 ms                                                      | 74.6 ms: 1.03x slower                                                         |
| tornado_http   | 124 ms                                                       | 123 ms: 1.01x faster                                                          |
| Geometric mean | (ref)                                                        | 1.05x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-c73f8ac |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 427 ms: 1.40x faster                                                          |
| async_tree_none            | 518 ms                                                       | 373 ms: 1.39x faster                                                          |
| async_tree_none_tg         | 474 ms                                                       | 343 ms: 1.38x faster                                                          |
| async_tree_memoization     | 629 ms                                                       | 474 ms: 1.33x faster                                                          |
| async_tree_io              | 1.17 sec                                                     | 883 ms: 1.33x faster                                                          |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 582 ms: 1.29x faster                                                          |
| async_tree_io_tg           | 1.15 sec                                                     | 897 ms: 1.29x faster                                                          |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 623 ms: 1.21x faster                                                          |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-c73f8ac |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 84.3 ms: 1.10x faster                                                         |
| Geometric mean | (ref)                                                        | 1.03x faster                                                                  |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-c73f8ac |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 141 ms: 1.11x faster                                                          |
| regex_effbot   | 3.34 ms                                                      | 3.43 ms: 1.03x slower                                                         |
| regex_v8       | 24.4 ms                                                      | 25.6 ms: 1.05x slower                                                         |
| regex_dna      | 227 ms                                                       | 245 ms: 1.08x slower                                                          |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-c73f8ac |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                         |
| json_loads           | 28.9 us                                                      | 25.4 us: 1.14x faster                                                         |
| xml_etree_parse      | 155 ms                                                       | 144 ms: 1.08x faster                                                          |
| tomli_loads          | 2.25 sec                                                     | 2.10 sec: 1.07x faster                                                        |
| xml_etree_iterparse  | 107 ms                                                       | 100 ms: 1.07x faster                                                          |
| unpickle_pure_python | 238 us                                                       | 224 us: 1.06x faster                                                          |
| pickle_dict          | 32.3 us                                                      | 31.6 us: 1.02x faster                                                         |
| xml_etree_generate   | 79.7 ms                                                      | 81.5 ms: 1.02x slower                                                         |
| unpickle_list        | 4.60 us                                                      | 4.73 us: 1.03x slower                                                         |
| pickle_pure_python   | 316 us                                                       | 326 us: 1.03x slower                                                          |
| xml_etree_process    | 55.9 ms                                                      | 58.3 ms: 1.04x slower                                                         |
| pickle               | 9.89 us                                                      | 10.5 us: 1.07x slower                                                         |
| pickle_list          | 3.94 us                                                      | 4.42 us: 1.12x slower                                                         |
| unpickle             | 13.3 us                                                      | 15.7 us: 1.18x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-c73f8ac |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 9.41 ms: 1.22x slower                                                         |
| python_startup         | 10.7 ms                                                      | 13.7 ms: 1.27x slower                                                         |
| Geometric mean         | (ref)                                                        | 1.24x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-c73f8ac |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 9.27 ms: 1.19x faster                                                         |
| django_template | 39.3 ms                                                      | 43.0 ms: 1.09x slower                                                         |
| genshi_text     | 25.5 ms                                                      | 28.8 ms: 1.13x slower                                                         |
| genshi_xml      | 57.1 ms                                                      | 67.0 ms: 1.17x slower                                                         |
| Geometric mean  | (ref)                                                        | 1.05x slower                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-c73f8ac |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 185 us: 2.87x faster                                                          |
| asyncio_tcp                | 747 ms                                                       | 381 ms: 1.96x faster                                                          |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                        |
| generators                 | 54.6 ms                                                      | 34.3 ms: 1.59x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 427 ms: 1.40x faster                                                          |
| async_tree_none            | 518 ms                                                       | 373 ms: 1.39x faster                                                          |
| async_tree_none_tg         | 474 ms                                                       | 343 ms: 1.38x faster                                                          |
| comprehensions             | 25.1 us                                                      | 18.4 us: 1.36x faster                                                         |
| pylint                     | 514 ms                                                       | 380 ms: 1.35x faster                                                          |
| async_tree_memoization     | 629 ms                                                       | 474 ms: 1.33x faster                                                          |
| async_tree_io              | 1.17 sec                                                     | 883 ms: 1.33x faster                                                          |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 582 ms: 1.29x faster                                                          |
| async_tree_io_tg           | 1.15 sec                                                     | 897 ms: 1.29x faster                                                          |
| coroutines                 | 27.8 ms                                                      | 22.0 ms: 1.26x faster                                                         |
| json_dumps                 | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 623 ms: 1.21x faster                                                          |
| richards_super             | 63.6 ms                                                      | 53.3 ms: 1.19x faster                                                         |
| mako                       | 11.0 ms                                                      | 9.27 ms: 1.19x faster                                                         |
| fannkuch                   | 416 ms                                                       | 355 ms: 1.17x faster                                                          |
| pathlib                    | 18.9 ms                                                      | 16.5 ms: 1.15x faster                                                         |
| crypto_pyaes               | 83.3 ms                                                      | 72.4 ms: 1.15x faster                                                         |
| spectral_norm              | 95.1 ms                                                      | 83.4 ms: 1.14x faster                                                         |
| json_loads                 | 28.9 us                                                      | 25.4 us: 1.14x faster                                                         |
| chaos                      | 74.9 ms                                                      | 66.0 ms: 1.14x faster                                                         |
| regex_compile              | 156 ms                                                       | 141 ms: 1.11x faster                                                          |
| sympy_sum                  | 186 ms                                                       | 168 ms: 1.11x faster                                                          |
| logging_simple             | 7.24 us                                                      | 6.55 us: 1.11x faster                                                         |
| nbody                      | 92.9 ms                                                      | 84.3 ms: 1.10x faster                                                         |
| richards                   | 49.7 ms                                                      | 45.7 ms: 1.09x faster                                                         |
| raytrace                   | 309 ms                                                       | 285 ms: 1.09x faster                                                          |
| logging_format             | 7.71 us                                                      | 7.12 us: 1.08x faster                                                         |
| xml_etree_parse            | 155 ms                                                       | 144 ms: 1.08x faster                                                          |
| tomli_loads                | 2.25 sec                                                     | 2.10 sec: 1.07x faster                                                        |
| mdp                        | 2.77 sec                                                     | 2.59 sec: 1.07x faster                                                        |
| sqlglot_parse              | 1.51 ms                                                      | 1.42 ms: 1.07x faster                                                         |
| xml_etree_iterparse        | 107 ms                                                       | 100 ms: 1.07x faster                                                          |
| sympy_str                  | 337 ms                                                       | 316 ms: 1.06x faster                                                          |
| unpickle_pure_python       | 238 us                                                       | 224 us: 1.06x faster                                                          |
| json                       | 5.58 ms                                                      | 5.31 ms: 1.05x faster                                                         |
| bench_thread_pool          | 1.00 ms                                                      | 959 us: 1.04x faster                                                          |
| sqlglot_transpile          | 1.91 ms                                                      | 1.84 ms: 1.04x faster                                                         |
| nqueens                    | 103 ms                                                       | 98.7 ms: 1.04x faster                                                         |
| deltablue                  | 3.97 ms                                                      | 3.82 ms: 1.04x faster                                                         |
| thrift                     | 931 us                                                       | 905 us: 1.03x faster                                                          |
| sympy_expand               | 553 ms                                                       | 538 ms: 1.03x faster                                                          |
| pycparser                  | 1.31 sec                                                     | 1.27 sec: 1.03x faster                                                        |
| pickle_dict                | 32.3 us                                                      | 31.6 us: 1.02x faster                                                         |
| pprint_pformat             | 1.67 sec                                                     | 1.63 sec: 1.02x faster                                                        |
| pprint_safe_repr           | 805 ms                                                       | 790 ms: 1.02x faster                                                          |
| dulwich_log                | 67.4 ms                                                      | 66.3 ms: 1.02x faster                                                         |
| tornado_http               | 124 ms                                                       | 123 ms: 1.01x faster                                                          |
| scimark_monte_carlo        | 69.8 ms                                                      | 69.1 ms: 1.01x faster                                                         |
| dask                       | 410 ms                                                       | 405 ms: 1.01x faster                                                          |
| meteor_contest             | 131 ms                                                       | 129 ms: 1.01x faster                                                          |
| pyflate                    | 449 ms                                                       | 454 ms: 1.01x slower                                                          |
| xml_etree_generate         | 79.7 ms                                                      | 81.5 ms: 1.02x slower                                                         |
| regex_effbot               | 3.34 ms                                                      | 3.43 ms: 1.03x slower                                                         |
| unpickle_list              | 4.60 us                                                      | 4.73 us: 1.03x slower                                                         |
| pickle_pure_python         | 316 us                                                       | 326 us: 1.03x slower                                                          |
| html5lib                   | 72.2 ms                                                      | 74.6 ms: 1.03x slower                                                         |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.20 ms: 1.03x slower                                                         |
| go                         | 158 ms                                                       | 163 ms: 1.04x slower                                                          |
| xml_etree_process          | 55.9 ms                                                      | 58.3 ms: 1.04x slower                                                         |
| regex_v8                   | 24.4 ms                                                      | 25.6 ms: 1.05x slower                                                         |
| scimark_fft                | 281 ms                                                       | 295 ms: 1.05x slower                                                          |
| sqlglot_normalize          | 122 ms                                                       | 129 ms: 1.06x slower                                                          |
| pickle                     | 9.89 us                                                      | 10.5 us: 1.07x slower                                                         |
| scimark_lu                 | 114 ms                                                       | 122 ms: 1.07x slower                                                          |
| 2to3                       | 287 ms                                                       | 308 ms: 1.07x slower                                                          |
| regex_dna                  | 227 ms                                                       | 245 ms: 1.08x slower                                                          |
| gc_traversal               | 4.15 ms                                                      | 4.47 ms: 1.08x slower                                                         |
| deepcopy                   | 391 us                                                       | 423 us: 1.08x slower                                                          |
| logging_silent             | 100 ns                                                       | 109 ns: 1.08x slower                                                          |
| sqlglot_optimize           | 59.0 ms                                                      | 64.2 ms: 1.09x slower                                                         |
| django_template            | 39.3 ms                                                      | 43.0 ms: 1.09x slower                                                         |
| deepcopy_reduce            | 3.40 us                                                      | 3.73 us: 1.10x slower                                                         |
| docutils                   | 2.85 sec                                                     | 3.14 sec: 1.10x slower                                                        |
| sqlite_synth               | 2.52 us                                                      | 2.78 us: 1.10x slower                                                         |
| pickle_list                | 3.94 us                                                      | 4.42 us: 1.12x slower                                                         |
| genshi_text                | 25.5 ms                                                      | 28.8 ms: 1.13x slower                                                         |
| genshi_xml                 | 57.1 ms                                                      | 67.0 ms: 1.17x slower                                                         |
| unpickle                   | 13.3 us                                                      | 15.7 us: 1.18x slower                                                         |
| create_gc_cycles           | 1.58 ms                                                      | 1.91 ms: 1.21x slower                                                         |
| telco                      | 6.81 ms                                                      | 8.27 ms: 1.22x slower                                                         |
| coverage                   | 66.1 ms                                                      | 80.3 ms: 1.22x slower                                                         |
| python_startup_no_site     | 7.73 ms                                                      | 9.41 ms: 1.22x slower                                                         |
| async_generators           | 322 ms                                                       | 392 ms: 1.22x slower                                                          |
| scimark_sor                | 110 ms                                                       | 134 ms: 1.22x slower                                                          |
| python_startup             | 10.7 ms                                                      | 13.7 ms: 1.27x slower                                                         |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                                  |

Benchmark hidden because not significant (7): hexiom, pidigits, asyncio_websockets, float, sympy_integrate, deepcopy_memo, bench_mp_pool
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.73% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x