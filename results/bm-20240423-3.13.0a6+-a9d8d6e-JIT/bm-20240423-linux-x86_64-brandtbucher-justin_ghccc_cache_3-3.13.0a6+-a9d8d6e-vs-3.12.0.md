# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_ghccc_cache_3
- machine: linux-x86_64
- commit hash: a9d8d6e
- commit date: 2024-04-23
- overall geometric mean: 1.04x faster
- HPT reliability: 98.10%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 275 ms: 1.00x slower                                                         |
| chameleon      | 7.41 ms                                                | 6.97 ms: 1.06x faster                                                        |
| docutils       | 2.77 sec                                               | 2.90 sec: 1.05x slower                                                       |
| tornado_http   | 103 ms                                                 | 96.6 ms: 1.06x faster                                                        |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                                         |
| async_tree_none            | 472 ms                                                 | 353 ms: 1.34x faster                                                         |
| async_tree_memoization_tg  | 575 ms                                                 | 441 ms: 1.30x faster                                                         |
| async_tree_io_tg           | 1.18 sec                                               | 941 ms: 1.26x faster                                                         |
| async_tree_io              | 1.16 sec                                               | 921 ms: 1.26x faster                                                         |
| async_tree_memoization     | 578 ms                                                 | 471 ms: 1.23x faster                                                         |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 603 ms: 1.20x faster                                                         |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 612 ms: 1.18x faster                                                         |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 76.0 ms: 1.28x faster                                                        |
| float          | 84.7 ms                                                | 73.1 ms: 1.16x faster                                                        |
| pidigits       | 187 ms                                                 | 189 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                  | 1.14x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 141 ms: 1.05x faster                                                         |
| regex_dna      | 212 ms                                                 | 221 ms: 1.04x slower                                                         |
| regex_effbot   | 3.61 ms                                                | 3.76 ms: 1.04x slower                                                        |
| regex_v8       | 23.1 ms                                                | 24.5 ms: 1.06x slower                                                        |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 1.90 sec: 1.23x faster                                                       |
| xml_etree_parse      | 159 ms                                                 | 149 ms: 1.07x faster                                                         |
| pickle_pure_python   | 324 us                                                 | 306 us: 1.06x faster                                                         |
| unpickle             | 15.9 us                                                | 15.3 us: 1.04x faster                                                        |
| xml_etree_iterparse  | 107 ms                                                 | 103 ms: 1.04x faster                                                         |
| xml_etree_process    | 61.7 ms                                                | 59.9 ms: 1.03x faster                                                        |
| json_loads           | 28.5 us                                                | 27.7 us: 1.03x faster                                                        |
| unpickle_pure_python | 230 us                                                 | 224 us: 1.03x faster                                                         |
| xml_etree_generate   | 89.2 ms                                                | 87.1 ms: 1.02x faster                                                        |
| pickle_dict          | 35.5 us                                                | 34.8 us: 1.02x faster                                                        |
| pickle_list          | 5.08 us                                                | 5.18 us: 1.02x slower                                                        |
| pickle               | 11.6 us                                                | 11.8 us: 1.02x slower                                                        |
| json_dumps           | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                        |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                                 |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.65 ms: 1.10x slower                                                        |
| python_startup         | 9.55 ms                                                | 11.1 ms: 1.16x slower                                                        |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.0 ms: 1.19x faster                                                        |
| django_template | 34.6 ms                                                | 35.9 ms: 1.04x slower                                                        |
| Geometric mean  | (ref)                                                  | 1.07x faster                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 115 us: 1.37x faster                                                         |
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                                         |
| async_tree_none            | 472 ms                                                 | 353 ms: 1.34x faster                                                         |
| async_tree_memoization_tg  | 575 ms                                                 | 441 ms: 1.30x faster                                                         |
| nbody                      | 97.0 ms                                                | 76.0 ms: 1.28x faster                                                        |
| scimark_fft                | 382 ms                                                 | 302 ms: 1.26x faster                                                         |
| async_tree_io_tg           | 1.18 sec                                               | 941 ms: 1.26x faster                                                         |
| async_tree_io              | 1.16 sec                                               | 921 ms: 1.26x faster                                                         |
| comprehensions             | 21.8 us                                                | 17.4 us: 1.25x faster                                                        |
| async_tree_memoization     | 578 ms                                                 | 471 ms: 1.23x faster                                                         |
| tomli_loads                | 2.33 sec                                               | 1.90 sec: 1.23x faster                                                       |
| crypto_pyaes               | 81.9 ms                                                | 67.9 ms: 1.21x faster                                                        |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 603 ms: 1.20x faster                                                         |
| scimark_monte_carlo        | 75.1 ms                                                | 62.6 ms: 1.20x faster                                                        |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.22 ms: 1.20x faster                                                        |
| fannkuch                   | 417 ms                                                 | 349 ms: 1.20x faster                                                         |
| mako                       | 11.9 ms                                                | 10.0 ms: 1.19x faster                                                        |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 612 ms: 1.18x faster                                                         |
| float                      | 84.7 ms                                                | 73.1 ms: 1.16x faster                                                        |
| spectral_norm              | 115 ms                                                 | 99.2 ms: 1.16x faster                                                        |
| raytrace                   | 312 ms                                                 | 277 ms: 1.13x faster                                                         |
| chaos                      | 67.0 ms                                                | 60.6 ms: 1.10x faster                                                        |
| logging_format             | 7.23 us                                                | 6.57 us: 1.10x faster                                                        |
| logging_simple             | 6.46 us                                                | 5.93 us: 1.09x faster                                                        |
| pathlib                    | 19.3 ms                                                | 17.8 ms: 1.09x faster                                                        |
| pyflate                    | 482 ms                                                 | 447 ms: 1.08x faster                                                         |
| xml_etree_parse            | 159 ms                                                 | 149 ms: 1.07x faster                                                         |
| chameleon                  | 7.41 ms                                                | 6.97 ms: 1.06x faster                                                        |
| tornado_http               | 103 ms                                                 | 96.6 ms: 1.06x faster                                                        |
| richards                   | 45.8 ms                                                | 43.2 ms: 1.06x faster                                                        |
| pickle_pure_python         | 324 us                                                 | 306 us: 1.06x faster                                                         |
| regex_compile              | 148 ms                                                 | 141 ms: 1.05x faster                                                         |
| generators                 | 31.2 ms                                                | 29.7 ms: 1.05x faster                                                        |
| pprint_safe_repr           | 776 ms                                                 | 738 ms: 1.05x faster                                                         |
| pprint_pformat             | 1.57 sec                                               | 1.49 sec: 1.05x faster                                                       |
| richards_super             | 51.5 ms                                                | 49.5 ms: 1.04x faster                                                        |
| unpickle                   | 15.9 us                                                | 15.3 us: 1.04x faster                                                        |
| xml_etree_iterparse        | 107 ms                                                 | 103 ms: 1.04x faster                                                         |
| deepcopy_reduce            | 3.35 us                                                | 3.23 us: 1.04x faster                                                        |
| deepcopy_memo              | 40.7 us                                                | 39.5 us: 1.03x faster                                                        |
| logging_silent             | 104 ns                                                 | 101 ns: 1.03x faster                                                         |
| xml_etree_process          | 61.7 ms                                                | 59.9 ms: 1.03x faster                                                        |
| sqlglot_parse              | 1.36 ms                                                | 1.32 ms: 1.03x faster                                                        |
| deepcopy                   | 371 us                                                 | 361 us: 1.03x faster                                                         |
| json_loads                 | 28.5 us                                                | 27.7 us: 1.03x faster                                                        |
| meteor_contest             | 112 ms                                                 | 110 ms: 1.03x faster                                                         |
| coroutines                 | 23.2 ms                                                | 22.6 ms: 1.03x faster                                                        |
| unpickle_pure_python       | 230 us                                                 | 224 us: 1.03x faster                                                         |
| sqlglot_transpile          | 1.68 ms                                                | 1.64 ms: 1.02x faster                                                        |
| xml_etree_generate         | 89.2 ms                                                | 87.1 ms: 1.02x faster                                                        |
| pickle_dict                | 35.5 us                                                | 34.8 us: 1.02x faster                                                        |
| sympy_str                  | 300 ms                                                 | 294 ms: 1.02x faster                                                         |
| json                       | 5.26 ms                                                | 5.20 ms: 1.01x faster                                                        |
| pycparser                  | 1.18 sec                                               | 1.17 sec: 1.01x faster                                                       |
| scimark_sor                | 129 ms                                                 | 128 ms: 1.01x faster                                                         |
| sympy_sum                  | 169 ms                                                 | 167 ms: 1.01x faster                                                         |
| 2to3                       | 274 ms                                                 | 275 ms: 1.00x slower                                                         |
| pidigits                   | 187 ms                                                 | 189 ms: 1.01x slower                                                         |
| mdp                        | 2.63 sec                                               | 2.65 sec: 1.01x slower                                                       |
| async_generators           | 463 ms                                                 | 468 ms: 1.01x slower                                                         |
| pickle_list                | 5.08 us                                                | 5.18 us: 1.02x slower                                                        |
| pickle                     | 11.6 us                                                | 11.8 us: 1.02x slower                                                        |
| dulwich_log                | 68.5 ms                                                | 70.1 ms: 1.02x slower                                                        |
| asyncio_websockets         | 551 ms                                                 | 564 ms: 1.02x slower                                                         |
| sympy_integrate            | 21.4 ms                                                | 22.1 ms: 1.03x slower                                                        |
| hexiom                     | 6.41 ms                                                | 6.61 ms: 1.03x slower                                                        |
| bench_thread_pool          | 842 us                                                 | 872 us: 1.04x slower                                                         |
| django_template            | 34.6 ms                                                | 35.9 ms: 1.04x slower                                                        |
| sympy_expand               | 478 ms                                                 | 495 ms: 1.04x slower                                                         |
| json_dumps                 | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                        |
| sqlglot_normalize          | 110 ms                                                 | 114 ms: 1.04x slower                                                         |
| regex_dna                  | 212 ms                                                 | 221 ms: 1.04x slower                                                         |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                                       |
| regex_effbot               | 3.61 ms                                                | 3.76 ms: 1.04x slower                                                        |
| scimark_lu                 | 118 ms                                                 | 123 ms: 1.04x slower                                                         |
| sqlglot_optimize           | 54.8 ms                                                | 57.2 ms: 1.04x slower                                                        |
| nqueens                    | 83.3 ms                                                | 87.1 ms: 1.05x slower                                                        |
| docutils                   | 2.77 sec                                               | 2.90 sec: 1.05x slower                                                       |
| gunicorn                   | 1.24 ms                                                | 1.30 ms: 1.05x slower                                                        |
| asyncio_tcp                | 491 ms                                                 | 516 ms: 1.05x slower                                                         |
| aiohttp                    | 1.15 ms                                                | 1.22 ms: 1.06x slower                                                        |
| regex_v8                   | 23.1 ms                                                | 24.5 ms: 1.06x slower                                                        |
| go                         | 139 ms                                                 | 149 ms: 1.07x slower                                                         |
| gc_traversal               | 3.79 ms                                                | 4.06 ms: 1.07x slower                                                        |
| python_startup_no_site     | 6.94 ms                                                | 7.65 ms: 1.10x slower                                                        |
| python_startup             | 9.55 ms                                                | 11.1 ms: 1.16x slower                                                        |
| create_gc_cycles           | 1.48 ms                                                | 1.77 ms: 1.20x slower                                                        |
| telco                      | 7.10 ms                                                | 8.53 ms: 1.20x slower                                                        |
| coverage                   | 72.7 ms                                                | 98.4 ms: 1.35x slower                                                        |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                                 |

Benchmark hidden because not significant (6): mypy2, bench_mp_pool, sqlite_synth, deltablue, unpickle_list, dask
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240423-3.13.0a6+-a9d8d6e-JIT/bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 98.10% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.07x