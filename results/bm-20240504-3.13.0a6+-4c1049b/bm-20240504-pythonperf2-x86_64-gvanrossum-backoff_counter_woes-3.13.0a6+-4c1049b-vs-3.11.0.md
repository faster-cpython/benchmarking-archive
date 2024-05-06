# Results vs. 3.11.0

- fork: gvanrossum
- ref: backoff_counter_woes
- machine: linux-x86_64
- commit hash: 4c1049b
- commit date: 2024-05-04
- overall geometric mean: 1.07x faster
- HPT reliability: 99.46%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf2-x86_64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 288 ms: 1.00x slower                                                             |
| chameleon      | 7.92 ms                                                      | 7.86 ms: 1.01x faster                                                            |
| docutils       | 2.85 sec                                                     | 3.02 sec: 1.06x slower                                                           |
| html5lib       | 72.2 ms                                                      | 74.9 ms: 1.04x slower                                                            |
| tornado_http   | 124 ms                                                       | 120 ms: 1.04x faster                                                             |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf2-x86_64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 518 ms                                                       | 371 ms: 1.40x faster                                                             |
| async_tree_memoization_tg  | 600 ms                                                       | 431 ms: 1.39x faster                                                             |
| async_tree_none_tg         | 474 ms                                                       | 342 ms: 1.39x faster                                                             |
| async_tree_memoization     | 629 ms                                                       | 465 ms: 1.35x faster                                                             |
| async_tree_io              | 1.17 sec                                                     | 868 ms: 1.35x faster                                                             |
| async_tree_io_tg           | 1.15 sec                                                     | 886 ms: 1.30x faster                                                             |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 585 ms: 1.28x faster                                                             |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 618 ms: 1.22x faster                                                             |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf2-x86_64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 89.9 ms: 1.03x faster                                                            |
| pidigits       | 251 ms                                                       | 257 ms: 1.02x slower                                                             |
| float          | 74.9 ms                                                      | 80.6 ms: 1.08x slower                                                            |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf2-x86_64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 148 ms: 1.06x faster                                                             |
| regex_effbot   | 3.34 ms                                                      | 3.42 ms: 1.02x slower                                                            |
| regex_dna      | 227 ms                                                       | 235 ms: 1.03x slower                                                             |
| regex_v8       | 24.4 ms                                                      | 26.3 ms: 1.08x slower                                                            |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf2-x86_64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 11.1 ms: 1.20x faster                                                            |
| json_loads           | 28.9 us                                                      | 24.8 us: 1.17x faster                                                            |
| unpickle_pure_python | 238 us                                                       | 215 us: 1.11x faster                                                             |
| xml_etree_parse      | 155 ms                                                       | 144 ms: 1.07x faster                                                             |
| pickle_dict          | 32.3 us                                                      | 30.9 us: 1.04x faster                                                            |
| xml_etree_iterparse  | 107 ms                                                       | 103 ms: 1.04x faster                                                             |
| pickle_pure_python   | 316 us                                                       | 317 us: 1.00x slower                                                             |
| pickle               | 9.89 us                                                      | 10.3 us: 1.04x slower                                                            |
| unpickle_list        | 4.60 us                                                      | 4.82 us: 1.05x slower                                                            |
| xml_etree_process    | 55.9 ms                                                      | 60.3 ms: 1.08x slower                                                            |
| xml_etree_generate   | 79.7 ms                                                      | 88.6 ms: 1.11x slower                                                            |
| unpickle             | 13.3 us                                                      | 14.8 us: 1.11x slower                                                            |
| tomli_loads          | 2.25 sec                                                     | 2.57 sec: 1.14x slower                                                           |
| pickle_list          | 3.94 us                                                      | 4.52 us: 1.15x slower                                                            |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf2-x86_64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 8.80 ms: 1.14x slower                                                            |
| python_startup         | 10.7 ms                                                      | 12.8 ms: 1.20x slower                                                            |
| Geometric mean         | (ref)                                                        | 1.17x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf2-x86_64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 11.0 ms                                                      | 10.5 ms: 1.05x faster                                                            |
| genshi_text    | 25.5 ms                                                      | 26.0 ms: 1.02x slower                                                            |
| Geometric mean | (ref)                                                        | 1.01x faster                                                                     |

