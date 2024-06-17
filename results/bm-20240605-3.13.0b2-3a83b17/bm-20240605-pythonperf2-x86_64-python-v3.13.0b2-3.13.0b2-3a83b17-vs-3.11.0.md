# Results vs. 3.11.0

- fork: python
- ref: v3.13.0b2
- machine: linux-x86_64
- commit hash: 3a83b17
- commit date: 2024-06-05
- overall geometric mean: 1.07x faster
- HPT reliability: 99.31%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 291 ms: 1.02x slower                                             |
| chameleon      | 7.92 ms                                                      | 7.40 ms: 1.07x faster                                            |
| docutils       | 2.85 sec                                                     | 2.98 sec: 1.05x slower                                           |
| html5lib       | 72.2 ms                                                      | 74.7 ms: 1.03x slower                                            |
| tornado_http   | 124 ms                                                       | 119 ms: 1.04x faster                                             |
| Geometric mean | (ref)                                                        | 1.00x faster                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 421 ms: 1.43x faster                                             |
| async_tree_none            | 518 ms                                                       | 365 ms: 1.42x faster                                             |
| async_tree_none_tg         | 474 ms                                                       | 340 ms: 1.39x faster                                             |
| async_tree_memoization     | 629 ms                                                       | 460 ms: 1.37x faster                                             |
| async_tree_io              | 1.17 sec                                                     | 873 ms: 1.34x faster                                             |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 573 ms: 1.31x faster                                             |
| async_tree_io_tg           | 1.15 sec                                                     | 900 ms: 1.28x faster                                             |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 604 ms: 1.25x faster                                             |
| Geometric mean             | (ref)                                                        | 1.35x faster                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 87.8 ms: 1.06x faster                                            |
| pidigits       | 251 ms                                                       | 254 ms: 1.01x slower                                             |
| float          | 74.9 ms                                                      | 80.2 ms: 1.07x slower                                            |
| Geometric mean | (ref)                                                        | 1.01x slower                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 144 ms: 1.08x faster                                             |
| regex_effbot   | 3.34 ms                                                      | 3.40 ms: 1.02x slower                                            |
| regex_v8       | 24.4 ms                                                      | 26.0 ms: 1.07x slower                                            |
| regex_dna      | 227 ms                                                       | 249 ms: 1.10x slower                                             |
| Geometric mean | (ref)                                                        | 1.02x slower                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.8 ms: 1.23x faster                                            |
| json_loads           | 28.9 us                                                      | 25.0 us: 1.16x faster                                            |
| xml_etree_parse      | 155 ms                                                       | 144 ms: 1.08x faster                                             |
| unpickle_pure_python | 238 us                                                       | 224 us: 1.06x faster                                             |
| xml_etree_iterparse  | 107 ms                                                       | 103 ms: 1.04x faster                                             |
| pickle_pure_python   | 316 us                                                       | 307 us: 1.03x faster                                             |
| pickle_dict          | 32.3 us                                                      | 32.8 us: 1.02x slower                                            |
| unpickle_list        | 4.60 us                                                      | 4.70 us: 1.02x slower                                            |
| tomli_loads          | 2.25 sec                                                     | 2.40 sec: 1.07x slower                                           |
| xml_etree_process    | 55.9 ms                                                      | 59.7 ms: 1.07x slower                                            |
| pickle               | 9.89 us                                                      | 10.6 us: 1.07x slower                                            |
| xml_etree_generate   | 79.7 ms                                                      | 85.7 ms: 1.08x slower                                            |
| pickle_list          | 3.94 us                                                      | 4.44 us: 1.13x slower                                            |
| unpickle             | 13.3 us                                                      | 15.7 us: 1.18x slower                                            |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 8.85 ms: 1.14x slower                                            |
| python_startup         | 10.7 ms                                                      | 13.2 ms: 1.23x slower                                            |
| Geometric mean         | (ref)                                                        | 1.19x slower                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 10.4 ms: 1.06x faster                                            |
| django_template | 39.3 ms                                                      | 39.0 ms: 1.01x faster                                            |
| genshi_text     | 25.5 ms                                                      | 25.9 ms: 1.02x slower                                            |
| genshi_xml      | 57.1 ms                                                      | 58.1 ms: 1.02x slower                                            |
| Geometric mean  | (ref)                                                        | 1.01x faster                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 171 us: 3.12x faster                                             |
| asyncio_tcp                | 747 ms                                                       | 378 ms: 1.98x faster                                             |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                           |
| generators                 | 54.6 ms                                                      | 33.5 ms: 1.63x faster                                            |
| pylint                     | 514 ms                                                       | 339 ms: 1.52x faster                                             |
| comprehensions             | 25.1 us                                                      | 17.0 us: 1.48x faster                                            |
| async_tree_memoization_tg  | 600 ms                                                       | 421 ms: 1.43x faster                                             |
| async_tree_none            | 518 ms                                                       | 365 ms: 1.42x faster                                             |
| async_tree_none_tg         | 474 ms                                                       | 340 ms: 1.39x faster                                             |
| async_tree_memoization     | 629 ms                                                       | 460 ms: 1.37x faster                                             |
| async_tree_io              | 1.17 sec                                                     | 873 ms: 1.34x faster                                             |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 573 ms: 1.31x faster                                             |
| async_tree_io_tg           | 1.15 sec                                                     | 900 ms: 1.28x faster                                             |
| coroutines                 | 27.8 ms                                                      | 22.0 ms: 1.26x faster                                            |
| chaos                      | 74.9 ms                                                      | 59.6 ms: 1.26x faster                                            |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 604 ms: 1.25x faster                                             |
| json_dumps                 | 13.3 ms                                                      | 10.8 ms: 1.23x faster                                            |
| sympy_sum                  | 186 ms                                                       | 155 ms: 1.20x faster                                             |
| raytrace                   | 309 ms                                                       | 260 ms: 1.19x faster                                             |
| fannkuch                   | 416 ms                                                       | 353 ms: 1.18x faster                                             |
| deltablue                  | 3.97 ms                                                      | 3.37 ms: 1.18x faster                                            |
| scimark_lu                 | 114 ms                                                       | 97.5 ms: 1.17x faster                                            |
| nqueens                    | 103 ms                                                       | 88.4 ms: 1.16x faster                                            |
| json_loads                 | 28.9 us                                                      | 25.0 us: 1.16x faster                                            |
| sympy_str                  | 337 ms                                                       | 295 ms: 1.14x faster                                             |
| crypto_pyaes               | 83.3 ms                                                      | 73.6 ms: 1.13x faster                                            |
| logging_simple             | 7.24 us                                                      | 6.40 us: 1.13x faster                                            |
| mdp                        | 2.77 sec                                                     | 2.46 sec: 1.13x faster                                           |
| sympy_integrate            | 25.8 ms                                                      | 23.2 ms: 1.11x faster                                            |
| pathlib                    | 18.9 ms                                                      | 17.1 ms: 1.11x faster                                            |
| sympy_expand               | 553 ms                                                       | 501 ms: 1.10x faster                                             |
| bench_thread_pool          | 1.00 ms                                                      | 908 us: 1.10x faster                                             |
| hexiom                     | 6.98 ms                                                      | 6.35 ms: 1.10x faster                                            |
| sqlglot_parse              | 1.51 ms                                                      | 1.39 ms: 1.09x faster                                            |
| logging_format             | 7.71 us                                                      | 7.11 us: 1.08x faster                                            |
| sqlglot_transpile          | 1.91 ms                                                      | 1.76 ms: 1.08x faster                                            |
| regex_compile              | 156 ms                                                       | 144 ms: 1.08x faster                                             |
| xml_etree_parse            | 155 ms                                                       | 144 ms: 1.08x faster                                             |
| chameleon                  | 7.92 ms                                                      | 7.40 ms: 1.07x faster                                            |
| pycparser                  | 1.31 sec                                                     | 1.22 sec: 1.07x faster                                           |
| scimark_monte_carlo        | 69.8 ms                                                      | 65.5 ms: 1.07x faster                                            |
| unpickle_pure_python       | 238 us                                                       | 224 us: 1.06x faster                                             |
| mako                       | 11.0 ms                                                      | 10.4 ms: 1.06x faster                                            |
| thrift                     | 931 us                                                       | 880 us: 1.06x faster                                             |
| nbody                      | 92.9 ms                                                      | 87.8 ms: 1.06x faster                                            |
| dask                       | 410 ms                                                       | 391 ms: 1.05x faster                                             |
| json                       | 5.58 ms                                                      | 5.35 ms: 1.04x faster                                            |
| logging_silent             | 100 ns                                                       | 96.3 ns: 1.04x faster                                            |
| tornado_http               | 124 ms                                                       | 119 ms: 1.04x faster                                             |
| xml_etree_iterparse        | 107 ms                                                       | 103 ms: 1.04x faster                                             |
| richards_super             | 63.6 ms                                                      | 61.2 ms: 1.04x faster                                            |
| deepcopy                   | 391 us                                                       | 377 us: 1.04x faster                                             |
| pickle_pure_python         | 316 us                                                       | 307 us: 1.03x faster                                             |
| meteor_contest             | 131 ms                                                       | 128 ms: 1.02x faster                                             |
| sqlglot_normalize          | 122 ms                                                       | 120 ms: 1.01x faster                                             |
| django_template            | 39.3 ms                                                      | 39.0 ms: 1.01x faster                                            |
| deepcopy_memo              | 37.5 us                                                      | 37.3 us: 1.01x faster                                            |
| pidigits                   | 251 ms                                                       | 254 ms: 1.01x slower                                             |
| sqlglot_optimize           | 59.0 ms                                                      | 59.5 ms: 1.01x slower                                            |
| asyncio_websockets         | 390 ms                                                       | 395 ms: 1.01x slower                                             |
| pickle_dict                | 32.3 us                                                      | 32.8 us: 1.02x slower                                            |
| pprint_safe_repr           | 805 ms                                                       | 818 ms: 1.02x slower                                             |
| 2to3                       | 287 ms                                                       | 291 ms: 1.02x slower                                             |
| genshi_text                | 25.5 ms                                                      | 25.9 ms: 1.02x slower                                            |
| genshi_xml                 | 57.1 ms                                                      | 58.1 ms: 1.02x slower                                            |
| regex_effbot               | 3.34 ms                                                      | 3.40 ms: 1.02x slower                                            |
| unpickle_list              | 4.60 us                                                      | 4.70 us: 1.02x slower                                            |
| spectral_norm              | 95.1 ms                                                      | 97.3 ms: 1.02x slower                                            |
| html5lib                   | 72.2 ms                                                      | 74.7 ms: 1.03x slower                                            |
| go                         | 158 ms                                                       | 165 ms: 1.05x slower                                             |
| docutils                   | 2.85 sec                                                     | 2.98 sec: 1.05x slower                                           |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.28 ms: 1.05x slower                                            |
| regex_v8                   | 24.4 ms                                                      | 26.0 ms: 1.07x slower                                            |
| tomli_loads                | 2.25 sec                                                     | 2.40 sec: 1.07x slower                                           |
| xml_etree_process          | 55.9 ms                                                      | 59.7 ms: 1.07x slower                                            |
| float                      | 74.9 ms                                                      | 80.2 ms: 1.07x slower                                            |
| pyflate                    | 449 ms                                                       | 482 ms: 1.07x slower                                             |
| pickle                     | 9.89 us                                                      | 10.6 us: 1.07x slower                                            |
| xml_etree_generate         | 79.7 ms                                                      | 85.7 ms: 1.08x slower                                            |
| richards                   | 49.7 ms                                                      | 53.4 ms: 1.08x slower                                            |
| gunicorn                   | 966 us                                                       | 1.04 ms: 1.08x slower                                            |
| scimark_sor                | 110 ms                                                       | 119 ms: 1.08x slower                                             |
| aiohttp                    | 986 us                                                       | 1.07 ms: 1.09x slower                                            |
| regex_dna                  | 227 ms                                                       | 249 ms: 1.10x slower                                             |
| sqlite_synth               | 2.52 us                                                      | 2.80 us: 1.11x slower                                            |
| scimark_fft                | 281 ms                                                       | 312 ms: 1.11x slower                                             |
| async_generators           | 322 ms                                                       | 363 ms: 1.13x slower                                             |
| pickle_list                | 3.94 us                                                      | 4.44 us: 1.13x slower                                            |
| gc_traversal               | 4.15 ms                                                      | 4.69 ms: 1.13x slower                                            |
| python_startup_no_site     | 7.73 ms                                                      | 8.85 ms: 1.14x slower                                            |
| unpickle                   | 13.3 us                                                      | 15.7 us: 1.18x slower                                            |
| flaskblogging              | 3.88 ms                                                      | 4.68 ms: 1.21x slower                                            |
| python_startup             | 10.7 ms                                                      | 13.2 ms: 1.23x slower                                            |
| telco                      | 6.81 ms                                                      | 8.40 ms: 1.23x slower                                            |
| coverage                   | 66.1 ms                                                      | 83.5 ms: 1.26x slower                                            |
| create_gc_cycles           | 1.58 ms                                                      | 2.00 ms: 1.27x slower                                            |
| Geometric mean             | (ref)                                                        | 1.07x faster                                                     |

Benchmark hidden because not significant (5): pprint_pformat, deepcopy_reduce, dulwich_log, mypy2, bench_mp_pool
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-pythonperf2-x86_64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser

# HPT report

- Reliability score: 99.31% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x