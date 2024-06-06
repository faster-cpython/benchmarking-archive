# Results vs. 3.11.0

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 5386b2d
- commit date: 2024-05-29
- overall geometric mean: 1.06x faster
- HPT reliability: 97.08%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240529-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-5386b2d |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 279 ms: 1.05x slower                                                            |
| docutils       | 2.66 sec                                               | 2.92 sec: 1.10x slower                                                          |
| html5lib       | 64.8 ms                                                | 66.9 ms: 1.03x slower                                                           |
| tornado_http   | 98.1 ms                                                | 96.6 ms: 1.01x faster                                                           |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240529-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-5386b2d |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 334 ms: 1.47x faster                                                            |
| async_tree_memoization_tg  | 626 ms                                                 | 444 ms: 1.41x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 464 ms: 1.38x faster                                                            |
| async_tree_io_tg           | 1.29 sec                                               | 942 ms: 1.37x faster                                                            |
| async_tree_none            | 528 ms                                                 | 384 ms: 1.37x faster                                                            |
| async_tree_io              | 1.29 sec                                               | 958 ms: 1.34x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 584 ms: 1.30x faster                                                            |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 615 ms: 1.22x faster                                                            |
| Geometric mean             | (ref)                                                  | 1.36x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240529-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-5386b2d |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 80.8 ms: 1.19x faster                                                           |
| float          | 78.9 ms                                                | 71.7 ms: 1.10x faster                                                           |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                            |
| Geometric mean | (ref)                                                  | 1.10x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240529-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-5386b2d |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 137 ms: 1.03x faster                                                            |
| regex_effbot   | 3.51 ms                                                | 3.69 ms: 1.05x slower                                                           |
| regex_v8       | 22.9 ms                                                | 24.1 ms: 1.05x slower                                                           |
| regex_dna      | 205 ms                                                 | 229 ms: 1.12x slower                                                            |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240529-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-5386b2d |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.4 ms: 1.28x faster                                                           |
| tomli_loads          | 2.30 sec                                               | 2.09 sec: 1.10x faster                                                          |
| xml_etree_parse      | 164 ms                                                 | 150 ms: 1.10x faster                                                            |
| unpickle_pure_python | 242 us                                                 | 222 us: 1.09x faster                                                            |
| xml_etree_iterparse  | 108 ms                                                 | 100 ms: 1.08x faster                                                            |
| pickle_pure_python   | 320 us                                                 | 300 us: 1.07x faster                                                            |
| json_loads           | 29.2 us                                                | 28.7 us: 1.02x faster                                                           |
| xml_etree_generate   | 81.1 ms                                                | 82.0 ms: 1.01x slower                                                           |
| xml_etree_process    | 56.9 ms                                                | 58.2 ms: 1.02x slower                                                           |
| pickle_dict          | 34.6 us                                                | 36.0 us: 1.04x slower                                                           |
| unpickle_list        | 5.21 us                                                | 5.48 us: 1.05x slower                                                           |
| unpickle             | 13.8 us                                                | 14.7 us: 1.07x slower                                                           |
| pickle               | 11.0 us                                                | 12.1 us: 1.10x slower                                                           |
| pickle_list          | 4.59 us                                                | 5.26 us: 1.15x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240529-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-5386b2d |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.59 ms: 1.26x slower                                                           |
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.29x slower                                                           |
| Geometric mean         | (ref)                                                  | 1.28x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240529-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-5386b2d |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.2 ms: 1.05x faster                                                           |
| django_template | 33.5 ms                                                | 36.1 ms: 1.08x slower                                                           |
| genshi_xml      | 53.4 ms                                                | 58.2 ms: 1.09x slower                                                           |
| genshi_text     | 22.5 ms                                                | 25.4 ms: 1.13x slower                                                           |
| Geometric mean  | (ref)                                                  | 1.06x slower                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240529-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-5386b2d |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 171 us: 3.04x faster                                                            |
| generators                 | 74.9 ms                                                | 30.3 ms: 2.47x faster                                                           |
| asyncio_tcp                | 875 ms                                                 | 518 ms: 1.69x faster                                                            |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                          |
| async_tree_none_tg         | 491 ms                                                 | 334 ms: 1.47x faster                                                            |
| comprehensions             | 23.6 us                                                | 16.6 us: 1.42x faster                                                           |
| async_tree_memoization_tg  | 626 ms                                                 | 444 ms: 1.41x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 464 ms: 1.38x faster                                                            |
| async_tree_io_tg           | 1.29 sec                                               | 942 ms: 1.37x faster                                                            |
| async_tree_none            | 528 ms                                                 | 384 ms: 1.37x faster                                                            |
| pylint                     | 476 ms                                                 | 352 ms: 1.35x faster                                                            |
| async_tree_io              | 1.29 sec                                               | 958 ms: 1.34x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 584 ms: 1.30x faster                                                            |
| richards_super             | 61.9 ms                                                | 47.9 ms: 1.29x faster                                                           |
| json_dumps                 | 13.3 ms                                                | 10.4 ms: 1.28x faster                                                           |
| chaos                      | 71.9 ms                                                | 58.9 ms: 1.22x faster                                                           |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 615 ms: 1.22x faster                                                            |
| coroutines                 | 27.0 ms                                                | 22.5 ms: 1.20x faster                                                           |
| richards                   | 49.8 ms                                                | 41.7 ms: 1.19x faster                                                           |
| nbody                      | 96.0 ms                                                | 80.8 ms: 1.19x faster                                                           |
| fannkuch                   | 405 ms                                                 | 356 ms: 1.14x faster                                                            |
| crypto_pyaes               | 76.7 ms                                                | 67.6 ms: 1.13x faster                                                           |
| scimark_monte_carlo        | 70.7 ms                                                | 62.5 ms: 1.13x faster                                                           |
| pathlib                    | 18.5 ms                                                | 16.6 ms: 1.12x faster                                                           |
| tomli_loads                | 2.30 sec                                               | 2.09 sec: 1.10x faster                                                          |
| float                      | 78.9 ms                                                | 71.7 ms: 1.10x faster                                                           |
| logging_simple             | 6.22 us                                                | 5.65 us: 1.10x faster                                                           |
| logging_format             | 6.81 us                                                | 6.20 us: 1.10x faster                                                           |
| xml_etree_parse            | 164 ms                                                 | 150 ms: 1.10x faster                                                            |
| unpickle_pure_python       | 242 us                                                 | 222 us: 1.09x faster                                                            |
| raytrace                   | 309 ms                                                 | 284 ms: 1.08x faster                                                            |
| xml_etree_iterparse        | 108 ms                                                 | 100 ms: 1.08x faster                                                            |
| pprint_pformat             | 1.55 sec                                               | 1.45 sec: 1.07x faster                                                          |
| sqlglot_parse              | 1.43 ms                                                | 1.34 ms: 1.07x faster                                                           |
| pickle_pure_python         | 320 us                                                 | 300 us: 1.07x faster                                                            |
| pprint_safe_repr           | 747 ms                                                 | 705 ms: 1.06x faster                                                            |
| mako                       | 10.7 ms                                                | 10.2 ms: 1.05x faster                                                           |
| sqlglot_transpile          | 1.75 ms                                                | 1.67 ms: 1.05x faster                                                           |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.82 ms: 1.04x faster                                                           |
| regex_compile              | 141 ms                                                 | 137 ms: 1.03x faster                                                            |
| hexiom                     | 6.89 ms                                                | 6.67 ms: 1.03x faster                                                           |
| deltablue                  | 3.92 ms                                                | 3.80 ms: 1.03x faster                                                           |
| scimark_fft                | 345 ms                                                 | 335 ms: 1.03x faster                                                            |
| logging_silent             | 111 ns                                                 | 108 ns: 1.03x faster                                                            |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                            |
| pycparser                  | 1.19 sec                                               | 1.17 sec: 1.02x faster                                                          |
| json_loads                 | 29.2 us                                                | 28.7 us: 1.02x faster                                                           |
| tornado_http               | 98.1 ms                                                | 96.6 ms: 1.01x faster                                                           |
| nqueens                    | 87.9 ms                                                | 86.7 ms: 1.01x faster                                                           |
| mdp                        | 2.77 sec                                               | 2.74 sec: 1.01x faster                                                          |
| go                         | 149 ms                                                 | 148 ms: 1.00x faster                                                            |
| gc_traversal               | 4.01 ms                                                | 4.04 ms: 1.01x slower                                                           |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                                            |
| sympy_str                  | 297 ms                                                 | 301 ms: 1.01x slower                                                            |
| xml_etree_generate         | 81.1 ms                                                | 82.0 ms: 1.01x slower                                                           |
| xml_etree_process          | 56.9 ms                                                | 58.2 ms: 1.02x slower                                                           |
| sympy_sum                  | 169 ms                                                 | 173 ms: 1.02x slower                                                            |
| deepcopy                   | 365 us                                                 | 374 us: 1.02x slower                                                            |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                            |
| pyflate                    | 434 ms                                                 | 448 ms: 1.03x slower                                                            |
| html5lib                   | 64.8 ms                                                | 66.9 ms: 1.03x slower                                                           |
| sqlglot_optimize           | 55.3 ms                                                | 57.1 ms: 1.03x slower                                                           |
| dask                       | 365 ms                                                 | 378 ms: 1.03x slower                                                            |
| pickle_dict                | 34.6 us                                                | 36.0 us: 1.04x slower                                                           |
| thrift                     | 784 us                                                 | 817 us: 1.04x slower                                                            |
| bench_thread_pool          | 834 us                                                 | 870 us: 1.04x slower                                                            |
| sympy_integrate            | 21.5 ms                                                | 22.5 ms: 1.05x slower                                                           |
| deepcopy_reduce            | 3.22 us                                                | 3.38 us: 1.05x slower                                                           |
| sympy_expand               | 484 ms                                                 | 509 ms: 1.05x slower                                                            |
| regex_effbot               | 3.51 ms                                                | 3.69 ms: 1.05x slower                                                           |
| unpickle_list              | 5.21 us                                                | 5.48 us: 1.05x slower                                                           |
| regex_v8                   | 22.9 ms                                                | 24.1 ms: 1.05x slower                                                           |
| 2to3                       | 264 ms                                                 | 279 ms: 1.05x slower                                                            |
| unpickle                   | 13.8 us                                                | 14.7 us: 1.07x slower                                                           |
| dulwich_log                | 64.6 ms                                                | 69.3 ms: 1.07x slower                                                           |
| django_template            | 33.5 ms                                                | 36.1 ms: 1.08x slower                                                           |
| spectral_norm              | 108 ms                                                 | 118 ms: 1.09x slower                                                            |
| genshi_xml                 | 53.4 ms                                                | 58.2 ms: 1.09x slower                                                           |
| scimark_lu                 | 116 ms                                                 | 128 ms: 1.10x slower                                                            |
| docutils                   | 2.66 sec                                               | 2.92 sec: 1.10x slower                                                          |
| pickle                     | 11.0 us                                                | 12.1 us: 1.10x slower                                                           |
| regex_dna                  | 205 ms                                                 | 229 ms: 1.12x slower                                                            |
| scimark_sor                | 121 ms                                                 | 136 ms: 1.12x slower                                                            |
| genshi_text                | 22.5 ms                                                | 25.4 ms: 1.13x slower                                                           |
| sqlite_synth               | 2.57 us                                                | 2.90 us: 1.13x slower                                                           |
| pickle_list                | 4.59 us                                                | 5.26 us: 1.15x slower                                                           |
| telco                      | 6.86 ms                                                | 8.16 ms: 1.19x slower                                                           |
| coverage                   | 78.8 ms                                                | 93.8 ms: 1.19x slower                                                           |
| async_generators           | 374 ms                                                 | 468 ms: 1.25x slower                                                            |
| create_gc_cycles           | 1.43 ms                                                | 1.80 ms: 1.25x slower                                                           |
| python_startup_no_site     | 6.01 ms                                                | 7.59 ms: 1.26x slower                                                           |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.29x slower                                                           |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                    |

Benchmark hidden because not significant (4): deepcopy_memo, bench_mp_pool, meteor_contest, json
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, djangocms, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 97.08% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x