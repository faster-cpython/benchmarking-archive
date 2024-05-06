# Results vs. 3.11.0

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: b64de3d
- commit date: 2024-05-03
- overall geometric mean: 1.06x faster
- HPT reliability: 98.45%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 291 ms: 1.01x slower                                                                   |
| chameleon      | 7.92 ms                                                      | 7.52 ms: 1.05x faster                                                                  |
| docutils       | 2.85 sec                                                     | 3.02 sec: 1.06x slower                                                                 |
| html5lib       | 72.2 ms                                                      | 75.9 ms: 1.05x slower                                                                  |
| tornado_http   | 124 ms                                                       | 119 ms: 1.04x faster                                                                   |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| async_tree_none            | 518 ms                                                       | 376 ms: 1.38x faster                                                                   |
| async_tree_none_tg         | 474 ms                                                       | 347 ms: 1.37x faster                                                                   |
| async_tree_memoization_tg  | 600 ms                                                       | 445 ms: 1.35x faster                                                                   |
| async_tree_memoization     | 629 ms                                                       | 475 ms: 1.33x faster                                                                   |
| async_tree_io              | 1.17 sec                                                     | 907 ms: 1.29x faster                                                                   |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 588 ms: 1.28x faster                                                                   |
| async_tree_io_tg           | 1.15 sec                                                     | 913 ms: 1.26x faster                                                                   |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 622 ms: 1.21x faster                                                                   |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 255 ms: 1.01x slower                                                                   |
| float          | 74.9 ms                                                      | 80.9 ms: 1.08x slower                                                                  |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 143 ms: 1.09x faster                                                                   |
| regex_dna      | 227 ms                                                       | 237 ms: 1.04x slower                                                                   |
| regex_v8       | 24.4 ms                                                      | 25.6 ms: 1.05x slower                                                                  |
| regex_effbot   | 3.34 ms                                                      | 3.52 ms: 1.05x slower                                                                  |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 11.1 ms: 1.20x faster                                                                  |
| json_loads           | 28.9 us                                                      | 24.6 us: 1.18x faster                                                                  |
| unpickle_pure_python | 238 us                                                       | 213 us: 1.12x faster                                                                   |
| xml_etree_parse      | 155 ms                                                       | 145 ms: 1.06x faster                                                                   |
| xml_etree_iterparse  | 107 ms                                                       | 104 ms: 1.03x faster                                                                   |
| pickle_dict          | 32.3 us                                                      | 32.9 us: 1.02x slower                                                                  |
| unpickle_list        | 4.60 us                                                      | 4.68 us: 1.02x slower                                                                  |
| pickle_pure_python   | 316 us                                                       | 326 us: 1.03x slower                                                                   |
| xml_etree_process    | 55.9 ms                                                      | 59.1 ms: 1.06x slower                                                                  |
| tomli_loads          | 2.25 sec                                                     | 2.38 sec: 1.06x slower                                                                 |
| xml_etree_generate   | 79.7 ms                                                      | 84.7 ms: 1.06x slower                                                                  |
| pickle               | 9.89 us                                                      | 10.9 us: 1.10x slower                                                                  |
| unpickle             | 13.3 us                                                      | 15.1 us: 1.14x slower                                                                  |
| pickle_list          | 3.94 us                                                      | 4.49 us: 1.14x slower                                                                  |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 8.80 ms: 1.14x slower                                                                  |
| python_startup         | 10.7 ms                                                      | 12.8 ms: 1.20x slower                                                                  |
| Geometric mean         | (ref)                                                        | 1.17x slower                                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| genshi_xml     | 57.1 ms                                                      | 53.3 ms: 1.07x faster                                                                  |
| mako           | 11.0 ms                                                      | 10.4 ms: 1.05x faster                                                                  |
| genshi_text    | 25.5 ms                                                      | 24.8 ms: 1.03x faster                                                                  |
| Geometric mean | (ref)                                                        | 1.04x faster                                                                           |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-b64de3d |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 175 us: 3.05x faster                                                                   |
| asyncio_tcp                | 747 ms                                                       | 373 ms: 2.00x faster                                                                   |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                                 |
| generators                 | 54.6 ms                                                      | 33.6 ms: 1.62x faster                                                                  |
| pylint                     | 514 ms                                                       | 345 ms: 1.49x faster                                                                   |
| comprehensions             | 25.1 us                                                      | 17.1 us: 1.47x faster                                                                  |
| async_tree_none            | 518 ms                                                       | 376 ms: 1.38x faster                                                                   |
| async_tree_none_tg         | 474 ms                                                       | 347 ms: 1.37x faster                                                                   |
| async_tree_memoization_tg  | 600 ms                                                       | 445 ms: 1.35x faster                                                                   |
| async_tree_memoization     | 629 ms                                                       | 475 ms: 1.33x faster                                                                   |
| coroutines                 | 27.8 ms                                                      | 21.5 ms: 1.29x faster                                                                  |
| async_tree_io              | 1.17 sec                                                     | 907 ms: 1.29x faster                                                                   |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 588 ms: 1.28x faster                                                                   |
| async_tree_io_tg           | 1.15 sec                                                     | 913 ms: 1.26x faster                                                                   |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 622 ms: 1.21x faster                                                                   |
| chaos                      | 74.9 ms                                                      | 62.1 ms: 1.21x faster                                                                  |
| sympy_sum                  | 186 ms                                                       | 154 ms: 1.20x faster                                                                   |
| json_dumps                 | 13.3 ms                                                      | 11.1 ms: 1.20x faster                                                                  |
| json_loads                 | 28.9 us                                                      | 24.6 us: 1.18x faster                                                                  |
| go                         | 158 ms                                                       | 134 ms: 1.17x faster                                                                   |
| deltablue                  | 3.97 ms                                                      | 3.46 ms: 1.15x faster                                                                  |
| fannkuch                   | 416 ms                                                       | 362 ms: 1.15x faster                                                                   |
| scimark_lu                 | 114 ms                                                       | 99.5 ms: 1.15x faster                                                                  |
| raytrace                   | 309 ms                                                       | 270 ms: 1.15x faster                                                                   |
| nqueens                    | 103 ms                                                       | 90.2 ms: 1.14x faster                                                                  |
| sympy_str                  | 337 ms                                                       | 298 ms: 1.13x faster                                                                   |
| unpickle_pure_python       | 238 us                                                       | 213 us: 1.12x faster                                                                   |
| bench_thread_pool          | 1.00 ms                                                      | 897 us: 1.12x faster                                                                   |
| mdp                        | 2.77 sec                                                     | 2.50 sec: 1.11x faster                                                                 |
| sympy_integrate            | 25.8 ms                                                      | 23.4 ms: 1.10x faster                                                                  |
| hexiom                     | 6.98 ms                                                      | 6.38 ms: 1.09x faster                                                                  |
| sympy_expand               | 553 ms                                                       | 506 ms: 1.09x faster                                                                   |
| regex_compile              | 156 ms                                                       | 143 ms: 1.09x faster                                                                   |
| sqlglot_parse              | 1.51 ms                                                      | 1.39 ms: 1.09x faster                                                                  |
| pathlib                    | 18.9 ms                                                      | 17.5 ms: 1.08x faster                                                                  |
| richards_super             | 63.6 ms                                                      | 58.8 ms: 1.08x faster                                                                  |
| sqlglot_transpile          | 1.91 ms                                                      | 1.78 ms: 1.08x faster                                                                  |
| genshi_xml                 | 57.1 ms                                                      | 53.3 ms: 1.07x faster                                                                  |
| xml_etree_parse            | 155 ms                                                       | 145 ms: 1.06x faster                                                                   |
| logging_simple             | 7.24 us                                                      | 6.81 us: 1.06x faster                                                                  |
| chameleon                  | 7.92 ms                                                      | 7.52 ms: 1.05x faster                                                                  |
| mako                       | 11.0 ms                                                      | 10.4 ms: 1.05x faster                                                                  |
| dask                       | 410 ms                                                       | 392 ms: 1.04x faster                                                                   |
| tornado_http               | 124 ms                                                       | 119 ms: 1.04x faster                                                                   |
| pycparser                  | 1.31 sec                                                     | 1.26 sec: 1.04x faster                                                                 |
| json                       | 5.58 ms                                                      | 5.38 ms: 1.04x faster                                                                  |
| thrift                     | 931 us                                                       | 898 us: 1.04x faster                                                                   |
| deepcopy                   | 391 us                                                       | 378 us: 1.04x faster                                                                   |
| xml_etree_iterparse        | 107 ms                                                       | 104 ms: 1.03x faster                                                                   |
| genshi_text                | 25.5 ms                                                      | 24.8 ms: 1.03x faster                                                                  |
| logging_silent             | 100 ns                                                       | 98.0 ns: 1.02x faster                                                                  |
| dulwich_log                | 67.4 ms                                                      | 66.2 ms: 1.02x faster                                                                  |
| crypto_pyaes               | 83.3 ms                                                      | 82.0 ms: 1.02x faster                                                                  |
| deepcopy_reduce            | 3.40 us                                                      | 3.43 us: 1.01x slower                                                                  |
| pprint_safe_repr           | 805 ms                                                       | 814 ms: 1.01x slower                                                                   |
| asyncio_websockets         | 390 ms                                                       | 395 ms: 1.01x slower                                                                   |
| pidigits                   | 251 ms                                                       | 255 ms: 1.01x slower                                                                   |
| 2to3                       | 287 ms                                                       | 291 ms: 1.01x slower                                                                   |
| pickle_dict                | 32.3 us                                                      | 32.9 us: 1.02x slower                                                                  |
| unpickle_list              | 4.60 us                                                      | 4.68 us: 1.02x slower                                                                  |
| sqlglot_optimize           | 59.0 ms                                                      | 60.1 ms: 1.02x slower                                                                  |
| mypy2                      | 762 ms                                                       | 778 ms: 1.02x slower                                                                   |
| richards                   | 49.7 ms                                                      | 51.2 ms: 1.03x slower                                                                  |
| pickle_pure_python         | 316 us                                                       | 326 us: 1.03x slower                                                                   |
| regex_dna                  | 227 ms                                                       | 237 ms: 1.04x slower                                                                   |
| regex_v8                   | 24.4 ms                                                      | 25.6 ms: 1.05x slower                                                                  |
| html5lib                   | 72.2 ms                                                      | 75.9 ms: 1.05x slower                                                                  |
| pyflate                    | 449 ms                                                       | 474 ms: 1.05x slower                                                                   |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.29 ms: 1.05x slower                                                                  |
| regex_effbot               | 3.34 ms                                                      | 3.52 ms: 1.05x slower                                                                  |
| xml_etree_process          | 55.9 ms                                                      | 59.1 ms: 1.06x slower                                                                  |
| scimark_monte_carlo        | 69.8 ms                                                      | 73.8 ms: 1.06x slower                                                                  |
| tomli_loads                | 2.25 sec                                                     | 2.38 sec: 1.06x slower                                                                 |
| spectral_norm              | 95.1 ms                                                      | 101 ms: 1.06x slower                                                                   |
| docutils                   | 2.85 sec                                                     | 3.02 sec: 1.06x slower                                                                 |
| xml_etree_generate         | 79.7 ms                                                      | 84.7 ms: 1.06x slower                                                                  |
| float                      | 74.9 ms                                                      | 80.9 ms: 1.08x slower                                                                  |
| gunicorn                   | 966 us                                                       | 1.05 ms: 1.09x slower                                                                  |
| pickle                     | 9.89 us                                                      | 10.9 us: 1.10x slower                                                                  |
| aiohttp                    | 986 us                                                       | 1.09 ms: 1.11x slower                                                                  |
| sqlite_synth               | 2.52 us                                                      | 2.82 us: 1.12x slower                                                                  |
| scimark_fft                | 281 ms                                                       | 317 ms: 1.13x slower                                                                   |
| python_startup_no_site     | 7.73 ms                                                      | 8.80 ms: 1.14x slower                                                                  |
| unpickle                   | 13.3 us                                                      | 15.1 us: 1.14x slower                                                                  |
| pickle_list                | 3.94 us                                                      | 4.49 us: 1.14x slower                                                                  |
| async_generators           | 322 ms                                                       | 368 ms: 1.14x slower                                                                   |
| gc_traversal               | 4.15 ms                                                      | 4.82 ms: 1.16x slower                                                                  |
| coverage                   | 66.1 ms                                                      | 77.4 ms: 1.17x slower                                                                  |
| scimark_sor                | 110 ms                                                       | 130 ms: 1.19x slower                                                                   |
| python_startup             | 10.7 ms                                                      | 12.8 ms: 1.20x slower                                                                  |
| telco                      | 6.81 ms                                                      | 8.27 ms: 1.21x slower                                                                  |
| flaskblogging              | 3.88 ms                                                      | 4.75 ms: 1.22x slower                                                                  |
| create_gc_cycles           | 1.58 ms                                                      | 2.01 ms: 1.27x slower                                                                  |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                                           |

Benchmark hidden because not significant (8): nbody, bench_mp_pool, logging_format, pprint_pformat, deepcopy_memo, sqlglot_normalize, meteor_contest, django_template
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 98.45% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x