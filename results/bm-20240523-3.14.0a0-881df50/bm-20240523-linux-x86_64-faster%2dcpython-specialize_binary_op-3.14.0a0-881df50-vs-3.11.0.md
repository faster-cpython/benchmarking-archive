# Results vs. 3.11.0

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 881df50
- commit date: 2024-05-23
- overall geometric mean: 1.06x faster
- HPT reliability: 99.78%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 271 ms: 1.02x slower                                                            |
| chameleon      | 6.70 ms                                                | 6.99 ms: 1.04x slower                                                           |
| docutils       | 2.66 sec                                               | 2.79 sec: 1.05x slower                                                          |
| html5lib       | 64.8 ms                                                | 66.5 ms: 1.03x slower                                                           |
| tornado_http   | 98.1 ms                                                | 94.5 ms: 1.04x faster                                                           |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 347 ms: 1.42x faster                                                            |
| async_tree_memoization_tg  | 626 ms                                                 | 448 ms: 1.40x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 460 ms: 1.39x faster                                                            |
| async_tree_none            | 528 ms                                                 | 382 ms: 1.38x faster                                                            |
| async_tree_io              | 1.29 sec                                               | 942 ms: 1.37x faster                                                            |
| async_tree_io_tg           | 1.29 sec                                               | 965 ms: 1.34x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 581 ms: 1.31x faster                                                            |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 614 ms: 1.22x faster                                                            |
| Geometric mean             | (ref)                                                  | 1.35x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                                            |
| nbody          | 96.0 ms                                                | 94.3 ms: 1.02x faster                                                           |
| float          | 78.9 ms                                                | 78.2 ms: 1.01x faster                                                           |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 134 ms: 1.06x faster                                                            |
| regex_effbot   | 3.51 ms                                                | 3.94 ms: 1.12x slower                                                           |
| regex_v8       | 22.9 ms                                                | 26.0 ms: 1.13x slower                                                           |
| regex_dna      | 205 ms                                                 | 233 ms: 1.14x slower                                                            |
| Geometric mean | (ref)                                                  | 1.08x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                           |
| unpickle_pure_python | 242 us                                                 | 218 us: 1.11x faster                                                            |
| tomli_loads          | 2.30 sec                                               | 2.19 sec: 1.05x faster                                                          |
| pickle_pure_python   | 320 us                                                 | 304 us: 1.05x faster                                                            |
| xml_etree_parse      | 164 ms                                                 | 159 ms: 1.03x faster                                                            |
| xml_etree_iterparse  | 108 ms                                                 | 106 ms: 1.02x faster                                                            |
| json_loads           | 29.2 us                                                | 28.7 us: 1.02x faster                                                           |
| pickle_dict          | 34.6 us                                                | 35.6 us: 1.03x slower                                                           |
| unpickle_list        | 5.21 us                                                | 5.48 us: 1.05x slower                                                           |
| xml_etree_process    | 56.9 ms                                                | 60.2 ms: 1.06x slower                                                           |
| xml_etree_generate   | 81.1 ms                                                | 86.5 ms: 1.07x slower                                                           |
| pickle               | 11.0 us                                                | 11.9 us: 1.08x slower                                                           |
| pickle_list          | 4.59 us                                                | 5.15 us: 1.12x slower                                                           |
| unpickle             | 13.8 us                                                | 15.6 us: 1.13x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.00x slower                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.09 ms: 1.18x slower                                                           |
| python_startup         | 8.56 ms                                                | 10.4 ms: 1.21x slower                                                           |
| Geometric mean         | (ref)                                                  | 1.19x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 51.2 ms: 1.04x faster                                                           |
| mako            | 10.7 ms                                                | 10.9 ms: 1.03x slower                                                           |
| genshi_text     | 22.5 ms                                                | 23.2 ms: 1.03x slower                                                           |
| django_template | 33.5 ms                                                | 35.3 ms: 1.05x slower                                                           |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 163 us: 3.19x faster                                                            |
| generators                 | 74.9 ms                                                | 29.3 ms: 2.55x faster                                                           |
| asyncio_tcp                | 875 ms                                                 | 503 ms: 1.74x faster                                                            |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                          |
| pylint                     | 476 ms                                                 | 318 ms: 1.50x faster                                                            |
| async_tree_none_tg         | 491 ms                                                 | 347 ms: 1.42x faster                                                            |
| comprehensions             | 23.6 us                                                | 16.8 us: 1.41x faster                                                           |
| async_tree_memoization_tg  | 626 ms                                                 | 448 ms: 1.40x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 460 ms: 1.39x faster                                                            |
| async_tree_none            | 528 ms                                                 | 382 ms: 1.38x faster                                                            |
| async_tree_io              | 1.29 sec                                               | 942 ms: 1.37x faster                                                            |
| async_tree_io_tg           | 1.29 sec                                               | 965 ms: 1.34x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 581 ms: 1.31x faster                                                            |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                           |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 614 ms: 1.22x faster                                                            |
| deltablue                  | 3.92 ms                                                | 3.28 ms: 1.19x faster                                                           |
| chaos                      | 71.9 ms                                                | 61.5 ms: 1.17x faster                                                           |
| coroutines                 | 27.0 ms                                                | 23.9 ms: 1.13x faster                                                           |
| richards_super             | 61.9 ms                                                | 54.9 ms: 1.13x faster                                                           |
| unpickle_pure_python       | 242 us                                                 | 218 us: 1.11x faster                                                            |
| pathlib                    | 18.5 ms                                                | 16.8 ms: 1.10x faster                                                           |
| raytrace                   | 309 ms                                                 | 280 ms: 1.10x faster                                                            |
| logging_silent             | 111 ns                                                 | 101 ns: 1.10x faster                                                            |
| hexiom                     | 6.89 ms                                                | 6.29 ms: 1.10x faster                                                           |
| sympy_sum                  | 169 ms                                                 | 154 ms: 1.09x faster                                                            |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.09x faster                                                           |
| sqlglot_transpile          | 1.75 ms                                                | 1.62 ms: 1.08x faster                                                           |
| nqueens                    | 87.9 ms                                                | 81.6 ms: 1.08x faster                                                           |
| gc_traversal               | 4.01 ms                                                | 3.72 ms: 1.08x faster                                                           |
| logging_simple             | 6.22 us                                                | 5.80 us: 1.07x faster                                                           |
| crypto_pyaes               | 76.7 ms                                                | 71.7 ms: 1.07x faster                                                           |
| logging_format             | 6.81 us                                                | 6.41 us: 1.06x faster                                                           |
| sympy_str                  | 297 ms                                                 | 281 ms: 1.06x faster                                                            |
| regex_compile              | 141 ms                                                 | 134 ms: 1.06x faster                                                            |
| mdp                        | 2.77 sec                                               | 2.63 sec: 1.06x faster                                                          |
| tomli_loads                | 2.30 sec                                               | 2.19 sec: 1.05x faster                                                          |
| sympy_integrate            | 21.5 ms                                                | 20.4 ms: 1.05x faster                                                           |
| pickle_pure_python         | 320 us                                                 | 304 us: 1.05x faster                                                            |
| genshi_xml                 | 53.4 ms                                                | 51.2 ms: 1.04x faster                                                           |
| pprint_pformat             | 1.55 sec                                               | 1.49 sec: 1.04x faster                                                          |
| tornado_http               | 98.1 ms                                                | 94.5 ms: 1.04x faster                                                           |
| sympy_expand               | 484 ms                                                 | 469 ms: 1.03x faster                                                            |
| xml_etree_parse            | 164 ms                                                 | 159 ms: 1.03x faster                                                            |
| go                         | 149 ms                                                 | 144 ms: 1.03x faster                                                            |
| richards                   | 49.8 ms                                                | 48.4 ms: 1.03x faster                                                           |
| sqlglot_normalize          | 113 ms                                                 | 110 ms: 1.02x faster                                                            |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                                            |
| pprint_safe_repr           | 747 ms                                                 | 730 ms: 1.02x faster                                                            |
| xml_etree_iterparse        | 108 ms                                                 | 106 ms: 1.02x faster                                                            |
| json_loads                 | 29.2 us                                                | 28.7 us: 1.02x faster                                                           |
| nbody                      | 96.0 ms                                                | 94.3 ms: 1.02x faster                                                           |
| spectral_norm              | 108 ms                                                 | 107 ms: 1.01x faster                                                            |
| deepcopy_memo              | 40.2 us                                                | 39.7 us: 1.01x faster                                                           |
| fannkuch                   | 405 ms                                                 | 401 ms: 1.01x faster                                                            |
| sqlglot_optimize           | 55.3 ms                                                | 54.8 ms: 1.01x faster                                                           |
| float                      | 78.9 ms                                                | 78.2 ms: 1.01x faster                                                           |
| scimark_monte_carlo        | 70.7 ms                                                | 70.3 ms: 1.01x faster                                                           |
| deepcopy                   | 365 us                                                 | 367 us: 1.01x slower                                                            |
| scimark_lu                 | 116 ms                                                 | 117 ms: 1.01x slower                                                            |
| deepcopy_reduce            | 3.22 us                                                | 3.25 us: 1.01x slower                                                           |
| dulwich_log                | 64.6 ms                                                | 65.6 ms: 1.02x slower                                                           |
| json                       | 5.24 ms                                                | 5.33 ms: 1.02x slower                                                           |
| pycparser                  | 1.19 sec                                               | 1.21 sec: 1.02x slower                                                          |
| scimark_sor                | 121 ms                                                 | 124 ms: 1.02x slower                                                            |
| 2to3                       | 264 ms                                                 | 271 ms: 1.02x slower                                                            |
| mako                       | 10.7 ms                                                | 10.9 ms: 1.03x slower                                                           |
| html5lib                   | 64.8 ms                                                | 66.5 ms: 1.03x slower                                                           |
| pickle_dict                | 34.6 us                                                | 35.6 us: 1.03x slower                                                           |
| genshi_text                | 22.5 ms                                                | 23.2 ms: 1.03x slower                                                           |
| asyncio_websockets         | 550 ms                                                 | 569 ms: 1.03x slower                                                            |
| thrift                     | 784 us                                                 | 817 us: 1.04x slower                                                            |
| chameleon                  | 6.70 ms                                                | 6.99 ms: 1.04x slower                                                           |
| docutils                   | 2.66 sec                                               | 2.79 sec: 1.05x slower                                                          |
| unpickle_list              | 5.21 us                                                | 5.48 us: 1.05x slower                                                           |
| django_template            | 33.5 ms                                                | 35.3 ms: 1.05x slower                                                           |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.31 ms: 1.06x slower                                                           |
| xml_etree_process          | 56.9 ms                                                | 60.2 ms: 1.06x slower                                                           |
| pyflate                    | 434 ms                                                 | 461 ms: 1.06x slower                                                            |
| xml_etree_generate         | 81.1 ms                                                | 86.5 ms: 1.07x slower                                                           |
| pickle                     | 11.0 us                                                | 11.9 us: 1.08x slower                                                           |
| pickle_list                | 4.59 us                                                | 5.15 us: 1.12x slower                                                           |
| regex_effbot               | 3.51 ms                                                | 3.94 ms: 1.12x slower                                                           |
| unpickle                   | 13.8 us                                                | 15.6 us: 1.13x slower                                                           |
| scimark_fft                | 345 ms                                                 | 391 ms: 1.13x slower                                                            |
| regex_v8                   | 22.9 ms                                                | 26.0 ms: 1.13x slower                                                           |
| regex_dna                  | 205 ms                                                 | 233 ms: 1.14x slower                                                            |
| sqlite_synth               | 2.57 us                                                | 2.98 us: 1.16x slower                                                           |
| coverage                   | 78.8 ms                                                | 92.1 ms: 1.17x slower                                                           |
| python_startup_no_site     | 6.01 ms                                                | 7.09 ms: 1.18x slower                                                           |
| async_generators           | 374 ms                                                 | 441 ms: 1.18x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.4 ms: 1.21x slower                                                           |
| flaskblogging              | 7.28 ms                                                | 8.96 ms: 1.23x slower                                                           |
| telco                      | 6.86 ms                                                | 8.46 ms: 1.23x slower                                                           |
| create_gc_cycles           | 1.43 ms                                                | 1.78 ms: 1.24x slower                                                           |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                    |

Benchmark hidden because not significant (4): bench_mp_pool, meteor_contest, bench_thread_pool, dask
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, djangocms, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.78% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x