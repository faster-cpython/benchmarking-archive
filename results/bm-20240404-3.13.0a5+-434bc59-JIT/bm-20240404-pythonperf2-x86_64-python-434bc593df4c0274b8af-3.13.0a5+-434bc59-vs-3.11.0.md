# Results vs. 3.11.0

- fork: python
- ref: 434bc593df4c0274b8af
- machine: linux-x86_64
- commit hash: 434bc59
- commit date: 2024-04-04
- overall geometric mean: 1.06x faster
- HPT reliability: 87.53%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 298 ms: 1.04x slower                                                         |
| chameleon      | 7.92 ms                                                      | 7.72 ms: 1.03x faster                                                        |
| docutils       | 2.85 sec                                                     | 3.07 sec: 1.08x slower                                                       |
| html5lib       | 72.2 ms                                                      | 75.4 ms: 1.04x slower                                                        |
| tornado_http   | 124 ms                                                       | 122 ms: 1.02x faster                                                         |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization     | 629 ms                                                       | 439 ms: 1.43x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 332 ms: 1.43x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 420 ms: 1.43x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 846 ms: 1.38x faster                                                         |
| async_tree_none            | 518 ms                                                       | 374 ms: 1.38x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 858 ms: 1.35x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 588 ms: 1.28x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 602 ms: 1.25x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.36x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 74.9 ms                                                      | 75.3 ms: 1.00x slower                                                        |
| nbody          | 92.9 ms                                                      | 96.3 ms: 1.04x slower                                                        |
| pidigits       | 251 ms                                                       | 261 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 147 ms: 1.06x faster                                                         |
| regex_v8       | 24.4 ms                                                      | 25.4 ms: 1.04x slower                                                        |
| regex_dna      | 227 ms                                                       | 237 ms: 1.04x slower                                                         |
| regex_effbot   | 3.34 ms                                                      | 3.61 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                        |
| json_loads           | 28.9 us                                                      | 25.2 us: 1.15x faster                                                        |
| unpickle_pure_python | 238 us                                                       | 225 us: 1.06x faster                                                         |
| pickle_dict          | 32.3 us                                                      | 30.6 us: 1.06x faster                                                        |
| tomli_loads          | 2.25 sec                                                     | 2.13 sec: 1.06x faster                                                       |
| xml_etree_parse      | 155 ms                                                       | 148 ms: 1.05x faster                                                         |
| xml_etree_iterparse  | 107 ms                                                       | 103 ms: 1.04x faster                                                         |
| pickle_pure_python   | 316 us                                                       | 313 us: 1.01x faster                                                         |
| pickle               | 9.89 us                                                      | 10.4 us: 1.05x slower                                                        |
| xml_etree_process    | 55.9 ms                                                      | 58.9 ms: 1.05x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 84.7 ms: 1.06x slower                                                        |
| pickle_list          | 3.94 us                                                      | 4.45 us: 1.13x slower                                                        |
| unpickle             | 13.3 us                                                      | 15.1 us: 1.14x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                                 |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 13.4 ms: 1.25x slower                                                        |
| python_startup_no_site | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 11.0 ms                                                      | 10.0 ms: 1.10x faster                                                        |
| genshi_xml     | 57.1 ms                                                      | 59.7 ms: 1.05x slower                                                        |
| genshi_text    | 25.5 ms                                                      | 26.7 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                        | 1.00x faster                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-python-434bc593df4c0274b8af-3.13.0a5+-434bc59 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 128 us: 4.15x faster                                                         |
| asyncio_tcp                | 747 ms                                                       | 373 ms: 2.00x faster                                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                       |
| generators                 | 54.6 ms                                                      | 33.4 ms: 1.64x faster                                                        |
| pylint                     | 514 ms                                                       | 334 ms: 1.54x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 439 ms: 1.43x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 332 ms: 1.43x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 420 ms: 1.43x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 846 ms: 1.38x faster                                                         |
| async_tree_none            | 518 ms                                                       | 374 ms: 1.38x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 858 ms: 1.35x faster                                                         |
| comprehensions             | 25.1 us                                                      | 19.1 us: 1.31x faster                                                        |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 588 ms: 1.28x faster                                                         |
| coroutines                 | 27.8 ms                                                      | 22.1 ms: 1.26x faster                                                        |
| json_dumps                 | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 602 ms: 1.25x faster                                                         |
| richards_super             | 63.6 ms                                                      | 51.9 ms: 1.22x faster                                                        |
| chaos                      | 74.9 ms                                                      | 64.6 ms: 1.16x faster                                                        |
| json_loads                 | 28.9 us                                                      | 25.2 us: 1.15x faster                                                        |
| logging_simple             | 7.24 us                                                      | 6.34 us: 1.14x faster                                                        |
| sympy_sum                  | 186 ms                                                       | 163 ms: 1.14x faster                                                         |
| raytrace                   | 309 ms                                                       | 272 ms: 1.14x faster                                                         |
| sympy_str                  | 337 ms                                                       | 305 ms: 1.11x faster                                                         |
| logging_format             | 7.71 us                                                      | 7.00 us: 1.10x faster                                                        |
| mako                       | 11.0 ms                                                      | 10.0 ms: 1.10x faster                                                        |
| sympy_expand               | 553 ms                                                       | 507 ms: 1.09x faster                                                         |
| richards                   | 49.7 ms                                                      | 45.7 ms: 1.09x faster                                                        |
| mdp                        | 2.77 sec                                                     | 2.57 sec: 1.08x faster                                                       |
| crypto_pyaes               | 83.3 ms                                                      | 77.2 ms: 1.08x faster                                                        |
| fannkuch                   | 416 ms                                                       | 388 ms: 1.07x faster                                                         |
| sqlglot_parse              | 1.51 ms                                                      | 1.42 ms: 1.07x faster                                                        |
| regex_compile              | 156 ms                                                       | 147 ms: 1.06x faster                                                         |
| unpickle_pure_python       | 238 us                                                       | 225 us: 1.06x faster                                                         |
| pickle_dict                | 32.3 us                                                      | 30.6 us: 1.06x faster                                                        |
| tomli_loads                | 2.25 sec                                                     | 2.13 sec: 1.06x faster                                                       |
| bench_thread_pool          | 1.00 ms                                                      | 947 us: 1.06x faster                                                         |
| deltablue                  | 3.97 ms                                                      | 3.76 ms: 1.06x faster                                                        |
| json                       | 5.58 ms                                                      | 5.30 ms: 1.05x faster                                                        |
| thrift                     | 931 us                                                       | 885 us: 1.05x faster                                                         |
| sqlglot_transpile          | 1.91 ms                                                      | 1.82 ms: 1.05x faster                                                        |
| xml_etree_parse            | 155 ms                                                       | 148 ms: 1.05x faster                                                         |
| pycparser                  | 1.31 sec                                                     | 1.25 sec: 1.04x faster                                                       |
| xml_etree_iterparse        | 107 ms                                                       | 103 ms: 1.04x faster                                                         |
| logging_silent             | 100 ns                                                       | 97.2 ns: 1.03x faster                                                        |
| chameleon                  | 7.92 ms                                                      | 7.72 ms: 1.03x faster                                                        |
| sympy_integrate            | 25.8 ms                                                      | 25.2 ms: 1.03x faster                                                        |
| dask                       | 410 ms                                                       | 400 ms: 1.02x faster                                                         |
| spectral_norm              | 95.1 ms                                                      | 93.2 ms: 1.02x faster                                                        |
| tornado_http               | 124 ms                                                       | 122 ms: 1.02x faster                                                         |
| pickle_pure_python         | 316 us                                                       | 313 us: 1.01x faster                                                         |
| float                      | 74.9 ms                                                      | 75.3 ms: 1.00x slower                                                        |
| deepcopy                   | 391 us                                                       | 398 us: 1.02x slower                                                         |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.14 ms: 1.02x slower                                                        |
| meteor_contest             | 131 ms                                                       | 133 ms: 1.02x slower                                                         |
| pathlib                    | 18.9 ms                                                      | 19.3 ms: 1.02x slower                                                        |
| sqlglot_normalize          | 122 ms                                                       | 125 ms: 1.02x slower                                                         |
| hexiom                     | 6.98 ms                                                      | 7.15 ms: 1.02x slower                                                        |
| pprint_pformat             | 1.67 sec                                                     | 1.71 sec: 1.03x slower                                                       |
| deepcopy_memo              | 37.5 us                                                      | 38.8 us: 1.03x slower                                                        |
| deepcopy_reduce            | 3.40 us                                                      | 3.51 us: 1.03x slower                                                        |
| pprint_safe_repr           | 805 ms                                                       | 834 ms: 1.04x slower                                                         |
| nbody                      | 92.9 ms                                                      | 96.3 ms: 1.04x slower                                                        |
| pidigits                   | 251 ms                                                       | 261 ms: 1.04x slower                                                         |
| regex_v8                   | 24.4 ms                                                      | 25.4 ms: 1.04x slower                                                        |
| 2to3                       | 287 ms                                                       | 298 ms: 1.04x slower                                                         |
| regex_dna                  | 227 ms                                                       | 237 ms: 1.04x slower                                                         |
| html5lib                   | 72.2 ms                                                      | 75.4 ms: 1.04x slower                                                        |
| scimark_lu                 | 114 ms                                                       | 119 ms: 1.04x slower                                                         |
| genshi_xml                 | 57.1 ms                                                      | 59.7 ms: 1.05x slower                                                        |
| pickle                     | 9.89 us                                                      | 10.4 us: 1.05x slower                                                        |
| genshi_text                | 25.5 ms                                                      | 26.7 ms: 1.05x slower                                                        |
| xml_etree_process          | 55.9 ms                                                      | 58.9 ms: 1.05x slower                                                        |
| xml_etree_generate         | 79.7 ms                                                      | 84.7 ms: 1.06x slower                                                        |
| sqlite_synth               | 2.52 us                                                      | 2.69 us: 1.07x slower                                                        |
| sqlglot_optimize           | 59.0 ms                                                      | 63.1 ms: 1.07x slower                                                        |
| mypy2                      | 762 ms                                                       | 819 ms: 1.07x slower                                                         |
| docutils                   | 2.85 sec                                                     | 3.07 sec: 1.08x slower                                                       |
| regex_effbot               | 3.34 ms                                                      | 3.61 ms: 1.08x slower                                                        |
| go                         | 158 ms                                                       | 172 ms: 1.09x slower                                                         |
| gc_traversal               | 4.15 ms                                                      | 4.58 ms: 1.10x slower                                                        |
| pyflate                    | 449 ms                                                       | 501 ms: 1.12x slower                                                         |
| scimark_fft                | 281 ms                                                       | 314 ms: 1.12x slower                                                         |
| pickle_list                | 3.94 us                                                      | 4.45 us: 1.13x slower                                                        |
| gunicorn                   | 966 us                                                       | 1.10 ms: 1.13x slower                                                        |
| aiohttp                    | 986 us                                                       | 1.12 ms: 1.14x slower                                                        |
| unpickle                   | 13.3 us                                                      | 15.1 us: 1.14x slower                                                        |
| async_generators           | 322 ms                                                       | 380 ms: 1.18x slower                                                         |
| create_gc_cycles           | 1.58 ms                                                      | 1.86 ms: 1.18x slower                                                        |
| telco                      | 6.81 ms                                                      | 8.22 ms: 1.21x slower                                                        |
| coverage                   | 66.1 ms                                                      | 81.6 ms: 1.23x slower                                                        |
| python_startup             | 10.7 ms                                                      | 13.4 ms: 1.25x slower                                                        |
| scimark_sor                | 110 ms                                                       | 151 ms: 1.38x slower                                                         |
| python_startup_no_site     | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                                 |

Benchmark hidden because not significant (6): nqueens, bench_mp_pool, asyncio_websockets, unpickle_list, scimark_monte_carlo, dulwich_log
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 87.53% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x