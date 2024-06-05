# Results vs. 3.11.0

- fork: python
- ref: 6725c78d376eadb01a9d
- machine: linux-x86_64
- commit hash: 6725c78
- commit date: 2024-06-04
- overall geometric mean: 1.09x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 346 ms: 1.21x slower                                                         |
| chameleon      | 7.92 ms                                                      | 8.73 ms: 1.10x slower                                                        |
| docutils       | 2.85 sec                                                     | 3.48 sec: 1.22x slower                                                       |
| html5lib       | 72.2 ms                                                      | 89.0 ms: 1.23x slower                                                        |
| tornado_http   | 124 ms                                                       | 130 ms: 1.05x slower                                                         |
| Geometric mean | (ref)                                                        | 1.16x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.15 sec                                                     | 881 ms: 1.31x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 480 ms: 1.31x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 461 ms: 1.30x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 367 ms: 1.29x faster                                                         |
| async_tree_none            | 518 ms                                                       | 402 ms: 1.29x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 921 ms: 1.27x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 619 ms: 1.21x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 656 ms: 1.15x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.27x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 254 ms: 1.01x slower                                                         |
| float          | 74.9 ms                                                      | 97.4 ms: 1.30x slower                                                        |
| nbody          | 92.9 ms                                                      | 125 ms: 1.35x slower                                                         |
| Geometric mean | (ref)                                                        | 1.21x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                      | 26.5 ms: 1.08x slower                                                        |
| regex_dna      | 227 ms                                                       | 247 ms: 1.09x slower                                                         |
| regex_effbot   | 3.34 ms                                                      | 3.63 ms: 1.09x slower                                                        |
| regex_compile  | 156 ms                                                       | 216 ms: 1.38x slower                                                         |
| Geometric mean | (ref)                                                        | 1.15x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_loads           | 28.9 us                                                      | 24.4 us: 1.18x faster                                                        |
| json_dumps           | 13.3 ms                                                      | 11.4 ms: 1.17x faster                                                        |
| xml_etree_parse      | 155 ms                                                       | 148 ms: 1.04x faster                                                         |
| pickle_dict          | 32.3 us                                                      | 32.9 us: 1.02x slower                                                        |
| unpickle_list        | 4.60 us                                                      | 4.81 us: 1.05x slower                                                        |
| xml_etree_iterparse  | 107 ms                                                       | 115 ms: 1.08x slower                                                         |
| pickle               | 9.89 us                                                      | 10.8 us: 1.09x slower                                                        |
| unpickle             | 13.3 us                                                      | 15.0 us: 1.13x slower                                                        |
| pickle_list          | 3.94 us                                                      | 4.49 us: 1.14x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 96.7 ms: 1.21x slower                                                        |
| xml_etree_process    | 55.9 ms                                                      | 69.0 ms: 1.24x slower                                                        |
| unpickle_pure_python | 238 us                                                       | 305 us: 1.28x slower                                                         |
| tomli_loads          | 2.25 sec                                                     | 2.94 sec: 1.31x slower                                                       |
| pickle_pure_python   | 316 us                                                       | 434 us: 1.38x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.10x slower                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 8.92 ms: 1.15x slower                                                        |
| python_startup         | 10.7 ms                                                      | 13.3 ms: 1.24x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.20x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 39.3 ms                                                      | 46.4 ms: 1.18x slower                                                        |
| genshi_xml      | 57.1 ms                                                      | 70.3 ms: 1.23x slower                                                        |
| genshi_text     | 25.5 ms                                                      | 33.3 ms: 1.31x slower                                                        |
| mako            | 11.0 ms                                                      | 14.5 ms: 1.32x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.26x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240604-pythonperf2-x86_64-python-6725c78d376eadb01a9d-3.13.0b1+-6725c78 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 199 us: 2.67x faster                                                         |
| asyncio_tcp                | 747 ms                                                       | 389 ms: 1.92x faster                                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.60 sec: 1.91x faster                                                       |
| generators                 | 54.6 ms                                                      | 34.3 ms: 1.59x faster                                                        |
| async_tree_io_tg           | 1.15 sec                                                     | 881 ms: 1.31x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 480 ms: 1.31x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 461 ms: 1.30x faster                                                         |
| pylint                     | 514 ms                                                       | 396 ms: 1.30x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 367 ms: 1.29x faster                                                         |
| async_tree_none            | 518 ms                                                       | 402 ms: 1.29x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 921 ms: 1.27x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 619 ms: 1.21x faster                                                         |
| coroutines                 | 27.8 ms                                                      | 23.0 ms: 1.21x faster                                                        |
| json_loads                 | 28.9 us                                                      | 24.4 us: 1.18x faster                                                        |
| json_dumps                 | 13.3 ms                                                      | 11.4 ms: 1.17x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 656 ms: 1.15x faster                                                         |
| logging_simple             | 7.24 us                                                      | 6.84 us: 1.06x faster                                                        |
| xml_etree_parse            | 155 ms                                                       | 148 ms: 1.04x faster                                                         |
| logging_format             | 7.71 us                                                      | 7.48 us: 1.03x faster                                                        |
| pathlib                    | 18.9 ms                                                      | 18.4 ms: 1.03x faster                                                        |
| thrift                     | 931 us                                                       | 907 us: 1.03x faster                                                         |
| pidigits                   | 251 ms                                                       | 254 ms: 1.01x slower                                                         |
| pickle_dict                | 32.3 us                                                      | 32.9 us: 1.02x slower                                                        |
| sympy_sum                  | 186 ms                                                       | 189 ms: 1.02x slower                                                         |
| dask                       | 410 ms                                                       | 426 ms: 1.04x slower                                                         |
| tornado_http               | 124 ms                                                       | 130 ms: 1.05x slower                                                         |
| unpickle_list              | 4.60 us                                                      | 4.81 us: 1.05x slower                                                        |
| bench_mp_pool              | 4.70 ms                                                      | 5.00 ms: 1.06x slower                                                        |
| raytrace                   | 309 ms                                                       | 333 ms: 1.07x slower                                                         |
| xml_etree_iterparse        | 107 ms                                                       | 115 ms: 1.08x slower                                                         |
| chaos                      | 74.9 ms                                                      | 81.1 ms: 1.08x slower                                                        |
| regex_v8                   | 24.4 ms                                                      | 26.5 ms: 1.08x slower                                                        |
| regex_dna                  | 227 ms                                                       | 247 ms: 1.09x slower                                                         |
| regex_effbot               | 3.34 ms                                                      | 3.63 ms: 1.09x slower                                                        |
| sympy_integrate            | 25.8 ms                                                      | 28.1 ms: 1.09x slower                                                        |
| pickle                     | 9.89 us                                                      | 10.8 us: 1.09x slower                                                        |
| richards_super             | 63.6 ms                                                      | 70.1 ms: 1.10x slower                                                        |
| chameleon                  | 7.92 ms                                                      | 8.73 ms: 1.10x slower                                                        |
| sympy_str                  | 337 ms                                                       | 372 ms: 1.10x slower                                                         |
| meteor_contest             | 131 ms                                                       | 144 ms: 1.10x slower                                                         |
| comprehensions             | 25.1 us                                                      | 27.8 us: 1.11x slower                                                        |
| crypto_pyaes               | 83.3 ms                                                      | 92.6 ms: 1.11x slower                                                        |
| pycparser                  | 1.31 sec                                                     | 1.46 sec: 1.12x slower                                                       |
| sympy_expand               | 553 ms                                                       | 625 ms: 1.13x slower                                                         |
| gc_traversal               | 4.15 ms                                                      | 4.70 ms: 1.13x slower                                                        |
| unpickle                   | 13.3 us                                                      | 15.0 us: 1.13x slower                                                        |
| pickle_list                | 3.94 us                                                      | 4.49 us: 1.14x slower                                                        |
| sqlite_synth               | 2.52 us                                                      | 2.87 us: 1.14x slower                                                        |
| sqlglot_parse              | 1.51 ms                                                      | 1.73 ms: 1.15x slower                                                        |
| sqlglot_transpile          | 1.91 ms                                                      | 2.19 ms: 1.15x slower                                                        |
| python_startup_no_site     | 7.73 ms                                                      | 8.92 ms: 1.15x slower                                                        |
| deltablue                  | 3.97 ms                                                      | 4.60 ms: 1.16x slower                                                        |
| nqueens                    | 103 ms                                                       | 120 ms: 1.17x slower                                                         |
| fannkuch                   | 416 ms                                                       | 490 ms: 1.18x slower                                                         |
| django_template            | 39.3 ms                                                      | 46.4 ms: 1.18x slower                                                        |
| sqlglot_normalize          | 122 ms                                                       | 144 ms: 1.19x slower                                                         |
| dulwich_log                | 67.4 ms                                                      | 80.2 ms: 1.19x slower                                                        |
| mypy2                      | 762 ms                                                       | 908 ms: 1.19x slower                                                         |
| coverage                   | 66.1 ms                                                      | 79.5 ms: 1.20x slower                                                        |
| gunicorn                   | 966 us                                                       | 1.16 ms: 1.20x slower                                                        |
| 2to3                       | 287 ms                                                       | 346 ms: 1.21x slower                                                         |
| aiohttp                    | 986 us                                                       | 1.19 ms: 1.21x slower                                                        |
| deepcopy_reduce            | 3.40 us                                                      | 4.10 us: 1.21x slower                                                        |
| sqlglot_optimize           | 59.0 ms                                                      | 71.5 ms: 1.21x slower                                                        |
| xml_etree_generate         | 79.7 ms                                                      | 96.7 ms: 1.21x slower                                                        |
| async_generators           | 322 ms                                                       | 391 ms: 1.21x slower                                                         |
| docutils                   | 2.85 sec                                                     | 3.48 sec: 1.22x slower                                                       |
| genshi_xml                 | 57.1 ms                                                      | 70.3 ms: 1.23x slower                                                        |
| html5lib                   | 72.2 ms                                                      | 89.0 ms: 1.23x slower                                                        |
| xml_etree_process          | 55.9 ms                                                      | 69.0 ms: 1.24x slower                                                        |
| deepcopy                   | 391 us                                                       | 483 us: 1.24x slower                                                         |
| python_startup             | 10.7 ms                                                      | 13.3 ms: 1.24x slower                                                        |
| richards                   | 49.7 ms                                                      | 62.3 ms: 1.25x slower                                                        |
| pprint_pformat             | 1.67 sec                                                     | 2.12 sec: 1.27x slower                                                       |
| unpickle_pure_python       | 238 us                                                       | 305 us: 1.28x slower                                                         |
| flaskblogging              | 3.88 ms                                                      | 4.97 ms: 1.28x slower                                                        |
| pprint_safe_repr           | 805 ms                                                       | 1.03 sec: 1.28x slower                                                       |
| float                      | 74.9 ms                                                      | 97.4 ms: 1.30x slower                                                        |
| scimark_lu                 | 114 ms                                                       | 149 ms: 1.31x slower                                                         |
| tomli_loads                | 2.25 sec                                                     | 2.94 sec: 1.31x slower                                                       |
| genshi_text                | 25.5 ms                                                      | 33.3 ms: 1.31x slower                                                        |
| go                         | 158 ms                                                       | 206 ms: 1.31x slower                                                         |
| create_gc_cycles           | 1.58 ms                                                      | 2.07 ms: 1.31x slower                                                        |
| mako                       | 11.0 ms                                                      | 14.5 ms: 1.32x slower                                                        |
| telco                      | 6.81 ms                                                      | 9.17 ms: 1.35x slower                                                        |
| nbody                      | 92.9 ms                                                      | 125 ms: 1.35x slower                                                         |
| pickle_pure_python         | 316 us                                                       | 434 us: 1.38x slower                                                         |
| regex_compile              | 156 ms                                                       | 216 ms: 1.38x slower                                                         |
| scimark_monte_carlo        | 69.8 ms                                                      | 99.5 ms: 1.43x slower                                                        |
| pyflate                    | 449 ms                                                       | 654 ms: 1.46x slower                                                         |
| scimark_sor                | 110 ms                                                       | 165 ms: 1.50x slower                                                         |
| scimark_fft                | 281 ms                                                       | 425 ms: 1.52x slower                                                         |
| hexiom                     | 6.98 ms                                                      | 10.7 ms: 1.54x slower                                                        |
| logging_silent             | 100 ns                                                       | 155 ns: 1.55x slower                                                         |
| deepcopy_memo              | 37.5 us                                                      | 58.6 us: 1.56x slower                                                        |
| spectral_norm              | 95.1 ms                                                      | 149 ms: 1.56x slower                                                         |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 6.60 ms: 1.63x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.09x slower                                                                 |

Benchmark hidden because not significant (4): asyncio_websockets, json, mdp, bench_thread_pool
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.05x