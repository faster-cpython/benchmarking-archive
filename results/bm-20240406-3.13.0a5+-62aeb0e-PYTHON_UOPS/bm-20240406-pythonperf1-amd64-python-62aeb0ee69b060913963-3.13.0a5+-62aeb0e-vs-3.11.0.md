# Results vs. 3.11.0

- fork: python
- ref: 62aeb0ee69b060913963
- machine: windows-amd64
- commit hash: 62aeb0e
- commit date: 2024-04-06
- overall geometric mean: 1.01x faster
- HPT reliability: 69.68%
- HPT 99th percentile: 1.00x slower
- Memory change: unknown

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 214 ms                                                      | 226 ms: 1.06x slower                                                        |
| chameleon      | 5.26 ms                                                     | 5.06 ms: 1.04x faster                                                       |
| docutils       | 1.64 sec                                                    | 1.76 sec: 1.07x slower                                                      |
| html5lib       | 38.9 ms                                                     | 37.9 ms: 1.03x faster                                                       |
| tornado_http   | 92.8 ms                                                     | 86.2 ms: 1.08x faster                                                       |
| Geometric mean | (ref)                                                       | 1.00x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 405 ms                                                      | 272 ms: 1.49x faster                                                        |
| async_tree_none            | 332 ms                                                      | 230 ms: 1.44x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 277 ms: 1.44x faster                                                        |
| async_tree_none_tg         | 309 ms                                                      | 221 ms: 1.40x faster                                                        |
| async_tree_io              | 808 ms                                                      | 590 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 395 ms: 1.34x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 622 ms: 1.33x faster                                                        |
| Geometric mean             | (ref)                                                       | 1.40x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| pidigits       | 150 ms                                                      | 148 ms: 1.01x faster                                                        |
| float          | 54.4 ms                                                     | 60.0 ms: 1.10x slower                                                       |
| nbody          | 70.3 ms                                                     | 83.2 ms: 1.18x slower                                                       |
| Geometric mean | (ref)                                                       | 1.09x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_dna      | 116 ms                                                      | 121 ms: 1.04x slower                                                        |
| regex_effbot   | 1.50 ms                                                     | 1.58 ms: 1.06x slower                                                       |
| regex_v8       | 14.2 ms                                                     | 15.1 ms: 1.07x slower                                                       |
| regex_compile  | 91.0 ms                                                     | 107 ms: 1.18x slower                                                        |
| Geometric mean | (ref)                                                       | 1.08x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| json_dumps           | 8.09 ms                                                     | 5.77 ms: 1.40x faster                                                       |
| pickle_pure_python   | 208 us                                                      | 184 us: 1.14x faster                                                        |
| xml_etree_parse      | 97.6 ms                                                     | 91.1 ms: 1.07x faster                                                       |
| pickle_dict          | 18.5 us                                                     | 19.0 us: 1.03x slower                                                       |
| xml_etree_iterparse  | 65.6 ms                                                     | 67.8 ms: 1.03x slower                                                       |
| tomli_loads          | 1.46 sec                                                    | 1.52 sec: 1.05x slower                                                      |
| xml_etree_process    | 37.2 ms                                                     | 39.1 ms: 1.05x slower                                                       |
| json_loads           | 13.0 us                                                     | 13.8 us: 1.06x slower                                                       |
| xml_etree_generate   | 52.5 ms                                                     | 56.6 ms: 1.08x slower                                                       |
| unpickle_pure_python | 157 us                                                      | 169 us: 1.08x slower                                                        |
| pickle_list          | 2.70 us                                                     | 2.93 us: 1.09x slower                                                       |
| unpickle_list        | 2.59 us                                                     | 2.88 us: 1.11x slower                                                       |
| unpickle             | 7.57 us                                                     | 8.54 us: 1.13x slower                                                       |
| pickle               | 6.64 us                                                     | 7.50 us: 1.13x slower                                                       |
| Geometric mean       | (ref)                                                       | 1.02x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 19.8 ms                                                     | 20.1 ms: 1.01x slower                                                       |
| python_startup_no_site | 16.8 ms                                                     | 18.1 ms: 1.08x slower                                                       |
| Geometric mean         | (ref)                                                       | 1.05x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text    | 18.4 ms                                                     | 17.0 ms: 1.09x faster                                                       |
| genshi_xml     | 39.9 ms                                                     | 37.1 ms: 1.08x faster                                                       |
| mako           | 7.58 ms                                                     | 7.47 ms: 1.02x faster                                                       |
| Geometric mean | (ref)                                                       | 1.06x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-pythonperf1-amd64-python-62aeb0ee69b060913963-3.13.0a5+-62aeb0e |
|----------------------------|:-----------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 326 us                                                      | 78.3 us: 4.16x faster                                                       |
| pylint                     | 323 ms                                                      | 200 ms: 1.62x faster                                                        |
| asyncio_tcp                | 726 ms                                                      | 480 ms: 1.51x faster                                                        |
| generators                 | 34.0 ms                                                     | 22.8 ms: 1.49x faster                                                       |
| async_tree_memoization_tg  | 405 ms                                                      | 272 ms: 1.49x faster                                                        |
| async_tree_none            | 332 ms                                                      | 230 ms: 1.44x faster                                                        |
| async_tree_memoization     | 399 ms                                                      | 277 ms: 1.44x faster                                                        |
| json_dumps                 | 8.09 ms                                                     | 5.77 ms: 1.40x faster                                                       |
| async_tree_none_tg         | 309 ms                                                      | 221 ms: 1.40x faster                                                        |
| async_tree_io              | 808 ms                                                      | 590 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed_tg | 523 ms                                                      | 383 ms: 1.37x faster                                                        |
| async_tree_cpu_io_mixed    | 530 ms                                                      | 395 ms: 1.34x faster                                                        |
| async_tree_io_tg           | 829 ms                                                      | 622 ms: 1.33x faster                                                        |
| asyncio_tcp_ssl            | 2.03 sec                                                    | 1.55 sec: 1.31x faster                                                      |
| logging_silent             | 71.8 ns                                                     | 56.4 ns: 1.27x faster                                                       |
| raytrace                   | 213 ms                                                      | 177 ms: 1.20x faster                                                        |
| richards_super             | 38.7 ms                                                     | 33.0 ms: 1.17x faster                                                       |
| coroutines                 | 15.0 ms                                                     | 13.1 ms: 1.15x faster                                                       |
| sqlglot_parse              | 953 us                                                      | 838 us: 1.14x faster                                                        |
| pickle_pure_python         | 208 us                                                      | 184 us: 1.14x faster                                                        |
| sqlglot_transpile          | 1.16 ms                                                     | 1.05 ms: 1.11x faster                                                       |
| sqlite_synth               | 1.77 us                                                     | 1.62 us: 1.09x faster                                                       |
| mdp                        | 1.59 sec                                                    | 1.47 sec: 1.09x faster                                                      |
| genshi_text                | 18.4 ms                                                     | 17.0 ms: 1.09x faster                                                       |
| richards                   | 31.4 ms                                                     | 29.0 ms: 1.08x faster                                                       |
| tornado_http               | 92.8 ms                                                     | 86.2 ms: 1.08x faster                                                       |
| genshi_xml                 | 39.9 ms                                                     | 37.1 ms: 1.08x faster                                                       |
| comprehensions             | 15.6 us                                                     | 14.6 us: 1.07x faster                                                       |
| xml_etree_parse            | 97.6 ms                                                     | 91.1 ms: 1.07x faster                                                       |
| logging_simple             | 6.86 us                                                     | 6.42 us: 1.07x faster                                                       |
| deltablue                  | 2.70 ms                                                     | 2.54 ms: 1.06x faster                                                       |
| chaos                      | 48.4 ms                                                     | 45.9 ms: 1.05x faster                                                       |
| sympy_sum                  | 100 ms                                                      | 95.3 ms: 1.05x faster                                                       |
| deepcopy                   | 246 us                                                      | 235 us: 1.05x faster                                                        |
| bench_thread_pool          | 872 us                                                      | 835 us: 1.05x faster                                                        |
| logging_format             | 7.16 us                                                     | 6.87 us: 1.04x faster                                                       |
| chameleon                  | 5.26 ms                                                     | 5.06 ms: 1.04x faster                                                       |
| deepcopy_memo              | 26.0 us                                                     | 25.1 us: 1.03x faster                                                       |
| dulwich_log                | 46.4 ms                                                     | 45.0 ms: 1.03x faster                                                       |
| html5lib                   | 38.9 ms                                                     | 37.9 ms: 1.03x faster                                                       |
| mako                       | 7.58 ms                                                     | 7.47 ms: 1.02x faster                                                       |
| pidigits                   | 150 ms                                                      | 148 ms: 1.01x faster                                                        |
| sympy_str                  | 185 ms                                                      | 186 ms: 1.01x slower                                                        |
| sympy_integrate            | 14.0 ms                                                     | 14.1 ms: 1.01x slower                                                       |
| mypy2                      | 459 ms                                                      | 462 ms: 1.01x slower                                                        |
| deepcopy_reduce            | 2.06 us                                                     | 2.08 us: 1.01x slower                                                       |
| python_startup             | 19.8 ms                                                     | 20.1 ms: 1.01x slower                                                       |
| pickle_dict                | 18.5 us                                                     | 19.0 us: 1.03x slower                                                       |
| meteor_contest             | 75.2 ms                                                     | 77.1 ms: 1.03x slower                                                       |
| go                         | 101 ms                                                      | 104 ms: 1.03x slower                                                        |
| sqlglot_normalize          | 190 ms                                                      | 196 ms: 1.03x slower                                                        |
| xml_etree_iterparse        | 65.6 ms                                                     | 67.8 ms: 1.03x slower                                                       |
| gc_traversal               | 1.49 ms                                                     | 1.54 ms: 1.03x slower                                                       |
| pprint_pformat             | 1.09 sec                                                    | 1.13 sec: 1.04x slower                                                      |
| bench_mp_pool              | 63.2 ms                                                     | 65.7 ms: 1.04x slower                                                       |
| aiohttp                    | 883 us                                                      | 919 us: 1.04x slower                                                        |
| regex_dna                  | 116 ms                                                      | 121 ms: 1.04x slower                                                        |
| sympy_expand               | 299 ms                                                      | 312 ms: 1.04x slower                                                        |
| pprint_safe_repr           | 529 ms                                                      | 553 ms: 1.05x slower                                                        |
| tomli_loads                | 1.46 sec                                                    | 1.52 sec: 1.05x slower                                                      |
| xml_etree_process          | 37.2 ms                                                     | 39.1 ms: 1.05x slower                                                       |
| nqueens                    | 68.3 ms                                                     | 72.0 ms: 1.05x slower                                                       |
| regex_effbot               | 1.50 ms                                                     | 1.58 ms: 1.06x slower                                                       |
| 2to3                       | 214 ms                                                      | 226 ms: 1.06x slower                                                        |
| json_loads                 | 13.0 us                                                     | 13.8 us: 1.06x slower                                                       |
| coverage                   | 43.4 ms                                                     | 46.0 ms: 1.06x slower                                                       |
| regex_v8                   | 14.2 ms                                                     | 15.1 ms: 1.07x slower                                                       |
| crypto_pyaes               | 48.9 ms                                                     | 52.1 ms: 1.07x slower                                                       |
| docutils                   | 1.64 sec                                                    | 1.76 sec: 1.07x slower                                                      |
| python_startup_no_site     | 16.8 ms                                                     | 18.1 ms: 1.08x slower                                                       |
| xml_etree_generate         | 52.5 ms                                                     | 56.6 ms: 1.08x slower                                                       |
| unpickle_pure_python       | 157 us                                                      | 169 us: 1.08x slower                                                        |
| pickle_list                | 2.70 us                                                     | 2.93 us: 1.09x slower                                                       |
| pyflate                    | 312 ms                                                      | 341 ms: 1.09x slower                                                        |
| sqlglot_optimize           | 34.5 ms                                                     | 37.9 ms: 1.10x slower                                                       |
| pathlib                    | 70.9 ms                                                     | 78.0 ms: 1.10x slower                                                       |
| float                      | 54.4 ms                                                     | 60.0 ms: 1.10x slower                                                       |
| unpickle_list              | 2.59 us                                                     | 2.88 us: 1.11x slower                                                       |
| unpickle                   | 7.57 us                                                     | 8.54 us: 1.13x slower                                                       |
| pickle                     | 6.64 us                                                     | 7.50 us: 1.13x slower                                                       |
| scimark_monte_carlo        | 45.3 ms                                                     | 52.2 ms: 1.15x slower                                                       |
| fannkuch                   | 253 ms                                                      | 296 ms: 1.17x slower                                                        |
| regex_compile              | 91.0 ms                                                     | 107 ms: 1.18x slower                                                        |
| scimark_fft                | 179 ms                                                      | 212 ms: 1.18x slower                                                        |
| scimark_sor                | 78.1 ms                                                     | 92.4 ms: 1.18x slower                                                       |
| nbody                      | 70.3 ms                                                     | 83.2 ms: 1.18x slower                                                       |
| hexiom                     | 4.55 ms                                                     | 5.54 ms: 1.22x slower                                                       |
| telco                      | 4.06 ms                                                     | 4.96 ms: 1.22x slower                                                       |
| spectral_norm              | 68.3 ms                                                     | 86.6 ms: 1.27x slower                                                       |
| scimark_sparse_mat_mult    | 2.58 ms                                                     | 3.28 ms: 1.28x slower                                                       |
| create_gc_cycles           | 713 us                                                      | 915 us: 1.28x slower                                                        |
| scimark_lu                 | 62.8 ms                                                     | 81.2 ms: 1.29x slower                                                       |
| async_generators           | 177 ms                                                      | 244 ms: 1.38x slower                                                        |
| thrift                     | 494 us                                                      | 9.47 ms: 19.17x slower                                                      |
| Geometric mean             | (ref)                                                       | 1.01x faster                                                                |

Benchmark hidden because not significant (2): json, pycparser
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf1-amd64-python-v3.11.0-3.11.0-deaf509.json: dask, django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 69.68% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: unknown