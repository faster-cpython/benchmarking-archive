# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_ghccc_cache_2
- machine: linux-x86_64
- commit hash: 7fbb9a2
- commit date: 2024-04-23
- overall geometric mean: 1.05x faster
- HPT reliability: 99.10%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.06x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 275 ms: 1.00x slower                                                         |
| chameleon      | 7.41 ms                                                | 6.88 ms: 1.08x faster                                                        |
| docutils       | 2.77 sec                                               | 2.89 sec: 1.05x slower                                                       |
| tornado_http   | 103 ms                                                 | 96.2 ms: 1.07x faster                                                        |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 339 ms: 1.33x faster                                                         |
| async_tree_none            | 472 ms                                                 | 356 ms: 1.32x faster                                                         |
| async_tree_memoization_tg  | 575 ms                                                 | 447 ms: 1.29x faster                                                         |
| async_tree_memoization     | 578 ms                                                 | 463 ms: 1.25x faster                                                         |
| async_tree_io_tg           | 1.18 sec                                               | 949 ms: 1.25x faster                                                         |
| async_tree_io              | 1.16 sec                                               | 944 ms: 1.22x faster                                                         |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 612 ms: 1.19x faster                                                         |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 620 ms: 1.17x faster                                                         |
| Geometric mean             | (ref)                                                  | 1.25x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 77.3 ms: 1.25x faster                                                        |
| float          | 84.7 ms                                                | 72.4 ms: 1.17x faster                                                        |
| pidigits       | 187 ms                                                 | 189 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                  | 1.13x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 139 ms: 1.07x faster                                                         |
| regex_effbot   | 3.61 ms                                                | 3.71 ms: 1.03x slower                                                        |
| regex_dna      | 212 ms                                                 | 218 ms: 1.03x slower                                                         |
| regex_v8       | 23.1 ms                                                | 24.7 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                  | 1.01x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 1.92 sec: 1.22x faster                                                       |
| pickle_pure_python   | 324 us                                                 | 304 us: 1.07x faster                                                         |
| xml_etree_parse      | 159 ms                                                 | 150 ms: 1.06x faster                                                         |
| unpickle             | 15.9 us                                                | 15.0 us: 1.06x faster                                                        |
| xml_etree_process    | 61.7 ms                                                | 59.2 ms: 1.04x faster                                                        |
| xml_etree_iterparse  | 107 ms                                                 | 103 ms: 1.04x faster                                                         |
| unpickle_pure_python | 230 us                                                 | 221 us: 1.04x faster                                                         |
| json_loads           | 28.5 us                                                | 27.5 us: 1.04x faster                                                        |
| xml_etree_generate   | 89.2 ms                                                | 86.7 ms: 1.03x faster                                                        |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                        |
| unpickle_list        | 5.29 us                                                | 5.42 us: 1.02x slower                                                        |
| pickle               | 11.6 us                                                | 11.9 us: 1.03x slower                                                        |
| pickle_dict          | 35.5 us                                                | 36.8 us: 1.04x slower                                                        |
| pickle_list          | 5.08 us                                                | 5.38 us: 1.06x slower                                                        |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.63 ms: 1.10x slower                                                        |
| python_startup         | 9.55 ms                                                | 11.1 ms: 1.16x slower                                                        |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.1 ms: 1.17x faster                                                        |
| django_template | 34.6 ms                                                | 35.6 ms: 1.03x slower                                                        |
| Geometric mean  | (ref)                                                  | 1.07x faster                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 111 us: 1.42x faster                                                         |
| async_tree_none_tg         | 450 ms                                                 | 339 ms: 1.33x faster                                                         |
| async_tree_none            | 472 ms                                                 | 356 ms: 1.32x faster                                                         |
| async_tree_memoization_tg  | 575 ms                                                 | 447 ms: 1.29x faster                                                         |
| comprehensions             | 21.8 us                                                | 17.1 us: 1.28x faster                                                        |
| scimark_fft                | 382 ms                                                 | 302 ms: 1.26x faster                                                         |
| nbody                      | 97.0 ms                                                | 77.3 ms: 1.25x faster                                                        |
| async_tree_memoization     | 578 ms                                                 | 463 ms: 1.25x faster                                                         |
| async_tree_io_tg           | 1.18 sec                                               | 949 ms: 1.25x faster                                                         |
| async_tree_io              | 1.16 sec                                               | 944 ms: 1.22x faster                                                         |
| tomli_loads                | 2.33 sec                                               | 1.92 sec: 1.22x faster                                                       |
| crypto_pyaes               | 81.9 ms                                                | 68.3 ms: 1.20x faster                                                        |
| fannkuch                   | 417 ms                                                 | 349 ms: 1.20x faster                                                         |
| scimark_monte_carlo        | 75.1 ms                                                | 63.3 ms: 1.19x faster                                                        |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 612 ms: 1.19x faster                                                         |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.29 ms: 1.18x faster                                                        |
| spectral_norm              | 115 ms                                                 | 97.7 ms: 1.18x faster                                                        |
| mako                       | 11.9 ms                                                | 10.1 ms: 1.17x faster                                                        |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 620 ms: 1.17x faster                                                         |
| float                      | 84.7 ms                                                | 72.4 ms: 1.17x faster                                                        |
| raytrace                   | 312 ms                                                 | 276 ms: 1.13x faster                                                         |
| logging_format             | 7.23 us                                                | 6.49 us: 1.11x faster                                                        |
| logging_simple             | 6.46 us                                                | 5.84 us: 1.11x faster                                                        |
| chaos                      | 67.0 ms                                                | 60.8 ms: 1.10x faster                                                        |
| richards                   | 45.8 ms                                                | 42.0 ms: 1.09x faster                                                        |
| pathlib                    | 19.3 ms                                                | 17.8 ms: 1.08x faster                                                        |
| pprint_safe_repr           | 776 ms                                                 | 718 ms: 1.08x faster                                                         |
| chameleon                  | 7.41 ms                                                | 6.88 ms: 1.08x faster                                                        |
| pyflate                    | 482 ms                                                 | 450 ms: 1.07x faster                                                         |
| richards_super             | 51.5 ms                                                | 48.2 ms: 1.07x faster                                                        |
| tornado_http               | 103 ms                                                 | 96.2 ms: 1.07x faster                                                        |
| mypy2                      | 830 ms                                                 | 778 ms: 1.07x faster                                                         |
| pickle_pure_python         | 324 us                                                 | 304 us: 1.07x faster                                                         |
| regex_compile              | 148 ms                                                 | 139 ms: 1.07x faster                                                         |
| xml_etree_parse            | 159 ms                                                 | 150 ms: 1.06x faster                                                         |
| deepcopy_memo              | 40.7 us                                                | 38.4 us: 1.06x faster                                                        |
| deepcopy_reduce            | 3.35 us                                                | 3.16 us: 1.06x faster                                                        |
| unpickle                   | 15.9 us                                                | 15.0 us: 1.06x faster                                                        |
| pprint_pformat             | 1.57 sec                                               | 1.50 sec: 1.05x faster                                                       |
| sqlglot_parse              | 1.36 ms                                                | 1.30 ms: 1.04x faster                                                        |
| xml_etree_process          | 61.7 ms                                                | 59.2 ms: 1.04x faster                                                        |
| json                       | 5.26 ms                                                | 5.05 ms: 1.04x faster                                                        |
| generators                 | 31.2 ms                                                | 30.0 ms: 1.04x faster                                                        |
| xml_etree_iterparse        | 107 ms                                                 | 103 ms: 1.04x faster                                                         |
| unpickle_pure_python       | 230 us                                                 | 221 us: 1.04x faster                                                         |
| deepcopy                   | 371 us                                                 | 358 us: 1.04x faster                                                         |
| json_loads                 | 28.5 us                                                | 27.5 us: 1.04x faster                                                        |
| sqlglot_transpile          | 1.68 ms                                                | 1.63 ms: 1.03x faster                                                        |
| meteor_contest             | 112 ms                                                 | 109 ms: 1.03x faster                                                         |
| sympy_str                  | 300 ms                                                 | 290 ms: 1.03x faster                                                         |
| logging_silent             | 104 ns                                                 | 102 ns: 1.03x faster                                                         |
| coroutines                 | 23.2 ms                                                | 22.5 ms: 1.03x faster                                                        |
| xml_etree_generate         | 89.2 ms                                                | 86.7 ms: 1.03x faster                                                        |
| gc_traversal               | 3.79 ms                                                | 3.70 ms: 1.03x faster                                                        |
| sympy_sum                  | 169 ms                                                 | 166 ms: 1.02x faster                                                         |
| pycparser                  | 1.18 sec                                               | 1.16 sec: 1.02x faster                                                       |
| 2to3                       | 274 ms                                                 | 275 ms: 1.00x slower                                                         |
| sqlite_synth               | 2.83 us                                                | 2.85 us: 1.01x slower                                                        |
| pidigits                   | 187 ms                                                 | 189 ms: 1.01x slower                                                         |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                        |
| dulwich_log                | 68.5 ms                                                | 69.1 ms: 1.01x slower                                                        |
| async_generators           | 463 ms                                                 | 470 ms: 1.02x slower                                                         |
| sympy_integrate            | 21.4 ms                                                | 21.8 ms: 1.02x slower                                                        |
| sqlglot_normalize          | 110 ms                                                 | 112 ms: 1.02x slower                                                         |
| nqueens                    | 83.3 ms                                                | 85.1 ms: 1.02x slower                                                        |
| hexiom                     | 6.41 ms                                                | 6.56 ms: 1.02x slower                                                        |
| bench_thread_pool          | 842 us                                                 | 862 us: 1.02x slower                                                         |
| unpickle_list              | 5.29 us                                                | 5.42 us: 1.02x slower                                                        |
| scimark_sor                | 129 ms                                                 | 132 ms: 1.03x slower                                                         |
| regex_effbot               | 3.61 ms                                                | 3.71 ms: 1.03x slower                                                        |
| pickle                     | 11.6 us                                                | 11.9 us: 1.03x slower                                                        |
| asyncio_websockets         | 551 ms                                                 | 566 ms: 1.03x slower                                                         |
| asyncio_tcp                | 491 ms                                                 | 504 ms: 1.03x slower                                                         |
| django_template            | 34.6 ms                                                | 35.6 ms: 1.03x slower                                                        |
| regex_dna                  | 212 ms                                                 | 218 ms: 1.03x slower                                                         |
| sympy_expand               | 478 ms                                                 | 493 ms: 1.03x slower                                                         |
| sqlglot_optimize           | 54.8 ms                                                | 56.7 ms: 1.03x slower                                                        |
| pickle_dict                | 35.5 us                                                | 36.8 us: 1.04x slower                                                        |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                                       |
| docutils                   | 2.77 sec                                               | 2.89 sec: 1.05x slower                                                       |
| gunicorn                   | 1.24 ms                                                | 1.30 ms: 1.05x slower                                                        |
| aiohttp                    | 1.15 ms                                                | 1.20 ms: 1.05x slower                                                        |
| scimark_lu                 | 118 ms                                                 | 124 ms: 1.05x slower                                                         |
| go                         | 139 ms                                                 | 147 ms: 1.06x slower                                                         |
| pickle_list                | 5.08 us                                                | 5.38 us: 1.06x slower                                                        |
| regex_v8                   | 23.1 ms                                                | 24.7 ms: 1.07x slower                                                        |
| python_startup_no_site     | 6.94 ms                                                | 7.63 ms: 1.10x slower                                                        |
| python_startup             | 9.55 ms                                                | 11.1 ms: 1.16x slower                                                        |
| create_gc_cycles           | 1.48 ms                                                | 1.75 ms: 1.19x slower                                                        |
| telco                      | 7.10 ms                                                | 8.53 ms: 1.20x slower                                                        |
| coverage                   | 72.7 ms                                                | 97.2 ms: 1.34x slower                                                        |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                                 |

Benchmark hidden because not significant (4): deltablue, mdp, bench_mp_pool, dask
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240423-3.13.0a6+-7fbb9a2-JIT/bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.10% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.06x