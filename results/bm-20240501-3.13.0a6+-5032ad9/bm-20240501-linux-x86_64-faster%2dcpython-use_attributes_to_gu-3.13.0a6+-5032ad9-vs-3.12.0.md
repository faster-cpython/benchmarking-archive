# Results vs. 3.12.0

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: 5032ad9
- commit date: 2024-05-01
- overall geometric mean: 1.03x faster
- HPT reliability: 99.86%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 272 ms: 1.01x faster                                                             |
| chameleon      | 7.41 ms                                                | 7.26 ms: 1.02x faster                                                            |
| docutils       | 2.77 sec                                               | 2.82 sec: 1.02x slower                                                           |
| tornado_http   | 103 ms                                                 | 93.6 ms: 1.10x faster                                                            |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                                             |
| async_tree_none            | 472 ms                                                 | 356 ms: 1.33x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 441 ms: 1.30x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 929 ms: 1.27x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 920 ms: 1.26x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 468 ms: 1.23x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 610 ms: 1.19x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 613 ms: 1.18x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 88.3 ms: 1.10x faster                                                            |
| float          | 84.7 ms                                                | 77.9 ms: 1.09x faster                                                            |
| pidigits       | 187 ms                                                 | 191 ms: 1.02x slower                                                             |
| Geometric mean | (ref)                                                  | 1.05x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 134 ms: 1.10x faster                                                             |
| regex_effbot   | 3.61 ms                                                | 3.89 ms: 1.08x slower                                                            |
| regex_dna      | 212 ms                                                 | 230 ms: 1.09x slower                                                             |
| regex_v8       | 23.1 ms                                                | 25.8 ms: 1.11x slower                                                            |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.17 sec: 1.08x faster                                                           |
| unpickle_pure_python | 230 us                                                 | 217 us: 1.06x faster                                                             |
| pickle_pure_python   | 324 us                                                 | 311 us: 1.04x faster                                                             |
| unpickle             | 15.9 us                                                | 15.3 us: 1.04x faster                                                            |
| pickle_dict          | 35.5 us                                                | 34.7 us: 1.03x faster                                                            |
| pickle_list          | 5.08 us                                                | 5.05 us: 1.01x faster                                                            |
| json_loads           | 28.5 us                                                | 28.4 us: 1.01x faster                                                            |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                            |
| pickle               | 11.6 us                                                | 12.0 us: 1.03x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (5): xml_etree_parse, unpickle_list, xml_etree_generate, xml_etree_process, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.09 ms: 1.02x slower                                                            |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 11.9 ms                                                | 11.5 ms: 1.04x faster                                                            |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                     |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                                             |
| comprehensions             | 21.8 us                                                | 16.4 us: 1.33x faster                                                            |
| async_tree_none            | 472 ms                                                 | 356 ms: 1.33x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 441 ms: 1.30x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 929 ms: 1.27x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 920 ms: 1.26x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 468 ms: 1.23x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 610 ms: 1.19x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 613 ms: 1.18x faster                                                             |
| raytrace                   | 312 ms                                                 | 267 ms: 1.17x faster                                                             |
| deltablue                  | 3.72 ms                                                | 3.22 ms: 1.16x faster                                                            |
| logging_format             | 7.23 us                                                | 6.39 us: 1.13x faster                                                            |
| mypy2                      | 830 ms                                                 | 738 ms: 1.13x faster                                                             |
| logging_simple             | 6.46 us                                                | 5.80 us: 1.11x faster                                                            |
| regex_compile              | 148 ms                                                 | 134 ms: 1.10x faster                                                             |
| chaos                      | 67.0 ms                                                | 60.6 ms: 1.10x faster                                                            |
| pathlib                    | 19.3 ms                                                | 17.6 ms: 1.10x faster                                                            |
| nbody                      | 97.0 ms                                                | 88.3 ms: 1.10x faster                                                            |
| tornado_http               | 103 ms                                                 | 93.6 ms: 1.10x faster                                                            |
| sympy_sum                  | 169 ms                                                 | 155 ms: 1.09x faster                                                             |
| float                      | 84.7 ms                                                | 77.9 ms: 1.09x faster                                                            |
| crypto_pyaes               | 81.9 ms                                                | 75.6 ms: 1.08x faster                                                            |
| sympy_str                  | 300 ms                                                 | 278 ms: 1.08x faster                                                             |
| tomli_loads                | 2.33 sec                                               | 2.17 sec: 1.08x faster                                                           |
| generators                 | 31.2 ms                                                | 29.1 ms: 1.07x faster                                                            |
| deepcopy_memo              | 40.7 us                                                | 38.0 us: 1.07x faster                                                            |
| scimark_monte_carlo        | 75.1 ms                                                | 70.5 ms: 1.07x faster                                                            |
| logging_silent             | 104 ns                                                 | 98.1 ns: 1.06x faster                                                            |
| unpickle_pure_python       | 230 us                                                 | 217 us: 1.06x faster                                                             |
| sqlglot_transpile          | 1.68 ms                                                | 1.60 ms: 1.05x faster                                                            |
| sympy_integrate            | 21.4 ms                                                | 20.3 ms: 1.05x faster                                                            |
| coroutines                 | 23.2 ms                                                | 22.0 ms: 1.05x faster                                                            |
| sqlglot_parse              | 1.36 ms                                                | 1.29 ms: 1.05x faster                                                            |
| nqueens                    | 83.3 ms                                                | 79.6 ms: 1.05x faster                                                            |
| spectral_norm              | 115 ms                                                 | 110 ms: 1.05x faster                                                             |
| dulwich_log                | 68.5 ms                                                | 65.6 ms: 1.04x faster                                                            |
| pickle_pure_python         | 324 us                                                 | 311 us: 1.04x faster                                                             |
| hexiom                     | 6.41 ms                                                | 6.16 ms: 1.04x faster                                                            |
| async_generators           | 463 ms                                                 | 445 ms: 1.04x faster                                                             |
| mako                       | 11.9 ms                                                | 11.5 ms: 1.04x faster                                                            |
| deepcopy_reduce            | 3.35 us                                                | 3.22 us: 1.04x faster                                                            |
| unpickle                   | 15.9 us                                                | 15.3 us: 1.04x faster                                                            |
| fannkuch                   | 417 ms                                                 | 403 ms: 1.03x faster                                                             |
| deepcopy                   | 371 us                                                 | 361 us: 1.03x faster                                                             |
| pickle_dict                | 35.5 us                                                | 34.7 us: 1.03x faster                                                            |
| pprint_safe_repr           | 776 ms                                                 | 758 ms: 1.02x faster                                                             |
| bench_thread_pool          | 842 us                                                 | 824 us: 1.02x faster                                                             |
| chameleon                  | 7.41 ms                                                | 7.26 ms: 1.02x faster                                                            |
| sympy_expand               | 478 ms                                                 | 470 ms: 1.02x faster                                                             |
| meteor_contest             | 112 ms                                                 | 111 ms: 1.02x faster                                                             |
| scimark_fft                | 382 ms                                                 | 377 ms: 1.01x faster                                                             |
| pprint_pformat             | 1.57 sec                                               | 1.55 sec: 1.01x faster                                                           |
| 2to3                       | 274 ms                                                 | 272 ms: 1.01x faster                                                             |
| pickle_list                | 5.08 us                                                | 5.05 us: 1.01x faster                                                            |
| json_loads                 | 28.5 us                                                | 28.4 us: 1.01x faster                                                            |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.00x faster                                                            |
| scimark_lu                 | 118 ms                                                 | 118 ms: 1.00x faster                                                             |
| pyflate                    | 482 ms                                                 | 480 ms: 1.00x faster                                                             |
| sqlglot_normalize          | 110 ms                                                 | 110 ms: 1.00x faster                                                             |
| scimark_sor                | 129 ms                                                 | 131 ms: 1.01x slower                                                             |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                            |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.02x slower                                                            |
| pidigits                   | 187 ms                                                 | 191 ms: 1.02x slower                                                             |
| docutils                   | 2.77 sec                                               | 2.82 sec: 1.02x slower                                                           |
| json                       | 5.26 ms                                                | 5.37 ms: 1.02x slower                                                            |
| python_startup_no_site     | 6.94 ms                                                | 7.09 ms: 1.02x slower                                                            |
| asyncio_websockets         | 551 ms                                                 | 563 ms: 1.02x slower                                                             |
| pycparser                  | 1.18 sec                                               | 1.21 sec: 1.03x slower                                                           |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                                           |
| gunicorn                   | 1.24 ms                                                | 1.28 ms: 1.03x slower                                                            |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.21 ms: 1.03x slower                                                            |
| pickle                     | 11.6 us                                                | 12.0 us: 1.03x slower                                                            |
| go                         | 139 ms                                                 | 144 ms: 1.03x slower                                                             |
| mdp                        | 2.63 sec                                               | 2.72 sec: 1.03x slower                                                           |
| sqlite_synth               | 2.83 us                                                | 2.95 us: 1.04x slower                                                            |
| typing_runtime_protocols   | 158 us                                                 | 164 us: 1.04x slower                                                             |
| asyncio_tcp                | 491 ms                                                 | 511 ms: 1.04x slower                                                             |
| gc_traversal               | 3.79 ms                                                | 3.98 ms: 1.05x slower                                                            |
| richards                   | 45.8 ms                                                | 48.3 ms: 1.05x slower                                                            |
| richards_super             | 51.5 ms                                                | 54.6 ms: 1.06x slower                                                            |
| regex_effbot               | 3.61 ms                                                | 3.89 ms: 1.08x slower                                                            |
| regex_dna                  | 212 ms                                                 | 230 ms: 1.09x slower                                                             |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| regex_v8                   | 23.1 ms                                                | 25.8 ms: 1.11x slower                                                            |
| create_gc_cycles           | 1.48 ms                                                | 1.75 ms: 1.18x slower                                                            |
| telco                      | 7.10 ms                                                | 8.53 ms: 1.20x slower                                                            |
| coverage                   | 72.7 ms                                                | 93.0 ms: 1.28x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                                     |

Benchmark hidden because not significant (8): dask, xml_etree_parse, unpickle_list, xml_etree_generate, xml_etree_process, django_template, sqlglot_optimize, xml_etree_iterparse
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240501-3.13.0a6+-5032ad9/bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.86% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.96x