# Results vs. 3.11.0

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 2c964fa
- commit date: 2024-04-05
- overall geometric mean: 1.08x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 288 ms: 1.01x slower                                                                   |
| chameleon      | 7.92 ms                                                      | 7.47 ms: 1.06x faster                                                                  |
| docutils       | 2.85 sec                                                     | 2.98 sec: 1.05x slower                                                                 |
| html5lib       | 72.2 ms                                                      | 73.9 ms: 1.02x slower                                                                  |
| tornado_http   | 124 ms                                                       | 119 ms: 1.04x faster                                                                   |
| Geometric mean | (ref)                                                        | 1.01x faster                                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 416 ms: 1.44x faster                                                                   |
| async_tree_none_tg         | 474 ms                                                       | 334 ms: 1.42x faster                                                                   |
| async_tree_none            | 518 ms                                                       | 366 ms: 1.41x faster                                                                   |
| async_tree_memoization     | 629 ms                                                       | 460 ms: 1.37x faster                                                                   |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 573 ms: 1.31x faster                                                                   |
| async_tree_io_tg           | 1.15 sec                                                     | 885 ms: 1.30x faster                                                                   |
| async_tree_io              | 1.17 sec                                                     | 907 ms: 1.29x faster                                                                   |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 607 ms: 1.24x faster                                                                   |
| Geometric mean             | (ref)                                                        | 1.35x faster                                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| float          | 74.9 ms                                                      | 76.4 ms: 1.02x slower                                                                  |
| pidigits       | 251 ms                                                       | 262 ms: 1.04x slower                                                                   |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 141 ms: 1.11x faster                                                                   |
| regex_v8       | 24.4 ms                                                      | 25.4 ms: 1.04x slower                                                                  |
| regex_effbot   | 3.34 ms                                                      | 3.48 ms: 1.04x slower                                                                  |
| regex_dna      | 227 ms                                                       | 240 ms: 1.05x slower                                                                   |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                                  |
| json_loads           | 28.9 us                                                      | 25.5 us: 1.13x faster                                                                  |
| unpickle_pure_python | 238 us                                                       | 221 us: 1.08x faster                                                                   |
| pickle_dict          | 32.3 us                                                      | 30.4 us: 1.07x faster                                                                  |
| xml_etree_parse      | 155 ms                                                       | 148 ms: 1.05x faster                                                                   |
| pickle_pure_python   | 316 us                                                       | 307 us: 1.03x faster                                                                   |
| xml_etree_iterparse  | 107 ms                                                       | 104 ms: 1.02x faster                                                                   |
| tomli_loads          | 2.25 sec                                                     | 2.20 sec: 1.02x faster                                                                 |
| unpickle_list        | 4.60 us                                                      | 4.57 us: 1.01x faster                                                                  |
| xml_etree_process    | 55.9 ms                                                      | 57.6 ms: 1.03x slower                                                                  |
| pickle               | 9.89 us                                                      | 10.2 us: 1.03x slower                                                                  |
| xml_etree_generate   | 79.7 ms                                                      | 82.6 ms: 1.04x slower                                                                  |
| pickle_list          | 3.94 us                                                      | 4.29 us: 1.09x slower                                                                  |
| unpickle             | 13.3 us                                                      | 15.2 us: 1.14x slower                                                                  |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 12.8 ms: 1.19x slower                                                                  |
| python_startup_no_site | 7.73 ms                                                      | 11.0 ms: 1.43x slower                                                                  |
| Geometric mean         | (ref)                                                        | 1.30x slower                                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| mako           | 11.0 ms                                                      | 10.3 ms: 1.07x faster                                                                  |
| genshi_xml     | 57.1 ms                                                      | 53.5 ms: 1.07x faster                                                                  |
| genshi_text    | 25.5 ms                                                      | 24.7 ms: 1.03x faster                                                                  |
| Geometric mean | (ref)                                                        | 1.06x faster                                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 116 us: 4.60x faster                                                                   |
| asyncio_tcp                | 747 ms                                                       | 369 ms: 2.02x faster                                                                   |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.95x faster                                                                 |
| generators                 | 54.6 ms                                                      | 32.9 ms: 1.66x faster                                                                  |
| pylint                     | 514 ms                                                       | 318 ms: 1.62x faster                                                                   |
| comprehensions             | 25.1 us                                                      | 16.5 us: 1.52x faster                                                                  |
| async_tree_memoization_tg  | 600 ms                                                       | 416 ms: 1.44x faster                                                                   |
| async_tree_none_tg         | 474 ms                                                       | 334 ms: 1.42x faster                                                                   |
| async_tree_none            | 518 ms                                                       | 366 ms: 1.41x faster                                                                   |
| async_tree_memoization     | 629 ms                                                       | 460 ms: 1.37x faster                                                                   |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 573 ms: 1.31x faster                                                                   |
| async_tree_io_tg           | 1.15 sec                                                     | 885 ms: 1.30x faster                                                                   |
| async_tree_io              | 1.17 sec                                                     | 907 ms: 1.29x faster                                                                   |
| json_dumps                 | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                                  |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 607 ms: 1.24x faster                                                                   |
| chaos                      | 74.9 ms                                                      | 60.7 ms: 1.24x faster                                                                  |
| coroutines                 | 27.8 ms                                                      | 22.7 ms: 1.22x faster                                                                  |
| sympy_sum                  | 186 ms                                                       | 153 ms: 1.21x faster                                                                   |
| raytrace                   | 309 ms                                                       | 258 ms: 1.20x faster                                                                   |
| deltablue                  | 3.97 ms                                                      | 3.42 ms: 1.16x faster                                                                  |
| scimark_lu                 | 114 ms                                                       | 98.7 ms: 1.16x faster                                                                  |
| crypto_pyaes               | 83.3 ms                                                      | 72.4 ms: 1.15x faster                                                                  |
| nqueens                    | 103 ms                                                       | 89.5 ms: 1.15x faster                                                                  |
| sympy_str                  | 337 ms                                                       | 294 ms: 1.14x faster                                                                   |
| json_loads                 | 28.9 us                                                      | 25.5 us: 1.13x faster                                                                  |
| bench_thread_pool          | 1.00 ms                                                      | 886 us: 1.13x faster                                                                   |
| sympy_expand               | 553 ms                                                       | 495 ms: 1.12x faster                                                                   |
| logging_simple             | 7.24 us                                                      | 6.49 us: 1.12x faster                                                                  |
| sympy_integrate            | 25.8 ms                                                      | 23.3 ms: 1.11x faster                                                                  |
| regex_compile              | 156 ms                                                       | 141 ms: 1.11x faster                                                                   |
| mdp                        | 2.77 sec                                                     | 2.51 sec: 1.10x faster                                                                 |
| richards_super             | 63.6 ms                                                      | 58.3 ms: 1.09x faster                                                                  |
| fannkuch                   | 416 ms                                                       | 381 ms: 1.09x faster                                                                   |
| sqlglot_transpile          | 1.91 ms                                                      | 1.77 ms: 1.08x faster                                                                  |
| unpickle_pure_python       | 238 us                                                       | 221 us: 1.08x faster                                                                   |
| sqlglot_parse              | 1.51 ms                                                      | 1.41 ms: 1.08x faster                                                                  |
| spectral_norm              | 95.1 ms                                                      | 88.4 ms: 1.08x faster                                                                  |
| hexiom                     | 6.98 ms                                                      | 6.50 ms: 1.07x faster                                                                  |
| thrift                     | 931 us                                                       | 867 us: 1.07x faster                                                                   |
| mako                       | 11.0 ms                                                      | 10.3 ms: 1.07x faster                                                                  |
| logging_silent             | 100 ns                                                       | 94.0 ns: 1.07x faster                                                                  |
| genshi_xml                 | 57.1 ms                                                      | 53.5 ms: 1.07x faster                                                                  |
| logging_format             | 7.71 us                                                      | 7.24 us: 1.07x faster                                                                  |
| pickle_dict                | 32.3 us                                                      | 30.4 us: 1.07x faster                                                                  |
| chameleon                  | 7.92 ms                                                      | 7.47 ms: 1.06x faster                                                                  |
| dask                       | 410 ms                                                       | 389 ms: 1.05x faster                                                                   |
| sqlglot_normalize          | 122 ms                                                       | 116 ms: 1.05x faster                                                                   |
| xml_etree_parse            | 155 ms                                                       | 148 ms: 1.05x faster                                                                   |
| pprint_pformat             | 1.67 sec                                                     | 1.60 sec: 1.04x faster                                                                 |
| tornado_http               | 124 ms                                                       | 119 ms: 1.04x faster                                                                   |
| pycparser                  | 1.31 sec                                                     | 1.26 sec: 1.04x faster                                                                 |
| deepcopy                   | 391 us                                                       | 379 us: 1.03x faster                                                                   |
| genshi_text                | 25.5 ms                                                      | 24.7 ms: 1.03x faster                                                                  |
| pickle_pure_python         | 316 us                                                       | 307 us: 1.03x faster                                                                   |
| pprint_safe_repr           | 805 ms                                                       | 785 ms: 1.03x faster                                                                   |
| meteor_contest             | 131 ms                                                       | 127 ms: 1.03x faster                                                                   |
| scimark_monte_carlo        | 69.8 ms                                                      | 68.2 ms: 1.02x faster                                                                  |
| xml_etree_iterparse        | 107 ms                                                       | 104 ms: 1.02x faster                                                                   |
| tomli_loads                | 2.25 sec                                                     | 2.20 sec: 1.02x faster                                                                 |
| json                       | 5.58 ms                                                      | 5.48 ms: 1.02x faster                                                                  |
| sqlglot_optimize           | 59.0 ms                                                      | 58.1 ms: 1.01x faster                                                                  |
| deepcopy_memo              | 37.5 us                                                      | 37.2 us: 1.01x faster                                                                  |
| unpickle_list              | 4.60 us                                                      | 4.57 us: 1.01x faster                                                                  |
| 2to3                       | 287 ms                                                       | 288 ms: 1.01x slower                                                                   |
| pathlib                    | 18.9 ms                                                      | 19.1 ms: 1.01x slower                                                                  |
| dulwich_log                | 67.4 ms                                                      | 68.1 ms: 1.01x slower                                                                  |
| deepcopy_reduce            | 3.40 us                                                      | 3.43 us: 1.01x slower                                                                  |
| float                      | 74.9 ms                                                      | 76.4 ms: 1.02x slower                                                                  |
| html5lib                   | 72.2 ms                                                      | 73.9 ms: 1.02x slower                                                                  |
| xml_etree_process          | 55.9 ms                                                      | 57.6 ms: 1.03x slower                                                                  |
| pickle                     | 9.89 us                                                      | 10.2 us: 1.03x slower                                                                  |
| xml_etree_generate         | 79.7 ms                                                      | 82.6 ms: 1.04x slower                                                                  |
| richards                   | 49.7 ms                                                      | 51.7 ms: 1.04x slower                                                                  |
| regex_v8                   | 24.4 ms                                                      | 25.4 ms: 1.04x slower                                                                  |
| pidigits                   | 251 ms                                                       | 262 ms: 1.04x slower                                                                   |
| regex_effbot               | 3.34 ms                                                      | 3.48 ms: 1.04x slower                                                                  |
| docutils                   | 2.85 sec                                                     | 2.98 sec: 1.05x slower                                                                 |
| regex_dna                  | 227 ms                                                       | 240 ms: 1.05x slower                                                                   |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.35 ms: 1.07x slower                                                                  |
| gunicorn                   | 966 us                                                       | 1.04 ms: 1.08x slower                                                                  |
| sqlite_synth               | 2.52 us                                                      | 2.74 us: 1.09x slower                                                                  |
| pickle_list                | 3.94 us                                                      | 4.29 us: 1.09x slower                                                                  |
| aiohttp                    | 986 us                                                       | 1.08 ms: 1.09x slower                                                                  |
| go                         | 158 ms                                                       | 173 ms: 1.10x slower                                                                   |
| gc_traversal               | 4.15 ms                                                      | 4.60 ms: 1.11x slower                                                                  |
| async_generators           | 322 ms                                                       | 359 ms: 1.12x slower                                                                   |
| pyflate                    | 449 ms                                                       | 507 ms: 1.13x slower                                                                   |
| scimark_fft                | 281 ms                                                       | 320 ms: 1.14x slower                                                                   |
| unpickle                   | 13.3 us                                                      | 15.2 us: 1.14x slower                                                                  |
| telco                      | 6.81 ms                                                      | 7.91 ms: 1.16x slower                                                                  |
| python_startup             | 10.7 ms                                                      | 12.8 ms: 1.19x slower                                                                  |
| create_gc_cycles           | 1.58 ms                                                      | 1.92 ms: 1.22x slower                                                                  |
| scimark_sor                | 110 ms                                                       | 139 ms: 1.27x slower                                                                   |
| coverage                   | 66.1 ms                                                      | 89.1 ms: 1.35x slower                                                                  |
| python_startup_no_site     | 7.73 ms                                                      | 11.0 ms: 1.43x slower                                                                  |
| Geometric mean             | (ref)                                                        | 1.08x faster                                                                           |

Benchmark hidden because not significant (4): bench_mp_pool, nbody, mypy2, asyncio_websockets
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.02x