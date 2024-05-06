# Results vs. 3.11.0

- fork: faster-cpython
- ref: stats_for_all_ops
- machine: linux-x86_64
- commit hash: 17ed8bc
- commit date: 2024-04-05
- overall geometric mean: 1.06x faster
- HPT reliability: 94.39%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 269 ms: 1.02x slower                                                          |
| chameleon      | 6.70 ms                                                | 6.99 ms: 1.04x slower                                                         |
| docutils       | 2.66 sec                                               | 2.81 sec: 1.05x slower                                                        |
| html5lib       | 64.8 ms                                                | 66.6 ms: 1.03x slower                                                         |
| tornado_http   | 98.1 ms                                                | 94.6 ms: 1.04x faster                                                         |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 352 ms: 1.50x faster                                                          |
| async_tree_none_tg         | 491 ms                                                 | 333 ms: 1.47x faster                                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                          |
| async_tree_io_tg           | 1.29 sec                                               | 928 ms: 1.39x faster                                                          |
| async_tree_io              | 1.29 sec                                               | 930 ms: 1.38x faster                                                          |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                                          |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 608 ms: 1.25x faster                                                          |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 615 ms: 1.22x faster                                                          |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 191 ms: 1.02x faster                                                          |
| float          | 78.9 ms                                                | 81.0 ms: 1.03x slower                                                         |
| nbody          | 96.0 ms                                                | 116 ms: 1.21x slower                                                          |
| Geometric mean | (ref)                                                  | 1.07x slower                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 136 ms: 1.04x faster                                                          |
| regex_effbot   | 3.51 ms                                                | 3.87 ms: 1.10x slower                                                         |
| regex_dna      | 205 ms                                                 | 232 ms: 1.13x slower                                                          |
| regex_v8       | 22.9 ms                                                | 26.1 ms: 1.14x slower                                                         |
| Geometric mean | (ref)                                                  | 1.08x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                         |
| unpickle_pure_python | 242 us                                                 | 217 us: 1.11x faster                                                          |
| pickle_pure_python   | 320 us                                                 | 299 us: 1.07x faster                                                          |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.02x faster                                                          |
| tomli_loads          | 2.30 sec                                               | 2.25 sec: 1.02x faster                                                        |
| json_loads           | 29.2 us                                                | 28.6 us: 1.02x faster                                                         |
| xml_etree_iterparse  | 108 ms                                                 | 106 ms: 1.02x faster                                                          |
| pickle_dict          | 34.6 us                                                | 34.5 us: 1.00x faster                                                         |
| unpickle_list        | 5.21 us                                                | 5.27 us: 1.01x slower                                                         |
| xml_etree_process    | 56.9 ms                                                | 59.8 ms: 1.05x slower                                                         |
| xml_etree_generate   | 81.1 ms                                                | 86.4 ms: 1.07x slower                                                         |
| pickle               | 11.0 us                                                | 11.9 us: 1.09x slower                                                         |
| unpickle             | 13.8 us                                                | 15.8 us: 1.14x slower                                                         |
| pickle_list          | 4.59 us                                                | 5.26 us: 1.15x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.6 ms: 1.24x slower                                                         |
| python_startup_no_site | 6.01 ms                                                | 9.02 ms: 1.50x slower                                                         |
| Geometric mean         | (ref)                                                  | 1.36x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_xml     | 53.4 ms                                                | 51.6 ms: 1.04x faster                                                         |
| mako           | 10.7 ms                                                | 11.0 ms: 1.03x slower                                                         |
| genshi_text    | 22.5 ms                                                | 23.4 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                  | 1.01x slower                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 114 us: 4.54x faster                                                          |
| generators                 | 74.9 ms                                                | 29.4 ms: 2.55x faster                                                         |
| asyncio_tcp                | 875 ms                                                 | 508 ms: 1.72x faster                                                          |
| pylint                     | 476 ms                                                 | 279 ms: 1.71x faster                                                          |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                        |
| async_tree_none            | 528 ms                                                 | 352 ms: 1.50x faster                                                          |
| async_tree_none_tg         | 491 ms                                                 | 333 ms: 1.47x faster                                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                          |
| comprehensions             | 23.6 us                                                | 16.7 us: 1.42x faster                                                         |
| async_tree_io_tg           | 1.29 sec                                               | 928 ms: 1.39x faster                                                          |
| async_tree_io              | 1.29 sec                                               | 930 ms: 1.38x faster                                                          |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                                          |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                         |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 608 ms: 1.25x faster                                                          |
| deltablue                  | 3.92 ms                                                | 3.21 ms: 1.22x faster                                                         |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 615 ms: 1.22x faster                                                          |
| richards_super             | 61.9 ms                                                | 52.9 ms: 1.17x faster                                                         |
| coroutines                 | 27.0 ms                                                | 24.0 ms: 1.12x faster                                                         |
| hexiom                     | 6.89 ms                                                | 6.15 ms: 1.12x faster                                                         |
| unpickle_pure_python       | 242 us                                                 | 217 us: 1.11x faster                                                          |
| raytrace                   | 309 ms                                                 | 278 ms: 1.11x faster                                                          |
| sqlglot_parse              | 1.43 ms                                                | 1.30 ms: 1.11x faster                                                         |
| logging_silent             | 111 ns                                                 | 101 ns: 1.10x faster                                                          |
| sqlglot_transpile          | 1.75 ms                                                | 1.60 ms: 1.09x faster                                                         |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.08x faster                                                          |
| logging_simple             | 6.22 us                                                | 5.78 us: 1.08x faster                                                         |
| pickle_pure_python         | 320 us                                                 | 299 us: 1.07x faster                                                          |
| richards                   | 49.8 ms                                                | 46.8 ms: 1.06x faster                                                         |
| sympy_str                  | 297 ms                                                 | 280 ms: 1.06x faster                                                          |
| chaos                      | 71.9 ms                                                | 67.8 ms: 1.06x faster                                                         |
| logging_format             | 6.81 us                                                | 6.44 us: 1.06x faster                                                         |
| deepcopy_memo              | 40.2 us                                                | 38.1 us: 1.05x faster                                                         |
| gc_traversal               | 4.01 ms                                                | 3.80 ms: 1.05x faster                                                         |
| nqueens                    | 87.9 ms                                                | 83.5 ms: 1.05x faster                                                         |
| crypto_pyaes               | 76.7 ms                                                | 73.0 ms: 1.05x faster                                                         |
| sympy_integrate            | 21.5 ms                                                | 20.4 ms: 1.05x faster                                                         |
| regex_compile              | 141 ms                                                 | 136 ms: 1.04x faster                                                          |
| tornado_http               | 98.1 ms                                                | 94.6 ms: 1.04x faster                                                         |
| genshi_xml                 | 53.4 ms                                                | 51.6 ms: 1.04x faster                                                         |
| sympy_expand               | 484 ms                                                 | 471 ms: 1.03x faster                                                          |
| deepcopy                   | 365 us                                                 | 355 us: 1.03x faster                                                          |
| pprint_pformat             | 1.55 sec                                               | 1.51 sec: 1.03x faster                                                        |
| go                         | 149 ms                                                 | 145 ms: 1.03x faster                                                          |
| sqlglot_normalize          | 113 ms                                                 | 110 ms: 1.02x faster                                                          |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.02x faster                                                          |
| tomli_loads                | 2.30 sec                                               | 2.25 sec: 1.02x faster                                                        |
| json_loads                 | 29.2 us                                                | 28.6 us: 1.02x faster                                                         |
| pidigits                   | 194 ms                                                 | 191 ms: 1.02x faster                                                          |
| xml_etree_iterparse        | 108 ms                                                 | 106 ms: 1.02x faster                                                          |
| pprint_safe_repr           | 747 ms                                                 | 737 ms: 1.01x faster                                                          |
| bench_thread_pool          | 834 us                                                 | 828 us: 1.01x faster                                                          |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                         |
| deepcopy_reduce            | 3.22 us                                                | 3.20 us: 1.01x faster                                                         |
| sqlglot_optimize           | 55.3 ms                                                | 54.9 ms: 1.01x faster                                                         |
| fannkuch                   | 405 ms                                                 | 404 ms: 1.00x faster                                                          |
| meteor_contest             | 109 ms                                                 | 109 ms: 1.00x faster                                                          |
| pickle_dict                | 34.6 us                                                | 34.5 us: 1.00x faster                                                         |
| mdp                        | 2.77 sec                                               | 2.79 sec: 1.00x slower                                                        |
| unpickle_list              | 5.21 us                                                | 5.27 us: 1.01x slower                                                         |
| pycparser                  | 1.19 sec                                               | 1.20 sec: 1.01x slower                                                        |
| 2to3                       | 264 ms                                                 | 269 ms: 1.02x slower                                                          |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                                          |
| float                      | 78.9 ms                                                | 81.0 ms: 1.03x slower                                                         |
| thrift                     | 784 us                                                 | 804 us: 1.03x slower                                                          |
| html5lib                   | 64.8 ms                                                | 66.6 ms: 1.03x slower                                                         |
| json                       | 5.24 ms                                                | 5.39 ms: 1.03x slower                                                         |
| mako                       | 10.7 ms                                                | 11.0 ms: 1.03x slower                                                         |
| scimark_monte_carlo        | 70.7 ms                                                | 72.8 ms: 1.03x slower                                                         |
| pathlib                    | 18.5 ms                                                | 19.1 ms: 1.03x slower                                                         |
| genshi_text                | 22.5 ms                                                | 23.4 ms: 1.04x slower                                                         |
| chameleon                  | 6.70 ms                                                | 6.99 ms: 1.04x slower                                                         |
| dulwich_log                | 64.6 ms                                                | 67.6 ms: 1.05x slower                                                         |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                         |
| xml_etree_process          | 56.9 ms                                                | 59.8 ms: 1.05x slower                                                         |
| docutils                   | 2.66 sec                                               | 2.81 sec: 1.05x slower                                                        |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                                         |
| xml_etree_generate         | 81.1 ms                                                | 86.4 ms: 1.07x slower                                                         |
| mypy2                      | 686 ms                                                 | 739 ms: 1.08x slower                                                          |
| pickle                     | 11.0 us                                                | 11.9 us: 1.09x slower                                                         |
| regex_effbot               | 3.51 ms                                                | 3.87 ms: 1.10x slower                                                         |
| scimark_sor                | 121 ms                                                 | 134 ms: 1.10x slower                                                          |
| pyflate                    | 434 ms                                                 | 482 ms: 1.11x slower                                                          |
| regex_dna                  | 205 ms                                                 | 232 ms: 1.13x slower                                                          |
| regex_v8                   | 22.9 ms                                                | 26.1 ms: 1.14x slower                                                         |
| sqlite_synth               | 2.57 us                                                | 2.93 us: 1.14x slower                                                         |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.74 ms: 1.14x slower                                                         |
| unpickle                   | 13.8 us                                                | 15.8 us: 1.14x slower                                                         |
| pickle_list                | 4.59 us                                                | 5.26 us: 1.15x slower                                                         |
| async_generators           | 374 ms                                                 | 444 ms: 1.19x slower                                                          |
| nbody                      | 96.0 ms                                                | 116 ms: 1.21x slower                                                          |
| scimark_fft                | 345 ms                                                 | 419 ms: 1.21x slower                                                          |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                                         |
| python_startup             | 8.56 ms                                                | 10.6 ms: 1.24x slower                                                         |
| spectral_norm              | 108 ms                                                 | 135 ms: 1.25x slower                                                          |
| coverage                   | 78.8 ms                                                | 98.6 ms: 1.25x slower                                                         |
| telco                      | 6.86 ms                                                | 8.63 ms: 1.26x slower                                                         |
| python_startup_no_site     | 6.01 ms                                                | 9.02 ms: 1.50x slower                                                         |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                  |

Benchmark hidden because not significant (2): scimark_lu, dask
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 94.39% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x