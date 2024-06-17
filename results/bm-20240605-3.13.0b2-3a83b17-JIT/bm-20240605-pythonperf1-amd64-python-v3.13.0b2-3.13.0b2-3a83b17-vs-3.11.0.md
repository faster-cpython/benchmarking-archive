# Results vs. 3.11.0

- fork: python
- ref: v3.13.0b2
- machine: windows-amd64
- commit hash: 3a83b17
- commit date: 2024-06-05
- overall geometric mean: 1.07x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.02x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 229 ms: 1.07x slower                                            |
| chameleon      | 5.26 ms                                                     | 5.00 ms: 1.05x faster                                           |
| docutils       | 1.64 sec                                                    | 1.77 sec: 1.08x slower                                          |
| html5lib       | 38.9 ms                                                     | 37.9 ms: 1.02x faster                                           |
| tornado_http   | 92.8 ms                                                     | 86.1 ms: 1.08x faster                                           |
| Geometric mean | (ref)                                                       | 1.00x faster                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 273 ms: 1.49x faster                                            |
| async_tree_none            | 332 ms                                                      | 227 ms: 1.46x faster                                            |
| async_tree_none_tg         | 309 ms                                                      | 215 ms: 1.44x faster                                            |
| async_tree_memoization     | 399 ms                                                      | 278 ms: 1.44x faster                                            |
| async_tree_io              | 808 ms                                                      | 579 ms: 1.40x faster                                            |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.37x faster                                            |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 392 ms: 1.35x faster                                            |
| async_tree_io_tg           | 829 ms                                                      | 624 ms: 1.33x faster                                            |
| Geometric mean             | (ref)                                                       | 1.41x faster                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 53.1 ms: 1.32x faster                                           |
| float          | 54.4 ms                                                     | 44.3 ms: 1.23x faster                                           |
| Geometric mean | (ref)                                                       | 1.18x faster                                                    |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 88.9 ms: 1.02x faster                                           |
| regex_dna      | 116 ms                                                      | 116 ms: 1.01x faster                                            |
| regex_effbot   | 1.50 ms                                                     | 1.55 ms: 1.04x slower                                           |
| regex_v8       | 14.2 ms                                                     | 15.2 ms: 1.07x slower                                           |
| Geometric mean | (ref)                                                       | 1.02x slower                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.70 ms: 1.42x faster                                           |
| unpickle_pure_python | 157 us                                                      | 130 us: 1.20x faster                                            |
| pickle_pure_python   | 208 us                                                      | 175 us: 1.19x faster                                            |
| tomli_loads          | 1.46 sec                                                    | 1.24 sec: 1.18x faster                                          |
| xml_etree_parse      | 97.6 ms                                                     | 90.3 ms: 1.08x faster                                           |
| xml_etree_iterparse  | 65.6 ms                                                     | 61.2 ms: 1.07x faster                                           |
| pickle_dict          | 18.5 us                                                     | 17.6 us: 1.05x faster                                           |
| xml_etree_generate   | 52.5 ms                                                     | 51.4 ms: 1.02x faster                                           |
| xml_etree_process    | 37.2 ms                                                     | 36.8 ms: 1.01x faster                                           |
| pickle_list          | 2.70 us                                                     | 2.85 us: 1.06x slower                                           |
| unpickle_list        | 2.59 us                                                     | 2.78 us: 1.07x slower                                           |
| json_loads           | 13.0 us                                                     | 14.1 us: 1.08x slower                                           |
| pickle               | 6.64 us                                                     | 7.27 us: 1.10x slower                                           |
| unpickle             | 7.57 us                                                     | 8.73 us: 1.15x slower                                           |
| Geometric mean       | (ref)                                                       | 1.05x faster                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 18.6 ms: 1.11x slower                                           |
| python_startup         | 19.8 ms                                                     | 22.7 ms: 1.15x slower                                           |
| Geometric mean         | (ref)                                                       | 1.13x slower                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 5.13 ms: 1.48x faster                                           |
| genshi_text     | 18.4 ms                                                     | 17.9 ms: 1.03x faster                                           |
| django_template | 24.4 ms                                                     | 25.4 ms: 1.04x slower                                           |
| genshi_xml      | 39.9 ms                                                     | 44.2 ms: 1.11x slower                                           |
| Geometric mean  | (ref)                                                       | 1.07x faster                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 113 us: 2.89x faster                                            |
| generators                 | 34.0 ms                                                     | 21.2 ms: 1.60x faster                                           |
| asyncio_tcp                | 726 ms                                                      | 479 ms: 1.51x faster                                            |
| spectral_norm              | 68.3 ms                                                     | 45.3 ms: 1.51x faster                                           |
| comprehensions             | 15.6 us                                                     | 10.4 us: 1.51x faster                                           |
| async_tree_memoization_tg  | 405 ms                                                      | 273 ms: 1.49x faster                                            |
| mako                       | 7.58 ms                                                     | 5.13 ms: 1.48x faster                                           |
| async_tree_none            | 332 ms                                                      | 227 ms: 1.46x faster                                            |
| async_tree_none_tg         | 309 ms                                                      | 215 ms: 1.44x faster                                            |
| async_tree_memoization     | 399 ms                                                      | 278 ms: 1.44x faster                                            |
| json_dumps                 | 8.09 ms                                                     | 5.70 ms: 1.42x faster                                           |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.43 sec: 1.41x faster                                          |
| async_tree_io              | 808 ms                                                      | 579 ms: 1.40x faster                                            |
| pylint                     | 323 ms                                                      | 235 ms: 1.38x faster                                            |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.37x faster                                            |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 392 ms: 1.35x faster                                            |
| async_tree_io_tg           | 829 ms                                                      | 624 ms: 1.33x faster                                            |
| nbody                      | 70.3 ms                                                     | 53.1 ms: 1.32x faster                                           |
| logging_silent             | 71.8 ns                                                     | 55.3 ns: 1.30x faster                                           |
| deepcopy_memo              | 26.0 us                                                     | 20.9 us: 1.24x faster                                           |
| chaos                      | 48.4 ms                                                     | 39.2 ms: 1.24x faster                                           |
| float                      | 54.4 ms                                                     | 44.3 ms: 1.23x faster                                           |
| pyflate                    | 312 ms                                                      | 257 ms: 1.21x faster                                            |
| raytrace                   | 213 ms                                                      | 176 ms: 1.21x faster                                            |
| unpickle_pure_python       | 157 us                                                      | 130 us: 1.20x faster                                            |
| scimark_monte_carlo        | 45.3 ms                                                     | 37.7 ms: 1.20x faster                                           |
| scimark_fft                | 179 ms                                                      | 150 ms: 1.20x faster                                            |
| sqlglot_parse              | 953 us                                                      | 801 us: 1.19x faster                                            |
| pickle_pure_python         | 208 us                                                      | 175 us: 1.19x faster                                            |
| fannkuch                   | 253 ms                                                      | 215 ms: 1.18x faster                                            |
| crypto_pyaes               | 48.9 ms                                                     | 41.5 ms: 1.18x faster                                           |
| tomli_loads                | 1.46 sec                                                    | 1.24 sec: 1.18x faster                                          |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.19 ms: 1.18x faster                                           |
| logging_simple             | 6.86 us                                                     | 5.91 us: 1.16x faster                                           |
| dulwich_log                | 46.4 ms                                                     | 40.2 ms: 1.15x faster                                           |
| richards_super             | 38.7 ms                                                     | 33.5 ms: 1.15x faster                                           |
| pprint_pformat             | 1.09 sec                                                    | 946 ms: 1.15x faster                                            |
| pprint_safe_repr           | 529 ms                                                      | 461 ms: 1.15x faster                                            |
| deltablue                  | 2.70 ms                                                     | 2.37 ms: 1.14x faster                                           |
| coroutines                 | 15.0 ms                                                     | 13.2 ms: 1.13x faster                                           |
| sqlglot_transpile          | 1.16 ms                                                     | 1.04 ms: 1.12x faster                                           |
| logging_format             | 7.16 us                                                     | 6.42 us: 1.12x faster                                           |
| nqueens                    | 68.3 ms                                                     | 61.4 ms: 1.11x faster                                           |
| bench_thread_pool          | 872 us                                                      | 793 us: 1.10x faster                                            |
| xml_etree_parse            | 97.6 ms                                                     | 90.3 ms: 1.08x faster                                           |
| tornado_http               | 92.8 ms                                                     | 86.1 ms: 1.08x faster                                           |
| go                         | 101 ms                                                      | 93.8 ms: 1.08x faster                                           |
| xml_etree_iterparse        | 65.6 ms                                                     | 61.2 ms: 1.07x faster                                           |
| sympy_sum                  | 100 ms                                                      | 93.9 ms: 1.07x faster                                           |
| richards                   | 31.4 ms                                                     | 29.7 ms: 1.06x faster                                           |
| mdp                        | 1.59 sec                                                    | 1.51 sec: 1.06x faster                                          |
| chameleon                  | 5.26 ms                                                     | 5.00 ms: 1.05x faster                                           |
| pickle_dict                | 18.5 us                                                     | 17.6 us: 1.05x faster                                           |
| sqlite_synth               | 1.77 us                                                     | 1.69 us: 1.05x faster                                           |
| meteor_contest             | 75.2 ms                                                     | 72.0 ms: 1.04x faster                                           |
| genshi_text                | 18.4 ms                                                     | 17.9 ms: 1.03x faster                                           |
| deepcopy                   | 246 us                                                      | 241 us: 1.02x faster                                            |
| regex_compile              | 91.0 ms                                                     | 88.9 ms: 1.02x faster                                           |
| html5lib                   | 38.9 ms                                                     | 37.9 ms: 1.02x faster                                           |
| xml_etree_generate         | 52.5 ms                                                     | 51.4 ms: 1.02x faster                                           |
| sympy_str                  | 185 ms                                                      | 181 ms: 1.02x faster                                            |
| xml_etree_process          | 37.2 ms                                                     | 36.8 ms: 1.01x faster                                           |
| regex_dna                  | 116 ms                                                      | 116 ms: 1.01x faster                                            |
| flaskblogging              | 2.03 sec                                                    | 2.03 sec: 1.00x slower                                          |
| deepcopy_reduce            | 2.06 us                                                     | 2.13 us: 1.04x slower                                           |
| regex_effbot               | 1.50 ms                                                     | 1.55 ms: 1.04x slower                                           |
| hexiom                     | 4.55 ms                                                     | 4.72 ms: 1.04x slower                                           |
| django_template            | 24.4 ms                                                     | 25.4 ms: 1.04x slower                                           |
| gc_traversal               | 1.49 ms                                                     | 1.55 ms: 1.04x slower                                           |
| coverage                   | 43.4 ms                                                     | 45.5 ms: 1.05x slower                                           |
| mypy2                      | 459 ms                                                      | 486 ms: 1.06x slower                                            |
| pickle_list                | 2.70 us                                                     | 2.85 us: 1.06x slower                                           |
| sympy_expand               | 299 ms                                                      | 317 ms: 1.06x slower                                            |
| scimark_sor                | 78.1 ms                                                     | 83.5 ms: 1.07x slower                                           |
| sqlglot_optimize           | 34.5 ms                                                     | 37.0 ms: 1.07x slower                                           |
| unpickle_list              | 2.59 us                                                     | 2.78 us: 1.07x slower                                           |
| regex_v8                   | 14.2 ms                                                     | 15.2 ms: 1.07x slower                                           |
| 2to3                       | 214 ms                                                      | 229 ms: 1.07x slower                                            |
| pathlib                    | 70.9 ms                                                     | 76.3 ms: 1.08x slower                                           |
| aiohttp                    | 883 us                                                      | 954 us: 1.08x slower                                            |
| docutils                   | 1.64 sec                                                    | 1.77 sec: 1.08x slower                                          |
| json_loads                 | 13.0 us                                                     | 14.1 us: 1.08x slower                                           |
| pickle                     | 6.64 us                                                     | 7.27 us: 1.10x slower                                           |
| telco                      | 4.06 ms                                                     | 4.46 ms: 1.10x slower                                           |
| scimark_lu                 | 62.8 ms                                                     | 69.4 ms: 1.10x slower                                           |
| genshi_xml                 | 39.9 ms                                                     | 44.2 ms: 1.11x slower                                           |
| python_startup_no_site     | 16.8 ms                                                     | 18.6 ms: 1.11x slower                                           |
| bench_mp_pool              | 63.2 ms                                                     | 72.0 ms: 1.14x slower                                           |
| python_startup             | 19.8 ms                                                     | 22.7 ms: 1.15x slower                                           |
| unpickle                   | 7.57 us                                                     | 8.73 us: 1.15x slower                                           |
| create_gc_cycles           | 713 us                                                      | 912 us: 1.28x slower                                            |
| async_generators           | 177 ms                                                      | 252 ms: 1.42x slower                                            |
| thrift                     | 494 us                                                      | 9.21 ms: 18.66x slower                                          |
| Geometric mean             | (ref)                                                       | 1.07x faster                                                    |

Benchmark hidden because not significant (4): json, pidigits, sympy_integrate, pycparser
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, unpack_sequence

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: unknown