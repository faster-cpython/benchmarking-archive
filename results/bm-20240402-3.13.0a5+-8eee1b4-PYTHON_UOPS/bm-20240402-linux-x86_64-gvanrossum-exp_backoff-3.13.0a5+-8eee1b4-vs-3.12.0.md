# Results vs. 3.12.0

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: 8eee1b4
- commit date: 2024-04-02
- overall geometric mean: 1.11x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 313 ms: 1.14x slower                                              |
| chameleon      | 7.41 ms                                                | 7.85 ms: 1.06x slower                                             |
| docutils       | 2.77 sec                                               | 3.16 sec: 1.14x slower                                            |
| Geometric mean | (ref)                                                  | 1.09x slower                                                      |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 363 ms: 1.24x faster                                              |
| async_tree_none            | 472 ms                                                 | 382 ms: 1.24x faster                                              |
| async_tree_memoization_tg  | 575 ms                                                 | 473 ms: 1.22x faster                                              |
| async_tree_io              | 1.16 sec                                               | 982 ms: 1.18x faster                                              |
| async_tree_io_tg           | 1.18 sec                                               | 1.01 sec: 1.17x faster                                            |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 634 ms: 1.14x faster                                              |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 643 ms: 1.13x faster                                              |
| async_tree_memoization     | 578 ms                                                 | 515 ms: 1.12x faster                                              |
| Geometric mean             | (ref)                                                  | 1.18x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 187 ms                                                 | 197 ms: 1.05x slower                                              |
| float          | 84.7 ms                                                | 94.6 ms: 1.12x slower                                             |
| nbody          | 97.0 ms                                                | 132 ms: 1.36x slower                                              |
| Geometric mean | (ref)                                                  | 1.17x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.61 ms                                                | 3.79 ms: 1.05x slower                                             |
| regex_dna      | 212 ms                                                 | 227 ms: 1.07x slower                                              |
| regex_v8       | 23.1 ms                                                | 26.7 ms: 1.15x slower                                             |
| regex_compile  | 148 ms                                                 | 194 ms: 1.31x slower                                              |
| Geometric mean | (ref)                                                  | 1.14x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| pickle_dict          | 35.5 us                                                | 34.1 us: 1.04x faster                                             |
| unpickle             | 15.9 us                                                | 15.4 us: 1.03x faster                                             |
| pickle_pure_python   | 324 us                                                 | 316 us: 1.03x faster                                              |
| unpickle_list        | 5.29 us                                                | 5.16 us: 1.03x faster                                             |
| pickle_list          | 5.08 us                                                | 5.00 us: 1.02x faster                                             |
| xml_etree_parse      | 159 ms                                                 | 163 ms: 1.02x slower                                              |
| pickle               | 11.6 us                                                | 11.9 us: 1.03x slower                                             |
| json_dumps           | 10.4 ms                                                | 10.8 ms: 1.04x slower                                             |
| xml_etree_process    | 61.7 ms                                                | 65.8 ms: 1.07x slower                                             |
| xml_etree_iterparse  | 107 ms                                                 | 115 ms: 1.08x slower                                              |
| xml_etree_generate   | 89.2 ms                                                | 96.8 ms: 1.09x slower                                             |
| tomli_loads          | 2.33 sec                                               | 2.78 sec: 1.19x slower                                            |
| unpickle_pure_python | 230 us                                                 | 309 us: 1.34x slower                                              |
| Geometric mean       | (ref)                                                  | 1.05x slower                                                      |

