# Results vs. 3.11.0

- fork: python
- ref: v3.13.0b1
- machine: windows-amd64
- commit hash: 2268289
- commit date: 2024-05-08
- overall geometric mean: 1.10x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-pythonperf1-amd64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 212 ms: 1.01x faster                                            |
| chameleon      | 5.26 ms                                                     | 4.75 ms: 1.11x faster                                           |
| html5lib       | 38.9 ms                                                     | 35.0 ms: 1.11x faster                                           |
| tornado_http   | 92.8 ms                                                     | 82.5 ms: 1.13x faster                                           |
| Geometric mean | (ref)                                                       | 1.07x faster                                                    |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-pythonperf1-amd64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| async_tree_none            | 332 ms                                                      | 219 ms: 1.51x faster                                            |
| async_tree_memoization_tg  | 405 ms                                                      | 267 ms: 1.51x faster                                            |
| async_tree_memoization     | 399 ms                                                      | 266 ms: 1.50x faster                                            |
| async_tree_none_tg         | 309 ms                                                      | 213 ms: 1.45x faster                                            |
| async_tree_io              | 808 ms                                                      | 582 ms: 1.39x faster                                            |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 385 ms: 1.38x faster                                            |
| async_tree_io_tg           | 829 ms                                                      | 604 ms: 1.37x faster                                            |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.36x faster                                            |
| Geometric mean             | (ref)                                                       | 1.43x faster                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-pythonperf1-amd64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 48.5 ms: 1.12x faster                                           |
| nbody          | 70.3 ms                                                     | 67.1 ms: 1.05x faster                                           |
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                            |
| Geometric mean | (ref)                                                       | 1.06x faster                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-pythonperf1-amd64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 78.5 ms: 1.16x faster                                           |
| regex_v8       | 14.2 ms                                                     | 14.3 ms: 1.01x slower                                           |
| regex_dna      | 116 ms                                                      | 118 ms: 1.01x slower                                            |
| regex_effbot   | 1.50 ms                                                     | 1.58 ms: 1.05x slower                                           |
| Geometric mean | (ref)                                                       | 1.02x faster                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-pythonperf1-amd64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.59 ms: 1.45x faster                                           |
| unpickle_pure_python | 157 us                                                      | 127 us: 1.24x faster                                            |
| pickle_pure_python   | 208 us                                                      | 177 us: 1.18x faster                                            |
| xml_etree_parse      | 97.6 ms                                                     | 90.0 ms: 1.08x faster                                           |
| tomli_loads          | 1.46 sec                                                    | 1.37 sec: 1.06x faster                                          |
| xml_etree_iterparse  | 65.6 ms                                                     | 61.9 ms: 1.06x faster                                           |
| xml_etree_process    | 37.2 ms                                                     | 36.8 ms: 1.01x faster                                           |
| pickle_dict          | 18.5 us                                                     | 18.4 us: 1.00x faster                                           |
| xml_etree_generate   | 52.5 ms                                                     | 53.7 ms: 1.02x slower                                           |
| json_loads           | 13.0 us                                                     | 13.7 us: 1.06x slower                                           |
| unpickle_list        | 2.59 us                                                     | 2.77 us: 1.07x slower                                           |
| pickle               | 6.64 us                                                     | 7.17 us: 1.08x slower                                           |
| unpickle             | 7.57 us                                                     | 8.44 us: 1.11x slower                                           |
| pickle_list          | 2.70 us                                                     | 3.02 us: 1.12x slower                                           |
| Geometric mean       | (ref)                                                       | 1.04x faster                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-pythonperf1-amd64-python-v3.13.0b1-3.13.0b1-2268289 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.5 ms: 1.02x faster                                           |
| python_startup         | 19.8 ms                                                     | 20.4 ms: 1.03x slower                                           |
| Geometric mean         | (ref)                                                       | 1.00x slower                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-pythonperf1-amd64-python-v3.13.0b1-3.13.0b1-2268289 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| genshi_text     | 18.4 ms                                                     | 14.7 ms: 1.25x faster                                           |
| genshi_xml      | 39.9 ms                                                     | 32.2 ms: 1.24x faster                                           |
| mako            | 7.58 ms                                                     | 6.28 ms: 1.21x faster                                           |
| django_template | 24.4 ms                                                     | 21.5 ms: 1.14x faster                                           |
| Geometric mean  | (ref)                                                       | 1.21x faster                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-pythonperf1-amd64-python-v3.13.0b1-3.13.0b1-2268289 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 103 us: 3.16x faster                                            |
| generators                 | 34.0 ms                                                     | 18.6 ms: 1.83x faster                                           |
| pylint                     | 323 ms                                                      | 209 ms: 1.54x faster                                            |
| comprehensions             | 15.6 us                                                     | 10.2 us: 1.53x faster                                           |
| async_tree_none            | 332 ms                                                      | 219 ms: 1.51x faster                                            |
| async_tree_memoization_tg  | 405 ms                                                      | 267 ms: 1.51x faster                                            |
| asyncio_tcp                | 726 ms                                                      | 482 ms: 1.51x faster                                            |
| async_tree_memoization     | 399 ms                                                      | 266 ms: 1.50x faster                                            |
| async_tree_none_tg         | 309 ms                                                      | 213 ms: 1.45x faster                                            |
| json_dumps                 | 8.09 ms                                                     | 5.59 ms: 1.45x faster                                           |
| deltablue                  | 2.70 ms                                                     | 1.90 ms: 1.42x faster                                           |
| raytrace                   | 213 ms                                                      | 154 ms: 1.39x faster                                            |
| async_tree_io              | 808 ms                                                      | 582 ms: 1.39x faster                                            |
| logging_silent             | 71.8 ns                                                     | 51.7 ns: 1.39x faster                                           |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 385 ms: 1.38x faster                                            |
| async_tree_io_tg           | 829 ms                                                      | 604 ms: 1.37x faster                                            |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.36x faster                                            |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.51 sec: 1.34x faster                                          |
| richards_super             | 38.7 ms                                                     | 29.9 ms: 1.29x faster                                           |
| sqlglot_parse              | 953 us                                                      | 754 us: 1.26x faster                                            |
| chaos                      | 48.4 ms                                                     | 38.3 ms: 1.26x faster                                           |
| genshi_text                | 18.4 ms                                                     | 14.7 ms: 1.25x faster                                           |
| genshi_xml                 | 39.9 ms                                                     | 32.2 ms: 1.24x faster                                           |
| unpickle_pure_python       | 157 us                                                      | 127 us: 1.24x faster                                            |
| nqueens                    | 68.3 ms                                                     | 56.2 ms: 1.22x faster                                           |
| mdp                        | 1.59 sec                                                    | 1.31 sec: 1.21x faster                                          |
| hexiom                     | 4.55 ms                                                     | 3.76 ms: 1.21x faster                                           |
| sqlglot_transpile          | 1.16 ms                                                     | 962 us: 1.21x faster                                            |
| mako                       | 7.58 ms                                                     | 6.28 ms: 1.21x faster                                           |
| go                         | 101 ms                                                      | 84.3 ms: 1.20x faster                                           |
| coroutines                 | 15.0 ms                                                     | 12.6 ms: 1.18x faster                                           |
| logging_simple             | 6.86 us                                                     | 5.80 us: 1.18x faster                                           |
| richards                   | 31.4 ms                                                     | 26.6 ms: 1.18x faster                                           |
| pickle_pure_python         | 208 us                                                      | 177 us: 1.18x faster                                            |
| sympy_sum                  | 100 ms                                                      | 85.2 ms: 1.17x faster                                           |
| dulwich_log                | 46.4 ms                                                     | 39.6 ms: 1.17x faster                                           |
| regex_compile              | 91.0 ms                                                     | 78.5 ms: 1.16x faster                                           |
| logging_format             | 7.16 us                                                     | 6.22 us: 1.15x faster                                           |
| sympy_str                  | 185 ms                                                      | 162 ms: 1.14x faster                                            |
| django_template            | 24.4 ms                                                     | 21.5 ms: 1.14x faster                                           |
| sympy_integrate            | 14.0 ms                                                     | 12.5 ms: 1.13x faster                                           |
| tornado_http               | 92.8 ms                                                     | 82.5 ms: 1.13x faster                                           |
| deepcopy_memo              | 26.0 us                                                     | 23.1 us: 1.12x faster                                           |
| float                      | 54.4 ms                                                     | 48.5 ms: 1.12x faster                                           |
| scimark_monte_carlo        | 45.3 ms                                                     | 40.5 ms: 1.12x faster                                           |
| pyflate                    | 312 ms                                                      | 280 ms: 1.11x faster                                            |
| html5lib                   | 38.9 ms                                                     | 35.0 ms: 1.11x faster                                           |
| chameleon                  | 5.26 ms                                                     | 4.75 ms: 1.11x faster                                           |
| pprint_pformat             | 1.09 sec                                                    | 982 ms: 1.11x faster                                            |
| scimark_lu                 | 62.8 ms                                                     | 56.8 ms: 1.11x faster                                           |
| sqlglot_normalize          | 190 ms                                                      | 172 ms: 1.11x faster                                            |
| deepcopy                   | 246 us                                                      | 223 us: 1.10x faster                                            |
| spectral_norm              | 68.3 ms                                                     | 61.9 ms: 1.10x faster                                           |
| pprint_safe_repr           | 529 ms                                                      | 481 ms: 1.10x faster                                            |
| bench_thread_pool          | 872 us                                                      | 793 us: 1.10x faster                                            |
| sqlite_synth               | 1.77 us                                                     | 1.62 us: 1.09x faster                                           |
| sympy_expand               | 299 ms                                                      | 275 ms: 1.09x faster                                            |
| xml_etree_parse            | 97.6 ms                                                     | 90.0 ms: 1.08x faster                                           |
| mypy2                      | 459 ms                                                      | 427 ms: 1.08x faster                                            |
| pycparser                  | 720 ms                                                      | 669 ms: 1.08x faster                                            |
| tomli_loads                | 1.46 sec                                                    | 1.37 sec: 1.06x faster                                          |
| xml_etree_iterparse        | 65.6 ms                                                     | 61.9 ms: 1.06x faster                                           |
| meteor_contest             | 75.2 ms                                                     | 71.3 ms: 1.05x faster                                           |
| sqlglot_optimize           | 34.5 ms                                                     | 32.9 ms: 1.05x faster                                           |
| nbody                      | 70.3 ms                                                     | 67.1 ms: 1.05x faster                                           |
| crypto_pyaes               | 48.9 ms                                                     | 46.9 ms: 1.04x faster                                           |
| deepcopy_reduce            | 2.06 us                                                     | 1.98 us: 1.04x faster                                           |
| fannkuch                   | 253 ms                                                      | 244 ms: 1.04x faster                                            |
| scimark_sor                | 78.1 ms                                                     | 75.9 ms: 1.03x faster                                           |
| scimark_fft                | 179 ms                                                      | 175 ms: 1.03x faster                                            |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                            |
| python_startup_no_site     | 16.8 ms                                                     | 16.5 ms: 1.02x faster                                           |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.53 ms: 1.02x faster                                           |
| xml_etree_process          | 37.2 ms                                                     | 36.8 ms: 1.01x faster                                           |
| 2to3                       | 214 ms                                                      | 212 ms: 1.01x faster                                            |
| pickle_dict                | 18.5 us                                                     | 18.4 us: 1.00x faster                                           |
| regex_v8                   | 14.2 ms                                                     | 14.3 ms: 1.01x slower                                           |
| regex_dna                  | 116 ms                                                      | 118 ms: 1.01x slower                                            |
| xml_etree_generate         | 52.5 ms                                                     | 53.7 ms: 1.02x slower                                           |
| aiohttp                    | 883 us                                                      | 908 us: 1.03x slower                                            |
| python_startup             | 19.8 ms                                                     | 20.4 ms: 1.03x slower                                           |
| bench_mp_pool              | 63.2 ms                                                     | 65.3 ms: 1.03x slower                                           |
| gc_traversal               | 1.49 ms                                                     | 1.55 ms: 1.04x slower                                           |
| coverage                   | 43.4 ms                                                     | 45.3 ms: 1.04x slower                                           |
| regex_effbot               | 1.50 ms                                                     | 1.58 ms: 1.05x slower                                           |
| json_loads                 | 13.0 us                                                     | 13.7 us: 1.06x slower                                           |
| unpickle_list              | 2.59 us                                                     | 2.77 us: 1.07x slower                                           |
| pickle                     | 6.64 us                                                     | 7.17 us: 1.08x slower                                           |
| unpickle                   | 7.57 us                                                     | 8.44 us: 1.11x slower                                           |
| pickle_list                | 2.70 us                                                     | 3.02 us: 1.12x slower                                           |
| pathlib                    | 70.9 ms                                                     | 80.1 ms: 1.13x slower                                           |
| dask                       | 273 ms                                                      | 316 ms: 1.16x slower                                            |
| telco                      | 4.06 ms                                                     | 4.72 ms: 1.16x slower                                           |
| create_gc_cycles           | 713 us                                                      | 893 us: 1.25x slower                                            |
| async_generators           | 177 ms                                                      | 225 ms: 1.27x slower                                            |
| thrift                     | 494 us                                                      | 8.23 ms: 16.66x slower                                          |
| Geometric mean             | (ref)                                                       | 1.10x faster                                                    |

Benchmark hidden because not significant (3): json, docutils, flaskblogging
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.09x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: unknown