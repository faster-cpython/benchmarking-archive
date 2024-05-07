# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a3
- machine: windows-amd64
- commit hash: f009305
- commit date: 2024-01-17
- overall geometric mean: 1.08x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf1-amd64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 210 ms: 1.02x faster                                            |
| chameleon      | 5.26 ms                                                     | 4.91 ms: 1.07x faster                                           |
| docutils       | 1.64 sec                                                    | 1.53 sec: 1.07x faster                                          |
| html5lib       | 38.9 ms                                                     | 35.9 ms: 1.08x faster                                           |
| tornado_http   | 92.8 ms                                                     | 85.5 ms: 1.09x faster                                           |
| Geometric mean | (ref)                                                       | 1.06x faster                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf1-amd64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| async_tree_none            | 332 ms                                                      | 263 ms: 1.26x faster                                            |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 448 ms: 1.18x faster                                            |
| async_tree_memoization     | 399 ms                                                      | 341 ms: 1.17x faster                                            |
| async_tree_memoization_tg  | 405 ms                                                      | 349 ms: 1.16x faster                                            |
| async_tree_none_tg         | 309 ms                                                      | 270 ms: 1.14x faster                                            |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 465 ms: 1.12x faster                                            |
| async_tree_io              | 808 ms                                                      | 724 ms: 1.12x faster                                            |
| async_tree_io_tg           | 829 ms                                                      | 750 ms: 1.11x faster                                            |
| Geometric mean             | (ref)                                                       | 1.16x faster                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf1-amd64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 52.5 ms: 1.04x faster                                           |
| pidigits       | 150 ms                                                      | 148 ms: 1.02x faster                                            |
| nbody          | 70.3 ms                                                     | 74.1 ms: 1.05x slower                                           |
| Geometric mean | (ref)                                                       | 1.00x slower                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf1-amd64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 77.7 ms: 1.17x faster                                           |
| regex_dna      | 116 ms                                                      | 121 ms: 1.04x slower                                            |
| regex_effbot   | 1.50 ms                                                     | 1.59 ms: 1.06x slower                                           |
| regex_v8       | 14.2 ms                                                     | 15.3 ms: 1.08x slower                                           |
| Geometric mean | (ref)                                                       | 1.00x slower                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf1-amd64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.54 ms: 1.46x faster                                           |
| unpickle_pure_python | 157 us                                                      | 128 us: 1.22x faster                                            |
| pickle_pure_python   | 208 us                                                      | 179 us: 1.17x faster                                            |
| xml_etree_parse      | 97.6 ms                                                     | 93.0 ms: 1.05x faster                                           |
| tomli_loads          | 1.46 sec                                                    | 1.39 sec: 1.04x faster                                          |
| xml_etree_iterparse  | 65.6 ms                                                     | 63.5 ms: 1.03x faster                                           |
| xml_etree_process    | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                           |
| pickle_dict          | 18.5 us                                                     | 18.2 us: 1.02x faster                                           |
| xml_etree_generate   | 52.5 ms                                                     | 53.6 ms: 1.02x slower                                           |
| json_loads           | 13.0 us                                                     | 13.7 us: 1.05x slower                                           |
| unpickle_list        | 2.59 us                                                     | 2.73 us: 1.05x slower                                           |
| pickle_list          | 2.70 us                                                     | 2.89 us: 1.07x slower                                           |
| pickle               | 6.64 us                                                     | 7.31 us: 1.10x slower                                           |
| unpickle             | 7.57 us                                                     | 8.42 us: 1.11x slower                                           |
| Geometric mean       | (ref)                                                       | 1.04x faster                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf1-amd64-python-v3.13.0a3-3.13.0a3-f009305 |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| python_startup         | 19.8 ms                                                     | 20.1 ms: 1.02x slower                                           |
| python_startup_no_site | 16.8 ms                                                     | 17.9 ms: 1.06x slower                                           |
| Geometric mean         | (ref)                                                       | 1.04x slower                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf1-amd64-python-v3.13.0a3-3.13.0a3-f009305 |
|-----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| mako            | 7.58 ms                                                     | 6.57 ms: 1.15x faster                                           |
| genshi_text     | 18.4 ms                                                     | 16.1 ms: 1.15x faster                                           |
| django_template | 24.4 ms                                                     | 21.4 ms: 1.14x faster                                           |
| genshi_xml      | 39.9 ms                                                     | 36.0 ms: 1.11x faster                                           |
| Geometric mean  | (ref)                                                       | 1.14x faster                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240117-pythonperf1-amd64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 70.5 us: 4.62x faster                                           |
| pylint                     | 323 ms                                                      | 205 ms: 1.58x faster                                            |
| asyncio_tcp                | 726 ms                                                      | 462 ms: 1.57x faster                                            |
| generators                 | 34.0 ms                                                     | 22.1 ms: 1.53x faster                                           |
| comprehensions             | 15.6 us                                                     | 10.3 us: 1.52x faster                                           |
| json_dumps                 | 8.09 ms                                                     | 5.54 ms: 1.46x faster                                           |
| deltablue                  | 2.70 ms                                                     | 1.97 ms: 1.37x faster                                           |
| raytrace                   | 213 ms                                                      | 161 ms: 1.33x faster                                            |
| logging_silent             | 71.8 ns                                                     | 54.1 ns: 1.33x faster                                           |
| async_tree_none            | 332 ms                                                      | 263 ms: 1.26x faster                                            |
| richards_super             | 38.7 ms                                                     | 30.8 ms: 1.26x faster                                           |
| sqlglot_parse              | 953 us                                                      | 761 us: 1.25x faster                                            |
| chaos                      | 48.4 ms                                                     | 39.5 ms: 1.22x faster                                           |
| unpickle_pure_python       | 157 us                                                      | 128 us: 1.22x faster                                            |
| sympy_sum                  | 100 ms                                                      | 82.6 ms: 1.21x faster                                           |
| hexiom                     | 4.55 ms                                                     | 3.82 ms: 1.19x faster                                           |
| go                         | 101 ms                                                      | 84.9 ms: 1.19x faster                                           |
| sqlglot_transpile          | 1.16 ms                                                     | 981 us: 1.19x faster                                            |
| sympy_str                  | 185 ms                                                      | 156 ms: 1.19x faster                                            |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 448 ms: 1.18x faster                                            |
| deepcopy_memo              | 26.0 us                                                     | 22.2 us: 1.17x faster                                           |
| async_tree_memoization     | 399 ms                                                      | 341 ms: 1.17x faster                                            |
| regex_compile              | 91.0 ms                                                     | 77.7 ms: 1.17x faster                                           |
| pickle_pure_python         | 208 us                                                      | 179 us: 1.17x faster                                            |
| async_tree_memoization_tg  | 405 ms                                                      | 349 ms: 1.16x faster                                            |
| mako                       | 7.58 ms                                                     | 6.57 ms: 1.15x faster                                           |
| nqueens                    | 68.3 ms                                                     | 59.3 ms: 1.15x faster                                           |
| coroutines                 | 15.0 ms                                                     | 13.0 ms: 1.15x faster                                           |
| genshi_text                | 18.4 ms                                                     | 16.1 ms: 1.15x faster                                           |
| richards                   | 31.4 ms                                                     | 27.4 ms: 1.15x faster                                           |
| sympy_integrate            | 14.0 ms                                                     | 12.3 ms: 1.15x faster                                           |
| scimark_lu                 | 62.8 ms                                                     | 54.9 ms: 1.15x faster                                           |
| django_template            | 24.4 ms                                                     | 21.4 ms: 1.14x faster                                           |
| async_tree_none_tg         | 309 ms                                                      | 270 ms: 1.14x faster                                            |
| crypto_pyaes               | 48.9 ms                                                     | 42.8 ms: 1.14x faster                                           |
| mdp                        | 1.59 sec                                                    | 1.40 sec: 1.14x faster                                          |
| logging_simple             | 6.86 us                                                     | 6.04 us: 1.14x faster                                           |
| scimark_monte_carlo        | 45.3 ms                                                     | 39.9 ms: 1.14x faster                                           |
| sqlite_synth               | 1.77 us                                                     | 1.57 us: 1.13x faster                                           |
| dulwich_log                | 46.4 ms                                                     | 41.1 ms: 1.13x faster                                           |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 465 ms: 1.12x faster                                            |
| mypy2                      | 459 ms                                                      | 409 ms: 1.12x faster                                            |
| sympy_expand               | 299 ms                                                      | 268 ms: 1.12x faster                                            |
| async_tree_io              | 808 ms                                                      | 724 ms: 1.12x faster                                            |
| genshi_xml                 | 39.9 ms                                                     | 36.0 ms: 1.11x faster                                           |
| spectral_norm              | 68.3 ms                                                     | 61.6 ms: 1.11x faster                                           |
| logging_format             | 7.16 us                                                     | 6.47 us: 1.11x faster                                           |
| deepcopy                   | 246 us                                                      | 223 us: 1.11x faster                                            |
| async_tree_io_tg           | 829 ms                                                      | 750 ms: 1.11x faster                                            |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.83 sec: 1.10x faster                                          |
| tornado_http               | 92.8 ms                                                     | 85.5 ms: 1.09x faster                                           |
| sqlglot_normalize          | 190 ms                                                      | 175 ms: 1.08x faster                                            |
| pyflate                    | 312 ms                                                      | 288 ms: 1.08x faster                                            |
| pprint_pformat             | 1.09 sec                                                    | 1.00 sec: 1.08x faster                                          |
| html5lib                   | 38.9 ms                                                     | 35.9 ms: 1.08x faster                                           |
| pprint_safe_repr           | 529 ms                                                      | 491 ms: 1.08x faster                                            |
| chameleon                  | 5.26 ms                                                     | 4.91 ms: 1.07x faster                                           |
| docutils                   | 1.64 sec                                                    | 1.53 sec: 1.07x faster                                          |
| deepcopy_reduce            | 2.06 us                                                     | 1.93 us: 1.07x faster                                           |
| xml_etree_parse            | 97.6 ms                                                     | 93.0 ms: 1.05x faster                                           |
| sqlglot_optimize           | 34.5 ms                                                     | 33.0 ms: 1.05x faster                                           |
| meteor_contest             | 75.2 ms                                                     | 71.9 ms: 1.05x faster                                           |
| tomli_loads                | 1.46 sec                                                    | 1.39 sec: 1.04x faster                                          |
| bench_thread_pool          | 872 us                                                      | 839 us: 1.04x faster                                            |
| float                      | 54.4 ms                                                     | 52.5 ms: 1.04x faster                                           |
| fannkuch                   | 253 ms                                                      | 245 ms: 1.03x faster                                            |
| xml_etree_iterparse        | 65.6 ms                                                     | 63.5 ms: 1.03x faster                                           |
| xml_etree_process          | 37.2 ms                                                     | 36.4 ms: 1.02x faster                                           |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.52 ms: 1.02x faster                                           |
| pidigits                   | 150 ms                                                      | 148 ms: 1.02x faster                                            |
| pickle_dict                | 18.5 us                                                     | 18.2 us: 1.02x faster                                           |
| 2to3                       | 214 ms                                                      | 210 ms: 1.02x faster                                            |
| scimark_fft                | 179 ms                                                      | 178 ms: 1.01x faster                                            |
| flaskblogging              | 2.03 sec                                                    | 2.03 sec: 1.00x slower                                          |
| aiohttp                    | 883 us                                                      | 896 us: 1.01x slower                                            |
| python_startup             | 19.8 ms                                                     | 20.1 ms: 1.02x slower                                           |
| gc_traversal               | 1.49 ms                                                     | 1.52 ms: 1.02x slower                                           |
| coverage                   | 43.4 ms                                                     | 44.3 ms: 1.02x slower                                           |
| xml_etree_generate         | 52.5 ms                                                     | 53.6 ms: 1.02x slower                                           |
| create_gc_cycles           | 713 us                                                      | 732 us: 1.03x slower                                            |
| regex_dna                  | 116 ms                                                      | 121 ms: 1.04x slower                                            |
| json_loads                 | 13.0 us                                                     | 13.7 us: 1.05x slower                                           |
| bench_mp_pool              | 63.2 ms                                                     | 66.6 ms: 1.05x slower                                           |
| unpickle_list              | 2.59 us                                                     | 2.73 us: 1.05x slower                                           |
| nbody                      | 70.3 ms                                                     | 74.1 ms: 1.05x slower                                           |
| regex_effbot               | 1.50 ms                                                     | 1.59 ms: 1.06x slower                                           |
| python_startup_no_site     | 16.8 ms                                                     | 17.9 ms: 1.06x slower                                           |
| pickle_list                | 2.70 us                                                     | 2.89 us: 1.07x slower                                           |
| regex_v8                   | 14.2 ms                                                     | 15.3 ms: 1.08x slower                                           |
| pickle                     | 6.64 us                                                     | 7.31 us: 1.10x slower                                           |
| unpickle                   | 7.57 us                                                     | 8.42 us: 1.11x slower                                           |
| pathlib                    | 70.9 ms                                                     | 79.3 ms: 1.12x slower                                           |
| telco                      | 4.06 ms                                                     | 4.77 ms: 1.17x slower                                           |
| async_generators           | 177 ms                                                      | 227 ms: 1.28x slower                                            |
| thrift                     | 494 us                                                      | 8.32 ms: 16.84x slower                                          |
| Geometric mean             | (ref)                                                       | 1.08x faster                                                    |

Benchmark hidden because not significant (3): json, pycparser, scimark_sor
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: unknown