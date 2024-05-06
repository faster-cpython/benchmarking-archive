# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_ghccc_cache_1
- machine: linux-x86_64
- commit hash: b8620f7
- commit date: 2024-04-23
- overall geometric mean: 1.04x faster
- HPT reliability: 98.36%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.07x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 277 ms: 1.01x slower                                                         |
| chameleon      | 7.41 ms                                                | 7.12 ms: 1.04x faster                                                        |
| docutils       | 2.77 sec                                               | 2.90 sec: 1.05x slower                                                       |
| tornado_http   | 103 ms                                                 | 95.7 ms: 1.07x faster                                                        |
| Geometric mean | (ref)                                                  | 1.01x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 337 ms: 1.33x faster                                                         |
| async_tree_none            | 472 ms                                                 | 359 ms: 1.32x faster                                                         |
| async_tree_memoization_tg  | 575 ms                                                 | 443 ms: 1.30x faster                                                         |
| async_tree_memoization     | 578 ms                                                 | 462 ms: 1.25x faster                                                         |
| async_tree_io_tg           | 1.18 sec                                               | 955 ms: 1.24x faster                                                         |
| async_tree_io              | 1.16 sec                                               | 949 ms: 1.22x faster                                                         |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 604 ms: 1.20x faster                                                         |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 611 ms: 1.19x faster                                                         |
| Geometric mean             | (ref)                                                  | 1.25x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 81.0 ms: 1.20x faster                                                        |
| float          | 84.7 ms                                                | 73.7 ms: 1.15x faster                                                        |
| pidigits       | 187 ms                                                 | 189 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                  | 1.11x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 140 ms: 1.06x faster                                                         |
| regex_v8       | 23.1 ms                                                | 25.0 ms: 1.08x slower                                                        |
| regex_dna      | 212 ms                                                 | 229 ms: 1.08x slower                                                         |
| regex_effbot   | 3.61 ms                                                | 4.21 ms: 1.16x slower                                                        |
| Geometric mean | (ref)                                                  | 1.06x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 1.92 sec: 1.21x faster                                                       |
| xml_etree_parse      | 159 ms                                                 | 148 ms: 1.07x faster                                                         |
| xml_etree_iterparse  | 107 ms                                                 | 101 ms: 1.06x faster                                                         |
| pickle_pure_python   | 324 us                                                 | 309 us: 1.05x faster                                                         |
| json_loads           | 28.5 us                                                | 27.3 us: 1.04x faster                                                        |
| unpickle             | 15.9 us                                                | 15.3 us: 1.04x faster                                                        |
| unpickle_pure_python | 230 us                                                 | 223 us: 1.03x faster                                                         |
| xml_etree_process    | 61.7 ms                                                | 60.6 ms: 1.02x faster                                                        |
| xml_etree_generate   | 89.2 ms                                                | 87.6 ms: 1.02x faster                                                        |
| unpickle_list        | 5.29 us                                                | 5.20 us: 1.02x faster                                                        |
| pickle_list          | 5.08 us                                                | 5.06 us: 1.01x faster                                                        |
| pickle               | 11.6 us                                                | 11.8 us: 1.01x slower                                                        |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                        |
| Geometric mean       | (ref)                                                  | 1.04x faster                                                                 |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.68 ms: 1.11x slower                                                        |
| python_startup         | 9.55 ms                                                | 11.1 ms: 1.17x slower                                                        |
| Geometric mean         | (ref)                                                  | 1.14x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 9.91 ms: 1.20x faster                                                        |
| django_template | 34.6 ms                                                | 35.8 ms: 1.03x slower                                                        |
| Geometric mean  | (ref)                                                  | 1.08x faster                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 115 us: 1.37x faster                                                         |
| async_tree_none_tg         | 450 ms                                                 | 337 ms: 1.33x faster                                                         |
| async_tree_none            | 472 ms                                                 | 359 ms: 1.32x faster                                                         |
| async_tree_memoization_tg  | 575 ms                                                 | 443 ms: 1.30x faster                                                         |
| comprehensions             | 21.8 us                                                | 16.9 us: 1.29x faster                                                        |
| async_tree_memoization     | 578 ms                                                 | 462 ms: 1.25x faster                                                         |
| async_tree_io_tg           | 1.18 sec                                               | 955 ms: 1.24x faster                                                         |
| scimark_fft                | 382 ms                                                 | 310 ms: 1.23x faster                                                         |
| async_tree_io              | 1.16 sec                                               | 949 ms: 1.22x faster                                                         |
| tomli_loads                | 2.33 sec                                               | 1.92 sec: 1.21x faster                                                       |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 604 ms: 1.20x faster                                                         |
| mako                       | 11.9 ms                                                | 9.91 ms: 1.20x faster                                                        |
| nbody                      | 97.0 ms                                                | 81.0 ms: 1.20x faster                                                        |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 611 ms: 1.19x faster                                                         |
| crypto_pyaes               | 81.9 ms                                                | 68.9 ms: 1.19x faster                                                        |
| scimark_monte_carlo        | 75.1 ms                                                | 63.6 ms: 1.18x faster                                                        |
| fannkuch                   | 417 ms                                                 | 356 ms: 1.17x faster                                                         |
| spectral_norm              | 115 ms                                                 | 98.5 ms: 1.17x faster                                                        |
| float                      | 84.7 ms                                                | 73.7 ms: 1.15x faster                                                        |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.42 ms: 1.14x faster                                                        |
| raytrace                   | 312 ms                                                 | 274 ms: 1.14x faster                                                         |
| logging_format             | 7.23 us                                                | 6.41 us: 1.13x faster                                                        |
| logging_simple             | 6.46 us                                                | 5.76 us: 1.12x faster                                                        |
| pyflate                    | 482 ms                                                 | 443 ms: 1.09x faster                                                         |
| pathlib                    | 19.3 ms                                                | 17.8 ms: 1.09x faster                                                        |
| chaos                      | 67.0 ms                                                | 61.8 ms: 1.08x faster                                                        |
| richards                   | 45.8 ms                                                | 42.4 ms: 1.08x faster                                                        |
| pprint_safe_repr           | 776 ms                                                 | 717 ms: 1.08x faster                                                         |
| xml_etree_parse            | 159 ms                                                 | 148 ms: 1.07x faster                                                         |
| tornado_http               | 103 ms                                                 | 95.7 ms: 1.07x faster                                                        |
| regex_compile              | 148 ms                                                 | 140 ms: 1.06x faster                                                         |
| pprint_pformat             | 1.57 sec                                               | 1.48 sec: 1.06x faster                                                       |
| xml_etree_iterparse        | 107 ms                                                 | 101 ms: 1.06x faster                                                         |
| logging_silent             | 104 ns                                                 | 99.0 ns: 1.05x faster                                                        |
| richards_super             | 51.5 ms                                                | 49.1 ms: 1.05x faster                                                        |
| pickle_pure_python         | 324 us                                                 | 309 us: 1.05x faster                                                         |
| json_loads                 | 28.5 us                                                | 27.3 us: 1.04x faster                                                        |
| generators                 | 31.2 ms                                                | 29.9 ms: 1.04x faster                                                        |
| deepcopy_memo              | 40.7 us                                                | 39.1 us: 1.04x faster                                                        |
| deepcopy_reduce            | 3.35 us                                                | 3.21 us: 1.04x faster                                                        |
| chameleon                  | 7.41 ms                                                | 7.12 ms: 1.04x faster                                                        |
| meteor_contest             | 112 ms                                                 | 108 ms: 1.04x faster                                                         |
| sqlglot_parse              | 1.36 ms                                                | 1.31 ms: 1.04x faster                                                        |
| unpickle                   | 15.9 us                                                | 15.3 us: 1.04x faster                                                        |
| json                       | 5.26 ms                                                | 5.08 ms: 1.04x faster                                                        |
| sqlglot_transpile          | 1.68 ms                                                | 1.63 ms: 1.03x faster                                                        |
| unpickle_pure_python       | 230 us                                                 | 223 us: 1.03x faster                                                         |
| coroutines                 | 23.2 ms                                                | 22.6 ms: 1.03x faster                                                        |
| sympy_str                  | 300 ms                                                 | 293 ms: 1.02x faster                                                         |
| deltablue                  | 3.72 ms                                                | 3.64 ms: 1.02x faster                                                        |
| deepcopy                   | 371 us                                                 | 364 us: 1.02x faster                                                         |
| xml_etree_process          | 61.7 ms                                                | 60.6 ms: 1.02x faster                                                        |
| xml_etree_generate         | 89.2 ms                                                | 87.6 ms: 1.02x faster                                                        |
| unpickle_list              | 5.29 us                                                | 5.20 us: 1.02x faster                                                        |
| gc_traversal               | 3.79 ms                                                | 3.74 ms: 1.02x faster                                                        |
| sympy_sum                  | 169 ms                                                 | 167 ms: 1.01x faster                                                         |
| pickle_list                | 5.08 us                                                | 5.06 us: 1.01x faster                                                        |
| mdp                        | 2.63 sec                                               | 2.64 sec: 1.00x slower                                                       |
| sqlite_synth               | 2.83 us                                                | 2.85 us: 1.01x slower                                                        |
| dulwich_log                | 68.5 ms                                                | 69.0 ms: 1.01x slower                                                        |
| pidigits                   | 187 ms                                                 | 189 ms: 1.01x slower                                                         |
| async_generators           | 463 ms                                                 | 467 ms: 1.01x slower                                                         |
| 2to3                       | 274 ms                                                 | 277 ms: 1.01x slower                                                         |
| pickle                     | 11.6 us                                                | 11.8 us: 1.01x slower                                                        |
| hexiom                     | 6.41 ms                                                | 6.54 ms: 1.02x slower                                                        |
| sympy_integrate            | 21.4 ms                                                | 21.9 ms: 1.02x slower                                                        |
| asyncio_websockets         | 551 ms                                                 | 563 ms: 1.02x slower                                                         |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                        |
| bench_thread_pool          | 842 us                                                 | 864 us: 1.03x slower                                                         |
| sqlglot_normalize          | 110 ms                                                 | 114 ms: 1.03x slower                                                         |
| sympy_expand               | 478 ms                                                 | 494 ms: 1.03x slower                                                         |
| django_template            | 34.6 ms                                                | 35.8 ms: 1.03x slower                                                        |
| nqueens                    | 83.3 ms                                                | 86.7 ms: 1.04x slower                                                        |
| sqlglot_optimize           | 54.8 ms                                                | 57.1 ms: 1.04x slower                                                        |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                                       |
| docutils                   | 2.77 sec                                               | 2.90 sec: 1.05x slower                                                       |
| gunicorn                   | 1.24 ms                                                | 1.30 ms: 1.05x slower                                                        |
| asyncio_tcp                | 491 ms                                                 | 515 ms: 1.05x slower                                                         |
| aiohttp                    | 1.15 ms                                                | 1.21 ms: 1.05x slower                                                        |
| go                         | 139 ms                                                 | 148 ms: 1.06x slower                                                         |
| scimark_lu                 | 118 ms                                                 | 125 ms: 1.06x slower                                                         |
| regex_v8                   | 23.1 ms                                                | 25.0 ms: 1.08x slower                                                        |
| regex_dna                  | 212 ms                                                 | 229 ms: 1.08x slower                                                         |
| python_startup_no_site     | 6.94 ms                                                | 7.68 ms: 1.11x slower                                                        |
| regex_effbot               | 3.61 ms                                                | 4.21 ms: 1.16x slower                                                        |
| python_startup             | 9.55 ms                                                | 11.1 ms: 1.17x slower                                                        |
| create_gc_cycles           | 1.48 ms                                                | 1.77 ms: 1.20x slower                                                        |
| telco                      | 7.10 ms                                                | 8.56 ms: 1.21x slower                                                        |
| coverage                   | 72.7 ms                                                | 98.1 ms: 1.35x slower                                                        |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                                 |

Benchmark hidden because not significant (6): mypy2, pycparser, scimark_sor, bench_mp_pool, pickle_dict, dask
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240423-3.13.0a6+-b8620f7-JIT/bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 98.36% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.07x