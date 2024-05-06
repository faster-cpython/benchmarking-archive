# Results vs. 3.12.0

- fork: python
- ref: c408c36e9b346f9f15a3
- machine: linux-aarch64
- commit hash: c408c36
- commit date: 2024-05-01
- overall geometric mean: 1.05x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 308 ms                                                                | 348 ms: 1.13x slower                                                     |
| chameleon      | 8.81 ms                                                               | 9.37 ms: 1.06x slower                                                    |
| docutils       | 2.98 sec                                                              | 3.40 sec: 1.14x slower                                                   |
| html5lib       | 65.1 ms                                                               | 70.4 ms: 1.08x slower                                                    |
| tornado_http   | 136 ms                                                                | 140 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                                 | 1.09x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 624 ms                                                                | 508 ms: 1.23x faster                                                     |
| async_tree_none_tg         | 577 ms                                                                | 472 ms: 1.22x faster                                                     |
| async_tree_memoization_tg  | 740 ms                                                                | 613 ms: 1.21x faster                                                     |
| async_tree_memoization     | 777 ms                                                                | 659 ms: 1.18x faster                                                     |
| async_tree_io_tg           | 1.40 sec                                                              | 1.20 sec: 1.17x faster                                                   |
| async_tree_cpu_io_mixed_tg | 884 ms                                                                | 773 ms: 1.14x faster                                                     |
| async_tree_io              | 1.41 sec                                                              | 1.24 sec: 1.14x faster                                                   |
| async_tree_cpu_io_mixed    | 912 ms                                                                | 804 ms: 1.13x faster                                                     |
| Geometric mean             | (ref)                                                                 | 1.18x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 92.1 ms                                                               | 89.2 ms: 1.03x faster                                                    |
| pidigits       | 233 ms                                                                | 233 ms: 1.00x slower                                                     |
| nbody          | 105 ms                                                                | 107 ms: 1.03x slower                                                     |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 254 ms                                                                | 247 ms: 1.03x faster                                                     |
| regex_effbot   | 4.64 ms                                                               | 4.85 ms: 1.05x slower                                                    |
| regex_v8       | 28.3 ms                                                               | 30.2 ms: 1.07x slower                                                    |
| regex_compile  | 137 ms                                                                | 160 ms: 1.17x slower                                                     |
| Geometric mean | (ref)                                                                 | 1.06x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 195 ms                                                                | 188 ms: 1.04x faster                                                     |
| pickle_pure_python   | 365 us                                                                | 354 us: 1.03x faster                                                     |
| xml_etree_iterparse  | 150 ms                                                                | 147 ms: 1.02x faster                                                     |
| tomli_loads          | 2.59 sec                                                              | 2.57 sec: 1.01x faster                                                   |
| xml_etree_generate   | 112 ms                                                                | 113 ms: 1.01x slower                                                     |
| pickle_dict          | 37.3 us                                                               | 37.8 us: 1.01x slower                                                    |
| xml_etree_process    | 79.0 ms                                                               | 80.3 ms: 1.02x slower                                                    |
| unpickle_list        | 6.17 us                                                               | 6.31 us: 1.02x slower                                                    |
| json_loads           | 30.7 us                                                               | 31.9 us: 1.04x slower                                                    |
| json_dumps           | 12.3 ms                                                               | 12.8 ms: 1.05x slower                                                    |
| unpickle_pure_python | 260 us                                                                | 276 us: 1.06x slower                                                     |
| unpickle             | 18.5 us                                                               | 19.7 us: 1.07x slower                                                    |
| Geometric mean       | (ref)                                                                 | 1.01x slower                                                             |

