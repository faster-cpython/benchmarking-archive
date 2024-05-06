# Results vs. 3.12.0

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: 846a7ef
- commit date: 2024-05-01
- overall geometric mean: 1.04x faster
- HPT reliability: 99.98%
- HPT 99th percentile: 1.01x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 272 ms: 1.01x faster                                                             |
| chameleon      | 7.41 ms                                                | 7.03 ms: 1.05x faster                                                            |
| docutils       | 2.77 sec                                               | 2.82 sec: 1.02x slower                                                           |
| tornado_http   | 103 ms                                                 | 93.7 ms: 1.10x faster                                                            |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 472 ms                                                 | 353 ms: 1.34x faster                                                             |
| async_tree_none_tg         | 450 ms                                                 | 341 ms: 1.32x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 452 ms: 1.27x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 914 ms: 1.26x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 937 ms: 1.26x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 459 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 610 ms: 1.19x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 614 ms: 1.18x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 78.2 ms: 1.08x faster                                                            |
| nbody          | 97.0 ms                                                | 89.6 ms: 1.08x faster                                                            |
| pidigits       | 187 ms                                                 | 190 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                  | 1.05x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 134 ms: 1.11x faster                                                             |
| regex_dna      | 212 ms                                                 | 221 ms: 1.04x slower                                                             |
| regex_effbot   | 3.61 ms                                                | 3.77 ms: 1.04x slower                                                            |
| regex_v8       | 23.1 ms                                                | 24.4 ms: 1.06x slower                                                            |
| Geometric mean | (ref)                                                  | 1.01x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.16 sec: 1.08x faster                                                           |
| unpickle             | 15.9 us                                                | 15.0 us: 1.06x faster                                                            |
| unpickle_pure_python | 230 us                                                 | 218 us: 1.05x faster                                                             |
| unpickle_list        | 5.29 us                                                | 5.18 us: 1.02x faster                                                            |
| pickle_dict          | 35.5 us                                                | 34.8 us: 1.02x faster                                                            |
| pickle_list          | 5.08 us                                                | 5.00 us: 1.02x faster                                                            |
| pickle_pure_python   | 324 us                                                 | 318 us: 1.02x faster                                                             |
| xml_etree_generate   | 89.2 ms                                                | 88.4 ms: 1.01x faster                                                            |
| json_dumps           | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                     |

