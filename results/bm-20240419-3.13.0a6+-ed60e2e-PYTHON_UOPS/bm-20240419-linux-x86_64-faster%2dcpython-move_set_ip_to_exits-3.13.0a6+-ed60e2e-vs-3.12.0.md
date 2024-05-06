# Results vs. 3.12.0

- fork: faster-cpython
- ref: move_set_ip_to_exits
- machine: linux-x86_64
- commit hash: ed60e2e
- commit date: 2024-04-19
- overall geometric mean: 1.09x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 311 ms: 1.13x slower                                                             |
| chameleon      | 7.41 ms                                                | 8.08 ms: 1.09x slower                                                            |
| docutils       | 2.77 sec                                               | 3.15 sec: 1.14x slower                                                           |
| Geometric mean | (ref)                                                  | 1.09x slower                                                                     |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 472 ms                                                 | 383 ms: 1.23x faster                                                             |
| async_tree_none_tg         | 450 ms                                                 | 367 ms: 1.23x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 476 ms: 1.21x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 968 ms: 1.19x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 1000 ms: 1.18x faster                                                            |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 640 ms: 1.13x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 511 ms: 1.13x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 646 ms: 1.12x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.18x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                 | 200 ms: 1.07x slower                                                             |
| float          | 84.7 ms                                                | 93.3 ms: 1.10x slower                                                            |
| nbody          | 97.0 ms                                                | 127 ms: 1.31x slower                                                             |
| Geometric mean | (ref)                                                  | 1.15x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.61 ms                                                | 3.68 ms: 1.02x slower                                                            |
| regex_dna      | 212 ms                                                 | 227 ms: 1.07x slower                                                             |
| regex_v8       | 23.1 ms                                                | 26.0 ms: 1.12x slower                                                            |
| regex_compile  | 148 ms                                                 | 191 ms: 1.29x slower                                                             |
| Geometric mean | (ref)                                                  | 1.12x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle             | 15.9 us                                                | 15.1 us: 1.05x faster                                                            |
| xml_etree_parse      | 159 ms                                                 | 152 ms: 1.05x faster                                                             |
| pickle_pure_python   | 324 us                                                 | 310 us: 1.05x faster                                                             |
| json_loads           | 28.5 us                                                | 27.7 us: 1.03x faster                                                            |
| pickle_dict          | 35.5 us                                                | 35.2 us: 1.01x faster                                                            |
| pickle_list          | 5.08 us                                                | 5.11 us: 1.00x slower                                                            |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                            |
| unpickle_list        | 5.29 us                                                | 5.46 us: 1.03x slower                                                            |
| xml_etree_iterparse  | 107 ms                                                 | 110 ms: 1.03x slower                                                             |
| xml_etree_process    | 61.7 ms                                                | 65.0 ms: 1.05x slower                                                            |
| xml_etree_generate   | 89.2 ms                                                | 96.0 ms: 1.08x slower                                                            |
| tomli_loads          | 2.33 sec                                               | 2.69 sec: 1.15x slower                                                           |
| unpickle_pure_python | 230 us                                                 | 303 us: 1.32x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.03x slower                                                                     |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.10 ms: 1.02x slower                                                            |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 13.7 ms: 1.15x slower                                                            |
| django_template | 34.6 ms                                                | 42.8 ms: 1.24x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.19x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 472 ms                                                 | 383 ms: 1.23x faster                                                             |
| typing_runtime_protocols   | 158 us                                                 | 129 us: 1.23x faster                                                             |
| async_tree_none_tg         | 450 ms                                                 | 367 ms: 1.23x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 476 ms: 1.21x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 968 ms: 1.19x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 1000 ms: 1.18x faster                                                            |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 640 ms: 1.13x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 511 ms: 1.13x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 646 ms: 1.12x faster                                                             |
| unpickle                   | 15.9 us                                                | 15.1 us: 1.05x faster                                                            |
| xml_etree_parse            | 159 ms                                                 | 152 ms: 1.05x faster                                                             |
| pathlib                    | 19.3 ms                                                | 18.5 ms: 1.05x faster                                                            |
| pickle_pure_python         | 324 us                                                 | 310 us: 1.05x faster                                                             |
| generators                 | 31.2 ms                                                | 29.9 ms: 1.04x faster                                                            |
| json_loads                 | 28.5 us                                                | 27.7 us: 1.03x faster                                                            |
| json                       | 5.26 ms                                                | 5.13 ms: 1.03x faster                                                            |
| logging_format             | 7.23 us                                                | 7.16 us: 1.01x faster                                                            |
| pickle_dict                | 35.5 us                                                | 35.2 us: 1.01x faster                                                            |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.00x faster                                                            |
| gc_traversal               | 3.79 ms                                                | 3.78 ms: 1.00x faster                                                            |
| pickle_list                | 5.08 us                                                | 5.11 us: 1.00x slower                                                            |
| deepcopy_reduce            | 3.35 us                                                | 3.38 us: 1.01x slower                                                            |
| regex_effbot               | 3.61 ms                                                | 3.68 ms: 1.02x slower                                                            |
| logging_silent             | 104 ns                                                 | 107 ns: 1.02x slower                                                             |
| python_startup_no_site     | 6.94 ms                                                | 7.10 ms: 1.02x slower                                                            |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                            |
| coroutines                 | 23.2 ms                                                | 23.8 ms: 1.03x slower                                                            |
| asyncio_websockets         | 551 ms                                                 | 567 ms: 1.03x slower                                                             |
| dask                       | 372 ms                                                 | 383 ms: 1.03x slower                                                             |
| unpickle_list              | 5.29 us                                                | 5.46 us: 1.03x slower                                                            |
| xml_etree_iterparse        | 107 ms                                                 | 110 ms: 1.03x slower                                                             |
| async_generators           | 463 ms                                                 | 479 ms: 1.03x slower                                                             |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                                           |
| asyncio_tcp                | 491 ms                                                 | 514 ms: 1.05x slower                                                             |
| deepcopy                   | 371 us                                                 | 390 us: 1.05x slower                                                             |
| xml_etree_process          | 61.7 ms                                                | 65.0 ms: 1.05x slower                                                            |
| bench_thread_pool          | 842 us                                                 | 889 us: 1.06x slower                                                             |
| sympy_sum                  | 169 ms                                                 | 180 ms: 1.07x slower                                                             |
| pidigits                   | 187 ms                                                 | 200 ms: 1.07x slower                                                             |
| gunicorn                   | 1.24 ms                                                | 1.33 ms: 1.07x slower                                                            |
| regex_dna                  | 212 ms                                                 | 227 ms: 1.07x slower                                                             |
| xml_etree_generate         | 89.2 ms                                                | 96.0 ms: 1.08x slower                                                            |
| aiohttp                    | 1.15 ms                                                | 1.24 ms: 1.08x slower                                                            |
| dulwich_log                | 68.5 ms                                                | 74.3 ms: 1.08x slower                                                            |
| chameleon                  | 7.41 ms                                                | 8.08 ms: 1.09x slower                                                            |
| sympy_str                  | 300 ms                                                 | 328 ms: 1.10x slower                                                             |
| raytrace                   | 312 ms                                                 | 343 ms: 1.10x slower                                                             |
| sympy_integrate            | 21.4 ms                                                | 23.5 ms: 1.10x slower                                                            |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| float                      | 84.7 ms                                                | 93.3 ms: 1.10x slower                                                            |
| mdp                        | 2.63 sec                                               | 2.90 sec: 1.10x slower                                                           |
| sqlite_synth               | 2.83 us                                                | 3.14 us: 1.11x slower                                                            |
| comprehensions             | 21.8 us                                                | 24.3 us: 1.11x slower                                                            |
| sqlglot_transpile          | 1.68 ms                                                | 1.88 ms: 1.12x slower                                                            |
| regex_v8                   | 23.1 ms                                                | 26.0 ms: 1.12x slower                                                            |
| pycparser                  | 1.18 sec                                               | 1.32 sec: 1.12x slower                                                           |
| 2to3                       | 274 ms                                                 | 311 ms: 1.13x slower                                                             |
| docutils                   | 2.77 sec                                               | 3.15 sec: 1.14x slower                                                           |
| deepcopy_memo              | 40.7 us                                                | 46.3 us: 1.14x slower                                                            |
| deltablue                  | 3.72 ms                                                | 4.23 ms: 1.14x slower                                                            |
| sqlglot_parse              | 1.36 ms                                                | 1.55 ms: 1.14x slower                                                            |
| sympy_expand               | 478 ms                                                 | 546 ms: 1.14x slower                                                             |
| mako                       | 11.9 ms                                                | 13.7 ms: 1.15x slower                                                            |
| tomli_loads                | 2.33 sec                                               | 2.69 sec: 1.15x slower                                                           |
| sqlglot_normalize          | 110 ms                                                 | 128 ms: 1.16x slower                                                             |
| meteor_contest             | 112 ms                                                 | 131 ms: 1.17x slower                                                             |
| scimark_fft                | 382 ms                                                 | 448 ms: 1.17x slower                                                             |
| scimark_sor                | 129 ms                                                 | 151 ms: 1.17x slower                                                             |
| create_gc_cycles           | 1.48 ms                                                | 1.77 ms: 1.20x slower                                                            |
| sqlglot_optimize           | 54.8 ms                                                | 65.9 ms: 1.20x slower                                                            |
| crypto_pyaes               | 81.9 ms                                                | 100 ms: 1.23x slower                                                             |
| spectral_norm              | 115 ms                                                 | 141 ms: 1.23x slower                                                             |
| fannkuch                   | 417 ms                                                 | 515 ms: 1.23x slower                                                             |
| django_template            | 34.6 ms                                                | 42.8 ms: 1.24x slower                                                            |
| chaos                      | 67.0 ms                                                | 83.3 ms: 1.24x slower                                                            |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 6.30 ms: 1.25x slower                                                            |
| richards                   | 45.8 ms                                                | 57.3 ms: 1.25x slower                                                            |
| richards_super             | 51.5 ms                                                | 65.0 ms: 1.26x slower                                                            |
| regex_compile              | 148 ms                                                 | 191 ms: 1.29x slower                                                             |
| nbody                      | 97.0 ms                                                | 127 ms: 1.31x slower                                                             |
| unpickle_pure_python       | 230 us                                                 | 303 us: 1.32x slower                                                             |
| telco                      | 7.10 ms                                                | 9.60 ms: 1.35x slower                                                            |
| coverage                   | 72.7 ms                                                | 98.8 ms: 1.36x slower                                                            |
| go                         | 139 ms                                                 | 191 ms: 1.37x slower                                                             |
| pprint_safe_repr           | 776 ms                                                 | 1.07 sec: 1.38x slower                                                           |
| pyflate                    | 482 ms                                                 | 672 ms: 1.39x slower                                                             |
| nqueens                    | 83.3 ms                                                | 117 ms: 1.40x slower                                                             |
| scimark_monte_carlo        | 75.1 ms                                                | 106 ms: 1.40x slower                                                             |
| pprint_pformat             | 1.57 sec                                               | 2.26 sec: 1.44x slower                                                           |
| scimark_lu                 | 118 ms                                                 | 172 ms: 1.46x slower                                                             |
| hexiom                     | 6.41 ms                                                | 10.2 ms: 1.59x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                                     |

Benchmark hidden because not significant (4): mypy2, logging_simple, pickle, tornado_http
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240419-3.13.0a6+-ed60e2e-PYTHON_UOPS/bm-20240419-linux-x86_64-faster%2dcpython-move_set_ip_to_exits-3.13.0a6+-ed60e2e.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 0.97x