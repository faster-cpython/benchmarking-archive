# Results vs. 3.12.0

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: accc60a
- commit date: 2024-04-04
- overall geometric mean: 1.02x faster
- HPT reliability: 93.78%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 268 ms: 1.02x faster                                                             |
| chameleon      | 7.41 ms                                                | 6.96 ms: 1.07x faster                                                            |
| docutils       | 2.77 sec                                               | 2.78 sec: 1.01x slower                                                           |
| tornado_http   | 103 ms                                                 | 94.3 ms: 1.09x faster                                                            |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 333 ms: 1.35x faster                                                             |
| async_tree_none            | 472 ms                                                 | 350 ms: 1.35x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 441 ms: 1.30x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 928 ms: 1.27x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 918 ms: 1.26x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 459 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 602 ms: 1.21x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 608 ms: 1.19x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 81.7 ms: 1.04x faster                                                            |
| pidigits       | 187 ms                                                 | 195 ms: 1.04x slower                                                             |
| nbody          | 97.0 ms                                                | 127 ms: 1.31x slower                                                             |
| Geometric mean | (ref)                                                  | 1.09x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 135 ms: 1.10x faster                                                             |
| regex_effbot   | 3.61 ms                                                | 3.66 ms: 1.01x slower                                                            |
| regex_dna      | 212 ms                                                 | 227 ms: 1.07x slower                                                             |
| regex_v8       | 23.1 ms                                                | 25.4 ms: 1.10x slower                                                            |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 324 us                                                 | 297 us: 1.09x faster                                                             |
| unpickle_pure_python | 230 us                                                 | 219 us: 1.05x faster                                                             |
| unpickle_list        | 5.29 us                                                | 5.09 us: 1.04x faster                                                            |
| tomli_loads          | 2.33 sec                                               | 2.26 sec: 1.03x faster                                                           |
| xml_etree_process    | 61.7 ms                                                | 61.1 ms: 1.01x faster                                                            |
| pickle_dict          | 35.5 us                                                | 35.2 us: 1.01x faster                                                            |
| xml_etree_generate   | 89.2 ms                                                | 88.6 ms: 1.01x faster                                                            |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                            |
| pickle_list          | 5.08 us                                                | 5.26 us: 1.03x slower                                                            |
| pickle               | 11.6 us                                                | 12.0 us: 1.04x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (4): unpickle, xml_etree_iterparse, json_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 10.6 ms: 1.11x slower                                                            |
| python_startup_no_site | 6.94 ms                                                | 9.01 ms: 1.30x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|-----------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako      | 11.9 ms                                                | 11.0 ms: 1.08x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 113 us: 1.39x faster                                                             |
| async_tree_none_tg         | 450 ms                                                 | 333 ms: 1.35x faster                                                             |
| async_tree_none            | 472 ms                                                 | 350 ms: 1.35x faster                                                             |
| comprehensions             | 21.8 us                                                | 16.3 us: 1.33x faster                                                            |
| async_tree_memoization_tg  | 575 ms                                                 | 441 ms: 1.30x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 928 ms: 1.27x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 918 ms: 1.26x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 459 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 602 ms: 1.21x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 608 ms: 1.19x faster                                                             |
| deltablue                  | 3.72 ms                                                | 3.17 ms: 1.17x faster                                                            |
| mypy2                      | 830 ms                                                 | 736 ms: 1.13x faster                                                             |
| logging_format             | 7.23 us                                                | 6.43 us: 1.12x faster                                                            |
| logging_simple             | 6.46 us                                                | 5.75 us: 1.12x faster                                                            |
| deepcopy_memo              | 40.7 us                                                | 36.5 us: 1.12x faster                                                            |
| raytrace                   | 312 ms                                                 | 280 ms: 1.11x faster                                                             |
| regex_compile              | 148 ms                                                 | 135 ms: 1.10x faster                                                             |
| crypto_pyaes               | 81.9 ms                                                | 75.0 ms: 1.09x faster                                                            |
| pickle_pure_python         | 324 us                                                 | 297 us: 1.09x faster                                                             |
| tornado_http               | 103 ms                                                 | 94.3 ms: 1.09x faster                                                            |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.09x faster                                                             |
| mako                       | 11.9 ms                                                | 11.0 ms: 1.08x faster                                                            |
| sympy_str                  | 300 ms                                                 | 278 ms: 1.08x faster                                                             |
| deepcopy_reduce            | 3.35 us                                                | 3.12 us: 1.07x faster                                                            |
| deepcopy                   | 371 us                                                 | 347 us: 1.07x faster                                                             |
| chameleon                  | 7.41 ms                                                | 6.96 ms: 1.07x faster                                                            |
| pprint_safe_repr           | 776 ms                                                 | 733 ms: 1.06x faster                                                             |
| sqlglot_transpile          | 1.68 ms                                                | 1.59 ms: 1.06x faster                                                            |
| generators                 | 31.2 ms                                                | 29.6 ms: 1.06x faster                                                            |
| sympy_integrate            | 21.4 ms                                                | 20.3 ms: 1.06x faster                                                            |
| logging_silent             | 104 ns                                                 | 99.2 ns: 1.05x faster                                                            |
| sqlglot_parse              | 1.36 ms                                                | 1.29 ms: 1.05x faster                                                            |
| unpickle_pure_python       | 230 us                                                 | 219 us: 1.05x faster                                                             |
| async_generators           | 463 ms                                                 | 444 ms: 1.04x faster                                                             |
| pprint_pformat             | 1.57 sec                                               | 1.50 sec: 1.04x faster                                                           |
| unpickle_list              | 5.29 us                                                | 5.09 us: 1.04x faster                                                            |
| float                      | 84.7 ms                                                | 81.7 ms: 1.04x faster                                                            |
| meteor_contest             | 112 ms                                                 | 109 ms: 1.03x faster                                                             |
| tomli_loads                | 2.33 sec                                               | 2.26 sec: 1.03x faster                                                           |
| pathlib                    | 19.3 ms                                                | 18.8 ms: 1.03x faster                                                            |
| scimark_monte_carlo        | 75.1 ms                                                | 73.0 ms: 1.03x faster                                                            |
| sympy_expand               | 478 ms                                                 | 466 ms: 1.03x faster                                                             |
| 2to3                       | 274 ms                                                 | 268 ms: 1.02x faster                                                             |
| hexiom                     | 6.41 ms                                                | 6.30 ms: 1.02x faster                                                            |
| bench_thread_pool          | 842 us                                                 | 828 us: 1.02x faster                                                             |
| dulwich_log                | 68.5 ms                                                | 67.6 ms: 1.01x faster                                                            |
| xml_etree_process          | 61.7 ms                                                | 61.1 ms: 1.01x faster                                                            |
| pickle_dict                | 35.5 us                                                | 35.2 us: 1.01x faster                                                            |
| fannkuch                   | 417 ms                                                 | 414 ms: 1.01x faster                                                             |
| sqlglot_normalize          | 110 ms                                                 | 109 ms: 1.01x faster                                                             |
| xml_etree_generate         | 89.2 ms                                                | 88.6 ms: 1.01x faster                                                            |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                            |
| sqlglot_optimize           | 54.8 ms                                                | 54.7 ms: 1.00x faster                                                            |
| docutils                   | 2.77 sec                                               | 2.78 sec: 1.01x slower                                                           |
| nqueens                    | 83.3 ms                                                | 83.8 ms: 1.01x slower                                                            |
| mdp                        | 2.63 sec                                               | 2.65 sec: 1.01x slower                                                           |
| pyflate                    | 482 ms                                                 | 486 ms: 1.01x slower                                                             |
| richards                   | 45.8 ms                                                | 46.2 ms: 1.01x slower                                                            |
| richards_super             | 51.5 ms                                                | 52.0 ms: 1.01x slower                                                            |
| pycparser                  | 1.18 sec                                               | 1.19 sec: 1.01x slower                                                           |
| aiohttp                    | 1.15 ms                                                | 1.16 ms: 1.01x slower                                                            |
| regex_effbot               | 3.61 ms                                                | 3.66 ms: 1.01x slower                                                            |
| gunicorn                   | 1.24 ms                                                | 1.26 ms: 1.02x slower                                                            |
| asyncio_websockets         | 551 ms                                                 | 563 ms: 1.02x slower                                                             |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                            |
| scimark_lu                 | 118 ms                                                 | 121 ms: 1.03x slower                                                             |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                                           |
| json                       | 5.26 ms                                                | 5.43 ms: 1.03x slower                                                            |
| pickle_list                | 5.08 us                                                | 5.26 us: 1.03x slower                                                            |
| pickle                     | 11.6 us                                                | 12.0 us: 1.04x slower                                                            |
| asyncio_tcp                | 491 ms                                                 | 510 ms: 1.04x slower                                                             |
| pidigits                   | 187 ms                                                 | 195 ms: 1.04x slower                                                             |
| coroutines                 | 23.2 ms                                                | 24.1 ms: 1.04x slower                                                            |
| scimark_sor                | 129 ms                                                 | 135 ms: 1.04x slower                                                             |
| chaos                      | 67.0 ms                                                | 69.9 ms: 1.04x slower                                                            |
| sqlite_synth               | 2.83 us                                                | 2.96 us: 1.04x slower                                                            |
| go                         | 139 ms                                                 | 146 ms: 1.05x slower                                                             |
| gc_traversal               | 3.79 ms                                                | 4.02 ms: 1.06x slower                                                            |
| regex_dna                  | 212 ms                                                 | 227 ms: 1.07x slower                                                             |
| regex_v8                   | 23.1 ms                                                | 25.4 ms: 1.10x slower                                                            |
| python_startup             | 9.55 ms                                                | 10.6 ms: 1.11x slower                                                            |
| scimark_fft                | 382 ms                                                 | 427 ms: 1.12x slower                                                             |
| create_gc_cycles           | 1.48 ms                                                | 1.75 ms: 1.18x slower                                                            |
| telco                      | 7.10 ms                                                | 8.60 ms: 1.21x slower                                                            |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 6.13 ms: 1.21x slower                                                            |
| spectral_norm              | 115 ms                                                 | 141 ms: 1.23x slower                                                             |
| python_startup_no_site     | 6.94 ms                                                | 9.01 ms: 1.30x slower                                                            |
| nbody                      | 97.0 ms                                                | 127 ms: 1.31x slower                                                             |
| coverage                   | 72.7 ms                                                | 101 ms: 1.38x slower                                                             |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                                     |

Benchmark hidden because not significant (5): unpickle, dask, xml_etree_iterparse, json_loads, xml_etree_parse
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240404-3.13.0a5+-accc60a/bm-20240404-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-accc60a.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 93.78% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.96x