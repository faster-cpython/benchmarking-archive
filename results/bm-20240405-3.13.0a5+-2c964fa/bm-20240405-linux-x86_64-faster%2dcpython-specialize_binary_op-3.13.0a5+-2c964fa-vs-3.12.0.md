# Results vs. 3.12.0

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 2c964fa
- commit date: 2024-04-05
- overall geometric mean: 1.04x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 267 ms: 1.03x faster                                                             |
| chameleon      | 7.41 ms                                                | 6.93 ms: 1.07x faster                                                            |
| docutils       | 2.77 sec                                               | 2.79 sec: 1.01x slower                                                           |
| tornado_http   | 103 ms                                                 | 94.3 ms: 1.09x faster                                                            |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 472 ms                                                 | 351 ms: 1.35x faster                                                             |
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 444 ms: 1.29x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 912 ms: 1.27x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 934 ms: 1.27x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 460 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 600 ms: 1.21x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 605 ms: 1.20x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 78.2 ms: 1.08x faster                                                            |
| nbody          | 97.0 ms                                                | 95.9 ms: 1.01x faster                                                            |
| pidigits       | 187 ms                                                 | 216 ms: 1.15x slower                                                             |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 135 ms: 1.10x faster                                                             |
| regex_effbot   | 3.61 ms                                                | 3.69 ms: 1.02x slower                                                            |
| regex_dna      | 212 ms                                                 | 218 ms: 1.03x slower                                                             |
| regex_v8       | 23.1 ms                                                | 24.4 ms: 1.05x slower                                                            |
| Geometric mean | (ref)                                                  | 1.00x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.19 sec: 1.06x faster                                                           |
| pickle_pure_python   | 324 us                                                 | 305 us: 1.06x faster                                                             |
| unpickle             | 15.9 us                                                | 15.0 us: 1.06x faster                                                            |
| unpickle_pure_python | 230 us                                                 | 221 us: 1.04x faster                                                             |
| unpickle_list        | 5.29 us                                                | 5.11 us: 1.03x faster                                                            |
| xml_etree_process    | 61.7 ms                                                | 59.8 ms: 1.03x faster                                                            |
| pickle_list          | 5.08 us                                                | 4.93 us: 1.03x faster                                                            |
| xml_etree_generate   | 89.2 ms                                                | 86.7 ms: 1.03x faster                                                            |
| pickle_dict          | 35.5 us                                                | 35.3 us: 1.01x faster                                                            |
| pickle               | 11.6 us                                                | 11.7 us: 1.01x slower                                                            |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                     |

