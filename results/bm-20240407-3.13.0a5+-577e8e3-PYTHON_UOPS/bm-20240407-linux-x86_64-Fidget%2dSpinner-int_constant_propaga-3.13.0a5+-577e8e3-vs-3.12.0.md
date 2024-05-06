# Results vs. 3.12.0

- fork: Fidget-Spinner
- ref: int_constant_propaga
- machine: linux-x86_64
- commit hash: 577e8e3
- commit date: 2024-04-07
- overall geometric mean: 1.12x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 320 ms: 1.17x slower                                                             |
| chameleon      | 7.41 ms                                                | 7.95 ms: 1.07x slower                                                            |
| docutils       | 2.77 sec                                               | 3.18 sec: 1.15x slower                                                           |
| tornado_http   | 103 ms                                                 | 104 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                  | 1.10x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 363 ms: 1.24x faster                                                             |
| async_tree_none            | 472 ms                                                 | 385 ms: 1.23x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 471 ms: 1.22x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 976 ms: 1.18x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 1.00 sec: 1.18x faster                                                           |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 635 ms: 1.14x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 515 ms: 1.12x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 648 ms: 1.12x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.18x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                 | 202 ms: 1.08x slower                                                             |
| float          | 84.7 ms                                                | 96.6 ms: 1.14x slower                                                            |
| nbody          | 97.0 ms                                                | 134 ms: 1.38x slower                                                             |
| Geometric mean | (ref)                                                  | 1.19x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.61 ms                                                | 3.78 ms: 1.05x slower                                                            |
| regex_dna      | 212 ms                                                 | 227 ms: 1.07x slower                                                             |
| regex_v8       | 23.1 ms                                                | 26.9 ms: 1.16x slower                                                            |
| regex_compile  | 148 ms                                                 | 208 ms: 1.40x slower                                                             |
| Geometric mean | (ref)                                                  | 1.16x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_dict          | 35.5 us                                                | 34.8 us: 1.02x faster                                                            |
| pickle_pure_python   | 324 us                                                 | 318 us: 1.02x faster                                                             |
| pickle_list          | 5.08 us                                                | 5.02 us: 1.01x faster                                                            |
| unpickle_list        | 5.29 us                                                | 5.23 us: 1.01x faster                                                            |
| xml_etree_parse      | 159 ms                                                 | 163 ms: 1.02x slower                                                             |
| pickle               | 11.6 us                                                | 12.0 us: 1.03x slower                                                            |
| json_dumps           | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                            |
| unpickle             | 15.9 us                                                | 16.7 us: 1.06x slower                                                            |
| xml_etree_process    | 61.7 ms                                                | 66.2 ms: 1.07x slower                                                            |
| xml_etree_iterparse  | 107 ms                                                 | 115 ms: 1.08x slower                                                             |
| xml_etree_generate   | 89.2 ms                                                | 98.1 ms: 1.10x slower                                                            |
| tomli_loads          | 2.33 sec                                               | 2.72 sec: 1.17x slower                                                           |
| unpickle_pure_python | 230 us                                                 | 333 us: 1.45x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                                     |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 10.7 ms: 1.12x slower                                                            |
| python_startup_no_site | 6.94 ms                                                | 9.09 ms: 1.31x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|-----------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako      | 11.9 ms                                                | 14.3 ms: 1.20x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 127 us: 1.25x faster                                                             |
| async_tree_none_tg         | 450 ms                                                 | 363 ms: 1.24x faster                                                             |
| async_tree_none            | 472 ms                                                 | 385 ms: 1.23x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 471 ms: 1.22x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 976 ms: 1.18x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 1.00 sec: 1.18x faster                                                           |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 635 ms: 1.14x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 515 ms: 1.12x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 648 ms: 1.12x faster                                                             |
| generators                 | 31.2 ms                                                | 30.3 ms: 1.03x faster                                                            |
| pickle_dict                | 35.5 us                                                | 34.8 us: 1.02x faster                                                            |
| pickle_pure_python         | 324 us                                                 | 318 us: 1.02x faster                                                             |
| pickle_list                | 5.08 us                                                | 5.02 us: 1.01x faster                                                            |
| unpickle_list              | 5.29 us                                                | 5.23 us: 1.01x faster                                                            |
| logging_format             | 7.23 us                                                | 7.32 us: 1.01x slower                                                            |
| tornado_http               | 103 ms                                                 | 104 ms: 1.01x slower                                                             |
| xml_etree_parse            | 159 ms                                                 | 163 ms: 1.02x slower                                                             |
| asyncio_websockets         | 551 ms                                                 | 564 ms: 1.02x slower                                                             |
| logging_simple             | 6.46 us                                                | 6.61 us: 1.02x slower                                                            |
| json                       | 5.26 ms                                                | 5.41 ms: 1.03x slower                                                            |
| pickle                     | 11.6 us                                                | 12.0 us: 1.03x slower                                                            |
| json_dumps                 | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                            |
| dask                       | 372 ms                                                 | 388 ms: 1.04x slower                                                             |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                                           |
| regex_effbot               | 3.61 ms                                                | 3.78 ms: 1.05x slower                                                            |
| coroutines                 | 23.2 ms                                                | 24.3 ms: 1.05x slower                                                            |
| async_generators           | 463 ms                                                 | 486 ms: 1.05x slower                                                             |
| asyncio_tcp                | 491 ms                                                 | 518 ms: 1.05x slower                                                             |
| unpickle                   | 15.9 us                                                | 16.7 us: 1.06x slower                                                            |
| deepcopy                   | 371 us                                                 | 394 us: 1.06x slower                                                             |
| gc_traversal               | 3.79 ms                                                | 4.03 ms: 1.06x slower                                                            |
| pathlib                    | 19.3 ms                                                | 20.6 ms: 1.06x slower                                                            |
| regex_dna                  | 212 ms                                                 | 227 ms: 1.07x slower                                                             |
| xml_etree_process          | 61.7 ms                                                | 66.2 ms: 1.07x slower                                                            |
| logging_silent             | 104 ns                                                 | 112 ns: 1.07x slower                                                             |
| chameleon                  | 7.41 ms                                                | 7.95 ms: 1.07x slower                                                            |
| xml_etree_iterparse        | 107 ms                                                 | 115 ms: 1.08x slower                                                             |
| pidigits                   | 187 ms                                                 | 202 ms: 1.08x slower                                                             |
| sympy_sum                  | 169 ms                                                 | 183 ms: 1.08x slower                                                             |
| gunicorn                   | 1.24 ms                                                | 1.35 ms: 1.09x slower                                                            |
| bench_thread_pool          | 842 us                                                 | 917 us: 1.09x slower                                                             |
| aiohttp                    | 1.15 ms                                                | 1.26 ms: 1.10x slower                                                            |
| xml_etree_generate         | 89.2 ms                                                | 98.1 ms: 1.10x slower                                                            |
| sqlite_synth               | 2.83 us                                                | 3.15 us: 1.11x slower                                                            |
| python_startup             | 9.55 ms                                                | 10.7 ms: 1.12x slower                                                            |
| dulwich_log                | 68.5 ms                                                | 76.5 ms: 1.12x slower                                                            |
| mdp                        | 2.63 sec                                               | 2.94 sec: 1.12x slower                                                           |
| raytrace                   | 312 ms                                                 | 350 ms: 1.12x slower                                                             |
| sympy_str                  | 300 ms                                                 | 337 ms: 1.12x slower                                                             |
| sqlglot_transpile          | 1.68 ms                                                | 1.90 ms: 1.13x slower                                                            |
| float                      | 84.7 ms                                                | 96.6 ms: 1.14x slower                                                            |
| sqlglot_parse              | 1.36 ms                                                | 1.56 ms: 1.14x slower                                                            |
| sympy_integrate            | 21.4 ms                                                | 24.5 ms: 1.14x slower                                                            |
| docutils                   | 2.77 sec                                               | 3.18 sec: 1.15x slower                                                           |
| deltablue                  | 3.72 ms                                                | 4.28 ms: 1.15x slower                                                            |
| comprehensions             | 21.8 us                                                | 25.3 us: 1.16x slower                                                            |
| sympy_expand               | 478 ms                                                 | 556 ms: 1.16x slower                                                             |
| regex_v8                   | 23.1 ms                                                | 26.9 ms: 1.16x slower                                                            |
| 2to3                       | 274 ms                                                 | 320 ms: 1.17x slower                                                             |
| tomli_loads                | 2.33 sec                                               | 2.72 sec: 1.17x slower                                                           |
| deepcopy_memo              | 40.7 us                                                | 47.8 us: 1.17x slower                                                            |
| pycparser                  | 1.18 sec                                               | 1.39 sec: 1.18x slower                                                           |
| crypto_pyaes               | 81.9 ms                                                | 96.7 ms: 1.18x slower                                                            |
| create_gc_cycles           | 1.48 ms                                                | 1.76 ms: 1.19x slower                                                            |
| meteor_contest             | 112 ms                                                 | 134 ms: 1.19x slower                                                             |
| mako                       | 11.9 ms                                                | 14.3 ms: 1.20x slower                                                            |
| sqlglot_normalize          | 110 ms                                                 | 133 ms: 1.21x slower                                                             |
| chaos                      | 67.0 ms                                                | 82.2 ms: 1.23x slower                                                            |
| scimark_fft                | 382 ms                                                 | 470 ms: 1.23x slower                                                             |
| scimark_sor                | 129 ms                                                 | 160 ms: 1.24x slower                                                             |
| sqlglot_optimize           | 54.8 ms                                                | 68.8 ms: 1.26x slower                                                            |
| fannkuch                   | 417 ms                                                 | 524 ms: 1.26x slower                                                             |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 6.38 ms: 1.26x slower                                                            |
| scimark_monte_carlo        | 75.1 ms                                                | 97.3 ms: 1.29x slower                                                            |
| python_startup_no_site     | 6.94 ms                                                | 9.09 ms: 1.31x slower                                                            |
| pyflate                    | 482 ms                                                 | 641 ms: 1.33x slower                                                             |
| spectral_norm              | 115 ms                                                 | 153 ms: 1.34x slower                                                             |
| coverage                   | 72.7 ms                                                | 98.1 ms: 1.35x slower                                                            |
| nbody                      | 97.0 ms                                                | 134 ms: 1.38x slower                                                             |
| telco                      | 7.10 ms                                                | 9.89 ms: 1.39x slower                                                            |
| richards_super             | 51.5 ms                                                | 72.2 ms: 1.40x slower                                                            |
| regex_compile              | 148 ms                                                 | 208 ms: 1.40x slower                                                             |
| richards                   | 45.8 ms                                                | 64.8 ms: 1.41x slower                                                            |
| go                         | 139 ms                                                 | 198 ms: 1.42x slower                                                             |
| unpickle_pure_python       | 230 us                                                 | 333 us: 1.45x slower                                                             |
| scimark_lu                 | 118 ms                                                 | 178 ms: 1.51x slower                                                             |
| pprint_safe_repr           | 776 ms                                                 | 1.18 sec: 1.52x slower                                                           |
| pprint_pformat             | 1.57 sec                                               | 2.40 sec: 1.53x slower                                                           |
| hexiom                     | 6.41 ms                                                | 10.4 ms: 1.62x slower                                                            |
| nqueens                    | 83.3 ms                                                | 139 ms: 1.67x slower                                                             |
| Geometric mean             | (ref)                                                  | 1.12x slower                                                                     |

Benchmark hidden because not significant (4): mypy2, json_loads, deepcopy_reduce, bench_mp_pool
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240407-3.13.0a5+-577e8e3-PYTHON_UOPS/bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 0.97x