Benchmark hidden because not significant (5): xml_etree_parse, xml_etree_process, pickle, json_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.09 ms: 1.02x slower                                                            |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 11.4 ms: 1.04x faster                                                            |
| django_template | 34.6 ms                                                | 34.9 ms: 1.01x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 472 ms                                                 | 353 ms: 1.34x faster                                                             |
| async_tree_none_tg         | 450 ms                                                 | 341 ms: 1.32x faster                                                             |
| comprehensions             | 21.8 us                                                | 16.7 us: 1.30x faster                                                            |
| async_tree_memoization_tg  | 575 ms                                                 | 452 ms: 1.27x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 914 ms: 1.26x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 937 ms: 1.26x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 459 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 610 ms: 1.19x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 614 ms: 1.18x faster                                                             |
| raytrace                   | 312 ms                                                 | 266 ms: 1.17x faster                                                             |
| go                         | 139 ms                                                 | 119 ms: 1.17x faster                                                             |
| deltablue                  | 3.72 ms                                                | 3.23 ms: 1.15x faster                                                            |
| mypy2                      | 830 ms                                                 | 739 ms: 1.12x faster                                                             |
| logging_format             | 7.23 us                                                | 6.44 us: 1.12x faster                                                            |
| logging_simple             | 6.46 us                                                | 5.78 us: 1.12x faster                                                            |
| chaos                      | 67.0 ms                                                | 60.1 ms: 1.11x faster                                                            |
| regex_compile              | 148 ms                                                 | 134 ms: 1.11x faster                                                             |
| pathlib                    | 19.3 ms                                                | 17.6 ms: 1.10x faster                                                            |
| sympy_sum                  | 169 ms                                                 | 154 ms: 1.10x faster                                                             |
| tornado_http               | 103 ms                                                 | 93.7 ms: 1.10x faster                                                            |
| float                      | 84.7 ms                                                | 78.2 ms: 1.08x faster                                                            |
| nbody                      | 97.0 ms                                                | 89.6 ms: 1.08x faster                                                            |
| tomli_loads                | 2.33 sec                                               | 2.16 sec: 1.08x faster                                                           |
| sympy_str                  | 300 ms                                                 | 279 ms: 1.07x faster                                                             |
| deepcopy_memo              | 40.7 us                                                | 38.1 us: 1.07x faster                                                            |
| generators                 | 31.2 ms                                                | 29.2 ms: 1.07x faster                                                            |
| unpickle                   | 15.9 us                                                | 15.0 us: 1.06x faster                                                            |
| nqueens                    | 83.3 ms                                                | 78.9 ms: 1.06x faster                                                            |
| sqlglot_parse              | 1.36 ms                                                | 1.29 ms: 1.05x faster                                                            |
| sqlglot_transpile          | 1.68 ms                                                | 1.60 ms: 1.05x faster                                                            |
| unpickle_pure_python       | 230 us                                                 | 218 us: 1.05x faster                                                             |
| sympy_integrate            | 21.4 ms                                                | 20.3 ms: 1.05x faster                                                            |
| chameleon                  | 7.41 ms                                                | 7.03 ms: 1.05x faster                                                            |
| deepcopy                   | 371 us                                                 | 354 us: 1.05x faster                                                             |
| mako                       | 11.9 ms                                                | 11.4 ms: 1.04x faster                                                            |
| scimark_fft                | 382 ms                                                 | 367 ms: 1.04x faster                                                             |
| fannkuch                   | 417 ms                                                 | 402 ms: 1.04x faster                                                             |
| async_generators           | 463 ms                                                 | 446 ms: 1.04x faster                                                             |
| dulwich_log                | 68.5 ms                                                | 66.1 ms: 1.04x faster                                                            |
| deepcopy_reduce            | 3.35 us                                                | 3.23 us: 1.04x faster                                                            |
| scimark_lu                 | 118 ms                                                 | 114 ms: 1.04x faster                                                             |
| pprint_safe_repr           | 776 ms                                                 | 751 ms: 1.03x faster                                                             |
| coroutines                 | 23.2 ms                                                | 22.5 ms: 1.03x faster                                                            |
| pycparser                  | 1.18 sec                                               | 1.15 sec: 1.02x faster                                                           |
| unpickle_list              | 5.29 us                                                | 5.18 us: 1.02x faster                                                            |
| hexiom                     | 6.41 ms                                                | 6.28 ms: 1.02x faster                                                            |
| meteor_contest             | 112 ms                                                 | 110 ms: 1.02x faster                                                             |
| pickle_dict                | 35.5 us                                                | 34.8 us: 1.02x faster                                                            |
| spectral_norm              | 115 ms                                                 | 113 ms: 1.02x faster                                                             |
| pickle_list                | 5.08 us                                                | 5.00 us: 1.02x faster                                                            |
| pickle_pure_python         | 324 us                                                 | 318 us: 1.02x faster                                                             |
| pprint_pformat             | 1.57 sec                                               | 1.54 sec: 1.02x faster                                                           |
| scimark_monte_carlo        | 75.1 ms                                                | 73.9 ms: 1.02x faster                                                            |
| mdp                        | 2.63 sec                                               | 2.59 sec: 1.02x faster                                                           |
| pyflate                    | 482 ms                                                 | 476 ms: 1.01x faster                                                             |
| dask                       | 372 ms                                                 | 367 ms: 1.01x faster                                                             |
| bench_thread_pool          | 842 us                                                 | 831 us: 1.01x faster                                                             |
| logging_silent             | 104 ns                                                 | 103 ns: 1.01x faster                                                             |
| gc_traversal               | 3.79 ms                                                | 3.75 ms: 1.01x faster                                                            |
| sympy_expand               | 478 ms                                                 | 473 ms: 1.01x faster                                                             |
| 2to3                       | 274 ms                                                 | 272 ms: 1.01x faster                                                             |
| xml_etree_generate         | 89.2 ms                                                | 88.4 ms: 1.01x faster                                                            |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.00x faster                                                            |
| sqlglot_optimize           | 54.8 ms                                                | 55.1 ms: 1.00x slower                                                            |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.10 ms: 1.01x slower                                                            |
| django_template            | 34.6 ms                                                | 34.9 ms: 1.01x slower                                                            |
| pidigits                   | 187 ms                                                 | 190 ms: 1.01x slower                                                             |
| typing_runtime_protocols   | 158 us                                                 | 161 us: 1.02x slower                                                             |
| docutils                   | 2.77 sec                                               | 2.82 sec: 1.02x slower                                                           |
| crypto_pyaes               | 81.9 ms                                                | 83.5 ms: 1.02x slower                                                            |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.02x slower                                                            |
| python_startup_no_site     | 6.94 ms                                                | 7.09 ms: 1.02x slower                                                            |
| asyncio_websockets         | 551 ms                                                 | 564 ms: 1.02x slower                                                             |
| json                       | 5.26 ms                                                | 5.39 ms: 1.02x slower                                                            |
| scimark_sor                | 129 ms                                                 | 132 ms: 1.02x slower                                                             |
| gunicorn                   | 1.24 ms                                                | 1.27 ms: 1.03x slower                                                            |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                                           |
| regex_dna                  | 212 ms                                                 | 221 ms: 1.04x slower                                                             |
| json_dumps                 | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                            |
| asyncio_tcp                | 491 ms                                                 | 511 ms: 1.04x slower                                                             |
| richards_super             | 51.5 ms                                                | 53.7 ms: 1.04x slower                                                            |
| regex_effbot               | 3.61 ms                                                | 3.77 ms: 1.04x slower                                                            |
| richards                   | 45.8 ms                                                | 47.9 ms: 1.04x slower                                                            |
| sqlite_synth               | 2.83 us                                                | 2.96 us: 1.04x slower                                                            |
| regex_v8                   | 23.1 ms                                                | 24.4 ms: 1.06x slower                                                            |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| create_gc_cycles           | 1.48 ms                                                | 1.75 ms: 1.18x slower                                                            |
| telco                      | 7.10 ms                                                | 8.62 ms: 1.21x slower                                                            |
| coverage                   | 72.7 ms                                                | 96.8 ms: 1.33x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                                     |

Benchmark hidden because not significant (6): xml_etree_parse, xml_etree_process, pickle, json_loads, sqlglot_normalize, xml_etree_iterparse
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240501-3.13.0a6+-846a7ef/bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.98% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 0.96x