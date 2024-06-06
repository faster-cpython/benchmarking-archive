# Results vs. 3.11.0

- fork: faster-cpython
- ref: spill_stack_pointer_
- machine: linux-x86_64
- commit hash: fb5ef8e
- commit date: 2024-06-06
- overall geometric mean: 1.06x faster
- HPT reliability: 99.36%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-faster%2dcpython-spill_stack_pointer_-3.14.0a0-fb5ef8e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 271 ms: 1.03x slower                                                            |
| docutils       | 2.66 sec                                               | 2.80 sec: 1.05x slower                                                          |
| html5lib       | 64.8 ms                                                | 67.7 ms: 1.04x slower                                                           |
| tornado_http   | 98.1 ms                                                | 94.9 ms: 1.03x faster                                                           |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-faster%2dcpython-spill_stack_pointer_-3.14.0a0-fb5ef8e |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 350 ms: 1.40x faster                                                            |
| async_tree_memoization_tg  | 626 ms                                                 | 449 ms: 1.40x faster                                                            |
| async_tree_io_tg           | 1.29 sec                                               | 952 ms: 1.36x faster                                                            |
| async_tree_none            | 528 ms                                                 | 391 ms: 1.35x faster                                                            |
| async_tree_io              | 1.29 sec                                               | 960 ms: 1.34x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 477 ms: 1.34x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 583 ms: 1.31x faster                                                            |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 621 ms: 1.21x faster                                                            |
| Geometric mean             | (ref)                                                  | 1.34x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-faster%2dcpython-spill_stack_pointer_-3.14.0a0-fb5ef8e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 92.1 ms: 1.04x faster                                                           |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                            |
| float          | 78.9 ms                                                | 79.3 ms: 1.00x slower                                                           |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-faster%2dcpython-spill_stack_pointer_-3.14.0a0-fb5ef8e |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 136 ms: 1.04x faster                                                            |
| regex_effbot   | 3.51 ms                                                | 3.67 ms: 1.05x slower                                                           |
| regex_v8       | 22.9 ms                                                | 24.8 ms: 1.09x slower                                                           |
| regex_dna      | 205 ms                                                 | 223 ms: 1.09x slower                                                            |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-faster%2dcpython-spill_stack_pointer_-3.14.0a0-fb5ef8e |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                           |
| unpickle_pure_python | 242 us                                                 | 223 us: 1.08x faster                                                            |
| pickle_pure_python   | 320 us                                                 | 302 us: 1.06x faster                                                            |
| tomli_loads          | 2.30 sec                                               | 2.19 sec: 1.05x faster                                                          |
| xml_etree_parse      | 164 ms                                                 | 158 ms: 1.04x faster                                                            |
| xml_etree_iterparse  | 108 ms                                                 | 106 ms: 1.01x faster                                                            |
| json_loads           | 29.2 us                                                | 28.8 us: 1.01x faster                                                           |
| pickle_dict          | 34.6 us                                                | 35.3 us: 1.02x slower                                                           |
| unpickle_list        | 5.21 us                                                | 5.40 us: 1.04x slower                                                           |
| xml_etree_process    | 56.9 ms                                                | 60.3 ms: 1.06x slower                                                           |
| pickle               | 11.0 us                                                | 11.7 us: 1.06x slower                                                           |
| xml_etree_generate   | 81.1 ms                                                | 87.0 ms: 1.07x slower                                                           |
| pickle_list          | 4.59 us                                                | 5.04 us: 1.10x slower                                                           |
| unpickle             | 13.8 us                                                | 15.3 us: 1.11x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-faster%2dcpython-spill_stack_pointer_-3.14.0a0-fb5ef8e |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.13 ms: 1.19x slower                                                           |
| python_startup         | 8.56 ms                                                | 10.6 ms: 1.24x slower                                                           |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-faster%2dcpython-spill_stack_pointer_-3.14.0a0-fb5ef8e |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 50.5 ms: 1.06x faster                                                           |
| mako            | 10.7 ms                                                | 10.9 ms: 1.03x slower                                                           |
| genshi_text     | 22.5 ms                                                | 23.6 ms: 1.05x slower                                                           |
| django_template | 33.5 ms                                                | 36.1 ms: 1.08x slower                                                           |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240606-linux-x86_64-faster%2dcpython-spill_stack_pointer_-3.14.0a0-fb5ef8e |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 168 us: 3.08x faster                                                            |
| generators                 | 74.9 ms                                                | 27.9 ms: 2.68x faster                                                           |
| asyncio_tcp                | 875 ms                                                 | 509 ms: 1.72x faster                                                            |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                          |
| pylint                     | 476 ms                                                 | 316 ms: 1.51x faster                                                            |
| async_tree_none_tg         | 491 ms                                                 | 350 ms: 1.40x faster                                                            |
| async_tree_memoization_tg  | 626 ms                                                 | 449 ms: 1.40x faster                                                            |
| comprehensions             | 23.6 us                                                | 16.9 us: 1.40x faster                                                           |
| async_tree_io_tg           | 1.29 sec                                               | 952 ms: 1.36x faster                                                            |
| async_tree_none            | 528 ms                                                 | 391 ms: 1.35x faster                                                            |
| async_tree_io              | 1.29 sec                                               | 960 ms: 1.34x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 477 ms: 1.34x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 583 ms: 1.31x faster                                                            |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                           |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 621 ms: 1.21x faster                                                            |
| deltablue                  | 3.92 ms                                                | 3.26 ms: 1.20x faster                                                           |
| chaos                      | 71.9 ms                                                | 60.8 ms: 1.18x faster                                                           |
| coroutines                 | 27.0 ms                                                | 23.1 ms: 1.17x faster                                                           |
| raytrace                   | 309 ms                                                 | 264 ms: 1.17x faster                                                            |
| pathlib                    | 18.5 ms                                                | 16.1 ms: 1.15x faster                                                           |
| richards_super             | 61.9 ms                                                | 54.0 ms: 1.14x faster                                                           |
| hexiom                     | 6.89 ms                                                | 6.16 ms: 1.12x faster                                                           |
| unpickle_pure_python       | 242 us                                                 | 223 us: 1.08x faster                                                            |
| nqueens                    | 87.9 ms                                                | 81.3 ms: 1.08x faster                                                           |
| sympy_sum                  | 169 ms                                                 | 157 ms: 1.08x faster                                                            |
| sqlglot_parse              | 1.43 ms                                                | 1.34 ms: 1.07x faster                                                           |
| logging_silent             | 111 ns                                                 | 104 ns: 1.07x faster                                                            |
| sqlglot_transpile          | 1.75 ms                                                | 1.64 ms: 1.07x faster                                                           |
| pickle_pure_python         | 320 us                                                 | 302 us: 1.06x faster                                                            |
| genshi_xml                 | 53.4 ms                                                | 50.5 ms: 1.06x faster                                                           |
| logging_simple             | 6.22 us                                                | 5.89 us: 1.06x faster                                                           |
| tomli_loads                | 2.30 sec                                               | 2.19 sec: 1.05x faster                                                          |
| sympy_str                  | 297 ms                                                 | 282 ms: 1.05x faster                                                            |
| sympy_integrate            | 21.5 ms                                                | 20.5 ms: 1.05x faster                                                           |
| nbody                      | 96.0 ms                                                | 92.1 ms: 1.04x faster                                                           |
| regex_compile              | 141 ms                                                 | 136 ms: 1.04x faster                                                            |
| logging_format             | 6.81 us                                                | 6.55 us: 1.04x faster                                                           |
| xml_etree_parse            | 164 ms                                                 | 158 ms: 1.04x faster                                                            |
| tornado_http               | 98.1 ms                                                | 94.9 ms: 1.03x faster                                                           |
| richards                   | 49.8 ms                                                | 48.3 ms: 1.03x faster                                                           |
| scimark_monte_carlo        | 70.7 ms                                                | 68.5 ms: 1.03x faster                                                           |
| go                         | 149 ms                                                 | 145 ms: 1.03x faster                                                            |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                            |
| mdp                        | 2.77 sec                                               | 2.71 sec: 1.02x faster                                                          |
| pprint_pformat             | 1.55 sec                                               | 1.53 sec: 1.02x faster                                                          |
| sympy_expand               | 484 ms                                                 | 476 ms: 1.02x faster                                                            |
| sqlglot_normalize          | 113 ms                                                 | 111 ms: 1.02x faster                                                            |
| deepcopy_memo              | 40.2 us                                                | 39.5 us: 1.02x faster                                                           |
| fannkuch                   | 405 ms                                                 | 399 ms: 1.02x faster                                                            |
| xml_etree_iterparse        | 108 ms                                                 | 106 ms: 1.01x faster                                                            |
| pycparser                  | 1.19 sec                                               | 1.17 sec: 1.01x faster                                                          |
| json_loads                 | 29.2 us                                                | 28.8 us: 1.01x faster                                                           |
| bench_thread_pool          | 834 us                                                 | 828 us: 1.01x faster                                                            |
| scimark_lu                 | 116 ms                                                 | 116 ms: 1.01x faster                                                            |
| crypto_pyaes               | 76.7 ms                                                | 76.4 ms: 1.00x faster                                                           |
| gc_traversal               | 4.01 ms                                                | 4.00 ms: 1.00x faster                                                           |
| sqlglot_optimize           | 55.3 ms                                                | 55.4 ms: 1.00x slower                                                           |
| float                      | 78.9 ms                                                | 79.3 ms: 1.00x slower                                                           |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                                            |
| dulwich_log                | 64.6 ms                                                | 65.8 ms: 1.02x slower                                                           |
| dask                       | 365 ms                                                 | 372 ms: 1.02x slower                                                            |
| pickle_dict                | 34.6 us                                                | 35.3 us: 1.02x slower                                                           |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.02x slower                                                            |
| deepcopy_reduce            | 3.22 us                                                | 3.30 us: 1.02x slower                                                           |
| mako                       | 10.7 ms                                                | 10.9 ms: 1.03x slower                                                           |
| 2to3                       | 264 ms                                                 | 271 ms: 1.03x slower                                                            |
| json                       | 5.24 ms                                                | 5.39 ms: 1.03x slower                                                           |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.17 ms: 1.03x slower                                                           |
| thrift                     | 784 us                                                 | 812 us: 1.04x slower                                                            |
| unpickle_list              | 5.21 us                                                | 5.40 us: 1.04x slower                                                           |
| scimark_sor                | 121 ms                                                 | 126 ms: 1.04x slower                                                            |
| html5lib                   | 64.8 ms                                                | 67.7 ms: 1.04x slower                                                           |
| genshi_text                | 22.5 ms                                                | 23.6 ms: 1.05x slower                                                           |
| regex_effbot               | 3.51 ms                                                | 3.67 ms: 1.05x slower                                                           |
| docutils                   | 2.66 sec                                               | 2.80 sec: 1.05x slower                                                          |
| xml_etree_process          | 56.9 ms                                                | 60.3 ms: 1.06x slower                                                           |
| pickle                     | 11.0 us                                                | 11.7 us: 1.06x slower                                                           |
| spectral_norm              | 108 ms                                                 | 116 ms: 1.07x slower                                                            |
| xml_etree_generate         | 81.1 ms                                                | 87.0 ms: 1.07x slower                                                           |
| django_template            | 33.5 ms                                                | 36.1 ms: 1.08x slower                                                           |
| regex_v8                   | 22.9 ms                                                | 24.8 ms: 1.09x slower                                                           |
| regex_dna                  | 205 ms                                                 | 223 ms: 1.09x slower                                                            |
| scimark_fft                | 345 ms                                                 | 379 ms: 1.10x slower                                                            |
| pickle_list                | 4.59 us                                                | 5.04 us: 1.10x slower                                                           |
| unpickle                   | 13.8 us                                                | 15.3 us: 1.11x slower                                                           |
| pyflate                    | 434 ms                                                 | 486 ms: 1.12x slower                                                            |
| sqlite_synth               | 2.57 us                                                | 2.97 us: 1.15x slower                                                           |
| python_startup_no_site     | 6.01 ms                                                | 7.13 ms: 1.19x slower                                                           |
| coverage                   | 78.8 ms                                                | 94.2 ms: 1.20x slower                                                           |
| async_generators           | 374 ms                                                 | 458 ms: 1.23x slower                                                            |
| telco                      | 6.86 ms                                                | 8.50 ms: 1.24x slower                                                           |
| python_startup             | 8.56 ms                                                | 10.6 ms: 1.24x slower                                                           |
| create_gc_cycles           | 1.43 ms                                                | 1.80 ms: 1.25x slower                                                           |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                    |

Benchmark hidden because not significant (3): bench_mp_pool, pprint_safe_repr, deepcopy
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, djangocms, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.36% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x