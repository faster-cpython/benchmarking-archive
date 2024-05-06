# Results vs. 3.12.0

- fork: mdboom
- ref: tier2_funcs
- machine: linux-x86_64
- commit hash: b917d1f
- commit date: 2024-04-03
- overall geometric mean: 1.02x faster
- HPT reliability: 73.11%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 278 ms: 1.01x slower                                          |
| chameleon      | 7.41 ms                                                | 6.92 ms: 1.07x faster                                         |
| docutils       | 2.77 sec                                               | 2.89 sec: 1.04x slower                                        |
| tornado_http   | 103 ms                                                 | 97.0 ms: 1.06x faster                                         |
| Geometric mean | (ref)                                                  | 1.02x faster                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 342 ms: 1.31x faster                                          |
| async_tree_memoization_tg  | 575 ms                                                 | 451 ms: 1.27x faster                                          |
| async_tree_io_tg           | 1.18 sec                                               | 930 ms: 1.27x faster                                          |
| async_tree_memoization     | 578 ms                                                 | 457 ms: 1.26x faster                                          |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 584 ms: 1.24x faster                                          |
| async_tree_io              | 1.16 sec                                               | 951 ms: 1.22x faster                                          |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 600 ms: 1.21x faster                                          |
| async_tree_none            | 472 ms                                                 | 390 ms: 1.21x faster                                          |
| Geometric mean             | (ref)                                                  | 1.25x faster                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| float          | 84.7 ms                                                | 77.6 ms: 1.09x faster                                         |
| nbody          | 97.0 ms                                                | 92.8 ms: 1.05x faster                                         |
| pidigits       | 187 ms                                                 | 190 ms: 1.02x slower                                          |
| Geometric mean | (ref)                                                  | 1.04x faster                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 147 ms: 1.01x faster                                          |
| regex_effbot   | 3.61 ms                                                | 3.75 ms: 1.04x slower                                         |
| regex_dna      | 212 ms                                                 | 229 ms: 1.08x slower                                          |
| regex_v8       | 23.1 ms                                                | 25.9 ms: 1.12x slower                                         |
| Geometric mean | (ref)                                                  | 1.06x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.08 sec: 1.12x faster                                        |
| pickle_pure_python   | 324 us                                                 | 307 us: 1.05x faster                                          |
| pickle_dict          | 35.5 us                                                | 34.5 us: 1.03x faster                                         |
| xml_etree_process    | 61.7 ms                                                | 59.9 ms: 1.03x faster                                         |
| unpickle_list        | 5.29 us                                                | 5.14 us: 1.03x faster                                         |
| xml_etree_generate   | 89.2 ms                                                | 87.2 ms: 1.02x faster                                         |
| pickle_list          | 5.08 us                                                | 5.00 us: 1.02x faster                                         |
| json_loads           | 28.5 us                                                | 28.4 us: 1.00x faster                                         |
| xml_etree_iterparse  | 107 ms                                                 | 108 ms: 1.01x slower                                          |
| pickle               | 11.6 us                                                | 11.8 us: 1.01x slower                                         |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.01x slower                                         |
| unpickle_pure_python | 230 us                                                 | 239 us: 1.04x slower                                          |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                  |

