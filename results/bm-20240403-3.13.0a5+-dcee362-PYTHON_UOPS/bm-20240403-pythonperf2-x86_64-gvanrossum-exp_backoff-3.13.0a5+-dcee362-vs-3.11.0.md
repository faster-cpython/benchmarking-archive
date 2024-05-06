# Results vs. 3.11.0

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: dcee362
- commit date: 2024-04-03
- overall geometric mean: 1.03x slower
- HPT reliability: 99.85%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 316 ms: 1.10x slower                                                    |
| chameleon      | 7.92 ms                                                      | 7.77 ms: 1.02x faster                                                   |
| docutils       | 2.85 sec                                                     | 3.24 sec: 1.14x slower                                                  |
| html5lib       | 72.2 ms                                                      | 79.7 ms: 1.10x slower                                                   |
| tornado_http   | 124 ms                                                       | 129 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                        | 1.07x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_memoization     | 629 ms                                                       | 463 ms: 1.36x faster                                                    |
| async_tree_memoization_tg  | 600 ms                                                       | 447 ms: 1.34x faster                                                    |
| async_tree_none_tg         | 474 ms                                                       | 354 ms: 1.34x faster                                                    |
| async_tree_none            | 518 ms                                                       | 395 ms: 1.31x faster                                                    |
| async_tree_io_tg           | 1.15 sec                                                     | 892 ms: 1.29x faster                                                    |
| async_tree_io              | 1.17 sec                                                     | 912 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 612 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 628 ms: 1.20x faster                                                    |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 266 ms: 1.06x slower                                                    |
| float          | 74.9 ms                                                      | 91.6 ms: 1.22x slower                                                   |
| nbody          | 92.9 ms                                                      | 114 ms: 1.23x slower                                                    |
| Geometric mean | (ref)                                                        | 1.17x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 227 ms                                                       | 236 ms: 1.04x slower                                                    |
| regex_v8       | 24.4 ms                                                      | 25.6 ms: 1.05x slower                                                   |
| regex_effbot   | 3.34 ms                                                      | 3.58 ms: 1.07x slower                                                   |
| regex_compile  | 156 ms                                                       | 196 ms: 1.25x slower                                                    |
| Geometric mean | (ref)                                                        | 1.10x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                   |
| json_loads           | 28.9 us                                                      | 25.3 us: 1.14x faster                                                   |
| xml_etree_parse      | 155 ms                                                       | 144 ms: 1.08x faster                                                    |
| pickle_dict          | 32.3 us                                                      | 31.2 us: 1.04x faster                                                   |
| xml_etree_iterparse  | 107 ms                                                       | 108 ms: 1.01x slower                                                    |
| pickle_pure_python   | 316 us                                                       | 326 us: 1.03x slower                                                    |
| unpickle_list        | 4.60 us                                                      | 4.77 us: 1.04x slower                                                   |
| pickle               | 9.89 us                                                      | 10.4 us: 1.05x slower                                                   |
| pickle_list          | 3.94 us                                                      | 4.38 us: 1.11x slower                                                   |
| unpickle             | 13.3 us                                                      | 14.8 us: 1.11x slower                                                   |
| xml_etree_process    | 55.9 ms                                                      | 62.5 ms: 1.12x slower                                                   |
| xml_etree_generate   | 79.7 ms                                                      | 90.3 ms: 1.13x slower                                                   |
| tomli_loads          | 2.25 sec                                                     | 2.74 sec: 1.22x slower                                                  |
| unpickle_pure_python | 238 us                                                       | 293 us: 1.23x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.04x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 13.0 ms: 1.21x slower                                                   |
| python_startup_no_site | 7.73 ms                                                      | 11.2 ms: 1.45x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.32x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml     | 57.1 ms                                                      | 62.3 ms: 1.09x slower                                                   |
| genshi_text    | 25.5 ms                                                      | 27.9 ms: 1.09x slower                                                   |
| mako           | 11.0 ms                                                      | 13.2 ms: 1.20x slower                                                   |
| Geometric mean | (ref)                                                        | 1.13x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 127 us: 4.20x faster                                                    |
| asyncio_tcp                | 747 ms                                                       | 383 ms: 1.95x faster                                                    |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.60 sec: 1.92x faster                                                  |
| generators                 | 54.6 ms                                                      | 33.7 ms: 1.62x faster                                                   |
| pylint                     | 514 ms                                                       | 347 ms: 1.48x faster                                                    |
| async_tree_memoization     | 629 ms                                                       | 463 ms: 1.36x faster                                                    |
| async_tree_memoization_tg  | 600 ms                                                       | 447 ms: 1.34x faster                                                    |
| async_tree_none_tg         | 474 ms                                                       | 354 ms: 1.34x faster                                                    |
| async_tree_none            | 518 ms                                                       | 395 ms: 1.31x faster                                                    |
| async_tree_io_tg           | 1.15 sec                                                     | 892 ms: 1.29x faster                                                    |
| async_tree_io              | 1.17 sec                                                     | 912 ms: 1.28x faster                                                    |
| json_dumps                 | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                   |
| coroutines                 | 27.8 ms                                                      | 22.6 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 612 ms: 1.23x faster                                                    |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 628 ms: 1.20x faster                                                    |
| json_loads                 | 28.9 us                                                      | 25.3 us: 1.14x faster                                                   |
| logging_simple             | 7.24 us                                                      | 6.59 us: 1.10x faster                                                   |
| xml_etree_parse            | 155 ms                                                       | 144 ms: 1.08x faster                                                    |
| logging_format             | 7.71 us                                                      | 7.29 us: 1.06x faster                                                   |
| thrift                     | 931 us                                                       | 882 us: 1.06x faster                                                    |
| bench_thread_pool          | 1.00 ms                                                      | 954 us: 1.05x faster                                                    |
| richards_super             | 63.6 ms                                                      | 60.9 ms: 1.05x faster                                                   |
| mdp                        | 2.77 sec                                                     | 2.67 sec: 1.04x faster                                                  |
| pickle_dict                | 32.3 us                                                      | 31.2 us: 1.04x faster                                                   |
| chaos                      | 74.9 ms                                                      | 72.5 ms: 1.03x faster                                                   |
| sympy_sum                  | 186 ms                                                       | 180 ms: 1.03x faster                                                    |
| json                       | 5.58 ms                                                      | 5.43 ms: 1.03x faster                                                   |
| chameleon                  | 7.92 ms                                                      | 7.77 ms: 1.02x faster                                                   |
| raytrace                   | 309 ms                                                       | 304 ms: 1.02x faster                                                    |
| comprehensions             | 25.1 us                                                      | 24.7 us: 1.01x faster                                                   |
| xml_etree_iterparse        | 107 ms                                                       | 108 ms: 1.01x slower                                                    |
| sqlglot_transpile          | 1.91 ms                                                      | 1.95 ms: 1.02x slower                                                   |
| dask                       | 410 ms                                                       | 419 ms: 1.02x slower                                                    |
| sqlglot_parse              | 1.51 ms                                                      | 1.55 ms: 1.03x slower                                                   |
| pycparser                  | 1.31 sec                                                     | 1.35 sec: 1.03x slower                                                  |
| sympy_integrate            | 25.8 ms                                                      | 26.5 ms: 1.03x slower                                                   |
| logging_silent             | 100 ns                                                       | 103 ns: 1.03x slower                                                    |
| sympy_str                  | 337 ms                                                       | 347 ms: 1.03x slower                                                    |
| pickle_pure_python         | 316 us                                                       | 326 us: 1.03x slower                                                    |
| tornado_http               | 124 ms                                                       | 129 ms: 1.03x slower                                                    |
| unpickle_list              | 4.60 us                                                      | 4.77 us: 1.04x slower                                                   |
| regex_dna                  | 227 ms                                                       | 236 ms: 1.04x slower                                                    |
| sympy_expand               | 553 ms                                                       | 577 ms: 1.04x slower                                                    |
| deltablue                  | 3.97 ms                                                      | 4.14 ms: 1.04x slower                                                   |
| regex_v8                   | 24.4 ms                                                      | 25.6 ms: 1.05x slower                                                   |
| pickle                     | 9.89 us                                                      | 10.4 us: 1.05x slower                                                   |
| crypto_pyaes               | 83.3 ms                                                      | 87.7 ms: 1.05x slower                                                   |
| pidigits                   | 251 ms                                                       | 266 ms: 1.06x slower                                                    |
| sqlglot_normalize          | 122 ms                                                       | 129 ms: 1.06x slower                                                    |
| deepcopy                   | 391 us                                                       | 417 us: 1.07x slower                                                    |
| regex_effbot               | 3.34 ms                                                      | 3.58 ms: 1.07x slower                                                   |
| deepcopy_reduce            | 3.40 us                                                      | 3.66 us: 1.08x slower                                                   |
| pathlib                    | 18.9 ms                                                      | 20.6 ms: 1.09x slower                                                   |
| meteor_contest             | 131 ms                                                       | 142 ms: 1.09x slower                                                    |
| genshi_xml                 | 57.1 ms                                                      | 62.3 ms: 1.09x slower                                                   |
| richards                   | 49.7 ms                                                      | 54.2 ms: 1.09x slower                                                   |
| genshi_text                | 25.5 ms                                                      | 27.9 ms: 1.09x slower                                                   |
| sqlite_synth               | 2.52 us                                                      | 2.78 us: 1.10x slower                                                   |
| html5lib                   | 72.2 ms                                                      | 79.7 ms: 1.10x slower                                                   |
| 2to3                       | 287 ms                                                       | 316 ms: 1.10x slower                                                    |
| pickle_list                | 3.94 us                                                      | 4.38 us: 1.11x slower                                                   |
| nqueens                    | 103 ms                                                       | 114 ms: 1.11x slower                                                    |
| unpickle                   | 13.3 us                                                      | 14.8 us: 1.11x slower                                                   |
| mypy2                      | 762 ms                                                       | 852 ms: 1.12x slower                                                    |
| xml_etree_process          | 55.9 ms                                                      | 62.5 ms: 1.12x slower                                                   |
| fannkuch                   | 416 ms                                                       | 466 ms: 1.12x slower                                                    |
| gc_traversal               | 4.15 ms                                                      | 4.69 ms: 1.13x slower                                                   |
| xml_etree_generate         | 79.7 ms                                                      | 90.3 ms: 1.13x slower                                                   |
| sqlglot_optimize           | 59.0 ms                                                      | 67.0 ms: 1.14x slower                                                   |
| docutils                   | 2.85 sec                                                     | 3.24 sec: 1.14x slower                                                  |
| dulwich_log                | 67.4 ms                                                      | 77.1 ms: 1.14x slower                                                   |
| gunicorn                   | 966 us                                                       | 1.12 ms: 1.16x slower                                                   |
| aiohttp                    | 986 us                                                       | 1.14 ms: 1.16x slower                                                   |
| deepcopy_memo              | 37.5 us                                                      | 43.7 us: 1.16x slower                                                   |
| create_gc_cycles           | 1.58 ms                                                      | 1.85 ms: 1.17x slower                                                   |
| scimark_lu                 | 114 ms                                                       | 135 ms: 1.19x slower                                                    |
| pprint_pformat             | 1.67 sec                                                     | 1.98 sec: 1.19x slower                                                  |
| async_generators           | 322 ms                                                       | 385 ms: 1.20x slower                                                    |
| mako                       | 11.0 ms                                                      | 13.2 ms: 1.20x slower                                                   |
| pprint_safe_repr           | 805 ms                                                       | 971 ms: 1.21x slower                                                    |
| python_startup             | 10.7 ms                                                      | 13.0 ms: 1.21x slower                                                   |
| tomli_loads                | 2.25 sec                                                     | 2.74 sec: 1.22x slower                                                  |
| float                      | 74.9 ms                                                      | 91.6 ms: 1.22x slower                                                   |
| nbody                      | 92.9 ms                                                      | 114 ms: 1.23x slower                                                    |
| unpickle_pure_python       | 238 us                                                       | 293 us: 1.23x slower                                                    |
| regex_compile              | 156 ms                                                       | 196 ms: 1.25x slower                                                    |
| telco                      | 6.81 ms                                                      | 8.59 ms: 1.26x slower                                                   |
| scimark_monte_carlo        | 69.8 ms                                                      | 92.2 ms: 1.32x slower                                                   |
| coverage                   | 66.1 ms                                                      | 87.8 ms: 1.33x slower                                                   |
| go                         | 158 ms                                                       | 210 ms: 1.33x slower                                                    |
| pyflate                    | 449 ms                                                       | 604 ms: 1.34x slower                                                    |
| hexiom                     | 6.98 ms                                                      | 9.76 ms: 1.40x slower                                                   |
| scimark_fft                | 281 ms                                                       | 404 ms: 1.44x slower                                                    |
| scimark_sor                | 110 ms                                                       | 159 ms: 1.45x slower                                                    |
| python_startup_no_site     | 7.73 ms                                                      | 11.2 ms: 1.45x slower                                                   |
| spectral_norm              | 95.1 ms                                                      | 140 ms: 1.47x slower                                                    |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 6.14 ms: 1.51x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                            |

Benchmark hidden because not significant (2): asyncio_websockets, bench_mp_pool
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.85% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.03x