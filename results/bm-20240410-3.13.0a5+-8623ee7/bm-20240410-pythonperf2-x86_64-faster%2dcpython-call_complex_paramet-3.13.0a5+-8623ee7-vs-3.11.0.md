# Results vs. 3.11.0

- fork: faster-cpython
- ref: call_complex_paramet
- machine: linux-x86_64
- commit hash: 8623ee7
- commit date: 2024-04-10
- overall geometric mean: 1.07x faster
- HPT reliability: 99.94%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 292 ms: 1.02x slower                                                                   |
| chameleon      | 7.92 ms                                                      | 7.12 ms: 1.11x faster                                                                  |
| docutils       | 2.85 sec                                                     | 2.99 sec: 1.05x slower                                                                 |
| html5lib       | 72.2 ms                                                      | 74.6 ms: 1.03x slower                                                                  |
| tornado_http   | 124 ms                                                       | 120 ms: 1.04x faster                                                                   |
| Geometric mean | (ref)                                                        | 1.01x faster                                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 419 ms: 1.43x faster                                                                   |
| async_tree_none            | 518 ms                                                       | 369 ms: 1.40x faster                                                                   |
| async_tree_none_tg         | 474 ms                                                       | 339 ms: 1.40x faster                                                                   |
| async_tree_memoization     | 629 ms                                                       | 462 ms: 1.36x faster                                                                   |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 573 ms: 1.31x faster                                                                   |
| async_tree_io_tg           | 1.15 sec                                                     | 885 ms: 1.30x faster                                                                   |
| async_tree_io              | 1.17 sec                                                     | 905 ms: 1.29x faster                                                                   |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 609 ms: 1.24x faster                                                                   |
| Geometric mean             | (ref)                                                        | 1.34x faster                                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 90.0 ms: 1.03x faster                                                                  |
| float          | 74.9 ms                                                      | 77.2 ms: 1.03x slower                                                                  |
| pidigits       | 251 ms                                                       | 262 ms: 1.04x slower                                                                   |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 142 ms: 1.10x faster                                                                   |
| regex_v8       | 24.4 ms                                                      | 26.0 ms: 1.06x slower                                                                  |
| regex_effbot   | 3.34 ms                                                      | 3.56 ms: 1.06x slower                                                                  |
| regex_dna      | 227 ms                                                       | 252 ms: 1.11x slower                                                                   |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.5 ms: 1.26x faster                                                                  |
| json_loads           | 28.9 us                                                      | 25.9 us: 1.12x faster                                                                  |
| xml_etree_parse      | 155 ms                                                       | 146 ms: 1.06x faster                                                                   |
| unpickle_pure_python | 238 us                                                       | 225 us: 1.06x faster                                                                   |
| tomli_loads          | 2.25 sec                                                     | 2.19 sec: 1.03x faster                                                                 |
| xml_etree_iterparse  | 107 ms                                                       | 105 ms: 1.02x faster                                                                   |
| pickle_dict          | 32.3 us                                                      | 33.6 us: 1.04x slower                                                                  |
| xml_etree_process    | 55.9 ms                                                      | 58.9 ms: 1.05x slower                                                                  |
| xml_etree_generate   | 79.7 ms                                                      | 84.5 ms: 1.06x slower                                                                  |
| pickle               | 9.89 us                                                      | 10.6 us: 1.07x slower                                                                  |
| pickle_list          | 3.94 us                                                      | 4.42 us: 1.12x slower                                                                  |
| unpickle             | 13.3 us                                                      | 14.9 us: 1.13x slower                                                                  |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                                           |

