# Results vs. 3.11.0

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 881df50
- commit date: 2024-05-23
- overall geometric mean: 1.06x faster
- HPT reliability: 98.18%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 271 ms: 1.02x slower                                                            |
| chameleon      | 6.70 ms                                                | 7.03 ms: 1.05x slower                                                           |
| docutils       | 2.66 sec                                               | 2.78 sec: 1.05x slower                                                          |
| html5lib       | 64.8 ms                                                | 67.2 ms: 1.04x slower                                                           |
| tornado_http   | 98.1 ms                                                | 94.1 ms: 1.04x faster                                                           |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 349 ms: 1.41x faster                                                            |
| async_tree_memoization_tg  | 626 ms                                                 | 451 ms: 1.39x faster                                                            |
| async_tree_none            | 528 ms                                                 | 383 ms: 1.38x faster                                                            |
| async_tree_io              | 1.29 sec                                               | 933 ms: 1.38x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 464 ms: 1.38x faster                                                            |
| async_tree_io_tg           | 1.29 sec                                               | 950 ms: 1.36x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 583 ms: 1.31x faster                                                            |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 613 ms: 1.22x faster                                                            |
| Geometric mean             | (ref)                                                  | 1.35x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 191 ms: 1.02x faster                                                            |
| float          | 78.9 ms                                                | 78.5 ms: 1.01x faster                                                           |
| nbody          | 96.0 ms                                                | 97.1 ms: 1.01x slower                                                           |
| Geometric mean | (ref)                                                  | 1.00x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 133 ms: 1.06x faster                                                            |
| regex_v8       | 22.9 ms                                                | 24.2 ms: 1.06x slower                                                           |
| regex_dna      | 205 ms                                                 | 221 ms: 1.08x slower                                                            |
| regex_effbot   | 3.51 ms                                                | 3.85 ms: 1.10x slower                                                           |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                           |
| unpickle_pure_python | 242 us                                                 | 222 us: 1.09x faster                                                            |
| tomli_loads          | 2.30 sec                                               | 2.18 sec: 1.06x faster                                                          |
| pickle_pure_python   | 320 us                                                 | 309 us: 1.04x faster                                                            |
| xml_etree_parse      | 164 ms                                                 | 161 ms: 1.02x faster                                                            |
| xml_etree_iterparse  | 108 ms                                                 | 106 ms: 1.02x faster                                                            |
| unpickle_list        | 5.21 us                                                | 5.35 us: 1.03x slower                                                           |
| pickle_dict          | 34.6 us                                                | 35.9 us: 1.04x slower                                                           |
| xml_etree_process    | 56.9 ms                                                | 60.0 ms: 1.05x slower                                                           |
| xml_etree_generate   | 81.1 ms                                                | 85.8 ms: 1.06x slower                                                           |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                                           |
| unpickle             | 13.8 us                                                | 15.2 us: 1.10x slower                                                           |
| pickle_list          | 4.59 us                                                | 5.19 us: 1.13x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.00x slower                                                                    |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.11 ms: 1.18x slower                                                           |
| python_startup         | 8.56 ms                                                | 10.4 ms: 1.22x slower                                                           |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 50.9 ms: 1.05x faster                                                           |
| genshi_text     | 22.5 ms                                                | 23.1 ms: 1.03x slower                                                           |
| django_template | 33.5 ms                                                | 34.7 ms: 1.04x slower                                                           |
| mako            | 10.7 ms                                                | 11.1 ms: 1.05x slower                                                           |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 163 us: 3.19x faster                                                            |
| generators                 | 74.9 ms                                                | 29.7 ms: 2.52x faster                                                           |
| asyncio_tcp                | 875 ms                                                 | 509 ms: 1.72x faster                                                            |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                          |
| pylint                     | 476 ms                                                 | 318 ms: 1.50x faster                                                            |
| comprehensions             | 23.6 us                                                | 16.5 us: 1.43x faster                                                           |
| async_tree_none_tg         | 491 ms                                                 | 349 ms: 1.41x faster                                                            |
| async_tree_memoization_tg  | 626 ms                                                 | 451 ms: 1.39x faster                                                            |
| async_tree_none            | 528 ms                                                 | 383 ms: 1.38x faster                                                            |
| async_tree_io              | 1.29 sec                                               | 933 ms: 1.38x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 464 ms: 1.38x faster                                                            |
| async_tree_io_tg           | 1.29 sec                                               | 950 ms: 1.36x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 583 ms: 1.31x faster                                                            |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                           |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 613 ms: 1.22x faster                                                            |
| deltablue                  | 3.92 ms                                                | 3.23 ms: 1.21x faster                                                           |
| chaos                      | 71.9 ms                                                | 61.7 ms: 1.16x faster                                                           |
| richards_super             | 61.9 ms                                                | 54.1 ms: 1.14x faster                                                           |
| pathlib                    | 18.5 ms                                                | 16.6 ms: 1.12x faster                                                           |
| raytrace                   | 309 ms                                                 | 277 ms: 1.11x faster                                                            |
| coroutines                 | 27.0 ms                                                | 24.3 ms: 1.11x faster                                                           |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.10x faster                                                           |
| sympy_sum                  | 169 ms                                                 | 155 ms: 1.09x faster                                                            |
| unpickle_pure_python       | 242 us                                                 | 222 us: 1.09x faster                                                            |
| hexiom                     | 6.89 ms                                                | 6.32 ms: 1.09x faster                                                           |
| sqlglot_transpile          | 1.75 ms                                                | 1.62 ms: 1.08x faster                                                           |
| nqueens                    | 87.9 ms                                                | 81.3 ms: 1.08x faster                                                           |
| logging_silent             | 111 ns                                                 | 104 ns: 1.07x faster                                                            |
| logging_simple             | 6.22 us                                                | 5.82 us: 1.07x faster                                                           |
| sympy_str                  | 297 ms                                                 | 279 ms: 1.07x faster                                                            |
| logging_format             | 6.81 us                                                | 6.39 us: 1.07x faster                                                           |
| regex_compile              | 141 ms                                                 | 133 ms: 1.06x faster                                                            |
| gc_traversal               | 4.01 ms                                                | 3.78 ms: 1.06x faster                                                           |
| crypto_pyaes               | 76.7 ms                                                | 72.4 ms: 1.06x faster                                                           |
| tomli_loads                | 2.30 sec                                               | 2.18 sec: 1.06x faster                                                          |
| sympy_integrate            | 21.5 ms                                                | 20.4 ms: 1.05x faster                                                           |
| genshi_xml                 | 53.4 ms                                                | 50.9 ms: 1.05x faster                                                           |
| mdp                        | 2.77 sec                                               | 2.64 sec: 1.05x faster                                                          |
| go                         | 149 ms                                                 | 142 ms: 1.04x faster                                                            |
| tornado_http               | 98.1 ms                                                | 94.1 ms: 1.04x faster                                                           |
| richards                   | 49.8 ms                                                | 47.9 ms: 1.04x faster                                                           |
| pickle_pure_python         | 320 us                                                 | 309 us: 1.04x faster                                                            |
| sympy_expand               | 484 ms                                                 | 468 ms: 1.03x faster                                                            |
| sqlglot_normalize          | 113 ms                                                 | 109 ms: 1.03x faster                                                            |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.02x faster                                                          |
| xml_etree_parse            | 164 ms                                                 | 161 ms: 1.02x faster                                                            |
| pidigits                   | 194 ms                                                 | 191 ms: 1.02x faster                                                            |
| pprint_pformat             | 1.55 sec                                               | 1.53 sec: 1.02x faster                                                          |
| xml_etree_iterparse        | 108 ms                                                 | 106 ms: 1.02x faster                                                            |
| scimark_monte_carlo        | 70.7 ms                                                | 69.6 ms: 1.02x faster                                                           |
| sqlglot_optimize           | 55.3 ms                                                | 54.6 ms: 1.01x faster                                                           |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                           |
| float                      | 78.9 ms                                                | 78.5 ms: 1.01x faster                                                           |
| bench_thread_pool          | 834 us                                                 | 831 us: 1.00x faster                                                            |
| meteor_contest             | 109 ms                                                 | 109 ms: 1.00x slower                                                            |
| fannkuch                   | 405 ms                                                 | 410 ms: 1.01x slower                                                            |
| nbody                      | 96.0 ms                                                | 97.1 ms: 1.01x slower                                                           |
| dask                       | 365 ms                                                 | 370 ms: 1.01x slower                                                            |
| json                       | 5.24 ms                                                | 5.32 ms: 1.01x slower                                                           |
| dulwich_log                | 64.6 ms                                                | 65.6 ms: 1.02x slower                                                           |
| deepcopy_reduce            | 3.22 us                                                | 3.27 us: 1.02x slower                                                           |
| scimark_lu                 | 116 ms                                                 | 118 ms: 1.02x slower                                                            |
| 2to3                       | 264 ms                                                 | 271 ms: 1.02x slower                                                            |
| unpickle_list              | 5.21 us                                                | 5.35 us: 1.03x slower                                                           |
| genshi_text                | 22.5 ms                                                | 23.1 ms: 1.03x slower                                                           |
| asyncio_websockets         | 550 ms                                                 | 569 ms: 1.03x slower                                                            |
| django_template            | 33.5 ms                                                | 34.7 ms: 1.04x slower                                                           |
| html5lib                   | 64.8 ms                                                | 67.2 ms: 1.04x slower                                                           |
| thrift                     | 784 us                                                 | 814 us: 1.04x slower                                                            |
| pickle_dict                | 34.6 us                                                | 35.9 us: 1.04x slower                                                           |
| docutils                   | 2.66 sec                                               | 2.78 sec: 1.05x slower                                                          |
| mako                       | 10.7 ms                                                | 11.1 ms: 1.05x slower                                                           |
| chameleon                  | 6.70 ms                                                | 7.03 ms: 1.05x slower                                                           |
| xml_etree_process          | 56.9 ms                                                | 60.0 ms: 1.05x slower                                                           |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.31 ms: 1.06x slower                                                           |
| xml_etree_generate         | 81.1 ms                                                | 85.8 ms: 1.06x slower                                                           |
| regex_v8                   | 22.9 ms                                                | 24.2 ms: 1.06x slower                                                           |
| regex_dna                  | 205 ms                                                 | 221 ms: 1.08x slower                                                            |
| pyflate                    | 434 ms                                                 | 472 ms: 1.09x slower                                                            |
| pickle                     | 11.0 us                                                | 12.0 us: 1.09x slower                                                           |
| scimark_sor                | 121 ms                                                 | 133 ms: 1.09x slower                                                            |
| regex_effbot               | 3.51 ms                                                | 3.85 ms: 1.10x slower                                                           |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.10x slower                                                           |
| scimark_fft                | 345 ms                                                 | 390 ms: 1.13x slower                                                            |
| pickle_list                | 4.59 us                                                | 5.19 us: 1.13x slower                                                           |
| sqlite_synth               | 2.57 us                                                | 2.96 us: 1.15x slower                                                           |
| coverage                   | 78.8 ms                                                | 92.4 ms: 1.17x slower                                                           |
| python_startup_no_site     | 6.01 ms                                                | 7.11 ms: 1.18x slower                                                           |
| async_generators           | 374 ms                                                 | 444 ms: 1.19x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.4 ms: 1.22x slower                                                           |
| flaskblogging              | 7.28 ms                                                | 8.90 ms: 1.22x slower                                                           |
| create_gc_cycles           | 1.43 ms                                                | 1.78 ms: 1.24x slower                                                           |
| telco                      | 6.86 ms                                                | 8.57 ms: 1.25x slower                                                           |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                    |

Benchmark hidden because not significant (5): spectral_norm, json_loads, deepcopy_memo, deepcopy, pprint_safe_repr
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, djangocms, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 98.18% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x