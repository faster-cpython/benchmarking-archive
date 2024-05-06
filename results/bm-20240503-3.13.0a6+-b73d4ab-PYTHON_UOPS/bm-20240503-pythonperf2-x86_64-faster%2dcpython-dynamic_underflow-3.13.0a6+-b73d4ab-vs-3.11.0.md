# Results vs. 3.11.0

- fork: faster-cpython
- ref: dynamic_underflow
- machine: linux-x86_64
- commit hash: b73d4ab
- commit date: 2024-05-03
- overall geometric mean: 1.12x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| chameleon      | 7.92 ms                                                      | 8.91 ms: 1.12x slower                                                               |
| tornado_http   | 124 ms                                                       | 139 ms: 1.12x slower                                                                |
| Geometric mean | (ref)                                                        | 1.12x slower                                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 451 ms: 1.33x faster                                                                |
| async_tree_none_tg         | 474 ms                                                       | 363 ms: 1.31x faster                                                                |
| async_tree_none            | 518 ms                                                       | 399 ms: 1.30x faster                                                                |
| async_tree_io              | 1.17 sec                                                     | 921 ms: 1.27x faster                                                                |
| async_tree_io_tg           | 1.15 sec                                                     | 922 ms: 1.25x faster                                                                |
| async_tree_memoization     | 629 ms                                                       | 502 ms: 1.25x faster                                                                |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 618 ms: 1.21x faster                                                                |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 649 ms: 1.16x faster                                                                |
| Geometric mean             | (ref)                                                        | 1.26x faster                                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 256 ms: 1.02x slower                                                                |
| float          | 74.9 ms                                                      | 98.7 ms: 1.32x slower                                                               |
| nbody          | 92.9 ms                                                      | 129 ms: 1.39x slower                                                                |
| Geometric mean | (ref)                                                        | 1.23x slower                                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| regex_effbot   | 3.34 ms                                                      | 3.52 ms: 1.05x slower                                                               |
| regex_dna      | 227 ms                                                       | 242 ms: 1.06x slower                                                                |
| regex_v8       | 24.4 ms                                                      | 26.3 ms: 1.08x slower                                                               |
| regex_compile  | 156 ms                                                       | 231 ms: 1.48x slower                                                                |
| Geometric mean | (ref)                                                        | 1.16x slower                                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 11.4 ms: 1.16x faster                                                               |
| json_loads           | 28.9 us                                                      | 25.1 us: 1.15x faster                                                               |
| xml_etree_parse      | 155 ms                                                       | 146 ms: 1.06x faster                                                                |
| pickle_dict          | 32.3 us                                                      | 32.7 us: 1.01x slower                                                               |
| unpickle_list        | 4.60 us                                                      | 4.80 us: 1.04x slower                                                               |
| pickle               | 9.89 us                                                      | 10.7 us: 1.09x slower                                                               |
| xml_etree_iterparse  | 107 ms                                                       | 116 ms: 1.09x slower                                                                |
| pickle_list          | 3.94 us                                                      | 4.37 us: 1.11x slower                                                               |
| unpickle             | 13.3 us                                                      | 15.2 us: 1.15x slower                                                               |
| xml_etree_generate   | 79.7 ms                                                      | 97.6 ms: 1.22x slower                                                               |
| xml_etree_process    | 55.9 ms                                                      | 69.2 ms: 1.24x slower                                                               |
| unpickle_pure_python | 238 us                                                       | 335 us: 1.41x slower                                                                |
| tomli_loads          | 2.25 sec                                                     | 3.32 sec: 1.48x slower                                                              |
| pickle_pure_python   | 316 us                                                       | 479 us: 1.52x slower                                                                |
| Geometric mean       | (ref)                                                        | 1.13x slower                                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 8.93 ms: 1.16x slower                                                               |
| python_startup         | 10.7 ms                                                      | 13.0 ms: 1.21x slower                                                               |
| Geometric mean         | (ref)                                                        | 1.18x slower                                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| django_template | 39.3 ms                                                      | 46.8 ms: 1.19x slower                                                               |
| mako            | 11.0 ms                                                      | 14.2 ms: 1.29x slower                                                               |
| Geometric mean  | (ref)                                                        | 1.24x slower                                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240503-pythonperf2-x86_64-faster%2dcpython-dynamic_underflow-3.13.0a6+-b73d4ab |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 204 us: 2.60x faster                                                                |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.61 sec: 1.91x faster                                                              |
| asyncio_tcp                | 747 ms                                                       | 392 ms: 1.91x faster                                                                |
| generators                 | 54.6 ms                                                      | 34.2 ms: 1.60x faster                                                               |
| async_tree_memoization_tg  | 600 ms                                                       | 451 ms: 1.33x faster                                                                |
| async_tree_none_tg         | 474 ms                                                       | 363 ms: 1.31x faster                                                                |
| async_tree_none            | 518 ms                                                       | 399 ms: 1.30x faster                                                                |
| async_tree_io              | 1.17 sec                                                     | 921 ms: 1.27x faster                                                                |
| async_tree_io_tg           | 1.15 sec                                                     | 922 ms: 1.25x faster                                                                |
| async_tree_memoization     | 629 ms                                                       | 502 ms: 1.25x faster                                                                |
| coroutines                 | 27.8 ms                                                      | 22.5 ms: 1.23x faster                                                               |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 618 ms: 1.21x faster                                                                |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 649 ms: 1.16x faster                                                                |
| json_dumps                 | 13.3 ms                                                      | 11.4 ms: 1.16x faster                                                               |
| json_loads                 | 28.9 us                                                      | 25.1 us: 1.15x faster                                                               |
| pylint                     | 514 ms                                                       | 454 ms: 1.13x faster                                                                |
| logging_simple             | 7.24 us                                                      | 6.81 us: 1.06x faster                                                               |
| xml_etree_parse            | 155 ms                                                       | 146 ms: 1.06x faster                                                                |
| logging_format             | 7.71 us                                                      | 7.50 us: 1.03x faster                                                               |
| pathlib                    | 18.9 ms                                                      | 18.5 ms: 1.02x faster                                                               |
| json                       | 5.58 ms                                                      | 5.53 ms: 1.01x faster                                                               |
| pickle_dict                | 32.3 us                                                      | 32.7 us: 1.01x slower                                                               |
| pidigits                   | 251 ms                                                       | 256 ms: 1.02x slower                                                                |
| unpickle_list              | 4.60 us                                                      | 4.80 us: 1.04x slower                                                               |
| bench_mp_pool              | 4.70 ms                                                      | 4.92 ms: 1.05x slower                                                               |
| bench_thread_pool          | 1.00 ms                                                      | 1.05 ms: 1.05x slower                                                               |
| regex_effbot               | 3.34 ms                                                      | 3.52 ms: 1.05x slower                                                               |
| regex_dna                  | 227 ms                                                       | 242 ms: 1.06x slower                                                                |
| dask                       | 410 ms                                                       | 441 ms: 1.08x slower                                                                |
| gc_traversal               | 4.15 ms                                                      | 4.47 ms: 1.08x slower                                                               |
| regex_v8                   | 24.4 ms                                                      | 26.3 ms: 1.08x slower                                                               |
| pickle                     | 9.89 us                                                      | 10.7 us: 1.09x slower                                                               |
| xml_etree_iterparse        | 107 ms                                                       | 116 ms: 1.09x slower                                                                |
| pickle_list                | 3.94 us                                                      | 4.37 us: 1.11x slower                                                               |
| chaos                      | 74.9 ms                                                      | 83.5 ms: 1.11x slower                                                               |
| crypto_pyaes               | 83.3 ms                                                      | 92.9 ms: 1.12x slower                                                               |
| sympy_sum                  | 186 ms                                                       | 208 ms: 1.12x slower                                                                |
| tornado_http               | 124 ms                                                       | 139 ms: 1.12x slower                                                                |
| chameleon                  | 7.92 ms                                                      | 8.91 ms: 1.12x slower                                                               |
| comprehensions             | 25.1 us                                                      | 28.3 us: 1.13x slower                                                               |
| meteor_contest             | 131 ms                                                       | 148 ms: 1.14x slower                                                                |
| unpickle                   | 13.3 us                                                      | 15.2 us: 1.15x slower                                                               |
| pycparser                  | 1.31 sec                                                     | 1.51 sec: 1.15x slower                                                              |
| python_startup_no_site     | 7.73 ms                                                      | 8.93 ms: 1.16x slower                                                               |
| sqlglot_parse              | 1.51 ms                                                      | 1.76 ms: 1.16x slower                                                               |
| nqueens                    | 103 ms                                                       | 120 ms: 1.17x slower                                                                |
| sqlite_synth               | 2.52 us                                                      | 2.95 us: 1.17x slower                                                               |
| raytrace                   | 309 ms                                                       | 365 ms: 1.18x slower                                                                |
| sympy_integrate            | 25.8 ms                                                      | 30.4 ms: 1.18x slower                                                               |
| sqlglot_transpile          | 1.91 ms                                                      | 2.26 ms: 1.18x slower                                                               |
| django_template            | 39.3 ms                                                      | 46.8 ms: 1.19x slower                                                               |
| fannkuch                   | 416 ms                                                       | 498 ms: 1.20x slower                                                                |
| python_startup             | 10.7 ms                                                      | 13.0 ms: 1.21x slower                                                               |
| sympy_str                  | 337 ms                                                       | 410 ms: 1.22x slower                                                                |
| deepcopy_reduce            | 3.40 us                                                      | 4.14 us: 1.22x slower                                                               |
| xml_etree_generate         | 79.7 ms                                                      | 97.6 ms: 1.22x slower                                                               |
| richards_super             | 63.6 ms                                                      | 78.3 ms: 1.23x slower                                                               |
| coverage                   | 66.1 ms                                                      | 81.6 ms: 1.23x slower                                                               |
| async_generators           | 322 ms                                                       | 398 ms: 1.24x slower                                                                |
| xml_etree_process          | 55.9 ms                                                      | 69.2 ms: 1.24x slower                                                               |
| sympy_expand               | 553 ms                                                       | 685 ms: 1.24x slower                                                                |
| sqlglot_normalize          | 122 ms                                                       | 153 ms: 1.26x slower                                                                |
| sqlglot_optimize           | 59.0 ms                                                      | 74.3 ms: 1.26x slower                                                               |
| deepcopy                   | 391 us                                                       | 495 us: 1.27x slower                                                                |
| create_gc_cycles           | 1.58 ms                                                      | 2.01 ms: 1.27x slower                                                               |
| mako                       | 11.0 ms                                                      | 14.2 ms: 1.29x slower                                                               |
| gunicorn                   | 966 us                                                       | 1.26 ms: 1.30x slower                                                               |
| scimark_lu                 | 114 ms                                                       | 149 ms: 1.31x slower                                                                |
| aiohttp                    | 986 us                                                       | 1.30 ms: 1.32x slower                                                               |
| float                      | 74.9 ms                                                      | 98.7 ms: 1.32x slower                                                               |
| dulwich_log                | 67.4 ms                                                      | 88.7 ms: 1.32x slower                                                               |
| mypy2                      | 762 ms                                                       | 1.01 sec: 1.33x slower                                                              |
| flaskblogging              | 3.88 ms                                                      | 5.19 ms: 1.34x slower                                                               |
| pprint_pformat             | 1.67 sec                                                     | 2.25 sec: 1.35x slower                                                              |
| pprint_safe_repr           | 805 ms                                                       | 1.10 sec: 1.36x slower                                                              |
| go                         | 158 ms                                                       | 216 ms: 1.37x slower                                                                |
| telco                      | 6.81 ms                                                      | 9.35 ms: 1.37x slower                                                               |
| nbody                      | 92.9 ms                                                      | 129 ms: 1.39x slower                                                                |
| unpickle_pure_python       | 238 us                                                       | 335 us: 1.41x slower                                                                |
| pyflate                    | 449 ms                                                       | 632 ms: 1.41x slower                                                                |
| richards                   | 49.7 ms                                                      | 70.8 ms: 1.42x slower                                                               |
| tomli_loads                | 2.25 sec                                                     | 3.32 sec: 1.48x slower                                                              |
| regex_compile              | 156 ms                                                       | 231 ms: 1.48x slower                                                                |
| pickle_pure_python         | 316 us                                                       | 479 us: 1.52x slower                                                                |
| scimark_sor                | 110 ms                                                       | 167 ms: 1.52x slower                                                                |
| spectral_norm              | 95.1 ms                                                      | 146 ms: 1.54x slower                                                                |
| scimark_fft                | 281 ms                                                       | 437 ms: 1.56x slower                                                                |
| scimark_monte_carlo        | 69.8 ms                                                      | 109 ms: 1.56x slower                                                                |
| hexiom                     | 6.98 ms                                                      | 10.9 ms: 1.57x slower                                                               |
| deltablue                  | 3.97 ms                                                      | 6.33 ms: 1.60x slower                                                               |
| deepcopy_memo              | 37.5 us                                                      | 62.1 us: 1.66x slower                                                               |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 6.92 ms: 1.70x slower                                                               |
| logging_silent             | 100 ns                                                       | 174 ns: 1.74x slower                                                                |
| Geometric mean             | (ref)                                                        | 1.12x slower                                                                        |

Benchmark hidden because not significant (3): mdp, asyncio_websockets, thrift
Ignored benchmarks (8) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: 2to3, docutils, genshi_text, genshi_xml, html5lib, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.03x