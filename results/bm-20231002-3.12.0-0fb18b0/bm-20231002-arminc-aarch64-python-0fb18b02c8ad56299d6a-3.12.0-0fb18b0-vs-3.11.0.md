# Results vs. 3.11.0

- fork: python
- ref: 0fb18b02c8ad56299d6a
- machine: linux-aarch64
- commit hash: 0fb18b0
- commit date: 2023-10-02
- overall geometric mean: 1.04x faster
- HPT reliability: 98.99%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 308 ms: 1.03x slower                                                  |
| chameleon      | 8.29 ms                                                               | 8.81 ms: 1.06x slower                                                 |
| docutils       | 2.92 sec                                                              | 2.98 sec: 1.02x slower                                                |
| tornado_http   | 140 ms                                                                | 136 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io              | 1.61 sec                                                              | 1.41 sec: 1.14x faster                                                |
| async_tree_none            | 701 ms                                                                | 624 ms: 1.12x faster                                                  |
| async_tree_memoization     | 872 ms                                                                | 777 ms: 1.12x faster                                                  |
| async_tree_memoization_tg  | 828 ms                                                                | 740 ms: 1.12x faster                                                  |
| async_tree_io_tg           | 1.54 sec                                                              | 1.40 sec: 1.09x faster                                                |
| async_tree_none_tg         | 620 ms                                                                | 577 ms: 1.08x faster                                                  |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 912 ms: 1.05x faster                                                  |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 884 ms: 1.04x faster                                                  |
| Geometric mean             | (ref)                                                                 | 1.09x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 113 ms                                                                | 105 ms: 1.08x faster                                                  |
| pidigits       | 242 ms                                                                | 233 ms: 1.04x faster                                                  |
| float          | 89.6 ms                                                               | 92.1 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.03x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 29.1 ms                                                               | 28.3 ms: 1.03x faster                                                 |
| regex_compile  | 137 ms                                                                | 137 ms: 1.00x slower                                                  |
| regex_dna      | 239 ms                                                                | 254 ms: 1.06x slower                                                  |
| regex_effbot   | 4.25 ms                                                               | 4.64 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 12.3 ms: 1.26x faster                                                 |
| unpickle_list        | 6.86 us                                                               | 6.17 us: 1.11x faster                                                 |
| xml_etree_parse      | 209 ms                                                                | 195 ms: 1.07x faster                                                  |
| unpickle_pure_python | 278 us                                                                | 260 us: 1.07x faster                                                  |
| pickle_pure_python   | 374 us                                                                | 365 us: 1.02x faster                                                  |
| tomli_loads          | 2.62 sec                                                              | 2.59 sec: 1.01x faster                                                |
| xml_etree_iterparse  | 152 ms                                                                | 150 ms: 1.01x faster                                                  |
| pickle_dict          | 37.6 us                                                               | 37.3 us: 1.01x faster                                                 |
| json_loads           | 30.3 us                                                               | 30.7 us: 1.01x slower                                                 |
| xml_etree_process    | 76.1 ms                                                               | 79.0 ms: 1.04x slower                                                 |
| pickle_list          | 5.01 us                                                               | 5.25 us: 1.05x slower                                                 |
| pickle               | 12.8 us                                                               | 13.4 us: 1.05x slower                                                 |
| xml_etree_generate   | 104 ms                                                                | 112 ms: 1.08x slower                                                  |
| unpickle             | 16.9 us                                                               | 18.5 us: 1.10x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 10.2 ms                                                               | 11.4 ms: 1.12x slower                                                 |
| python_startup_no_site | 7.35 ms                                                               | 8.37 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                                 | 1.13x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 13.3 ms                                                               | 12.9 ms: 1.03x faster                                                 |
| django_template | 41.8 ms                                                               | 40.7 ms: 1.03x faster                                                 |
| genshi_xml      | 62.2 ms                                                               | 60.6 ms: 1.03x faster                                                 |
| genshi_text     | 28.2 ms                                                               | 27.4 ms: 1.03x faster                                                 |
| Geometric mean  | (ref)                                                                 | 1.03x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 181 us: 3.62x faster                                                  |
| asyncio_tcp                | 920 ms                                                                | 566 ms: 1.63x faster                                                  |
| generators                 | 64.2 ms                                                               | 43.5 ms: 1.48x faster                                                 |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.19 sec: 1.46x faster                                                |
| json_dumps                 | 15.4 ms                                                               | 12.3 ms: 1.26x faster                                                 |
| richards_super             | 70.2 ms                                                               | 58.5 ms: 1.20x faster                                                 |
| deltablue                  | 4.75 ms                                                               | 4.12 ms: 1.15x faster                                                 |
| coroutines                 | 33.3 ms                                                               | 29.0 ms: 1.15x faster                                                 |
| comprehensions             | 29.0 us                                                               | 25.4 us: 1.14x faster                                                 |
| richards                   | 58.1 ms                                                               | 50.9 ms: 1.14x faster                                                 |
| async_tree_io              | 1.61 sec                                                              | 1.41 sec: 1.14x faster                                                |
| sqlglot_parse              | 1.65 ms                                                               | 1.46 ms: 1.13x faster                                                 |
| async_tree_none            | 701 ms                                                                | 624 ms: 1.12x faster                                                  |
| async_tree_memoization     | 872 ms                                                                | 777 ms: 1.12x faster                                                  |
| pylint                     | 397 ms                                                                | 355 ms: 1.12x faster                                                  |
| async_tree_memoization_tg  | 828 ms                                                                | 740 ms: 1.12x faster                                                  |
| unpickle_list              | 6.86 us                                                               | 6.17 us: 1.11x faster                                                 |
| chaos                      | 78.8 ms                                                               | 71.4 ms: 1.10x faster                                                 |
| async_tree_io_tg           | 1.54 sec                                                              | 1.40 sec: 1.09x faster                                                |
| sqlglot_transpile          | 2.00 ms                                                               | 1.83 ms: 1.09x faster                                                 |
| sympy_sum                  | 168 ms                                                                | 154 ms: 1.09x faster                                                  |
| hexiom                     | 7.57 ms                                                               | 6.98 ms: 1.09x faster                                                 |
| nbody                      | 113 ms                                                                | 105 ms: 1.08x faster                                                  |
| async_tree_none_tg         | 620 ms                                                                | 577 ms: 1.08x faster                                                  |
| xml_etree_parse            | 209 ms                                                                | 195 ms: 1.07x faster                                                  |
| sympy_integrate            | 23.2 ms                                                               | 21.6 ms: 1.07x faster                                                 |
| unpickle_pure_python       | 278 us                                                                | 260 us: 1.07x faster                                                  |
| sympy_expand               | 482 ms                                                                | 454 ms: 1.06x faster                                                  |
| bench_mp_pool              | 7.44 ms                                                               | 7.05 ms: 1.05x faster                                                 |
| sympy_str                  | 295 ms                                                                | 280 ms: 1.05x faster                                                  |
| sqlglot_normalize          | 132 ms                                                                | 126 ms: 1.05x faster                                                  |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 912 ms: 1.05x faster                                                  |
| gunicorn                   | 1.19 ms                                                               | 1.14 ms: 1.05x faster                                                 |
| logging_silent             | 133 ns                                                                | 127 ns: 1.04x faster                                                  |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 884 ms: 1.04x faster                                                  |
| pidigits                   | 242 ms                                                                | 233 ms: 1.04x faster                                                  |
| go                         | 163 ms                                                                | 157 ms: 1.04x faster                                                  |
| bench_thread_pool          | 1.36 ms                                                               | 1.31 ms: 1.04x faster                                                 |
| sqlglot_optimize           | 63.4 ms                                                               | 61.3 ms: 1.03x faster                                                 |
| nqueens                    | 102 ms                                                                | 99.2 ms: 1.03x faster                                                 |
| meteor_contest             | 115 ms                                                                | 112 ms: 1.03x faster                                                  |
| tornado_http               | 140 ms                                                                | 136 ms: 1.03x faster                                                  |
| mako                       | 13.3 ms                                                               | 12.9 ms: 1.03x faster                                                 |
| django_template            | 41.8 ms                                                               | 40.7 ms: 1.03x faster                                                 |
| genshi_xml                 | 62.2 ms                                                               | 60.6 ms: 1.03x faster                                                 |
| genshi_text                | 28.2 ms                                                               | 27.4 ms: 1.03x faster                                                 |
| regex_v8                   | 29.1 ms                                                               | 28.3 ms: 1.03x faster                                                 |
| pickle_pure_python         | 374 us                                                                | 365 us: 1.02x faster                                                  |
| dask                       | 385 ms                                                                | 376 ms: 1.02x faster                                                  |
| dulwich_log                | 63.2 ms                                                               | 62.0 ms: 1.02x faster                                                 |
| fannkuch                   | 451 ms                                                                | 443 ms: 1.02x faster                                                  |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.19 ms: 1.01x faster                                                 |
| pathlib                    | 24.8 ms                                                               | 24.5 ms: 1.01x faster                                                 |
| tomli_loads                | 2.62 sec                                                              | 2.59 sec: 1.01x faster                                                |
| xml_etree_iterparse        | 152 ms                                                                | 150 ms: 1.01x faster                                                  |
| pickle_dict                | 37.6 us                                                               | 37.3 us: 1.01x faster                                                 |
| spectral_norm              | 131 ms                                                                | 131 ms: 1.00x faster                                                  |
| asyncio_websockets         | 656 ms                                                                | 658 ms: 1.00x slower                                                  |
| json                       | 5.52 ms                                                               | 5.54 ms: 1.00x slower                                                 |
| regex_compile              | 137 ms                                                                | 137 ms: 1.00x slower                                                  |
| raytrace                   | 351 ms                                                                | 353 ms: 1.01x slower                                                  |
| logging_simple             | 7.57 us                                                               | 7.63 us: 1.01x slower                                                 |
| deepcopy_memo              | 49.0 us                                                               | 49.6 us: 1.01x slower                                                 |
| json_loads                 | 30.3 us                                                               | 30.7 us: 1.01x slower                                                 |
| pprint_pformat             | 1.85 sec                                                              | 1.88 sec: 1.01x slower                                                |
| pprint_safe_repr           | 903 ms                                                                | 916 ms: 1.01x slower                                                  |
| logging_format             | 8.22 us                                                               | 8.34 us: 1.02x slower                                                 |
| gc_traversal               | 4.33 ms                                                               | 4.40 ms: 1.02x slower                                                 |
| mdp                        | 3.35 sec                                                              | 3.41 sec: 1.02x slower                                                |
| sqlalchemy_imperative      | 16.4 ms                                                               | 16.7 ms: 1.02x slower                                                 |
| docutils                   | 2.92 sec                                                              | 2.98 sec: 1.02x slower                                                |
| scimark_monte_carlo        | 83.2 ms                                                               | 85.1 ms: 1.02x slower                                                 |
| aiohttp                    | 1.13 ms                                                               | 1.16 ms: 1.02x slower                                                 |
| deepcopy                   | 435 us                                                                | 446 us: 1.02x slower                                                  |
| create_gc_cycles           | 1.87 ms                                                               | 1.92 ms: 1.02x slower                                                 |
| 2to3                       | 300 ms                                                                | 308 ms: 1.03x slower                                                  |
| float                      | 89.6 ms                                                               | 92.1 ms: 1.03x slower                                                 |
| scimark_sor                | 145 ms                                                                | 150 ms: 1.03x slower                                                  |
| thrift                     | 910 us                                                                | 937 us: 1.03x slower                                                  |
| xml_etree_process          | 76.1 ms                                                               | 79.0 ms: 1.04x slower                                                 |
| coverage                   | 84.1 ms                                                               | 87.3 ms: 1.04x slower                                                 |
| scimark_lu                 | 140 ms                                                                | 146 ms: 1.04x slower                                                  |
| scimark_fft                | 402 ms                                                                | 418 ms: 1.04x slower                                                  |
| pickle_list                | 5.01 us                                                               | 5.25 us: 1.05x slower                                                 |
| pickle                     | 12.8 us                                                               | 13.4 us: 1.05x slower                                                 |
| deepcopy_reduce            | 3.89 us                                                               | 4.10 us: 1.05x slower                                                 |
| sqlite_synth               | 3.56 us                                                               | 3.77 us: 1.06x slower                                                 |
| regex_dna                  | 239 ms                                                                | 254 ms: 1.06x slower                                                  |
| chameleon                  | 8.29 ms                                                               | 8.81 ms: 1.06x slower                                                 |
| xml_etree_generate         | 104 ms                                                                | 112 ms: 1.08x slower                                                  |
| pyflate                    | 516 ms                                                                | 559 ms: 1.08x slower                                                  |
| telco                      | 7.80 ms                                                               | 8.51 ms: 1.09x slower                                                 |
| regex_effbot               | 4.25 ms                                                               | 4.64 ms: 1.09x slower                                                 |
| unpickle                   | 16.9 us                                                               | 18.5 us: 1.10x slower                                                 |
| python_startup             | 10.2 ms                                                               | 11.4 ms: 1.12x slower                                                 |
| python_startup_no_site     | 7.35 ms                                                               | 8.37 ms: 1.14x slower                                                 |
| mypy2                      | 737 ms                                                                | 873 ms: 1.19x slower                                                  |
| async_generators           | 378 ms                                                                | 491 ms: 1.30x slower                                                  |
| Geometric mean             | (ref)                                                                 | 1.04x faster                                                          |

Benchmark hidden because not significant (4): html5lib, crypto_pyaes, sqlalchemy_declarative, pycparser
Ignored benchmarks (1) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: flaskblogging

# HPT report

- Reliability score: 98.99% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x