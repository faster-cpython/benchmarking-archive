# Results vs. 3.11.0

- fork: mdboom
- ref: dont_inline
- machine: linux-x86_64
- commit hash: c35ee28
- commit date: 2024-04-04
- overall geometric mean: 1.05x faster
- HPT reliability: 79.89%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 298 ms: 1.04x slower                                                |
| chameleon      | 7.92 ms                                                      | 7.46 ms: 1.06x faster                                               |
| docutils       | 2.85 sec                                                     | 3.10 sec: 1.09x slower                                              |
| tornado_http   | 124 ms                                                       | 122 ms: 1.02x faster                                                |
| Geometric mean | (ref)                                                        | 1.01x slower                                                        |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none_tg         | 474 ms                                                       | 334 ms: 1.42x faster                                                |
| async_tree_memoization_tg  | 600 ms                                                       | 425 ms: 1.41x faster                                                |
| async_tree_memoization     | 629 ms                                                       | 447 ms: 1.41x faster                                                |
| async_tree_io              | 1.17 sec                                                     | 856 ms: 1.37x faster                                                |
| async_tree_none            | 518 ms                                                       | 379 ms: 1.37x faster                                                |
| async_tree_io_tg           | 1.15 sec                                                     | 864 ms: 1.34x faster                                                |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 592 ms: 1.27x faster                                                |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 610 ms: 1.23x faster                                                |
| Geometric mean             | (ref)                                                        | 1.35x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 95.1 ms: 1.02x slower                                               |
| pidigits       | 251 ms                                                       | 261 ms: 1.04x slower                                                |
| Geometric mean | (ref)                                                        | 1.02x slower                                                        |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 148 ms: 1.05x faster                                                |
| regex_effbot   | 3.34 ms                                                      | 3.52 ms: 1.05x slower                                               |
| regex_dna      | 227 ms                                                       | 241 ms: 1.06x slower                                                |
| regex_v8       | 24.4 ms                                                      | 26.0 ms: 1.06x slower                                               |
| Geometric mean | (ref)                                                        | 1.03x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                               |
| json_loads           | 28.9 us                                                      | 25.5 us: 1.13x faster                                               |
| xml_etree_parse      | 155 ms                                                       | 146 ms: 1.06x faster                                                |
| tomli_loads          | 2.25 sec                                                     | 2.16 sec: 1.04x faster                                              |
| xml_etree_iterparse  | 107 ms                                                       | 103 ms: 1.03x faster                                                |
| pickle_pure_python   | 316 us                                                       | 309 us: 1.02x faster                                                |
| unpickle_pure_python | 238 us                                                       | 234 us: 1.02x faster                                                |
| unpickle_list        | 4.60 us                                                      | 4.54 us: 1.01x faster                                               |
| pickle_dict          | 32.3 us                                                      | 32.7 us: 1.01x slower                                               |
| xml_etree_process    | 55.9 ms                                                      | 57.9 ms: 1.04x slower                                               |
| xml_etree_generate   | 79.7 ms                                                      | 83.4 ms: 1.05x slower                                               |
| pickle               | 9.89 us                                                      | 10.7 us: 1.08x slower                                               |
| pickle_list          | 3.94 us                                                      | 4.43 us: 1.12x slower                                               |
| unpickle             | 13.3 us                                                      | 15.2 us: 1.14x slower                                               |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                               |
| python_startup_no_site | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                               |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako           | 11.0 ms                                                      | 9.85 ms: 1.12x faster                                               |
| genshi_xml     | 57.1 ms                                                      | 58.0 ms: 1.02x slower                                               |
| genshi_text    | 25.5 ms                                                      | 26.4 ms: 1.04x slower                                               |
| Geometric mean | (ref)                                                        | 1.02x faster                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 120 us: 4.43x faster                                                |
| asyncio_tcp                | 747 ms                                                       | 370 ms: 2.02x faster                                                |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                              |
| generators                 | 54.6 ms                                                      | 33.4 ms: 1.64x faster                                               |
| pylint                     | 514 ms                                                       | 338 ms: 1.52x faster                                                |
| async_tree_none_tg         | 474 ms                                                       | 334 ms: 1.42x faster                                                |
| async_tree_memoization_tg  | 600 ms                                                       | 425 ms: 1.41x faster                                                |
| async_tree_memoization     | 629 ms                                                       | 447 ms: 1.41x faster                                                |
| async_tree_io              | 1.17 sec                                                     | 856 ms: 1.37x faster                                                |
| async_tree_none            | 518 ms                                                       | 379 ms: 1.37x faster                                                |
| async_tree_io_tg           | 1.15 sec                                                     | 864 ms: 1.34x faster                                                |
| comprehensions             | 25.1 us                                                      | 19.5 us: 1.28x faster                                               |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 592 ms: 1.27x faster                                                |
| json_dumps                 | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                               |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 610 ms: 1.23x faster                                                |
| coroutines                 | 27.8 ms                                                      | 23.4 ms: 1.19x faster                                               |
| chaos                      | 74.9 ms                                                      | 63.8 ms: 1.17x faster                                               |
| json_loads                 | 28.9 us                                                      | 25.5 us: 1.13x faster                                               |
| sympy_sum                  | 186 ms                                                       | 164 ms: 1.13x faster                                                |
| mako                       | 11.0 ms                                                      | 9.85 ms: 1.12x faster                                               |
| richards_super             | 63.6 ms                                                      | 57.0 ms: 1.12x faster                                               |
| logging_simple             | 7.24 us                                                      | 6.52 us: 1.11x faster                                               |
| sympy_str                  | 337 ms                                                       | 305 ms: 1.10x faster                                                |
| deltablue                  | 3.97 ms                                                      | 3.61 ms: 1.10x faster                                               |
| crypto_pyaes               | 83.3 ms                                                      | 76.7 ms: 1.09x faster                                               |
| fannkuch                   | 416 ms                                                       | 384 ms: 1.08x faster                                                |
| sqlglot_parse              | 1.51 ms                                                      | 1.40 ms: 1.08x faster                                               |
| sympy_expand               | 553 ms                                                       | 513 ms: 1.08x faster                                                |
| logging_format             | 7.71 us                                                      | 7.15 us: 1.08x faster                                               |
| mdp                        | 2.77 sec                                                     | 2.59 sec: 1.07x faster                                              |
| raytrace                   | 309 ms                                                       | 291 ms: 1.06x faster                                                |
| chameleon                  | 7.92 ms                                                      | 7.46 ms: 1.06x faster                                               |
| xml_etree_parse            | 155 ms                                                       | 146 ms: 1.06x faster                                                |
| sqlglot_transpile          | 1.91 ms                                                      | 1.81 ms: 1.06x faster                                               |
| regex_compile              | 156 ms                                                       | 148 ms: 1.05x faster                                                |
| pycparser                  | 1.31 sec                                                     | 1.24 sec: 1.05x faster                                              |
| tomli_loads                | 2.25 sec                                                     | 2.16 sec: 1.04x faster                                              |
| xml_etree_iterparse        | 107 ms                                                       | 103 ms: 1.03x faster                                                |
| thrift                     | 931 us                                                       | 902 us: 1.03x faster                                                |
| logging_silent             | 100 ns                                                       | 97.8 ns: 1.03x faster                                               |
| tornado_http               | 124 ms                                                       | 122 ms: 1.02x faster                                                |
| json                       | 5.58 ms                                                      | 5.47 ms: 1.02x faster                                               |
| pickle_pure_python         | 316 us                                                       | 309 us: 1.02x faster                                                |
| unpickle_pure_python       | 238 us                                                       | 234 us: 1.02x faster                                                |
| dask                       | 410 ms                                                       | 403 ms: 1.02x faster                                                |
| sympy_integrate            | 25.8 ms                                                      | 25.4 ms: 1.02x faster                                               |
| spectral_norm              | 95.1 ms                                                      | 93.7 ms: 1.01x faster                                               |
| unpickle_list              | 4.60 us                                                      | 4.54 us: 1.01x faster                                               |
| scimark_monte_carlo        | 69.8 ms                                                      | 69.5 ms: 1.01x faster                                               |
| sqlglot_normalize          | 122 ms                                                       | 123 ms: 1.01x slower                                                |
| deepcopy_reduce            | 3.40 us                                                      | 3.43 us: 1.01x slower                                               |
| pickle_dict                | 32.3 us                                                      | 32.7 us: 1.01x slower                                               |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.13 ms: 1.02x slower                                               |
| meteor_contest             | 131 ms                                                       | 133 ms: 1.02x slower                                                |
| genshi_xml                 | 57.1 ms                                                      | 58.0 ms: 1.02x slower                                               |
| dulwich_log                | 67.4 ms                                                      | 68.7 ms: 1.02x slower                                               |
| richards                   | 49.7 ms                                                      | 50.8 ms: 1.02x slower                                               |
| deepcopy_memo              | 37.5 us                                                      | 38.4 us: 1.02x slower                                               |
| nbody                      | 92.9 ms                                                      | 95.1 ms: 1.02x slower                                               |
| pprint_pformat             | 1.67 sec                                                     | 1.71 sec: 1.03x slower                                              |
| pathlib                    | 18.9 ms                                                      | 19.5 ms: 1.03x slower                                               |
| genshi_text                | 25.5 ms                                                      | 26.4 ms: 1.04x slower                                               |
| xml_etree_process          | 55.9 ms                                                      | 57.9 ms: 1.04x slower                                               |
| pidigits                   | 251 ms                                                       | 261 ms: 1.04x slower                                                |
| pprint_safe_repr           | 805 ms                                                       | 836 ms: 1.04x slower                                                |
| 2to3                       | 287 ms                                                       | 298 ms: 1.04x slower                                                |
| xml_etree_generate         | 79.7 ms                                                      | 83.4 ms: 1.05x slower                                               |
| regex_effbot               | 3.34 ms                                                      | 3.52 ms: 1.05x slower                                               |
| regex_dna                  | 227 ms                                                       | 241 ms: 1.06x slower                                                |
| hexiom                     | 6.98 ms                                                      | 7.39 ms: 1.06x slower                                               |
| sqlite_synth               | 2.52 us                                                      | 2.68 us: 1.06x slower                                               |
| gc_traversal               | 4.15 ms                                                      | 4.41 ms: 1.06x slower                                               |
| regex_v8                   | 24.4 ms                                                      | 26.0 ms: 1.06x slower                                               |
| bench_mp_pool              | 4.70 ms                                                      | 5.00 ms: 1.06x slower                                               |
| sqlglot_optimize           | 59.0 ms                                                      | 62.7 ms: 1.06x slower                                               |
| pickle                     | 9.89 us                                                      | 10.7 us: 1.08x slower                                               |
| pyflate                    | 449 ms                                                       | 487 ms: 1.08x slower                                                |
| mypy2                      | 762 ms                                                       | 827 ms: 1.09x slower                                                |
| scimark_lu                 | 114 ms                                                       | 124 ms: 1.09x slower                                                |
| docutils                   | 2.85 sec                                                     | 3.10 sec: 1.09x slower                                              |
| bench_thread_pool          | 1.00 ms                                                      | 1.10 ms: 1.10x slower                                               |
| go                         | 158 ms                                                       | 175 ms: 1.11x slower                                                |
| scimark_fft                | 281 ms                                                       | 313 ms: 1.11x slower                                                |
| pickle_list                | 3.94 us                                                      | 4.43 us: 1.12x slower                                               |
| gunicorn                   | 966 us                                                       | 1.10 ms: 1.14x slower                                               |
| aiohttp                    | 986 us                                                       | 1.13 ms: 1.14x slower                                               |
| unpickle                   | 13.3 us                                                      | 15.2 us: 1.14x slower                                               |
| telco                      | 6.81 ms                                                      | 8.01 ms: 1.18x slower                                               |
| create_gc_cycles           | 1.58 ms                                                      | 1.86 ms: 1.18x slower                                               |
| async_generators           | 322 ms                                                       | 397 ms: 1.23x slower                                                |
| python_startup             | 10.7 ms                                                      | 13.5 ms: 1.26x slower                                               |
| coverage                   | 66.1 ms                                                      | 86.4 ms: 1.31x slower                                               |
| scimark_sor                | 110 ms                                                       | 153 ms: 1.39x slower                                                |
| python_startup_no_site     | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                               |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                        |

Benchmark hidden because not significant (5): deepcopy, nqueens, float, html5lib, asyncio_websockets
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 79.89% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x