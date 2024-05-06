# Results vs. 3.12.0

- fork: faster-cpython
- ref: stats_for_all_ops
- machine: linux-x86_64
- commit hash: 17ed8bc
- commit date: 2024-04-05
- overall geometric mean: 1.02x faster
- HPT reliability: 97.02%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 269 ms: 1.02x faster                                                          |
| chameleon      | 7.41 ms                                                | 6.99 ms: 1.06x faster                                                         |
| docutils       | 2.77 sec                                               | 2.81 sec: 1.01x slower                                                        |
| tornado_http   | 103 ms                                                 | 94.6 ms: 1.08x faster                                                         |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 333 ms: 1.35x faster                                                          |
| async_tree_none            | 472 ms                                                 | 352 ms: 1.34x faster                                                          |
| async_tree_memoization_tg  | 575 ms                                                 | 441 ms: 1.30x faster                                                          |
| async_tree_io_tg           | 1.18 sec                                               | 928 ms: 1.27x faster                                                          |
| async_tree_memoization     | 578 ms                                                 | 462 ms: 1.25x faster                                                          |
| async_tree_io              | 1.16 sec                                               | 930 ms: 1.24x faster                                                          |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 608 ms: 1.19x faster                                                          |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 615 ms: 1.18x faster                                                          |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 81.0 ms: 1.05x faster                                                         |
| pidigits       | 187 ms                                                 | 191 ms: 1.02x slower                                                          |
| nbody          | 97.0 ms                                                | 116 ms: 1.19x slower                                                          |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 136 ms: 1.09x faster                                                          |
| regex_effbot   | 3.61 ms                                                | 3.87 ms: 1.07x slower                                                         |
| regex_dna      | 212 ms                                                 | 232 ms: 1.09x slower                                                          |
| regex_v8       | 23.1 ms                                                | 26.1 ms: 1.13x slower                                                         |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pickle_pure_python   | 324 us                                                 | 299 us: 1.08x faster                                                          |
| unpickle_pure_python | 230 us                                                 | 217 us: 1.06x faster                                                          |
| tomli_loads          | 2.33 sec                                               | 2.25 sec: 1.03x faster                                                        |
| xml_etree_process    | 61.7 ms                                                | 59.8 ms: 1.03x faster                                                         |
| xml_etree_generate   | 89.2 ms                                                | 86.4 ms: 1.03x faster                                                         |
| pickle_dict          | 35.5 us                                                | 34.5 us: 1.03x faster                                                         |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                         |
| pickle               | 11.6 us                                                | 11.9 us: 1.03x slower                                                         |
| pickle_list          | 5.08 us                                                | 5.26 us: 1.03x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                  |

