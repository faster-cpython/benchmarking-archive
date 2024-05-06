# Results vs. 3.11.0

- fork: python
- ref: c43f6a4dfaa1c1974141
- machine: linux-x86_64
- commit hash: c43f6a4
- commit date: 2024-04-03
- overall geometric mean: 1.05x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 320 ms: 1.12x slower                                                         |
| chameleon      | 7.92 ms                                                      | 8.00 ms: 1.01x slower                                                        |
| docutils       | 2.85 sec                                                     | 3.29 sec: 1.16x slower                                                       |
| html5lib       | 72.2 ms                                                      | 79.1 ms: 1.10x slower                                                        |
| tornado_http   | 124 ms                                                       | 128 ms: 1.03x slower                                                         |
| Geometric mean | (ref)                                                        | 1.08x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 436 ms: 1.37x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 346 ms: 1.37x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 459 ms: 1.37x faster                                                         |
| async_tree_none            | 518 ms                                                       | 394 ms: 1.32x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 882 ms: 1.31x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 905 ms: 1.29x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 601 ms: 1.25x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 623 ms: 1.21x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.31x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 265 ms: 1.05x slower                                                         |
| float          | 74.9 ms                                                      | 101 ms: 1.34x slower                                                         |
| nbody          | 92.9 ms                                                      | 130 ms: 1.40x slower                                                         |
| Geometric mean | (ref)                                                        | 1.26x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 227 ms                                                       | 239 ms: 1.05x slower                                                         |
| regex_effbot   | 3.34 ms                                                      | 3.54 ms: 1.06x slower                                                        |
| regex_v8       | 24.4 ms                                                      | 26.6 ms: 1.09x slower                                                        |
| regex_compile  | 156 ms                                                       | 208 ms: 1.33x slower                                                         |
| Geometric mean | (ref)                                                        | 1.13x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                        |
| json_loads           | 28.9 us                                                      | 25.2 us: 1.15x faster                                                        |
| xml_etree_parse      | 155 ms                                                       | 147 ms: 1.05x faster                                                         |
| pickle_dict          | 32.3 us                                                      | 32.7 us: 1.01x slower                                                        |
| pickle_pure_python   | 316 us                                                       | 324 us: 1.03x slower                                                         |
| unpickle_list        | 4.60 us                                                      | 4.77 us: 1.04x slower                                                        |
| xml_etree_iterparse  | 107 ms                                                       | 114 ms: 1.07x slower                                                         |
| pickle               | 9.89 us                                                      | 10.8 us: 1.10x slower                                                        |
| pickle_list          | 3.94 us                                                      | 4.46 us: 1.13x slower                                                        |
| unpickle             | 13.3 us                                                      | 15.3 us: 1.15x slower                                                        |
| xml_etree_process    | 55.9 ms                                                      | 64.6 ms: 1.16x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 93.8 ms: 1.18x slower                                                        |
| tomli_loads          | 2.25 sec                                                     | 2.89 sec: 1.28x slower                                                       |
| unpickle_pure_python | 238 us                                                       | 310 us: 1.30x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.07x slower                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 12.9 ms: 1.20x slower                                                        |
| python_startup_no_site | 7.73 ms                                                      | 11.2 ms: 1.45x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.32x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_xml     | 57.1 ms                                                      | 62.2 ms: 1.09x slower                                                        |
| genshi_text    | 25.5 ms                                                      | 27.9 ms: 1.09x slower                                                        |
| mako           | 11.0 ms                                                      | 14.0 ms: 1.27x slower                                                        |
| Geometric mean | (ref)                                                        | 1.15x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 126 us: 4.22x faster                                                         |
| asyncio_tcp                | 747 ms                                                       | 379 ms: 1.97x faster                                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.60 sec: 1.92x faster                                                       |
| generators                 | 54.6 ms                                                      | 33.0 ms: 1.66x faster                                                        |
| pylint                     | 514 ms                                                       | 346 ms: 1.48x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 436 ms: 1.37x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 346 ms: 1.37x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 459 ms: 1.37x faster                                                         |
| async_tree_none            | 518 ms                                                       | 394 ms: 1.32x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 882 ms: 1.31x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 905 ms: 1.29x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 601 ms: 1.25x faster                                                         |
| coroutines                 | 27.8 ms                                                      | 22.3 ms: 1.24x faster                                                        |
| json_dumps                 | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 623 ms: 1.21x faster                                                         |
| json_loads                 | 28.9 us                                                      | 25.2 us: 1.15x faster                                                        |
| logging_simple             | 7.24 us                                                      | 6.63 us: 1.09x faster                                                        |
| xml_etree_parse            | 155 ms                                                       | 147 ms: 1.05x faster                                                         |
| logging_format             | 7.71 us                                                      | 7.33 us: 1.05x faster                                                        |
| thrift                     | 931 us                                                       | 893 us: 1.04x faster                                                         |
| json                       | 5.58 ms                                                      | 5.38 ms: 1.04x faster                                                        |
| sympy_sum                  | 186 ms                                                       | 180 ms: 1.03x faster                                                         |
| mdp                        | 2.77 sec                                                     | 2.68 sec: 1.03x faster                                                       |
| logging_silent             | 100 ns                                                       | 99.4 ns: 1.01x faster                                                        |
| chameleon                  | 7.92 ms                                                      | 8.00 ms: 1.01x slower                                                        |
| pickle_dict                | 32.3 us                                                      | 32.7 us: 1.01x slower                                                        |
| asyncio_websockets         | 390 ms                                                       | 395 ms: 1.01x slower                                                         |
| chaos                      | 74.9 ms                                                      | 75.9 ms: 1.01x slower                                                        |
| dask                       | 410 ms                                                       | 416 ms: 1.02x slower                                                         |
| pickle_pure_python         | 316 us                                                       | 324 us: 1.03x slower                                                         |
| tornado_http               | 124 ms                                                       | 128 ms: 1.03x slower                                                         |
| unpickle_list              | 4.60 us                                                      | 4.77 us: 1.04x slower                                                        |
| sqlglot_parse              | 1.51 ms                                                      | 1.57 ms: 1.04x slower                                                        |
| sqlglot_transpile          | 1.91 ms                                                      | 1.99 ms: 1.04x slower                                                        |
| sympy_str                  | 337 ms                                                       | 350 ms: 1.04x slower                                                         |
| pycparser                  | 1.31 sec                                                     | 1.36 sec: 1.04x slower                                                       |
| sympy_integrate            | 25.8 ms                                                      | 26.9 ms: 1.04x slower                                                        |
| gc_traversal               | 4.15 ms                                                      | 4.35 ms: 1.05x slower                                                        |
| regex_dna                  | 227 ms                                                       | 239 ms: 1.05x slower                                                         |
| pidigits                   | 251 ms                                                       | 265 ms: 1.05x slower                                                         |
| sympy_expand               | 553 ms                                                       | 584 ms: 1.06x slower                                                         |
| bench_mp_pool              | 4.70 ms                                                      | 4.97 ms: 1.06x slower                                                        |
| deepcopy_reduce            | 3.40 us                                                      | 3.59 us: 1.06x slower                                                        |
| richards_super             | 63.6 ms                                                      | 67.4 ms: 1.06x slower                                                        |
| regex_effbot               | 3.34 ms                                                      | 3.54 ms: 1.06x slower                                                        |
| comprehensions             | 25.1 us                                                      | 26.7 us: 1.06x slower                                                        |
| sqlglot_normalize          | 122 ms                                                       | 130 ms: 1.07x slower                                                         |
| deepcopy                   | 391 us                                                       | 417 us: 1.07x slower                                                         |
| xml_etree_iterparse        | 107 ms                                                       | 114 ms: 1.07x slower                                                         |
| pathlib                    | 18.9 ms                                                      | 20.3 ms: 1.07x slower                                                        |
| raytrace                   | 309 ms                                                       | 336 ms: 1.09x slower                                                         |
| regex_v8                   | 24.4 ms                                                      | 26.6 ms: 1.09x slower                                                        |
| genshi_xml                 | 57.1 ms                                                      | 62.2 ms: 1.09x slower                                                        |
| genshi_text                | 25.5 ms                                                      | 27.9 ms: 1.09x slower                                                        |
| html5lib                   | 72.2 ms                                                      | 79.1 ms: 1.10x slower                                                        |
| meteor_contest             | 131 ms                                                       | 143 ms: 1.10x slower                                                         |
| pickle                     | 9.89 us                                                      | 10.8 us: 1.10x slower                                                        |
| crypto_pyaes               | 83.3 ms                                                      | 92.2 ms: 1.11x slower                                                        |
| 2to3                       | 287 ms                                                       | 320 ms: 1.12x slower                                                         |
| pickle_list                | 3.94 us                                                      | 4.46 us: 1.13x slower                                                        |
| mypy2                      | 762 ms                                                       | 862 ms: 1.13x slower                                                         |
| sqlite_synth               | 2.52 us                                                      | 2.87 us: 1.14x slower                                                        |
| bench_thread_pool          | 1.00 ms                                                      | 1.14 ms: 1.14x slower                                                        |
| sqlglot_optimize           | 59.0 ms                                                      | 67.5 ms: 1.14x slower                                                        |
| aiohttp                    | 986 us                                                       | 1.13 ms: 1.15x slower                                                        |
| unpickle                   | 13.3 us                                                      | 15.3 us: 1.15x slower                                                        |
| dulwich_log                | 67.4 ms                                                      | 77.8 ms: 1.15x slower                                                        |
| gunicorn                   | 966 us                                                       | 1.12 ms: 1.16x slower                                                        |
| xml_etree_process          | 55.9 ms                                                      | 64.6 ms: 1.16x slower                                                        |
| docutils                   | 2.85 sec                                                     | 3.29 sec: 1.16x slower                                                       |
| xml_etree_generate         | 79.7 ms                                                      | 93.8 ms: 1.18x slower                                                        |
| nqueens                    | 103 ms                                                       | 122 ms: 1.19x slower                                                         |
| python_startup             | 10.7 ms                                                      | 12.9 ms: 1.20x slower                                                        |
| deepcopy_memo              | 37.5 us                                                      | 45.1 us: 1.20x slower                                                        |
| pprint_pformat             | 1.67 sec                                                     | 2.01 sec: 1.21x slower                                                       |
| async_generators           | 322 ms                                                       | 391 ms: 1.22x slower                                                         |
| telco                      | 6.81 ms                                                      | 8.29 ms: 1.22x slower                                                        |
| pprint_safe_repr           | 805 ms                                                       | 983 ms: 1.22x slower                                                         |
| create_gc_cycles           | 1.58 ms                                                      | 1.94 ms: 1.23x slower                                                        |
| richards                   | 49.7 ms                                                      | 61.0 ms: 1.23x slower                                                        |
| fannkuch                   | 416 ms                                                       | 520 ms: 1.25x slower                                                         |
| mako                       | 11.0 ms                                                      | 14.0 ms: 1.27x slower                                                        |
| tomli_loads                | 2.25 sec                                                     | 2.89 sec: 1.28x slower                                                       |
| go                         | 158 ms                                                       | 205 ms: 1.30x slower                                                         |
| unpickle_pure_python       | 238 us                                                       | 310 us: 1.30x slower                                                         |
| scimark_lu                 | 114 ms                                                       | 149 ms: 1.31x slower                                                         |
| coverage                   | 66.1 ms                                                      | 87.6 ms: 1.32x slower                                                        |
| regex_compile              | 156 ms                                                       | 208 ms: 1.33x slower                                                         |
| float                      | 74.9 ms                                                      | 101 ms: 1.34x slower                                                         |
| nbody                      | 92.9 ms                                                      | 130 ms: 1.40x slower                                                         |
| scimark_monte_carlo        | 69.8 ms                                                      | 99.0 ms: 1.42x slower                                                        |
| pyflate                    | 449 ms                                                       | 649 ms: 1.45x slower                                                         |
| python_startup_no_site     | 7.73 ms                                                      | 11.2 ms: 1.45x slower                                                        |
| hexiom                     | 6.98 ms                                                      | 10.8 ms: 1.55x slower                                                        |
| scimark_fft                | 281 ms                                                       | 437 ms: 1.56x slower                                                         |
| scimark_sor                | 110 ms                                                       | 172 ms: 1.57x slower                                                         |
| spectral_norm              | 95.1 ms                                                      | 154 ms: 1.62x slower                                                         |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 6.68 ms: 1.64x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.05x slower                                                                 |

Benchmark hidden because not significant (1): deltablue
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.03x