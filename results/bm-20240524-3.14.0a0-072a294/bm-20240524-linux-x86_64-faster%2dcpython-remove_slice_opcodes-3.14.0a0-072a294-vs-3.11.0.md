# Results vs. 3.11.0

- fork: faster-cpython
- ref: remove_slice_opcodes
- machine: linux-x86_64
- commit hash: 072a294
- commit date: 2024-05-24
- overall geometric mean: 1.06x faster
- HPT reliability: 97.09%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240524-linux-x86_64-faster%2dcpython-remove_slice_opcodes-3.14.0a0-072a294 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 271 ms: 1.03x slower                                                            |
| chameleon      | 6.70 ms                                                | 7.05 ms: 1.05x slower                                                           |
| docutils       | 2.66 sec                                               | 2.78 sec: 1.04x slower                                                          |
| html5lib       | 64.8 ms                                                | 67.8 ms: 1.05x slower                                                           |
| tornado_http   | 98.1 ms                                                | 94.2 ms: 1.04x faster                                                           |
| Geometric mean | (ref)                                                  | 1.03x slower                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240524-linux-x86_64-faster%2dcpython-remove_slice_opcodes-3.14.0a0-072a294 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 340 ms: 1.45x faster                                                            |
| async_tree_memoization_tg  | 626 ms                                                 | 450 ms: 1.39x faster                                                            |
| async_tree_io_tg           | 1.29 sec                                               | 942 ms: 1.37x faster                                                            |
| async_tree_none            | 528 ms                                                 | 387 ms: 1.36x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 485 ms: 1.32x faster                                                            |
| async_tree_io              | 1.29 sec                                               | 976 ms: 1.32x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 589 ms: 1.29x faster                                                            |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 623 ms: 1.20x faster                                                            |
| Geometric mean             | (ref)                                                  | 1.34x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240524-linux-x86_64-faster%2dcpython-remove_slice_opcodes-3.14.0a0-072a294 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 86.0 ms: 1.12x faster                                                           |
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                    |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240524-linux-x86_64-faster%2dcpython-remove_slice_opcodes-3.14.0a0-072a294 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 133 ms: 1.06x faster                                                            |
| regex_effbot   | 3.51 ms                                                | 3.78 ms: 1.08x slower                                                           |
| regex_dna      | 205 ms                                                 | 230 ms: 1.12x slower                                                            |
| regex_v8       | 22.9 ms                                                | 25.9 ms: 1.13x slower                                                           |
| Geometric mean | (ref)                                                  | 1.07x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240524-linux-x86_64-faster%2dcpython-remove_slice_opcodes-3.14.0a0-072a294 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.24x faster                                                           |
| unpickle_pure_python | 242 us                                                 | 215 us: 1.12x faster                                                            |
| tomli_loads          | 2.30 sec                                               | 2.16 sec: 1.07x faster                                                          |
| pickle_pure_python   | 320 us                                                 | 304 us: 1.05x faster                                                            |
| xml_etree_parse      | 164 ms                                                 | 161 ms: 1.02x faster                                                            |
| json_loads           | 29.2 us                                                | 29.0 us: 1.01x faster                                                           |
| pickle_dict          | 34.6 us                                                | 34.9 us: 1.01x slower                                                           |
| pickle               | 11.0 us                                                | 11.6 us: 1.06x slower                                                           |
| xml_etree_process    | 56.9 ms                                                | 60.3 ms: 1.06x slower                                                           |
| xml_etree_generate   | 81.1 ms                                                | 86.8 ms: 1.07x slower                                                           |
| unpickle_list        | 5.21 us                                                | 5.60 us: 1.07x slower                                                           |
| unpickle             | 13.8 us                                                | 15.2 us: 1.10x slower                                                           |
| pickle_list          | 4.59 us                                                | 5.07 us: 1.11x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                                    |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240524-linux-x86_64-faster%2dcpython-remove_slice_opcodes-3.14.0a0-072a294 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.14 ms: 1.19x slower                                                           |
| python_startup         | 8.56 ms                                                | 10.4 ms: 1.22x slower                                                           |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240524-linux-x86_64-faster%2dcpython-remove_slice_opcodes-3.14.0a0-072a294 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 52.1 ms: 1.03x faster                                                           |
| genshi_text     | 22.5 ms                                                | 23.6 ms: 1.05x slower                                                           |
| django_template | 33.5 ms                                                | 35.2 ms: 1.05x slower                                                           |
| mako            | 10.7 ms                                                | 11.2 ms: 1.05x slower                                                           |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240524-linux-x86_64-faster%2dcpython-remove_slice_opcodes-3.14.0a0-072a294 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 165 us: 3.15x faster                                                            |
| generators                 | 74.9 ms                                                | 29.5 ms: 2.54x faster                                                           |
| asyncio_tcp                | 875 ms                                                 | 508 ms: 1.72x faster                                                            |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                          |
| pylint                     | 476 ms                                                 | 317 ms: 1.50x faster                                                            |
| async_tree_none_tg         | 491 ms                                                 | 340 ms: 1.45x faster                                                            |
| comprehensions             | 23.6 us                                                | 16.6 us: 1.42x faster                                                           |
| async_tree_memoization_tg  | 626 ms                                                 | 450 ms: 1.39x faster                                                            |
| async_tree_io_tg           | 1.29 sec                                               | 942 ms: 1.37x faster                                                            |
| async_tree_none            | 528 ms                                                 | 387 ms: 1.36x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 485 ms: 1.32x faster                                                            |
| async_tree_io              | 1.29 sec                                               | 976 ms: 1.32x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 589 ms: 1.29x faster                                                            |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.24x faster                                                           |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 623 ms: 1.20x faster                                                            |
| chaos                      | 71.9 ms                                                | 60.0 ms: 1.20x faster                                                           |
| deltablue                  | 3.92 ms                                                | 3.32 ms: 1.18x faster                                                           |
| coroutines                 | 27.0 ms                                                | 23.5 ms: 1.15x faster                                                           |
| raytrace                   | 309 ms                                                 | 269 ms: 1.15x faster                                                            |
| richards_super             | 61.9 ms                                                | 54.3 ms: 1.14x faster                                                           |
| hexiom                     | 6.89 ms                                                | 6.12 ms: 1.13x faster                                                           |
| unpickle_pure_python       | 242 us                                                 | 215 us: 1.12x faster                                                            |
| nbody                      | 96.0 ms                                                | 86.0 ms: 1.12x faster                                                           |
| pathlib                    | 18.5 ms                                                | 16.7 ms: 1.11x faster                                                           |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.08x faster                                                            |
| sqlglot_parse              | 1.43 ms                                                | 1.33 ms: 1.08x faster                                                           |
| sqlglot_transpile          | 1.75 ms                                                | 1.63 ms: 1.07x faster                                                           |
| tomli_loads                | 2.30 sec                                               | 2.16 sec: 1.07x faster                                                          |
| logging_silent             | 111 ns                                                 | 104 ns: 1.07x faster                                                            |
| nqueens                    | 87.9 ms                                                | 82.9 ms: 1.06x faster                                                           |
| regex_compile              | 141 ms                                                 | 133 ms: 1.06x faster                                                            |
| sympy_str                  | 297 ms                                                 | 281 ms: 1.06x faster                                                            |
| logging_simple             | 6.22 us                                                | 5.90 us: 1.06x faster                                                           |
| sympy_integrate            | 21.5 ms                                                | 20.4 ms: 1.05x faster                                                           |
| scimark_monte_carlo        | 70.7 ms                                                | 67.2 ms: 1.05x faster                                                           |
| pickle_pure_python         | 320 us                                                 | 304 us: 1.05x faster                                                            |
| logging_format             | 6.81 us                                                | 6.49 us: 1.05x faster                                                           |
| richards                   | 49.8 ms                                                | 47.5 ms: 1.05x faster                                                           |
| tornado_http               | 98.1 ms                                                | 94.2 ms: 1.04x faster                                                           |
| gc_traversal               | 4.01 ms                                                | 3.87 ms: 1.04x faster                                                           |
| go                         | 149 ms                                                 | 144 ms: 1.03x faster                                                            |
| sympy_expand               | 484 ms                                                 | 472 ms: 1.03x faster                                                            |
| sqlglot_normalize          | 113 ms                                                 | 110 ms: 1.03x faster                                                            |
| genshi_xml                 | 53.4 ms                                                | 52.1 ms: 1.03x faster                                                           |
| crypto_pyaes               | 76.7 ms                                                | 75.0 ms: 1.02x faster                                                           |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                                            |
| xml_etree_parse            | 164 ms                                                 | 161 ms: 1.02x faster                                                            |
| deepcopy_memo              | 40.2 us                                                | 39.8 us: 1.01x faster                                                           |
| sqlglot_optimize           | 55.3 ms                                                | 54.9 ms: 1.01x faster                                                           |
| json_loads                 | 29.2 us                                                | 29.0 us: 1.01x faster                                                           |
| pprint_pformat             | 1.55 sec                                               | 1.55 sec: 1.01x faster                                                          |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.00x faster                                                           |
| meteor_contest             | 109 ms                                                 | 109 ms: 1.00x faster                                                            |
| mdp                        | 2.77 sec                                               | 2.78 sec: 1.00x slower                                                          |
| pprint_safe_repr           | 747 ms                                                 | 753 ms: 1.01x slower                                                            |
| pickle_dict                | 34.6 us                                                | 34.9 us: 1.01x slower                                                           |
| dulwich_log                | 64.6 ms                                                | 65.4 ms: 1.01x slower                                                           |
| deepcopy_reduce            | 3.22 us                                                | 3.27 us: 1.02x slower                                                           |
| json                       | 5.24 ms                                                | 5.37 ms: 1.02x slower                                                           |
| fannkuch                   | 405 ms                                                 | 416 ms: 1.03x slower                                                            |
| 2to3                       | 264 ms                                                 | 271 ms: 1.03x slower                                                            |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                                            |
| thrift                     | 784 us                                                 | 807 us: 1.03x slower                                                            |
| docutils                   | 2.66 sec                                               | 2.78 sec: 1.04x slower                                                          |
| html5lib                   | 64.8 ms                                                | 67.8 ms: 1.05x slower                                                           |
| genshi_text                | 22.5 ms                                                | 23.6 ms: 1.05x slower                                                           |
| django_template            | 33.5 ms                                                | 35.2 ms: 1.05x slower                                                           |
| pycparser                  | 1.19 sec                                               | 1.25 sec: 1.05x slower                                                          |
| mako                       | 10.7 ms                                                | 11.2 ms: 1.05x slower                                                           |
| chameleon                  | 6.70 ms                                                | 7.05 ms: 1.05x slower                                                           |
| scimark_fft                | 345 ms                                                 | 365 ms: 1.06x slower                                                            |
| pickle                     | 11.0 us                                                | 11.6 us: 1.06x slower                                                           |
| xml_etree_process          | 56.9 ms                                                | 60.3 ms: 1.06x slower                                                           |
| spectral_norm              | 108 ms                                                 | 115 ms: 1.07x slower                                                            |
| xml_etree_generate         | 81.1 ms                                                | 86.8 ms: 1.07x slower                                                           |
| unpickle_list              | 5.21 us                                                | 5.60 us: 1.07x slower                                                           |
| regex_effbot               | 3.51 ms                                                | 3.78 ms: 1.08x slower                                                           |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.10x slower                                                           |
| scimark_sor                | 121 ms                                                 | 133 ms: 1.10x slower                                                            |
| pickle_list                | 4.59 us                                                | 5.07 us: 1.11x slower                                                           |
| regex_dna                  | 205 ms                                                 | 230 ms: 1.12x slower                                                            |
| pyflate                    | 434 ms                                                 | 491 ms: 1.13x slower                                                            |
| regex_v8                   | 22.9 ms                                                | 25.9 ms: 1.13x slower                                                           |
| sqlite_synth               | 2.57 us                                                | 2.99 us: 1.16x slower                                                           |
| coverage                   | 78.8 ms                                                | 91.8 ms: 1.17x slower                                                           |
| python_startup_no_site     | 6.01 ms                                                | 7.14 ms: 1.19x slower                                                           |
| async_generators           | 374 ms                                                 | 447 ms: 1.20x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.4 ms: 1.22x slower                                                           |
| flaskblogging              | 7.28 ms                                                | 8.90 ms: 1.22x slower                                                           |
| telco                      | 6.86 ms                                                | 8.40 ms: 1.23x slower                                                           |
| create_gc_cycles           | 1.43 ms                                                | 1.87 ms: 1.30x slower                                                           |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                    |

Benchmark hidden because not significant (7): xml_etree_iterparse, bench_thread_pool, deepcopy, float, scimark_lu, scimark_sparse_mat_mult, dask
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, djangocms, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 97.09% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x