Benchmark hidden because not significant (2): xml_etree_parse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 11.1 ms: 1.17x slower                                         |
| python_startup_no_site | 6.94 ms                                                | 9.57 ms: 1.38x slower                                         |
| Geometric mean         | (ref)                                                  | 1.27x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.7 ms: 1.11x faster                                         |
| django_template | 34.6 ms                                                | 36.3 ms: 1.05x slower                                         |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 110 us: 1.43x faster                                          |
| async_tree_none_tg         | 450 ms                                                 | 342 ms: 1.31x faster                                          |
| async_tree_memoization_tg  | 575 ms                                                 | 451 ms: 1.27x faster                                          |
| async_tree_io_tg           | 1.18 sec                                               | 930 ms: 1.27x faster                                          |
| async_tree_memoization     | 578 ms                                                 | 457 ms: 1.26x faster                                          |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 584 ms: 1.24x faster                                          |
| async_tree_io              | 1.16 sec                                               | 951 ms: 1.22x faster                                          |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 600 ms: 1.21x faster                                          |
| async_tree_none            | 472 ms                                                 | 390 ms: 1.21x faster                                          |
| comprehensions             | 21.8 us                                                | 18.5 us: 1.18x faster                                         |
| tomli_loads                | 2.33 sec                                               | 2.08 sec: 1.12x faster                                        |
| mako                       | 11.9 ms                                                | 10.7 ms: 1.11x faster                                         |
| scimark_fft                | 382 ms                                                 | 345 ms: 1.11x faster                                          |
| crypto_pyaes               | 81.9 ms                                                | 74.5 ms: 1.10x faster                                         |
| float                      | 84.7 ms                                                | 77.6 ms: 1.09x faster                                         |
| logging_format             | 7.23 us                                                | 6.67 us: 1.08x faster                                         |
| logging_simple             | 6.46 us                                                | 5.97 us: 1.08x faster                                         |
| scimark_monte_carlo        | 75.1 ms                                                | 69.8 ms: 1.08x faster                                         |
| deltablue                  | 3.72 ms                                                | 3.47 ms: 1.07x faster                                         |
| chameleon                  | 7.41 ms                                                | 6.92 ms: 1.07x faster                                         |
| chaos                      | 67.0 ms                                                | 63.0 ms: 1.06x faster                                         |
| raytrace                   | 312 ms                                                 | 294 ms: 1.06x faster                                          |
| deepcopy_reduce            | 3.35 us                                                | 3.16 us: 1.06x faster                                         |
| tornado_http               | 103 ms                                                 | 97.0 ms: 1.06x faster                                         |
| pickle_pure_python         | 324 us                                                 | 307 us: 1.05x faster                                          |
| fannkuch                   | 417 ms                                                 | 396 ms: 1.05x faster                                          |
| nbody                      | 97.0 ms                                                | 92.8 ms: 1.05x faster                                         |
| deepcopy_memo              | 40.7 us                                                | 39.1 us: 1.04x faster                                         |
| generators                 | 31.2 ms                                                | 30.1 ms: 1.04x faster                                         |
| coroutines                 | 23.2 ms                                                | 22.4 ms: 1.03x faster                                         |
| sympy_str                  | 300 ms                                                 | 290 ms: 1.03x faster                                          |
| pickle_dict                | 35.5 us                                                | 34.5 us: 1.03x faster                                         |
| xml_etree_process          | 61.7 ms                                                | 59.9 ms: 1.03x faster                                         |
| deepcopy                   | 371 us                                                 | 360 us: 1.03x faster                                          |
| unpickle_list              | 5.29 us                                                | 5.14 us: 1.03x faster                                         |
| pprint_safe_repr           | 776 ms                                                 | 755 ms: 1.03x faster                                          |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.93 ms: 1.03x faster                                         |
| pprint_pformat             | 1.57 sec                                               | 1.53 sec: 1.03x faster                                        |
| sympy_sum                  | 169 ms                                                 | 165 ms: 1.02x faster                                          |
| xml_etree_generate         | 89.2 ms                                                | 87.2 ms: 1.02x faster                                         |
| sqlglot_parse              | 1.36 ms                                                | 1.34 ms: 1.02x faster                                         |
| pickle_list                | 5.08 us                                                | 5.00 us: 1.02x faster                                         |
| sqlglot_transpile          | 1.68 ms                                                | 1.66 ms: 1.02x faster                                         |
| meteor_contest             | 112 ms                                                 | 111 ms: 1.01x faster                                          |
| pathlib                    | 19.3 ms                                                | 19.2 ms: 1.01x faster                                         |
| regex_compile              | 148 ms                                                 | 147 ms: 1.01x faster                                          |
| async_generators           | 463 ms                                                 | 461 ms: 1.00x faster                                          |
| json_loads                 | 28.5 us                                                | 28.4 us: 1.00x faster                                         |
| mdp                        | 2.63 sec                                               | 2.66 sec: 1.01x slower                                        |
| xml_etree_iterparse        | 107 ms                                                 | 108 ms: 1.01x slower                                          |
| 2to3                       | 274 ms                                                 | 278 ms: 1.01x slower                                          |
| scimark_sor                | 129 ms                                                 | 131 ms: 1.01x slower                                          |
| pickle                     | 11.6 us                                                | 11.8 us: 1.01x slower                                         |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.01x slower                                         |
| bench_thread_pool          | 842 us                                                 | 855 us: 1.02x slower                                          |
| pidigits                   | 187 ms                                                 | 190 ms: 1.02x slower                                          |
| dask                       | 372 ms                                                 | 379 ms: 1.02x slower                                          |
| sqlite_synth               | 2.83 us                                                | 2.89 us: 1.02x slower                                         |
| sympy_integrate            | 21.4 ms                                                | 21.9 ms: 1.02x slower                                         |
| json                       | 5.26 ms                                                | 5.37 ms: 1.02x slower                                         |
| sympy_expand               | 478 ms                                                 | 489 ms: 1.02x slower                                          |
| richards                   | 45.8 ms                                                | 46.9 ms: 1.02x slower                                         |
| sqlglot_normalize          | 110 ms                                                 | 113 ms: 1.03x slower                                          |
| spectral_norm              | 115 ms                                                 | 118 ms: 1.03x slower                                          |
| dulwich_log                | 68.5 ms                                                | 70.6 ms: 1.03x slower                                         |
| asyncio_websockets         | 551 ms                                                 | 570 ms: 1.03x slower                                          |
| asyncio_tcp                | 491 ms                                                 | 508 ms: 1.03x slower                                          |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                        |
| gc_traversal               | 3.79 ms                                                | 3.94 ms: 1.04x slower                                         |
| unpickle_pure_python       | 230 us                                                 | 239 us: 1.04x slower                                          |
| regex_effbot               | 3.61 ms                                                | 3.75 ms: 1.04x slower                                         |
| richards_super             | 51.5 ms                                                | 53.6 ms: 1.04x slower                                         |
| pycparser                  | 1.18 sec                                               | 1.23 sec: 1.04x slower                                        |
| docutils                   | 2.77 sec                                               | 2.89 sec: 1.04x slower                                        |
| django_template            | 34.6 ms                                                | 36.3 ms: 1.05x slower                                         |
| gunicorn                   | 1.24 ms                                                | 1.31 ms: 1.05x slower                                         |
| aiohttp                    | 1.15 ms                                                | 1.21 ms: 1.05x slower                                         |
| sqlglot_optimize           | 54.8 ms                                                | 57.9 ms: 1.06x slower                                         |
| regex_dna                  | 212 ms                                                 | 229 ms: 1.08x slower                                          |
| nqueens                    | 83.3 ms                                                | 90.7 ms: 1.09x slower                                         |
| regex_v8                   | 23.1 ms                                                | 25.9 ms: 1.12x slower                                         |
| go                         | 139 ms                                                 | 157 ms: 1.12x slower                                          |
| scimark_lu                 | 118 ms                                                 | 133 ms: 1.13x slower                                          |
| hexiom                     | 6.41 ms                                                | 7.33 ms: 1.14x slower                                         |
| create_gc_cycles           | 1.48 ms                                                | 1.69 ms: 1.15x slower                                         |
| python_startup             | 9.55 ms                                                | 11.1 ms: 1.17x slower                                         |
| telco                      | 7.10 ms                                                | 8.73 ms: 1.23x slower                                         |
| coverage                   | 72.7 ms                                                | 97.0 ms: 1.33x slower                                         |
| python_startup_no_site     | 6.94 ms                                                | 9.57 ms: 1.38x slower                                         |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                  |

Benchmark hidden because not significant (6): mypy2, logging_silent, pyflate, xml_etree_parse, bench_mp_pool, unpickle
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240403-3.13.0a5+-b917d1f-JIT/bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 73.11% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x