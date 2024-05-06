# Results vs. 3.12.0

- fork: python
- ref: main
- machine: linux-aarch64
- commit hash: 2770d5c
- commit date: 2024-05-02
- overall geometric mean: 1.03x faster
- HPT reliability: 99.94%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.89x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 308 ms                                                                | 298 ms: 1.03x faster                                     |
| chameleon      | 8.81 ms                                                               | 9.06 ms: 1.03x slower                                    |
| docutils       | 2.98 sec                                                              | 3.06 sec: 1.03x slower                                   |
| tornado_http   | 136 ms                                                                | 126 ms: 1.08x faster                                     |
| Geometric mean | (ref)                                                                 | 1.01x faster                                             |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_none            | 624 ms                                                                | 486 ms: 1.28x faster                                     |
| async_tree_memoization_tg  | 740 ms                                                                | 590 ms: 1.25x faster                                     |
| async_tree_none_tg         | 577 ms                                                                | 462 ms: 1.25x faster                                     |
| async_tree_memoization     | 777 ms                                                                | 642 ms: 1.21x faster                                     |
| async_tree_io_tg           | 1.40 sec                                                              | 1.19 sec: 1.18x faster                                   |
| async_tree_cpu_io_mixed    | 912 ms                                                                | 783 ms: 1.17x faster                                     |
| async_tree_io              | 1.41 sec                                                              | 1.22 sec: 1.16x faster                                   |
| async_tree_cpu_io_mixed_tg | 884 ms                                                                | 769 ms: 1.15x faster                                     |
| Geometric mean             | (ref)                                                                 | 1.21x faster                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| float          | 92.1 ms                                                               | 88.7 ms: 1.04x faster                                    |
| pidigits       | 233 ms                                                                | 233 ms: 1.00x slower                                     |
| nbody          | 105 ms                                                                | 106 ms: 1.01x slower                                     |
| Geometric mean | (ref)                                                                 | 1.01x faster                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| regex_compile  | 137 ms                                                                | 127 ms: 1.08x faster                                     |
| regex_dna      | 254 ms                                                                | 248 ms: 1.02x faster                                     |
| regex_effbot   | 4.64 ms                                                               | 4.86 ms: 1.05x slower                                    |
| regex_v8       | 28.3 ms                                                               | 31.2 ms: 1.10x slower                                    |
| Geometric mean | (ref)                                                                 | 1.01x slower                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|----------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| xml_etree_parse      | 195 ms                                                                | 186 ms: 1.05x faster                                     |
| unpickle_pure_python | 260 us                                                                | 248 us: 1.05x faster                                     |
| pickle_pure_python   | 365 us                                                                | 350 us: 1.04x faster                                     |
| tomli_loads          | 2.59 sec                                                              | 2.49 sec: 1.04x faster                                   |
| xml_etree_iterparse  | 150 ms                                                                | 146 ms: 1.03x faster                                     |
| xml_etree_generate   | 112 ms                                                                | 111 ms: 1.01x faster                                     |
| pickle               | 13.4 us                                                               | 13.3 us: 1.01x faster                                    |
| xml_etree_process    | 79.0 ms                                                               | 79.4 ms: 1.01x slower                                    |
| pickle_list          | 5.25 us                                                               | 5.29 us: 1.01x slower                                    |
| unpickle_list        | 6.17 us                                                               | 6.25 us: 1.01x slower                                    |
| pickle_dict          | 37.3 us                                                               | 37.9 us: 1.01x slower                                    |
| json_loads           | 30.7 us                                                               | 31.9 us: 1.04x slower                                    |
| json_dumps           | 12.3 ms                                                               | 12.8 ms: 1.05x slower                                    |
| unpickle             | 18.5 us                                                               | 19.6 us: 1.06x slower                                    |
| Geometric mean       | (ref)                                                                 | 1.00x faster                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup_no_site | 8.37 ms                                                               | 8.29 ms: 1.01x faster                                    |
| python_startup         | 11.4 ms                                                               | 12.1 ms: 1.06x slower                                    |
| Geometric mean         | (ref)                                                                 | 1.03x slower                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| genshi_xml      | 60.6 ms                                                               | 59.8 ms: 1.01x faster                                    |
| genshi_text     | 27.4 ms                                                               | 27.3 ms: 1.00x faster                                    |
| django_template | 40.7 ms                                                               | 40.5 ms: 1.00x faster                                    |
| mako            | 12.9 ms                                                               | 13.1 ms: 1.02x slower                                    |
| Geometric mean  | (ref)                                                                 | 1.00x faster                                             |

All benchmarks:
===============

