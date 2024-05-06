# Results vs. 3.12.0

- fork: mdboom
- ref: tier2_func_simple
- machine: linux-x86_64
- commit hash: 81bda60
- commit date: 2024-04-05
- overall geometric mean: 1.02x faster
- HPT reliability: 87.84%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 279 ms: 1.02x slower                                                |
| chameleon      | 7.41 ms                                                | 7.07 ms: 1.05x faster                                               |
| docutils       | 2.77 sec                                               | 2.94 sec: 1.06x slower                                              |
| tornado_http   | 103 ms                                                 | 96.6 ms: 1.06x faster                                               |
| Geometric mean | (ref)                                                  | 1.01x faster                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 337 ms: 1.33x faster                                                |
| async_tree_none            | 472 ms                                                 | 354 ms: 1.33x faster                                                |
| async_tree_memoization_tg  | 575 ms                                                 | 443 ms: 1.30x faster                                                |
| async_tree_memoization     | 578 ms                                                 | 459 ms: 1.26x faster                                                |
| async_tree_io_tg           | 1.18 sec                                               | 940 ms: 1.26x faster                                                |
| async_tree_io              | 1.16 sec                                               | 937 ms: 1.23x faster                                                |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 600 ms: 1.21x faster                                                |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 610 ms: 1.19x faster                                                |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 77.0 ms: 1.10x faster                                               |
| nbody          | 97.0 ms                                                | 92.3 ms: 1.05x faster                                               |
| pidigits       | 187 ms                                                 | 193 ms: 1.03x slower                                                |
| Geometric mean | (ref)                                                  | 1.04x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 144 ms: 1.03x faster                                                |
| regex_effbot   | 3.61 ms                                                | 3.86 ms: 1.07x slower                                               |
| regex_dna      | 212 ms                                                 | 230 ms: 1.09x slower                                                |
| regex_v8       | 23.1 ms                                                | 25.5 ms: 1.10x slower                                               |
| Geometric mean | (ref)                                                  | 1.06x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.03 sec: 1.15x faster                                              |
| pickle_pure_python   | 324 us                                                 | 306 us: 1.06x faster                                                |
| pickle_dict          | 35.5 us                                                | 34.1 us: 1.04x faster                                               |
| unpickle_list        | 5.29 us                                                | 5.12 us: 1.03x faster                                               |
| xml_etree_process    | 61.7 ms                                                | 60.2 ms: 1.03x faster                                               |
| pickle_list          | 5.08 us                                                | 4.99 us: 1.02x faster                                               |
| xml_etree_generate   | 89.2 ms                                                | 87.8 ms: 1.02x faster                                               |
| json_loads           | 28.5 us                                                | 28.2 us: 1.01x faster                                               |
| pickle               | 11.6 us                                                | 11.6 us: 1.00x slower                                               |
| xml_etree_iterparse  | 107 ms                                                 | 107 ms: 1.01x slower                                                |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.01x slower                                               |
| xml_etree_parse      | 159 ms                                                 | 162 ms: 1.01x slower                                                |
| unpickle_pure_python | 230 us                                                 | 241 us: 1.05x slower                                                |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                        |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 11.0 ms: 1.15x slower                                               |
| python_startup_no_site | 6.94 ms                                                | 9.45 ms: 1.36x slower                                               |
| Geometric mean         | (ref)                                                  | 1.25x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|-----------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako      | 11.9 ms                                                | 10.7 ms: 1.11x faster                                               |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 114 us: 1.38x faster                                                |
| async_tree_none_tg         | 450 ms                                                 | 337 ms: 1.33x faster                                                |
| async_tree_none            | 472 ms                                                 | 354 ms: 1.33x faster                                                |
| async_tree_memoization_tg  | 575 ms                                                 | 443 ms: 1.30x faster                                                |
| async_tree_memoization     | 578 ms                                                 | 459 ms: 1.26x faster                                                |
| async_tree_io_tg           | 1.18 sec                                               | 940 ms: 1.26x faster                                                |
| async_tree_io              | 1.16 sec                                               | 937 ms: 1.23x faster                                                |
| comprehensions             | 21.8 us                                                | 17.9 us: 1.22x faster                                               |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 600 ms: 1.21x faster                                                |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 610 ms: 1.19x faster                                                |
| tomli_loads                | 2.33 sec                                               | 2.03 sec: 1.15x faster                                              |
| raytrace                   | 312 ms                                                 | 275 ms: 1.14x faster                                                |
| logging_format             | 7.23 us                                                | 6.42 us: 1.13x faster                                               |
| scimark_fft                | 382 ms                                                 | 341 ms: 1.12x faster                                                |
| mako                       | 11.9 ms                                                | 10.7 ms: 1.11x faster                                               |
| logging_simple             | 6.46 us                                                | 5.83 us: 1.11x faster                                               |
| float                      | 84.7 ms                                                | 77.0 ms: 1.10x faster                                               |
| crypto_pyaes               | 81.9 ms                                                | 75.6 ms: 1.08x faster                                               |
| chaos                      | 67.0 ms                                                | 62.6 ms: 1.07x faster                                               |
| tornado_http               | 103 ms                                                 | 96.6 ms: 1.06x faster                                               |
| scimark_monte_carlo        | 75.1 ms                                                | 70.7 ms: 1.06x faster                                               |
| fannkuch                   | 417 ms                                                 | 393 ms: 1.06x faster                                                |
| pickle_pure_python         | 324 us                                                 | 306 us: 1.06x faster                                                |
| nbody                      | 97.0 ms                                                | 92.3 ms: 1.05x faster                                               |
| chameleon                  | 7.41 ms                                                | 7.07 ms: 1.05x faster                                               |
| deepcopy_memo              | 40.7 us                                                | 39.0 us: 1.05x faster                                               |
| pickle_dict                | 35.5 us                                                | 34.1 us: 1.04x faster                                               |
| generators                 | 31.2 ms                                                | 30.0 ms: 1.04x faster                                               |
| richards                   | 45.8 ms                                                | 44.2 ms: 1.04x faster                                               |
| unpickle_list              | 5.29 us                                                | 5.12 us: 1.03x faster                                               |
| pyflate                    | 482 ms                                                 | 468 ms: 1.03x faster                                                |
| regex_compile              | 148 ms                                                 | 144 ms: 1.03x faster                                                |
| deepcopy_reduce            | 3.35 us                                                | 3.25 us: 1.03x faster                                               |
| xml_etree_process          | 61.7 ms                                                | 60.2 ms: 1.03x faster                                               |
| sqlglot_parse              | 1.36 ms                                                | 1.33 ms: 1.02x faster                                               |
| richards_super             | 51.5 ms                                                | 50.3 ms: 1.02x faster                                               |
| coroutines                 | 23.2 ms                                                | 22.6 ms: 1.02x faster                                               |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.94 ms: 1.02x faster                                               |
| deepcopy                   | 371 us                                                 | 363 us: 1.02x faster                                                |
| sqlglot_transpile          | 1.68 ms                                                | 1.65 ms: 1.02x faster                                               |
| pickle_list                | 5.08 us                                                | 4.99 us: 1.02x faster                                               |
| pprint_safe_repr           | 776 ms                                                 | 762 ms: 1.02x faster                                                |
| pathlib                    | 19.3 ms                                                | 19.0 ms: 1.02x faster                                               |
| xml_etree_generate         | 89.2 ms                                                | 87.8 ms: 1.02x faster                                               |
| meteor_contest             | 112 ms                                                 | 111 ms: 1.01x faster                                                |
| json_loads                 | 28.5 us                                                | 28.2 us: 1.01x faster                                               |
| sympy_sum                  | 169 ms                                                 | 168 ms: 1.01x faster                                                |
| sympy_str                  | 300 ms                                                 | 297 ms: 1.01x faster                                                |
| gc_traversal               | 3.79 ms                                                | 3.77 ms: 1.01x faster                                               |
| async_generators           | 463 ms                                                 | 461 ms: 1.01x faster                                                |
| pickle                     | 11.6 us                                                | 11.6 us: 1.00x slower                                               |
| xml_etree_iterparse        | 107 ms                                                 | 107 ms: 1.01x slower                                                |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.01x slower                                               |
| xml_etree_parse            | 159 ms                                                 | 162 ms: 1.01x slower                                                |
| sqlite_synth               | 2.83 us                                                | 2.88 us: 1.02x slower                                               |
| pprint_pformat             | 1.57 sec                                               | 1.59 sec: 1.02x slower                                              |
| 2to3                       | 274 ms                                                 | 279 ms: 1.02x slower                                                |
| bench_thread_pool          | 842 us                                                 | 857 us: 1.02x slower                                                |
| logging_silent             | 104 ns                                                 | 106 ns: 1.02x slower                                                |
| json                       | 5.26 ms                                                | 5.36 ms: 1.02x slower                                               |
| dulwich_log                | 68.5 ms                                                | 70.1 ms: 1.02x slower                                               |
| asyncio_websockets         | 551 ms                                                 | 566 ms: 1.03x slower                                                |
| pidigits                   | 187 ms                                                 | 193 ms: 1.03x slower                                                |
| sqlglot_normalize          | 110 ms                                                 | 114 ms: 1.03x slower                                                |
| sympy_integrate            | 21.4 ms                                                | 22.1 ms: 1.03x slower                                               |
| pycparser                  | 1.18 sec                                               | 1.22 sec: 1.03x slower                                              |
| sympy_expand               | 478 ms                                                 | 496 ms: 1.04x slower                                                |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                              |
| asyncio_tcp                | 491 ms                                                 | 513 ms: 1.05x slower                                                |
| gunicorn                   | 1.24 ms                                                | 1.30 ms: 1.05x slower                                               |
| unpickle_pure_python       | 230 us                                                 | 241 us: 1.05x slower                                                |
| aiohttp                    | 1.15 ms                                                | 1.21 ms: 1.05x slower                                               |
| sqlglot_optimize           | 54.8 ms                                                | 57.6 ms: 1.05x slower                                               |
| mdp                        | 2.63 sec                                               | 2.77 sec: 1.05x slower                                              |
| docutils                   | 2.77 sec                                               | 2.94 sec: 1.06x slower                                              |
| regex_effbot               | 3.61 ms                                                | 3.86 ms: 1.07x slower                                               |
| regex_dna                  | 212 ms                                                 | 230 ms: 1.09x slower                                                |
| nqueens                    | 83.3 ms                                                | 90.5 ms: 1.09x slower                                               |
| scimark_sor                | 129 ms                                                 | 140 ms: 1.09x slower                                                |
| hexiom                     | 6.41 ms                                                | 7.01 ms: 1.09x slower                                               |
| regex_v8                   | 23.1 ms                                                | 25.5 ms: 1.10x slower                                               |
| go                         | 139 ms                                                 | 155 ms: 1.11x slower                                                |
| scimark_lu                 | 118 ms                                                 | 132 ms: 1.12x slower                                                |
| python_startup             | 9.55 ms                                                | 11.0 ms: 1.15x slower                                               |
| create_gc_cycles           | 1.48 ms                                                | 1.73 ms: 1.17x slower                                               |
| telco                      | 7.10 ms                                                | 8.68 ms: 1.22x slower                                               |
| coverage                   | 72.7 ms                                                | 98.9 ms: 1.36x slower                                               |
| python_startup_no_site     | 6.94 ms                                                | 9.45 ms: 1.36x slower                                               |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                        |

Benchmark hidden because not significant (6): mypy2, deltablue, bench_mp_pool, spectral_norm, dask, unpickle
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240405-3.13.0a5+-81bda60-JIT/bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 87.84% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x