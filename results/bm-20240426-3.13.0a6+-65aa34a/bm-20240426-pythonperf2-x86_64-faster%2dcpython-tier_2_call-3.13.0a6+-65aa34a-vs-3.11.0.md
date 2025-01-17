# Results vs. 3.11.0

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.09x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 286 ms: 1.00x faster                                                          |
| chameleon      | 7.92 ms                                                      | 7.18 ms: 1.10x faster                                                         |
| docutils       | 2.85 sec                                                     | 3.00 sec: 1.05x slower                                                        |
| html5lib       | 72.2 ms                                                      | 73.0 ms: 1.01x slower                                                         |
| tornado_http   | 124 ms                                                       | 119 ms: 1.04x faster                                                          |
| Geometric mean | (ref)                                                        | 1.02x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none_tg         | 474 ms                                                       | 329 ms: 1.44x faster                                                          |
| async_tree_memoization_tg  | 600 ms                                                       | 418 ms: 1.44x faster                                                          |
| async_tree_none            | 518 ms                                                       | 363 ms: 1.42x faster                                                          |
| async_tree_memoization     | 629 ms                                                       | 458 ms: 1.37x faster                                                          |
| async_tree_io              | 1.17 sec                                                     | 867 ms: 1.35x faster                                                          |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 574 ms: 1.31x faster                                                          |
| async_tree_io_tg           | 1.15 sec                                                     | 888 ms: 1.30x faster                                                          |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 606 ms: 1.24x faster                                                          |
| Geometric mean             | (ref)                                                        | 1.36x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 86.5 ms: 1.07x faster                                                         |
| float          | 74.9 ms                                                      | 77.4 ms: 1.03x slower                                                         |
| pidigits       | 251 ms                                                       | 262 ms: 1.04x slower                                                          |
| Geometric mean | (ref)                                                        | 1.00x slower                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 142 ms: 1.10x faster                                                          |
| regex_dna      | 227 ms                                                       | 239 ms: 1.05x slower                                                          |
| regex_v8       | 24.4 ms                                                      | 26.5 ms: 1.08x slower                                                         |
| regex_effbot   | 3.34 ms                                                      | 3.70 ms: 1.11x slower                                                         |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                         |
| json_loads           | 28.9 us                                                      | 24.6 us: 1.18x faster                                                         |
| unpickle_pure_python | 238 us                                                       | 212 us: 1.12x faster                                                          |
| xml_etree_parse      | 155 ms                                                       | 150 ms: 1.03x faster                                                          |
| pickle_pure_python   | 316 us                                                       | 308 us: 1.03x faster                                                          |
| tomli_loads          | 2.25 sec                                                     | 2.23 sec: 1.01x faster                                                        |
| pickle               | 9.89 us                                                      | 10.4 us: 1.05x slower                                                         |
| xml_etree_process    | 55.9 ms                                                      | 59.0 ms: 1.06x slower                                                         |
| xml_etree_generate   | 79.7 ms                                                      | 84.8 ms: 1.06x slower                                                         |
| pickle_list          | 3.94 us                                                      | 4.52 us: 1.15x slower                                                         |
| unpickle             | 13.3 us                                                      | 15.3 us: 1.15x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                                  |

