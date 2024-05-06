# Results vs. 3.12.0

- fork: brandtbucher
- ref: justin_preserve_most
- machine: linux-x86_64
- commit hash: 377ec17
- commit date: 2024-04-18
- overall geometric mean: 1.03x faster
- HPT reliability: 91.75%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 276 ms: 1.00x slower                                                         |
| chameleon      | 7.41 ms                                                | 6.92 ms: 1.07x faster                                                        |
| docutils       | 2.77 sec                                               | 2.90 sec: 1.05x slower                                                       |
| tornado_http   | 103 ms                                                 | 96.0 ms: 1.07x faster                                                        |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                                         |
| async_tree_none            | 472 ms                                                 | 354 ms: 1.33x faster                                                         |
| async_tree_memoization_tg  | 575 ms                                                 | 441 ms: 1.30x faster                                                         |
| async_tree_io              | 1.16 sec                                               | 923 ms: 1.25x faster                                                         |
| async_tree_io_tg           | 1.18 sec                                               | 945 ms: 1.25x faster                                                         |
| async_tree_memoization     | 578 ms                                                 | 465 ms: 1.24x faster                                                         |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 605 ms: 1.20x faster                                                         |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 609 ms: 1.19x faster                                                         |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 76.6 ms: 1.11x faster                                                        |
| nbody          | 97.0 ms                                                | 95.1 ms: 1.02x faster                                                        |
| pidigits       | 187 ms                                                 | 190 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 142 ms: 1.04x faster                                                         |
| regex_effbot   | 3.61 ms                                                | 3.78 ms: 1.05x slower                                                        |
| regex_dna      | 212 ms                                                 | 228 ms: 1.08x slower                                                         |
| regex_v8       | 23.1 ms                                                | 25.3 ms: 1.10x slower                                                        |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 1.99 sec: 1.17x faster                                                       |
| pickle_pure_python   | 324 us                                                 | 304 us: 1.07x faster                                                         |
| unpickle_list        | 5.29 us                                                | 5.00 us: 1.06x faster                                                        |
| unpickle             | 15.9 us                                                | 15.2 us: 1.05x faster                                                        |
| xml_etree_process    | 61.7 ms                                                | 60.0 ms: 1.03x faster                                                        |
| json_loads           | 28.5 us                                                | 27.8 us: 1.03x faster                                                        |
| xml_etree_generate   | 89.2 ms                                                | 87.2 ms: 1.02x faster                                                        |
| unpickle_pure_python | 230 us                                                 | 231 us: 1.00x slower                                                         |
| pickle_dict          | 35.5 us                                                | 35.7 us: 1.01x slower                                                        |
| pickle               | 11.6 us                                                | 11.7 us: 1.01x slower                                                        |
| pickle_list          | 5.08 us                                                | 5.15 us: 1.01x slower                                                        |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                        |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                 |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.55 ms: 1.09x slower                                                        |
| python_startup         | 9.55 ms                                                | 10.9 ms: 1.14x slower                                                        |
| Geometric mean         | (ref)                                                  | 1.12x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.6 ms: 1.13x faster                                                        |
| django_template | 34.6 ms                                                | 35.9 ms: 1.04x slower                                                        |
| Geometric mean  | (ref)                                                  | 1.04x faster                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 114 us: 1.39x faster                                                         |
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                                         |
| async_tree_none            | 472 ms                                                 | 354 ms: 1.33x faster                                                         |
| async_tree_memoization_tg  | 575 ms                                                 | 441 ms: 1.30x faster                                                         |
| async_tree_io              | 1.16 sec                                               | 923 ms: 1.25x faster                                                         |
| async_tree_io_tg           | 1.18 sec                                               | 945 ms: 1.25x faster                                                         |
| comprehensions             | 21.8 us                                                | 17.4 us: 1.25x faster                                                        |
| async_tree_memoization     | 578 ms                                                 | 465 ms: 1.24x faster                                                         |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 605 ms: 1.20x faster                                                         |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 609 ms: 1.19x faster                                                         |
| tomli_loads                | 2.33 sec                                               | 1.99 sec: 1.17x faster                                                       |
| raytrace                   | 312 ms                                                 | 269 ms: 1.16x faster                                                         |
| logging_format             | 7.23 us                                                | 6.38 us: 1.13x faster                                                        |
| mako                       | 11.9 ms                                                | 10.6 ms: 1.13x faster                                                        |
| logging_simple             | 6.46 us                                                | 5.81 us: 1.11x faster                                                        |
| scimark_monte_carlo        | 75.1 ms                                                | 67.8 ms: 1.11x faster                                                        |
| float                      | 84.7 ms                                                | 76.6 ms: 1.11x faster                                                        |
| crypto_pyaes               | 81.9 ms                                                | 74.1 ms: 1.10x faster                                                        |
| richards                   | 45.8 ms                                                | 42.1 ms: 1.09x faster                                                        |
| pathlib                    | 19.3 ms                                                | 17.9 ms: 1.08x faster                                                        |
| scimark_fft                | 382 ms                                                 | 353 ms: 1.08x faster                                                         |
| chaos                      | 67.0 ms                                                | 62.3 ms: 1.07x faster                                                        |
| chameleon                  | 7.41 ms                                                | 6.92 ms: 1.07x faster                                                        |
| tornado_http               | 103 ms                                                 | 96.0 ms: 1.07x faster                                                        |
| pickle_pure_python         | 324 us                                                 | 304 us: 1.07x faster                                                         |
| deepcopy_reduce            | 3.35 us                                                | 3.14 us: 1.06x faster                                                        |
| richards_super             | 51.5 ms                                                | 48.4 ms: 1.06x faster                                                        |
| fannkuch                   | 417 ms                                                 | 392 ms: 1.06x faster                                                         |
| deepcopy_memo              | 40.7 us                                                | 38.3 us: 1.06x faster                                                        |
| unpickle_list              | 5.29 us                                                | 5.00 us: 1.06x faster                                                        |
| unpickle                   | 15.9 us                                                | 15.2 us: 1.05x faster                                                        |
| regex_compile              | 148 ms                                                 | 142 ms: 1.04x faster                                                         |
| pyflate                    | 482 ms                                                 | 463 ms: 1.04x faster                                                         |
| deepcopy                   | 371 us                                                 | 356 us: 1.04x faster                                                         |
| generators                 | 31.2 ms                                                | 30.0 ms: 1.04x faster                                                        |
| pprint_safe_repr           | 776 ms                                                 | 748 ms: 1.04x faster                                                         |
| sqlglot_transpile          | 1.68 ms                                                | 1.63 ms: 1.03x faster                                                        |
| sqlglot_parse              | 1.36 ms                                                | 1.32 ms: 1.03x faster                                                        |
| xml_etree_process          | 61.7 ms                                                | 60.0 ms: 1.03x faster                                                        |
| logging_silent             | 104 ns                                                 | 102 ns: 1.03x faster                                                         |
| deltablue                  | 3.72 ms                                                | 3.62 ms: 1.03x faster                                                        |
| json_loads                 | 28.5 us                                                | 27.8 us: 1.03x faster                                                        |
| xml_etree_generate         | 89.2 ms                                                | 87.2 ms: 1.02x faster                                                        |
| json                       | 5.26 ms                                                | 5.15 ms: 1.02x faster                                                        |
| nbody                      | 97.0 ms                                                | 95.1 ms: 1.02x faster                                                        |
| coroutines                 | 23.2 ms                                                | 22.8 ms: 1.02x faster                                                        |
| pprint_pformat             | 1.57 sec                                               | 1.55 sec: 1.02x faster                                                       |
| sympy_str                  | 300 ms                                                 | 297 ms: 1.01x faster                                                         |
| sympy_sum                  | 169 ms                                                 | 168 ms: 1.01x faster                                                         |
| meteor_contest             | 112 ms                                                 | 112 ms: 1.01x faster                                                         |
| mdp                        | 2.63 sec                                               | 2.62 sec: 1.00x faster                                                       |
| unpickle_pure_python       | 230 us                                                 | 231 us: 1.00x slower                                                         |
| 2to3                       | 274 ms                                                 | 276 ms: 1.00x slower                                                         |
| pickle_dict                | 35.5 us                                                | 35.7 us: 1.01x slower                                                        |
| pickle                     | 11.6 us                                                | 11.7 us: 1.01x slower                                                        |
| dulwich_log                | 68.5 ms                                                | 69.3 ms: 1.01x slower                                                        |
| pickle_list                | 5.08 us                                                | 5.15 us: 1.01x slower                                                        |
| pidigits                   | 187 ms                                                 | 190 ms: 1.01x slower                                                         |
| bench_thread_pool          | 842 us                                                 | 855 us: 1.02x slower                                                         |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                        |
| sympy_integrate            | 21.4 ms                                                | 21.9 ms: 1.02x slower                                                        |
| gc_traversal               | 3.79 ms                                                | 3.89 ms: 1.03x slower                                                        |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.19 ms: 1.03x slower                                                        |
| pycparser                  | 1.18 sec                                               | 1.21 sec: 1.03x slower                                                       |
| sqlite_synth               | 2.83 us                                                | 2.91 us: 1.03x slower                                                        |
| scimark_sor                | 129 ms                                                 | 133 ms: 1.03x slower                                                         |
| asyncio_websockets         | 551 ms                                                 | 567 ms: 1.03x slower                                                         |
| spectral_norm              | 115 ms                                                 | 119 ms: 1.03x slower                                                         |
| sqlglot_normalize          | 110 ms                                                 | 114 ms: 1.03x slower                                                         |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.85 sec: 1.04x slower                                                       |
| django_template            | 34.6 ms                                                | 35.9 ms: 1.04x slower                                                        |
| asyncio_tcp                | 491 ms                                                 | 510 ms: 1.04x slower                                                         |
| sympy_expand               | 478 ms                                                 | 498 ms: 1.04x slower                                                         |
| docutils                   | 2.77 sec                                               | 2.90 sec: 1.05x slower                                                       |
| gunicorn                   | 1.24 ms                                                | 1.30 ms: 1.05x slower                                                        |
| regex_effbot               | 3.61 ms                                                | 3.78 ms: 1.05x slower                                                        |
| aiohttp                    | 1.15 ms                                                | 1.20 ms: 1.05x slower                                                        |
| sqlglot_optimize           | 54.8 ms                                                | 57.6 ms: 1.05x slower                                                        |
| hexiom                     | 6.41 ms                                                | 6.86 ms: 1.07x slower                                                        |
| nqueens                    | 83.3 ms                                                | 89.6 ms: 1.08x slower                                                        |
| regex_dna                  | 212 ms                                                 | 228 ms: 1.08x slower                                                         |
| python_startup_no_site     | 6.94 ms                                                | 7.55 ms: 1.09x slower                                                        |
| regex_v8                   | 23.1 ms                                                | 25.3 ms: 1.10x slower                                                        |
| go                         | 139 ms                                                 | 153 ms: 1.10x slower                                                         |
| scimark_lu                 | 118 ms                                                 | 131 ms: 1.11x slower                                                         |
| python_startup             | 9.55 ms                                                | 10.9 ms: 1.14x slower                                                        |
| create_gc_cycles           | 1.48 ms                                                | 1.76 ms: 1.19x slower                                                        |
| telco                      | 7.10 ms                                                | 8.64 ms: 1.22x slower                                                        |
| coverage                   | 72.7 ms                                                | 98.4 ms: 1.35x slower                                                        |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                                 |

Benchmark hidden because not significant (6): mypy2, bench_mp_pool, async_generators, xml_etree_iterparse, xml_etree_parse, dask
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240418-3.13.0a6+-377ec17-JIT/bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 91.75% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x