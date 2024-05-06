# Results vs. 3.11.0

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: linux-x86_64
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.09x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| chameleon      | 7.92 ms                                                      | 7.29 ms: 1.09x faster                                                                |
| docutils       | 2.85 sec                                                     | 2.99 sec: 1.05x slower                                                               |
| tornado_http   | 124 ms                                                       | 120 ms: 1.03x faster                                                                 |
| Geometric mean | (ref)                                                        | 1.01x faster                                                                         |

Benchmark hidden because not significant (2): 2to3, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 418 ms: 1.44x faster                                                                 |
| async_tree_none_tg         | 474 ms                                                       | 336 ms: 1.41x faster                                                                 |
| async_tree_none            | 518 ms                                                       | 368 ms: 1.41x faster                                                                 |
| async_tree_memoization     | 629 ms                                                       | 464 ms: 1.36x faster                                                                 |
| async_tree_io_tg           | 1.15 sec                                                     | 880 ms: 1.31x faster                                                                 |
| async_tree_io              | 1.17 sec                                                     | 900 ms: 1.30x faster                                                                 |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 577 ms: 1.30x faster                                                                 |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 613 ms: 1.23x faster                                                                 |
| Geometric mean             | (ref)                                                        | 1.34x faster                                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 86.7 ms: 1.07x faster                                                                |
| float          | 74.9 ms                                                      | 77.2 ms: 1.03x slower                                                                |
| pidigits       | 251 ms                                                       | 262 ms: 1.04x slower                                                                 |
| Geometric mean | (ref)                                                        | 1.00x slower                                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 143 ms: 1.09x faster                                                                 |
| regex_effbot   | 3.34 ms                                                      | 3.47 ms: 1.04x slower                                                                |
| regex_dna      | 227 ms                                                       | 238 ms: 1.04x slower                                                                 |
| regex_v8       | 24.4 ms                                                      | 26.0 ms: 1.06x slower                                                                |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                                |
| unpickle_pure_python | 238 us                                                       | 204 us: 1.17x faster                                                                 |
| json_loads           | 28.9 us                                                      | 24.8 us: 1.17x faster                                                                |
| xml_etree_parse      | 155 ms                                                       | 146 ms: 1.06x faster                                                                 |
| xml_etree_iterparse  | 107 ms                                                       | 104 ms: 1.03x faster                                                                 |
| tomli_loads          | 2.25 sec                                                     | 2.18 sec: 1.03x faster                                                               |
| pickle_pure_python   | 316 us                                                       | 310 us: 1.02x faster                                                                 |
| unpickle_list        | 4.60 us                                                      | 4.56 us: 1.01x faster                                                                |
| pickle_dict          | 32.3 us                                                      | 33.3 us: 1.03x slower                                                                |
| pickle               | 9.89 us                                                      | 10.5 us: 1.06x slower                                                                |
| xml_etree_process    | 55.9 ms                                                      | 59.6 ms: 1.07x slower                                                                |
| xml_etree_generate   | 79.7 ms                                                      | 85.1 ms: 1.07x slower                                                                |
| unpickle             | 13.3 us                                                      | 14.8 us: 1.11x slower                                                                |
| pickle_list          | 3.94 us                                                      | 4.44 us: 1.13x slower                                                                |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 8.84 ms: 1.14x slower                                                                |
| python_startup         | 10.7 ms                                                      | 12.9 ms: 1.20x slower                                                                |
| Geometric mean         | (ref)                                                        | 1.17x slower                                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 10.5 ms: 1.05x faster                                                                |
| genshi_xml      | 57.1 ms                                                      | 56.2 ms: 1.02x faster                                                                |
| django_template | 39.3 ms                                                      | 38.8 ms: 1.01x faster                                                                |
| genshi_text     | 25.5 ms                                                      | 26.4 ms: 1.04x slower                                                                |
| Geometric mean  | (ref)                                                        | 1.01x faster                                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 118 us: 4.52x faster                                                                 |
| asyncio_tcp                | 747 ms                                                       | 373 ms: 2.00x faster                                                                 |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                               |
| generators                 | 54.6 ms                                                      | 33.1 ms: 1.65x faster                                                                |
| pylint                     | 514 ms                                                       | 345 ms: 1.49x faster                                                                 |
| comprehensions             | 25.1 us                                                      | 16.8 us: 1.49x faster                                                                |
| async_tree_memoization_tg  | 600 ms                                                       | 418 ms: 1.44x faster                                                                 |
| async_tree_none_tg         | 474 ms                                                       | 336 ms: 1.41x faster                                                                 |
| async_tree_none            | 518 ms                                                       | 368 ms: 1.41x faster                                                                 |
| async_tree_memoization     | 629 ms                                                       | 464 ms: 1.36x faster                                                                 |
| coroutines                 | 27.8 ms                                                      | 21.2 ms: 1.31x faster                                                                |
| async_tree_io_tg           | 1.15 sec                                                     | 880 ms: 1.31x faster                                                                 |
| async_tree_io              | 1.17 sec                                                     | 900 ms: 1.30x faster                                                                 |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 577 ms: 1.30x faster                                                                 |
| chaos                      | 74.9 ms                                                      | 58.6 ms: 1.28x faster                                                                |
| json_dumps                 | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                                |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 613 ms: 1.23x faster                                                                 |
| raytrace                   | 309 ms                                                       | 253 ms: 1.22x faster                                                                 |
| sympy_sum                  | 186 ms                                                       | 154 ms: 1.20x faster                                                                 |
| deltablue                  | 3.97 ms                                                      | 3.32 ms: 1.19x faster                                                                |
| nqueens                    | 103 ms                                                       | 86.6 ms: 1.19x faster                                                                |
| unpickle_pure_python       | 238 us                                                       | 204 us: 1.17x faster                                                                 |
| json_loads                 | 28.9 us                                                      | 24.8 us: 1.17x faster                                                                |
| scimark_lu                 | 114 ms                                                       | 98.6 ms: 1.16x faster                                                                |
| fannkuch                   | 416 ms                                                       | 361 ms: 1.15x faster                                                                 |
| crypto_pyaes               | 83.3 ms                                                      | 72.6 ms: 1.15x faster                                                                |
| logging_simple             | 7.24 us                                                      | 6.32 us: 1.15x faster                                                                |
| hexiom                     | 6.98 ms                                                      | 6.10 ms: 1.14x faster                                                                |
| sympy_str                  | 337 ms                                                       | 298 ms: 1.13x faster                                                                 |
| bench_thread_pool          | 1.00 ms                                                      | 884 us: 1.13x faster                                                                 |
| logging_format             | 7.71 us                                                      | 6.91 us: 1.12x faster                                                                |
| sympy_integrate            | 25.8 ms                                                      | 23.1 ms: 1.12x faster                                                                |
| mdp                        | 2.77 sec                                                     | 2.50 sec: 1.11x faster                                                               |
| pathlib                    | 18.9 ms                                                      | 17.1 ms: 1.11x faster                                                                |
| scimark_monte_carlo        | 69.8 ms                                                      | 63.2 ms: 1.11x faster                                                                |
| sympy_expand               | 553 ms                                                       | 504 ms: 1.10x faster                                                                 |
| richards_super             | 63.6 ms                                                      | 58.0 ms: 1.10x faster                                                                |
| regex_compile              | 156 ms                                                       | 143 ms: 1.09x faster                                                                 |
| chameleon                  | 7.92 ms                                                      | 7.29 ms: 1.09x faster                                                                |
| sqlglot_parse              | 1.51 ms                                                      | 1.41 ms: 1.07x faster                                                                |
| nbody                      | 92.9 ms                                                      | 86.7 ms: 1.07x faster                                                                |
| sqlglot_transpile          | 1.91 ms                                                      | 1.79 ms: 1.07x faster                                                                |
| xml_etree_parse            | 155 ms                                                       | 146 ms: 1.06x faster                                                                 |
| logging_silent             | 100 ns                                                       | 94.6 ns: 1.06x faster                                                                |
| mako                       | 11.0 ms                                                      | 10.5 ms: 1.05x faster                                                                |
| dask                       | 410 ms                                                       | 391 ms: 1.05x faster                                                                 |
| bench_mp_pool              | 4.70 ms                                                      | 4.50 ms: 1.04x faster                                                                |
| sqlglot_normalize          | 122 ms                                                       | 117 ms: 1.04x faster                                                                 |
| thrift                     | 931 us                                                       | 900 us: 1.03x faster                                                                 |
| tornado_http               | 124 ms                                                       | 120 ms: 1.03x faster                                                                 |
| deepcopy                   | 391 us                                                       | 379 us: 1.03x faster                                                                 |
| xml_etree_iterparse        | 107 ms                                                       | 104 ms: 1.03x faster                                                                 |
| tomli_loads                | 2.25 sec                                                     | 2.18 sec: 1.03x faster                                                               |
| meteor_contest             | 131 ms                                                       | 127 ms: 1.02x faster                                                                 |
| json                       | 5.58 ms                                                      | 5.46 ms: 1.02x faster                                                                |
| pycparser                  | 1.31 sec                                                     | 1.28 sec: 1.02x faster                                                               |
| pickle_pure_python         | 316 us                                                       | 310 us: 1.02x faster                                                                 |
| go                         | 158 ms                                                       | 155 ms: 1.02x faster                                                                 |
| pprint_pformat             | 1.67 sec                                                     | 1.64 sec: 1.02x faster                                                               |
| genshi_xml                 | 57.1 ms                                                      | 56.2 ms: 1.02x faster                                                                |
| django_template            | 39.3 ms                                                      | 38.8 ms: 1.01x faster                                                                |
| unpickle_list              | 4.60 us                                                      | 4.56 us: 1.01x faster                                                                |
| pprint_safe_repr           | 805 ms                                                       | 801 ms: 1.00x faster                                                                 |
| deepcopy_reduce            | 3.40 us                                                      | 3.42 us: 1.01x slower                                                                |
| deepcopy_memo              | 37.5 us                                                      | 37.9 us: 1.01x slower                                                                |
| asyncio_websockets         | 390 ms                                                       | 396 ms: 1.02x slower                                                                 |
| mypy2                      | 762 ms                                                       | 774 ms: 1.02x slower                                                                 |
| spectral_norm              | 95.1 ms                                                      | 96.6 ms: 1.02x slower                                                                |
| float                      | 74.9 ms                                                      | 77.2 ms: 1.03x slower                                                                |
| pickle_dict                | 32.3 us                                                      | 33.3 us: 1.03x slower                                                                |
| genshi_text                | 25.5 ms                                                      | 26.4 ms: 1.04x slower                                                                |
| richards                   | 49.7 ms                                                      | 51.5 ms: 1.04x slower                                                                |
| regex_effbot               | 3.34 ms                                                      | 3.47 ms: 1.04x slower                                                                |
| pyflate                    | 449 ms                                                       | 468 ms: 1.04x slower                                                                 |
| pidigits                   | 251 ms                                                       | 262 ms: 1.04x slower                                                                 |
| regex_dna                  | 227 ms                                                       | 238 ms: 1.04x slower                                                                 |
| docutils                   | 2.85 sec                                                     | 2.99 sec: 1.05x slower                                                               |
| pickle                     | 9.89 us                                                      | 10.5 us: 1.06x slower                                                                |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.32 ms: 1.06x slower                                                                |
| scimark_fft                | 281 ms                                                       | 298 ms: 1.06x slower                                                                 |
| regex_v8                   | 24.4 ms                                                      | 26.0 ms: 1.06x slower                                                                |
| gc_traversal               | 4.15 ms                                                      | 4.42 ms: 1.07x slower                                                                |
| xml_etree_process          | 55.9 ms                                                      | 59.6 ms: 1.07x slower                                                                |
| xml_etree_generate         | 79.7 ms                                                      | 85.1 ms: 1.07x slower                                                                |
| gunicorn                   | 966 us                                                       | 1.05 ms: 1.08x slower                                                                |
| scimark_sor                | 110 ms                                                       | 119 ms: 1.09x slower                                                                 |
| aiohttp                    | 986 us                                                       | 1.07 ms: 1.09x slower                                                                |
| sqlite_synth               | 2.52 us                                                      | 2.77 us: 1.10x slower                                                                |
| async_generators           | 322 ms                                                       | 356 ms: 1.11x slower                                                                 |
| unpickle                   | 13.3 us                                                      | 14.8 us: 1.11x slower                                                                |
| pickle_list                | 3.94 us                                                      | 4.44 us: 1.13x slower                                                                |
| python_startup_no_site     | 7.73 ms                                                      | 8.84 ms: 1.14x slower                                                                |
| telco                      | 6.81 ms                                                      | 8.06 ms: 1.18x slower                                                                |
| python_startup             | 10.7 ms                                                      | 12.9 ms: 1.20x slower                                                                |
| create_gc_cycles           | 1.58 ms                                                      | 1.93 ms: 1.22x slower                                                                |
| coverage                   | 66.1 ms                                                      | 86.3 ms: 1.31x slower                                                                |
| Geometric mean             | (ref)                                                        | 1.09x faster                                                                         |

Benchmark hidden because not significant (4): 2to3, sqlglot_optimize, dulwich_log, html5lib
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.03x