# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a4
- machine: linux-x86_64
- commit hash: 9d34f60
- commit date: 2024-02-15
- overall geometric mean: 1.06x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.01x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf2-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 292 ms: 1.02x slower                                             |
| chameleon      | 7.92 ms                                                      | 7.42 ms: 1.07x faster                                            |
| html5lib       | 72.2 ms                                                      | 76.0 ms: 1.05x slower                                            |
| tornado_http   | 124 ms                                                       | 122 ms: 1.02x faster                                             |
| Geometric mean | (ref)                                                        | 1.00x faster                                                     |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf2-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| async_tree_none            | 518 ms                                                       | 434 ms: 1.19x faster                                             |
| async_tree_memoization     | 629 ms                                                       | 546 ms: 1.15x faster                                             |
| async_tree_none_tg         | 474 ms                                                       | 434 ms: 1.09x faster                                             |
| async_tree_memoization_tg  | 600 ms                                                       | 551 ms: 1.09x faster                                             |
| async_tree_io              | 1.17 sec                                                     | 1.08 sec: 1.09x faster                                           |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 699 ms: 1.08x faster                                             |
| async_tree_io_tg           | 1.15 sec                                                     | 1.08 sec: 1.07x faster                                           |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 705 ms: 1.06x faster                                             |
| Geometric mean             | (ref)                                                        | 1.10x faster                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf2-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 84.8 ms: 1.10x faster                                            |
| pidigits       | 251 ms                                                       | 262 ms: 1.04x slower                                             |
| float          | 74.9 ms                                                      | 78.8 ms: 1.05x slower                                            |
| Geometric mean | (ref)                                                        | 1.00x slower                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf2-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 142 ms: 1.10x faster                                             |
| regex_effbot   | 3.34 ms                                                      | 3.48 ms: 1.04x slower                                            |
| regex_dna      | 227 ms                                                       | 241 ms: 1.06x slower                                             |
| regex_v8       | 24.4 ms                                                      | 26.0 ms: 1.06x slower                                            |
| Geometric mean | (ref)                                                        | 1.02x slower                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf2-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.5 ms: 1.27x faster                                            |
| json_loads           | 28.9 us                                                      | 25.3 us: 1.14x faster                                            |
| unpickle_pure_python | 238 us                                                       | 217 us: 1.10x faster                                             |
| pickle_dict          | 32.3 us                                                      | 30.3 us: 1.07x faster                                            |
| xml_etree_parse      | 155 ms                                                       | 148 ms: 1.04x faster                                             |
| xml_etree_iterparse  | 107 ms                                                       | 105 ms: 1.02x faster                                             |
| unpickle_list        | 4.60 us                                                      | 4.68 us: 1.02x slower                                            |
| xml_etree_process    | 55.9 ms                                                      | 57.7 ms: 1.03x slower                                            |
| pickle               | 9.89 us                                                      | 10.3 us: 1.04x slower                                            |
| tomli_loads          | 2.25 sec                                                     | 2.38 sec: 1.06x slower                                           |
| xml_etree_generate   | 79.7 ms                                                      | 85.1 ms: 1.07x slower                                            |
| pickle_list          | 3.94 us                                                      | 4.33 us: 1.10x slower                                            |
| unpickle             | 13.3 us                                                      | 15.3 us: 1.15x slower                                            |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                     |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf2-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 12.6 ms: 1.18x slower                                            |
| python_startup_no_site | 7.73 ms                                                      | 11.0 ms: 1.43x slower                                            |
| Geometric mean         | (ref)                                                        | 1.30x slower                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf2-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 10.4 ms: 1.06x faster                                            |
| django_template | 39.3 ms                                                      | 38.4 ms: 1.02x faster                                            |
| genshi_xml      | 57.1 ms                                                      | 55.8 ms: 1.02x faster                                            |
| genshi_text     | 25.5 ms                                                      | 25.9 ms: 1.02x slower                                            |
| Geometric mean  | (ref)                                                        | 1.02x faster                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf2-x86_64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 117 us: 4.55x faster                                             |
| asyncio_tcp                | 747 ms                                                       | 374 ms: 2.00x faster                                             |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.57 sec: 1.95x faster                                           |
| generators                 | 54.6 ms                                                      | 34.1 ms: 1.60x faster                                            |
| comprehensions             | 25.1 us                                                      | 16.5 us: 1.52x faster                                            |
| pylint                     | 514 ms                                                       | 345 ms: 1.49x faster                                             |
| json_dumps                 | 13.3 ms                                                      | 10.5 ms: 1.27x faster                                            |
| coroutines                 | 27.8 ms                                                      | 22.2 ms: 1.25x faster                                            |
| chaos                      | 74.9 ms                                                      | 61.0 ms: 1.23x faster                                            |
| sympy_sum                  | 186 ms                                                       | 153 ms: 1.22x faster                                             |
| scimark_lu                 | 114 ms                                                       | 94.4 ms: 1.21x faster                                            |
| async_tree_none            | 518 ms                                                       | 434 ms: 1.19x faster                                             |
| raytrace                   | 309 ms                                                       | 262 ms: 1.18x faster                                             |
| crypto_pyaes               | 83.3 ms                                                      | 71.3 ms: 1.17x faster                                            |
| nqueens                    | 103 ms                                                       | 88.8 ms: 1.16x faster                                            |
| sympy_str                  | 337 ms                                                       | 291 ms: 1.16x faster                                             |
| async_tree_memoization     | 629 ms                                                       | 546 ms: 1.15x faster                                             |
| json_loads                 | 28.9 us                                                      | 25.3 us: 1.14x faster                                            |
| sympy_expand               | 553 ms                                                       | 496 ms: 1.12x faster                                             |
| sympy_integrate            | 25.8 ms                                                      | 23.2 ms: 1.11x faster                                            |
| mdp                        | 2.77 sec                                                     | 2.50 sec: 1.11x faster                                           |
| deltablue                  | 3.97 ms                                                      | 3.59 ms: 1.10x faster                                            |
| gc_traversal               | 4.15 ms                                                      | 3.76 ms: 1.10x faster                                            |
| regex_compile              | 156 ms                                                       | 142 ms: 1.10x faster                                             |
| unpickle_pure_python       | 238 us                                                       | 217 us: 1.10x faster                                             |
| nbody                      | 92.9 ms                                                      | 84.8 ms: 1.10x faster                                            |
| async_tree_none_tg         | 474 ms                                                       | 434 ms: 1.09x faster                                             |
| logging_simple             | 7.24 us                                                      | 6.63 us: 1.09x faster                                            |
| sqlglot_parse              | 1.51 ms                                                      | 1.39 ms: 1.09x faster                                            |
| async_tree_memoization_tg  | 600 ms                                                       | 551 ms: 1.09x faster                                             |
| async_tree_io              | 1.17 sec                                                     | 1.08 sec: 1.09x faster                                           |
| hexiom                     | 6.98 ms                                                      | 6.44 ms: 1.08x faster                                            |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 699 ms: 1.08x faster                                             |
| logging_silent             | 100 ns                                                       | 93.6 ns: 1.07x faster                                            |
| async_tree_io_tg           | 1.15 sec                                                     | 1.08 sec: 1.07x faster                                           |
| logging_format             | 7.71 us                                                      | 7.21 us: 1.07x faster                                            |
| chameleon                  | 7.92 ms                                                      | 7.42 ms: 1.07x faster                                            |
| thrift                     | 931 us                                                       | 873 us: 1.07x faster                                             |
| pickle_dict                | 32.3 us                                                      | 30.3 us: 1.07x faster                                            |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 705 ms: 1.06x faster                                             |
| sqlglot_normalize          | 122 ms                                                       | 115 ms: 1.06x faster                                             |
| sqlglot_transpile          | 1.91 ms                                                      | 1.80 ms: 1.06x faster                                            |
| mako                       | 11.0 ms                                                      | 10.4 ms: 1.06x faster                                            |
| deepcopy                   | 391 us                                                       | 369 us: 1.06x faster                                             |
| fannkuch                   | 416 ms                                                       | 393 ms: 1.06x faster                                             |
| json                       | 5.58 ms                                                      | 5.30 ms: 1.05x faster                                            |
| richards_super             | 63.6 ms                                                      | 60.8 ms: 1.05x faster                                            |
| xml_etree_parse            | 155 ms                                                       | 148 ms: 1.04x faster                                             |
| bench_thread_pool          | 1.00 ms                                                      | 958 us: 1.04x faster                                             |
| scimark_monte_carlo        | 69.8 ms                                                      | 67.0 ms: 1.04x faster                                            |
| meteor_contest             | 131 ms                                                       | 126 ms: 1.04x faster                                             |
| pprint_pformat             | 1.67 sec                                                     | 1.62 sec: 1.03x faster                                           |
| spectral_norm              | 95.1 ms                                                      | 92.5 ms: 1.03x faster                                            |
| django_template            | 39.3 ms                                                      | 38.4 ms: 1.02x faster                                            |
| genshi_xml                 | 57.1 ms                                                      | 55.8 ms: 1.02x faster                                            |
| pycparser                  | 1.31 sec                                                     | 1.28 sec: 1.02x faster                                           |
| xml_etree_iterparse        | 107 ms                                                       | 105 ms: 1.02x faster                                             |
| tornado_http               | 124 ms                                                       | 122 ms: 1.02x faster                                             |
| pprint_safe_repr           | 805 ms                                                       | 791 ms: 1.02x faster                                             |
| asyncio_websockets         | 390 ms                                                       | 385 ms: 1.01x faster                                             |
| deepcopy_memo              | 37.5 us                                                      | 37.2 us: 1.01x faster                                            |
| sqlglot_optimize           | 59.0 ms                                                      | 58.6 ms: 1.01x faster                                            |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.12 ms: 1.02x slower                                            |
| genshi_text                | 25.5 ms                                                      | 25.9 ms: 1.02x slower                                            |
| unpickle_list              | 4.60 us                                                      | 4.68 us: 1.02x slower                                            |
| 2to3                       | 287 ms                                                       | 292 ms: 1.02x slower                                             |
| create_gc_cycles           | 1.58 ms                                                      | 1.61 ms: 1.02x slower                                            |
| dulwich_log                | 67.4 ms                                                      | 69.0 ms: 1.02x slower                                            |
| xml_etree_process          | 55.9 ms                                                      | 57.7 ms: 1.03x slower                                            |
| pickle                     | 9.89 us                                                      | 10.3 us: 1.04x slower                                            |
| regex_effbot               | 3.34 ms                                                      | 3.48 ms: 1.04x slower                                            |
| pidigits                   | 251 ms                                                       | 262 ms: 1.04x slower                                             |
| float                      | 74.9 ms                                                      | 78.8 ms: 1.05x slower                                            |
| html5lib                   | 72.2 ms                                                      | 76.0 ms: 1.05x slower                                            |
| tomli_loads                | 2.25 sec                                                     | 2.38 sec: 1.06x slower                                           |
| regex_dna                  | 227 ms                                                       | 241 ms: 1.06x slower                                             |
| regex_v8                   | 24.4 ms                                                      | 26.0 ms: 1.06x slower                                            |
| xml_etree_generate         | 79.7 ms                                                      | 85.1 ms: 1.07x slower                                            |
| scimark_fft                | 281 ms                                                       | 301 ms: 1.07x slower                                             |
| gunicorn                   | 966 us                                                       | 1.04 ms: 1.08x slower                                            |
| aiohttp                    | 986 us                                                       | 1.06 ms: 1.08x slower                                            |
| go                         | 158 ms                                                       | 170 ms: 1.08x slower                                             |
| sqlite_synth               | 2.52 us                                                      | 2.73 us: 1.08x slower                                            |
| richards                   | 49.7 ms                                                      | 54.4 ms: 1.10x slower                                            |
| pickle_list                | 3.94 us                                                      | 4.33 us: 1.10x slower                                            |
| async_generators           | 322 ms                                                       | 359 ms: 1.12x slower                                             |
| pyflate                    | 449 ms                                                       | 506 ms: 1.13x slower                                             |
| mypy2                      | 762 ms                                                       | 867 ms: 1.14x slower                                             |
| unpickle                   | 13.3 us                                                      | 15.3 us: 1.15x slower                                            |
| python_startup             | 10.7 ms                                                      | 12.6 ms: 1.18x slower                                            |
| flaskblogging              | 3.88 ms                                                      | 4.58 ms: 1.18x slower                                            |
| telco                      | 6.81 ms                                                      | 8.16 ms: 1.20x slower                                            |
| coverage                   | 66.1 ms                                                      | 82.9 ms: 1.25x slower                                            |
| scimark_sor                | 110 ms                                                       | 146 ms: 1.34x slower                                             |
| python_startup_no_site     | 7.73 ms                                                      | 11.0 ms: 1.43x slower                                            |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                     |

Benchmark hidden because not significant (5): bench_mp_pool, docutils, pickle_pure_python, pathlib, deepcopy_reduce
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 0.99x