Benchmark hidden because not significant (2): pickle_list, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 8.37 ms                                                               | 10.7 ms: 1.28x slower                                                    |
| python_startup         | 11.4 ms                                                               | 14.7 ms: 1.29x slower                                                    |
| Geometric mean         | (ref)                                                                 | 1.28x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 12.9 ms                                                               | 12.8 ms: 1.01x faster                                                    |
| django_template | 40.7 ms                                                               | 48.3 ms: 1.19x slower                                                    |
| genshi_text     | 27.4 ms                                                               | 33.8 ms: 1.23x slower                                                    |
| genshi_xml      | 60.6 ms                                                               | 79.5 ms: 1.31x slower                                                    |
| Geometric mean  | (ref)                                                                 | 1.17x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0 | bm-20240501-arminc-aarch64-python-c408c36e9b346f9f15a3-3.13.0a6+-c408c36 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 624 ms                                                                | 508 ms: 1.23x faster                                                     |
| async_tree_none_tg         | 577 ms                                                                | 472 ms: 1.22x faster                                                     |
| async_tree_memoization_tg  | 740 ms                                                                | 613 ms: 1.21x faster                                                     |
| async_tree_memoization     | 777 ms                                                                | 659 ms: 1.18x faster                                                     |
| async_tree_io_tg           | 1.40 sec                                                              | 1.20 sec: 1.17x faster                                                   |
| async_tree_cpu_io_mixed_tg | 884 ms                                                                | 773 ms: 1.14x faster                                                     |
| generators                 | 43.5 ms                                                               | 38.1 ms: 1.14x faster                                                    |
| async_tree_io              | 1.41 sec                                                              | 1.24 sec: 1.14x faster                                                   |
| async_tree_cpu_io_mixed    | 912 ms                                                                | 804 ms: 1.13x faster                                                     |
| raytrace                   | 353 ms                                                                | 317 ms: 1.11x faster                                                     |
| comprehensions             | 25.4 us                                                               | 23.5 us: 1.08x faster                                                    |
| pathlib                    | 24.5 ms                                                               | 23.3 ms: 1.05x faster                                                    |
| xml_etree_parse            | 195 ms                                                                | 188 ms: 1.04x faster                                                     |
| float                      | 92.1 ms                                                               | 89.2 ms: 1.03x faster                                                    |
| pickle_pure_python         | 365 us                                                                | 354 us: 1.03x faster                                                     |
| regex_dna                  | 254 ms                                                                | 247 ms: 1.03x faster                                                     |
| xml_etree_iterparse        | 150 ms                                                                | 147 ms: 1.02x faster                                                     |
| tomli_loads                | 2.59 sec                                                              | 2.57 sec: 1.01x faster                                                   |
| mako                       | 12.9 ms                                                               | 12.8 ms: 1.01x faster                                                    |
| scimark_monte_carlo        | 85.1 ms                                                               | 84.4 ms: 1.01x faster                                                    |
| pidigits                   | 233 ms                                                                | 233 ms: 1.00x slower                                                     |
| crypto_pyaes               | 86.6 ms                                                               | 87.5 ms: 1.01x slower                                                    |
| xml_etree_generate         | 112 ms                                                                | 113 ms: 1.01x slower                                                     |
| pickle_dict                | 37.3 us                                                               | 37.8 us: 1.01x slower                                                    |
| sqlite_synth               | 3.77 us                                                               | 3.81 us: 1.01x slower                                                    |
| bench_thread_pool          | 1.31 ms                                                               | 1.33 ms: 1.01x slower                                                    |
| richards_super             | 58.5 ms                                                               | 59.3 ms: 1.01x slower                                                    |
| xml_etree_process          | 79.0 ms                                                               | 80.3 ms: 1.02x slower                                                    |
| pycparser                  | 1.26 sec                                                              | 1.28 sec: 1.02x slower                                                   |
| json                       | 5.54 ms                                                               | 5.66 ms: 1.02x slower                                                    |
| unpickle_list              | 6.17 us                                                               | 6.31 us: 1.02x slower                                                    |
| deepcopy_memo              | 49.6 us                                                               | 50.8 us: 1.02x slower                                                    |
| nbody                      | 105 ms                                                                | 107 ms: 1.03x slower                                                     |
| deepcopy_reduce            | 4.10 us                                                               | 4.22 us: 1.03x slower                                                    |
| tornado_http               | 136 ms                                                                | 140 ms: 1.03x slower                                                     |
| richards                   | 50.9 ms                                                               | 52.5 ms: 1.03x slower                                                    |
| sqlglot_transpile          | 1.83 ms                                                               | 1.88 ms: 1.03x slower                                                    |
| sqlglot_parse              | 1.46 ms                                                               | 1.51 ms: 1.03x slower                                                    |
| coroutines                 | 29.0 ms                                                               | 29.9 ms: 1.03x slower                                                    |
| deepcopy                   | 446 us                                                                | 461 us: 1.04x slower                                                     |
| json_loads                 | 30.7 us                                                               | 31.9 us: 1.04x slower                                                    |
| async_generators           | 491 ms                                                                | 510 ms: 1.04x slower                                                     |
| asyncio_tcp_ssl            | 2.19 sec                                                              | 2.27 sec: 1.04x slower                                                   |
| fannkuch                   | 443 ms                                                                | 461 ms: 1.04x slower                                                     |
| regex_effbot               | 4.64 ms                                                               | 4.85 ms: 1.05x slower                                                    |
| dask                       | 376 ms                                                                | 394 ms: 1.05x slower                                                     |
| json_dumps                 | 12.3 ms                                                               | 12.8 ms: 1.05x slower                                                    |
| logging_silent             | 127 ns                                                                | 133 ns: 1.05x slower                                                     |
| thrift                     | 937 us                                                                | 985 us: 1.05x slower                                                     |
| pyflate                    | 559 ms                                                                | 592 ms: 1.06x slower                                                     |
| meteor_contest             | 112 ms                                                                | 119 ms: 1.06x slower                                                     |
| unpickle_pure_python       | 260 us                                                                | 276 us: 1.06x slower                                                     |
| chameleon                  | 8.81 ms                                                               | 9.37 ms: 1.06x slower                                                    |
| regex_v8                   | 28.3 ms                                                               | 30.2 ms: 1.07x slower                                                    |
| unpickle                   | 18.5 us                                                               | 19.7 us: 1.07x slower                                                    |
| html5lib                   | 65.1 ms                                                               | 70.4 ms: 1.08x slower                                                    |
| scimark_fft                | 418 ms                                                                | 453 ms: 1.08x slower                                                     |
| sqlglot_normalize          | 126 ms                                                                | 137 ms: 1.09x slower                                                     |
| spectral_norm              | 131 ms                                                                | 143 ms: 1.09x slower                                                     |
| sympy_str                  | 280 ms                                                                | 307 ms: 1.10x slower                                                     |
| asyncio_tcp                | 566 ms                                                                | 622 ms: 1.10x slower                                                     |
| sqlglot_optimize           | 61.3 ms                                                               | 68.0 ms: 1.11x slower                                                    |
| deltablue                  | 4.12 ms                                                               | 4.59 ms: 1.11x slower                                                    |
| scimark_sparse_mat_mult    | 6.19 ms                                                               | 6.96 ms: 1.12x slower                                                    |
| sympy_sum                  | 154 ms                                                                | 174 ms: 1.13x slower                                                     |
| 2to3                       | 308 ms                                                                | 348 ms: 1.13x slower                                                     |
| coverage                   | 87.3 ms                                                               | 99.2 ms: 1.14x slower                                                    |
| dulwich_log                | 62.0 ms                                                               | 70.5 ms: 1.14x slower                                                    |
| docutils                   | 2.98 sec                                                              | 3.40 sec: 1.14x slower                                                   |
| sympy_expand               | 454 ms                                                                | 520 ms: 1.15x slower                                                     |
| gc_traversal               | 4.40 ms                                                               | 5.05 ms: 1.15x slower                                                    |
| chaos                      | 71.4 ms                                                               | 82.1 ms: 1.15x slower                                                    |
| pylint                     | 355 ms                                                                | 408 ms: 1.15x slower                                                     |
| regex_compile              | 137 ms                                                                | 160 ms: 1.17x slower                                                     |
| sympy_integrate            | 21.6 ms                                                               | 25.5 ms: 1.18x slower                                                    |
| typing_runtime_protocols   | 181 us                                                                | 213 us: 1.18x slower                                                     |
| django_template            | 40.7 ms                                                               | 48.3 ms: 1.19x slower                                                    |
| go                         | 157 ms                                                                | 187 ms: 1.19x slower                                                     |
| create_gc_cycles           | 1.92 ms                                                               | 2.30 ms: 1.20x slower                                                    |
| nqueens                    | 99.2 ms                                                               | 120 ms: 1.21x slower                                                     |
| telco                      | 8.51 ms                                                               | 10.3 ms: 1.21x slower                                                    |
| scimark_sor                | 150 ms                                                                | 183 ms: 1.22x slower                                                     |
| genshi_text                | 27.4 ms                                                               | 33.8 ms: 1.23x slower                                                    |
| bench_mp_pool              | 7.05 ms                                                               | 8.69 ms: 1.23x slower                                                    |
| scimark_lu                 | 146 ms                                                                | 181 ms: 1.24x slower                                                     |
| python_startup_no_site     | 8.37 ms                                                               | 10.7 ms: 1.28x slower                                                    |
| hexiom                     | 6.98 ms                                                               | 8.94 ms: 1.28x slower                                                    |
| pprint_safe_repr           | 916 ms                                                                | 1.18 sec: 1.29x slower                                                   |
| pprint_pformat             | 1.88 sec                                                              | 2.43 sec: 1.29x slower                                                   |
| python_startup             | 11.4 ms                                                               | 14.7 ms: 1.29x slower                                                    |
| genshi_xml                 | 60.6 ms                                                               | 79.5 ms: 1.31x slower                                                    |
| Geometric mean             | (ref)                                                                 | 1.05x slower                                                             |

Benchmark hidden because not significant (6): pickle_list, logging_simple, logging_format, asyncio_websockets, pickle, mdp
Ignored benchmarks (5) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-arminc-aarch64-python-0fb18b02c8ad56299d6a-3.12.0-0fb18b0.json: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.03x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 0.99x