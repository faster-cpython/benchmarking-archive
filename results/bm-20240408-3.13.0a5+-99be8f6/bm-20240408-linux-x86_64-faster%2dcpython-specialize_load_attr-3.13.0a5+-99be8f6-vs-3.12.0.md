# Results vs. 3.12.0

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: 99be8f6
- commit date: 2024-04-08
- overall geometric mean: 1.04x faster
- HPT reliability: 99.89%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 271 ms: 1.01x faster                                                             |
| chameleon      | 7.41 ms                                                | 6.87 ms: 1.08x faster                                                            |
| docutils       | 2.77 sec                                               | 2.83 sec: 1.02x slower                                                           |
| tornado_http   | 103 ms                                                 | 94.5 ms: 1.09x faster                                                            |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 333 ms: 1.35x faster                                                             |
| async_tree_none            | 472 ms                                                 | 350 ms: 1.35x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 442 ms: 1.30x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 918 ms: 1.29x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 918 ms: 1.26x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 459 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 603 ms: 1.20x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 607 ms: 1.20x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 77.5 ms: 1.09x faster                                                            |
| nbody          | 97.0 ms                                                | 89.4 ms: 1.09x faster                                                            |
| pidigits       | 187 ms                                                 | 190 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                  | 1.05x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 135 ms: 1.10x faster                                                             |
| regex_dna      | 212 ms                                                 | 225 ms: 1.06x slower                                                             |
| regex_effbot   | 3.61 ms                                                | 3.85 ms: 1.07x slower                                                            |
| regex_v8       | 23.1 ms                                                | 25.0 ms: 1.08x slower                                                            |
| Geometric mean | (ref)                                                  | 1.03x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_pure_python   | 324 us                                                 | 300 us: 1.08x faster                                                             |
| tomli_loads          | 2.33 sec                                               | 2.17 sec: 1.08x faster                                                           |
| unpickle             | 15.9 us                                                | 14.9 us: 1.07x faster                                                            |
| unpickle_pure_python | 230 us                                                 | 225 us: 1.02x faster                                                             |
| xml_etree_process    | 61.7 ms                                                | 60.9 ms: 1.01x faster                                                            |
| pickle_dict          | 35.5 us                                                | 35.1 us: 1.01x faster                                                            |
| xml_etree_generate   | 89.2 ms                                                | 88.3 ms: 1.01x faster                                                            |
| json_loads           | 28.5 us                                                | 28.6 us: 1.00x slower                                                            |
| pickle               | 11.6 us                                                | 11.7 us: 1.01x slower                                                            |
| pickle_list          | 5.08 us                                                | 5.14 us: 1.01x slower                                                            |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                     |