Benchmark hidden because not significant (3): json_loads, xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| python_startup_no_site | 6.94 ms                                                | 8.97 ms: 1.29x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.19x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|-----------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako      | 11.9 ms                                                | 10.7 ms: 1.12x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 114 us: 1.38x faster                                                             |
| async_tree_none            | 472 ms                                                 | 351 ms: 1.35x faster                                                             |
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 444 ms: 1.29x faster                                                             |
| comprehensions             | 21.8 us                                                | 16.8 us: 1.29x faster                                                            |
| async_tree_io              | 1.16 sec                                               | 912 ms: 1.27x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 934 ms: 1.27x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 460 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 600 ms: 1.21x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 605 ms: 1.20x faster                                                             |
| raytrace                   | 312 ms                                                 | 265 ms: 1.18x faster                                                             |
| crypto_pyaes               | 81.9 ms                                                | 69.9 ms: 1.17x faster                                                            |
| deltablue                  | 3.72 ms                                                | 3.22 ms: 1.15x faster                                                            |
| mypy2                      | 830 ms                                                 | 733 ms: 1.13x faster                                                             |
| logging_format             | 7.23 us                                                | 6.47 us: 1.12x faster                                                            |
| mako                       | 11.9 ms                                                | 10.7 ms: 1.12x faster                                                            |
| spectral_norm              | 115 ms                                                 | 103 ms: 1.11x faster                                                             |
| logging_simple             | 6.46 us                                                | 5.81 us: 1.11x faster                                                            |
| regex_compile              | 148 ms                                                 | 135 ms: 1.10x faster                                                             |
| sympy_sum                  | 169 ms                                                 | 154 ms: 1.10x faster                                                             |
| tornado_http               | 103 ms                                                 | 94.3 ms: 1.09x faster                                                            |
| float                      | 84.7 ms                                                | 78.2 ms: 1.08x faster                                                            |
| sympy_str                  | 300 ms                                                 | 279 ms: 1.07x faster                                                             |
| scimark_monte_carlo        | 75.1 ms                                                | 70.3 ms: 1.07x faster                                                            |
| chameleon                  | 7.41 ms                                                | 6.93 ms: 1.07x faster                                                            |
| generators                 | 31.2 ms                                                | 29.3 ms: 1.07x faster                                                            |
| chaos                      | 67.0 ms                                                | 62.8 ms: 1.07x faster                                                            |
| deepcopy_reduce            | 3.35 us                                                | 3.14 us: 1.07x faster                                                            |
| tomli_loads                | 2.33 sec                                               | 2.19 sec: 1.06x faster                                                           |
| pickle_pure_python         | 324 us                                                 | 305 us: 1.06x faster                                                             |
| deepcopy_memo              | 40.7 us                                                | 38.4 us: 1.06x faster                                                            |
| scimark_sor                | 129 ms                                                 | 122 ms: 1.06x faster                                                             |
| sqlglot_transpile          | 1.68 ms                                                | 1.59 ms: 1.06x faster                                                            |
| unpickle                   | 15.9 us                                                | 15.0 us: 1.06x faster                                                            |
| sympy_integrate            | 21.4 ms                                                | 20.3 ms: 1.06x faster                                                            |
| sqlglot_parse              | 1.36 ms                                                | 1.29 ms: 1.05x faster                                                            |
| deepcopy                   | 371 us                                                 | 352 us: 1.05x faster                                                             |
| async_generators           | 463 ms                                                 | 440 ms: 1.05x faster                                                             |
| fannkuch                   | 417 ms                                                 | 397 ms: 1.05x faster                                                             |
| pprint_safe_repr           | 776 ms                                                 | 739 ms: 1.05x faster                                                             |
| scimark_lu                 | 118 ms                                                 | 113 ms: 1.04x faster                                                             |
| unpickle_pure_python       | 230 us                                                 | 221 us: 1.04x faster                                                             |
| pprint_pformat             | 1.57 sec                                               | 1.51 sec: 1.04x faster                                                           |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.87 ms: 1.04x faster                                                            |
| unpickle_list              | 5.29 us                                                | 5.11 us: 1.03x faster                                                            |
| pycparser                  | 1.18 sec                                               | 1.14 sec: 1.03x faster                                                           |
| xml_etree_process          | 61.7 ms                                                | 59.8 ms: 1.03x faster                                                            |
| pickle_list                | 5.08 us                                                | 4.93 us: 1.03x faster                                                            |
| meteor_contest             | 112 ms                                                 | 109 ms: 1.03x faster                                                             |
| pathlib                    | 19.3 ms                                                | 18.8 ms: 1.03x faster                                                            |
| xml_etree_generate         | 89.2 ms                                                | 86.7 ms: 1.03x faster                                                            |
| nqueens                    | 83.3 ms                                                | 81.0 ms: 1.03x faster                                                            |
| sympy_expand               | 478 ms                                                 | 465 ms: 1.03x faster                                                             |
| pyflate                    | 482 ms                                                 | 469 ms: 1.03x faster                                                             |
| 2to3                       | 274 ms                                                 | 267 ms: 1.03x faster                                                             |
| mdp                        | 2.63 sec                                               | 2.58 sec: 1.02x faster                                                           |
| dulwich_log                | 68.5 ms                                                | 67.3 ms: 1.02x faster                                                            |
| bench_thread_pool          | 842 us                                                 | 827 us: 1.02x faster                                                             |
| hexiom                     | 6.41 ms                                                | 6.30 ms: 1.02x faster                                                            |
| scimark_fft                | 382 ms                                                 | 375 ms: 1.02x faster                                                             |
| dask                       | 372 ms                                                 | 366 ms: 1.02x faster                                                             |
| coroutines                 | 23.2 ms                                                | 22.9 ms: 1.01x faster                                                            |
| nbody                      | 97.0 ms                                                | 95.9 ms: 1.01x faster                                                            |
| pickle_dict                | 35.5 us                                                | 35.3 us: 1.01x faster                                                            |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                            |
| logging_silent             | 104 ns                                                 | 105 ns: 1.00x slower                                                             |
| sqlglot_optimize           | 54.8 ms                                                | 55.1 ms: 1.01x slower                                                            |
| pickle                     | 11.6 us                                                | 11.7 us: 1.01x slower                                                            |
| docutils                   | 2.77 sec                                               | 2.79 sec: 1.01x slower                                                           |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                            |
| gunicorn                   | 1.24 ms                                                | 1.26 ms: 1.01x slower                                                            |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.01x slower                                                            |
| sqlglot_normalize          | 110 ms                                                 | 112 ms: 1.01x slower                                                             |
| regex_effbot               | 3.61 ms                                                | 3.69 ms: 1.02x slower                                                            |
| asyncio_websockets         | 551 ms                                                 | 563 ms: 1.02x slower                                                             |
| richards_super             | 51.5 ms                                                | 52.7 ms: 1.02x slower                                                            |
| richards                   | 45.8 ms                                                | 47.0 ms: 1.03x slower                                                            |
| regex_dna                  | 212 ms                                                 | 218 ms: 1.03x slower                                                             |
| sqlite_synth               | 2.83 us                                                | 2.92 us: 1.03x slower                                                            |
| asyncio_tcp                | 491 ms                                                 | 506 ms: 1.03x slower                                                             |
| go                         | 139 ms                                                 | 144 ms: 1.03x slower                                                             |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                                           |
| json                       | 5.26 ms                                                | 5.45 ms: 1.04x slower                                                            |
| gc_traversal               | 3.79 ms                                                | 3.97 ms: 1.05x slower                                                            |
| regex_v8                   | 23.1 ms                                                | 24.4 ms: 1.05x slower                                                            |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| pidigits                   | 187 ms                                                 | 216 ms: 1.15x slower                                                             |
| telco                      | 7.10 ms                                                | 8.43 ms: 1.19x slower                                                            |
| create_gc_cycles           | 1.48 ms                                                | 1.76 ms: 1.19x slower                                                            |
| python_startup_no_site     | 6.94 ms                                                | 8.97 ms: 1.29x slower                                                            |
| coverage                   | 72.7 ms                                                | 98.2 ms: 1.35x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                                     |

Benchmark hidden because not significant (3): json_loads, xml_etree_iterparse, xml_etree_parse
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240405-3.13.0a5+-2c964fa/bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 0.96x