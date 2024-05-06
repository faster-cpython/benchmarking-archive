# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_refactor
- machine: linux-x86_64
- commit hash: 8ca0f58
- commit date: 2024-04-27
- overall geometric mean: 1.03x faster
- HPT reliability: 97.79%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 276 ms: 1.01x slower                                                    |
| chameleon      | 7.41 ms                                                | 7.02 ms: 1.06x faster                                                   |
| docutils       | 2.77 sec                                               | 2.90 sec: 1.05x slower                                                  |
| tornado_http   | 103 ms                                                 | 95.6 ms: 1.07x faster                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                                    |
| async_tree_none            | 472 ms                                                 | 355 ms: 1.33x faster                                                    |
| async_tree_memoization_tg  | 575 ms                                                 | 441 ms: 1.30x faster                                                    |
| async_tree_memoization     | 578 ms                                                 | 465 ms: 1.24x faster                                                    |
| async_tree_io              | 1.16 sec                                               | 930 ms: 1.24x faster                                                    |
| async_tree_io_tg           | 1.18 sec                                               | 952 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 604 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 610 ms: 1.19x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 77.2 ms: 1.10x faster                                                   |
| nbody          | 97.0 ms                                                | 89.9 ms: 1.08x faster                                                   |
| pidigits       | 187 ms                                                 | 189 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                  | 1.05x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 140 ms: 1.06x faster                                                    |
| regex_effbot   | 3.61 ms                                                | 3.70 ms: 1.03x slower                                                   |
| regex_dna      | 212 ms                                                 | 227 ms: 1.07x slower                                                    |
| regex_v8       | 23.1 ms                                                | 26.2 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.04 sec: 1.14x faster                                                  |
| pickle_pure_python   | 324 us                                                 | 301 us: 1.07x faster                                                    |
| xml_etree_parse      | 159 ms                                                 | 153 ms: 1.04x faster                                                    |
| xml_etree_process    | 61.7 ms                                                | 59.6 ms: 1.04x faster                                                   |
| xml_etree_generate   | 89.2 ms                                                | 87.0 ms: 1.03x faster                                                   |
| xml_etree_iterparse  | 107 ms                                                 | 104 ms: 1.02x faster                                                    |
| unpickle_list        | 5.29 us                                                | 5.20 us: 1.02x faster                                                   |
| json_loads           | 28.5 us                                                | 28.0 us: 1.02x faster                                                   |
| pickle_dict          | 35.5 us                                                | 35.1 us: 1.01x faster                                                   |
| pickle               | 11.6 us                                                | 11.5 us: 1.01x faster                                                   |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                   |
| unpickle_pure_python | 230 us                                                 | 233 us: 1.01x slower                                                    |
| unpickle             | 15.9 us                                                | 16.3 us: 1.02x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                            |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.57 ms: 1.09x slower                                                   |
| python_startup         | 9.55 ms                                                | 11.0 ms: 1.15x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.12x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.8 ms: 1.10x faster                                                   |
| django_template | 34.6 ms                                                | 35.7 ms: 1.03x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 113 us: 1.39x faster                                                    |
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                                    |
| async_tree_none            | 472 ms                                                 | 355 ms: 1.33x faster                                                    |
| async_tree_memoization_tg  | 575 ms                                                 | 441 ms: 1.30x faster                                                    |
| async_tree_memoization     | 578 ms                                                 | 465 ms: 1.24x faster                                                    |
| async_tree_io              | 1.16 sec                                               | 930 ms: 1.24x faster                                                    |
| async_tree_io_tg           | 1.18 sec                                               | 952 ms: 1.24x faster                                                    |
| comprehensions             | 21.8 us                                                | 17.9 us: 1.22x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 604 ms: 1.20x faster                                                    |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 610 ms: 1.19x faster                                                    |
| raytrace                   | 312 ms                                                 | 272 ms: 1.15x faster                                                    |
| tomli_loads                | 2.33 sec                                               | 2.04 sec: 1.14x faster                                                  |
| scimark_fft                | 382 ms                                                 | 336 ms: 1.14x faster                                                    |
| logging_format             | 7.23 us                                                | 6.43 us: 1.12x faster                                                   |
| logging_simple             | 6.46 us                                                | 5.77 us: 1.12x faster                                                   |
| crypto_pyaes               | 81.9 ms                                                | 73.7 ms: 1.11x faster                                                   |
| mako                       | 11.9 ms                                                | 10.8 ms: 1.10x faster                                                   |
| float                      | 84.7 ms                                                | 77.2 ms: 1.10x faster                                                   |
| pathlib                    | 19.3 ms                                                | 17.7 ms: 1.10x faster                                                   |
| scimark_monte_carlo        | 75.1 ms                                                | 69.1 ms: 1.09x faster                                                   |
| nbody                      | 97.0 ms                                                | 89.9 ms: 1.08x faster                                                   |
| fannkuch                   | 417 ms                                                 | 387 ms: 1.08x faster                                                    |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.69 ms: 1.08x faster                                                   |
| deepcopy_memo              | 40.7 us                                                | 37.9 us: 1.08x faster                                                   |
| pickle_pure_python         | 324 us                                                 | 301 us: 1.07x faster                                                    |
| tornado_http               | 103 ms                                                 | 95.6 ms: 1.07x faster                                                   |
| logging_silent             | 104 ns                                                 | 98.0 ns: 1.07x faster                                                   |
| richards                   | 45.8 ms                                                | 43.1 ms: 1.06x faster                                                   |
| chaos                      | 67.0 ms                                                | 63.2 ms: 1.06x faster                                                   |
| regex_compile              | 148 ms                                                 | 140 ms: 1.06x faster                                                    |
| chameleon                  | 7.41 ms                                                | 7.02 ms: 1.06x faster                                                   |
| deepcopy_reduce            | 3.35 us                                                | 3.17 us: 1.05x faster                                                   |
| deepcopy                   | 371 us                                                 | 353 us: 1.05x faster                                                    |
| pyflate                    | 482 ms                                                 | 459 ms: 1.05x faster                                                    |
| richards_super             | 51.5 ms                                                | 49.0 ms: 1.05x faster                                                   |
| pprint_safe_repr           | 776 ms                                                 | 740 ms: 1.05x faster                                                    |
| generators                 | 31.2 ms                                                | 29.8 ms: 1.05x faster                                                   |
| xml_etree_parse            | 159 ms                                                 | 153 ms: 1.04x faster                                                    |
| xml_etree_process          | 61.7 ms                                                | 59.6 ms: 1.04x faster                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.32 ms: 1.03x faster                                                   |
| sqlglot_transpile          | 1.68 ms                                                | 1.63 ms: 1.03x faster                                                   |
| sympy_str                  | 300 ms                                                 | 291 ms: 1.03x faster                                                    |
| json                       | 5.26 ms                                                | 5.12 ms: 1.03x faster                                                   |
| deltablue                  | 3.72 ms                                                | 3.62 ms: 1.03x faster                                                   |
| xml_etree_generate         | 89.2 ms                                                | 87.0 ms: 1.03x faster                                                   |
| coroutines                 | 23.2 ms                                                | 22.6 ms: 1.02x faster                                                   |
| xml_etree_iterparse        | 107 ms                                                 | 104 ms: 1.02x faster                                                    |
| spectral_norm              | 115 ms                                                 | 112 ms: 1.02x faster                                                    |
| sympy_sum                  | 169 ms                                                 | 165 ms: 1.02x faster                                                    |
| meteor_contest             | 112 ms                                                 | 110 ms: 1.02x faster                                                    |
| unpickle_list              | 5.29 us                                                | 5.20 us: 1.02x faster                                                   |
| json_loads                 | 28.5 us                                                | 28.0 us: 1.02x faster                                                   |
| pprint_pformat             | 1.57 sec                                               | 1.54 sec: 1.02x faster                                                  |
| pickle_dict                | 35.5 us                                                | 35.1 us: 1.01x faster                                                   |
| pickle                     | 11.6 us                                                | 11.5 us: 1.01x faster                                                   |
| 2to3                       | 274 ms                                                 | 276 ms: 1.01x slower                                                    |
| dulwich_log                | 68.5 ms                                                | 69.1 ms: 1.01x slower                                                   |
| pidigits                   | 187 ms                                                 | 189 ms: 1.01x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                   |
| sqlglot_normalize          | 110 ms                                                 | 111 ms: 1.01x slower                                                    |
| bench_thread_pool          | 842 us                                                 | 852 us: 1.01x slower                                                    |
| unpickle_pure_python       | 230 us                                                 | 233 us: 1.01x slower                                                    |
| sympy_integrate            | 21.4 ms                                                | 21.8 ms: 1.02x slower                                                   |
| sqlite_synth               | 2.83 us                                                | 2.89 us: 1.02x slower                                                   |
| sympy_expand               | 478 ms                                                 | 489 ms: 1.02x slower                                                    |
| unpickle                   | 15.9 us                                                | 16.3 us: 1.02x slower                                                   |
| regex_effbot               | 3.61 ms                                                | 3.70 ms: 1.03x slower                                                   |
| pycparser                  | 1.18 sec                                               | 1.21 sec: 1.03x slower                                                  |
| asyncio_websockets         | 551 ms                                                 | 566 ms: 1.03x slower                                                    |
| django_template            | 34.6 ms                                                | 35.7 ms: 1.03x slower                                                   |
| sqlglot_optimize           | 54.8 ms                                                | 56.7 ms: 1.03x slower                                                   |
| asyncio_tcp                | 491 ms                                                 | 509 ms: 1.04x slower                                                    |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                                  |
| gunicorn                   | 1.24 ms                                                | 1.30 ms: 1.04x slower                                                   |
| docutils                   | 2.77 sec                                               | 2.90 sec: 1.05x slower                                                  |
| aiohttp                    | 1.15 ms                                                | 1.21 ms: 1.05x slower                                                   |
| mdp                        | 2.63 sec                                               | 2.78 sec: 1.06x slower                                                  |
| gc_traversal               | 3.79 ms                                                | 4.01 ms: 1.06x slower                                                   |
| nqueens                    | 83.3 ms                                                | 88.6 ms: 1.06x slower                                                   |
| regex_dna                  | 212 ms                                                 | 227 ms: 1.07x slower                                                    |
| hexiom                     | 6.41 ms                                                | 6.86 ms: 1.07x slower                                                   |
| python_startup_no_site     | 6.94 ms                                                | 7.57 ms: 1.09x slower                                                   |
| go                         | 139 ms                                                 | 153 ms: 1.09x slower                                                    |
| scimark_lu                 | 118 ms                                                 | 130 ms: 1.11x slower                                                    |
| regex_v8                   | 23.1 ms                                                | 26.2 ms: 1.13x slower                                                   |
| python_startup             | 9.55 ms                                                | 11.0 ms: 1.15x slower                                                   |
| create_gc_cycles           | 1.48 ms                                                | 1.76 ms: 1.19x slower                                                   |
| telco                      | 7.10 ms                                                | 8.56 ms: 1.21x slower                                                   |
| coverage                   | 72.7 ms                                                | 98.7 ms: 1.36x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                            |

Benchmark hidden because not significant (6): mypy2, async_generators, pickle_list, dask, bench_mp_pool, scimark_sor
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240427-3.13.0a6+-8ca0f58-JIT/bm-20240427-linux-x86_64-brandtbucher-justin_refactor-3.13.0a6+-8ca0f58.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 97.79% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x