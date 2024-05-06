# Results vs. 3.12.0

- fork: python
- ref: main
- machine: linux-aarch64
- commit hash: a7711a2
- commit date: 2024-05-01
- overall geometric mean: 1.05x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| 2to3           | 308 ms                                                                | 348 ms: 1.13x slower                                     |
| chameleon      | 8.81 ms                                                               | 9.13 ms: 1.04x slower                                    |
| docutils       | 2.98 sec                                                              | 3.41 sec: 1.14x slower                                   |
| html5lib       | 65.1 ms                                                               | 70.3 ms: 1.08x slower                                    |
| tornado_http   | 136 ms                                                                | 139 ms: 1.02x slower                                     |
| Geometric mean | (ref)                                                                 | 1.08x slower                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_none            | 624 ms                                                                | 511 ms: 1.22x faster                                     |
| async_tree_none_tg         | 577 ms                                                                | 474 ms: 1.22x faster                                     |
| async_tree_memoization_tg  | 740 ms                                                                | 616 ms: 1.20x faster                                     |
| async_tree_memoization     | 777 ms                                                                | 661 ms: 1.18x faster                                     |
| async_tree_io_tg           | 1.40 sec                                                              | 1.20 sec: 1.17x faster                                   |
| async_tree_io              | 1.41 sec                                                              | 1.23 sec: 1.15x faster                                   |
| async_tree_cpu_io_mixed_tg | 884 ms                                                                | 775 ms: 1.14x faster                                     |
| async_tree_cpu_io_mixed    | 912 ms                                                                | 809 ms: 1.13x faster                                     |
| Geometric mean             | (ref)                                                                 | 1.18x faster                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| float          | 92.1 ms                                                               | 90.3 ms: 1.02x faster                                    |
| pidigits       | 233 ms                                                                | 233 ms: 1.00x slower                                     |
| nbody          | 105 ms                                                                | 108 ms: 1.03x slower                                     |
| Geometric mean | (ref)                                                                 | 1.00x slower                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| regex_dna      | 254 ms                                                                | 246 ms: 1.03x faster                                     |
| regex_effbot   | 4.64 ms                                                               | 4.84 ms: 1.04x slower                                    |
| regex_v8       | 28.3 ms                                                               | 30.3 ms: 1.07x slower                                    |
| regex_compile  | 137 ms                                                                | 159 ms: 1.16x slower                                     |
| Geometric mean | (ref)                                                                 | 1.06x slower                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|----------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| xml_etree_parse      | 195 ms                                                                | 186 ms: 1.05x faster                                     |
| pickle_pure_python   | 365 us                                                                | 356 us: 1.03x faster                                     |
| xml_etree_iterparse  | 150 ms                                                                | 148 ms: 1.02x faster                                     |
| tomli_loads          | 2.59 sec                                                              | 2.56 sec: 1.01x faster                                   |
| pickle               | 13.4 us                                                               | 13.5 us: 1.01x slower                                    |
| pickle_dict          | 37.3 us                                                               | 37.7 us: 1.01x slower                                    |
| xml_etree_generate   | 112 ms                                                                | 114 ms: 1.01x slower                                     |
| xml_etree_process    | 79.0 ms                                                               | 80.3 ms: 1.02x slower                                    |
| json_loads           | 30.7 us                                                               | 31.8 us: 1.04x slower                                    |
| unpickle_list        | 6.17 us                                                               | 6.48 us: 1.05x slower                                    |
| json_dumps           | 12.3 ms                                                               | 12.9 ms: 1.05x slower                                    |
| unpickle_pure_python | 260 us                                                                | 277 us: 1.07x slower                                     |
| unpickle             | 18.5 us                                                               | 19.8 us: 1.07x slower                                    |
| Geometric mean       | (ref)                                                                 | 1.02x slower                                             |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| python_startup_no_site | 8.37 ms                                                               | 10.7 ms: 1.27x slower                                    |
| python_startup         | 11.4 ms                                                               | 14.7 ms: 1.29x slower                                    |
| Geometric mean         | (ref)                                                                 | 1.28x slower                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|-----------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| mako            | 12.9 ms                                                               | 13.0 ms: 1.00x slower                                    |
| django_template | 40.7 ms                                                               | 48.5 ms: 1.19x slower                                    |
| genshi_text     | 27.4 ms                                                               | 33.6 ms: 1.23x slower                                    |
| genshi_xml      | 60.6 ms                                                               | 78.3 ms: 1.29x slower                                    |
| Geometric mean  | (ref)                                                                 | 1.17x slower                                             |

All benchmarks:
===============

