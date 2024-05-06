# Results vs. 3.12.0

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 198ceb6
- commit date: 2024-04-03
- overall geometric mean: 1.03x faster
- HPT reliability: 98.60%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.95x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 266 ms: 1.03x faster                                                             |
| chameleon      | 7.41 ms                                                | 6.86 ms: 1.08x faster                                                            |
| tornado_http   | 103 ms                                                 | 95.6 ms: 1.07x faster                                                            |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                     |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 575 ms                                                 | 439 ms: 1.31x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 919 ms: 1.29x faster                                                             |
| async_tree_none_tg         | 450 ms                                                 | 350 ms: 1.28x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 920 ms: 1.26x faster                                                             |
| async_tree_none            | 472 ms                                                 | 378 ms: 1.25x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 463 ms: 1.25x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 594 ms: 1.22x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 605 ms: 1.20x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 80.8 ms: 1.05x faster                                                            |
| pidigits       | 187 ms                                                 | 191 ms: 1.02x slower                                                             |
| nbody          | 97.0 ms                                                | 120 ms: 1.24x slower                                                             |
| Geometric mean | (ref)                                                  | 1.06x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 135 ms: 1.10x faster                                                             |
| regex_effbot   | 3.61 ms                                                | 3.73 ms: 1.03x slower                                                            |
| regex_dna      | 212 ms                                                 | 223 ms: 1.05x slower                                                             |
| regex_v8       | 23.1 ms                                                | 25.3 ms: 1.09x slower                                                            |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 324 us                                                 | 301 us: 1.08x faster                                                             |
| unpickle_pure_python | 230 us                                                 | 215 us: 1.07x faster                                                             |
| pickle_dict          | 35.5 us                                                | 34.0 us: 1.04x faster                                                            |
| xml_etree_generate   | 89.2 ms                                                | 85.9 ms: 1.04x faster                                                            |
| xml_etree_process    | 61.7 ms                                                | 59.6 ms: 1.03x faster                                                            |
| pickle_list          | 5.08 us                                                | 4.93 us: 1.03x faster                                                            |
| tomli_loads          | 2.33 sec                                               | 2.26 sec: 1.03x faster                                                           |
| unpickle_list        | 5.29 us                                                | 5.33 us: 1.01x slower                                                            |
| xml_etree_parse      | 159 ms                                                 | 161 ms: 1.01x slower                                                             |
| xml_etree_iterparse  | 107 ms                                                 | 108 ms: 1.01x slower                                                             |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                     |

