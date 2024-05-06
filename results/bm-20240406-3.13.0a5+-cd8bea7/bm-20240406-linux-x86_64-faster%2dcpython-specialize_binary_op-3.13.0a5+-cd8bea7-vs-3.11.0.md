# Results vs. 3.11.0

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: cd8bea7
- commit date: 2024-04-06
- overall geometric mean: 1.07x faster
- HPT reliability: 99.80%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 268 ms: 1.02x slower                                                             |
| chameleon      | 6.70 ms                                                | 6.97 ms: 1.04x slower                                                            |
| docutils       | 2.66 sec                                               | 2.80 sec: 1.05x slower                                                           |
| html5lib       | 64.8 ms                                                | 68.2 ms: 1.05x slower                                                            |
| tornado_http   | 98.1 ms                                                | 93.9 ms: 1.04x faster                                                            |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 355 ms: 1.49x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 334 ms: 1.47x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 920 ms: 1.40x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 926 ms: 1.40x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 457 ms: 1.40x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 600 ms: 1.27x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 607 ms: 1.23x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.38x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 78.9 ms                                                | 77.6 ms: 1.02x faster                                                            |
| nbody          | 96.0 ms                                                | 94.4 ms: 1.02x faster                                                            |
| pidigits       | 194 ms                                                 | 194 ms: 1.00x faster                                                             |
| Geometric mean | (ref)                                                  | 1.01x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 135 ms: 1.05x faster                                                             |
| regex_effbot   | 3.51 ms                                                | 3.81 ms: 1.09x slower                                                            |
| regex_dna      | 205 ms                                                 | 230 ms: 1.12x slower                                                             |
| regex_v8       | 22.9 ms                                                | 26.2 ms: 1.14x slower                                                            |
| Geometric mean | (ref)                                                  | 1.07x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                            |
| unpickle_pure_python | 242 us                                                 | 219 us: 1.10x faster                                                             |
| pickle_pure_python   | 320 us                                                 | 302 us: 1.06x faster                                                             |
| unpickle_list        | 5.21 us                                                | 4.98 us: 1.05x faster                                                            |
| tomli_loads          | 2.30 sec                                               | 2.21 sec: 1.04x faster                                                           |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.03x faster                                                             |
| json_loads           | 29.2 us                                                | 28.7 us: 1.02x faster                                                            |
| xml_etree_iterparse  | 108 ms                                                 | 106 ms: 1.01x faster                                                             |
| pickle_dict          | 34.6 us                                                | 35.5 us: 1.03x slower                                                            |
| xml_etree_process    | 56.9 ms                                                | 60.0 ms: 1.05x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 86.7 ms: 1.07x slower                                                            |
| pickle               | 11.0 us                                                | 11.8 us: 1.07x slower                                                            |
| unpickle             | 13.8 us                                                | 15.4 us: 1.11x slower                                                            |
| pickle_list          | 4.59 us                                                | 5.18 us: 1.13x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.6 ms: 1.23x slower                                                            |
| python_startup_no_site | 6.01 ms                                                | 8.99 ms: 1.50x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.36x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml     | 53.4 ms                                                | 51.7 ms: 1.03x faster                                                            |
| genshi_text    | 22.5 ms                                                | 23.5 ms: 1.04x slower                                                            |
| mako           | 10.7 ms                                                | 11.2 ms: 1.05x slower                                                            |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240406-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-cd8bea7 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 111 us: 4.67x faster                                                             |
| generators                 | 74.9 ms                                                | 29.7 ms: 2.52x faster                                                            |
| asyncio_tcp                | 875 ms                                                 | 506 ms: 1.73x faster                                                             |
| pylint                     | 476 ms                                                 | 278 ms: 1.71x faster                                                             |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                           |
| async_tree_none            | 528 ms                                                 | 355 ms: 1.49x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 334 ms: 1.47x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                             |
| comprehensions             | 23.6 us                                                | 16.7 us: 1.41x faster                                                            |
| async_tree_io              | 1.29 sec                                               | 920 ms: 1.40x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 926 ms: 1.40x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 457 ms: 1.40x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 600 ms: 1.27x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                            |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 607 ms: 1.23x faster                                                             |
| deltablue                  | 3.92 ms                                                | 3.25 ms: 1.21x faster                                                            |
| chaos                      | 71.9 ms                                                | 61.2 ms: 1.17x faster                                                            |
| coroutines                 | 27.0 ms                                                | 23.2 ms: 1.17x faster                                                            |
| richards_super             | 61.9 ms                                                | 53.1 ms: 1.17x faster                                                            |
| raytrace                   | 309 ms                                                 | 267 ms: 1.16x faster                                                             |
| gc_traversal               | 4.01 ms                                                | 3.57 ms: 1.12x faster                                                            |
| logging_simple             | 6.22 us                                                | 5.64 us: 1.10x faster                                                            |
| sqlglot_parse              | 1.43 ms                                                | 1.30 ms: 1.10x faster                                                            |
| unpickle_pure_python       | 242 us                                                 | 219 us: 1.10x faster                                                             |
| hexiom                     | 6.89 ms                                                | 6.27 ms: 1.10x faster                                                            |
| sqlglot_transpile          | 1.75 ms                                                | 1.59 ms: 1.10x faster                                                            |
| sympy_sum                  | 169 ms                                                 | 155 ms: 1.09x faster                                                             |
| logging_silent             | 111 ns                                                 | 102 ns: 1.09x faster                                                             |
| logging_format             | 6.81 us                                                | 6.27 us: 1.09x faster                                                            |
| crypto_pyaes               | 76.7 ms                                                | 70.9 ms: 1.08x faster                                                            |
| mdp                        | 2.77 sec                                               | 2.57 sec: 1.08x faster                                                           |
| sympy_str                  | 297 ms                                                 | 278 ms: 1.07x faster                                                             |
| nqueens                    | 87.9 ms                                                | 82.5 ms: 1.06x faster                                                            |
| pickle_pure_python         | 320 us                                                 | 302 us: 1.06x faster                                                             |
| sympy_integrate            | 21.5 ms                                                | 20.3 ms: 1.06x faster                                                            |
| richards                   | 49.8 ms                                                | 47.3 ms: 1.05x faster                                                            |
| deepcopy_memo              | 40.2 us                                                | 38.2 us: 1.05x faster                                                            |
| unpickle_list              | 5.21 us                                                | 4.98 us: 1.05x faster                                                            |
| regex_compile              | 141 ms                                                 | 135 ms: 1.05x faster                                                             |
| sympy_expand               | 484 ms                                                 | 464 ms: 1.05x faster                                                             |
| tomli_loads                | 2.30 sec                                               | 2.21 sec: 1.04x faster                                                           |
| tornado_http               | 98.1 ms                                                | 93.9 ms: 1.04x faster                                                            |
| go                         | 149 ms                                                 | 143 ms: 1.04x faster                                                             |
| deepcopy                   | 365 us                                                 | 352 us: 1.04x faster                                                             |
| genshi_xml                 | 53.4 ms                                                | 51.7 ms: 1.03x faster                                                            |
| scimark_monte_carlo        | 70.7 ms                                                | 68.4 ms: 1.03x faster                                                            |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.03x faster                                                             |
| fannkuch                   | 405 ms                                                 | 396 ms: 1.02x faster                                                             |
| pprint_pformat             | 1.55 sec                                               | 1.52 sec: 1.02x faster                                                           |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.92 ms: 1.02x faster                                                            |
| sqlglot_normalize          | 113 ms                                                 | 110 ms: 1.02x faster                                                             |
| deepcopy_reduce            | 3.22 us                                                | 3.15 us: 1.02x faster                                                            |
| scimark_lu                 | 116 ms                                                 | 114 ms: 1.02x faster                                                             |
| json_loads                 | 29.2 us                                                | 28.7 us: 1.02x faster                                                            |
| float                      | 78.9 ms                                                | 77.6 ms: 1.02x faster                                                            |
| nbody                      | 96.0 ms                                                | 94.4 ms: 1.02x faster                                                            |
| xml_etree_iterparse        | 108 ms                                                 | 106 ms: 1.01x faster                                                             |
| spectral_norm              | 108 ms                                                 | 107 ms: 1.01x faster                                                             |
| bench_thread_pool          | 834 us                                                 | 828 us: 1.01x faster                                                             |
| pprint_safe_repr           | 747 ms                                                 | 741 ms: 1.01x faster                                                             |
| sqlglot_optimize           | 55.3 ms                                                | 54.9 ms: 1.01x faster                                                            |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                            |
| pidigits                   | 194 ms                                                 | 194 ms: 1.00x faster                                                             |
| meteor_contest             | 109 ms                                                 | 109 ms: 1.00x slower                                                             |
| pycparser                  | 1.19 sec                                               | 1.20 sec: 1.01x slower                                                           |
| 2to3                       | 264 ms                                                 | 268 ms: 1.02x slower                                                             |
| pickle_dict                | 34.6 us                                                | 35.5 us: 1.03x slower                                                            |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                             |
| json                       | 5.24 ms                                                | 5.42 ms: 1.03x slower                                                            |
| thrift                     | 784 us                                                 | 814 us: 1.04x slower                                                             |
| chameleon                  | 6.70 ms                                                | 6.97 ms: 1.04x slower                                                            |
| pyflate                    | 434 ms                                                 | 452 ms: 1.04x slower                                                             |
| aiohttp                    | 1.12 ms                                                | 1.16 ms: 1.04x slower                                                            |
| genshi_text                | 22.5 ms                                                | 23.5 ms: 1.04x slower                                                            |
| docutils                   | 2.66 sec                                               | 2.80 sec: 1.05x slower                                                           |
| mako                       | 10.7 ms                                                | 11.2 ms: 1.05x slower                                                            |
| dulwich_log                | 64.6 ms                                                | 67.9 ms: 1.05x slower                                                            |
| html5lib                   | 64.8 ms                                                | 68.2 ms: 1.05x slower                                                            |
| gunicorn                   | 1.20 ms                                                | 1.26 ms: 1.05x slower                                                            |
| xml_etree_process          | 56.9 ms                                                | 60.0 ms: 1.05x slower                                                            |
| scimark_sor                | 121 ms                                                 | 130 ms: 1.07x slower                                                             |
| xml_etree_generate         | 81.1 ms                                                | 86.7 ms: 1.07x slower                                                            |
| pickle                     | 11.0 us                                                | 11.8 us: 1.07x slower                                                            |
| mypy2                      | 686 ms                                                 | 738 ms: 1.08x slower                                                             |
| regex_effbot               | 3.51 ms                                                | 3.81 ms: 1.09x slower                                                            |
| scimark_fft                | 345 ms                                                 | 377 ms: 1.09x slower                                                             |
| unpickle                   | 13.8 us                                                | 15.4 us: 1.11x slower                                                            |
| regex_dna                  | 205 ms                                                 | 230 ms: 1.12x slower                                                             |
| pickle_list                | 4.59 us                                                | 5.18 us: 1.13x slower                                                            |
| regex_v8                   | 22.9 ms                                                | 26.2 ms: 1.14x slower                                                            |
| sqlite_synth               | 2.57 us                                                | 2.95 us: 1.15x slower                                                            |
| async_generators           | 374 ms                                                 | 439 ms: 1.17x slower                                                             |
| create_gc_cycles           | 1.43 ms                                                | 1.74 ms: 1.21x slower                                                            |
| telco                      | 6.86 ms                                                | 8.46 ms: 1.23x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.6 ms: 1.23x slower                                                            |
| coverage                   | 78.8 ms                                                | 97.7 ms: 1.24x slower                                                            |
| python_startup_no_site     | 6.01 ms                                                | 8.99 ms: 1.50x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                                     |

Benchmark hidden because not significant (2): pathlib, dask
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.80% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x