Benchmark hidden because not significant (2): genshi_xml, django_template

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240504-pythonperf2-x86_64-gvanrossum-backoff_counter_woes-3.13.0a6+-4c1049b |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 179 us: 2.96x faster                                                             |
| asyncio_tcp                | 747 ms                                                       | 375 ms: 1.99x faster                                                             |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.95x faster                                                           |
| generators                 | 54.6 ms                                                      | 34.1 ms: 1.60x faster                                                            |
| pylint                     | 514 ms                                                       | 348 ms: 1.48x faster                                                             |
| comprehensions             | 25.1 us                                                      | 17.3 us: 1.45x faster                                                            |
| async_tree_none            | 518 ms                                                       | 371 ms: 1.40x faster                                                             |
| async_tree_memoization_tg  | 600 ms                                                       | 431 ms: 1.39x faster                                                             |
| async_tree_none_tg         | 474 ms                                                       | 342 ms: 1.39x faster                                                             |
| async_tree_memoization     | 629 ms                                                       | 465 ms: 1.35x faster                                                             |
| async_tree_io              | 1.17 sec                                                     | 868 ms: 1.35x faster                                                             |
| async_tree_io_tg           | 1.15 sec                                                     | 886 ms: 1.30x faster                                                             |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 585 ms: 1.28x faster                                                             |
| chaos                      | 74.9 ms                                                      | 58.8 ms: 1.28x faster                                                            |
| coroutines                 | 27.8 ms                                                      | 22.0 ms: 1.26x faster                                                            |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 618 ms: 1.22x faster                                                             |
| json_dumps                 | 13.3 ms                                                      | 11.1 ms: 1.20x faster                                                            |
| sympy_sum                  | 186 ms                                                       | 157 ms: 1.18x faster                                                             |
| deltablue                  | 3.97 ms                                                      | 3.35 ms: 1.18x faster                                                            |
| raytrace                   | 309 ms                                                       | 262 ms: 1.18x faster                                                             |
| scimark_lu                 | 114 ms                                                       | 97.1 ms: 1.17x faster                                                            |
| fannkuch                   | 416 ms                                                       | 357 ms: 1.17x faster                                                             |
| json_loads                 | 28.9 us                                                      | 24.8 us: 1.17x faster                                                            |
| nqueens                    | 103 ms                                                       | 88.6 ms: 1.16x faster                                                            |
| sympy_str                  | 337 ms                                                       | 301 ms: 1.12x faster                                                             |
| mdp                        | 2.77 sec                                                     | 2.49 sec: 1.11x faster                                                           |
| pathlib                    | 18.9 ms                                                      | 17.1 ms: 1.11x faster                                                            |
| hexiom                     | 6.98 ms                                                      | 6.29 ms: 1.11x faster                                                            |
| unpickle_pure_python       | 238 us                                                       | 215 us: 1.11x faster                                                             |
| crypto_pyaes               | 83.3 ms                                                      | 75.1 ms: 1.11x faster                                                            |
| logging_simple             | 7.24 us                                                      | 6.59 us: 1.10x faster                                                            |
| bench_thread_pool          | 1.00 ms                                                      | 912 us: 1.10x faster                                                             |
| sympy_integrate            | 25.8 ms                                                      | 23.6 ms: 1.10x faster                                                            |
| sympy_expand               | 553 ms                                                       | 513 ms: 1.08x faster                                                             |
| xml_etree_parse            | 155 ms                                                       | 144 ms: 1.07x faster                                                             |
| sqlglot_parse              | 1.51 ms                                                      | 1.41 ms: 1.07x faster                                                            |
| pycparser                  | 1.31 sec                                                     | 1.22 sec: 1.07x faster                                                           |
| logging_format             | 7.71 us                                                      | 7.21 us: 1.07x faster                                                            |
| scimark_monte_carlo        | 69.8 ms                                                      | 65.4 ms: 1.07x faster                                                            |
| sqlglot_transpile          | 1.91 ms                                                      | 1.79 ms: 1.06x faster                                                            |
| regex_compile              | 156 ms                                                       | 148 ms: 1.06x faster                                                             |
| thrift                     | 931 us                                                       | 886 us: 1.05x faster                                                             |
| mako                       | 11.0 ms                                                      | 10.5 ms: 1.05x faster                                                            |
| pickle_dict                | 32.3 us                                                      | 30.9 us: 1.04x faster                                                            |
| dask                       | 410 ms                                                       | 395 ms: 1.04x faster                                                             |
| tornado_http               | 124 ms                                                       | 120 ms: 1.04x faster                                                             |
| richards_super             | 63.6 ms                                                      | 61.4 ms: 1.04x faster                                                            |
| xml_etree_iterparse        | 107 ms                                                       | 103 ms: 1.04x faster                                                             |
| logging_silent             | 100 ns                                                       | 97.1 ns: 1.03x faster                                                            |
| nbody                      | 92.9 ms                                                      | 89.9 ms: 1.03x faster                                                            |
| bench_mp_pool              | 4.70 ms                                                      | 4.57 ms: 1.03x faster                                                            |
| deepcopy                   | 391 us                                                       | 384 us: 1.02x faster                                                             |
| json                       | 5.58 ms                                                      | 5.51 ms: 1.01x faster                                                            |
| dulwich_log                | 67.4 ms                                                      | 66.5 ms: 1.01x faster                                                            |
| chameleon                  | 7.92 ms                                                      | 7.86 ms: 1.01x faster                                                            |
| meteor_contest             | 131 ms                                                       | 130 ms: 1.00x faster                                                             |
| spectral_norm              | 95.1 ms                                                      | 94.7 ms: 1.00x faster                                                            |
| 2to3                       | 287 ms                                                       | 288 ms: 1.00x slower                                                             |
| pickle_pure_python         | 316 us                                                       | 317 us: 1.00x slower                                                             |
| pprint_safe_repr           | 805 ms                                                       | 813 ms: 1.01x slower                                                             |
| sqlglot_optimize           | 59.0 ms                                                      | 59.7 ms: 1.01x slower                                                            |
| deepcopy_reduce            | 3.40 us                                                      | 3.44 us: 1.01x slower                                                            |
| mypy2                      | 762 ms                                                       | 774 ms: 1.02x slower                                                             |
| genshi_text                | 25.5 ms                                                      | 26.0 ms: 1.02x slower                                                            |
| deepcopy_memo              | 37.5 us                                                      | 38.3 us: 1.02x slower                                                            |
| pidigits                   | 251 ms                                                       | 257 ms: 1.02x slower                                                             |
| regex_effbot               | 3.34 ms                                                      | 3.42 ms: 1.02x slower                                                            |
| scimark_sor                | 110 ms                                                       | 113 ms: 1.03x slower                                                             |
| regex_dna                  | 227 ms                                                       | 235 ms: 1.03x slower                                                             |
| html5lib                   | 72.2 ms                                                      | 74.9 ms: 1.04x slower                                                            |
| go                         | 158 ms                                                       | 163 ms: 1.04x slower                                                             |
| pickle                     | 9.89 us                                                      | 10.3 us: 1.04x slower                                                            |
| pyflate                    | 449 ms                                                       | 470 ms: 1.05x slower                                                             |
| unpickle_list              | 4.60 us                                                      | 4.82 us: 1.05x slower                                                            |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.30 ms: 1.06x slower                                                            |
| scimark_fft                | 281 ms                                                       | 297 ms: 1.06x slower                                                             |
| docutils                   | 2.85 sec                                                     | 3.02 sec: 1.06x slower                                                           |
| regex_v8                   | 24.4 ms                                                      | 26.3 ms: 1.08x slower                                                            |
| float                      | 74.9 ms                                                      | 80.6 ms: 1.08x slower                                                            |
| xml_etree_process          | 55.9 ms                                                      | 60.3 ms: 1.08x slower                                                            |
| gunicorn                   | 966 us                                                       | 1.05 ms: 1.09x slower                                                            |
| richards                   | 49.7 ms                                                      | 54.4 ms: 1.10x slower                                                            |
| sqlite_synth               | 2.52 us                                                      | 2.79 us: 1.11x slower                                                            |
| xml_etree_generate         | 79.7 ms                                                      | 88.6 ms: 1.11x slower                                                            |
| unpickle                   | 13.3 us                                                      | 14.8 us: 1.11x slower                                                            |
| aiohttp                    | 986 us                                                       | 1.10 ms: 1.11x slower                                                            |
| async_generators           | 322 ms                                                       | 360 ms: 1.12x slower                                                             |
| gc_traversal               | 4.15 ms                                                      | 4.67 ms: 1.13x slower                                                            |
| python_startup_no_site     | 7.73 ms                                                      | 8.80 ms: 1.14x slower                                                            |
| tomli_loads                | 2.25 sec                                                     | 2.57 sec: 1.14x slower                                                           |
| pickle_list                | 3.94 us                                                      | 4.52 us: 1.15x slower                                                            |
| flaskblogging              | 3.88 ms                                                      | 4.64 ms: 1.20x slower                                                            |
| python_startup             | 10.7 ms                                                      | 12.8 ms: 1.20x slower                                                            |
| telco                      | 6.81 ms                                                      | 8.30 ms: 1.22x slower                                                            |
| coverage                   | 66.1 ms                                                      | 83.2 ms: 1.26x slower                                                            |
| create_gc_cycles           | 1.58 ms                                                      | 2.02 ms: 1.28x slower                                                            |
| Geometric mean             | (ref)                                                        | 1.07x faster                                                                     |

Benchmark hidden because not significant (5): genshi_xml, pprint_pformat, django_template, sqlglot_normalize, asyncio_websockets
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.46% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x