Benchmark hidden because not significant (3): json_loads, pickle, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| python_startup_no_site | 6.94 ms                                                | 8.89 ms: 1.28x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.19x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.9 ms: 1.09x faster                                                            |
| django_template | 34.6 ms                                                | 35.1 ms: 1.01x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.04x faster                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 111 us: 1.42x faster                                                             |
| comprehensions             | 21.8 us                                                | 16.5 us: 1.32x faster                                                            |
| async_tree_memoization_tg  | 575 ms                                                 | 439 ms: 1.31x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 919 ms: 1.29x faster                                                             |
| async_tree_none_tg         | 450 ms                                                 | 350 ms: 1.28x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 920 ms: 1.26x faster                                                             |
| async_tree_none            | 472 ms                                                 | 378 ms: 1.25x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 463 ms: 1.25x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 594 ms: 1.22x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 605 ms: 1.20x faster                                                             |
| deltablue                  | 3.72 ms                                                | 3.23 ms: 1.15x faster                                                            |
| mypy2                      | 830 ms                                                 | 739 ms: 1.12x faster                                                             |
| sympy_sum                  | 169 ms                                                 | 152 ms: 1.11x faster                                                             |
| logging_format             | 7.23 us                                                | 6.56 us: 1.10x faster                                                            |
| regex_compile              | 148 ms                                                 | 135 ms: 1.10x faster                                                             |
| sympy_str                  | 300 ms                                                 | 273 ms: 1.10x faster                                                             |
| logging_simple             | 6.46 us                                                | 5.91 us: 1.09x faster                                                            |
| mako                       | 11.9 ms                                                | 10.9 ms: 1.09x faster                                                            |
| raytrace                   | 312 ms                                                 | 288 ms: 1.08x faster                                                             |
| chameleon                  | 7.41 ms                                                | 6.86 ms: 1.08x faster                                                            |
| crypto_pyaes               | 81.9 ms                                                | 75.9 ms: 1.08x faster                                                            |
| pickle_pure_python         | 324 us                                                 | 301 us: 1.08x faster                                                             |
| deepcopy_memo              | 40.7 us                                                | 37.9 us: 1.07x faster                                                            |
| tornado_http               | 103 ms                                                 | 95.6 ms: 1.07x faster                                                            |
| sympy_integrate            | 21.4 ms                                                | 20.0 ms: 1.07x faster                                                            |
| unpickle_pure_python       | 230 us                                                 | 215 us: 1.07x faster                                                             |
| pprint_safe_repr           | 776 ms                                                 | 734 ms: 1.06x faster                                                             |
| deepcopy_reduce            | 3.35 us                                                | 3.17 us: 1.05x faster                                                            |
| sqlglot_transpile          | 1.68 ms                                                | 1.60 ms: 1.05x faster                                                            |
| async_generators           | 463 ms                                                 | 441 ms: 1.05x faster                                                             |
| sqlglot_parse              | 1.36 ms                                                | 1.30 ms: 1.05x faster                                                            |
| float                      | 84.7 ms                                                | 80.8 ms: 1.05x faster                                                            |
| hexiom                     | 6.41 ms                                                | 6.13 ms: 1.05x faster                                                            |
| deepcopy                   | 371 us                                                 | 355 us: 1.05x faster                                                             |
| logging_silent             | 104 ns                                                 | 99.9 ns: 1.05x faster                                                            |
| pickle_dict                | 35.5 us                                                | 34.0 us: 1.04x faster                                                            |
| meteor_contest             | 112 ms                                                 | 108 ms: 1.04x faster                                                             |
| pprint_pformat             | 1.57 sec                                               | 1.51 sec: 1.04x faster                                                           |
| xml_etree_generate         | 89.2 ms                                                | 85.9 ms: 1.04x faster                                                            |
| xml_etree_process          | 61.7 ms                                                | 59.6 ms: 1.03x faster                                                            |
| fannkuch                   | 417 ms                                                 | 404 ms: 1.03x faster                                                             |
| pickle_list                | 5.08 us                                                | 4.93 us: 1.03x faster                                                            |
| scimark_monte_carlo        | 75.1 ms                                                | 72.8 ms: 1.03x faster                                                            |
| tomli_loads                | 2.33 sec                                               | 2.26 sec: 1.03x faster                                                           |
| sympy_expand               | 478 ms                                                 | 464 ms: 1.03x faster                                                             |
| 2to3                       | 274 ms                                                 | 266 ms: 1.03x faster                                                             |
| pathlib                    | 19.3 ms                                                | 18.8 ms: 1.03x faster                                                            |
| generators                 | 31.2 ms                                                | 30.4 ms: 1.03x faster                                                            |
| create_gc_cycles           | 1.48 ms                                                | 1.44 ms: 1.03x faster                                                            |
| gc_traversal               | 3.79 ms                                                | 3.73 ms: 1.02x faster                                                            |
| bench_thread_pool          | 842 us                                                 | 827 us: 1.02x faster                                                             |
| pycparser                  | 1.18 sec                                               | 1.16 sec: 1.02x faster                                                           |
| sqlglot_normalize          | 110 ms                                                 | 110 ms: 1.01x faster                                                             |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                            |
| dulwich_log                | 68.5 ms                                                | 68.2 ms: 1.00x faster                                                            |
| sqlglot_optimize           | 54.8 ms                                                | 55.2 ms: 1.01x slower                                                            |
| scimark_lu                 | 118 ms                                                 | 119 ms: 1.01x slower                                                             |
| unpickle_list              | 5.29 us                                                | 5.33 us: 1.01x slower                                                            |
| xml_etree_parse            | 159 ms                                                 | 161 ms: 1.01x slower                                                             |
| xml_etree_iterparse        | 107 ms                                                 | 108 ms: 1.01x slower                                                             |
| mdp                        | 2.63 sec                                               | 2.66 sec: 1.01x slower                                                           |
| json                       | 5.26 ms                                                | 5.33 ms: 1.01x slower                                                            |
| django_template            | 34.6 ms                                                | 35.1 ms: 1.01x slower                                                            |
| asyncio_tcp                | 491 ms                                                 | 500 ms: 1.02x slower                                                             |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.02x slower                                                            |
| pidigits                   | 187 ms                                                 | 191 ms: 1.02x slower                                                             |
| go                         | 139 ms                                                 | 142 ms: 1.02x slower                                                             |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.83 sec: 1.02x slower                                                           |
| gunicorn                   | 1.24 ms                                                | 1.27 ms: 1.02x slower                                                            |
| chaos                      | 67.0 ms                                                | 68.7 ms: 1.03x slower                                                            |
| asyncio_websockets         | 551 ms                                                 | 566 ms: 1.03x slower                                                             |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                            |
| regex_effbot               | 3.61 ms                                                | 3.73 ms: 1.03x slower                                                            |
| sqlite_synth               | 2.83 us                                                | 2.94 us: 1.04x slower                                                            |
| coroutines                 | 23.2 ms                                                | 24.1 ms: 1.04x slower                                                            |
| scimark_sor                | 129 ms                                                 | 134 ms: 1.04x slower                                                             |
| regex_dna                  | 212 ms                                                 | 223 ms: 1.05x slower                                                             |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.45 ms: 1.08x slower                                                            |
| regex_v8                   | 23.1 ms                                                | 25.3 ms: 1.09x slower                                                            |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| scimark_fft                | 382 ms                                                 | 422 ms: 1.10x slower                                                             |
| telco                      | 7.10 ms                                                | 8.41 ms: 1.18x slower                                                            |
| spectral_norm              | 115 ms                                                 | 140 ms: 1.22x slower                                                             |
| nbody                      | 97.0 ms                                                | 120 ms: 1.24x slower                                                             |
| python_startup_no_site     | 6.94 ms                                                | 8.89 ms: 1.28x slower                                                            |
| coverage                   | 72.7 ms                                                | 98.1 ms: 1.35x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                                     |

Benchmark hidden because not significant (9): dask, nqueens, richards, json_loads, pyflate, pickle, richards_super, docutils, unpickle
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240403-3.13.0a5+-198ceb6/bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 98.60% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.95x