Benchmark hidden because not significant (3): xml_etree_iterparse, unpickle_list, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 8.81 ms: 1.14x slower                                                         |
| python_startup         | 10.7 ms                                                      | 12.9 ms: 1.20x slower                                                         |
| Geometric mean         | (ref)                                                        | 1.17x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 10.2 ms: 1.08x faster                                                         |
| genshi_xml      | 57.1 ms                                                      | 54.0 ms: 1.06x faster                                                         |
| genshi_text     | 25.5 ms                                                      | 24.8 ms: 1.03x faster                                                         |
| django_template | 39.3 ms                                                      | 38.7 ms: 1.01x faster                                                         |
| Geometric mean  | (ref)                                                        | 1.05x faster                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-pythonperf2-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 173 us: 3.08x faster                                                          |
| asyncio_tcp                | 747 ms                                                       | 367 ms: 2.04x faster                                                          |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.57 sec: 1.95x faster                                                        |
| generators                 | 54.6 ms                                                      | 33.4 ms: 1.64x faster                                                         |
| pylint                     | 514 ms                                                       | 345 ms: 1.49x faster                                                          |
| comprehensions             | 25.1 us                                                      | 17.1 us: 1.47x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 329 ms: 1.44x faster                                                          |
| async_tree_memoization_tg  | 600 ms                                                       | 418 ms: 1.44x faster                                                          |
| async_tree_none            | 518 ms                                                       | 363 ms: 1.42x faster                                                          |
| async_tree_memoization     | 629 ms                                                       | 458 ms: 1.37x faster                                                          |
| async_tree_io              | 1.17 sec                                                     | 867 ms: 1.35x faster                                                          |
| coroutines                 | 27.8 ms                                                      | 20.6 ms: 1.35x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 574 ms: 1.31x faster                                                          |
| async_tree_io_tg           | 1.15 sec                                                     | 888 ms: 1.30x faster                                                          |
| chaos                      | 74.9 ms                                                      | 58.8 ms: 1.27x faster                                                         |
| json_dumps                 | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 606 ms: 1.24x faster                                                          |
| deltablue                  | 3.97 ms                                                      | 3.22 ms: 1.23x faster                                                         |
| sympy_sum                  | 186 ms                                                       | 153 ms: 1.21x faster                                                          |
| raytrace                   | 309 ms                                                       | 257 ms: 1.20x faster                                                          |
| scimark_lu                 | 114 ms                                                       | 95.4 ms: 1.20x faster                                                         |
| json_loads                 | 28.9 us                                                      | 24.6 us: 1.18x faster                                                         |
| nqueens                    | 103 ms                                                       | 87.6 ms: 1.17x faster                                                         |
| fannkuch                   | 416 ms                                                       | 356 ms: 1.17x faster                                                          |
| crypto_pyaes               | 83.3 ms                                                      | 71.3 ms: 1.17x faster                                                         |
| hexiom                     | 6.98 ms                                                      | 5.99 ms: 1.16x faster                                                         |
| sympy_str                  | 337 ms                                                       | 294 ms: 1.15x faster                                                          |
| scimark_monte_carlo        | 69.8 ms                                                      | 61.8 ms: 1.13x faster                                                         |
| logging_simple             | 7.24 us                                                      | 6.41 us: 1.13x faster                                                         |
| unpickle_pure_python       | 238 us                                                       | 212 us: 1.12x faster                                                          |
| bench_thread_pool          | 1.00 ms                                                      | 890 us: 1.12x faster                                                          |
| mdp                        | 2.77 sec                                                     | 2.50 sec: 1.11x faster                                                        |
| sympy_integrate            | 25.8 ms                                                      | 23.3 ms: 1.11x faster                                                         |
| sympy_expand               | 553 ms                                                       | 499 ms: 1.11x faster                                                          |
| chameleon                  | 7.92 ms                                                      | 7.18 ms: 1.10x faster                                                         |
| pathlib                    | 18.9 ms                                                      | 17.2 ms: 1.10x faster                                                         |
| regex_compile              | 156 ms                                                       | 142 ms: 1.10x faster                                                          |
| logging_format             | 7.71 us                                                      | 7.03 us: 1.10x faster                                                         |
| sqlglot_parse              | 1.51 ms                                                      | 1.38 ms: 1.10x faster                                                         |
| richards_super             | 63.6 ms                                                      | 58.4 ms: 1.09x faster                                                         |
| mako                       | 11.0 ms                                                      | 10.2 ms: 1.08x faster                                                         |
| bench_mp_pool              | 4.70 ms                                                      | 4.35 ms: 1.08x faster                                                         |
| sqlglot_transpile          | 1.91 ms                                                      | 1.77 ms: 1.08x faster                                                         |
| nbody                      | 92.9 ms                                                      | 86.5 ms: 1.07x faster                                                         |
| logging_silent             | 100 ns                                                       | 93.9 ns: 1.07x faster                                                         |
| thrift                     | 931 us                                                       | 878 us: 1.06x faster                                                          |
| genshi_xml                 | 57.1 ms                                                      | 54.0 ms: 1.06x faster                                                         |
| dask                       | 410 ms                                                       | 391 ms: 1.05x faster                                                          |
| tornado_http               | 124 ms                                                       | 119 ms: 1.04x faster                                                          |
| pycparser                  | 1.31 sec                                                     | 1.26 sec: 1.04x faster                                                        |
| json                       | 5.58 ms                                                      | 5.38 ms: 1.04x faster                                                         |
| sqlglot_normalize          | 122 ms                                                       | 118 ms: 1.03x faster                                                          |
| xml_etree_parse            | 155 ms                                                       | 150 ms: 1.03x faster                                                          |
| genshi_text                | 25.5 ms                                                      | 24.8 ms: 1.03x faster                                                         |
| pickle_pure_python         | 316 us                                                       | 308 us: 1.03x faster                                                          |
| meteor_contest             | 131 ms                                                       | 128 ms: 1.02x faster                                                          |
| pprint_pformat             | 1.67 sec                                                     | 1.63 sec: 1.02x faster                                                        |
| dulwich_log                | 67.4 ms                                                      | 66.4 ms: 1.02x faster                                                         |
| django_template            | 39.3 ms                                                      | 38.7 ms: 1.01x faster                                                         |
| deepcopy                   | 391 us                                                       | 386 us: 1.01x faster                                                          |
| pprint_safe_repr           | 805 ms                                                       | 798 ms: 1.01x faster                                                          |
| tomli_loads                | 2.25 sec                                                     | 2.23 sec: 1.01x faster                                                        |
| 2to3                       | 287 ms                                                       | 286 ms: 1.00x faster                                                          |
| html5lib                   | 72.2 ms                                                      | 73.0 ms: 1.01x slower                                                         |
| pyflate                    | 449 ms                                                       | 454 ms: 1.01x slower                                                          |
| mypy2                      | 762 ms                                                       | 771 ms: 1.01x slower                                                          |
| go                         | 158 ms                                                       | 160 ms: 1.01x slower                                                          |
| spectral_norm              | 95.1 ms                                                      | 97.8 ms: 1.03x slower                                                         |
| float                      | 74.9 ms                                                      | 77.4 ms: 1.03x slower                                                         |
| deepcopy_memo              | 37.5 us                                                      | 38.9 us: 1.04x slower                                                         |
| pidigits                   | 251 ms                                                       | 262 ms: 1.04x slower                                                          |
| richards                   | 49.7 ms                                                      | 52.0 ms: 1.05x slower                                                         |
| deepcopy_reduce            | 3.40 us                                                      | 3.56 us: 1.05x slower                                                         |
| regex_dna                  | 227 ms                                                       | 239 ms: 1.05x slower                                                          |
| pickle                     | 9.89 us                                                      | 10.4 us: 1.05x slower                                                         |
| docutils                   | 2.85 sec                                                     | 3.00 sec: 1.05x slower                                                        |
| xml_etree_process          | 55.9 ms                                                      | 59.0 ms: 1.06x slower                                                         |
| xml_etree_generate         | 79.7 ms                                                      | 84.8 ms: 1.06x slower                                                         |
| gc_traversal               | 4.15 ms                                                      | 4.42 ms: 1.07x slower                                                         |
| scimark_fft                | 281 ms                                                       | 301 ms: 1.07x slower                                                          |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.36 ms: 1.07x slower                                                         |
| aiohttp                    | 986 us                                                       | 1.07 ms: 1.08x slower                                                         |
| regex_v8                   | 24.4 ms                                                      | 26.5 ms: 1.08x slower                                                         |
| sqlite_synth               | 2.52 us                                                      | 2.74 us: 1.09x slower                                                         |
| gunicorn                   | 966 us                                                       | 1.06 ms: 1.09x slower                                                         |
| regex_effbot               | 3.34 ms                                                      | 3.70 ms: 1.11x slower                                                         |
| scimark_sor                | 110 ms                                                       | 123 ms: 1.12x slower                                                          |
| async_generators           | 322 ms                                                       | 365 ms: 1.14x slower                                                          |
| python_startup_no_site     | 7.73 ms                                                      | 8.81 ms: 1.14x slower                                                         |
| pickle_list                | 3.94 us                                                      | 4.52 us: 1.15x slower                                                         |
| unpickle                   | 13.3 us                                                      | 15.3 us: 1.15x slower                                                         |
| telco                      | 6.81 ms                                                      | 7.97 ms: 1.17x slower                                                         |
| python_startup             | 10.7 ms                                                      | 12.9 ms: 1.20x slower                                                         |
| create_gc_cycles           | 1.58 ms                                                      | 1.95 ms: 1.24x slower                                                         |
| coverage                   | 66.1 ms                                                      | 85.3 ms: 1.29x slower                                                         |
| Geometric mean             | (ref)                                                        | 1.09x faster                                                                  |

Benchmark hidden because not significant (5): xml_etree_iterparse, unpickle_list, pickle_dict, sqlglot_optimize, asyncio_websockets
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.03x