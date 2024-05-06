# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_ghccc
- machine: linux-x86_64
- commit hash: 07e95c4
- commit date: 2024-04-23
- overall geometric mean: 1.04x faster
- HPT reliability: 97.50%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 275 ms: 1.00x slower                                                 |
| chameleon      | 7.41 ms                                                | 6.93 ms: 1.07x faster                                                |
| docutils       | 2.77 sec                                               | 2.90 sec: 1.05x slower                                               |
| tornado_http   | 103 ms                                                 | 96.3 ms: 1.07x faster                                                |
| Geometric mean | (ref)                                                  | 1.02x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 336 ms: 1.34x faster                                                 |
| async_tree_none            | 472 ms                                                 | 356 ms: 1.33x faster                                                 |
| async_tree_memoization_tg  | 575 ms                                                 | 440 ms: 1.30x faster                                                 |
| async_tree_io_tg           | 1.18 sec                                               | 942 ms: 1.25x faster                                                 |
| async_tree_memoization     | 578 ms                                                 | 461 ms: 1.25x faster                                                 |
| async_tree_io              | 1.16 sec                                               | 925 ms: 1.25x faster                                                 |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 608 ms: 1.19x faster                                                 |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 614 ms: 1.18x faster                                                 |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 82.2 ms: 1.18x faster                                                |
| float          | 84.7 ms                                                | 73.4 ms: 1.15x faster                                                |
| pidigits       | 187 ms                                                 | 197 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                  | 1.09x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 140 ms: 1.06x faster                                                 |
| regex_effbot   | 3.61 ms                                                | 3.57 ms: 1.01x faster                                                |
| regex_dna      | 212 ms                                                 | 218 ms: 1.03x slower                                                 |
| regex_v8       | 23.1 ms                                                | 24.4 ms: 1.05x slower                                                |
| Geometric mean | (ref)                                                  | 1.00x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 1.96 sec: 1.19x faster                                               |
| pickle_list          | 5.08 us                                                | 4.75 us: 1.07x faster                                                |
| pickle_pure_python   | 324 us                                                 | 305 us: 1.06x faster                                                 |
| xml_etree_parse      | 159 ms                                                 | 150 ms: 1.06x faster                                                 |
| pickle_dict          | 35.5 us                                                | 33.5 us: 1.06x faster                                                |
| xml_etree_iterparse  | 107 ms                                                 | 102 ms: 1.05x faster                                                 |
| unpickle_list        | 5.29 us                                                | 5.05 us: 1.05x faster                                                |
| json_loads           | 28.5 us                                                | 27.6 us: 1.03x faster                                                |
| xml_etree_process    | 61.7 ms                                                | 60.1 ms: 1.03x faster                                                |
| xml_etree_generate   | 89.2 ms                                                | 87.1 ms: 1.02x faster                                                |
| unpickle             | 15.9 us                                                | 15.5 us: 1.02x faster                                                |
| unpickle_pure_python | 230 us                                                 | 227 us: 1.01x faster                                                 |
| pickle               | 11.6 us                                                | 11.9 us: 1.02x slower                                                |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.57 ms: 1.09x slower                                                |
| python_startup         | 9.55 ms                                                | 11.0 ms: 1.15x slower                                                |
| Geometric mean         | (ref)                                                  | 1.12x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 9.96 ms: 1.19x faster                                                |
| django_template | 34.6 ms                                                | 36.2 ms: 1.05x slower                                                |
| Geometric mean  | (ref)                                                  | 1.07x faster                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 114 us: 1.39x faster                                                 |
| async_tree_none_tg         | 450 ms                                                 | 336 ms: 1.34x faster                                                 |
| async_tree_none            | 472 ms                                                 | 356 ms: 1.33x faster                                                 |
| async_tree_memoization_tg  | 575 ms                                                 | 440 ms: 1.30x faster                                                 |
| comprehensions             | 21.8 us                                                | 17.0 us: 1.28x faster                                                |
| async_tree_io_tg           | 1.18 sec                                               | 942 ms: 1.25x faster                                                 |
| async_tree_memoization     | 578 ms                                                 | 461 ms: 1.25x faster                                                 |
| async_tree_io              | 1.16 sec                                               | 925 ms: 1.25x faster                                                 |
| scimark_fft                | 382 ms                                                 | 316 ms: 1.21x faster                                                 |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 608 ms: 1.19x faster                                                 |
| mako                       | 11.9 ms                                                | 9.96 ms: 1.19x faster                                                |
| crypto_pyaes               | 81.9 ms                                                | 68.6 ms: 1.19x faster                                                |
| tomli_loads                | 2.33 sec                                               | 1.96 sec: 1.19x faster                                               |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 614 ms: 1.18x faster                                                 |
| fannkuch                   | 417 ms                                                 | 353 ms: 1.18x faster                                                 |
| nbody                      | 97.0 ms                                                | 82.2 ms: 1.18x faster                                                |
| scimark_monte_carlo        | 75.1 ms                                                | 63.9 ms: 1.18x faster                                                |
| spectral_norm              | 115 ms                                                 | 98.9 ms: 1.16x faster                                                |
| raytrace                   | 312 ms                                                 | 271 ms: 1.15x faster                                                 |
| float                      | 84.7 ms                                                | 73.4 ms: 1.15x faster                                                |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.52 ms: 1.12x faster                                                |
| logging_format             | 7.23 us                                                | 6.52 us: 1.11x faster                                                |
| logging_simple             | 6.46 us                                                | 5.86 us: 1.10x faster                                                |
| chaos                      | 67.0 ms                                                | 60.9 ms: 1.10x faster                                                |
| pyflate                    | 482 ms                                                 | 442 ms: 1.09x faster                                                 |
| pathlib                    | 19.3 ms                                                | 17.8 ms: 1.09x faster                                                |
| richards                   | 45.8 ms                                                | 42.5 ms: 1.08x faster                                                |
| pickle_list                | 5.08 us                                                | 4.75 us: 1.07x faster                                                |
| chameleon                  | 7.41 ms                                                | 6.93 ms: 1.07x faster                                                |
| tornado_http               | 103 ms                                                 | 96.3 ms: 1.07x faster                                                |
| pickle_pure_python         | 324 us                                                 | 305 us: 1.06x faster                                                 |
| xml_etree_parse            | 159 ms                                                 | 150 ms: 1.06x faster                                                 |
| regex_compile              | 148 ms                                                 | 140 ms: 1.06x faster                                                 |
| pickle_dict                | 35.5 us                                                | 33.5 us: 1.06x faster                                                |
| deepcopy_memo              | 40.7 us                                                | 38.5 us: 1.06x faster                                                |
| richards_super             | 51.5 ms                                                | 48.8 ms: 1.06x faster                                                |
| deepcopy_reduce            | 3.35 us                                                | 3.18 us: 1.05x faster                                                |
| xml_etree_iterparse        | 107 ms                                                 | 102 ms: 1.05x faster                                                 |
| unpickle_list              | 5.29 us                                                | 5.05 us: 1.05x faster                                                |
| pprint_safe_repr           | 776 ms                                                 | 745 ms: 1.04x faster                                                 |
| deepcopy                   | 371 us                                                 | 358 us: 1.04x faster                                                 |
| json_loads                 | 28.5 us                                                | 27.6 us: 1.03x faster                                                |
| sqlglot_parse              | 1.36 ms                                                | 1.32 ms: 1.03x faster                                                |
| meteor_contest             | 112 ms                                                 | 109 ms: 1.03x faster                                                 |
| sqlglot_transpile          | 1.68 ms                                                | 1.64 ms: 1.03x faster                                                |
| xml_etree_process          | 61.7 ms                                                | 60.1 ms: 1.03x faster                                                |
| json                       | 5.26 ms                                                | 5.13 ms: 1.03x faster                                                |
| generators                 | 31.2 ms                                                | 30.4 ms: 1.03x faster                                                |
| xml_etree_generate         | 89.2 ms                                                | 87.1 ms: 1.02x faster                                                |
| unpickle                   | 15.9 us                                                | 15.5 us: 1.02x faster                                                |
| sympy_str                  | 300 ms                                                 | 294 ms: 1.02x faster                                                 |
| pprint_pformat             | 1.57 sec                                               | 1.54 sec: 1.02x faster                                               |
| unpickle_pure_python       | 230 us                                                 | 227 us: 1.01x faster                                                 |
| regex_effbot               | 3.61 ms                                                | 3.57 ms: 1.01x faster                                                |
| sympy_sum                  | 169 ms                                                 | 167 ms: 1.01x faster                                                 |
| coroutines                 | 23.2 ms                                                | 22.9 ms: 1.01x faster                                                |
| logging_silent             | 104 ns                                                 | 104 ns: 1.01x faster                                                 |
| gc_traversal               | 3.79 ms                                                | 3.79 ms: 1.00x faster                                                |
| 2to3                       | 274 ms                                                 | 275 ms: 1.00x slower                                                 |
| scimark_sor                | 129 ms                                                 | 130 ms: 1.01x slower                                                 |
| dulwich_log                | 68.5 ms                                                | 69.1 ms: 1.01x slower                                                |
| async_generators           | 463 ms                                                 | 469 ms: 1.01x slower                                                 |
| hexiom                     | 6.41 ms                                                | 6.50 ms: 1.01x slower                                                |
| dask                       | 372 ms                                                 | 378 ms: 1.02x slower                                                 |
| bench_thread_pool          | 842 us                                                 | 861 us: 1.02x slower                                                 |
| pickle                     | 11.6 us                                                | 11.9 us: 1.02x slower                                                |
| sympy_integrate            | 21.4 ms                                                | 22.0 ms: 1.03x slower                                                |
| regex_dna                  | 212 ms                                                 | 218 ms: 1.03x slower                                                 |
| asyncio_websockets         | 551 ms                                                 | 567 ms: 1.03x slower                                                 |
| sqlglot_normalize          | 110 ms                                                 | 114 ms: 1.03x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                |
| sympy_expand               | 478 ms                                                 | 495 ms: 1.03x slower                                                 |
| nqueens                    | 83.3 ms                                                | 86.4 ms: 1.04x slower                                                |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                               |
| asyncio_tcp                | 491 ms                                                 | 513 ms: 1.05x slower                                                 |
| django_template            | 34.6 ms                                                | 36.2 ms: 1.05x slower                                                |
| sqlglot_optimize           | 54.8 ms                                                | 57.4 ms: 1.05x slower                                                |
| docutils                   | 2.77 sec                                               | 2.90 sec: 1.05x slower                                               |
| mdp                        | 2.63 sec                                               | 2.76 sec: 1.05x slower                                               |
| pidigits                   | 187 ms                                                 | 197 ms: 1.05x slower                                                 |
| gunicorn                   | 1.24 ms                                                | 1.30 ms: 1.05x slower                                                |
| regex_v8                   | 23.1 ms                                                | 24.4 ms: 1.05x slower                                                |
| aiohttp                    | 1.15 ms                                                | 1.22 ms: 1.06x slower                                                |
| scimark_lu                 | 118 ms                                                 | 126 ms: 1.07x slower                                                 |
| python_startup_no_site     | 6.94 ms                                                | 7.57 ms: 1.09x slower                                                |
| go                         | 139 ms                                                 | 153 ms: 1.10x slower                                                 |
| python_startup             | 9.55 ms                                                | 11.0 ms: 1.15x slower                                                |
| create_gc_cycles           | 1.48 ms                                                | 1.76 ms: 1.19x slower                                                |
| telco                      | 7.10 ms                                                | 8.69 ms: 1.22x slower                                                |
| coverage                   | 72.7 ms                                                | 104 ms: 1.43x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                         |

Benchmark hidden because not significant (5): mypy2, deltablue, pycparser, bench_mp_pool, sqlite_synth
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240423-3.13.0a6+-07e95c4-JIT/bm-20240423-linux-x86_64-brandtbucher-justin_ghccc-3.13.0a6+-07e95c4.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 97.50% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x