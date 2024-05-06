# Results vs. 3.11.0

- fork: python
- ref: 62aeb0ee69b060913963
- machine: windows-amd64
- commit hash: 62aeb0e
- commit date: 2024-04-06
- overall geometric mean: 1.09x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| chameleon      | 5.26 ms                                                     | 4.93 ms: 1.07x faster                                                       |
| html5lib       | 38.9 ms                                                     | 37.3 ms: 1.04x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 83.5 ms: 1.11x faster                                                       |
| Geometric mean | (ref)                                                       | 1.04x faster                                                                |

Benchmark hidden because not significant (2): 2to3, docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 270 ms: 1.50x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 272 ms: 1.47x faster                                                        |
| async_tree_none            | 332 ms                                                      | 227 ms: 1.46x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 218 ms: 1.41x faster                                                        |
| async_tree_io              | 808 ms                                                      | 582 ms: 1.39x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 384 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 393 ms: 1.35x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 626 ms: 1.32x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.41x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 54.4 ms                                                     | 51.7 ms: 1.05x faster                                                       |
| pidigits       | 150 ms                                                      | 147 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                       | 1.03x faster                                                                |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 91.0 ms                                                     | 78.5 ms: 1.16x faster                                                       |
| regex_dna      | 116 ms                                                      | 118 ms: 1.02x slower                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.58 ms: 1.05x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 16.4 ms: 1.15x slower                                                       |
| Geometric mean | (ref)                                                       | 1.02x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.73 ms: 1.41x faster                                                       |
| unpickle_pure_python | 157 us                                                      | 134 us: 1.17x faster                                                        |
| pickle_pure_python   | 208 us                                                      | 179 us: 1.16x faster                                                        |
| xml_etree_parse      | 97.6 ms                                                     | 93.2 ms: 1.05x faster                                                       |
| xml_etree_iterparse  | 65.6 ms                                                     | 63.4 ms: 1.03x faster                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.45 sec: 1.01x faster                                                      |
| pickle_dict          | 18.5 us                                                     | 18.7 us: 1.01x slower                                                       |
| xml_etree_process    | 37.2 ms                                                     | 37.9 ms: 1.02x slower                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 55.5 ms: 1.06x slower                                                       |
| json_loads           | 13.0 us                                                     | 13.9 us: 1.07x slower                                                       |
| pickle               | 6.64 us                                                     | 7.21 us: 1.09x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.83 us: 1.10x slower                                                       |
| pickle_list          | 2.70 us                                                     | 2.97 us: 1.10x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.58 us: 1.13x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.01x faster                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 16.8 ms                                                     | 18.4 ms: 1.10x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.05x slower                                                                |