Benchmark hidden because not significant (3): unpickle_list, xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 10.6 ms: 1.11x slower                                                            |
| python_startup_no_site | 6.94 ms                                                | 9.00 ms: 1.30x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|-----------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako      | 11.9 ms                                                | 10.9 ms: 1.09x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 333 ms: 1.35x faster                                                             |
| async_tree_none            | 472 ms                                                 | 350 ms: 1.35x faster                                                             |
| typing_runtime_protocols   | 158 us                                                 | 117 us: 1.35x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 442 ms: 1.30x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 918 ms: 1.29x faster                                                             |
| comprehensions             | 21.8 us                                                | 17.0 us: 1.28x faster                                                            |
| async_tree_io              | 1.16 sec                                               | 918 ms: 1.26x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 459 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 603 ms: 1.20x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 607 ms: 1.20x faster                                                             |
| raytrace                   | 312 ms                                                 | 263 ms: 1.19x faster                                                             |
| deltablue                  | 3.72 ms                                                | 3.22 ms: 1.16x faster                                                            |
| logging_format             | 7.23 us                                                | 6.29 us: 1.15x faster                                                            |
| logging_simple             | 6.46 us                                                | 5.73 us: 1.13x faster                                                            |
| mypy2                      | 830 ms                                                 | 738 ms: 1.12x faster                                                             |
| chaos                      | 67.0 ms                                                | 60.1 ms: 1.11x faster                                                            |
| deepcopy_memo              | 40.7 us                                                | 36.9 us: 1.10x faster                                                            |
| regex_compile              | 148 ms                                                 | 135 ms: 1.10x faster                                                             |
| scimark_monte_carlo        | 75.1 ms                                                | 68.5 ms: 1.10x faster                                                            |
| crypto_pyaes               | 81.9 ms                                                | 74.9 ms: 1.09x faster                                                            |
| mako                       | 11.9 ms                                                | 10.9 ms: 1.09x faster                                                            |
| float                      | 84.7 ms                                                | 77.5 ms: 1.09x faster                                                            |
| tornado_http               | 103 ms                                                 | 94.5 ms: 1.09x faster                                                            |
| nbody                      | 97.0 ms                                                | 89.4 ms: 1.09x faster                                                            |
| pickle_pure_python         | 324 us                                                 | 300 us: 1.08x faster                                                             |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.08x faster                                                             |
| chameleon                  | 7.41 ms                                                | 6.87 ms: 1.08x faster                                                            |
| tomli_loads                | 2.33 sec                                               | 2.17 sec: 1.08x faster                                                           |
| sympy_str                  | 300 ms                                                 | 279 ms: 1.07x faster                                                             |
| unpickle                   | 15.9 us                                                | 14.9 us: 1.07x faster                                                            |
| sqlglot_transpile          | 1.68 ms                                                | 1.59 ms: 1.06x faster                                                            |
| fannkuch                   | 417 ms                                                 | 394 ms: 1.06x faster                                                             |
| sqlglot_parse              | 1.36 ms                                                | 1.29 ms: 1.06x faster                                                            |
| sympy_integrate            | 21.4 ms                                                | 20.3 ms: 1.05x faster                                                            |
| scimark_sor                | 129 ms                                                 | 123 ms: 1.05x faster                                                             |
| generators                 | 31.2 ms                                                | 29.7 ms: 1.05x faster                                                            |
| deepcopy                   | 371 us                                                 | 353 us: 1.05x faster                                                             |
| deepcopy_reduce            | 3.35 us                                                | 3.20 us: 1.05x faster                                                            |
| async_generators           | 463 ms                                                 | 443 ms: 1.04x faster                                                             |
| logging_silent             | 104 ns                                                 | 101 ns: 1.04x faster                                                             |
| pathlib                    | 19.3 ms                                                | 18.6 ms: 1.04x faster                                                            |
| pprint_safe_repr           | 776 ms                                                 | 751 ms: 1.03x faster                                                             |
| pycparser                  | 1.18 sec                                               | 1.15 sec: 1.03x faster                                                           |
| unpickle_pure_python       | 230 us                                                 | 225 us: 1.02x faster                                                             |
| scimark_lu                 | 118 ms                                                 | 116 ms: 1.02x faster                                                             |
| pprint_pformat             | 1.57 sec                                               | 1.54 sec: 1.02x faster                                                           |
| scimark_fft                | 382 ms                                                 | 375 ms: 1.02x faster                                                             |
| sympy_expand               | 478 ms                                                 | 471 ms: 1.02x faster                                                             |
| nqueens                    | 83.3 ms                                                | 82.2 ms: 1.01x faster                                                            |
| xml_etree_process          | 61.7 ms                                                | 60.9 ms: 1.01x faster                                                            |
| pickle_dict                | 35.5 us                                                | 35.1 us: 1.01x faster                                                            |
| dask                       | 372 ms                                                 | 367 ms: 1.01x faster                                                             |
| dulwich_log                | 68.5 ms                                                | 67.8 ms: 1.01x faster                                                            |
| 2to3                       | 274 ms                                                 | 271 ms: 1.01x faster                                                             |
| xml_etree_generate         | 89.2 ms                                                | 88.3 ms: 1.01x faster                                                            |
| hexiom                     | 6.41 ms                                                | 6.36 ms: 1.01x faster                                                            |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                            |
| bench_thread_pool          | 842 us                                                 | 836 us: 1.01x faster                                                             |
| pyflate                    | 482 ms                                                 | 480 ms: 1.00x faster                                                             |
| json_loads                 | 28.5 us                                                | 28.6 us: 1.00x slower                                                            |
| sqlglot_normalize          | 110 ms                                                 | 111 ms: 1.01x slower                                                             |
| sqlglot_optimize           | 54.8 ms                                                | 55.3 ms: 1.01x slower                                                            |
| pickle                     | 11.6 us                                                | 11.7 us: 1.01x slower                                                            |
| pickle_list                | 5.08 us                                                | 5.14 us: 1.01x slower                                                            |
| pidigits                   | 187 ms                                                 | 190 ms: 1.01x slower                                                             |
| gunicorn                   | 1.24 ms                                                | 1.27 ms: 1.02x slower                                                            |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.02x slower                                                            |
| docutils                   | 2.77 sec                                               | 2.83 sec: 1.02x slower                                                           |
| json                       | 5.26 ms                                                | 5.38 ms: 1.02x slower                                                            |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                            |
| asyncio_tcp                | 491 ms                                                 | 503 ms: 1.03x slower                                                             |
| richards                   | 45.8 ms                                                | 47.0 ms: 1.03x slower                                                            |
| asyncio_websockets         | 551 ms                                                 | 566 ms: 1.03x slower                                                             |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                                           |
| richards_super             | 51.5 ms                                                | 53.0 ms: 1.03x slower                                                            |
| sqlite_synth               | 2.83 us                                                | 2.93 us: 1.03x slower                                                            |
| mdp                        | 2.63 sec                                               | 2.73 sec: 1.04x slower                                                           |
| coroutines                 | 23.2 ms                                                | 24.1 ms: 1.04x slower                                                            |
| go                         | 139 ms                                                 | 146 ms: 1.05x slower                                                             |
| gc_traversal               | 3.79 ms                                                | 4.00 ms: 1.06x slower                                                            |
| regex_dna                  | 212 ms                                                 | 225 ms: 1.06x slower                                                             |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.36 ms: 1.06x slower                                                            |
| regex_effbot               | 3.61 ms                                                | 3.85 ms: 1.07x slower                                                            |
| regex_v8                   | 23.1 ms                                                | 25.0 ms: 1.08x slower                                                            |
| python_startup             | 9.55 ms                                                | 10.6 ms: 1.11x slower                                                            |
| create_gc_cycles           | 1.48 ms                                                | 1.74 ms: 1.18x slower                                                            |
| telco                      | 7.10 ms                                                | 8.61 ms: 1.21x slower                                                            |
| python_startup_no_site     | 6.94 ms                                                | 9.00 ms: 1.30x slower                                                            |
| coverage                   | 72.7 ms                                                | 99.5 ms: 1.37x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                                     |

Benchmark hidden because not significant (5): unpickle_list, xml_etree_iterparse, meteor_contest, spectral_norm, xml_etree_parse
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240408-3.13.0a5+-99be8f6/bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.89% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.96x