# Results vs. 3.11.0

- fork: python
- ref: v3.13.0b2
- machine: windows-amd64
- commit hash: 3a83b17
- commit date: 2024-06-05
- overall geometric mean: 1.11x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 207 ms: 1.03x faster                                            |
| chameleon      | 5.26 ms                                                     | 4.80 ms: 1.10x faster                                           |
| docutils       | 1.64 sec                                                    | 1.63 sec: 1.01x faster                                          |
| html5lib       | 38.9 ms                                                     | 35.0 ms: 1.11x faster                                           |
| tornado_http   | 92.8 ms                                                     | 81.8 ms: 1.13x faster                                           |
| Geometric mean | (ref)                                                       | 1.08x faster                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 258 ms: 1.57x faster                                            |
| async_tree_none_tg         | 309 ms                                                      | 202 ms: 1.53x faster                                            |
| async_tree_none            | 332 ms                                                      | 218 ms: 1.52x faster                                            |
| async_tree_memoization     | 399 ms                                                      | 264 ms: 1.51x faster                                            |
| async_tree_io              | 808 ms                                                      | 588 ms: 1.37x faster                                            |
| async_tree_io_tg           | 829 ms                                                      | 605 ms: 1.37x faster                                            |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 382 ms: 1.37x faster                                            |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 389 ms: 1.36x faster                                            |
| Geometric mean             | (ref)                                                       | 1.45x faster                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 49.7 ms: 1.09x faster                                           |
| nbody          | 70.3 ms                                                     | 67.6 ms: 1.04x faster                                           |
| Geometric mean | (ref)                                                       | 1.04x faster                                                    |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 78.0 ms: 1.17x faster                                           |
| regex_dna      | 116 ms                                                      | 119 ms: 1.02x slower                                            |
| regex_effbot   | 1.50 ms                                                     | 1.58 ms: 1.06x slower                                           |
| regex_v8       | 14.2 ms                                                     | 15.8 ms: 1.11x slower                                           |
| Geometric mean | (ref)                                                       | 1.01x slower                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.61 ms: 1.44x faster                                           |
| unpickle_pure_python | 157 us                                                      | 122 us: 1.29x faster                                            |
| pickle_pure_python   | 208 us                                                      | 175 us: 1.19x faster                                            |
| tomli_loads          | 1.46 sec                                                    | 1.35 sec: 1.08x faster                                          |
| xml_etree_parse      | 97.6 ms                                                     | 90.9 ms: 1.07x faster                                           |
| xml_etree_iterparse  | 65.6 ms                                                     | 62.3 ms: 1.05x faster                                           |
| xml_etree_process    | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                           |
| pickle_dict          | 18.5 us                                                     | 18.1 us: 1.02x faster                                           |
| xml_etree_generate   | 52.5 ms                                                     | 53.2 ms: 1.01x slower                                           |
| unpickle_list        | 2.59 us                                                     | 2.62 us: 1.01x slower                                           |
| pickle               | 6.64 us                                                     | 7.11 us: 1.07x slower                                           |
| pickle_list          | 2.70 us                                                     | 2.90 us: 1.08x slower                                           |
| json_loads           | 13.0 us                                                     | 14.2 us: 1.09x slower                                           |
| unpickle             | 7.57 us                                                     | 8.40 us: 1.11x slower                                           |
| Geometric mean       | (ref)                                                       | 1.05x faster                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.2 ms: 1.04x faster                                           |
| python_startup         | 19.8 ms                                                     | 20.3 ms: 1.03x slower                                           |
| Geometric mean         | (ref)                                                       | 1.01x faster                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| genshi_text     | 18.4 ms                                                     | 14.4 ms: 1.28x faster                                           |
| genshi_xml      | 39.9 ms                                                     | 31.6 ms: 1.26x faster                                           |
| mako            | 7.58 ms                                                     | 6.36 ms: 1.19x faster                                           |
| django_template | 24.4 ms                                                     | 21.7 ms: 1.13x faster                                           |
| Geometric mean  | (ref)                                                       | 1.22x faster                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240605-pythonperf1-amd64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 101 us: 3.23x faster                                            |
| generators                 | 34.0 ms                                                     | 19.6 ms: 1.74x faster                                           |
| pylint                     | 323 ms                                                      | 205 ms: 1.58x faster                                            |
| async_tree_memoization_tg  | 405 ms                                                      | 258 ms: 1.57x faster                                            |
| asyncio_tcp                | 726 ms                                                      | 471 ms: 1.54x faster                                            |
| async_tree_none_tg         | 309 ms                                                      | 202 ms: 1.53x faster                                            |
| async_tree_none            | 332 ms                                                      | 218 ms: 1.52x faster                                            |
| async_tree_memoization     | 399 ms                                                      | 264 ms: 1.51x faster                                            |
| comprehensions             | 15.6 us                                                     | 10.4 us: 1.51x faster                                           |
| json_dumps                 | 8.09 ms                                                     | 5.61 ms: 1.44x faster                                           |
| deltablue                  | 2.70 ms                                                     | 1.88 ms: 1.43x faster                                           |
| async_tree_io              | 808 ms                                                      | 588 ms: 1.37x faster                                            |
| async_tree_io_tg           | 829 ms                                                      | 605 ms: 1.37x faster                                            |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.48 sec: 1.37x faster                                          |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 382 ms: 1.37x faster                                            |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 389 ms: 1.36x faster                                            |
| logging_silent             | 71.8 ns                                                     | 52.9 ns: 1.36x faster                                           |
| raytrace                   | 213 ms                                                      | 162 ms: 1.32x faster                                            |
| unpickle_pure_python       | 157 us                                                      | 122 us: 1.29x faster                                            |
| richards_super             | 38.7 ms                                                     | 30.2 ms: 1.28x faster                                           |
| genshi_text                | 18.4 ms                                                     | 14.4 ms: 1.28x faster                                           |
| sqlglot_parse              | 953 us                                                      | 748 us: 1.27x faster                                            |
| genshi_xml                 | 39.9 ms                                                     | 31.6 ms: 1.26x faster                                           |
| chaos                      | 48.4 ms                                                     | 38.4 ms: 1.26x faster                                           |
| go                         | 101 ms                                                      | 82.1 ms: 1.23x faster                                           |
| hexiom                     | 4.55 ms                                                     | 3.72 ms: 1.22x faster                                           |
| sqlglot_transpile          | 1.16 ms                                                     | 955 us: 1.22x faster                                            |
| dulwich_log                | 46.4 ms                                                     | 38.0 ms: 1.22x faster                                           |
| mdp                        | 1.59 sec                                                    | 1.31 sec: 1.21x faster                                          |
| nqueens                    | 68.3 ms                                                     | 56.7 ms: 1.21x faster                                           |
| mako                       | 7.58 ms                                                     | 6.36 ms: 1.19x faster                                           |
| pickle_pure_python         | 208 us                                                      | 175 us: 1.19x faster                                            |
| logging_simple             | 6.86 us                                                     | 5.78 us: 1.19x faster                                           |
| sympy_sum                  | 100 ms                                                      | 84.4 ms: 1.19x faster                                           |
| richards                   | 31.4 ms                                                     | 26.7 ms: 1.18x faster                                           |
| deepcopy_memo              | 26.0 us                                                     | 22.1 us: 1.18x faster                                           |
| coroutines                 | 15.0 ms                                                     | 12.8 ms: 1.17x faster                                           |
| regex_compile              | 91.0 ms                                                     | 78.0 ms: 1.17x faster                                           |
| sympy_str                  | 185 ms                                                      | 159 ms: 1.16x faster                                            |
| scimark_monte_carlo        | 45.3 ms                                                     | 39.1 ms: 1.16x faster                                           |
| logging_format             | 7.16 us                                                     | 6.22 us: 1.15x faster                                           |
| sympy_integrate            | 14.0 ms                                                     | 12.2 ms: 1.15x faster                                           |
| bench_thread_pool          | 872 us                                                      | 768 us: 1.14x faster                                            |
| tornado_http               | 92.8 ms                                                     | 81.8 ms: 1.13x faster                                           |
| django_template            | 24.4 ms                                                     | 21.7 ms: 1.13x faster                                           |
| pprint_pformat             | 1.09 sec                                                    | 966 ms: 1.13x faster                                            |
| deepcopy                   | 246 us                                                      | 220 us: 1.12x faster                                            |
| pyflate                    | 312 ms                                                      | 279 ms: 1.12x faster                                            |
| pprint_safe_repr           | 529 ms                                                      | 474 ms: 1.12x faster                                            |
| scimark_lu                 | 62.8 ms                                                     | 56.6 ms: 1.11x faster                                           |
| html5lib                   | 38.9 ms                                                     | 35.0 ms: 1.11x faster                                           |
| sqlite_synth               | 1.77 us                                                     | 1.60 us: 1.11x faster                                           |
| sympy_expand               | 299 ms                                                      | 271 ms: 1.10x faster                                            |
| sqlglot_normalize          | 190 ms                                                      | 173 ms: 1.10x faster                                            |
| mypy2                      | 459 ms                                                      | 418 ms: 1.10x faster                                            |
| chameleon                  | 5.26 ms                                                     | 4.80 ms: 1.10x faster                                           |
| float                      | 54.4 ms                                                     | 49.7 ms: 1.09x faster                                           |
| tomli_loads                | 1.46 sec                                                    | 1.35 sec: 1.08x faster                                          |
| meteor_contest             | 75.2 ms                                                     | 69.9 ms: 1.08x faster                                           |
| crypto_pyaes               | 48.9 ms                                                     | 45.5 ms: 1.07x faster                                           |
| xml_etree_parse            | 97.6 ms                                                     | 90.9 ms: 1.07x faster                                           |
| spectral_norm              | 68.3 ms                                                     | 63.7 ms: 1.07x faster                                           |
| sqlglot_optimize           | 34.5 ms                                                     | 32.7 ms: 1.06x faster                                           |
| xml_etree_iterparse        | 65.6 ms                                                     | 62.3 ms: 1.05x faster                                           |
| scimark_fft                | 179 ms                                                      | 171 ms: 1.05x faster                                            |
| fannkuch                   | 253 ms                                                      | 243 ms: 1.04x faster                                            |
| nbody                      | 70.3 ms                                                     | 67.6 ms: 1.04x faster                                           |
| python_startup_no_site     | 16.8 ms                                                     | 16.2 ms: 1.04x faster                                           |
| scimark_sor                | 78.1 ms                                                     | 75.3 ms: 1.04x faster                                           |
| deepcopy_reduce            | 2.06 us                                                     | 1.99 us: 1.03x faster                                           |
| 2to3                       | 214 ms                                                      | 207 ms: 1.03x faster                                            |
| coverage                   | 43.4 ms                                                     | 42.1 ms: 1.03x faster                                           |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.50 ms: 1.03x faster                                           |
| xml_etree_process          | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                           |
| pickle_dict                | 18.5 us                                                     | 18.1 us: 1.02x faster                                           |
| docutils                   | 1.64 sec                                                    | 1.63 sec: 1.01x faster                                          |
| flaskblogging              | 2.03 sec                                                    | 2.03 sec: 1.00x slower                                          |
| xml_etree_generate         | 52.5 ms                                                     | 53.2 ms: 1.01x slower                                           |
| unpickle_list              | 2.59 us                                                     | 2.62 us: 1.01x slower                                           |
| regex_dna                  | 116 ms                                                      | 119 ms: 1.02x slower                                            |
| bench_mp_pool              | 63.2 ms                                                     | 64.8 ms: 1.02x slower                                           |
| python_startup             | 19.8 ms                                                     | 20.3 ms: 1.03x slower                                           |
| gc_traversal               | 1.49 ms                                                     | 1.55 ms: 1.04x slower                                           |
| regex_effbot               | 1.50 ms                                                     | 1.58 ms: 1.06x slower                                           |
| pathlib                    | 70.9 ms                                                     | 75.9 ms: 1.07x slower                                           |
| json                       | 2.98 ms                                                     | 3.19 ms: 1.07x slower                                           |
| pickle                     | 6.64 us                                                     | 7.11 us: 1.07x slower                                           |
| pickle_list                | 2.70 us                                                     | 2.90 us: 1.08x slower                                           |
| json_loads                 | 13.0 us                                                     | 14.2 us: 1.09x slower                                           |
| unpickle                   | 7.57 us                                                     | 8.40 us: 1.11x slower                                           |
| regex_v8                   | 14.2 ms                                                     | 15.8 ms: 1.11x slower                                           |
| telco                      | 4.06 ms                                                     | 4.67 ms: 1.15x slower                                           |
| create_gc_cycles           | 713 us                                                      | 888 us: 1.24x slower                                            |
| async_generators           | 177 ms                                                      | 223 ms: 1.26x slower                                            |
| thrift                     | 494 us                                                      | 8.11 ms: 16.42x slower                                          |
| Geometric mean             | (ref)                                                       | 1.11x faster                                                    |

Benchmark hidden because not significant (3): pidigits, aiohttp, pycparser
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: unknown