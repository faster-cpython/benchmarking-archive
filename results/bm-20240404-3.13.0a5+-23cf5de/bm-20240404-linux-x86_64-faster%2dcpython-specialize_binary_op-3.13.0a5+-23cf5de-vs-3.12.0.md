# Results vs. 3.12.0

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 23cf5de
- commit date: 2024-04-04
- overall geometric mean: 1.02x faster
- HPT reliability: 94.97%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 268 ms: 1.02x faster                                                             |
| chameleon      | 7.41 ms                                                | 7.00 ms: 1.06x faster                                                            |
| docutils       | 2.77 sec                                               | 2.79 sec: 1.01x slower                                                           |
| tornado_http   | 103 ms                                                 | 94.8 ms: 1.08x faster                                                            |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 333 ms: 1.35x faster                                                             |
| async_tree_none            | 472 ms                                                 | 352 ms: 1.34x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 440 ms: 1.30x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 927 ms: 1.28x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 918 ms: 1.26x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 461 ms: 1.25x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 601 ms: 1.21x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 608 ms: 1.19x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 81.7 ms: 1.04x faster                                                            |
| pidigits       | 187 ms                                                 | 199 ms: 1.06x slower                                                             |
| nbody          | 97.0 ms                                                | 118 ms: 1.22x slower                                                             |
| Geometric mean | (ref)                                                  | 1.08x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 135 ms: 1.10x faster                                                             |
| regex_dna      | 212 ms                                                 | 220 ms: 1.04x slower                                                             |
| regex_v8       | 23.1 ms                                                | 24.8 ms: 1.07x slower                                                            |
| Geometric mean | (ref)                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 324 us                                                 | 299 us: 1.08x faster                                                             |
| unpickle_pure_python | 230 us                                                 | 219 us: 1.05x faster                                                             |
| unpickle             | 15.9 us                                                | 15.2 us: 1.04x faster                                                            |
| pickle_dict          | 35.5 us                                                | 34.3 us: 1.04x faster                                                            |
| xml_etree_process    | 61.7 ms                                                | 60.2 ms: 1.03x faster                                                            |
| xml_etree_generate   | 89.2 ms                                                | 87.5 ms: 1.02x faster                                                            |
| tomli_loads          | 2.33 sec                                               | 2.30 sec: 1.02x faster                                                           |
| unpickle_list        | 5.29 us                                                | 5.24 us: 1.01x faster                                                            |
| pickle_list          | 5.08 us                                                | 5.04 us: 1.01x faster                                                            |
| xml_etree_iterparse  | 107 ms                                                 | 108 ms: 1.01x slower                                                             |
| json_loads           | 28.5 us                                                | 28.7 us: 1.01x slower                                                            |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                     |