Benchmark hidden because not significant (1): json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 10.7 ms: 1.12x slower                                             |
| python_startup_no_site | 6.94 ms                                                | 9.10 ms: 1.31x slower                                             |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|-----------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| mako      | 11.9 ms                                                | 13.9 ms: 1.17x slower                                             |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 363 ms: 1.24x faster                                              |
| async_tree_none            | 472 ms                                                 | 382 ms: 1.24x faster                                              |
| typing_runtime_protocols   | 158 us                                                 | 129 us: 1.22x faster                                              |
| async_tree_memoization_tg  | 575 ms                                                 | 473 ms: 1.22x faster                                              |
| async_tree_io              | 1.16 sec                                               | 982 ms: 1.18x faster                                              |
| async_tree_io_tg           | 1.18 sec                                               | 1.01 sec: 1.17x faster                                            |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 634 ms: 1.14x faster                                              |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 643 ms: 1.13x faster                                              |
| async_tree_memoization     | 578 ms                                                 | 515 ms: 1.12x faster                                              |
| pickle_dict                | 35.5 us                                                | 34.1 us: 1.04x faster                                             |
| generators                 | 31.2 ms                                                | 30.0 ms: 1.04x faster                                             |
| coroutines                 | 23.2 ms                                                | 22.3 ms: 1.04x faster                                             |
| unpickle                   | 15.9 us                                                | 15.4 us: 1.03x faster                                             |
| pickle_pure_python         | 324 us                                                 | 316 us: 1.03x faster                                              |
| unpickle_list              | 5.29 us                                                | 5.16 us: 1.03x faster                                             |
| pickle_list                | 5.08 us                                                | 5.00 us: 1.02x faster                                             |
| logging_format             | 7.23 us                                                | 7.37 us: 1.02x slower                                             |
| xml_etree_parse            | 159 ms                                                 | 163 ms: 1.02x slower                                              |
| asyncio_websockets         | 551 ms                                                 | 565 ms: 1.02x slower                                              |
| pickle                     | 11.6 us                                                | 11.9 us: 1.03x slower                                             |
| logging_silent             | 104 ns                                                 | 108 ns: 1.03x slower                                              |
| dask                       | 372 ms                                                 | 384 ms: 1.03x slower                                              |
| logging_simple             | 6.46 us                                                | 6.68 us: 1.03x slower                                             |
| json_dumps                 | 10.4 ms                                                | 10.8 ms: 1.04x slower                                             |
| json                       | 5.26 ms                                                | 5.47 ms: 1.04x slower                                             |
| async_generators           | 463 ms                                                 | 483 ms: 1.04x slower                                              |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.87 sec: 1.05x slower                                            |
| regex_effbot               | 3.61 ms                                                | 3.79 ms: 1.05x slower                                             |
| gc_traversal               | 3.79 ms                                                | 4.00 ms: 1.05x slower                                             |
| asyncio_tcp                | 491 ms                                                 | 517 ms: 1.05x slower                                              |
| pidigits                   | 187 ms                                                 | 197 ms: 1.05x slower                                              |
| deepcopy                   | 371 us                                                 | 391 us: 1.05x slower                                              |
| pathlib                    | 19.3 ms                                                | 20.4 ms: 1.06x slower                                             |
| chameleon                  | 7.41 ms                                                | 7.85 ms: 1.06x slower                                             |
| xml_etree_process          | 61.7 ms                                                | 65.8 ms: 1.07x slower                                             |
| bench_thread_pool          | 842 us                                                 | 897 us: 1.07x slower                                              |
| regex_dna                  | 212 ms                                                 | 227 ms: 1.07x slower                                              |
| mdp                        | 2.63 sec                                               | 2.84 sec: 1.08x slower                                            |
| xml_etree_iterparse        | 107 ms                                                 | 115 ms: 1.08x slower                                              |
| xml_etree_generate         | 89.2 ms                                                | 96.8 ms: 1.09x slower                                             |
| sympy_sum                  | 169 ms                                                 | 184 ms: 1.09x slower                                              |
| sqlite_synth               | 2.83 us                                                | 3.09 us: 1.09x slower                                             |
| aiohttp                    | 1.15 ms                                                | 1.25 ms: 1.09x slower                                             |
| gunicorn                   | 1.24 ms                                                | 1.36 ms: 1.09x slower                                             |
| dulwich_log                | 68.5 ms                                                | 76.3 ms: 1.11x slower                                             |
| sqlglot_transpile          | 1.68 ms                                                | 1.88 ms: 1.12x slower                                             |
| float                      | 84.7 ms                                                | 94.6 ms: 1.12x slower                                             |
| python_startup             | 9.55 ms                                                | 10.7 ms: 1.12x slower                                             |
| sympy_integrate            | 21.4 ms                                                | 24.1 ms: 1.12x slower                                             |
| sympy_str                  | 300 ms                                                 | 338 ms: 1.13x slower                                              |
| meteor_contest             | 112 ms                                                 | 127 ms: 1.13x slower                                              |
| crypto_pyaes               | 81.9 ms                                                | 93.4 ms: 1.14x slower                                             |
| 2to3                       | 274 ms                                                 | 313 ms: 1.14x slower                                              |
| sqlglot_parse              | 1.36 ms                                                | 1.55 ms: 1.14x slower                                             |
| docutils                   | 2.77 sec                                               | 3.16 sec: 1.14x slower                                            |
| regex_v8                   | 23.1 ms                                                | 26.7 ms: 1.15x slower                                             |
| sympy_expand               | 478 ms                                                 | 554 ms: 1.16x slower                                              |
| mako                       | 11.9 ms                                                | 13.9 ms: 1.17x slower                                             |
| scimark_sor                | 129 ms                                                 | 151 ms: 1.17x slower                                              |
| create_gc_cycles           | 1.48 ms                                                | 1.75 ms: 1.19x slower                                             |
| comprehensions             | 21.8 us                                                | 25.9 us: 1.19x slower                                             |
| fannkuch                   | 417 ms                                                 | 497 ms: 1.19x slower                                              |
| tomli_loads                | 2.33 sec                                               | 2.78 sec: 1.19x slower                                            |
| sqlglot_normalize          | 110 ms                                                 | 131 ms: 1.19x slower                                              |
| chaos                      | 67.0 ms                                                | 79.9 ms: 1.19x slower                                             |
| raytrace                   | 312 ms                                                 | 373 ms: 1.20x slower                                              |
| scimark_monte_carlo        | 75.1 ms                                                | 90.2 ms: 1.20x slower                                             |
| scimark_fft                | 382 ms                                                 | 463 ms: 1.21x slower                                              |
| deltablue                  | 3.72 ms                                                | 4.53 ms: 1.22x slower                                             |
| deepcopy_memo              | 40.7 us                                                | 49.9 us: 1.23x slower                                             |
| pycparser                  | 1.18 sec                                               | 1.45 sec: 1.23x slower                                            |
| sqlglot_optimize           | 54.8 ms                                                | 67.5 ms: 1.23x slower                                             |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 6.33 ms: 1.25x slower                                             |
| regex_compile              | 148 ms                                                 | 194 ms: 1.31x slower                                              |
| python_startup_no_site     | 6.94 ms                                                | 9.10 ms: 1.31x slower                                             |
| richards_super             | 51.5 ms                                                | 68.0 ms: 1.32x slower                                             |
| go                         | 139 ms                                                 | 185 ms: 1.32x slower                                              |
| richards                   | 45.8 ms                                                | 61.1 ms: 1.33x slower                                             |
| spectral_norm              | 115 ms                                                 | 153 ms: 1.33x slower                                              |
| unpickle_pure_python       | 230 us                                                 | 309 us: 1.34x slower                                              |
| pyflate                    | 482 ms                                                 | 651 ms: 1.35x slower                                              |
| coverage                   | 72.7 ms                                                | 98.2 ms: 1.35x slower                                             |
| nbody                      | 97.0 ms                                                | 132 ms: 1.36x slower                                              |
| telco                      | 7.10 ms                                                | 9.69 ms: 1.36x slower                                             |
| nqueens                    | 83.3 ms                                                | 121 ms: 1.45x slower                                              |
| pprint_safe_repr           | 776 ms                                                 | 1.13 sec: 1.45x slower                                            |
| unpack_sequence            | 54.0 ns                                                | 79.3 ns: 1.47x slower                                             |
| scimark_lu                 | 118 ms                                                 | 176 ms: 1.49x slower                                              |
| pprint_pformat             | 1.57 sec                                               | 2.35 sec: 1.50x slower                                            |
| hexiom                     | 6.41 ms                                                | 10.2 ms: 1.59x slower                                             |
| Geometric mean             | (ref)                                                  | 1.11x slower                                                      |

Benchmark hidden because not significant (5): bench_mp_pool, deepcopy_reduce, json_loads, tornado_http, mypy2
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240402-3.13.0a5+-8eee1b4-PYTHON_UOPS/bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 0.96x