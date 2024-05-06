# Results vs. 3.11.0

- fork: gvanrossum
- ref: backoff_counter_woes
- machine: windows-amd64
- commit hash: 4c1049b
- commit date: 2024-05-04
- overall geometric mean: 1.10x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf1-amd64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 207 ms: 1.03x faster                                                            |
| chameleon      | 5.26 ms                                                     | 4.74 ms: 1.11x faster                                                           |
| html5lib       | 38.9 ms                                                     | 36.4 ms: 1.07x faster                                                           |
| tornado_http   | 92.8 ms                                                     | 79.8 ms: 1.16x faster                                                           |
| Geometric mean | (ref)                                                       | 1.07x faster                                                                    |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf1-amd64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 259 ms: 1.56x faster                                                            |
| async_tree_none            | 332 ms                                                      | 218 ms: 1.52x faster                                                            |
| async_tree_memoization     | 399 ms                                                      | 267 ms: 1.50x faster                                                            |
| async_tree_none_tg         | 309 ms                                                      | 211 ms: 1.46x faster                                                            |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 384 ms: 1.38x faster                                                            |
| async_tree_io              | 808 ms                                                      | 588 ms: 1.37x faster                                                            |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.37x faster                                                            |
| async_tree_io_tg           | 829 ms                                                      | 611 ms: 1.36x faster                                                            |
| Geometric mean             | (ref)                                                       | 1.44x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf1-amd64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 48.7 ms: 1.12x faster                                                           |
| nbody          | 70.3 ms                                                     | 67.0 ms: 1.05x faster                                                           |
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                       | 1.06x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf1-amd64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 78.1 ms: 1.17x faster                                                           |
| regex_dna      | 116 ms                                                      | 118 ms: 1.02x slower                                                            |
| regex_effbot   | 1.50 ms                                                     | 1.59 ms: 1.06x slower                                                           |
| regex_v8       | 14.2 ms                                                     | 15.2 ms: 1.07x slower                                                           |
| Geometric mean | (ref)                                                       | 1.00x faster                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf1-amd64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.57 ms: 1.45x faster                                                           |
| unpickle_pure_python | 157 us                                                      | 124 us: 1.26x faster                                                            |
| pickle_pure_python   | 208 us                                                      | 174 us: 1.20x faster                                                            |
| xml_etree_parse      | 97.6 ms                                                     | 88.2 ms: 1.11x faster                                                           |
| xml_etree_iterparse  | 65.6 ms                                                     | 60.8 ms: 1.08x faster                                                           |
| tomli_loads          | 1.46 sec                                                    | 1.37 sec: 1.06x faster                                                          |
| xml_etree_process    | 37.2 ms                                                     | 36.2 ms: 1.03x faster                                                           |
| xml_etree_generate   | 52.5 ms                                                     | 52.9 ms: 1.01x slower                                                           |
| pickle_dict          | 18.5 us                                                     | 18.9 us: 1.02x slower                                                           |
| unpickle_list        | 2.59 us                                                     | 2.74 us: 1.06x slower                                                           |
| unpickle             | 7.57 us                                                     | 8.17 us: 1.08x slower                                                           |
| json_loads           | 13.0 us                                                     | 14.0 us: 1.08x slower                                                           |
| pickle               | 6.64 us                                                     | 7.47 us: 1.12x slower                                                           |
| pickle_list          | 2.70 us                                                     | 3.28 us: 1.22x slower                                                           |
| Geometric mean       | (ref)                                                       | 1.04x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf1-amd64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 16.4 ms: 1.03x faster                                                           |
| python_startup         | 19.8 ms                                                     | 20.0 ms: 1.01x slower                                                           |
| Geometric mean         | (ref)                                                       | 1.01x faster                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf1-amd64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|-----------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_text     | 18.4 ms                                                     | 15.0 ms: 1.23x faster                                                           |
| genshi_xml      | 39.9 ms                                                     | 34.0 ms: 1.18x faster                                                           |
| mako            | 7.58 ms                                                     | 6.48 ms: 1.17x faster                                                           |
| django_template | 24.4 ms                                                     | 21.7 ms: 1.13x faster                                                           |
| Geometric mean  | (ref)                                                       | 1.17x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf1-amd64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------------------|:-----------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 99.5 us: 3.27x faster                                                           |
| generators                 | 34.0 ms                                                     | 19.0 ms: 1.79x faster                                                           |
| pylint                     | 323 ms                                                      | 206 ms: 1.57x faster                                                            |
| async_tree_memoization_tg  | 405 ms                                                      | 259 ms: 1.56x faster                                                            |
| asyncio_tcp                | 726 ms                                                      | 471 ms: 1.54x faster                                                            |
| comprehensions             | 15.6 us                                                     | 10.2 us: 1.54x faster                                                           |
| async_tree_none            | 332 ms                                                      | 218 ms: 1.52x faster                                                            |
| async_tree_memoization     | 399 ms                                                      | 267 ms: 1.50x faster                                                            |
| async_tree_none_tg         | 309 ms                                                      | 211 ms: 1.46x faster                                                            |
| json_dumps                 | 8.09 ms                                                     | 5.57 ms: 1.45x faster                                                           |
| deltablue                  | 2.70 ms                                                     | 1.89 ms: 1.43x faster                                                           |
| logging_silent             | 71.8 ns                                                     | 50.7 ns: 1.42x faster                                                           |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 384 ms: 1.38x faster                                                            |
| async_tree_io              | 808 ms                                                      | 588 ms: 1.37x faster                                                            |
| raytrace                   | 213 ms                                                      | 156 ms: 1.37x faster                                                            |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.37x faster                                                            |
| async_tree_io_tg           | 829 ms                                                      | 611 ms: 1.36x faster                                                            |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.54 sec: 1.31x faster                                                          |
| richards_super             | 38.7 ms                                                     | 29.7 ms: 1.30x faster                                                           |
| chaos                      | 48.4 ms                                                     | 37.9 ms: 1.28x faster                                                           |
| unpickle_pure_python       | 157 us                                                      | 124 us: 1.26x faster                                                            |
| sqlglot_parse              | 953 us                                                      | 757 us: 1.26x faster                                                            |
| genshi_text                | 18.4 ms                                                     | 15.0 ms: 1.23x faster                                                           |
| mdp                        | 1.59 sec                                                    | 1.31 sec: 1.22x faster                                                          |
| sqlglot_transpile          | 1.16 ms                                                     | 963 us: 1.21x faster                                                            |
| nqueens                    | 68.3 ms                                                     | 56.8 ms: 1.20x faster                                                           |
| pickle_pure_python         | 208 us                                                      | 174 us: 1.20x faster                                                            |
| go                         | 101 ms                                                      | 84.5 ms: 1.20x faster                                                           |
| hexiom                     | 4.55 ms                                                     | 3.81 ms: 1.20x faster                                                           |
| logging_simple             | 6.86 us                                                     | 5.76 us: 1.19x faster                                                           |
| richards                   | 31.4 ms                                                     | 26.4 ms: 1.19x faster                                                           |
| coroutines                 | 15.0 ms                                                     | 12.6 ms: 1.19x faster                                                           |
| deepcopy_memo              | 26.0 us                                                     | 21.9 us: 1.18x faster                                                           |
| sympy_sum                  | 100 ms                                                      | 84.9 ms: 1.18x faster                                                           |
| genshi_xml                 | 39.9 ms                                                     | 34.0 ms: 1.18x faster                                                           |
| mako                       | 7.58 ms                                                     | 6.48 ms: 1.17x faster                                                           |
| regex_compile              | 91.0 ms                                                     | 78.1 ms: 1.17x faster                                                           |
| tornado_http               | 92.8 ms                                                     | 79.8 ms: 1.16x faster                                                           |
| logging_format             | 7.16 us                                                     | 6.17 us: 1.16x faster                                                           |
| scimark_lu                 | 62.8 ms                                                     | 54.4 ms: 1.15x faster                                                           |
| dulwich_log                | 46.4 ms                                                     | 40.2 ms: 1.15x faster                                                           |
| sympy_str                  | 185 ms                                                      | 161 ms: 1.15x faster                                                            |
| spectral_norm              | 68.3 ms                                                     | 59.3 ms: 1.15x faster                                                           |
| scimark_monte_carlo        | 45.3 ms                                                     | 39.7 ms: 1.14x faster                                                           |
| sympy_integrate            | 14.0 ms                                                     | 12.3 ms: 1.14x faster                                                           |
| deepcopy                   | 246 us                                                      | 217 us: 1.14x faster                                                            |
| django_template            | 24.4 ms                                                     | 21.7 ms: 1.13x faster                                                           |
| float                      | 54.4 ms                                                     | 48.7 ms: 1.12x faster                                                           |
| pprint_pformat             | 1.09 sec                                                    | 975 ms: 1.11x faster                                                            |
| pyflate                    | 312 ms                                                      | 281 ms: 1.11x faster                                                            |
| chameleon                  | 5.26 ms                                                     | 4.74 ms: 1.11x faster                                                           |
| xml_etree_parse            | 97.6 ms                                                     | 88.2 ms: 1.11x faster                                                           |
| sqlglot_normalize          | 190 ms                                                      | 172 ms: 1.11x faster                                                            |
| pprint_safe_repr           | 529 ms                                                      | 478 ms: 1.11x faster                                                            |
| sympy_expand               | 299 ms                                                      | 273 ms: 1.10x faster                                                            |
| mypy2                      | 459 ms                                                      | 420 ms: 1.09x faster                                                            |
| bench_thread_pool          | 872 us                                                      | 801 us: 1.09x faster                                                            |
| sqlite_synth               | 1.77 us                                                     | 1.63 us: 1.09x faster                                                           |
| xml_etree_iterparse        | 65.6 ms                                                     | 60.8 ms: 1.08x faster                                                           |
| html5lib                   | 38.9 ms                                                     | 36.4 ms: 1.07x faster                                                           |
| tomli_loads                | 1.46 sec                                                    | 1.37 sec: 1.06x faster                                                          |
| meteor_contest             | 75.2 ms                                                     | 70.9 ms: 1.06x faster                                                           |
| sqlglot_optimize           | 34.5 ms                                                     | 32.6 ms: 1.06x faster                                                           |
| nbody                      | 70.3 ms                                                     | 67.0 ms: 1.05x faster                                                           |
| deepcopy_reduce            | 2.06 us                                                     | 1.97 us: 1.05x faster                                                           |
| crypto_pyaes               | 48.9 ms                                                     | 46.9 ms: 1.04x faster                                                           |
| fannkuch                   | 253 ms                                                      | 245 ms: 1.03x faster                                                            |
| 2to3                       | 214 ms                                                      | 207 ms: 1.03x faster                                                            |
| python_startup_no_site     | 16.8 ms                                                     | 16.4 ms: 1.03x faster                                                           |
| scimark_sor                | 78.1 ms                                                     | 76.0 ms: 1.03x faster                                                           |
| xml_etree_process          | 37.2 ms                                                     | 36.2 ms: 1.03x faster                                                           |
| scimark_fft                | 179 ms                                                      | 175 ms: 1.02x faster                                                            |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                                            |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.55 ms: 1.01x faster                                                           |
| flaskblogging              | 2.03 sec                                                    | 2.03 sec: 1.00x slower                                                          |
| xml_etree_generate         | 52.5 ms                                                     | 52.9 ms: 1.01x slower                                                           |
| python_startup             | 19.8 ms                                                     | 20.0 ms: 1.01x slower                                                           |
| aiohttp                    | 883 us                                                      | 896 us: 1.01x slower                                                            |
| regex_dna                  | 116 ms                                                      | 118 ms: 1.02x slower                                                            |
| bench_mp_pool              | 63.2 ms                                                     | 64.5 ms: 1.02x slower                                                           |
| pickle_dict                | 18.5 us                                                     | 18.9 us: 1.02x slower                                                           |
| coverage                   | 43.4 ms                                                     | 44.6 ms: 1.03x slower                                                           |
| gc_traversal               | 1.49 ms                                                     | 1.55 ms: 1.04x slower                                                           |
| unpickle_list              | 2.59 us                                                     | 2.74 us: 1.06x slower                                                           |
| regex_effbot               | 1.50 ms                                                     | 1.59 ms: 1.06x slower                                                           |
| regex_v8                   | 14.2 ms                                                     | 15.2 ms: 1.07x slower                                                           |
| unpickle                   | 7.57 us                                                     | 8.17 us: 1.08x slower                                                           |
| json_loads                 | 13.0 us                                                     | 14.0 us: 1.08x slower                                                           |
| pathlib                    | 70.9 ms                                                     | 78.7 ms: 1.11x slower                                                           |
| pickle                     | 6.64 us                                                     | 7.47 us: 1.12x slower                                                           |
| dask                       | 273 ms                                                      | 309 ms: 1.13x slower                                                            |
| telco                      | 4.06 ms                                                     | 4.82 ms: 1.19x slower                                                           |
| pickle_list                | 2.70 us                                                     | 3.28 us: 1.22x slower                                                           |
| create_gc_cycles           | 713 us                                                      | 898 us: 1.26x slower                                                            |
| async_generators           | 177 ms                                                      | 228 ms: 1.29x slower                                                            |
| thrift                     | 494 us                                                      | 8.10 ms: 16.41x slower                                                          |
| Geometric mean             | (ref)                                                       | 1.10x faster                                                                    |

Benchmark hidden because not significant (3): docutils, pycparser, json
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.10x
- 95% likely to have a speedup of 1.09x
- 99% likely to have a speedup of 1.08x

# Memory
- memory change: unknown