Benchmark hidden because not significant (2): pickle_pure_python, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 12.9 ms: 1.20x slower                                                                  |
| python_startup_no_site | 7.73 ms                                                      | 11.1 ms: 1.44x slower                                                                  |
| Geometric mean         | (ref)                                                        | 1.31x slower                                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| mako           | 11.0 ms                                                      | 10.2 ms: 1.08x faster                                                                  |
| genshi_xml     | 57.1 ms                                                      | 54.3 ms: 1.05x faster                                                                  |
| genshi_text    | 25.5 ms                                                      | 25.1 ms: 1.02x faster                                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 114 us: 4.68x faster                                                                   |
| asyncio_tcp                | 747 ms                                                       | 372 ms: 2.01x faster                                                                   |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                                 |
| generators                 | 54.6 ms                                                      | 33.6 ms: 1.63x faster                                                                  |
| pylint                     | 514 ms                                                       | 317 ms: 1.62x faster                                                                   |
| comprehensions             | 25.1 us                                                      | 16.6 us: 1.51x faster                                                                  |
| async_tree_memoization_tg  | 600 ms                                                       | 419 ms: 1.43x faster                                                                   |
| async_tree_none            | 518 ms                                                       | 369 ms: 1.40x faster                                                                   |
| async_tree_none_tg         | 474 ms                                                       | 339 ms: 1.40x faster                                                                   |
| async_tree_memoization     | 629 ms                                                       | 462 ms: 1.36x faster                                                                   |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 573 ms: 1.31x faster                                                                   |
| async_tree_io_tg           | 1.15 sec                                                     | 885 ms: 1.30x faster                                                                   |
| async_tree_io              | 1.17 sec                                                     | 905 ms: 1.29x faster                                                                   |
| json_dumps                 | 13.3 ms                                                      | 10.5 ms: 1.26x faster                                                                  |
| chaos                      | 74.9 ms                                                      | 59.9 ms: 1.25x faster                                                                  |
| coroutines                 | 27.8 ms                                                      | 22.4 ms: 1.24x faster                                                                  |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 609 ms: 1.24x faster                                                                   |
| scimark_lu                 | 114 ms                                                       | 95.2 ms: 1.20x faster                                                                  |
| raytrace                   | 309 ms                                                       | 258 ms: 1.20x faster                                                                   |
| sympy_sum                  | 186 ms                                                       | 155 ms: 1.20x faster                                                                   |
| crypto_pyaes               | 83.3 ms                                                      | 71.8 ms: 1.16x faster                                                                  |
| deltablue                  | 3.97 ms                                                      | 3.45 ms: 1.15x faster                                                                  |
| nqueens                    | 103 ms                                                       | 90.1 ms: 1.14x faster                                                                  |
| sympy_str                  | 337 ms                                                       | 296 ms: 1.14x faster                                                                   |
| bench_thread_pool          | 1.00 ms                                                      | 888 us: 1.13x faster                                                                   |
| json_loads                 | 28.9 us                                                      | 25.9 us: 1.12x faster                                                                  |
| chameleon                  | 7.92 ms                                                      | 7.12 ms: 1.11x faster                                                                  |
| sympy_expand               | 553 ms                                                       | 499 ms: 1.11x faster                                                                   |
| sympy_integrate            | 25.8 ms                                                      | 23.4 ms: 1.10x faster                                                                  |
| logging_simple             | 7.24 us                                                      | 6.59 us: 1.10x faster                                                                  |
| regex_compile              | 156 ms                                                       | 142 ms: 1.10x faster                                                                   |
| richards_super             | 63.6 ms                                                      | 58.2 ms: 1.09x faster                                                                  |
| mdp                        | 2.77 sec                                                     | 2.54 sec: 1.09x faster                                                                 |
| sqlglot_parse              | 1.51 ms                                                      | 1.40 ms: 1.08x faster                                                                  |
| hexiom                     | 6.98 ms                                                      | 6.45 ms: 1.08x faster                                                                  |
| mako                       | 11.0 ms                                                      | 10.2 ms: 1.08x faster                                                                  |
| sqlglot_transpile          | 1.91 ms                                                      | 1.78 ms: 1.07x faster                                                                  |
| logging_format             | 7.71 us                                                      | 7.27 us: 1.06x faster                                                                  |
| fannkuch                   | 416 ms                                                       | 392 ms: 1.06x faster                                                                   |
| xml_etree_parse            | 155 ms                                                       | 146 ms: 1.06x faster                                                                   |
| thrift                     | 931 us                                                       | 880 us: 1.06x faster                                                                   |
| unpickle_pure_python       | 238 us                                                       | 225 us: 1.06x faster                                                                   |
| logging_silent             | 100 ns                                                       | 95.3 ns: 1.05x faster                                                                  |
| genshi_xml                 | 57.1 ms                                                      | 54.3 ms: 1.05x faster                                                                  |
| dask                       | 410 ms                                                       | 395 ms: 1.04x faster                                                                   |
| tornado_http               | 124 ms                                                       | 120 ms: 1.04x faster                                                                   |
| sqlglot_normalize          | 122 ms                                                       | 118 ms: 1.03x faster                                                                   |
| nbody                      | 92.9 ms                                                      | 90.0 ms: 1.03x faster                                                                  |
| pprint_pformat             | 1.67 sec                                                     | 1.62 sec: 1.03x faster                                                                 |
| pycparser                  | 1.31 sec                                                     | 1.27 sec: 1.03x faster                                                                 |
| tomli_loads                | 2.25 sec                                                     | 2.19 sec: 1.03x faster                                                                 |
| genshi_text                | 25.5 ms                                                      | 25.1 ms: 1.02x faster                                                                  |
| xml_etree_iterparse        | 107 ms                                                       | 105 ms: 1.02x faster                                                                   |
| pprint_safe_repr           | 805 ms                                                       | 792 ms: 1.02x faster                                                                   |
| meteor_contest             | 131 ms                                                       | 129 ms: 1.01x faster                                                                   |
| json                       | 5.58 ms                                                      | 5.53 ms: 1.01x faster                                                                  |
| deepcopy                   | 391 us                                                       | 387 us: 1.01x faster                                                                   |
| sqlglot_optimize           | 59.0 ms                                                      | 58.6 ms: 1.01x faster                                                                  |
| dulwich_log                | 67.4 ms                                                      | 68.0 ms: 1.01x slower                                                                  |
| asyncio_websockets         | 390 ms                                                       | 395 ms: 1.01x slower                                                                   |
| mypy2                      | 762 ms                                                       | 772 ms: 1.01x slower                                                                   |
| 2to3                       | 287 ms                                                       | 292 ms: 1.02x slower                                                                   |
| deepcopy_reduce            | 3.40 us                                                      | 3.48 us: 1.03x slower                                                                  |
| pathlib                    | 18.9 ms                                                      | 19.4 ms: 1.03x slower                                                                  |
| float                      | 74.9 ms                                                      | 77.2 ms: 1.03x slower                                                                  |
| html5lib                   | 72.2 ms                                                      | 74.6 ms: 1.03x slower                                                                  |
| pickle_dict                | 32.3 us                                                      | 33.6 us: 1.04x slower                                                                  |
| pidigits                   | 251 ms                                                       | 262 ms: 1.04x slower                                                                   |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.24 ms: 1.04x slower                                                                  |
| richards                   | 49.7 ms                                                      | 52.2 ms: 1.05x slower                                                                  |
| docutils                   | 2.85 sec                                                     | 2.99 sec: 1.05x slower                                                                 |
| xml_etree_process          | 55.9 ms                                                      | 58.9 ms: 1.05x slower                                                                  |
| scimark_fft                | 281 ms                                                       | 297 ms: 1.06x slower                                                                   |
| xml_etree_generate         | 79.7 ms                                                      | 84.5 ms: 1.06x slower                                                                  |
| regex_v8                   | 24.4 ms                                                      | 26.0 ms: 1.06x slower                                                                  |
| regex_effbot               | 3.34 ms                                                      | 3.56 ms: 1.06x slower                                                                  |
| pickle                     | 9.89 us                                                      | 10.6 us: 1.07x slower                                                                  |
| gunicorn                   | 966 us                                                       | 1.04 ms: 1.08x slower                                                                  |
| go                         | 158 ms                                                       | 170 ms: 1.08x slower                                                                   |
| sqlite_synth               | 2.52 us                                                      | 2.74 us: 1.09x slower                                                                  |
| aiohttp                    | 986 us                                                       | 1.07 ms: 1.09x slower                                                                  |
| regex_dna                  | 227 ms                                                       | 252 ms: 1.11x slower                                                                   |
| pickle_list                | 3.94 us                                                      | 4.42 us: 1.12x slower                                                                  |
| unpickle                   | 13.3 us                                                      | 14.9 us: 1.13x slower                                                                  |
| gc_traversal               | 4.15 ms                                                      | 4.68 ms: 1.13x slower                                                                  |
| async_generators           | 322 ms                                                       | 364 ms: 1.13x slower                                                                   |
| pyflate                    | 449 ms                                                       | 523 ms: 1.16x slower                                                                   |
| create_gc_cycles           | 1.58 ms                                                      | 1.87 ms: 1.19x slower                                                                  |
| telco                      | 6.81 ms                                                      | 8.11 ms: 1.19x slower                                                                  |
| python_startup             | 10.7 ms                                                      | 12.9 ms: 1.20x slower                                                                  |
| scimark_sor                | 110 ms                                                       | 141 ms: 1.29x slower                                                                   |
| coverage                   | 66.1 ms                                                      | 85.3 ms: 1.29x slower                                                                  |
| python_startup_no_site     | 7.73 ms                                                      | 11.1 ms: 1.44x slower                                                                  |
| Geometric mean             | (ref)                                                        | 1.07x faster                                                                           |

Benchmark hidden because not significant (6): bench_mp_pool, pickle_pure_python, spectral_norm, unpickle_list, scimark_monte_carlo, deepcopy_memo
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.94% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.02x