# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a3
- machine: linux-x86_64
- commit hash: f009305
- commit date: 2024-01-17
- overall geometric mean: 1.06x faster
- HPT reliability: 99.93%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf2-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 294 ms: 1.03x slower                                             |
| chameleon      | 7.92 ms                                                      | 7.26 ms: 1.09x faster                                            |
| docutils       | 2.85 sec                                                     | 2.83 sec: 1.01x faster                                           |
| html5lib       | 72.2 ms                                                      | 73.9 ms: 1.02x slower                                            |
| tornado_http   | 124 ms                                                       | 118 ms: 1.06x faster                                             |
| Geometric mean | (ref)                                                        | 1.02x faster                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf2-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| async_tree_none            | 518 ms                                                       | 435 ms: 1.19x faster                                             |
| async_tree_memoization     | 629 ms                                                       | 547 ms: 1.15x faster                                             |
| async_tree_none_tg         | 474 ms                                                       | 430 ms: 1.10x faster                                             |
| async_tree_memoization_tg  | 600 ms                                                       | 545 ms: 1.10x faster                                             |
| async_tree_io              | 1.17 sec                                                     | 1.08 sec: 1.09x faster                                           |
| async_tree_io_tg           | 1.15 sec                                                     | 1.07 sec: 1.08x faster                                           |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 701 ms: 1.07x faster                                             |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 701 ms: 1.07x faster                                             |
| Geometric mean             | (ref)                                                        | 1.11x faster                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf2-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 85.3 ms: 1.09x faster                                            |
| float          | 74.9 ms                                                      | 78.0 ms: 1.04x slower                                            |
| pidigits       | 251 ms                                                       | 263 ms: 1.05x slower                                             |
| Geometric mean | (ref)                                                        | 1.00x slower                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf2-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 141 ms: 1.11x faster                                             |
| regex_dna      | 227 ms                                                       | 238 ms: 1.05x slower                                             |
| regex_effbot   | 3.34 ms                                                      | 3.50 ms: 1.05x slower                                            |
| regex_v8       | 24.4 ms                                                      | 26.0 ms: 1.06x slower                                            |
| Geometric mean | (ref)                                                        | 1.01x slower                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf2-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                            |
| json_loads           | 28.9 us                                                      | 25.0 us: 1.16x faster                                            |
| unpickle_pure_python | 238 us                                                       | 213 us: 1.12x faster                                             |
| xml_etree_parse      | 155 ms                                                       | 150 ms: 1.03x faster                                             |
| pickle_pure_python   | 316 us                                                       | 307 us: 1.03x faster                                             |
| tomli_loads          | 2.25 sec                                                     | 2.23 sec: 1.01x faster                                           |
| pickle_dict          | 32.3 us                                                      | 32.5 us: 1.00x slower                                            |
| pickle               | 9.89 us                                                      | 10.4 us: 1.05x slower                                            |
| unpickle_list        | 4.60 us                                                      | 4.82 us: 1.05x slower                                            |
| xml_etree_process    | 55.9 ms                                                      | 58.7 ms: 1.05x slower                                            |
| xml_etree_generate   | 79.7 ms                                                      | 85.6 ms: 1.07x slower                                            |
| pickle_list          | 3.94 us                                                      | 4.49 us: 1.14x slower                                            |
| unpickle             | 13.3 us                                                      | 15.4 us: 1.16x slower                                            |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                     |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf2-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 12.6 ms: 1.17x slower                                            |
| python_startup_no_site | 7.73 ms                                                      | 11.0 ms: 1.42x slower                                            |
| Geometric mean         | (ref)                                                        | 1.29x slower                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf2-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 10.3 ms: 1.07x faster                                            |
| genshi_xml      | 57.1 ms                                                      | 55.6 ms: 1.03x faster                                            |
| django_template | 39.3 ms                                                      | 38.4 ms: 1.02x faster                                            |
| genshi_text     | 25.5 ms                                                      | 25.7 ms: 1.01x slower                                            |
| Geometric mean  | (ref)                                                        | 1.03x faster                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf2-x86_64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 113 us: 4.70x faster                                             |
| asyncio_tcp                | 747 ms                                                       | 371 ms: 2.02x faster                                             |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.57 sec: 1.95x faster                                           |
| generators                 | 54.6 ms                                                      | 33.8 ms: 1.62x faster                                            |
| comprehensions             | 25.1 us                                                      | 16.5 us: 1.52x faster                                            |
| pylint                     | 514 ms                                                       | 343 ms: 1.50x faster                                             |
| json_dumps                 | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                            |
| chaos                      | 74.9 ms                                                      | 59.9 ms: 1.25x faster                                            |
| coroutines                 | 27.8 ms                                                      | 22.3 ms: 1.24x faster                                            |
| sympy_sum                  | 186 ms                                                       | 154 ms: 1.21x faster                                             |
| async_tree_none            | 518 ms                                                       | 435 ms: 1.19x faster                                             |
| crypto_pyaes               | 83.3 ms                                                      | 71.4 ms: 1.17x faster                                            |
| raytrace                   | 309 ms                                                       | 265 ms: 1.17x faster                                             |
| scimark_lu                 | 114 ms                                                       | 97.8 ms: 1.17x faster                                            |
| json_loads                 | 28.9 us                                                      | 25.0 us: 1.16x faster                                            |
| nqueens                    | 103 ms                                                       | 89.1 ms: 1.15x faster                                            |
| async_tree_memoization     | 629 ms                                                       | 547 ms: 1.15x faster                                             |
| sympy_str                  | 337 ms                                                       | 294 ms: 1.15x faster                                             |
| deltablue                  | 3.97 ms                                                      | 3.54 ms: 1.12x faster                                            |
| unpickle_pure_python       | 238 us                                                       | 213 us: 1.12x faster                                             |
| sympy_expand               | 553 ms                                                       | 494 ms: 1.12x faster                                             |
| regex_compile              | 156 ms                                                       | 141 ms: 1.11x faster                                             |
| mdp                        | 2.77 sec                                                     | 2.50 sec: 1.11x faster                                           |
| sympy_integrate            | 25.8 ms                                                      | 23.3 ms: 1.11x faster                                            |
| async_tree_none_tg         | 474 ms                                                       | 430 ms: 1.10x faster                                             |
| async_tree_memoization_tg  | 600 ms                                                       | 545 ms: 1.10x faster                                             |
| chameleon                  | 7.92 ms                                                      | 7.26 ms: 1.09x faster                                            |
| nbody                      | 92.9 ms                                                      | 85.3 ms: 1.09x faster                                            |
| sqlglot_parse              | 1.51 ms                                                      | 1.39 ms: 1.09x faster                                            |
| logging_simple             | 7.24 us                                                      | 6.66 us: 1.09x faster                                            |
| async_tree_io              | 1.17 sec                                                     | 1.08 sec: 1.09x faster                                           |
| hexiom                     | 6.98 ms                                                      | 6.46 ms: 1.08x faster                                            |
| async_tree_io_tg           | 1.15 sec                                                     | 1.07 sec: 1.08x faster                                           |
| fannkuch                   | 416 ms                                                       | 386 ms: 1.08x faster                                             |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 701 ms: 1.07x faster                                             |
| richards_super             | 63.6 ms                                                      | 59.4 ms: 1.07x faster                                            |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 701 ms: 1.07x faster                                             |
| sqlglot_transpile          | 1.91 ms                                                      | 1.79 ms: 1.07x faster                                            |
| thrift                     | 931 us                                                       | 872 us: 1.07x faster                                             |
| mako                       | 11.0 ms                                                      | 10.3 ms: 1.07x faster                                            |
| deepcopy                   | 391 us                                                       | 367 us: 1.06x faster                                             |
| json                       | 5.58 ms                                                      | 5.27 ms: 1.06x faster                                            |
| tornado_http               | 124 ms                                                       | 118 ms: 1.06x faster                                             |
| logging_format             | 7.71 us                                                      | 7.31 us: 1.05x faster                                            |
| gc_traversal               | 4.15 ms                                                      | 3.94 ms: 1.05x faster                                            |
| sqlglot_normalize          | 122 ms                                                       | 116 ms: 1.05x faster                                             |
| logging_silent             | 100 ns                                                       | 96.0 ns: 1.04x faster                                            |
| bench_thread_pool          | 1.00 ms                                                      | 960 us: 1.04x faster                                             |
| deepcopy_reduce            | 3.40 us                                                      | 3.28 us: 1.04x faster                                            |
| xml_etree_parse            | 155 ms                                                       | 150 ms: 1.03x faster                                             |
| spectral_norm              | 95.1 ms                                                      | 92.3 ms: 1.03x faster                                            |
| pickle_pure_python         | 316 us                                                       | 307 us: 1.03x faster                                             |
| bench_mp_pool              | 4.70 ms                                                      | 4.57 ms: 1.03x faster                                            |
| scimark_monte_carlo        | 69.8 ms                                                      | 67.9 ms: 1.03x faster                                            |
| genshi_xml                 | 57.1 ms                                                      | 55.6 ms: 1.03x faster                                            |
| django_template            | 39.3 ms                                                      | 38.4 ms: 1.02x faster                                            |
| deepcopy_memo              | 37.5 us                                                      | 37.1 us: 1.01x faster                                            |
| tomli_loads                | 2.25 sec                                                     | 2.23 sec: 1.01x faster                                           |
| docutils                   | 2.85 sec                                                     | 2.83 sec: 1.01x faster                                           |
| meteor_contest             | 131 ms                                                       | 130 ms: 1.01x faster                                             |
| pprint_pformat             | 1.67 sec                                                     | 1.66 sec: 1.01x faster                                           |
| pickle_dict                | 32.3 us                                                      | 32.5 us: 1.00x slower                                            |
| pprint_safe_repr           | 805 ms                                                       | 813 ms: 1.01x slower                                             |
| genshi_text                | 25.5 ms                                                      | 25.7 ms: 1.01x slower                                            |
| dulwich_log                | 67.4 ms                                                      | 68.2 ms: 1.01x slower                                            |
| asyncio_websockets         | 390 ms                                                       | 395 ms: 1.01x slower                                             |
| html5lib                   | 72.2 ms                                                      | 73.9 ms: 1.02x slower                                            |
| 2to3                       | 287 ms                                                       | 294 ms: 1.03x slower                                             |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.21 ms: 1.04x slower                                            |
| float                      | 74.9 ms                                                      | 78.0 ms: 1.04x slower                                            |
| pickle                     | 9.89 us                                                      | 10.4 us: 1.05x slower                                            |
| regex_dna                  | 227 ms                                                       | 238 ms: 1.05x slower                                             |
| unpickle_list              | 4.60 us                                                      | 4.82 us: 1.05x slower                                            |
| pidigits                   | 251 ms                                                       | 263 ms: 1.05x slower                                             |
| regex_effbot               | 3.34 ms                                                      | 3.50 ms: 1.05x slower                                            |
| xml_etree_process          | 55.9 ms                                                      | 58.7 ms: 1.05x slower                                            |
| go                         | 158 ms                                                       | 166 ms: 1.05x slower                                             |
| regex_v8                   | 24.4 ms                                                      | 26.0 ms: 1.06x slower                                            |
| xml_etree_generate         | 79.7 ms                                                      | 85.6 ms: 1.07x slower                                            |
| scimark_fft                | 281 ms                                                       | 302 ms: 1.08x slower                                             |
| aiohttp                    | 986 us                                                       | 1.06 ms: 1.08x slower                                            |
| richards                   | 49.7 ms                                                      | 53.7 ms: 1.08x slower                                            |
| gunicorn                   | 966 us                                                       | 1.05 ms: 1.08x slower                                            |
| sqlite_synth               | 2.52 us                                                      | 2.77 us: 1.10x slower                                            |
| pyflate                    | 449 ms                                                       | 501 ms: 1.11x slower                                             |
| mypy2                      | 762 ms                                                       | 864 ms: 1.13x slower                                             |
| pickle_list                | 3.94 us                                                      | 4.49 us: 1.14x slower                                            |
| async_generators           | 322 ms                                                       | 368 ms: 1.14x slower                                             |
| unpickle                   | 13.3 us                                                      | 15.4 us: 1.16x slower                                            |
| python_startup             | 10.7 ms                                                      | 12.6 ms: 1.17x slower                                            |
| flaskblogging              | 3.88 ms                                                      | 4.61 ms: 1.19x slower                                            |
| telco                      | 6.81 ms                                                      | 8.23 ms: 1.21x slower                                            |
| coverage                   | 66.1 ms                                                      | 82.9 ms: 1.25x slower                                            |
| scimark_sor                | 110 ms                                                       | 144 ms: 1.31x slower                                             |
| python_startup_no_site     | 7.73 ms                                                      | 11.0 ms: 1.42x slower                                            |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                     |

Benchmark hidden because not significant (5): create_gc_cycles, pathlib, xml_etree_iterparse, sqlglot_optimize, pycparser
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.93% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x