# Results vs. 3.12.0

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 881df50
- commit date: 2024-05-23
- overall geometric mean: 1.03x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.01x faster
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 271 ms: 1.01x faster                                                            |
| chameleon      | 7.41 ms                                                | 6.99 ms: 1.06x faster                                                           |
| docutils       | 2.77 sec                                               | 2.79 sec: 1.01x slower                                                          |
| tornado_http   | 103 ms                                                 | 94.5 ms: 1.09x faster                                                           |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 347 ms: 1.30x faster                                                            |
| async_tree_memoization_tg  | 575 ms                                                 | 448 ms: 1.28x faster                                                            |
| async_tree_memoization     | 578 ms                                                 | 460 ms: 1.26x faster                                                            |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 581 ms: 1.25x faster                                                            |
| async_tree_none            | 472 ms                                                 | 382 ms: 1.24x faster                                                            |
| async_tree_io              | 1.16 sec                                               | 942 ms: 1.23x faster                                                            |
| async_tree_io_tg           | 1.18 sec                                               | 965 ms: 1.22x faster                                                            |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 614 ms: 1.18x faster                                                            |
| Geometric mean             | (ref)                                                  | 1.24x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 78.2 ms: 1.08x faster                                                           |
| nbody          | 97.0 ms                                                | 94.3 ms: 1.03x faster                                                           |
| pidigits       | 187 ms                                                 | 190 ms: 1.01x slower                                                            |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 134 ms: 1.11x faster                                                            |
| regex_effbot   | 3.61 ms                                                | 3.94 ms: 1.09x slower                                                           |
| regex_dna      | 212 ms                                                 | 233 ms: 1.10x slower                                                            |
| regex_v8       | 23.1 ms                                                | 26.0 ms: 1.12x slower                                                           |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pickle_pure_python   | 324 us                                                 | 304 us: 1.07x faster                                                            |
| tomli_loads          | 2.33 sec                                               | 2.19 sec: 1.07x faster                                                          |
| unpickle_pure_python | 230 us                                                 | 218 us: 1.05x faster                                                            |
| xml_etree_generate   | 89.2 ms                                                | 86.5 ms: 1.03x faster                                                           |
| xml_etree_process    | 61.7 ms                                                | 60.2 ms: 1.03x faster                                                           |
| unpickle             | 15.9 us                                                | 15.6 us: 1.02x faster                                                           |
| xml_etree_iterparse  | 107 ms                                                 | 106 ms: 1.01x faster                                                            |
| pickle_dict          | 35.5 us                                                | 35.6 us: 1.00x slower                                                           |
| json_loads           | 28.5 us                                                | 28.7 us: 1.01x slower                                                           |
| pickle_list          | 5.08 us                                                | 5.15 us: 1.01x slower                                                           |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                           |
| pickle               | 11.6 us                                                | 11.9 us: 1.03x slower                                                           |
| unpickle_list        | 5.29 us                                                | 5.48 us: 1.04x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                    |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.09 ms: 1.02x slower                                                           |
| python_startup         | 9.55 ms                                                | 10.4 ms: 1.08x slower                                                           |
| Geometric mean         | (ref)                                                  | 1.05x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.9 ms: 1.09x faster                                                           |
| django_template | 34.6 ms                                                | 35.3 ms: 1.02x slower                                                           |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| comprehensions             | 21.8 us                                                | 16.8 us: 1.30x faster                                                           |
| async_tree_none_tg         | 450 ms                                                 | 347 ms: 1.30x faster                                                            |
| async_tree_memoization_tg  | 575 ms                                                 | 448 ms: 1.28x faster                                                            |
| async_tree_memoization     | 578 ms                                                 | 460 ms: 1.26x faster                                                            |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 581 ms: 1.25x faster                                                            |
| async_tree_none            | 472 ms                                                 | 382 ms: 1.24x faster                                                            |
| async_tree_io              | 1.16 sec                                               | 942 ms: 1.23x faster                                                            |
| async_tree_io_tg           | 1.18 sec                                               | 965 ms: 1.22x faster                                                            |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 614 ms: 1.18x faster                                                            |
| pathlib                    | 19.3 ms                                                | 16.8 ms: 1.15x faster                                                           |
| crypto_pyaes               | 81.9 ms                                                | 71.7 ms: 1.14x faster                                                           |
| deltablue                  | 3.72 ms                                                | 3.28 ms: 1.13x faster                                                           |
| logging_format             | 7.23 us                                                | 6.41 us: 1.13x faster                                                           |
| raytrace                   | 312 ms                                                 | 280 ms: 1.12x faster                                                            |
| logging_simple             | 6.46 us                                                | 5.80 us: 1.11x faster                                                           |
| regex_compile              | 148 ms                                                 | 134 ms: 1.11x faster                                                            |
| sympy_sum                  | 169 ms                                                 | 154 ms: 1.09x faster                                                            |
| chaos                      | 67.0 ms                                                | 61.5 ms: 1.09x faster                                                           |
| mako                       | 11.9 ms                                                | 10.9 ms: 1.09x faster                                                           |
| tornado_http               | 103 ms                                                 | 94.5 ms: 1.09x faster                                                           |
| float                      | 84.7 ms                                                | 78.2 ms: 1.08x faster                                                           |
| spectral_norm              | 115 ms                                                 | 107 ms: 1.07x faster                                                            |
| scimark_monte_carlo        | 75.1 ms                                                | 70.3 ms: 1.07x faster                                                           |
| sympy_str                  | 300 ms                                                 | 281 ms: 1.07x faster                                                            |
| pickle_pure_python         | 324 us                                                 | 304 us: 1.07x faster                                                            |
| tomli_loads                | 2.33 sec                                               | 2.19 sec: 1.07x faster                                                          |
| generators                 | 31.2 ms                                                | 29.3 ms: 1.07x faster                                                           |
| pprint_safe_repr           | 776 ms                                                 | 730 ms: 1.06x faster                                                            |
| chameleon                  | 7.41 ms                                                | 6.99 ms: 1.06x faster                                                           |
| unpickle_pure_python       | 230 us                                                 | 218 us: 1.05x faster                                                            |
| sympy_integrate            | 21.4 ms                                                | 20.4 ms: 1.05x faster                                                           |
| async_generators           | 463 ms                                                 | 441 ms: 1.05x faster                                                            |
| pprint_pformat             | 1.57 sec                                               | 1.49 sec: 1.05x faster                                                          |
| pyflate                    | 482 ms                                                 | 461 ms: 1.05x faster                                                            |
| dulwich_log                | 68.5 ms                                                | 65.6 ms: 1.04x faster                                                           |
| scimark_sor                | 129 ms                                                 | 124 ms: 1.04x faster                                                            |
| sqlglot_transpile          | 1.68 ms                                                | 1.62 ms: 1.04x faster                                                           |
| fannkuch                   | 417 ms                                                 | 401 ms: 1.04x faster                                                            |
| sqlglot_parse              | 1.36 ms                                                | 1.31 ms: 1.04x faster                                                           |
| logging_silent             | 104 ns                                                 | 101 ns: 1.03x faster                                                            |
| meteor_contest             | 112 ms                                                 | 109 ms: 1.03x faster                                                            |
| xml_etree_generate         | 89.2 ms                                                | 86.5 ms: 1.03x faster                                                           |
| nbody                      | 97.0 ms                                                | 94.3 ms: 1.03x faster                                                           |
| deepcopy_reduce            | 3.35 us                                                | 3.25 us: 1.03x faster                                                           |
| xml_etree_process          | 61.7 ms                                                | 60.2 ms: 1.03x faster                                                           |
| deepcopy_memo              | 40.7 us                                                | 39.7 us: 1.02x faster                                                           |
| nqueens                    | 83.3 ms                                                | 81.6 ms: 1.02x faster                                                           |
| hexiom                     | 6.41 ms                                                | 6.29 ms: 1.02x faster                                                           |
| gc_traversal               | 3.79 ms                                                | 3.72 ms: 1.02x faster                                                           |
| sympy_expand               | 478 ms                                                 | 469 ms: 1.02x faster                                                            |
| unpickle                   | 15.9 us                                                | 15.6 us: 1.02x faster                                                           |
| 2to3                       | 274 ms                                                 | 271 ms: 1.01x faster                                                            |
| deepcopy                   | 371 us                                                 | 367 us: 1.01x faster                                                            |
| xml_etree_iterparse        | 107 ms                                                 | 106 ms: 1.01x faster                                                            |
| bench_thread_pool          | 842 us                                                 | 834 us: 1.01x faster                                                            |
| scimark_lu                 | 118 ms                                                 | 117 ms: 1.01x faster                                                            |
| pickle_dict                | 35.5 us                                                | 35.6 us: 1.00x slower                                                           |
| json_loads                 | 28.5 us                                                | 28.7 us: 1.01x slower                                                           |
| docutils                   | 2.77 sec                                               | 2.79 sec: 1.01x slower                                                          |
| pickle_list                | 5.08 us                                                | 5.15 us: 1.01x slower                                                           |
| pidigits                   | 187 ms                                                 | 190 ms: 1.01x slower                                                            |
| json                       | 5.26 ms                                                | 5.33 ms: 1.01x slower                                                           |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                           |
| django_template            | 34.6 ms                                                | 35.3 ms: 1.02x slower                                                           |
| python_startup_no_site     | 6.94 ms                                                | 7.09 ms: 1.02x slower                                                           |
| scimark_fft                | 382 ms                                                 | 391 ms: 1.02x slower                                                            |
| asyncio_tcp                | 491 ms                                                 | 503 ms: 1.02x slower                                                            |
| pycparser                  | 1.18 sec                                               | 1.21 sec: 1.03x slower                                                          |
| pickle                     | 11.6 us                                                | 11.9 us: 1.03x slower                                                           |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                                          |
| typing_runtime_protocols   | 158 us                                                 | 163 us: 1.03x slower                                                            |
| asyncio_websockets         | 551 ms                                                 | 569 ms: 1.03x slower                                                            |
| coroutines                 | 23.2 ms                                                | 23.9 ms: 1.03x slower                                                           |
| go                         | 139 ms                                                 | 144 ms: 1.03x slower                                                            |
| unpickle_list              | 5.29 us                                                | 5.48 us: 1.04x slower                                                           |
| sqlite_synth               | 2.83 us                                                | 2.98 us: 1.05x slower                                                           |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.31 ms: 1.05x slower                                                           |
| richards                   | 45.8 ms                                                | 48.4 ms: 1.06x slower                                                           |
| richards_super             | 51.5 ms                                                | 54.9 ms: 1.07x slower                                                           |
| python_startup             | 9.55 ms                                                | 10.4 ms: 1.08x slower                                                           |
| regex_effbot               | 3.61 ms                                                | 3.94 ms: 1.09x slower                                                           |
| regex_dna                  | 212 ms                                                 | 233 ms: 1.10x slower                                                            |
| regex_v8                   | 23.1 ms                                                | 26.0 ms: 1.12x slower                                                           |
| telco                      | 7.10 ms                                                | 8.46 ms: 1.19x slower                                                           |
| create_gc_cycles           | 1.48 ms                                                | 1.78 ms: 1.20x slower                                                           |
| coverage                   | 72.7 ms                                                | 92.1 ms: 1.27x slower                                                           |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                                    |

Benchmark hidden because not significant (6): dask, bench_mp_pool, sqlglot_normalize, xml_etree_parse, mdp, sqlglot_optimize
Ignored benchmarks (6) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240523-3.14.0a0-881df50/bm-20240523-linux-x86_64-faster%2dcpython-specialize_binary_op-3.14.0a0-881df50.json: flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 0.97x