Benchmark hidden because not significant (2): pickle, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 10.6 ms: 1.11x slower                                                            |
| python_startup_no_site | 6.94 ms                                                | 8.99 ms: 1.30x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|-----------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako      | 11.9 ms                                                | 11.0 ms: 1.08x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 114 us: 1.39x faster                                                             |
| async_tree_none_tg         | 450 ms                                                 | 333 ms: 1.35x faster                                                             |
| async_tree_none            | 472 ms                                                 | 352 ms: 1.34x faster                                                             |
| comprehensions             | 21.8 us                                                | 16.5 us: 1.32x faster                                                            |
| async_tree_memoization_tg  | 575 ms                                                 | 440 ms: 1.30x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 927 ms: 1.28x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 918 ms: 1.26x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 461 ms: 1.25x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 601 ms: 1.21x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 608 ms: 1.19x faster                                                             |
| deltablue                  | 3.72 ms                                                | 3.27 ms: 1.13x faster                                                            |
| mypy2                      | 830 ms                                                 | 739 ms: 1.12x faster                                                             |
| raytrace                   | 312 ms                                                 | 279 ms: 1.12x faster                                                             |
| crypto_pyaes               | 81.9 ms                                                | 73.5 ms: 1.11x faster                                                            |
| logging_simple             | 6.46 us                                                | 5.83 us: 1.11x faster                                                            |
| logging_format             | 7.23 us                                                | 6.54 us: 1.11x faster                                                            |
| regex_compile              | 148 ms                                                 | 135 ms: 1.10x faster                                                             |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.09x faster                                                             |
| pickle_pure_python         | 324 us                                                 | 299 us: 1.08x faster                                                             |
| tornado_http               | 103 ms                                                 | 94.8 ms: 1.08x faster                                                            |
| mako                       | 11.9 ms                                                | 11.0 ms: 1.08x faster                                                            |
| sympy_str                  | 300 ms                                                 | 279 ms: 1.07x faster                                                             |
| deepcopy_memo              | 40.7 us                                                | 38.3 us: 1.06x faster                                                            |
| chameleon                  | 7.41 ms                                                | 7.00 ms: 1.06x faster                                                            |
| pprint_safe_repr           | 776 ms                                                 | 734 ms: 1.06x faster                                                             |
| sqlglot_transpile          | 1.68 ms                                                | 1.59 ms: 1.06x faster                                                            |
| generators                 | 31.2 ms                                                | 29.6 ms: 1.06x faster                                                            |
| sqlglot_parse              | 1.36 ms                                                | 1.29 ms: 1.05x faster                                                            |
| sympy_integrate            | 21.4 ms                                                | 20.3 ms: 1.05x faster                                                            |
| unpickle_pure_python       | 230 us                                                 | 219 us: 1.05x faster                                                             |
| deepcopy                   | 371 us                                                 | 353 us: 1.05x faster                                                             |
| async_generators           | 463 ms                                                 | 442 ms: 1.05x faster                                                             |
| logging_silent             | 104 ns                                                 | 100 ns: 1.04x faster                                                             |
| pprint_pformat             | 1.57 sec                                               | 1.51 sec: 1.04x faster                                                           |
| deepcopy_reduce            | 3.35 us                                                | 3.21 us: 1.04x faster                                                            |
| unpickle                   | 15.9 us                                                | 15.2 us: 1.04x faster                                                            |
| float                      | 84.7 ms                                                | 81.7 ms: 1.04x faster                                                            |
| pickle_dict                | 35.5 us                                                | 34.3 us: 1.04x faster                                                            |
| meteor_contest             | 112 ms                                                 | 109 ms: 1.03x faster                                                             |
| pathlib                    | 19.3 ms                                                | 18.8 ms: 1.03x faster                                                            |
| xml_etree_process          | 61.7 ms                                                | 60.2 ms: 1.03x faster                                                            |
| 2to3                       | 274 ms                                                 | 268 ms: 1.02x faster                                                             |
| xml_etree_generate         | 89.2 ms                                                | 87.5 ms: 1.02x faster                                                            |
| pycparser                  | 1.18 sec                                               | 1.16 sec: 1.02x faster                                                           |
| sympy_expand               | 478 ms                                                 | 470 ms: 1.02x faster                                                             |
| gc_traversal               | 3.79 ms                                                | 3.73 ms: 1.02x faster                                                            |
| bench_thread_pool          | 842 us                                                 | 829 us: 1.02x faster                                                             |
| tomli_loads                | 2.33 sec                                               | 2.30 sec: 1.02x faster                                                           |
| scimark_monte_carlo        | 75.1 ms                                                | 74.0 ms: 1.01x faster                                                            |
| fannkuch                   | 417 ms                                                 | 413 ms: 1.01x faster                                                             |
| dulwich_log                | 68.5 ms                                                | 67.8 ms: 1.01x faster                                                            |
| unpickle_list              | 5.29 us                                                | 5.24 us: 1.01x faster                                                            |
| pickle_list                | 5.08 us                                                | 5.04 us: 1.01x faster                                                            |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                            |
| pyflate                    | 482 ms                                                 | 480 ms: 1.00x faster                                                             |
| hexiom                     | 6.41 ms                                                | 6.39 ms: 1.00x faster                                                            |
| xml_etree_iterparse        | 107 ms                                                 | 108 ms: 1.01x slower                                                             |
| docutils                   | 2.77 sec                                               | 2.79 sec: 1.01x slower                                                           |
| json_loads                 | 28.5 us                                                | 28.7 us: 1.01x slower                                                            |
| nqueens                    | 83.3 ms                                                | 84.2 ms: 1.01x slower                                                            |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.01x slower                                                            |
| gunicorn                   | 1.24 ms                                                | 1.26 ms: 1.02x slower                                                            |
| scimark_lu                 | 118 ms                                                 | 121 ms: 1.02x slower                                                             |
| asyncio_websockets         | 551 ms                                                 | 564 ms: 1.02x slower                                                             |
| chaos                      | 67.0 ms                                                | 68.6 ms: 1.03x slower                                                            |
| richards                   | 45.8 ms                                                | 47.0 ms: 1.03x slower                                                            |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                            |
| richards_super             | 51.5 ms                                                | 53.1 ms: 1.03x slower                                                            |
| asyncio_tcp                | 491 ms                                                 | 506 ms: 1.03x slower                                                             |
| coroutines                 | 23.2 ms                                                | 23.9 ms: 1.03x slower                                                            |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                                           |
| sqlite_synth               | 2.83 us                                                | 2.93 us: 1.03x slower                                                            |
| regex_dna                  | 212 ms                                                 | 220 ms: 1.04x slower                                                             |
| go                         | 139 ms                                                 | 146 ms: 1.04x slower                                                             |
| json                       | 5.26 ms                                                | 5.51 ms: 1.05x slower                                                            |
| scimark_sor                | 129 ms                                                 | 137 ms: 1.06x slower                                                             |
| pidigits                   | 187 ms                                                 | 199 ms: 1.06x slower                                                             |
| mdp                        | 2.63 sec                                               | 2.80 sec: 1.07x slower                                                           |
| regex_v8                   | 23.1 ms                                                | 24.8 ms: 1.07x slower                                                            |
| python_startup             | 9.55 ms                                                | 10.6 ms: 1.11x slower                                                            |
| scimark_fft                | 382 ms                                                 | 428 ms: 1.12x slower                                                             |
| create_gc_cycles           | 1.48 ms                                                | 1.73 ms: 1.17x slower                                                            |
| spectral_norm              | 115 ms                                                 | 138 ms: 1.20x slower                                                             |
| telco                      | 7.10 ms                                                | 8.56 ms: 1.21x slower                                                            |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 6.14 ms: 1.21x slower                                                            |
| nbody                      | 97.0 ms                                                | 118 ms: 1.22x slower                                                             |
| python_startup_no_site     | 6.94 ms                                                | 8.99 ms: 1.30x slower                                                            |
| coverage                   | 72.7 ms                                                | 98.3 ms: 1.35x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                                     |

Benchmark hidden because not significant (6): dask, sqlglot_optimize, sqlglot_normalize, regex_effbot, pickle, xml_etree_parse
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240404-3.13.0a5+-23cf5de/bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-23cf5de.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 94.97% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.96x