Benchmark hidden because not significant (5): unpickle_list, xml_etree_iterparse, unpickle, json_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 10.6 ms: 1.11x slower                                                         |
| python_startup_no_site | 6.94 ms                                                | 9.02 ms: 1.30x slower                                                         |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|-----------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| mako      | 11.9 ms                                                | 11.0 ms: 1.08x faster                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 114 us: 1.38x faster                                                          |
| async_tree_none_tg         | 450 ms                                                 | 333 ms: 1.35x faster                                                          |
| async_tree_none            | 472 ms                                                 | 352 ms: 1.34x faster                                                          |
| comprehensions             | 21.8 us                                                | 16.7 us: 1.31x faster                                                         |
| async_tree_memoization_tg  | 575 ms                                                 | 441 ms: 1.30x faster                                                          |
| async_tree_io_tg           | 1.18 sec                                               | 928 ms: 1.27x faster                                                          |
| async_tree_memoization     | 578 ms                                                 | 462 ms: 1.25x faster                                                          |
| async_tree_io              | 1.16 sec                                               | 930 ms: 1.24x faster                                                          |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 608 ms: 1.19x faster                                                          |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 615 ms: 1.18x faster                                                          |
| deltablue                  | 3.72 ms                                                | 3.21 ms: 1.16x faster                                                         |
| mypy2                      | 830 ms                                                 | 739 ms: 1.12x faster                                                          |
| logging_format             | 7.23 us                                                | 6.44 us: 1.12x faster                                                         |
| raytrace                   | 312 ms                                                 | 278 ms: 1.12x faster                                                          |
| crypto_pyaes               | 81.9 ms                                                | 73.0 ms: 1.12x faster                                                         |
| logging_simple             | 6.46 us                                                | 5.78 us: 1.12x faster                                                         |
| regex_compile              | 148 ms                                                 | 136 ms: 1.09x faster                                                          |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.08x faster                                                          |
| tornado_http               | 103 ms                                                 | 94.6 ms: 1.08x faster                                                         |
| mako                       | 11.9 ms                                                | 11.0 ms: 1.08x faster                                                         |
| pickle_pure_python         | 324 us                                                 | 299 us: 1.08x faster                                                          |
| sympy_str                  | 300 ms                                                 | 280 ms: 1.07x faster                                                          |
| deepcopy_memo              | 40.7 us                                                | 38.1 us: 1.07x faster                                                         |
| generators                 | 31.2 ms                                                | 29.4 ms: 1.06x faster                                                         |
| chameleon                  | 7.41 ms                                                | 6.99 ms: 1.06x faster                                                         |
| unpickle_pure_python       | 230 us                                                 | 217 us: 1.06x faster                                                          |
| sqlglot_transpile          | 1.68 ms                                                | 1.60 ms: 1.05x faster                                                         |
| pprint_safe_repr           | 776 ms                                                 | 737 ms: 1.05x faster                                                          |
| sqlglot_parse              | 1.36 ms                                                | 1.30 ms: 1.05x faster                                                         |
| sympy_integrate            | 21.4 ms                                                | 20.4 ms: 1.05x faster                                                         |
| deepcopy_reduce            | 3.35 us                                                | 3.20 us: 1.05x faster                                                         |
| float                      | 84.7 ms                                                | 81.0 ms: 1.05x faster                                                         |
| deepcopy                   | 371 us                                                 | 355 us: 1.04x faster                                                          |
| hexiom                     | 6.41 ms                                                | 6.15 ms: 1.04x faster                                                         |
| async_generators           | 463 ms                                                 | 444 ms: 1.04x faster                                                          |
| pprint_pformat             | 1.57 sec                                               | 1.51 sec: 1.04x faster                                                        |
| meteor_contest             | 112 ms                                                 | 109 ms: 1.04x faster                                                          |
| fannkuch                   | 417 ms                                                 | 404 ms: 1.03x faster                                                          |
| tomli_loads                | 2.33 sec                                               | 2.25 sec: 1.03x faster                                                        |
| xml_etree_process          | 61.7 ms                                                | 59.8 ms: 1.03x faster                                                         |
| xml_etree_generate         | 89.2 ms                                                | 86.4 ms: 1.03x faster                                                         |
| logging_silent             | 104 ns                                                 | 101 ns: 1.03x faster                                                          |
| scimark_monte_carlo        | 75.1 ms                                                | 72.8 ms: 1.03x faster                                                         |
| pickle_dict                | 35.5 us                                                | 34.5 us: 1.03x faster                                                         |
| 2to3                       | 274 ms                                                 | 269 ms: 1.02x faster                                                          |
| bench_thread_pool          | 842 us                                                 | 828 us: 1.02x faster                                                          |
| sympy_expand               | 478 ms                                                 | 471 ms: 1.02x faster                                                          |
| dulwich_log                | 68.5 ms                                                | 67.6 ms: 1.01x faster                                                         |
| scimark_lu                 | 118 ms                                                 | 117 ms: 1.01x faster                                                          |
| pathlib                    | 19.3 ms                                                | 19.1 ms: 1.01x faster                                                         |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                         |
| gc_traversal               | 3.79 ms                                                | 3.80 ms: 1.00x slower                                                         |
| sqlglot_optimize           | 54.8 ms                                                | 54.9 ms: 1.00x slower                                                         |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                         |
| chaos                      | 67.0 ms                                                | 67.8 ms: 1.01x slower                                                         |
| docutils                   | 2.77 sec                                               | 2.81 sec: 1.01x slower                                                        |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.02x slower                                                         |
| pidigits                   | 187 ms                                                 | 191 ms: 1.02x slower                                                          |
| pycparser                  | 1.18 sec                                               | 1.20 sec: 1.02x slower                                                        |
| gunicorn                   | 1.24 ms                                                | 1.27 ms: 1.02x slower                                                         |
| richards                   | 45.8 ms                                                | 46.8 ms: 1.02x slower                                                         |
| asyncio_websockets         | 551 ms                                                 | 563 ms: 1.02x slower                                                          |
| json                       | 5.26 ms                                                | 5.39 ms: 1.03x slower                                                         |
| richards_super             | 51.5 ms                                                | 52.9 ms: 1.03x slower                                                         |
| pickle                     | 11.6 us                                                | 11.9 us: 1.03x slower                                                         |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                                        |
| sqlite_synth               | 2.83 us                                                | 2.93 us: 1.03x slower                                                         |
| pickle_list                | 5.08 us                                                | 5.26 us: 1.03x slower                                                         |
| asyncio_tcp                | 491 ms                                                 | 508 ms: 1.04x slower                                                          |
| go                         | 139 ms                                                 | 145 ms: 1.04x slower                                                          |
| coroutines                 | 23.2 ms                                                | 24.0 ms: 1.04x slower                                                         |
| scimark_sor                | 129 ms                                                 | 134 ms: 1.04x slower                                                          |
| mdp                        | 2.63 sec                                               | 2.79 sec: 1.06x slower                                                        |
| regex_effbot               | 3.61 ms                                                | 3.87 ms: 1.07x slower                                                         |
| regex_dna                  | 212 ms                                                 | 232 ms: 1.09x slower                                                          |
| scimark_fft                | 382 ms                                                 | 419 ms: 1.10x slower                                                          |
| python_startup             | 9.55 ms                                                | 10.6 ms: 1.11x slower                                                         |
| regex_v8                   | 23.1 ms                                                | 26.1 ms: 1.13x slower                                                         |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.74 ms: 1.13x slower                                                         |
| spectral_norm              | 115 ms                                                 | 135 ms: 1.18x slower                                                          |
| create_gc_cycles           | 1.48 ms                                                | 1.75 ms: 1.19x slower                                                         |
| nbody                      | 97.0 ms                                                | 116 ms: 1.19x slower                                                          |
| telco                      | 7.10 ms                                                | 8.63 ms: 1.22x slower                                                         |
| python_startup_no_site     | 6.94 ms                                                | 9.02 ms: 1.30x slower                                                         |
| coverage                   | 72.7 ms                                                | 98.6 ms: 1.36x slower                                                         |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                                  |

Benchmark hidden because not significant (9): dask, unpickle_list, xml_etree_iterparse, unpickle, sqlglot_normalize, pyflate, nqueens, json_loads, xml_etree_parse
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240405-3.13.0a5+-17ed8bc/bm-20240405-linux-x86_64-faster%2dcpython-stats_for_all_ops-3.13.0a5+-17ed8bc.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 97.02% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.96x