Benchmark hidden because not significant (1): python_startup

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako           | 7.58 ms                                                     | 6.38 ms: 1.19x faster                                                       |
| genshi_xml     | 39.9 ms                                                     | 36.1 ms: 1.11x faster                                                       |
| genshi_text    | 18.4 ms                                                     | 16.8 ms: 1.10x faster                                                       |
| Geometric mean | (ref)                                                       | 1.13x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 71.4 us: 4.56x faster                                                       |
| pylint                     | 323 ms                                                      | 187 ms: 1.73x faster                                                        |
| generators                 | 34.0 ms                                                     | 20.9 ms: 1.63x faster                                                       |
| asyncio_tcp                | 726 ms                                                      | 483 ms: 1.50x faster                                                        |
| async_tree_memoization_tg  | 405 ms                                                      | 270 ms: 1.50x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 272 ms: 1.47x faster                                                        |
| async_tree_none            | 332 ms                                                      | 227 ms: 1.46x faster                                                        |
| comprehensions             | 15.6 us                                                     | 10.9 us: 1.43x faster                                                       |
| json_dumps                 | 8.09 ms                                                     | 5.73 ms: 1.41x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 218 ms: 1.41x faster                                                        |
| async_tree_io              | 808 ms                                                      | 582 ms: 1.39x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 384 ms: 1.36x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 393 ms: 1.35x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 626 ms: 1.32x faster                                                        |
| deltablue                  | 2.70 ms                                                     | 2.07 ms: 1.30x faster                                                       |
| raytrace                   | 213 ms                                                      | 164 ms: 1.30x faster                                                        |
| logging_silent             | 71.8 ns                                                     | 56.1 ns: 1.28x faster                                                       |
| chaos                      | 48.4 ms                                                     | 38.5 ms: 1.26x faster                                                       |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.64 sec: 1.23x faster                                                      |
| sqlglot_parse              | 953 us                                                      | 776 us: 1.23x faster                                                        |
| richards_super             | 38.7 ms                                                     | 32.0 ms: 1.21x faster                                                       |
| hexiom                     | 4.55 ms                                                     | 3.79 ms: 1.20x faster                                                       |
| deepcopy_memo              | 26.0 us                                                     | 21.6 us: 1.20x faster                                                       |
| mako                       | 7.58 ms                                                     | 6.38 ms: 1.19x faster                                                       |
| sqlglot_transpile          | 1.16 ms                                                     | 988 us: 1.18x faster                                                        |
| unpickle_pure_python       | 157 us                                                      | 134 us: 1.17x faster                                                        |
| sympy_sum                  | 100 ms                                                      | 85.8 ms: 1.17x faster                                                       |
| pickle_pure_python         | 208 us                                                      | 179 us: 1.16x faster                                                        |
| nqueens                    | 68.3 ms                                                     | 58.8 ms: 1.16x faster                                                       |
| scimark_lu                 | 62.8 ms                                                     | 54.1 ms: 1.16x faster                                                       |
| regex_compile              | 91.0 ms                                                     | 78.5 ms: 1.16x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 40.1 ms: 1.16x faster                                                       |
| logging_simple             | 6.86 us                                                     | 6.01 us: 1.14x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.41 sec: 1.13x faster                                                      |
| scimark_monte_carlo        | 45.3 ms                                                     | 40.3 ms: 1.13x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 13.3 ms: 1.13x faster                                                       |
| sympy_str                  | 185 ms                                                      | 165 ms: 1.12x faster                                                        |
| sympy_integrate            | 14.0 ms                                                     | 12.6 ms: 1.12x faster                                                       |
| deepcopy                   | 246 us                                                      | 221 us: 1.12x faster                                                        |
| go                         | 101 ms                                                      | 90.9 ms: 1.11x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 83.5 ms: 1.11x faster                                                       |
| logging_format             | 7.16 us                                                     | 6.45 us: 1.11x faster                                                       |
| genshi_xml                 | 39.9 ms                                                     | 36.1 ms: 1.11x faster                                                       |
| genshi_text                | 18.4 ms                                                     | 16.8 ms: 1.10x faster                                                       |
| pprint_pformat             | 1.09 sec                                                    | 989 ms: 1.10x faster                                                        |
| sqlite_synth               | 1.77 us                                                     | 1.61 us: 1.10x faster                                                       |
| pyflate                    | 312 ms                                                      | 286 ms: 1.09x faster                                                        |
| spectral_norm              | 68.3 ms                                                     | 63.0 ms: 1.09x faster                                                       |
| pprint_safe_repr           | 529 ms                                                      | 488 ms: 1.08x faster                                                        |
| bench_thread_pool          | 872 us                                                      | 809 us: 1.08x faster                                                        |
| mypy2                      | 459 ms                                                      | 426 ms: 1.08x faster                                                        |
| scimark_sor                | 78.1 ms                                                     | 72.5 ms: 1.08x faster                                                       |
| crypto_pyaes               | 48.9 ms                                                     | 45.5 ms: 1.07x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 4.93 ms: 1.07x faster                                                       |
| pycparser                  | 720 ms                                                      | 677 ms: 1.06x faster                                                        |
| sympy_expand               | 299 ms                                                      | 282 ms: 1.06x faster                                                        |
| richards                   | 31.4 ms                                                     | 29.8 ms: 1.05x faster                                                       |
| float                      | 54.4 ms                                                     | 51.7 ms: 1.05x faster                                                       |
| xml_etree_parse            | 97.6 ms                                                     | 93.2 ms: 1.05x faster                                                       |
| html5lib                   | 38.9 ms                                                     | 37.3 ms: 1.04x faster                                                       |
| sqlglot_normalize          | 190 ms                                                      | 183 ms: 1.04x faster                                                        |
| xml_etree_iterparse        | 65.6 ms                                                     | 63.4 ms: 1.03x faster                                                       |
| deepcopy_reduce            | 2.06 us                                                     | 1.99 us: 1.03x faster                                                       |
| scimark_fft                | 179 ms                                                      | 176 ms: 1.02x faster                                                        |
| meteor_contest             | 75.2 ms                                                     | 73.9 ms: 1.02x faster                                                       |
| pidigits                   | 150 ms                                                      | 147 ms: 1.02x faster                                                        |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 2.54 ms: 1.01x faster                                                       |
| fannkuch                   | 253 ms                                                      | 250 ms: 1.01x faster                                                        |
| tomli_loads                | 1.46 sec                                                    | 1.45 sec: 1.01x faster                                                      |
| pickle_dict                | 18.5 us                                                     | 18.7 us: 1.01x slower                                                       |
| bench_mp_pool              | 63.2 ms                                                     | 64.3 ms: 1.02x slower                                                       |
| xml_etree_process          | 37.2 ms                                                     | 37.9 ms: 1.02x slower                                                       |
| regex_dna                  | 116 ms                                                      | 118 ms: 1.02x slower                                                        |
| gc_traversal               | 1.49 ms                                                     | 1.55 ms: 1.04x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.58 ms: 1.05x slower                                                       |
| coverage                   | 43.4 ms                                                     | 45.7 ms: 1.05x slower                                                       |
| xml_etree_generate         | 52.5 ms                                                     | 55.5 ms: 1.06x slower                                                       |
| json_loads                 | 13.0 us                                                     | 13.9 us: 1.07x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.21 us: 1.09x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.83 us: 1.10x slower                                                       |
| python_startup_no_site     | 16.8 ms                                                     | 18.4 ms: 1.10x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 77.8 ms: 1.10x slower                                                       |
| pickle_list                | 2.70 us                                                     | 2.97 us: 1.10x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.58 us: 1.13x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 16.4 ms: 1.15x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 884 us: 1.24x slower                                                        |
| telco                      | 4.06 ms                                                     | 5.04 ms: 1.24x slower                                                       |
| async_generators           | 177 ms                                                      | 231 ms: 1.31x slower                                                        |
| thrift                     | 494 us                                                      | 8.04 ms: 16.27x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.09x faster                                                                |

Benchmark hidden because not significant (7): json, nbody, docutils, 2to3, sqlglot_optimize, python_startup, aiohttp
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: unknown