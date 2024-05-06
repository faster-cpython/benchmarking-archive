# Results vs. 3.11.0

- fork: python
- ref: 62aeb0ee69b060913963
- machine: windows-amd64
- commit hash: 62aeb0e
- commit date: 2024-04-06
- overall geometric mean: 1.10x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 221 ms: 1.03x slower                                                        |
| chameleon      | 5.26 ms                                                     | 4.70 ms: 1.12x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.70 sec: 1.04x slower                                                      |
| html5lib       | 38.9 ms                                                     | 35.4 ms: 1.10x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 83.6 ms: 1.11x faster                                                       |
| Geometric mean | (ref)                                                       | 1.05x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 262 ms: 1.54x faster                                                        |
| async_tree_none            | 332 ms                                                      | 217 ms: 1.53x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 265 ms: 1.51x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 212 ms: 1.46x faster                                                        |
| async_tree_io              | 808 ms                                                      | 582 ms: 1.39x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 605 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 387 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.36x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.44x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| nbody          | 70.3 ms                                                     | 57.8 ms: 1.22x faster                                                       |
| float          | 54.4 ms                                                     | 46.8 ms: 1.16x faster                                                       |
| pidigits       | 150 ms                                                      | 146 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                       | 1.13x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 87.0 ms: 1.05x faster                                                       |
| regex_dna      | 116 ms                                                      | 119 ms: 1.02x slower                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.55 ms: 1.04x slower                                                       |
| Geometric mean | (ref)                                                       | 1.00x slower                                                                |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.54 ms: 1.46x faster                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.19 sec: 1.23x faster                                                      |
| unpickle_pure_python | 157 us                                                      | 129 us: 1.22x faster                                                        |
| pickle_pure_python   | 208 us                                                      | 172 us: 1.22x faster                                                        |
| xml_etree_iterparse  | 65.6 ms                                                     | 60.6 ms: 1.08x faster                                                       |
| xml_etree_parse      | 97.6 ms                                                     | 90.9 ms: 1.07x faster                                                       |
| xml_etree_process    | 37.2 ms                                                     | 36.6 ms: 1.02x faster                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 53.1 ms: 1.01x slower                                                       |
| pickle_dict          | 18.5 us                                                     | 19.0 us: 1.03x slower                                                       |
| json_loads           | 13.0 us                                                     | 13.7 us: 1.05x slower                                                       |
| pickle_list          | 2.70 us                                                     | 2.85 us: 1.06x slower                                                       |
| pickle               | 6.64 us                                                     | 7.39 us: 1.11x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.90 us: 1.12x slower                                                       |
| unpickle             | 7.57 us                                                     | 9.09 us: 1.20x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.04x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.8 ms                                                     | 22.2 ms: 1.12x slower                                                       |
| python_startup_no_site | 16.8 ms                                                     | 20.2 ms: 1.20x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.16x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 7.58 ms                                                     | 5.63 ms: 1.35x faster                                                       |
| genshi_text    | 18.4 ms                                                     | 15.6 ms: 1.18x faster                                                       |
| genshi_xml     | 39.9 ms                                                     | 34.8 ms: 1.15x faster                                                       |
| Geometric mean | (ref)                                                       | 1.22x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 72.5 us: 4.50x faster                                                       |
| generators                 | 34.0 ms                                                     | 19.6 ms: 1.73x faster                                                       |
| pylint                     | 323 ms                                                      | 194 ms: 1.67x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 262 ms: 1.54x faster                                                        |
| async_tree_none            | 332 ms                                                      | 217 ms: 1.53x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 265 ms: 1.51x faster                                                        |
| asyncio_tcp                | 726 ms                                                      | 482 ms: 1.51x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.54 ms: 1.46x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 212 ms: 1.46x faster                                                        |
| comprehensions             | 15.6 us                                                     | 10.9 us: 1.44x faster                                                       |
| async_tree_io              | 808 ms                                                      | 582 ms: 1.39x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 605 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 387 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.36x faster                                                        |
| spectral_norm              | 68.3 ms                                                     | 50.4 ms: 1.36x faster                                                       |
| mako                       | 7.58 ms                                                     | 5.63 ms: 1.35x faster                                                       |
| logging_silent             | 71.8 ns                                                     | 53.6 ns: 1.34x faster                                                       |
| raytrace                   | 213 ms                                                      | 164 ms: 1.30x faster                                                        |
| richards_super             | 38.7 ms                                                     | 30.1 ms: 1.29x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.58 sec: 1.28x faster                                                      |
| deltablue                  | 2.70 ms                                                     | 2.15 ms: 1.26x faster                                                       |
| chaos                      | 48.4 ms                                                     | 38.5 ms: 1.26x faster                                                       |
| deepcopy_memo              | 26.0 us                                                     | 21.0 us: 1.23x faster                                                       |
| tomli_loads                | 1.46 sec                                                    | 1.19 sec: 1.23x faster                                                      |
| unpickle_pure_python       | 157 us                                                      | 129 us: 1.22x faster                                                        |
| nbody                      | 70.3 ms                                                     | 57.8 ms: 1.22x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 172 us: 1.22x faster                                                        |
| sqlglot_parse              | 953 us                                                      | 785 us: 1.21x faster                                                        |
| logging_simple             | 6.86 us                                                     | 5.72 us: 1.20x faster                                                       |
| richards                   | 31.4 ms                                                     | 26.5 ms: 1.18x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 15.6 ms: 1.18x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 994 us: 1.17x faster                                                        |
| logging_format             | 7.16 us                                                     | 6.11 us: 1.17x faster                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 38.7 ms: 1.17x faster                                                       |
| pyflate                    | 312 ms                                                      | 268 ms: 1.16x faster                                                        |
| float                      | 54.4 ms                                                     | 46.8 ms: 1.16x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 13.0 ms: 1.15x faster                                                       |
| genshi_xml                 | 39.9 ms                                                     | 34.8 ms: 1.15x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 40.4 ms: 1.15x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 88.0 ms: 1.14x faster                                                       |
| deepcopy                   | 246 us                                                      | 219 us: 1.12x faster                                                        |
| crypto_pyaes               | 48.9 ms                                                     | 43.6 ms: 1.12x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 4.70 ms: 1.12x faster                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.30 ms: 1.12x faster                                                       |
| nqueens                    | 68.3 ms                                                     | 61.5 ms: 1.11x faster                                                       |
| pprint_pformat             | 1.09 sec                                                    | 979 ms: 1.11x faster                                                        |
| tornado_http               | 92.8 ms                                                     | 83.6 ms: 1.11x faster                                                       |
| sqlite_synth               | 1.77 us                                                     | 1.59 us: 1.11x faster                                                       |
| sympy_str                  | 185 ms                                                      | 168 ms: 1.10x faster                                                        |
| pprint_safe_repr           | 529 ms                                                      | 481 ms: 1.10x faster                                                        |
| go                         | 101 ms                                                      | 92.0 ms: 1.10x faster                                                       |
| html5lib                   | 38.9 ms                                                     | 35.4 ms: 1.10x faster                                                       |
| bench_thread_pool          | 872 us                                                      | 795 us: 1.10x faster                                                        |
| fannkuch                   | 253 ms                                                      | 231 ms: 1.10x faster                                                        |
| mdp                        | 1.59 sec                                                    | 1.47 sec: 1.08x faster                                                      |
| xml_etree_iterparse        | 65.6 ms                                                     | 60.6 ms: 1.08x faster                                                       |
| xml_etree_parse            | 97.6 ms                                                     | 90.9 ms: 1.07x faster                                                       |
| scimark_fft                | 179 ms                                                      | 169 ms: 1.06x faster                                                        |
| sqlglot_normalize          | 190 ms                                                      | 180 ms: 1.06x faster                                                        |
| deepcopy_reduce            | 2.06 us                                                     | 1.95 us: 1.05x faster                                                       |
| sympy_integrate            | 14.0 ms                                                     | 13.3 ms: 1.05x faster                                                       |
| sympy_expand               | 299 ms                                                      | 285 ms: 1.05x faster                                                        |
| pycparser                  | 720 ms                                                      | 687 ms: 1.05x faster                                                        |
| regex_compile              | 91.0 ms                                                     | 87.0 ms: 1.05x faster                                                       |
| meteor_contest             | 75.2 ms                                                     | 72.5 ms: 1.04x faster                                                       |
| pidigits                   | 150 ms                                                      | 146 ms: 1.02x faster                                                        |
| mypy2                      | 459 ms                                                      | 449 ms: 1.02x faster                                                        |
| hexiom                     | 4.55 ms                                                     | 4.45 ms: 1.02x faster                                                       |
| xml_etree_process          | 37.2 ms                                                     | 36.6 ms: 1.02x faster                                                       |
| xml_etree_generate         | 52.5 ms                                                     | 53.1 ms: 1.01x slower                                                       |
| sqlglot_optimize           | 34.5 ms                                                     | 35.0 ms: 1.01x slower                                                       |
| aiohttp                    | 883 us                                                      | 900 us: 1.02x slower                                                        |
| regex_dna                  | 116 ms                                                      | 119 ms: 1.02x slower                                                        |
| pickle_dict                | 18.5 us                                                     | 19.0 us: 1.03x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.54 ms: 1.03x slower                                                       |
| 2to3                       | 214 ms                                                      | 221 ms: 1.03x slower                                                        |
| docutils                   | 1.64 sec                                                    | 1.70 sec: 1.04x slower                                                      |
| regex_effbot               | 1.50 ms                                                     | 1.55 ms: 1.04x slower                                                       |
| json_loads                 | 13.0 us                                                     | 13.7 us: 1.05x slower                                                       |
| pickle_list                | 2.70 us                                                     | 2.85 us: 1.06x slower                                                       |
| scimark_sor                | 78.1 ms                                                     | 83.4 ms: 1.07x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 76.8 ms: 1.08x slower                                                       |
| coverage                   | 43.4 ms                                                     | 47.2 ms: 1.09x slower                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 69.9 ms: 1.11x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.39 us: 1.11x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.90 us: 1.12x slower                                                       |
| python_startup             | 19.8 ms                                                     | 22.2 ms: 1.12x slower                                                       |
| scimark_lu                 | 62.8 ms                                                     | 73.2 ms: 1.17x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.74 ms: 1.17x slower                                                       |
| unpickle                   | 7.57 us                                                     | 9.09 us: 1.20x slower                                                       |
| python_startup_no_site     | 16.8 ms                                                     | 20.2 ms: 1.20x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 900 us: 1.26x slower                                                        |
| async_generators           | 177 ms                                                      | 235 ms: 1.33x slower                                                        |
| thrift                     | 494 us                                                      | 8.54 ms: 17.30x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.10x faster                                                                |

Benchmark hidden because not significant (2): json, regex_v8
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.08x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: unknown