| Benchmark                  | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240502-arminc-aarch64-python-main-3.13.0a6+-2770d5c |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_none            | 624 ms                                                                | 486 ms: 1.28x faster                                     |
| comprehensions             | 25.4 us                                                               | 19.9 us: 1.27x faster                                    |
| async_tree_memoization_tg  | 740 ms                                                                | 590 ms: 1.25x faster                                     |
| async_tree_none_tg         | 577 ms                                                                | 462 ms: 1.25x faster                                     |
| raytrace                   | 353 ms                                                                | 291 ms: 1.22x faster                                     |
| async_tree_memoization     | 777 ms                                                                | 642 ms: 1.21x faster                                     |
| async_tree_io_tg           | 1.40 sec                                                              | 1.19 sec: 1.18x faster                                   |
| generators                 | 43.5 ms                                                               | 37.2 ms: 1.17x faster                                    |
| async_tree_cpu_io_mixed    | 912 ms                                                                | 783 ms: 1.17x faster                                     |
| async_tree_io              | 1.41 sec                                                              | 1.22 sec: 1.16x faster                                   |
| async_tree_cpu_io_mixed_tg | 884 ms                                                                | 769 ms: 1.15x faster                                     |
| logging_format             | 8.34 us                                                               | 7.56 us: 1.10x faster                                    |
| logging_simple             | 7.63 us                                                               | 6.97 us: 1.10x faster                                    |
| dulwich_log                | 62.0 ms                                                               | 56.7 ms: 1.09x faster                                    |
| sqlglot_transpile          | 1.83 ms                                                               | 1.68 ms: 1.09x faster                                    |
| regex_compile              | 137 ms                                                                | 127 ms: 1.08x faster                                     |
| deltablue                  | 4.12 ms                                                               | 3.80 ms: 1.08x faster                                    |
| scimark_lu                 | 146 ms                                                                | 134 ms: 1.08x faster                                     |
| tornado_http               | 136 ms                                                                | 126 ms: 1.08x faster                                     |
| pathlib                    | 24.5 ms                                                               | 22.8 ms: 1.08x faster                                    |
| sympy_sum                  | 154 ms                                                                | 144 ms: 1.07x faster                                     |
| chaos                      | 71.4 ms                                                               | 66.5 ms: 1.07x faster                                    |
| sqlglot_parse              | 1.46 ms                                                               | 1.37 ms: 1.07x faster                                    |
| asyncio_tcp                | 566 ms                                                                | 530 ms: 1.07x faster                                     |
| sympy_str                  | 280 ms                                                                | 264 ms: 1.06x faster                                     |
| scimark_monte_carlo        | 85.1 ms                                                               | 80.6 ms: 1.06x faster                                    |
| crypto_pyaes               | 86.6 ms                                                               | 82.2 ms: 1.05x faster                                    |
| xml_etree_parse            | 195 ms                                                                | 186 ms: 1.05x faster                                     |
| unpickle_pure_python       | 260 us                                                                | 248 us: 1.05x faster                                     |
| pickle_pure_python         | 365 us                                                                | 350 us: 1.04x faster                                     |
| sympy_integrate            | 21.6 ms                                                               | 20.8 ms: 1.04x faster                                    |
| bench_thread_pool          | 1.31 ms                                                               | 1.26 ms: 1.04x faster                                    |
| tomli_loads                | 2.59 sec                                                              | 2.49 sec: 1.04x faster                                   |
| pycparser                  | 1.26 sec                                                              | 1.21 sec: 1.04x faster                                   |
| mdp                        | 3.41 sec                                                              | 3.29 sec: 1.04x faster                                   |
| float                      | 92.1 ms                                                               | 88.7 ms: 1.04x faster                                    |
| nqueens                    | 99.2 ms                                                               | 95.7 ms: 1.04x faster                                    |
| 2to3                       | 308 ms                                                                | 298 ms: 1.03x faster                                     |
| async_generators           | 491 ms                                                                | 476 ms: 1.03x faster                                     |
| xml_etree_iterparse        | 150 ms                                                                | 146 ms: 1.03x faster                                     |
| asyncio_tcp_ssl            | 2.19 sec                                                              | 2.12 sec: 1.03x faster                                   |
| deepcopy_reduce            | 4.10 us                                                               | 4.00 us: 1.02x faster                                    |
| regex_dna                  | 254 ms                                                                | 248 ms: 1.02x faster                                     |
| deepcopy_memo              | 49.6 us                                                               | 48.6 us: 1.02x faster                                    |
| bench_mp_pool              | 7.05 ms                                                               | 6.95 ms: 1.01x faster                                    |
| genshi_xml                 | 60.6 ms                                                               | 59.8 ms: 1.01x faster                                    |
| xml_etree_generate         | 112 ms                                                                | 111 ms: 1.01x faster                                     |
| coroutines                 | 29.0 ms                                                               | 28.7 ms: 1.01x faster                                    |
| python_startup_no_site     | 8.37 ms                                                               | 8.29 ms: 1.01x faster                                    |
| deepcopy                   | 446 us                                                                | 442 us: 1.01x faster                                     |
| pyflate                    | 559 ms                                                                | 555 ms: 1.01x faster                                     |
| sqlglot_normalize          | 126 ms                                                                | 125 ms: 1.01x faster                                     |
| pickle                     | 13.4 us                                                               | 13.3 us: 1.01x faster                                    |
| sqlglot_optimize           | 61.3 ms                                                               | 61.0 ms: 1.01x faster                                    |
| sympy_expand               | 454 ms                                                                | 451 ms: 1.01x faster                                     |
| genshi_text                | 27.4 ms                                                               | 27.3 ms: 1.00x faster                                    |
| django_template            | 40.7 ms                                                               | 40.5 ms: 1.00x faster                                    |
| pidigits                   | 233 ms                                                                | 233 ms: 1.00x slower                                     |
| pprint_pformat             | 1.88 sec                                                              | 1.89 sec: 1.00x slower                                   |
| xml_etree_process          | 79.0 ms                                                               | 79.4 ms: 1.01x slower                                    |
| hexiom                     | 6.98 ms                                                               | 7.01 ms: 1.01x slower                                    |
| pickle_list                | 5.25 us                                                               | 5.29 us: 1.01x slower                                    |
| pprint_safe_repr           | 916 ms                                                                | 923 ms: 1.01x slower                                     |
| json                       | 5.54 ms                                                               | 5.59 ms: 1.01x slower                                    |
| go                         | 157 ms                                                                | 159 ms: 1.01x slower                                     |
| nbody                      | 105 ms                                                                | 106 ms: 1.01x slower                                     |
| meteor_contest             | 112 ms                                                                | 113 ms: 1.01x slower                                     |
| unpickle_list              | 6.17 us                                                               | 6.25 us: 1.01x slower                                    |
| pickle_dict                | 37.3 us                                                               | 37.9 us: 1.01x slower                                    |
| richards_super             | 58.5 ms                                                               | 59.4 ms: 1.02x slower                                    |
| mako                       | 12.9 ms                                                               | 13.1 ms: 1.02x slower                                    |
| fannkuch                   | 443 ms                                                                | 453 ms: 1.02x slower                                     |
| docutils                   | 2.98 sec                                                              | 3.06 sec: 1.03x slower                                   |
| chameleon                  | 8.81 ms                                                               | 9.06 ms: 1.03x slower                                    |
| scimark_sor                | 150 ms                                                                | 155 ms: 1.03x slower                                     |
| logging_silent             | 127 ns                                                                | 131 ns: 1.04x slower                                     |
| richards                   | 50.9 ms                                                               | 52.8 ms: 1.04x slower                                    |
| json_loads                 | 30.7 us                                                               | 31.9 us: 1.04x slower                                    |
| scimark_sparse_mat_mult    | 6.19 ms                                                               | 6.47 ms: 1.04x slower                                    |
| json_dumps                 | 12.3 ms                                                               | 12.8 ms: 1.05x slower                                    |
| regex_effbot               | 4.64 ms                                                               | 4.86 ms: 1.05x slower                                    |
| scimark_fft                | 418 ms                                                                | 438 ms: 1.05x slower                                     |
| typing_runtime_protocols   | 181 us                                                                | 191 us: 1.06x slower                                     |
| spectral_norm              | 131 ms                                                                | 139 ms: 1.06x slower                                     |
| unpickle                   | 18.5 us                                                               | 19.6 us: 1.06x slower                                    |
| python_startup             | 11.4 ms                                                               | 12.1 ms: 1.06x slower                                    |
| regex_v8                   | 28.3 ms                                                               | 31.2 ms: 1.10x slower                                    |
| telco                      | 8.51 ms                                                               | 9.38 ms: 1.10x slower                                    |
| coverage                   | 87.3 ms                                                               | 98.4 ms: 1.13x slower                                    |
| gc_traversal               | 4.40 ms                                                               | 5.10 ms: 1.16x slower                                    |
| create_gc_cycles           | 1.92 ms                                                               | 2.31 ms: 1.20x slower                                    |
| Geometric mean             | (ref)                                                                 | 1.03x faster                                             |

Benchmark hidden because not significant (6): pylint, dask, asyncio_websockets, thrift, sqlite_synth, html5lib
Ignored benchmarks (5) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0.json: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.94% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.89x