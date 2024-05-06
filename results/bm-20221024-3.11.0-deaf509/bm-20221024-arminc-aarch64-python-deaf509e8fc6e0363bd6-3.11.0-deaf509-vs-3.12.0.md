# Results vs. 3.12.0

- fork: python
- ref: deaf509e8fc6e0363bd6
- machine: linux-aarch64
- commit hash: deaf509
- commit date: 2022-10-24
- overall geometric mean: 1.04x slower
- HPT reliability: 98.99%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.90x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 308 ms                                                                | 300 ms: 1.03x faster                                                  |
| chameleon      | 8.81 ms                                                               | 8.29 ms: 1.06x faster                                                 |
| docutils       | 2.98 sec                                                              | 2.92 sec: 1.02x faster                                                |
| tornado_http   | 136 ms                                                                | 140 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.02x faster                                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 884 ms                                                                | 922 ms: 1.04x slower                                                  |
| async_tree_cpu_io_mixed    | 912 ms                                                                | 955 ms: 1.05x slower                                                  |
| async_tree_none_tg         | 577 ms                                                                | 620 ms: 1.08x slower                                                  |
| async_tree_io_tg           | 1.40 sec                                                              | 1.54 sec: 1.09x slower                                                |
| async_tree_memoization_tg  | 740 ms                                                                | 828 ms: 1.12x slower                                                  |
| async_tree_memoization     | 777 ms                                                                | 872 ms: 1.12x slower                                                  |
| async_tree_none            | 624 ms                                                                | 701 ms: 1.12x slower                                                  |
| async_tree_io              | 1.41 sec                                                              | 1.61 sec: 1.14x slower                                                |
| Geometric mean             | (ref)                                                                 | 1.09x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 92.1 ms                                                               | 89.6 ms: 1.03x faster                                                 |
| pidigits       | 233 ms                                                                | 242 ms: 1.04x slower                                                  |
| nbody          | 105 ms                                                                | 113 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.03x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.64 ms                                                               | 4.25 ms: 1.09x faster                                                 |
| regex_dna      | 254 ms                                                                | 239 ms: 1.06x faster                                                  |
| regex_compile  | 137 ms                                                                | 137 ms: 1.00x faster                                                  |
| regex_v8       | 28.3 ms                                                               | 29.1 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| unpickle             | 18.5 us                                                               | 16.9 us: 1.10x faster                                                 |
| xml_etree_generate   | 112 ms                                                                | 104 ms: 1.08x faster                                                  |
| pickle               | 13.4 us                                                               | 12.8 us: 1.05x faster                                                 |
| pickle_list          | 5.25 us                                                               | 5.01 us: 1.05x faster                                                 |
| xml_etree_process    | 79.0 ms                                                               | 76.1 ms: 1.04x faster                                                 |
| json_loads           | 30.7 us                                                               | 30.3 us: 1.01x faster                                                 |
| pickle_dict          | 37.3 us                                                               | 37.6 us: 1.01x slower                                                 |
| xml_etree_iterparse  | 150 ms                                                                | 152 ms: 1.01x slower                                                  |
| tomli_loads          | 2.59 sec                                                              | 2.62 sec: 1.01x slower                                                |
| pickle_pure_python   | 365 us                                                                | 374 us: 1.02x slower                                                  |
| unpickle_pure_python | 260 us                                                                | 278 us: 1.07x slower                                                  |
| xml_etree_parse      | 195 ms                                                                | 209 ms: 1.07x slower                                                  |
| unpickle_list        | 6.17 us                                                               | 6.86 us: 1.11x slower                                                 |
| json_dumps           | 12.3 ms                                                               | 15.4 ms: 1.26x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.02x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 8.37 ms                                                               | 7.35 ms: 1.14x faster                                                 |
| python_startup         | 11.4 ms                                                               | 10.2 ms: 1.12x faster                                                 |
| Geometric mean         | (ref)                                                                 | 1.13x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 27.4 ms                                                               | 28.2 ms: 1.03x slower                                                 |
| genshi_xml      | 60.6 ms                                                               | 62.2 ms: 1.03x slower                                                 |
| django_template | 40.7 ms                                                               | 41.8 ms: 1.03x slower                                                 |
| mako            | 12.9 ms                                                               | 13.3 ms: 1.03x slower                                                 |
| Geometric mean  | (ref)                                                                 | 1.03x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_generators           | 491 ms                                                                | 378 ms: 1.30x faster                                                  |
| mypy2                      | 873 ms                                                                | 737 ms: 1.19x faster                                                  |
| python_startup_no_site     | 8.37 ms                                                               | 7.35 ms: 1.14x faster                                                 |
| python_startup             | 11.4 ms                                                               | 10.2 ms: 1.12x faster                                                 |
| unpickle                   | 18.5 us                                                               | 16.9 us: 1.10x faster                                                 |
| regex_effbot               | 4.64 ms                                                               | 4.25 ms: 1.09x faster                                                 |
| telco                      | 8.51 ms                                                               | 7.80 ms: 1.09x faster                                                 |
| pyflate                    | 559 ms                                                                | 516 ms: 1.08x faster                                                  |
| xml_etree_generate         | 112 ms                                                                | 104 ms: 1.08x faster                                                  |
| chameleon                  | 8.81 ms                                                               | 8.29 ms: 1.06x faster                                                 |
| regex_dna                  | 254 ms                                                                | 239 ms: 1.06x faster                                                  |
| sqlite_synth               | 3.77 us                                                               | 3.56 us: 1.06x faster                                                 |
| deepcopy_reduce            | 4.10 us                                                               | 3.89 us: 1.05x faster                                                 |
| pickle                     | 13.4 us                                                               | 12.8 us: 1.05x faster                                                 |
| pickle_list                | 5.25 us                                                               | 5.01 us: 1.05x faster                                                 |
| scimark_fft                | 418 ms                                                                | 402 ms: 1.04x faster                                                  |
| scimark_lu                 | 146 ms                                                                | 140 ms: 1.04x faster                                                  |
| coverage                   | 87.3 ms                                                               | 84.1 ms: 1.04x faster                                                 |
| xml_etree_process          | 79.0 ms                                                               | 76.1 ms: 1.04x faster                                                 |
| thrift                     | 937 us                                                                | 910 us: 1.03x faster                                                  |
| scimark_sor                | 150 ms                                                                | 145 ms: 1.03x faster                                                  |
| float                      | 92.1 ms                                                               | 89.6 ms: 1.03x faster                                                 |
| 2to3                       | 308 ms                                                                | 300 ms: 1.03x faster                                                  |
| create_gc_cycles           | 1.92 ms                                                               | 1.87 ms: 1.02x faster                                                 |
| deepcopy                   | 446 us                                                                | 435 us: 1.02x faster                                                  |
| aiohttp                    | 1.16 ms                                                               | 1.13 ms: 1.02x faster                                                 |
| scimark_monte_carlo        | 85.1 ms                                                               | 83.2 ms: 1.02x faster                                                 |
| docutils                   | 2.98 sec                                                              | 2.92 sec: 1.02x faster                                                |
| sqlalchemy_imperative      | 16.7 ms                                                               | 16.4 ms: 1.02x faster                                                 |
| mdp                        | 3.41 sec                                                              | 3.35 sec: 1.02x faster                                                |
| gc_traversal               | 4.40 ms                                                               | 4.33 ms: 1.02x faster                                                 |
| logging_format             | 8.34 us                                                               | 8.22 us: 1.02x faster                                                 |
| pprint_safe_repr           | 916 ms                                                                | 903 ms: 1.01x faster                                                  |
| pprint_pformat             | 1.88 sec                                                              | 1.85 sec: 1.01x faster                                                |
| json_loads                 | 30.7 us                                                               | 30.3 us: 1.01x faster                                                 |
| deepcopy_memo              | 49.6 us                                                               | 49.0 us: 1.01x faster                                                 |
| logging_simple             | 7.63 us                                                               | 7.57 us: 1.01x faster                                                 |
| raytrace                   | 353 ms                                                                | 351 ms: 1.01x faster                                                  |
| regex_compile              | 137 ms                                                                | 137 ms: 1.00x faster                                                  |
| json                       | 5.54 ms                                                               | 5.52 ms: 1.00x faster                                                 |
| asyncio_websockets         | 658 ms                                                                | 656 ms: 1.00x faster                                                  |
| spectral_norm              | 131 ms                                                                | 131 ms: 1.00x slower                                                  |
| pickle_dict                | 37.3 us                                                               | 37.6 us: 1.01x slower                                                 |
| xml_etree_iterparse        | 150 ms                                                                | 152 ms: 1.01x slower                                                  |
| tomli_loads                | 2.59 sec                                                              | 2.62 sec: 1.01x slower                                                |
| pathlib                    | 24.5 ms                                                               | 24.8 ms: 1.01x slower                                                 |
| scimark_sparse_mat_mult    | 6.19 ms                                                               | 6.29 ms: 1.01x slower                                                 |
| fannkuch                   | 443 ms                                                                | 451 ms: 1.02x slower                                                  |
| dulwich_log                | 62.0 ms                                                               | 63.2 ms: 1.02x slower                                                 |
| dask                       | 376 ms                                                                | 385 ms: 1.02x slower                                                  |
| pickle_pure_python         | 365 us                                                                | 374 us: 1.02x slower                                                  |
| regex_v8                   | 28.3 ms                                                               | 29.1 ms: 1.03x slower                                                 |
| genshi_text                | 27.4 ms                                                               | 28.2 ms: 1.03x slower                                                 |
| genshi_xml                 | 60.6 ms                                                               | 62.2 ms: 1.03x slower                                                 |
| django_template            | 40.7 ms                                                               | 41.8 ms: 1.03x slower                                                 |
| mako                       | 12.9 ms                                                               | 13.3 ms: 1.03x slower                                                 |
| tornado_http               | 136 ms                                                                | 140 ms: 1.03x slower                                                  |
| meteor_contest             | 112 ms                                                                | 115 ms: 1.03x slower                                                  |
| nqueens                    | 99.2 ms                                                               | 102 ms: 1.03x slower                                                  |
| sqlglot_optimize           | 61.3 ms                                                               | 63.4 ms: 1.03x slower                                                 |
| bench_thread_pool          | 1.31 ms                                                               | 1.36 ms: 1.04x slower                                                 |
| go                         | 157 ms                                                                | 163 ms: 1.04x slower                                                  |
| pidigits                   | 233 ms                                                                | 242 ms: 1.04x slower                                                  |
| async_tree_cpu_io_mixed_tg | 884 ms                                                                | 922 ms: 1.04x slower                                                  |
| logging_silent             | 127 ns                                                                | 133 ns: 1.04x slower                                                  |
| gunicorn                   | 1.14 ms                                                               | 1.19 ms: 1.05x slower                                                 |
| async_tree_cpu_io_mixed    | 912 ms                                                                | 955 ms: 1.05x slower                                                  |
| sqlglot_normalize          | 126 ms                                                                | 132 ms: 1.05x slower                                                  |
| sympy_str                  | 280 ms                                                                | 295 ms: 1.05x slower                                                  |
| bench_mp_pool              | 7.05 ms                                                               | 7.44 ms: 1.05x slower                                                 |
| sympy_expand               | 454 ms                                                                | 482 ms: 1.06x slower                                                  |
| unpickle_pure_python       | 260 us                                                                | 278 us: 1.07x slower                                                  |
| sympy_integrate            | 21.6 ms                                                               | 23.2 ms: 1.07x slower                                                 |
| xml_etree_parse            | 195 ms                                                                | 209 ms: 1.07x slower                                                  |
| async_tree_none_tg         | 577 ms                                                                | 620 ms: 1.08x slower                                                  |
| nbody                      | 105 ms                                                                | 113 ms: 1.08x slower                                                  |
| hexiom                     | 6.98 ms                                                               | 7.57 ms: 1.09x slower                                                 |
| sympy_sum                  | 154 ms                                                                | 168 ms: 1.09x slower                                                  |
| sqlglot_transpile          | 1.83 ms                                                               | 2.00 ms: 1.09x slower                                                 |
| async_tree_io_tg           | 1.40 sec                                                              | 1.54 sec: 1.09x slower                                                |
| chaos                      | 71.4 ms                                                               | 78.8 ms: 1.10x slower                                                 |
| unpickle_list              | 6.17 us                                                               | 6.86 us: 1.11x slower                                                 |
| async_tree_memoization_tg  | 740 ms                                                                | 828 ms: 1.12x slower                                                  |
| pylint                     | 355 ms                                                                | 397 ms: 1.12x slower                                                  |
| async_tree_memoization     | 777 ms                                                                | 872 ms: 1.12x slower                                                  |
| async_tree_none            | 624 ms                                                                | 701 ms: 1.12x slower                                                  |
| sqlglot_parse              | 1.46 ms                                                               | 1.65 ms: 1.13x slower                                                 |
| async_tree_io              | 1.41 sec                                                              | 1.61 sec: 1.14x slower                                                |
| richards                   | 50.9 ms                                                               | 58.1 ms: 1.14x slower                                                 |
| comprehensions             | 25.4 us                                                               | 29.0 us: 1.14x slower                                                 |
| coroutines                 | 29.0 ms                                                               | 33.3 ms: 1.15x slower                                                 |
| deltablue                  | 4.12 ms                                                               | 4.75 ms: 1.15x slower                                                 |
| richards_super             | 58.5 ms                                                               | 70.2 ms: 1.20x slower                                                 |
| json_dumps                 | 12.3 ms                                                               | 15.4 ms: 1.26x slower                                                 |
| asyncio_tcp_ssl            | 2.19 sec                                                              | 3.19 sec: 1.46x slower                                                |
| generators                 | 43.5 ms                                                               | 64.2 ms: 1.48x slower                                                 |
| asyncio_tcp                | 566 ms                                                                | 920 ms: 1.63x slower                                                  |
| typing_runtime_protocols   | 181 us                                                                | 653 us: 3.62x slower                                                  |
| Geometric mean             | (ref)                                                                 | 1.04x slower                                                          |

Benchmark hidden because not significant (4): pycparser, sqlalchemy_declarative, crypto_pyaes, html5lib
Ignored benchmarks (1) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: flaskblogging

# HPT report

- Reliability score: 98.99% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.90x