# Results vs. 3.11.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: c32dc47
- commit date: 2024-04-02
- overall geometric mean: 1.09x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 288 ms: 1.01x slower                                         |
| chameleon      | 7.92 ms                                                      | 7.15 ms: 1.11x faster                                        |
| docutils       | 2.85 sec                                                     | 2.97 sec: 1.04x slower                                       |
| html5lib       | 72.2 ms                                                      | 73.2 ms: 1.01x slower                                        |
| tornado_http   | 124 ms                                                       | 120 ms: 1.04x faster                                         |
| Geometric mean | (ref)                                                        | 1.02x faster                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 413 ms: 1.45x faster                                         |
| async_tree_none            | 518 ms                                                       | 363 ms: 1.42x faster                                         |
| async_tree_none_tg         | 474 ms                                                       | 334 ms: 1.42x faster                                         |
| async_tree_memoization     | 629 ms                                                       | 457 ms: 1.38x faster                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 854 ms: 1.35x faster                                         |
| async_tree_io              | 1.17 sec                                                     | 883 ms: 1.33x faster                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 573 ms: 1.31x faster                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 607 ms: 1.24x faster                                         |
| Geometric mean             | (ref)                                                        | 1.36x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 85.3 ms: 1.09x faster                                        |
| float          | 74.9 ms                                                      | 75.3 ms: 1.00x slower                                        |
| pidigits       | 251 ms                                                       | 263 ms: 1.05x slower                                         |
| Geometric mean | (ref)                                                        | 1.01x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 141 ms: 1.11x faster                                         |
| regex_dna      | 227 ms                                                       | 230 ms: 1.01x slower                                         |
| regex_v8       | 24.4 ms                                                      | 25.7 ms: 1.05x slower                                        |
| regex_effbot   | 3.34 ms                                                      | 3.56 ms: 1.07x slower                                        |
| Geometric mean | (ref)                                                        | 1.01x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.5 ms: 1.27x faster                                        |
| unpickle_pure_python | 238 us                                                       | 210 us: 1.13x faster                                         |
| json_loads           | 28.9 us                                                      | 25.6 us: 1.13x faster                                        |
| xml_etree_parse      | 155 ms                                                       | 142 ms: 1.09x faster                                         |
| pickle_pure_python   | 316 us                                                       | 305 us: 1.04x faster                                         |
| xml_etree_iterparse  | 107 ms                                                       | 104 ms: 1.03x faster                                         |
| tomli_loads          | 2.25 sec                                                     | 2.19 sec: 1.03x faster                                       |
| pickle_dict          | 32.3 us                                                      | 33.1 us: 1.02x slower                                        |
| xml_etree_process    | 55.9 ms                                                      | 57.5 ms: 1.03x slower                                        |
| xml_etree_generate   | 79.7 ms                                                      | 82.4 ms: 1.03x slower                                        |
| pickle               | 9.89 us                                                      | 10.5 us: 1.06x slower                                        |
| unpickle             | 13.3 us                                                      | 14.9 us: 1.12x slower                                        |
| pickle_list          | 3.94 us                                                      | 4.53 us: 1.15x slower                                        |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                 |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 12.9 ms: 1.20x slower                                        |
| python_startup_no_site | 7.73 ms                                                      | 11.1 ms: 1.44x slower                                        |
| Geometric mean         | (ref)                                                        | 1.32x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_xml     | 57.1 ms                                                      | 53.1 ms: 1.07x faster                                        |
| mako           | 11.0 ms                                                      | 10.3 ms: 1.07x faster                                        |
| genshi_text    | 25.5 ms                                                      | 25.1 ms: 1.01x faster                                        |
| Geometric mean | (ref)                                                        | 1.05x faster                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 114 us: 4.66x faster                                         |
| asyncio_tcp                | 747 ms                                                       | 371 ms: 2.01x faster                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.95x faster                                       |
| generators                 | 54.6 ms                                                      | 33.1 ms: 1.65x faster                                        |
| pylint                     | 514 ms                                                       | 317 ms: 1.62x faster                                         |
| comprehensions             | 25.1 us                                                      | 16.8 us: 1.49x faster                                        |
| async_tree_memoization_tg  | 600 ms                                                       | 413 ms: 1.45x faster                                         |
| async_tree_none            | 518 ms                                                       | 363 ms: 1.42x faster                                         |
| async_tree_none_tg         | 474 ms                                                       | 334 ms: 1.42x faster                                         |
| async_tree_memoization     | 629 ms                                                       | 457 ms: 1.38x faster                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 854 ms: 1.35x faster                                         |
| async_tree_io              | 1.17 sec                                                     | 883 ms: 1.33x faster                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 573 ms: 1.31x faster                                         |
| chaos                      | 74.9 ms                                                      | 58.6 ms: 1.28x faster                                        |
| json_dumps                 | 13.3 ms                                                      | 10.5 ms: 1.27x faster                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 607 ms: 1.24x faster                                         |
| raytrace                   | 309 ms                                                       | 251 ms: 1.23x faster                                         |
| coroutines                 | 27.8 ms                                                      | 22.6 ms: 1.23x faster                                        |
| scimark_lu                 | 114 ms                                                       | 93.7 ms: 1.22x faster                                        |
| sympy_sum                  | 186 ms                                                       | 153 ms: 1.22x faster                                         |
| deltablue                  | 3.97 ms                                                      | 3.39 ms: 1.17x faster                                        |
| nqueens                    | 103 ms                                                       | 88.0 ms: 1.17x faster                                        |
| sympy_str                  | 337 ms                                                       | 291 ms: 1.16x faster                                         |
| crypto_pyaes               | 83.3 ms                                                      | 72.4 ms: 1.15x faster                                        |
| bench_thread_pool          | 1.00 ms                                                      | 880 us: 1.14x faster                                         |
| unpickle_pure_python       | 238 us                                                       | 210 us: 1.13x faster                                         |
| json_loads                 | 28.9 us                                                      | 25.6 us: 1.13x faster                                        |
| sympy_expand               | 553 ms                                                       | 491 ms: 1.13x faster                                         |
| fannkuch                   | 416 ms                                                       | 371 ms: 1.12x faster                                         |
| richards_super             | 63.6 ms                                                      | 57.0 ms: 1.12x faster                                        |
| sqlglot_parse              | 1.51 ms                                                      | 1.36 ms: 1.11x faster                                        |
| sympy_integrate            | 25.8 ms                                                      | 23.2 ms: 1.11x faster                                        |
| regex_compile              | 156 ms                                                       | 141 ms: 1.11x faster                                         |
| chameleon                  | 7.92 ms                                                      | 7.15 ms: 1.11x faster                                        |
| mdp                        | 2.77 sec                                                     | 2.51 sec: 1.10x faster                                       |
| sqlglot_transpile          | 1.91 ms                                                      | 1.74 ms: 1.10x faster                                        |
| hexiom                     | 6.98 ms                                                      | 6.38 ms: 1.09x faster                                        |
| logging_simple             | 7.24 us                                                      | 6.62 us: 1.09x faster                                        |
| xml_etree_parse            | 155 ms                                                       | 142 ms: 1.09x faster                                         |
| nbody                      | 92.9 ms                                                      | 85.3 ms: 1.09x faster                                        |
| thrift                     | 931 us                                                       | 859 us: 1.08x faster                                         |
| scimark_monte_carlo        | 69.8 ms                                                      | 64.4 ms: 1.08x faster                                        |
| genshi_xml                 | 57.1 ms                                                      | 53.1 ms: 1.07x faster                                        |
| mako                       | 11.0 ms                                                      | 10.3 ms: 1.07x faster                                        |
| pycparser                  | 1.31 sec                                                     | 1.22 sec: 1.07x faster                                       |
| logging_silent             | 100 ns                                                       | 93.8 ns: 1.07x faster                                        |
| deepcopy                   | 391 us                                                       | 367 us: 1.07x faster                                         |
| bench_mp_pool              | 4.70 ms                                                      | 4.47 ms: 1.05x faster                                        |
| dask                       | 410 ms                                                       | 391 ms: 1.05x faster                                         |
| sqlglot_normalize          | 122 ms                                                       | 117 ms: 1.04x faster                                         |
| logging_format             | 7.71 us                                                      | 7.41 us: 1.04x faster                                        |
| pprint_pformat             | 1.67 sec                                                     | 1.60 sec: 1.04x faster                                       |
| pickle_pure_python         | 316 us                                                       | 305 us: 1.04x faster                                         |
| meteor_contest             | 131 ms                                                       | 126 ms: 1.04x faster                                         |
| tornado_http               | 124 ms                                                       | 120 ms: 1.04x faster                                         |
| deepcopy_memo              | 37.5 us                                                      | 36.3 us: 1.03x faster                                        |
| pprint_safe_repr           | 805 ms                                                       | 780 ms: 1.03x faster                                         |
| xml_etree_iterparse        | 107 ms                                                       | 104 ms: 1.03x faster                                         |
| spectral_norm              | 95.1 ms                                                      | 92.3 ms: 1.03x faster                                        |
| tomli_loads                | 2.25 sec                                                     | 2.19 sec: 1.03x faster                                       |
| genshi_text                | 25.5 ms                                                      | 25.1 ms: 1.01x faster                                        |
| deepcopy_reduce            | 3.40 us                                                      | 3.35 us: 1.01x faster                                        |
| sqlglot_optimize           | 59.0 ms                                                      | 58.2 ms: 1.01x faster                                        |
| float                      | 74.9 ms                                                      | 75.3 ms: 1.00x slower                                        |
| 2to3                       | 287 ms                                                       | 288 ms: 1.01x slower                                         |
| richards                   | 49.7 ms                                                      | 50.1 ms: 1.01x slower                                        |
| pathlib                    | 18.9 ms                                                      | 19.2 ms: 1.01x slower                                        |
| mypy2                      | 762 ms                                                       | 771 ms: 1.01x slower                                         |
| asyncio_websockets         | 390 ms                                                       | 395 ms: 1.01x slower                                         |
| regex_dna                  | 227 ms                                                       | 230 ms: 1.01x slower                                         |
| html5lib                   | 72.2 ms                                                      | 73.2 ms: 1.01x slower                                        |
| dulwich_log                | 67.4 ms                                                      | 69.0 ms: 1.02x slower                                        |
| pickle_dict                | 32.3 us                                                      | 33.1 us: 1.02x slower                                        |
| xml_etree_process          | 55.9 ms                                                      | 57.5 ms: 1.03x slower                                        |
| xml_etree_generate         | 79.7 ms                                                      | 82.4 ms: 1.03x slower                                        |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.21 ms: 1.04x slower                                        |
| docutils                   | 2.85 sec                                                     | 2.97 sec: 1.04x slower                                       |
| pidigits                   | 251 ms                                                       | 263 ms: 1.05x slower                                         |
| regex_v8                   | 24.4 ms                                                      | 25.7 ms: 1.05x slower                                        |
| sqlite_synth               | 2.52 us                                                      | 2.68 us: 1.06x slower                                        |
| pickle                     | 9.89 us                                                      | 10.5 us: 1.06x slower                                        |
| regex_effbot               | 3.34 ms                                                      | 3.56 ms: 1.07x slower                                        |
| gunicorn                   | 966 us                                                       | 1.04 ms: 1.07x slower                                        |
| scimark_fft                | 281 ms                                                       | 301 ms: 1.07x slower                                         |
| go                         | 158 ms                                                       | 170 ms: 1.08x slower                                         |
| aiohttp                    | 986 us                                                       | 1.07 ms: 1.08x slower                                        |
| async_generators           | 322 ms                                                       | 356 ms: 1.11x slower                                         |
| pyflate                    | 449 ms                                                       | 500 ms: 1.11x slower                                         |
| gc_traversal               | 4.15 ms                                                      | 4.64 ms: 1.12x slower                                        |
| unpickle                   | 13.3 us                                                      | 14.9 us: 1.12x slower                                        |
| pickle_list                | 3.94 us                                                      | 4.53 us: 1.15x slower                                        |
| telco                      | 6.81 ms                                                      | 8.04 ms: 1.18x slower                                        |
| python_startup             | 10.7 ms                                                      | 12.9 ms: 1.20x slower                                        |
| create_gc_cycles           | 1.58 ms                                                      | 1.94 ms: 1.23x slower                                        |
| coverage                   | 66.1 ms                                                      | 81.9 ms: 1.24x slower                                        |
| scimark_sor                | 110 ms                                                       | 142 ms: 1.29x slower                                         |
| python_startup_no_site     | 7.73 ms                                                      | 11.1 ms: 1.44x slower                                        |
| Geometric mean             | (ref)                                                        | 1.09x faster                                                 |

Benchmark hidden because not significant (3): json, unpack_sequence, unpickle_list
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.02x