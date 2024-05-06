# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_ghccc_cache_4
- machine: linux-x86_64
- commit hash: b309fd7
- commit date: 2024-04-24
- overall geometric mean: 1.00x faster
- HPT reliability: 88.11%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.08x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 290 ms: 1.06x slower                                                         |
| chameleon      | 7.41 ms                                                | 7.24 ms: 1.02x faster                                                        |
| docutils       | 2.77 sec                                               | 3.00 sec: 1.08x slower                                                       |
| tornado_http   | 103 ms                                                 | 98.0 ms: 1.05x faster                                                        |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 344 ms: 1.31x faster                                                         |
| async_tree_none            | 472 ms                                                 | 367 ms: 1.29x faster                                                         |
| async_tree_memoization_tg  | 575 ms                                                 | 450 ms: 1.28x faster                                                         |
| async_tree_io_tg           | 1.18 sec                                               | 950 ms: 1.24x faster                                                         |
| async_tree_io              | 1.16 sec                                               | 940 ms: 1.23x faster                                                         |
| async_tree_memoization     | 578 ms                                                 | 478 ms: 1.21x faster                                                         |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 612 ms: 1.19x faster                                                         |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 624 ms: 1.16x faster                                                         |
| Geometric mean             | (ref)                                                  | 1.24x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 83.1 ms: 1.17x faster                                                        |
| float          | 84.7 ms                                                | 75.3 ms: 1.12x faster                                                        |
| pidigits       | 187 ms                                                 | 210 ms: 1.12x slower                                                         |
| Geometric mean | (ref)                                                  | 1.05x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 23.1 ms                                                | 24.5 ms: 1.06x slower                                                        |
| regex_dna      | 212 ms                                                 | 225 ms: 1.06x slower                                                         |
| regex_compile  | 148 ms                                                 | 171 ms: 1.15x slower                                                         |
| regex_effbot   | 3.61 ms                                                | 4.23 ms: 1.17x slower                                                        |
| Geometric mean | (ref)                                                  | 1.11x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.15 sec: 1.08x faster                                                       |
| xml_etree_parse      | 159 ms                                                 | 148 ms: 1.08x faster                                                         |
| pickle_pure_python   | 324 us                                                 | 309 us: 1.05x faster                                                         |
| unpickle             | 15.9 us                                                | 15.2 us: 1.04x faster                                                        |
| json_loads           | 28.5 us                                                | 27.4 us: 1.04x faster                                                        |
| xml_etree_iterparse  | 107 ms                                                 | 104 ms: 1.03x faster                                                         |
| pickle_dict          | 35.5 us                                                | 34.9 us: 1.02x faster                                                        |
| xml_etree_process    | 61.7 ms                                                | 60.9 ms: 1.01x faster                                                        |
| xml_etree_generate   | 89.2 ms                                                | 88.1 ms: 1.01x faster                                                        |
| unpickle_list        | 5.29 us                                                | 5.34 us: 1.01x slower                                                        |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                        |
| pickle               | 11.6 us                                                | 12.0 us: 1.04x slower                                                        |
| unpickle_pure_python | 230 us                                                 | 240 us: 1.05x slower                                                         |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                 |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.71 ms: 1.11x slower                                                        |
| python_startup         | 9.55 ms                                                | 11.1 ms: 1.16x slower                                                        |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.7 ms: 1.11x faster                                                        |
| django_template | 34.6 ms                                                | 37.5 ms: 1.08x slower                                                        |
| Geometric mean  | (ref)                                                  | 1.01x faster                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 116 us: 1.36x faster                                                         |
| async_tree_none_tg         | 450 ms                                                 | 344 ms: 1.31x faster                                                         |
| async_tree_none            | 472 ms                                                 | 367 ms: 1.29x faster                                                         |
| async_tree_memoization_tg  | 575 ms                                                 | 450 ms: 1.28x faster                                                         |
| async_tree_io_tg           | 1.18 sec                                               | 950 ms: 1.24x faster                                                         |
| async_tree_io              | 1.16 sec                                               | 940 ms: 1.23x faster                                                         |
| async_tree_memoization     | 578 ms                                                 | 478 ms: 1.21x faster                                                         |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 612 ms: 1.19x faster                                                         |
| nbody                      | 97.0 ms                                                | 83.1 ms: 1.17x faster                                                        |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 624 ms: 1.16x faster                                                         |
| comprehensions             | 21.8 us                                                | 19.0 us: 1.15x faster                                                        |
| scimark_fft                | 382 ms                                                 | 333 ms: 1.15x faster                                                         |
| float                      | 84.7 ms                                                | 75.3 ms: 1.12x faster                                                        |
| mako                       | 11.9 ms                                                | 10.7 ms: 1.11x faster                                                        |
| crypto_pyaes               | 81.9 ms                                                | 73.7 ms: 1.11x faster                                                        |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.55 ms: 1.11x faster                                                        |
| tomli_loads                | 2.33 sec                                               | 2.15 sec: 1.08x faster                                                       |
| raytrace                   | 312 ms                                                 | 288 ms: 1.08x faster                                                         |
| logging_format             | 7.23 us                                                | 6.70 us: 1.08x faster                                                        |
| xml_etree_parse            | 159 ms                                                 | 148 ms: 1.08x faster                                                         |
| pathlib                    | 19.3 ms                                                | 18.0 ms: 1.07x faster                                                        |
| fannkuch                   | 417 ms                                                 | 391 ms: 1.07x faster                                                         |
| spectral_norm              | 115 ms                                                 | 108 ms: 1.06x faster                                                         |
| logging_simple             | 6.46 us                                                | 6.11 us: 1.06x faster                                                        |
| pickle_pure_python         | 324 us                                                 | 309 us: 1.05x faster                                                         |
| tornado_http               | 103 ms                                                 | 98.0 ms: 1.05x faster                                                        |
| unpickle                   | 15.9 us                                                | 15.2 us: 1.04x faster                                                        |
| json_loads                 | 28.5 us                                                | 27.4 us: 1.04x faster                                                        |
| generators                 | 31.2 ms                                                | 30.0 ms: 1.04x faster                                                        |
| deepcopy_reduce            | 3.35 us                                                | 3.23 us: 1.04x faster                                                        |
| xml_etree_iterparse        | 107 ms                                                 | 104 ms: 1.03x faster                                                         |
| logging_silent             | 104 ns                                                 | 102 ns: 1.03x faster                                                         |
| json                       | 5.26 ms                                                | 5.13 ms: 1.02x faster                                                        |
| chameleon                  | 7.41 ms                                                | 7.24 ms: 1.02x faster                                                        |
| pickle_dict                | 35.5 us                                                | 34.9 us: 1.02x faster                                                        |
| deepcopy_memo              | 40.7 us                                                | 40.1 us: 1.02x faster                                                        |
| xml_etree_process          | 61.7 ms                                                | 60.9 ms: 1.01x faster                                                        |
| coroutines                 | 23.2 ms                                                | 22.9 ms: 1.01x faster                                                        |
| xml_etree_generate         | 89.2 ms                                                | 88.1 ms: 1.01x faster                                                        |
| meteor_contest             | 112 ms                                                 | 112 ms: 1.01x faster                                                         |
| chaos                      | 67.0 ms                                                | 67.4 ms: 1.01x slower                                                        |
| sqlglot_transpile          | 1.68 ms                                                | 1.70 ms: 1.01x slower                                                        |
| unpickle_list              | 5.29 us                                                | 5.34 us: 1.01x slower                                                        |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                        |
| sqlglot_parse              | 1.36 ms                                                | 1.38 ms: 1.02x slower                                                        |
| mdp                        | 2.63 sec                                               | 2.68 sec: 1.02x slower                                                       |
| async_generators           | 463 ms                                                 | 471 ms: 1.02x slower                                                         |
| sqlite_synth               | 2.83 us                                                | 2.89 us: 1.02x slower                                                        |
| dask                       | 372 ms                                                 | 380 ms: 1.02x slower                                                         |
| asyncio_websockets         | 551 ms                                                 | 564 ms: 1.02x slower                                                         |
| sympy_sum                  | 169 ms                                                 | 174 ms: 1.03x slower                                                         |
| pycparser                  | 1.18 sec                                               | 1.21 sec: 1.03x slower                                                       |
| scimark_sor                | 129 ms                                                 | 133 ms: 1.03x slower                                                         |
| sympy_str                  | 300 ms                                                 | 310 ms: 1.04x slower                                                         |
| gc_traversal               | 3.79 ms                                                | 3.93 ms: 1.04x slower                                                        |
| bench_thread_pool          | 842 us                                                 | 874 us: 1.04x slower                                                         |
| pickle                     | 11.6 us                                                | 12.0 us: 1.04x slower                                                        |
| richards                   | 45.8 ms                                                | 47.7 ms: 1.04x slower                                                        |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.87 sec: 1.05x slower                                                       |
| unpickle_pure_python       | 230 us                                                 | 240 us: 1.05x slower                                                         |
| richards_super             | 51.5 ms                                                | 54.3 ms: 1.05x slower                                                        |
| asyncio_tcp                | 491 ms                                                 | 517 ms: 1.05x slower                                                         |
| dulwich_log                | 68.5 ms                                                | 72.2 ms: 1.05x slower                                                        |
| sqlglot_normalize          | 110 ms                                                 | 116 ms: 1.05x slower                                                         |
| 2to3                       | 274 ms                                                 | 290 ms: 1.06x slower                                                         |
| regex_v8                   | 23.1 ms                                                | 24.5 ms: 1.06x slower                                                        |
| regex_dna                  | 212 ms                                                 | 225 ms: 1.06x slower                                                         |
| gunicorn                   | 1.24 ms                                                | 1.32 ms: 1.06x slower                                                        |
| pyflate                    | 482 ms                                                 | 514 ms: 1.07x slower                                                         |
| sympy_integrate            | 21.4 ms                                                | 22.8 ms: 1.07x slower                                                        |
| aiohttp                    | 1.15 ms                                                | 1.23 ms: 1.07x slower                                                        |
| docutils                   | 2.77 sec                                               | 3.00 sec: 1.08x slower                                                       |
| django_template            | 34.6 ms                                                | 37.5 ms: 1.08x slower                                                        |
| sqlglot_optimize           | 54.8 ms                                                | 59.5 ms: 1.09x slower                                                        |
| sympy_expand               | 478 ms                                                 | 524 ms: 1.10x slower                                                         |
| scimark_lu                 | 118 ms                                                 | 130 ms: 1.10x slower                                                         |
| go                         | 139 ms                                                 | 155 ms: 1.11x slower                                                         |
| python_startup_no_site     | 6.94 ms                                                | 7.71 ms: 1.11x slower                                                        |
| pidigits                   | 187 ms                                                 | 210 ms: 1.12x slower                                                         |
| nqueens                    | 83.3 ms                                                | 95.5 ms: 1.15x slower                                                        |
| regex_compile              | 148 ms                                                 | 171 ms: 1.15x slower                                                         |
| pprint_safe_repr           | 776 ms                                                 | 897 ms: 1.16x slower                                                         |
| python_startup             | 9.55 ms                                                | 11.1 ms: 1.16x slower                                                        |
| regex_effbot               | 3.61 ms                                                | 4.23 ms: 1.17x slower                                                        |
| create_gc_cycles           | 1.48 ms                                                | 1.79 ms: 1.21x slower                                                        |
| pprint_pformat             | 1.57 sec                                               | 1.94 sec: 1.24x slower                                                       |
| telco                      | 7.10 ms                                                | 8.84 ms: 1.24x slower                                                        |
| hexiom                     | 6.41 ms                                                | 8.20 ms: 1.28x slower                                                        |
| coverage                   | 72.7 ms                                                | 98.3 ms: 1.35x slower                                                        |
| Geometric mean             | (ref)                                                  | 1.00x faster                                                                 |

Benchmark hidden because not significant (6): mypy2, scimark_monte_carlo, pickle_list, bench_mp_pool, deepcopy, deltablue
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240424-3.13.0a6+-b309fd7-JIT/bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 88.11% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.08x