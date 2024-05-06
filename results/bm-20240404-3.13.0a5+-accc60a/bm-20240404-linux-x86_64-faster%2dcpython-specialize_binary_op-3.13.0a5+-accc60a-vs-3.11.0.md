# Results vs. 3.11.0

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: accc60a
- commit date: 2024-04-04
- overall geometric mean: 1.06x faster
- HPT reliability: 90.99%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 268 ms: 1.02x slower                                                             |
| chameleon      | 6.70 ms                                                | 6.96 ms: 1.04x slower                                                            |
| docutils       | 2.66 sec                                               | 2.78 sec: 1.05x slower                                                           |
| html5lib       | 64.8 ms                                                | 68.2 ms: 1.05x slower                                                            |
| tornado_http   | 98.1 ms                                                | 94.3 ms: 1.04x faster                                                            |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 350 ms: 1.51x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 333 ms: 1.47x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 918 ms: 1.40x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 928 ms: 1.39x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 459 ms: 1.39x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 602 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 608 ms: 1.23x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.38x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 195 ms: 1.00x slower                                                             |
| float          | 78.9 ms                                                | 81.7 ms: 1.04x slower                                                            |
| nbody          | 96.0 ms                                                | 127 ms: 1.32x slower                                                             |
| Geometric mean | (ref)                                                  | 1.11x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 135 ms: 1.05x faster                                                             |
| regex_effbot   | 3.51 ms                                                | 3.66 ms: 1.04x slower                                                            |
| regex_dna      | 205 ms                                                 | 227 ms: 1.11x slower                                                             |
| regex_v8       | 22.9 ms                                                | 25.4 ms: 1.11x slower                                                            |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                            |
| unpickle_pure_python | 242 us                                                 | 219 us: 1.11x faster                                                             |
| pickle_pure_python   | 320 us                                                 | 297 us: 1.08x faster                                                             |
| unpickle_list        | 5.21 us                                                | 5.09 us: 1.02x faster                                                            |
| json_loads           | 29.2 us                                                | 28.5 us: 1.02x faster                                                            |
| xml_etree_parse      | 164 ms                                                 | 161 ms: 1.02x faster                                                             |
| tomli_loads          | 2.30 sec                                               | 2.26 sec: 1.02x faster                                                           |
| xml_etree_iterparse  | 108 ms                                                 | 106 ms: 1.02x faster                                                             |
| pickle_dict          | 34.6 us                                                | 35.2 us: 1.02x slower                                                            |
| xml_etree_process    | 56.9 ms                                                | 61.1 ms: 1.07x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 88.6 ms: 1.09x slower                                                            |
| pickle               | 11.0 us                                                | 12.0 us: 1.10x slower                                                            |
| unpickle             | 13.8 us                                                | 15.6 us: 1.13x slower                                                            |
| pickle_list          | 4.59 us                                                | 5.26 us: 1.15x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.00x slower                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.6 ms: 1.24x slower                                                            |
| python_startup_no_site | 6.01 ms                                                | 9.01 ms: 1.50x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.36x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml     | 53.4 ms                                                | 51.2 ms: 1.04x faster                                                            |
| mako           | 10.7 ms                                                | 11.0 ms: 1.04x slower                                                            |
| genshi_text    | 22.5 ms                                                | 23.5 ms: 1.04x slower                                                            |
| Geometric mean | (ref)                                                  | 1.01x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 113 us: 4.59x faster                                                             |
| generators                 | 74.9 ms                                                | 29.6 ms: 2.53x faster                                                            |
| asyncio_tcp                | 875 ms                                                 | 510 ms: 1.72x faster                                                             |
| pylint                     | 476 ms                                                 | 278 ms: 1.71x faster                                                             |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                           |
| async_tree_none            | 528 ms                                                 | 350 ms: 1.51x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 333 ms: 1.47x faster                                                             |
| comprehensions             | 23.6 us                                                | 16.3 us: 1.45x faster                                                            |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 918 ms: 1.40x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 928 ms: 1.39x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 459 ms: 1.39x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 602 ms: 1.26x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                            |
| deltablue                  | 3.92 ms                                                | 3.17 ms: 1.24x faster                                                            |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 608 ms: 1.23x faster                                                             |
| richards_super             | 61.9 ms                                                | 52.0 ms: 1.19x faster                                                            |
| coroutines                 | 27.0 ms                                                | 24.1 ms: 1.12x faster                                                            |
| logging_silent             | 111 ns                                                 | 99.2 ns: 1.12x faster                                                            |
| sqlglot_parse              | 1.43 ms                                                | 1.29 ms: 1.11x faster                                                            |
| unpickle_pure_python       | 242 us                                                 | 219 us: 1.11x faster                                                             |
| raytrace                   | 309 ms                                                 | 280 ms: 1.10x faster                                                             |
| deepcopy_memo              | 40.2 us                                                | 36.5 us: 1.10x faster                                                            |
| sqlglot_transpile          | 1.75 ms                                                | 1.59 ms: 1.10x faster                                                            |
| hexiom                     | 6.89 ms                                                | 6.30 ms: 1.09x faster                                                            |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.08x faster                                                             |
| logging_simple             | 6.22 us                                                | 5.75 us: 1.08x faster                                                            |
| richards                   | 49.8 ms                                                | 46.2 ms: 1.08x faster                                                            |
| pickle_pure_python         | 320 us                                                 | 297 us: 1.08x faster                                                             |
| sympy_str                  | 297 ms                                                 | 278 ms: 1.07x faster                                                             |
| logging_format             | 6.81 us                                                | 6.43 us: 1.06x faster                                                            |
| sympy_integrate            | 21.5 ms                                                | 20.3 ms: 1.06x faster                                                            |
| deepcopy                   | 365 us                                                 | 347 us: 1.05x faster                                                             |
| nqueens                    | 87.9 ms                                                | 83.8 ms: 1.05x faster                                                            |
| mdp                        | 2.77 sec                                               | 2.65 sec: 1.05x faster                                                           |
| regex_compile              | 141 ms                                                 | 135 ms: 1.05x faster                                                             |
| genshi_xml                 | 53.4 ms                                                | 51.2 ms: 1.04x faster                                                            |
| sympy_expand               | 484 ms                                                 | 466 ms: 1.04x faster                                                             |
| tornado_http               | 98.1 ms                                                | 94.3 ms: 1.04x faster                                                            |
| pprint_pformat             | 1.55 sec                                               | 1.50 sec: 1.03x faster                                                           |
| deepcopy_reduce            | 3.22 us                                                | 3.12 us: 1.03x faster                                                            |
| sqlglot_normalize          | 113 ms                                                 | 109 ms: 1.03x faster                                                             |
| chaos                      | 71.9 ms                                                | 69.9 ms: 1.03x faster                                                            |
| unpickle_list              | 5.21 us                                                | 5.09 us: 1.02x faster                                                            |
| json_loads                 | 29.2 us                                                | 28.5 us: 1.02x faster                                                            |
| crypto_pyaes               | 76.7 ms                                                | 75.0 ms: 1.02x faster                                                            |
| xml_etree_parse            | 164 ms                                                 | 161 ms: 1.02x faster                                                             |
| pprint_safe_repr           | 747 ms                                                 | 733 ms: 1.02x faster                                                             |
| go                         | 149 ms                                                 | 146 ms: 1.02x faster                                                             |
| tomli_loads                | 2.30 sec                                               | 2.26 sec: 1.02x faster                                                           |
| xml_etree_iterparse        | 108 ms                                                 | 106 ms: 1.02x faster                                                             |
| sqlglot_optimize           | 55.3 ms                                                | 54.7 ms: 1.01x faster                                                            |
| bench_thread_pool          | 834 us                                                 | 828 us: 1.01x faster                                                             |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                            |
| gc_traversal               | 4.01 ms                                                | 4.02 ms: 1.00x slower                                                            |
| pidigits                   | 194 ms                                                 | 195 ms: 1.00x slower                                                             |
| pathlib                    | 18.5 ms                                                | 18.8 ms: 1.01x slower                                                            |
| 2to3                       | 264 ms                                                 | 268 ms: 1.02x slower                                                             |
| pickle_dict                | 34.6 us                                                | 35.2 us: 1.02x slower                                                            |
| fannkuch                   | 405 ms                                                 | 414 ms: 1.02x slower                                                             |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                                             |
| scimark_monte_carlo        | 70.7 ms                                                | 73.0 ms: 1.03x slower                                                            |
| thrift                     | 784 us                                                 | 811 us: 1.03x slower                                                             |
| float                      | 78.9 ms                                                | 81.7 ms: 1.04x slower                                                            |
| json                       | 5.24 ms                                                | 5.43 ms: 1.04x slower                                                            |
| mako                       | 10.7 ms                                                | 11.0 ms: 1.04x slower                                                            |
| chameleon                  | 6.70 ms                                                | 6.96 ms: 1.04x slower                                                            |
| genshi_text                | 22.5 ms                                                | 23.5 ms: 1.04x slower                                                            |
| scimark_lu                 | 116 ms                                                 | 121 ms: 1.04x slower                                                             |
| regex_effbot               | 3.51 ms                                                | 3.66 ms: 1.04x slower                                                            |
| aiohttp                    | 1.12 ms                                                | 1.16 ms: 1.04x slower                                                            |
| docutils                   | 2.66 sec                                               | 2.78 sec: 1.05x slower                                                           |
| dulwich_log                | 64.6 ms                                                | 67.6 ms: 1.05x slower                                                            |
| gunicorn                   | 1.20 ms                                                | 1.26 ms: 1.05x slower                                                            |
| html5lib                   | 64.8 ms                                                | 68.2 ms: 1.05x slower                                                            |
| mypy2                      | 686 ms                                                 | 736 ms: 1.07x slower                                                             |
| xml_etree_process          | 56.9 ms                                                | 61.1 ms: 1.07x slower                                                            |
| xml_etree_generate         | 81.1 ms                                                | 88.6 ms: 1.09x slower                                                            |
| pickle                     | 11.0 us                                                | 12.0 us: 1.10x slower                                                            |
| regex_dna                  | 205 ms                                                 | 227 ms: 1.11x slower                                                             |
| regex_v8                   | 22.9 ms                                                | 25.4 ms: 1.11x slower                                                            |
| scimark_sor                | 121 ms                                                 | 135 ms: 1.11x slower                                                             |
| pyflate                    | 434 ms                                                 | 486 ms: 1.12x slower                                                             |
| unpickle                   | 13.8 us                                                | 15.6 us: 1.13x slower                                                            |
| pickle_list                | 4.59 us                                                | 5.26 us: 1.15x slower                                                            |
| sqlite_synth               | 2.57 us                                                | 2.96 us: 1.15x slower                                                            |
| async_generators           | 374 ms                                                 | 444 ms: 1.19x slower                                                             |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                                            |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 6.13 ms: 1.22x slower                                                            |
| scimark_fft                | 345 ms                                                 | 427 ms: 1.24x slower                                                             |
| python_startup             | 8.56 ms                                                | 10.6 ms: 1.24x slower                                                            |
| telco                      | 6.86 ms                                                | 8.60 ms: 1.25x slower                                                            |
| coverage                   | 78.8 ms                                                | 101 ms: 1.28x slower                                                             |
| spectral_norm              | 108 ms                                                 | 141 ms: 1.31x slower                                                             |
| nbody                      | 96.0 ms                                                | 127 ms: 1.32x slower                                                             |
| python_startup_no_site     | 6.01 ms                                                | 9.01 ms: 1.50x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                     |

Benchmark hidden because not significant (3): meteor_contest, pycparser, dask
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 90.99% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x