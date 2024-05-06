# Results vs. 3.11.0

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: linux-x86_64
- commit hash: 4675ce8
- commit date: 2024-04-08
- overall geometric mean: 1.08x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 290 ms: 1.01x slower                                                                   |
| chameleon      | 7.92 ms                                                      | 7.24 ms: 1.09x faster                                                                  |
| docutils       | 2.85 sec                                                     | 2.98 sec: 1.05x slower                                                                 |
| html5lib       | 72.2 ms                                                      | 74.4 ms: 1.03x slower                                                                  |
| tornado_http   | 124 ms                                                       | 120 ms: 1.04x faster                                                                   |
| Geometric mean | (ref)                                                        | 1.01x faster                                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 417 ms: 1.44x faster                                                                   |
| async_tree_none_tg         | 474 ms                                                       | 337 ms: 1.41x faster                                                                   |
| async_tree_none            | 518 ms                                                       | 368 ms: 1.41x faster                                                                   |
| async_tree_memoization     | 629 ms                                                       | 462 ms: 1.36x faster                                                                   |
| async_tree_io_tg           | 1.15 sec                                                     | 880 ms: 1.31x faster                                                                   |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 573 ms: 1.31x faster                                                                   |
| async_tree_io              | 1.17 sec                                                     | 902 ms: 1.30x faster                                                                   |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 610 ms: 1.23x faster                                                                   |
| Geometric mean             | (ref)                                                        | 1.34x faster                                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 85.5 ms: 1.09x faster                                                                  |
| float          | 74.9 ms                                                      | 75.4 ms: 1.01x slower                                                                  |
| pidigits       | 251 ms                                                       | 262 ms: 1.04x slower                                                                   |
| Geometric mean | (ref)                                                        | 1.01x faster                                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 143 ms: 1.09x faster                                                                   |
| regex_v8       | 24.4 ms                                                      | 25.4 ms: 1.04x slower                                                                  |
| regex_effbot   | 3.34 ms                                                      | 3.57 ms: 1.07x slower                                                                  |
| regex_dna      | 227 ms                                                       | 243 ms: 1.07x slower                                                                   |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.5 ms: 1.26x faster                                                                  |
| json_loads           | 28.9 us                                                      | 25.5 us: 1.14x faster                                                                  |
| pickle_dict          | 32.3 us                                                      | 30.7 us: 1.05x faster                                                                  |
| xml_etree_parse      | 155 ms                                                       | 147 ms: 1.05x faster                                                                   |
| unpickle_pure_python | 238 us                                                       | 227 us: 1.05x faster                                                                   |
| pickle_pure_python   | 316 us                                                       | 307 us: 1.03x faster                                                                   |
| xml_etree_iterparse  | 107 ms                                                       | 105 ms: 1.02x faster                                                                   |
| unpickle_list        | 4.60 us                                                      | 4.55 us: 1.01x faster                                                                  |
| tomli_loads          | 2.25 sec                                                     | 2.23 sec: 1.01x faster                                                                 |
| pickle               | 9.89 us                                                      | 10.3 us: 1.04x slower                                                                  |
| xml_etree_process    | 55.9 ms                                                      | 58.6 ms: 1.05x slower                                                                  |
| xml_etree_generate   | 79.7 ms                                                      | 84.8 ms: 1.06x slower                                                                  |
| pickle_list          | 3.94 us                                                      | 4.39 us: 1.12x slower                                                                  |
| unpickle             | 13.3 us                                                      | 14.9 us: 1.12x slower                                                                  |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 12.8 ms: 1.19x slower                                                                  |
| python_startup_no_site | 7.73 ms                                                      | 11.1 ms: 1.43x slower                                                                  |
| Geometric mean         | (ref)                                                        | 1.31x slower                                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| mako           | 11.0 ms                                                      | 10.2 ms: 1.08x faster                                                                  |
| genshi_xml     | 57.1 ms                                                      | 54.8 ms: 1.04x faster                                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                                           |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 118 us: 4.49x faster                                                                   |
| asyncio_tcp                | 747 ms                                                       | 368 ms: 2.03x faster                                                                   |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                                 |
| generators                 | 54.6 ms                                                      | 33.4 ms: 1.64x faster                                                                  |
| pylint                     | 514 ms                                                       | 315 ms: 1.63x faster                                                                   |
| comprehensions             | 25.1 us                                                      | 16.6 us: 1.51x faster                                                                  |
| async_tree_memoization_tg  | 600 ms                                                       | 417 ms: 1.44x faster                                                                   |
| async_tree_none_tg         | 474 ms                                                       | 337 ms: 1.41x faster                                                                   |
| async_tree_none            | 518 ms                                                       | 368 ms: 1.41x faster                                                                   |
| async_tree_memoization     | 629 ms                                                       | 462 ms: 1.36x faster                                                                   |
| async_tree_io_tg           | 1.15 sec                                                     | 880 ms: 1.31x faster                                                                   |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 573 ms: 1.31x faster                                                                   |
| async_tree_io              | 1.17 sec                                                     | 902 ms: 1.30x faster                                                                   |
| chaos                      | 74.9 ms                                                      | 58.2 ms: 1.29x faster                                                                  |
| json_dumps                 | 13.3 ms                                                      | 10.5 ms: 1.26x faster                                                                  |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 610 ms: 1.23x faster                                                                   |
| raytrace                   | 309 ms                                                       | 251 ms: 1.23x faster                                                                   |
| coroutines                 | 27.8 ms                                                      | 22.6 ms: 1.23x faster                                                                  |
| sympy_sum                  | 186 ms                                                       | 155 ms: 1.20x faster                                                                   |
| scimark_lu                 | 114 ms                                                       | 95.6 ms: 1.19x faster                                                                  |
| nqueens                    | 103 ms                                                       | 86.7 ms: 1.18x faster                                                                  |
| crypto_pyaes               | 83.3 ms                                                      | 71.3 ms: 1.17x faster                                                                  |
| deltablue                  | 3.97 ms                                                      | 3.43 ms: 1.16x faster                                                                  |
| sympy_str                  | 337 ms                                                       | 296 ms: 1.14x faster                                                                   |
| json_loads                 | 28.9 us                                                      | 25.5 us: 1.14x faster                                                                  |
| bench_thread_pool          | 1.00 ms                                                      | 900 us: 1.11x faster                                                                   |
| logging_simple             | 7.24 us                                                      | 6.52 us: 1.11x faster                                                                  |
| mdp                        | 2.77 sec                                                     | 2.50 sec: 1.11x faster                                                                 |
| sympy_expand               | 553 ms                                                       | 500 ms: 1.11x faster                                                                   |
| sympy_integrate            | 25.8 ms                                                      | 23.5 ms: 1.10x faster                                                                  |
| chameleon                  | 7.92 ms                                                      | 7.24 ms: 1.09x faster                                                                  |
| regex_compile              | 156 ms                                                       | 143 ms: 1.09x faster                                                                   |
| fannkuch                   | 416 ms                                                       | 380 ms: 1.09x faster                                                                   |
| nbody                      | 92.9 ms                                                      | 85.5 ms: 1.09x faster                                                                  |
| richards_super             | 63.6 ms                                                      | 58.6 ms: 1.09x faster                                                                  |
| sqlglot_parse              | 1.51 ms                                                      | 1.40 ms: 1.08x faster                                                                  |
| hexiom                     | 6.98 ms                                                      | 6.45 ms: 1.08x faster                                                                  |
| scimark_monte_carlo        | 69.8 ms                                                      | 64.7 ms: 1.08x faster                                                                  |
| mako                       | 11.0 ms                                                      | 10.2 ms: 1.08x faster                                                                  |
| sqlglot_transpile          | 1.91 ms                                                      | 1.78 ms: 1.07x faster                                                                  |
| logging_format             | 7.71 us                                                      | 7.27 us: 1.06x faster                                                                  |
| thrift                     | 931 us                                                       | 880 us: 1.06x faster                                                                   |
| pickle_dict                | 32.3 us                                                      | 30.7 us: 1.05x faster                                                                  |
| xml_etree_parse            | 155 ms                                                       | 147 ms: 1.05x faster                                                                   |
| unpickle_pure_python       | 238 us                                                       | 227 us: 1.05x faster                                                                   |
| dask                       | 410 ms                                                       | 393 ms: 1.04x faster                                                                   |
| genshi_xml                 | 57.1 ms                                                      | 54.8 ms: 1.04x faster                                                                  |
| sqlglot_normalize          | 122 ms                                                       | 117 ms: 1.04x faster                                                                   |
| logging_silent             | 100 ns                                                       | 96.7 ns: 1.04x faster                                                                  |
| deepcopy                   | 391 us                                                       | 377 us: 1.04x faster                                                                   |
| tornado_http               | 124 ms                                                       | 120 ms: 1.04x faster                                                                   |
| pprint_pformat             | 1.67 sec                                                     | 1.61 sec: 1.04x faster                                                                 |
| pycparser                  | 1.31 sec                                                     | 1.27 sec: 1.03x faster                                                                 |
| pickle_pure_python         | 316 us                                                       | 307 us: 1.03x faster                                                                   |
| meteor_contest             | 131 ms                                                       | 127 ms: 1.03x faster                                                                   |
| pprint_safe_repr           | 805 ms                                                       | 787 ms: 1.02x faster                                                                   |
| xml_etree_iterparse        | 107 ms                                                       | 105 ms: 1.02x faster                                                                   |
| deepcopy_memo              | 37.5 us                                                      | 36.9 us: 1.02x faster                                                                  |
| json                       | 5.58 ms                                                      | 5.50 ms: 1.02x faster                                                                  |
| spectral_norm              | 95.1 ms                                                      | 94.0 ms: 1.01x faster                                                                  |
| sqlglot_optimize           | 59.0 ms                                                      | 58.4 ms: 1.01x faster                                                                  |
| unpickle_list              | 4.60 us                                                      | 4.55 us: 1.01x faster                                                                  |
| tomli_loads                | 2.25 sec                                                     | 2.23 sec: 1.01x faster                                                                 |
| float                      | 74.9 ms                                                      | 75.4 ms: 1.01x slower                                                                  |
| deepcopy_reduce            | 3.40 us                                                      | 3.42 us: 1.01x slower                                                                  |
| 2to3                       | 287 ms                                                       | 290 ms: 1.01x slower                                                                   |
| pathlib                    | 18.9 ms                                                      | 19.2 ms: 1.02x slower                                                                  |
| mypy2                      | 762 ms                                                       | 774 ms: 1.02x slower                                                                   |
| html5lib                   | 72.2 ms                                                      | 74.4 ms: 1.03x slower                                                                  |
| pickle                     | 9.89 us                                                      | 10.3 us: 1.04x slower                                                                  |
| regex_v8                   | 24.4 ms                                                      | 25.4 ms: 1.04x slower                                                                  |
| pidigits                   | 251 ms                                                       | 262 ms: 1.04x slower                                                                   |
| docutils                   | 2.85 sec                                                     | 2.98 sec: 1.05x slower                                                                 |
| richards                   | 49.7 ms                                                      | 52.0 ms: 1.05x slower                                                                  |
| xml_etree_process          | 55.9 ms                                                      | 58.6 ms: 1.05x slower                                                                  |
| xml_etree_generate         | 79.7 ms                                                      | 84.8 ms: 1.06x slower                                                                  |
| regex_effbot               | 3.34 ms                                                      | 3.57 ms: 1.07x slower                                                                  |
| regex_dna                  | 227 ms                                                       | 243 ms: 1.07x slower                                                                   |
| aiohttp                    | 986 us                                                       | 1.06 ms: 1.07x slower                                                                  |
| gunicorn                   | 966 us                                                       | 1.04 ms: 1.07x slower                                                                  |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.38 ms: 1.08x slower                                                                  |
| sqlite_synth               | 2.52 us                                                      | 2.73 us: 1.08x slower                                                                  |
| go                         | 158 ms                                                       | 172 ms: 1.09x slower                                                                   |
| async_generators           | 322 ms                                                       | 353 ms: 1.10x slower                                                                   |
| scimark_fft                | 281 ms                                                       | 309 ms: 1.10x slower                                                                   |
| pickle_list                | 3.94 us                                                      | 4.39 us: 1.12x slower                                                                  |
| pyflate                    | 449 ms                                                       | 502 ms: 1.12x slower                                                                   |
| gc_traversal               | 4.15 ms                                                      | 4.65 ms: 1.12x slower                                                                  |
| unpickle                   | 13.3 us                                                      | 14.9 us: 1.12x slower                                                                  |
| telco                      | 6.81 ms                                                      | 7.92 ms: 1.16x slower                                                                  |
| scimark_sor                | 110 ms                                                       | 130 ms: 1.19x slower                                                                   |
| python_startup             | 10.7 ms                                                      | 12.8 ms: 1.19x slower                                                                  |
| create_gc_cycles           | 1.58 ms                                                      | 1.89 ms: 1.20x slower                                                                  |
| coverage                   | 66.1 ms                                                      | 82.1 ms: 1.24x slower                                                                  |
| python_startup_no_site     | 7.73 ms                                                      | 11.1 ms: 1.43x slower                                                                  |
| Geometric mean             | (ref)                                                        | 1.08x faster                                                                           |

Benchmark hidden because not significant (4): asyncio_websockets, dulwich_log, genshi_text, bench_mp_pool
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.02x