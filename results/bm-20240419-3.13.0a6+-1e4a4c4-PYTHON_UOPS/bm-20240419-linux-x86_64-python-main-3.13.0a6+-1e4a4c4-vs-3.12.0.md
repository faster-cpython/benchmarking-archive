# Results vs. 3.12.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 1e4a4c4
- commit date: 2024-04-19
- overall geometric mean: 1.07x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 301 ms: 1.10x slower                                   |
| chameleon      | 7.41 ms                                                | 7.65 ms: 1.03x slower                                  |
| docutils       | 2.77 sec                                               | 3.08 sec: 1.11x slower                                 |
| Geometric mean | (ref)                                                  | 1.06x slower                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_none            | 472 ms                                                 | 374 ms: 1.26x faster                                   |
| async_tree_none_tg         | 450 ms                                                 | 356 ms: 1.26x faster                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 466 ms: 1.23x faster                                   |
| async_tree_io_tg           | 1.18 sec                                               | 973 ms: 1.22x faster                                   |
| async_tree_io              | 1.16 sec                                               | 984 ms: 1.17x faster                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 627 ms: 1.16x faster                                   |
| async_tree_memoization     | 578 ms                                                 | 501 ms: 1.15x faster                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 636 ms: 1.14x faster                                   |
| Geometric mean             | (ref)                                                  | 1.20x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 84.7 ms                                                | 89.3 ms: 1.05x slower                                  |
| pidigits       | 187 ms                                                 | 208 ms: 1.11x slower                                   |
| nbody          | 97.0 ms                                                | 119 ms: 1.23x slower                                   |
| Geometric mean | (ref)                                                  | 1.13x slower                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_effbot   | 3.61 ms                                                | 3.88 ms: 1.07x slower                                  |
| regex_dna      | 212 ms                                                 | 234 ms: 1.10x slower                                   |
| regex_v8       | 23.1 ms                                                | 26.2 ms: 1.13x slower                                  |
| regex_compile  | 148 ms                                                 | 177 ms: 1.20x slower                                   |
| Geometric mean | (ref)                                                  | 1.13x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| xml_etree_parse      | 159 ms                                                 | 152 ms: 1.05x faster                                   |
| pickle_pure_python   | 324 us                                                 | 311 us: 1.04x faster                                   |
| unpickle             | 15.9 us                                                | 15.4 us: 1.03x faster                                  |
| pickle_dict          | 35.5 us                                                | 34.6 us: 1.03x faster                                  |
| json_loads           | 28.5 us                                                | 28.0 us: 1.02x faster                                  |
| pickle               | 11.6 us                                                | 11.8 us: 1.02x slower                                  |
| xml_etree_iterparse  | 107 ms                                                 | 110 ms: 1.03x slower                                   |
| xml_etree_process    | 61.7 ms                                                | 63.8 ms: 1.03x slower                                  |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                  |
| unpickle_list        | 5.29 us                                                | 5.49 us: 1.04x slower                                  |
| xml_etree_generate   | 89.2 ms                                                | 93.5 ms: 1.05x slower                                  |
| tomli_loads          | 2.33 sec                                               | 2.51 sec: 1.08x slower                                 |
| unpickle_pure_python | 230 us                                                 | 282 us: 1.23x slower                                   |
| Geometric mean       | (ref)                                                  | 1.02x slower                                           |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.13 ms: 1.03x slower                                  |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                  |
| Geometric mean         | (ref)                                                  | 1.07x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| django_template | 34.6 ms                                                | 39.5 ms: 1.14x slower                                  |
| mako            | 11.9 ms                                                | 13.6 ms: 1.15x slower                                  |
| Geometric mean  | (ref)                                                  | 1.14x slower                                           |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 119 us: 1.32x faster                                   |
| async_tree_none            | 472 ms                                                 | 374 ms: 1.26x faster                                   |
| async_tree_none_tg         | 450 ms                                                 | 356 ms: 1.26x faster                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 466 ms: 1.23x faster                                   |
| async_tree_io_tg           | 1.18 sec                                               | 973 ms: 1.22x faster                                   |
| async_tree_io              | 1.16 sec                                               | 984 ms: 1.17x faster                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 627 ms: 1.16x faster                                   |
| async_tree_memoization     | 578 ms                                                 | 501 ms: 1.15x faster                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 636 ms: 1.14x faster                                   |
| pathlib                    | 19.3 ms                                                | 18.2 ms: 1.06x faster                                  |
| xml_etree_parse            | 159 ms                                                 | 152 ms: 1.05x faster                                   |
| pickle_pure_python         | 324 us                                                 | 311 us: 1.04x faster                                   |
| generators                 | 31.2 ms                                                | 30.0 ms: 1.04x faster                                  |
| logging_format             | 7.23 us                                                | 7.01 us: 1.03x faster                                  |
| unpickle                   | 15.9 us                                                | 15.4 us: 1.03x faster                                  |
| pickle_dict                | 35.5 us                                                | 34.6 us: 1.03x faster                                  |
| logging_simple             | 6.46 us                                                | 6.32 us: 1.02x faster                                  |
| json_loads                 | 28.5 us                                                | 28.0 us: 1.02x faster                                  |
| deepcopy_reduce            | 3.35 us                                                | 3.30 us: 1.01x faster                                  |
| json                       | 5.26 ms                                                | 5.19 ms: 1.01x faster                                  |
| coroutines                 | 23.2 ms                                                | 23.3 ms: 1.01x slower                                  |
| pickle                     | 11.6 us                                                | 11.8 us: 1.02x slower                                  |
| logging_silent             | 104 ns                                                 | 106 ns: 1.02x slower                                   |
| dask                       | 372 ms                                                 | 379 ms: 1.02x slower                                   |
| deepcopy                   | 371 us                                                 | 378 us: 1.02x slower                                   |
| asyncio_websockets         | 551 ms                                                 | 564 ms: 1.02x slower                                   |
| async_generators           | 463 ms                                                 | 476 ms: 1.03x slower                                   |
| python_startup_no_site     | 6.94 ms                                                | 7.13 ms: 1.03x slower                                  |
| comprehensions             | 21.8 us                                                | 22.4 us: 1.03x slower                                  |
| xml_etree_iterparse        | 107 ms                                                 | 110 ms: 1.03x slower                                   |
| chameleon                  | 7.41 ms                                                | 7.65 ms: 1.03x slower                                  |
| raytrace                   | 312 ms                                                 | 323 ms: 1.03x slower                                   |
| xml_etree_process          | 61.7 ms                                                | 63.8 ms: 1.03x slower                                  |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                  |
| unpickle_list              | 5.29 us                                                | 5.49 us: 1.04x slower                                  |
| gc_traversal               | 3.79 ms                                                | 3.94 ms: 1.04x slower                                  |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                 |
| bench_thread_pool          | 842 us                                                 | 882 us: 1.05x slower                                   |
| xml_etree_generate         | 89.2 ms                                                | 93.5 ms: 1.05x slower                                  |
| sympy_sum                  | 169 ms                                                 | 178 ms: 1.05x slower                                   |
| float                      | 84.7 ms                                                | 89.3 ms: 1.05x slower                                  |
| meteor_contest             | 112 ms                                                 | 119 ms: 1.06x slower                                   |
| asyncio_tcp                | 491 ms                                                 | 522 ms: 1.06x slower                                   |
| gunicorn                   | 1.24 ms                                                | 1.32 ms: 1.07x slower                                  |
| sqlglot_transpile          | 1.68 ms                                                | 1.80 ms: 1.07x slower                                  |
| aiohttp                    | 1.15 ms                                                | 1.23 ms: 1.07x slower                                  |
| sqlite_synth               | 2.83 us                                                | 3.04 us: 1.07x slower                                  |
| sympy_str                  | 300 ms                                                 | 322 ms: 1.07x slower                                   |
| regex_effbot               | 3.61 ms                                                | 3.88 ms: 1.07x slower                                  |
| tomli_loads                | 2.33 sec                                               | 2.51 sec: 1.08x slower                                 |
| dulwich_log                | 68.5 ms                                                | 73.8 ms: 1.08x slower                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.48 ms: 1.09x slower                                  |
| sympy_integrate            | 21.4 ms                                                | 23.2 ms: 1.09x slower                                  |
| deltablue                  | 3.72 ms                                                | 4.06 ms: 1.09x slower                                  |
| 2to3                       | 274 ms                                                 | 301 ms: 1.10x slower                                   |
| deepcopy_memo              | 40.7 us                                                | 44.8 us: 1.10x slower                                  |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                  |
| regex_dna                  | 212 ms                                                 | 234 ms: 1.10x slower                                   |
| mdp                        | 2.63 sec                                               | 2.91 sec: 1.11x slower                                 |
| pidigits                   | 187 ms                                                 | 208 ms: 1.11x slower                                   |
| docutils                   | 2.77 sec                                               | 3.08 sec: 1.11x slower                                 |
| sqlglot_normalize          | 110 ms                                                 | 123 ms: 1.11x slower                                   |
| pycparser                  | 1.18 sec                                               | 1.31 sec: 1.11x slower                                 |
| sympy_expand               | 478 ms                                                 | 533 ms: 1.12x slower                                   |
| crypto_pyaes               | 81.9 ms                                                | 91.7 ms: 1.12x slower                                  |
| regex_v8                   | 23.1 ms                                                | 26.2 ms: 1.13x slower                                  |
| django_template            | 34.6 ms                                                | 39.5 ms: 1.14x slower                                  |
| mako                       | 11.9 ms                                                | 13.6 ms: 1.15x slower                                  |
| sqlglot_optimize           | 54.8 ms                                                | 63.1 ms: 1.15x slower                                  |
| scimark_sor                | 129 ms                                                 | 150 ms: 1.16x slower                                   |
| fannkuch                   | 417 ms                                                 | 489 ms: 1.17x slower                                   |
| chaos                      | 67.0 ms                                                | 78.7 ms: 1.18x slower                                  |
| regex_compile              | 148 ms                                                 | 177 ms: 1.20x slower                                   |
| richards                   | 45.8 ms                                                | 55.0 ms: 1.20x slower                                  |
| create_gc_cycles           | 1.48 ms                                                | 1.77 ms: 1.20x slower                                  |
| richards_super             | 51.5 ms                                                | 62.0 ms: 1.20x slower                                  |
| scimark_fft                | 382 ms                                                 | 461 ms: 1.21x slower                                   |
| scimark_monte_carlo        | 75.1 ms                                                | 91.3 ms: 1.22x slower                                  |
| pyflate                    | 482 ms                                                 | 589 ms: 1.22x slower                                   |
| pprint_safe_repr           | 776 ms                                                 | 947 ms: 1.22x slower                                   |
| unpickle_pure_python       | 230 us                                                 | 282 us: 1.23x slower                                   |
| nbody                      | 97.0 ms                                                | 119 ms: 1.23x slower                                   |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 6.28 ms: 1.24x slower                                  |
| pprint_pformat             | 1.57 sec                                               | 1.97 sec: 1.26x slower                                 |
| spectral_norm              | 115 ms                                                 | 147 ms: 1.28x slower                                   |
| telco                      | 7.10 ms                                                | 9.19 ms: 1.30x slower                                  |
| go                         | 139 ms                                                 | 182 ms: 1.31x slower                                   |
| nqueens                    | 83.3 ms                                                | 110 ms: 1.32x slower                                   |
| coverage                   | 72.7 ms                                                | 99.4 ms: 1.37x slower                                  |
| scimark_lu                 | 118 ms                                                 | 167 ms: 1.42x slower                                   |
| hexiom                     | 6.41 ms                                                | 9.41 ms: 1.47x slower                                  |
| Geometric mean             | (ref)                                                  | 1.07x slower                                           |

Benchmark hidden because not significant (4): mypy2, pickle_list, bench_mp_pool, tornado_http
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240419-3.13.0a6+-1e4a4c4-PYTHON_UOPS/bm-20240419-linux-x86_64-python-main-3.13.0a6+-1e4a4c4.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 0.97x