| Benchmark                  | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240501-arminc-aarch64-python-main-3.13.0a6+-a7711a2 |
|----------------------------|:---------------------------------------------------------------------:|:--------------------------------------------------------:|
| async_tree_none            | 624 ms                                                                | 511 ms: 1.22x faster                                     |
| async_tree_none_tg         | 577 ms                                                                | 474 ms: 1.22x faster                                     |
| async_tree_memoization_tg  | 740 ms                                                                | 616 ms: 1.20x faster                                     |
| async_tree_memoization     | 777 ms                                                                | 661 ms: 1.18x faster                                     |
| async_tree_io_tg           | 1.40 sec                                                              | 1.20 sec: 1.17x faster                                   |
| async_tree_io              | 1.41 sec                                                              | 1.23 sec: 1.15x faster                                   |
| generators                 | 43.5 ms                                                               | 38.1 ms: 1.14x faster                                    |
| async_tree_cpu_io_mixed_tg | 884 ms                                                                | 775 ms: 1.14x faster                                     |
| async_tree_cpu_io_mixed    | 912 ms                                                                | 809 ms: 1.13x faster                                     |
| raytrace                   | 353 ms                                                                | 316 ms: 1.12x faster                                     |
| comprehensions             | 25.4 us                                                               | 23.4 us: 1.09x faster                                    |
| pathlib                    | 24.5 ms                                                               | 23.3 ms: 1.06x faster                                    |
| xml_etree_parse            | 195 ms                                                                | 186 ms: 1.05x faster                                     |
| regex_dna                  | 254 ms                                                                | 246 ms: 1.03x faster                                     |
| pickle_pure_python         | 365 us                                                                | 356 us: 1.03x faster                                     |
| float                      | 92.1 ms                                                               | 90.3 ms: 1.02x faster                                    |
| xml_etree_iterparse        | 150 ms                                                                | 148 ms: 1.02x faster                                     |
| tomli_loads                | 2.59 sec                                                              | 2.56 sec: 1.01x faster                                   |
| logging_format             | 8.34 us                                                               | 8.27 us: 1.01x faster                                    |
| pidigits                   | 233 ms                                                                | 233 ms: 1.00x slower                                     |
| mako                       | 12.9 ms                                                               | 13.0 ms: 1.00x slower                                    |
| crypto_pyaes               | 86.6 ms                                                               | 87.2 ms: 1.01x slower                                    |
| pickle                     | 13.4 us                                                               | 13.5 us: 1.01x slower                                    |
| mdp                        | 3.41 sec                                                              | 3.44 sec: 1.01x slower                                   |
| json                       | 5.54 ms                                                               | 5.59 ms: 1.01x slower                                    |
| pickle_dict                | 37.3 us                                                               | 37.7 us: 1.01x slower                                    |
| xml_etree_generate         | 112 ms                                                                | 114 ms: 1.01x slower                                     |
| deepcopy_memo              | 49.6 us                                                               | 50.3 us: 1.01x slower                                    |
| richards_super             | 58.5 ms                                                               | 59.4 ms: 1.02x slower                                    |
| xml_etree_process          | 79.0 ms                                                               | 80.3 ms: 1.02x slower                                    |
| async_generators           | 491 ms                                                                | 501 ms: 1.02x slower                                     |
| pycparser                  | 1.26 sec                                                              | 1.28 sec: 1.02x slower                                   |
| sqlite_synth               | 3.77 us                                                               | 3.85 us: 1.02x slower                                    |
| tornado_http               | 136 ms                                                                | 139 ms: 1.02x slower                                     |
| richards                   | 50.9 ms                                                               | 52.3 ms: 1.03x slower                                    |
| nbody                      | 105 ms                                                                | 108 ms: 1.03x slower                                     |
| sqlglot_transpile          | 1.83 ms                                                               | 1.89 ms: 1.03x slower                                    |
| deepcopy                   | 446 us                                                                | 460 us: 1.03x slower                                     |
| coroutines                 | 29.0 ms                                                               | 30.0 ms: 1.03x slower                                    |
| asyncio_tcp_ssl            | 2.19 sec                                                              | 2.26 sec: 1.04x slower                                   |
| sqlglot_parse              | 1.46 ms                                                               | 1.52 ms: 1.04x slower                                    |
| chameleon                  | 8.81 ms                                                               | 9.13 ms: 1.04x slower                                    |
| fannkuch                   | 443 ms                                                                | 460 ms: 1.04x slower                                     |
| thrift                     | 937 us                                                                | 971 us: 1.04x slower                                     |
| json_loads                 | 30.7 us                                                               | 31.8 us: 1.04x slower                                    |
| regex_effbot               | 4.64 ms                                                               | 4.84 ms: 1.04x slower                                    |
| unpickle_list              | 6.17 us                                                               | 6.48 us: 1.05x slower                                    |
| json_dumps                 | 12.3 ms                                                               | 12.9 ms: 1.05x slower                                    |
| logging_silent             | 127 ns                                                                | 134 ns: 1.05x slower                                     |
| dask                       | 376 ms                                                                | 397 ms: 1.05x slower                                     |
| bench_mp_pool              | 7.05 ms                                                               | 7.46 ms: 1.06x slower                                    |
| unpickle_pure_python       | 260 us                                                                | 277 us: 1.07x slower                                     |
| regex_v8                   | 28.3 ms                                                               | 30.3 ms: 1.07x slower                                    |
| pyflate                    | 559 ms                                                                | 598 ms: 1.07x slower                                     |
| meteor_contest             | 112 ms                                                                | 120 ms: 1.07x slower                                     |
| unpickle                   | 18.5 us                                                               | 19.8 us: 1.07x slower                                    |
| html5lib                   | 65.1 ms                                                               | 70.3 ms: 1.08x slower                                    |
| asyncio_tcp                | 566 ms                                                                | 614 ms: 1.08x slower                                     |
| scimark_fft                | 418 ms                                                                | 454 ms: 1.09x slower                                     |
| spectral_norm              | 131 ms                                                                | 142 ms: 1.09x slower                                     |
| sqlglot_normalize          | 126 ms                                                                | 137 ms: 1.09x slower                                     |
| sympy_str                  | 280 ms                                                                | 306 ms: 1.09x slower                                     |
| sqlglot_optimize           | 61.3 ms                                                               | 68.1 ms: 1.11x slower                                    |
| deltablue                  | 4.12 ms                                                               | 4.58 ms: 1.11x slower                                    |
| 2to3                       | 308 ms                                                                | 348 ms: 1.13x slower                                     |
| sympy_sum                  | 154 ms                                                                | 175 ms: 1.13x slower                                     |
| scimark_sparse_mat_mult    | 6.19 ms                                                               | 7.02 ms: 1.13x slower                                    |
| coverage                   | 87.3 ms                                                               | 99.2 ms: 1.14x slower                                    |
| dulwich_log                | 62.0 ms                                                               | 70.7 ms: 1.14x slower                                    |
| docutils                   | 2.98 sec                                                              | 3.41 sec: 1.14x slower                                   |
| sympy_expand               | 454 ms                                                                | 519 ms: 1.14x slower                                     |
| pylint                     | 355 ms                                                                | 406 ms: 1.15x slower                                     |
| gc_traversal               | 4.40 ms                                                               | 5.05 ms: 1.15x slower                                    |
| chaos                      | 71.4 ms                                                               | 82.8 ms: 1.16x slower                                    |
| regex_compile              | 137 ms                                                                | 159 ms: 1.16x slower                                     |
| telco                      | 8.51 ms                                                               | 9.88 ms: 1.16x slower                                    |
| sympy_integrate            | 21.6 ms                                                               | 25.5 ms: 1.18x slower                                    |
| go                         | 157 ms                                                                | 186 ms: 1.19x slower                                     |
| typing_runtime_protocols   | 181 us                                                                | 215 us: 1.19x slower                                     |
| django_template            | 40.7 ms                                                               | 48.5 ms: 1.19x slower                                    |
| create_gc_cycles           | 1.92 ms                                                               | 2.32 ms: 1.21x slower                                    |
| scimark_sor                | 150 ms                                                                | 181 ms: 1.21x slower                                     |
| nqueens                    | 99.2 ms                                                               | 120 ms: 1.21x slower                                     |
| scimark_lu                 | 146 ms                                                                | 178 ms: 1.22x slower                                     |
| genshi_text                | 27.4 ms                                                               | 33.6 ms: 1.23x slower                                    |
| python_startup_no_site     | 8.37 ms                                                               | 10.7 ms: 1.27x slower                                    |
| pprint_safe_repr           | 916 ms                                                                | 1.17 sec: 1.28x slower                                   |
| hexiom                     | 6.98 ms                                                               | 8.94 ms: 1.28x slower                                    |
| pprint_pformat             | 1.88 sec                                                              | 2.42 sec: 1.29x slower                                   |
| python_startup             | 11.4 ms                                                               | 14.7 ms: 1.29x slower                                    |
| genshi_xml                 | 60.6 ms                                                               | 78.3 ms: 1.29x slower                                    |
| Geometric mean             | (ref)                                                                 | 1.05x slower                                             |

Benchmark hidden because not significant (6): scimark_monte_carlo, deepcopy_reduce, logging_simple, asyncio_websockets, pickle_list, bench_thread_pool
Ignored benchmarks (5) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0.json: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 0.99x