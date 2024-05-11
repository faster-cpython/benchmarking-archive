# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a4
- machine: windows-amd64
- commit hash: 9d34f60
- commit date: 2024-02-15
- overall geometric mean: 1.07x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf1-amd64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| chameleon      | 5.26 ms                                                     | 5.01 ms: 1.05x faster                                           |
| docutils       | 1.64 sec                                                    | 1.55 sec: 1.06x faster                                          |
| html5lib       | 38.9 ms                                                     | 36.9 ms: 1.05x faster                                           |
| tornado_http   | 92.8 ms                                                     | 84.3 ms: 1.10x faster                                           |
| Geometric mean | (ref)                                                       | 1.05x faster                                                    |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf1-amd64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| async_tree_none            | 332 ms                                                      | 266 ms: 1.25x faster                                            |
| async_tree_memoization     | 399 ms                                                      | 340 ms: 1.17x faster                                            |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 453 ms: 1.17x faster                                            |
| async_tree_memoization_tg  | 405 ms                                                      | 349 ms: 1.16x faster                                            |
| async_tree_none_tg         | 309 ms                                                      | 274 ms: 1.13x faster                                            |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 472 ms: 1.11x faster                                            |
| async_tree_io              | 808 ms                                                      | 732 ms: 1.10x faster                                            |
| async_tree_io_tg           | 829 ms                                                      | 758 ms: 1.09x faster                                            |
| Geometric mean             | (ref)                                                       | 1.15x faster                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf1-amd64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 51.0 ms: 1.07x faster                                           |
| pidigits       | 150 ms                                                      | 148 ms: 1.02x faster                                            |
| nbody          | 70.3 ms                                                     | 73.2 ms: 1.04x slower                                           |
| Geometric mean | (ref)                                                       | 1.01x faster                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf1-amd64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 77.8 ms: 1.17x faster                                           |
| regex_dna      | 116 ms                                                      | 115 ms: 1.01x faster                                            |
| regex_v8       | 14.2 ms                                                     | 14.4 ms: 1.02x slower                                           |
| regex_effbot   | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                           |
| Geometric mean | (ref)                                                       | 1.03x faster                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf1-amd64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.58 ms: 1.45x faster                                           |
| unpickle_pure_python | 157 us                                                      | 129 us: 1.21x faster                                            |
| pickle_pure_python   | 208 us                                                      | 186 us: 1.12x faster                                            |
| xml_etree_parse      | 97.6 ms                                                     | 92.2 ms: 1.06x faster                                           |
| tomli_loads          | 1.46 sec                                                    | 1.43 sec: 1.02x faster                                          |
| pickle_dict          | 18.5 us                                                     | 18.4 us: 1.01x faster                                           |
| unpickle_list        | 2.59 us                                                     | 2.68 us: 1.04x slower                                           |
| xml_etree_generate   | 52.5 ms                                                     | 54.5 ms: 1.04x slower                                           |
| json_loads           | 13.0 us                                                     | 13.7 us: 1.05x slower                                           |
| pickle_list          | 2.70 us                                                     | 2.96 us: 1.10x slower                                           |
| pickle               | 6.64 us                                                     | 7.32 us: 1.10x slower                                           |
| unpickle             | 7.57 us                                                     | 8.66 us: 1.14x slower                                           |
| Geometric mean       | (ref)                                                       | 1.02x faster                                                    |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf1-amd64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| python_startup         | 19.8 ms                                                     | 20.2 ms: 1.02x slower                                           |
| python_startup_no_site | 16.8 ms                                                     | 17.8 ms: 1.06x slower                                           |
| Geometric mean         | (ref)                                                       | 1.04x slower                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf1-amd64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 6.29 ms: 1.21x faster                                           |
| genshi_text     | 18.4 ms                                                     | 16.0 ms: 1.15x faster                                           |
| genshi_xml      | 39.9 ms                                                     | 35.1 ms: 1.14x faster                                           |
| django_template | 24.4 ms                                                     | 22.5 ms: 1.09x faster                                           |
| Geometric mean  | (ref)                                                       | 1.15x faster                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240215-pythonperf1-amd64-python-v3.13.0a4-3.13.0a4-9d34f60 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 71.0 us: 4.59x faster                                           |
| generators                 | 34.0 ms                                                     | 20.8 ms: 1.63x faster                                           |
| pylint                     | 323 ms                                                      | 207 ms: 1.56x faster                                            |
| asyncio_tcp                | 726 ms                                                      | 481 ms: 1.51x faster                                            |
| comprehensions             | 15.6 us                                                     | 10.8 us: 1.45x faster                                           |
| json_dumps                 | 8.09 ms                                                     | 5.58 ms: 1.45x faster                                           |
| deltablue                  | 2.70 ms                                                     | 1.98 ms: 1.36x faster                                           |
| raytrace                   | 213 ms                                                      | 165 ms: 1.30x faster                                            |
| logging_silent             | 71.8 ns                                                     | 57.3 ns: 1.25x faster                                           |
| async_tree_none            | 332 ms                                                      | 266 ms: 1.25x faster                                            |
| sqlglot_parse              | 953 us                                                      | 768 us: 1.24x faster                                            |
| chaos                      | 48.4 ms                                                     | 39.5 ms: 1.23x faster                                           |
| richards_super             | 38.7 ms                                                     | 31.6 ms: 1.22x faster                                           |
| unpickle_pure_python       | 157 us                                                      | 129 us: 1.21x faster                                            |
| mako                       | 7.58 ms                                                     | 6.29 ms: 1.21x faster                                           |
| sympy_sum                  | 100 ms                                                      | 83.5 ms: 1.20x faster                                           |
| go                         | 101 ms                                                      | 84.4 ms: 1.20x faster                                           |
| hexiom                     | 4.55 ms                                                     | 3.82 ms: 1.19x faster                                           |
| mdp                        | 1.59 sec                                                    | 1.34 sec: 1.19x faster                                          |
| sqlglot_transpile          | 1.16 ms                                                     | 983 us: 1.18x faster                                            |
| nqueens                    | 68.3 ms                                                     | 58.2 ms: 1.17x faster                                           |
| async_tree_memoization     | 399 ms                                                      | 340 ms: 1.17x faster                                            |
| regex_compile              | 91.0 ms                                                     | 77.8 ms: 1.17x faster                                           |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 453 ms: 1.17x faster                                            |
| sympy_str                  | 185 ms                                                      | 160 ms: 1.16x faster                                            |
| async_tree_memoization_tg  | 405 ms                                                      | 349 ms: 1.16x faster                                            |
| spectral_norm              | 68.3 ms                                                     | 59.0 ms: 1.16x faster                                           |
| sqlite_synth               | 1.77 us                                                     | 1.53 us: 1.15x faster                                           |
| genshi_text                | 18.4 ms                                                     | 16.0 ms: 1.15x faster                                           |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.77 sec: 1.14x faster                                          |
| crypto_pyaes               | 48.9 ms                                                     | 42.8 ms: 1.14x faster                                           |
| scimark_lu                 | 62.8 ms                                                     | 55.0 ms: 1.14x faster                                           |
| genshi_xml                 | 39.9 ms                                                     | 35.1 ms: 1.14x faster                                           |
| sympy_integrate            | 14.0 ms                                                     | 12.4 ms: 1.13x faster                                           |
| deepcopy_memo              | 26.0 us                                                     | 23.0 us: 1.13x faster                                           |
| coroutines                 | 15.0 ms                                                     | 13.2 ms: 1.13x faster                                           |
| async_tree_none_tg         | 309 ms                                                      | 274 ms: 1.13x faster                                            |
| dulwich_log                | 46.4 ms                                                     | 41.3 ms: 1.12x faster                                           |
| pickle_pure_python         | 208 us                                                      | 186 us: 1.12x faster                                            |
| richards                   | 31.4 ms                                                     | 28.0 ms: 1.12x faster                                           |
| logging_simple             | 6.86 us                                                     | 6.15 us: 1.12x faster                                           |
| scimark_monte_carlo        | 45.3 ms                                                     | 40.7 ms: 1.11x faster                                           |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 472 ms: 1.11x faster                                            |
| mypy2                      | 459 ms                                                      | 416 ms: 1.10x faster                                            |
| async_tree_io              | 808 ms                                                      | 732 ms: 1.10x faster                                            |
| tornado_http               | 92.8 ms                                                     | 84.3 ms: 1.10x faster                                           |
| pyflate                    | 312 ms                                                      | 285 ms: 1.09x faster                                            |
| async_tree_io_tg           | 829 ms                                                      | 758 ms: 1.09x faster                                            |
| sympy_expand               | 299 ms                                                      | 274 ms: 1.09x faster                                            |
| logging_format             | 7.16 us                                                     | 6.57 us: 1.09x faster                                           |
| django_template            | 24.4 ms                                                     | 22.5 ms: 1.09x faster                                           |
| sqlglot_normalize          | 190 ms                                                      | 176 ms: 1.08x faster                                            |
| float                      | 54.4 ms                                                     | 51.0 ms: 1.07x faster                                           |
| pprint_pformat             | 1.09 sec                                                    | 1.02 sec: 1.06x faster                                          |
| docutils                   | 1.64 sec                                                    | 1.55 sec: 1.06x faster                                          |
| xml_etree_parse            | 97.6 ms                                                     | 92.2 ms: 1.06x faster                                           |
| deepcopy                   | 246 us                                                      | 233 us: 1.06x faster                                            |
| pprint_safe_repr           | 529 ms                                                      | 500 ms: 1.06x faster                                            |
| bench_thread_pool          | 872 us                                                      | 824 us: 1.06x faster                                            |
| html5lib                   | 38.9 ms                                                     | 36.9 ms: 1.05x faster                                           |
| chameleon                  | 5.26 ms                                                     | 5.01 ms: 1.05x faster                                           |
| meteor_contest             | 75.2 ms                                                     | 72.2 ms: 1.04x faster                                           |
| sqlglot_optimize           | 34.5 ms                                                     | 33.4 ms: 1.03x faster                                           |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.49 ms: 1.03x faster                                           |
| tomli_loads                | 1.46 sec                                                    | 1.43 sec: 1.02x faster                                          |
| pidigits                   | 150 ms                                                      | 148 ms: 1.02x faster                                            |
| fannkuch                   | 253 ms                                                      | 250 ms: 1.01x faster                                            |
| regex_dna                  | 116 ms                                                      | 115 ms: 1.01x faster                                            |
| pickle_dict                | 18.5 us                                                     | 18.4 us: 1.01x faster                                           |
| deepcopy_reduce            | 2.06 us                                                     | 2.05 us: 1.01x faster                                           |
| regex_v8                   | 14.2 ms                                                     | 14.4 ms: 1.02x slower                                           |
| python_startup             | 19.8 ms                                                     | 20.2 ms: 1.02x slower                                           |
| unpickle_list              | 2.59 us                                                     | 2.68 us: 1.04x slower                                           |
| xml_etree_generate         | 52.5 ms                                                     | 54.5 ms: 1.04x slower                                           |
| nbody                      | 70.3 ms                                                     | 73.2 ms: 1.04x slower                                           |
| create_gc_cycles           | 713 us                                                      | 743 us: 1.04x slower                                            |
| regex_effbot               | 1.50 ms                                                     | 1.56 ms: 1.04x slower                                           |
| bench_mp_pool              | 63.2 ms                                                     | 66.4 ms: 1.05x slower                                           |
| json_loads                 | 13.0 us                                                     | 13.7 us: 1.05x slower                                           |
| python_startup_no_site     | 16.8 ms                                                     | 17.8 ms: 1.06x slower                                           |
| coverage                   | 43.4 ms                                                     | 47.3 ms: 1.09x slower                                           |
| pickle_list                | 2.70 us                                                     | 2.96 us: 1.10x slower                                           |
| pickle                     | 6.64 us                                                     | 7.32 us: 1.10x slower                                           |
| pathlib                    | 70.9 ms                                                     | 80.8 ms: 1.14x slower                                           |
| unpickle                   | 7.57 us                                                     | 8.66 us: 1.14x slower                                           |
| telco                      | 4.06 ms                                                     | 4.73 ms: 1.16x slower                                           |
| async_generators           | 177 ms                                                      | 230 ms: 1.30x slower                                            |
| thrift                     | 494 us                                                      | 8.18 ms: 16.57x slower                                          |
| Geometric mean             | (ref)                                                       | 1.07x faster                                                    |

Benchmark hidden because not significant (10): json, xml_etree_iterparse, scimark_sor, xml_etree_process, scimark_fft, flaskblogging, 2to3, aiohttp, gc_traversal, pycparser
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: unknown