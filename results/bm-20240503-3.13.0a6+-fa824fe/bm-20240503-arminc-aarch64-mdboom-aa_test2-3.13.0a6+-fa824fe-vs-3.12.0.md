# Results vs. 3.12.0

- fork: mdboom
- ref: aa_test2
- machine: linux-aarch64
- commit hash: fa824fe
- commit date: 2024-05-03
- overall geometric mean: 1.01x faster
- HPT reliability: 75.08%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.90x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 308 ms                                                                | 302 ms: 1.02x faster                                         |
| chameleon      | 8.81 ms                                                               | 9.17 ms: 1.04x slower                                        |
| docutils       | 2.98 sec                                                              | 3.10 sec: 1.04x slower                                       |
| tornado_http   | 136 ms                                                                | 128 ms: 1.06x faster                                         |
| Geometric mean | (ref)                                                                 | 1.00x slower                                                 |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_none            | 624 ms                                                                | 494 ms: 1.26x faster                                         |
| async_tree_none_tg         | 577 ms                                                                | 474 ms: 1.22x faster                                         |
| async_tree_memoization     | 777 ms                                                                | 650 ms: 1.19x faster                                         |
| async_tree_memoization_tg  | 740 ms                                                                | 620 ms: 1.19x faster                                         |
| async_tree_io_tg           | 1.40 sec                                                              | 1.21 sec: 1.16x faster                                       |
| async_tree_cpu_io_mixed    | 912 ms                                                                | 792 ms: 1.15x faster                                         |
| async_tree_io              | 1.41 sec                                                              | 1.23 sec: 1.14x faster                                       |
| async_tree_cpu_io_mixed_tg | 884 ms                                                                | 785 ms: 1.13x faster                                         |
| Geometric mean             | (ref)                                                                 | 1.18x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| float          | 92.1 ms                                                               | 91.0 ms: 1.01x faster                                        |
| pidigits       | 233 ms                                                                | 233 ms: 1.00x slower                                         |
| nbody          | 105 ms                                                                | 111 ms: 1.06x slower                                         |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 137 ms                                                                | 128 ms: 1.07x faster                                         |
| regex_dna      | 254 ms                                                                | 249 ms: 1.02x faster                                         |
| regex_effbot   | 4.64 ms                                                               | 4.88 ms: 1.05x slower                                        |
| regex_v8       | 28.3 ms                                                               | 31.1 ms: 1.10x slower                                        |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| unpickle_pure_python | 260 us                                                                | 248 us: 1.05x faster                                         |
| xml_etree_parse      | 195 ms                                                                | 188 ms: 1.04x faster                                         |
| tomli_loads          | 2.59 sec                                                              | 2.53 sec: 1.02x faster                                       |
| xml_etree_iterparse  | 150 ms                                                                | 148 ms: 1.02x faster                                         |
| pickle_pure_python   | 365 us                                                                | 363 us: 1.01x faster                                         |
| pickle               | 13.4 us                                                               | 13.5 us: 1.00x slower                                        |
| pickle_dict          | 37.3 us                                                               | 37.6 us: 1.01x slower                                        |
| xml_etree_generate   | 112 ms                                                                | 114 ms: 1.02x slower                                         |
| xml_etree_process    | 79.0 ms                                                               | 80.5 ms: 1.02x slower                                        |
| pickle_list          | 5.25 us                                                               | 5.36 us: 1.02x slower                                        |
| unpickle_list        | 6.17 us                                                               | 6.32 us: 1.02x slower                                        |
| json_loads           | 30.7 us                                                               | 32.2 us: 1.05x slower                                        |
| json_dumps           | 12.3 ms                                                               | 13.1 ms: 1.07x slower                                        |
| unpickle             | 18.5 us                                                               | 19.9 us: 1.08x slower                                        |
| Geometric mean       | (ref)                                                                 | 1.01x slower                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup | 11.4 ms                                                               | 12.5 ms: 1.10x slower                                        |
| Geometric mean | (ref)                                                                 | 1.05x slower                                                 |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_text     | 27.4 ms                                                               | 27.8 ms: 1.01x slower                                        |
| mako            | 12.9 ms                                                               | 13.2 ms: 1.02x slower                                        |
| django_template | 40.7 ms                                                               | 41.9 ms: 1.03x slower                                        |
| Geometric mean  | (ref)                                                                 | 1.02x slower                                                 |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_none            | 624 ms                                                                | 494 ms: 1.26x faster                                         |
| comprehensions             | 25.4 us                                                               | 20.5 us: 1.24x faster                                        |
| async_tree_none_tg         | 577 ms                                                                | 474 ms: 1.22x faster                                         |
| async_tree_memoization     | 777 ms                                                                | 650 ms: 1.19x faster                                         |
| async_tree_memoization_tg  | 740 ms                                                                | 620 ms: 1.19x faster                                         |
| raytrace                   | 353 ms                                                                | 297 ms: 1.19x faster                                         |
| async_tree_io_tg           | 1.40 sec                                                              | 1.21 sec: 1.16x faster                                       |
| generators                 | 43.5 ms                                                               | 37.7 ms: 1.15x faster                                        |
| async_tree_cpu_io_mixed    | 912 ms                                                                | 792 ms: 1.15x faster                                         |
| async_tree_io              | 1.41 sec                                                              | 1.23 sec: 1.14x faster                                       |
| async_tree_cpu_io_mixed_tg | 884 ms                                                                | 785 ms: 1.13x faster                                         |
| dulwich_log                | 62.0 ms                                                               | 57.1 ms: 1.08x faster                                        |
| pathlib                    | 24.5 ms                                                               | 22.7 ms: 1.08x faster                                        |
| logging_simple             | 7.63 us                                                               | 7.09 us: 1.08x faster                                        |
| logging_format             | 8.34 us                                                               | 7.76 us: 1.07x faster                                        |
| crypto_pyaes               | 86.6 ms                                                               | 80.7 ms: 1.07x faster                                        |
| scimark_lu                 | 146 ms                                                                | 136 ms: 1.07x faster                                         |
| sqlglot_transpile          | 1.83 ms                                                               | 1.71 ms: 1.07x faster                                        |
| regex_compile              | 137 ms                                                                | 128 ms: 1.07x faster                                         |
| sympy_sum                  | 154 ms                                                                | 145 ms: 1.07x faster                                         |
| tornado_http               | 136 ms                                                                | 128 ms: 1.06x faster                                         |
| deltablue                  | 4.12 ms                                                               | 3.88 ms: 1.06x faster                                        |
| sqlglot_parse              | 1.46 ms                                                               | 1.38 ms: 1.06x faster                                        |
| sympy_str                  | 280 ms                                                                | 265 ms: 1.06x faster                                         |
| unpickle_pure_python       | 260 us                                                                | 248 us: 1.05x faster                                         |
| chaos                      | 71.4 ms                                                               | 68.1 ms: 1.05x faster                                        |
| xml_etree_parse            | 195 ms                                                                | 188 ms: 1.04x faster                                         |
| bench_thread_pool          | 1.31 ms                                                               | 1.26 ms: 1.04x faster                                        |
| mdp                        | 3.41 sec                                                              | 3.31 sec: 1.03x faster                                       |
| scimark_monte_carlo        | 85.1 ms                                                               | 82.5 ms: 1.03x faster                                        |
| sympy_integrate            | 21.6 ms                                                               | 21.1 ms: 1.03x faster                                        |
| pycparser                  | 1.26 sec                                                              | 1.22 sec: 1.03x faster                                       |
| tomli_loads                | 2.59 sec                                                              | 2.53 sec: 1.02x faster                                       |
| dask                       | 376 ms                                                                | 369 ms: 1.02x faster                                         |
| regex_dna                  | 254 ms                                                                | 249 ms: 1.02x faster                                         |
| xml_etree_iterparse        | 150 ms                                                                | 148 ms: 1.02x faster                                         |
| 2to3                       | 308 ms                                                                | 302 ms: 1.02x faster                                         |
| async_generators           | 491 ms                                                                | 484 ms: 1.01x faster                                         |
| float                      | 92.1 ms                                                               | 91.0 ms: 1.01x faster                                        |
| nqueens                    | 99.2 ms                                                               | 98.3 ms: 1.01x faster                                        |
| pickle_pure_python         | 365 us                                                                | 363 us: 1.01x faster                                         |
| deepcopy_memo              | 49.6 us                                                               | 49.4 us: 1.01x faster                                        |
| deepcopy_reduce            | 4.10 us                                                               | 4.08 us: 1.00x faster                                        |
| pidigits                   | 233 ms                                                                | 233 ms: 1.00x slower                                         |
| pickle                     | 13.4 us                                                               | 13.5 us: 1.00x slower                                        |
| sympy_expand               | 454 ms                                                                | 455 ms: 1.00x slower                                         |
| thrift                     | 937 us                                                                | 942 us: 1.01x slower                                         |
| pickle_dict                | 37.3 us                                                               | 37.6 us: 1.01x slower                                        |
| sqlglot_optimize           | 61.3 ms                                                               | 61.9 ms: 1.01x slower                                        |
| meteor_contest             | 112 ms                                                                | 113 ms: 1.01x slower                                         |
| bench_mp_pool              | 7.05 ms                                                               | 7.14 ms: 1.01x slower                                        |
| sqlglot_normalize          | 126 ms                                                                | 127 ms: 1.01x slower                                         |
| genshi_text                | 27.4 ms                                                               | 27.8 ms: 1.01x slower                                        |
| asyncio_tcp_ssl            | 2.19 sec                                                              | 2.21 sec: 1.01x slower                                       |
| hexiom                     | 6.98 ms                                                               | 7.07 ms: 1.01x slower                                        |
| go                         | 157 ms                                                                | 160 ms: 1.02x slower                                         |
| xml_etree_generate         | 112 ms                                                                | 114 ms: 1.02x slower                                         |
| xml_etree_process          | 79.0 ms                                                               | 80.5 ms: 1.02x slower                                        |
| pickle_list                | 5.25 us                                                               | 5.36 us: 1.02x slower                                        |
| mako                       | 12.9 ms                                                               | 13.2 ms: 1.02x slower                                        |
| pprint_pformat             | 1.88 sec                                                              | 1.93 sec: 1.02x slower                                       |
| unpickle_list              | 6.17 us                                                               | 6.32 us: 1.02x slower                                        |
| pprint_safe_repr           | 916 ms                                                                | 939 ms: 1.02x slower                                         |
| fannkuch                   | 443 ms                                                                | 456 ms: 1.03x slower                                         |
| sqlite_synth               | 3.77 us                                                               | 3.88 us: 1.03x slower                                        |
| django_template            | 40.7 ms                                                               | 41.9 ms: 1.03x slower                                        |
| json                       | 5.54 ms                                                               | 5.72 ms: 1.03x slower                                        |
| docutils                   | 2.98 sec                                                              | 3.10 sec: 1.04x slower                                       |
| chameleon                  | 8.81 ms                                                               | 9.17 ms: 1.04x slower                                        |
| richards_super             | 58.5 ms                                                               | 61.0 ms: 1.04x slower                                        |
| json_loads                 | 30.7 us                                                               | 32.2 us: 1.05x slower                                        |
| regex_effbot               | 4.64 ms                                                               | 4.88 ms: 1.05x slower                                        |
| scimark_sparse_mat_mult    | 6.19 ms                                                               | 6.52 ms: 1.05x slower                                        |
| logging_silent             | 127 ns                                                                | 134 ns: 1.06x slower                                         |
| scimark_sor                | 150 ms                                                                | 159 ms: 1.06x slower                                         |
| scimark_fft                | 418 ms                                                                | 445 ms: 1.06x slower                                         |
| gunicorn                   | 1.14 ms                                                               | 1.21 ms: 1.06x slower                                        |
| nbody                      | 105 ms                                                                | 111 ms: 1.06x slower                                         |
| typing_runtime_protocols   | 181 us                                                                | 193 us: 1.07x slower                                         |
| json_dumps                 | 12.3 ms                                                               | 13.1 ms: 1.07x slower                                        |
| spectral_norm              | 131 ms                                                                | 141 ms: 1.08x slower                                         |
| unpickle                   | 18.5 us                                                               | 19.9 us: 1.08x slower                                        |
| richards                   | 50.9 ms                                                               | 55.5 ms: 1.09x slower                                        |
| python_startup             | 11.4 ms                                                               | 12.5 ms: 1.10x slower                                        |
| regex_v8                   | 28.3 ms                                                               | 31.1 ms: 1.10x slower                                        |
| coverage                   | 87.3 ms                                                               | 99.0 ms: 1.13x slower                                        |
| gc_traversal               | 4.40 ms                                                               | 5.01 ms: 1.14x slower                                        |
| create_gc_cycles           | 1.92 ms                                                               | 2.27 ms: 1.18x slower                                        |
| telco                      | 8.51 ms                                                               | 10.1 ms: 1.19x slower                                        |
| Geometric mean             | (ref)                                                                 | 1.01x faster                                                 |

Benchmark hidden because not significant (10): pylint, asyncio_tcp, python_startup_no_site, coroutines, pyflate, deepcopy, genshi_xml, asyncio_websockets, aiohttp, html5lib
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0.json: mypy2, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (1) of results/bm-20240503-3.13.0a6+-fa824fe/bm-20240503-arminc-aarch64-mdboom-aa_test2-3.13.0a6+-fa824fe.json: flaskblogging

# HPT report

- Reliability score: 75.08% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.90x