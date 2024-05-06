# Results vs. 3.11.0

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 23cf5de
- commit date: 2024-04-04
- overall geometric mean: 1.06x faster
- HPT reliability: 81.33%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 268 ms: 1.02x slower                                                             |
| chameleon      | 6.70 ms                                                | 7.00 ms: 1.04x slower                                                            |
| docutils       | 2.66 sec                                               | 2.79 sec: 1.05x slower                                                           |
| html5lib       | 64.8 ms                                                | 68.0 ms: 1.05x slower                                                            |
| tornado_http   | 98.1 ms                                                | 94.8 ms: 1.03x faster                                                            |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 352 ms: 1.50x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 333 ms: 1.47x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 440 ms: 1.42x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 918 ms: 1.40x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 927 ms: 1.40x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 461 ms: 1.38x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 601 ms: 1.27x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 608 ms: 1.23x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.38x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 199 ms: 1.02x slower                                                             |
| float          | 78.9 ms                                                | 81.7 ms: 1.04x slower                                                            |
| nbody          | 96.0 ms                                                | 118 ms: 1.23x slower                                                             |
| Geometric mean | (ref)                                                  | 1.09x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 135 ms: 1.04x faster                                                             |
| regex_effbot   | 3.51 ms                                                | 3.62 ms: 1.03x slower                                                            |
| regex_dna      | 205 ms                                                 | 220 ms: 1.08x slower                                                             |
| regex_v8       | 22.9 ms                                                | 24.8 ms: 1.08x slower                                                            |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                            |
| unpickle_pure_python | 242 us                                                 | 219 us: 1.11x faster                                                             |
| pickle_pure_python   | 320 us                                                 | 299 us: 1.07x faster                                                             |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.02x faster                                                             |
| json_loads           | 29.2 us                                                | 28.7 us: 1.02x faster                                                            |
| pickle_dict          | 34.6 us                                                | 34.3 us: 1.01x faster                                                            |
| unpickle_list        | 5.21 us                                                | 5.24 us: 1.00x slower                                                            |
| xml_etree_process    | 56.9 ms                                                | 60.2 ms: 1.06x slower                                                            |
| pickle               | 11.0 us                                                | 11.6 us: 1.06x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 87.5 ms: 1.08x slower                                                            |
| pickle_list          | 4.59 us                                                | 5.04 us: 1.10x slower                                                            |
| unpickle             | 13.8 us                                                | 15.2 us: 1.10x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (2): xml_etree_iterparse, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.6 ms: 1.24x slower                                                            |
| python_startup_no_site | 6.01 ms                                                | 8.99 ms: 1.50x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.36x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml     | 53.4 ms                                                | 51.5 ms: 1.04x faster                                                            |
| mako           | 10.7 ms                                                | 11.0 ms: 1.03x slower                                                            |
| genshi_text    | 22.5 ms                                                | 23.7 ms: 1.05x slower                                                            |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 114 us: 4.56x faster                                                             |
| generators                 | 74.9 ms                                                | 29.6 ms: 2.53x faster                                                            |
| asyncio_tcp                | 875 ms                                                 | 506 ms: 1.73x faster                                                             |
| pylint                     | 476 ms                                                 | 278 ms: 1.71x faster                                                             |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                           |
| async_tree_none            | 528 ms                                                 | 352 ms: 1.50x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 333 ms: 1.47x faster                                                             |
| comprehensions             | 23.6 us                                                | 16.5 us: 1.43x faster                                                            |
| async_tree_memoization_tg  | 626 ms                                                 | 440 ms: 1.42x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 918 ms: 1.40x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 927 ms: 1.40x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 461 ms: 1.38x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 601 ms: 1.27x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                            |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 608 ms: 1.23x faster                                                             |
| deltablue                  | 3.92 ms                                                | 3.27 ms: 1.20x faster                                                            |
| richards_super             | 61.9 ms                                                | 53.1 ms: 1.17x faster                                                            |
| coroutines                 | 27.0 ms                                                | 23.9 ms: 1.13x faster                                                            |
| logging_silent             | 111 ns                                                 | 100 ns: 1.11x faster                                                             |
| sqlglot_parse              | 1.43 ms                                                | 1.29 ms: 1.11x faster                                                            |
| unpickle_pure_python       | 242 us                                                 | 219 us: 1.11x faster                                                             |
| raytrace                   | 309 ms                                                 | 279 ms: 1.11x faster                                                             |
| sqlglot_transpile          | 1.75 ms                                                | 1.59 ms: 1.10x faster                                                            |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.09x faster                                                             |
| hexiom                     | 6.89 ms                                                | 6.39 ms: 1.08x faster                                                            |
| gc_traversal               | 4.01 ms                                                | 3.73 ms: 1.07x faster                                                            |
| pickle_pure_python         | 320 us                                                 | 299 us: 1.07x faster                                                             |
| logging_simple             | 6.22 us                                                | 5.83 us: 1.07x faster                                                            |
| sympy_str                  | 297 ms                                                 | 279 ms: 1.06x faster                                                             |
| richards                   | 49.8 ms                                                | 47.0 ms: 1.06x faster                                                            |
| sympy_integrate            | 21.5 ms                                                | 20.3 ms: 1.06x faster                                                            |
| deepcopy_memo              | 40.2 us                                                | 38.3 us: 1.05x faster                                                            |
| chaos                      | 71.9 ms                                                | 68.6 ms: 1.05x faster                                                            |
| crypto_pyaes               | 76.7 ms                                                | 73.5 ms: 1.04x faster                                                            |
| nqueens                    | 87.9 ms                                                | 84.2 ms: 1.04x faster                                                            |
| regex_compile              | 141 ms                                                 | 135 ms: 1.04x faster                                                             |
| logging_format             | 6.81 us                                                | 6.54 us: 1.04x faster                                                            |
| genshi_xml                 | 53.4 ms                                                | 51.5 ms: 1.04x faster                                                            |
| tornado_http               | 98.1 ms                                                | 94.8 ms: 1.03x faster                                                            |
| deepcopy                   | 365 us                                                 | 353 us: 1.03x faster                                                             |
| pprint_pformat             | 1.55 sec                                               | 1.51 sec: 1.03x faster                                                           |
| sympy_expand               | 484 ms                                                 | 470 ms: 1.03x faster                                                             |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.02x faster                                                             |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.02x faster                                                           |
| go                         | 149 ms                                                 | 146 ms: 1.02x faster                                                             |
| sqlglot_normalize          | 113 ms                                                 | 110 ms: 1.02x faster                                                             |
| pprint_safe_repr           | 747 ms                                                 | 734 ms: 1.02x faster                                                             |
| json_loads                 | 29.2 us                                                | 28.7 us: 1.02x faster                                                            |
| sqlglot_optimize           | 55.3 ms                                                | 54.9 ms: 1.01x faster                                                            |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                            |
| pickle_dict                | 34.6 us                                                | 34.3 us: 1.01x faster                                                            |
| bench_thread_pool          | 834 us                                                 | 829 us: 1.01x faster                                                             |
| unpickle_list              | 5.21 us                                                | 5.24 us: 1.00x slower                                                            |
| mdp                        | 2.77 sec                                               | 2.80 sec: 1.01x slower                                                           |
| 2to3                       | 264 ms                                                 | 268 ms: 1.02x slower                                                             |
| pathlib                    | 18.5 ms                                                | 18.8 ms: 1.02x slower                                                            |
| fannkuch                   | 405 ms                                                 | 413 ms: 1.02x slower                                                             |
| pidigits                   | 194 ms                                                 | 199 ms: 1.02x slower                                                             |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.02x slower                                                             |
| thrift                     | 784 us                                                 | 808 us: 1.03x slower                                                             |
| regex_effbot               | 3.51 ms                                                | 3.62 ms: 1.03x slower                                                            |
| mako                       | 10.7 ms                                                | 11.0 ms: 1.03x slower                                                            |
| float                      | 78.9 ms                                                | 81.7 ms: 1.04x slower                                                            |
| scimark_lu                 | 116 ms                                                 | 121 ms: 1.04x slower                                                             |
| chameleon                  | 6.70 ms                                                | 7.00 ms: 1.04x slower                                                            |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                            |
| scimark_monte_carlo        | 70.7 ms                                                | 74.0 ms: 1.05x slower                                                            |
| docutils                   | 2.66 sec                                               | 2.79 sec: 1.05x slower                                                           |
| html5lib                   | 64.8 ms                                                | 68.0 ms: 1.05x slower                                                            |
| dulwich_log                | 64.6 ms                                                | 67.8 ms: 1.05x slower                                                            |
| genshi_text                | 22.5 ms                                                | 23.7 ms: 1.05x slower                                                            |
| json                       | 5.24 ms                                                | 5.51 ms: 1.05x slower                                                            |
| gunicorn                   | 1.20 ms                                                | 1.26 ms: 1.05x slower                                                            |
| xml_etree_process          | 56.9 ms                                                | 60.2 ms: 1.06x slower                                                            |
| pickle                     | 11.0 us                                                | 11.6 us: 1.06x slower                                                            |
| regex_dna                  | 205 ms                                                 | 220 ms: 1.08x slower                                                             |
| mypy2                      | 686 ms                                                 | 739 ms: 1.08x slower                                                             |
| xml_etree_generate         | 81.1 ms                                                | 87.5 ms: 1.08x slower                                                            |
| regex_v8                   | 22.9 ms                                                | 24.8 ms: 1.08x slower                                                            |
| pickle_list                | 4.59 us                                                | 5.04 us: 1.10x slower                                                            |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.10x slower                                                            |
| pyflate                    | 434 ms                                                 | 480 ms: 1.11x slower                                                             |
| scimark_sor                | 121 ms                                                 | 137 ms: 1.13x slower                                                             |
| sqlite_synth               | 2.57 us                                                | 2.93 us: 1.14x slower                                                            |
| async_generators           | 374 ms                                                 | 442 ms: 1.18x slower                                                             |
| create_gc_cycles           | 1.43 ms                                                | 1.73 ms: 1.21x slower                                                            |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 6.14 ms: 1.22x slower                                                            |
| nbody                      | 96.0 ms                                                | 118 ms: 1.23x slower                                                             |
| python_startup             | 8.56 ms                                                | 10.6 ms: 1.24x slower                                                            |
| scimark_fft                | 345 ms                                                 | 428 ms: 1.24x slower                                                             |
| telco                      | 6.86 ms                                                | 8.56 ms: 1.25x slower                                                            |
| coverage                   | 78.8 ms                                                | 98.3 ms: 1.25x slower                                                            |
| spectral_norm              | 108 ms                                                 | 138 ms: 1.27x slower                                                             |
| python_startup_no_site     | 6.01 ms                                                | 8.99 ms: 1.50x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                     |

Benchmark hidden because not significant (5): xml_etree_iterparse, tomli_loads, deepcopy_reduce, meteor_contest, dask
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 81.33% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x