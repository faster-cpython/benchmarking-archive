# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a5
- machine: linux-x86_64
- commit hash: 076d169
- commit date: 2024-03-12
- overall geometric mean: 1.06x faster
- HPT reliability: 99.96%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf2-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 292 ms: 1.02x slower                                             |
| chameleon      | 7.92 ms                                                      | 7.28 ms: 1.09x faster                                            |
| docutils       | 2.85 sec                                                     | 2.83 sec: 1.01x faster                                           |
| html5lib       | 72.2 ms                                                      | 76.2 ms: 1.05x slower                                            |
| tornado_http   | 124 ms                                                       | 123 ms: 1.01x faster                                             |
| Geometric mean | (ref)                                                        | 1.01x faster                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf2-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| async_tree_none            | 518 ms                                                       | 433 ms: 1.20x faster                                             |
| async_tree_memoization     | 629 ms                                                       | 543 ms: 1.16x faster                                             |
| async_tree_memoization_tg  | 600 ms                                                       | 546 ms: 1.10x faster                                             |
| async_tree_none_tg         | 474 ms                                                       | 434 ms: 1.09x faster                                             |
| async_tree_io              | 1.17 sec                                                     | 1.07 sec: 1.09x faster                                           |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 697 ms: 1.08x faster                                             |
| async_tree_io_tg           | 1.15 sec                                                     | 1.07 sec: 1.07x faster                                           |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 703 ms: 1.07x faster                                             |
| Geometric mean             | (ref)                                                        | 1.11x faster                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf2-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 262 ms: 1.04x slower                                             |
| float          | 74.9 ms                                                      | 78.8 ms: 1.05x slower                                            |
| Geometric mean | (ref)                                                        | 1.03x slower                                                     |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf2-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 143 ms: 1.09x faster                                             |
| regex_dna      | 227 ms                                                       | 237 ms: 1.04x slower                                             |
| regex_v8       | 24.4 ms                                                      | 26.0 ms: 1.06x slower                                            |
| regex_effbot   | 3.34 ms                                                      | 3.57 ms: 1.07x slower                                            |
| Geometric mean | (ref)                                                        | 1.02x slower                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf2-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.3 ms: 1.28x faster                                            |
| json_loads           | 28.9 us                                                      | 24.5 us: 1.18x faster                                            |
| unpickle_pure_python | 238 us                                                       | 211 us: 1.13x faster                                             |
| xml_etree_parse      | 155 ms                                                       | 145 ms: 1.07x faster                                             |
| pickle_dict          | 32.3 us                                                      | 31.0 us: 1.04x faster                                            |
| pickle_pure_python   | 316 us                                                       | 305 us: 1.03x faster                                             |
| xml_etree_iterparse  | 107 ms                                                       | 105 ms: 1.02x faster                                             |
| unpickle_list        | 4.60 us                                                      | 4.56 us: 1.01x faster                                            |
| tomli_loads          | 2.25 sec                                                     | 2.29 sec: 1.02x slower                                           |
| pickle               | 9.89 us                                                      | 10.2 us: 1.03x slower                                            |
| xml_etree_process    | 55.9 ms                                                      | 60.2 ms: 1.08x slower                                            |
| xml_etree_generate   | 79.7 ms                                                      | 87.7 ms: 1.10x slower                                            |
| pickle_list          | 3.94 us                                                      | 4.51 us: 1.14x slower                                            |
| unpickle             | 13.3 us                                                      | 15.3 us: 1.15x slower                                            |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf2-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 12.7 ms: 1.18x slower                                            |
| python_startup_no_site | 7.73 ms                                                      | 11.1 ms: 1.44x slower                                            |
| Geometric mean         | (ref)                                                        | 1.30x slower                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf2-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 10.1 ms: 1.09x faster                                            |
| django_template | 39.3 ms                                                      | 37.7 ms: 1.04x faster                                            |
| genshi_xml      | 57.1 ms                                                      | 54.9 ms: 1.04x faster                                            |
| Geometric mean  | (ref)                                                        | 1.04x faster                                                     |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240312-pythonperf2-x86_64-python-v3.13.0a5-3.13.0a5-076d169 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 116 us: 4.59x faster                                             |
| asyncio_tcp                | 747 ms                                                       | 377 ms: 1.98x faster                                             |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                           |
| generators                 | 54.6 ms                                                      | 33.1 ms: 1.65x faster                                            |
| comprehensions             | 25.1 us                                                      | 16.7 us: 1.51x faster                                            |
| pylint                     | 514 ms                                                       | 344 ms: 1.49x faster                                             |
| json_dumps                 | 13.3 ms                                                      | 10.3 ms: 1.28x faster                                            |
| coroutines                 | 27.8 ms                                                      | 22.2 ms: 1.25x faster                                            |
| chaos                      | 74.9 ms                                                      | 61.1 ms: 1.23x faster                                            |
| raytrace                   | 309 ms                                                       | 253 ms: 1.22x faster                                             |
| sympy_sum                  | 186 ms                                                       | 152 ms: 1.22x faster                                             |
| scimark_lu                 | 114 ms                                                       | 94.6 ms: 1.21x faster                                            |
| async_tree_none            | 518 ms                                                       | 433 ms: 1.20x faster                                             |
| json_loads                 | 28.9 us                                                      | 24.5 us: 1.18x faster                                            |
| gc_traversal               | 4.15 ms                                                      | 3.55 ms: 1.17x faster                                            |
| async_tree_memoization     | 629 ms                                                       | 543 ms: 1.16x faster                                             |
| nqueens                    | 103 ms                                                       | 88.7 ms: 1.16x faster                                            |
| sympy_str                  | 337 ms                                                       | 293 ms: 1.15x faster                                             |
| crypto_pyaes               | 83.3 ms                                                      | 72.5 ms: 1.15x faster                                            |
| unpickle_pure_python       | 238 us                                                       | 211 us: 1.13x faster                                             |
| logging_simple             | 7.24 us                                                      | 6.44 us: 1.12x faster                                            |
| deltablue                  | 3.97 ms                                                      | 3.56 ms: 1.11x faster                                            |
| mdp                        | 2.77 sec                                                     | 2.49 sec: 1.11x faster                                           |
| sympy_integrate            | 25.8 ms                                                      | 23.2 ms: 1.11x faster                                            |
| richards_super             | 63.6 ms                                                      | 57.5 ms: 1.11x faster                                            |
| hexiom                     | 6.98 ms                                                      | 6.32 ms: 1.10x faster                                            |
| async_tree_memoization_tg  | 600 ms                                                       | 546 ms: 1.10x faster                                             |
| sympy_expand               | 553 ms                                                       | 504 ms: 1.10x faster                                             |
| regex_compile              | 156 ms                                                       | 143 ms: 1.09x faster                                             |
| async_tree_none_tg         | 474 ms                                                       | 434 ms: 1.09x faster                                             |
| async_tree_io              | 1.17 sec                                                     | 1.07 sec: 1.09x faster                                           |
| sqlglot_parse              | 1.51 ms                                                      | 1.39 ms: 1.09x faster                                            |
| chameleon                  | 7.92 ms                                                      | 7.28 ms: 1.09x faster                                            |
| mako                       | 11.0 ms                                                      | 10.1 ms: 1.09x faster                                            |
| logging_format             | 7.71 us                                                      | 7.11 us: 1.08x faster                                            |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 697 ms: 1.08x faster                                             |
| async_tree_io_tg           | 1.15 sec                                                     | 1.07 sec: 1.07x faster                                           |
| thrift                     | 931 us                                                       | 870 us: 1.07x faster                                             |
| xml_etree_parse            | 155 ms                                                       | 145 ms: 1.07x faster                                             |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 703 ms: 1.07x faster                                             |
| sqlglot_transpile          | 1.91 ms                                                      | 1.80 ms: 1.06x faster                                            |
| logging_silent             | 100 ns                                                       | 95.3 ns: 1.05x faster                                            |
| deepcopy                   | 391 us                                                       | 373 us: 1.05x faster                                             |
| bench_mp_pool              | 4.70 ms                                                      | 4.49 ms: 1.05x faster                                            |
| json                       | 5.58 ms                                                      | 5.34 ms: 1.05x faster                                            |
| sqlglot_normalize          | 122 ms                                                       | 117 ms: 1.04x faster                                             |
| pickle_dict                | 32.3 us                                                      | 31.0 us: 1.04x faster                                            |
| django_template            | 39.3 ms                                                      | 37.7 ms: 1.04x faster                                            |
| genshi_xml                 | 57.1 ms                                                      | 54.9 ms: 1.04x faster                                            |
| pickle_pure_python         | 316 us                                                       | 305 us: 1.03x faster                                             |
| dask                       | 410 ms                                                       | 397 ms: 1.03x faster                                             |
| deepcopy_reduce            | 3.40 us                                                      | 3.29 us: 1.03x faster                                            |
| spectral_norm              | 95.1 ms                                                      | 92.4 ms: 1.03x faster                                            |
| fannkuch                   | 416 ms                                                       | 406 ms: 1.02x faster                                             |
| pprint_pformat             | 1.67 sec                                                     | 1.63 sec: 1.02x faster                                           |
| asyncio_websockets         | 390 ms                                                       | 384 ms: 1.02x faster                                             |
| xml_etree_iterparse        | 107 ms                                                       | 105 ms: 1.02x faster                                             |
| tornado_http               | 124 ms                                                       | 123 ms: 1.01x faster                                             |
| deepcopy_memo              | 37.5 us                                                      | 37.0 us: 1.01x faster                                            |
| meteor_contest             | 131 ms                                                       | 129 ms: 1.01x faster                                             |
| unpickle_list              | 4.60 us                                                      | 4.56 us: 1.01x faster                                            |
| docutils                   | 2.85 sec                                                     | 2.83 sec: 1.01x faster                                           |
| pprint_safe_repr           | 805 ms                                                       | 800 ms: 1.01x faster                                             |
| pathlib                    | 18.9 ms                                                      | 18.9 ms: 1.00x faster                                            |
| sqlglot_optimize           | 59.0 ms                                                      | 59.1 ms: 1.00x slower                                            |
| scimark_monte_carlo        | 69.8 ms                                                      | 70.6 ms: 1.01x slower                                            |
| tomli_loads                | 2.25 sec                                                     | 2.29 sec: 1.02x slower                                           |
| 2to3                       | 287 ms                                                       | 292 ms: 1.02x slower                                             |
| create_gc_cycles           | 1.58 ms                                                      | 1.61 ms: 1.02x slower                                            |
| dulwich_log                | 67.4 ms                                                      | 68.8 ms: 1.02x slower                                            |
| pickle                     | 9.89 us                                                      | 10.2 us: 1.03x slower                                            |
| richards                   | 49.7 ms                                                      | 51.2 ms: 1.03x slower                                            |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.20 ms: 1.03x slower                                            |
| pidigits                   | 251 ms                                                       | 262 ms: 1.04x slower                                             |
| regex_dna                  | 227 ms                                                       | 237 ms: 1.04x slower                                             |
| float                      | 74.9 ms                                                      | 78.8 ms: 1.05x slower                                            |
| html5lib                   | 72.2 ms                                                      | 76.2 ms: 1.05x slower                                            |
| go                         | 158 ms                                                       | 167 ms: 1.06x slower                                             |
| regex_v8                   | 24.4 ms                                                      | 26.0 ms: 1.06x slower                                            |
| sqlite_synth               | 2.52 us                                                      | 2.69 us: 1.07x slower                                            |
| regex_effbot               | 3.34 ms                                                      | 3.57 ms: 1.07x slower                                            |
| gunicorn                   | 966 us                                                       | 1.04 ms: 1.08x slower                                            |
| xml_etree_process          | 55.9 ms                                                      | 60.2 ms: 1.08x slower                                            |
| scimark_fft                | 281 ms                                                       | 307 ms: 1.09x slower                                             |
| xml_etree_generate         | 79.7 ms                                                      | 87.7 ms: 1.10x slower                                            |
| aiohttp                    | 986 us                                                       | 1.09 ms: 1.10x slower                                            |
| pyflate                    | 449 ms                                                       | 509 ms: 1.13x slower                                             |
| mypy2                      | 762 ms                                                       | 864 ms: 1.13x slower                                             |
| async_generators           | 322 ms                                                       | 366 ms: 1.14x slower                                             |
| pickle_list                | 3.94 us                                                      | 4.51 us: 1.14x slower                                            |
| unpickle                   | 13.3 us                                                      | 15.3 us: 1.15x slower                                            |
| python_startup             | 10.7 ms                                                      | 12.7 ms: 1.18x slower                                            |
| telco                      | 6.81 ms                                                      | 8.09 ms: 1.19x slower                                            |
| coverage                   | 66.1 ms                                                      | 78.5 ms: 1.19x slower                                            |
| flaskblogging              | 3.88 ms                                                      | 4.66 ms: 1.20x slower                                            |
| scimark_sor                | 110 ms                                                       | 143 ms: 1.30x slower                                             |
| python_startup_no_site     | 7.73 ms                                                      | 11.1 ms: 1.44x slower                                            |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                     |

Benchmark hidden because not significant (4): bench_thread_pool, nbody, pycparser, genshi_text
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.96% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x