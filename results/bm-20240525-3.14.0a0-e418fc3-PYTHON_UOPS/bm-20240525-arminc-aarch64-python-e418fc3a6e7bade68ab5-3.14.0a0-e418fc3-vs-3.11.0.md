# Results vs. 3.11.0

- fork: python
- ref: e418fc3a6e7bade68ab5
- machine: linux-aarch64
- commit hash: e418fc3
- commit date: 2024-05-25
- overall geometric mean: 1.10x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 359 ms: 1.20x slower                                                    |
| chameleon      | 8.29 ms                                                               | 10.2 ms: 1.24x slower                                                   |
| docutils       | 2.92 sec                                                              | 3.54 sec: 1.21x slower                                                  |
| html5lib       | 65.3 ms                                                               | 74.4 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                                 | 1.15x slower                                                            |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 529 ms: 1.33x faster                                                    |
| async_tree_memoization_tg  | 828 ms                                                                | 640 ms: 1.29x faster                                                    |
| async_tree_memoization     | 872 ms                                                                | 697 ms: 1.25x faster                                                    |
| async_tree_io              | 1.61 sec                                                              | 1.30 sec: 1.24x faster                                                  |
| async_tree_none_tg         | 620 ms                                                                | 501 ms: 1.24x faster                                                    |
| async_tree_io_tg           | 1.54 sec                                                              | 1.24 sec: 1.24x faster                                                  |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 809 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 850 ms: 1.12x faster                                                    |
| Geometric mean             | (ref)                                                                 | 1.23x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 237 ms: 1.02x faster                                                    |
| float          | 89.6 ms                                                               | 117 ms: 1.30x slower                                                    |
| nbody          | 113 ms                                                                | 151 ms: 1.34x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.19x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_v8       | 29.1 ms                                                               | 30.9 ms: 1.06x slower                                                   |
| regex_dna      | 239 ms                                                                | 257 ms: 1.08x slower                                                    |
| regex_effbot   | 4.25 ms                                                               | 4.93 ms: 1.16x slower                                                   |
| regex_compile  | 137 ms                                                                | 171 ms: 1.25x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.14x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 13.7 ms: 1.13x faster                                                   |
| xml_etree_parse      | 209 ms                                                                | 191 ms: 1.10x faster                                                    |
| unpickle_list        | 6.86 us                                                               | 6.51 us: 1.05x faster                                                   |
| pickle_list          | 5.01 us                                                               | 5.32 us: 1.06x slower                                                   |
| xml_etree_iterparse  | 152 ms                                                                | 162 ms: 1.07x slower                                                    |
| json_loads           | 30.3 us                                                               | 32.4 us: 1.07x slower                                                   |
| pickle               | 12.8 us                                                               | 13.8 us: 1.08x slower                                                   |
| xml_etree_process    | 76.1 ms                                                               | 88.2 ms: 1.16x slower                                                   |
| unpickle             | 16.9 us                                                               | 19.7 us: 1.17x slower                                                   |
| xml_etree_generate   | 104 ms                                                                | 128 ms: 1.23x slower                                                    |
| tomli_loads          | 2.62 sec                                                              | 3.25 sec: 1.24x slower                                                  |
| pickle_pure_python   | 374 us                                                                | 467 us: 1.25x slower                                                    |
| unpickle_pure_python | 278 us                                                                | 367 us: 1.32x slower                                                    |
| Geometric mean       | (ref)                                                                 | 1.09x slower                                                            |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 8.57 ms: 1.17x slower                                                   |
| python_startup         | 10.2 ms                                                               | 12.8 ms: 1.25x slower                                                   |
| Geometric mean         | (ref)                                                                 | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| django_template | 41.8 ms                                                               | 50.1 ms: 1.20x slower                                                   |
| genshi_xml      | 62.2 ms                                                               | 78.5 ms: 1.26x slower                                                   |
| mako            | 13.3 ms                                                               | 17.3 ms: 1.30x slower                                                   |
| genshi_text     | 28.2 ms                                                               | 37.6 ms: 1.33x slower                                                   |
| Geometric mean  | (ref)                                                                 | 1.27x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240525-arminc-aarch64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 226 us: 2.89x faster                                                    |
| generators                 | 64.2 ms                                                               | 40.7 ms: 1.58x faster                                                   |
| asyncio_tcp                | 920 ms                                                                | 588 ms: 1.56x faster                                                    |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.23 sec: 1.43x faster                                                  |
| async_tree_none            | 701 ms                                                                | 529 ms: 1.33x faster                                                    |
| async_tree_memoization_tg  | 828 ms                                                                | 640 ms: 1.29x faster                                                    |
| async_tree_memoization     | 872 ms                                                                | 697 ms: 1.25x faster                                                    |
| async_tree_io              | 1.61 sec                                                              | 1.30 sec: 1.24x faster                                                  |
| async_tree_none_tg         | 620 ms                                                                | 501 ms: 1.24x faster                                                    |
| async_tree_io_tg           | 1.54 sec                                                              | 1.24 sec: 1.24x faster                                                  |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 809 ms: 1.14x faster                                                    |
| json_dumps                 | 15.4 ms                                                               | 13.7 ms: 1.13x faster                                                   |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 850 ms: 1.12x faster                                                    |
| pathlib                    | 24.8 ms                                                               | 22.3 ms: 1.11x faster                                                   |
| xml_etree_parse            | 209 ms                                                                | 191 ms: 1.10x faster                                                    |
| coroutines                 | 33.3 ms                                                               | 30.8 ms: 1.08x faster                                                   |
| unpickle_list              | 6.86 us                                                               | 6.51 us: 1.05x faster                                                   |
| logging_simple             | 7.57 us                                                               | 7.36 us: 1.03x faster                                                   |
| logging_format             | 8.22 us                                                               | 8.01 us: 1.03x faster                                                   |
| pidigits                   | 242 ms                                                                | 237 ms: 1.02x faster                                                    |
| raytrace                   | 351 ms                                                                | 348 ms: 1.01x faster                                                    |
| asyncio_websockets         | 656 ms                                                                | 662 ms: 1.01x slower                                                    |
| bench_thread_pool          | 1.36 ms                                                               | 1.39 ms: 1.03x slower                                                   |
| dulwich_log                | 63.2 ms                                                               | 66.1 ms: 1.05x slower                                                   |
| sympy_sum                  | 168 ms                                                                | 176 ms: 1.05x slower                                                    |
| json                       | 5.52 ms                                                               | 5.83 ms: 1.05x slower                                                   |
| pickle_list                | 5.01 us                                                               | 5.32 us: 1.06x slower                                                   |
| regex_v8                   | 29.1 ms                                                               | 30.9 ms: 1.06x slower                                                   |
| richards_super             | 70.2 ms                                                               | 74.7 ms: 1.06x slower                                                   |
| xml_etree_iterparse        | 152 ms                                                                | 162 ms: 1.07x slower                                                    |
| json_loads                 | 30.3 us                                                               | 32.4 us: 1.07x slower                                                   |
| mdp                        | 3.35 sec                                                              | 3.60 sec: 1.07x slower                                                  |
| pickle                     | 12.8 us                                                               | 13.8 us: 1.08x slower                                                   |
| regex_dna                  | 239 ms                                                                | 257 ms: 1.08x slower                                                    |
| thrift                     | 910 us                                                                | 987 us: 1.08x slower                                                    |
| sympy_str                  | 295 ms                                                                | 321 ms: 1.09x slower                                                    |
| sqlglot_parse              | 1.65 ms                                                               | 1.81 ms: 1.10x slower                                                   |
| comprehensions             | 29.0 us                                                               | 31.8 us: 1.10x slower                                                   |
| sqlite_synth               | 3.56 us                                                               | 3.93 us: 1.11x slower                                                   |
| sympy_expand               | 482 ms                                                                | 533 ms: 1.11x slower                                                    |
| deltablue                  | 4.75 ms                                                               | 5.31 ms: 1.12x slower                                                   |
| pycparser                  | 1.25 sec                                                              | 1.40 sec: 1.12x slower                                                  |
| sqlglot_normalize          | 132 ms                                                                | 149 ms: 1.13x slower                                                    |
| sqlglot_transpile          | 2.00 ms                                                               | 2.26 ms: 1.13x slower                                                   |
| chaos                      | 78.8 ms                                                               | 89.4 ms: 1.13x slower                                                   |
| html5lib                   | 65.3 ms                                                               | 74.4 ms: 1.14x slower                                                   |
| sympy_integrate            | 23.2 ms                                                               | 26.6 ms: 1.15x slower                                                   |
| sqlglot_optimize           | 63.4 ms                                                               | 72.9 ms: 1.15x slower                                                   |
| regex_effbot               | 4.25 ms                                                               | 4.93 ms: 1.16x slower                                                   |
| bench_mp_pool              | 7.44 ms                                                               | 8.62 ms: 1.16x slower                                                   |
| xml_etree_process          | 76.1 ms                                                               | 88.2 ms: 1.16x slower                                                   |
| python_startup_no_site     | 7.35 ms                                                               | 8.57 ms: 1.17x slower                                                   |
| meteor_contest             | 115 ms                                                                | 135 ms: 1.17x slower                                                    |
| unpickle                   | 16.9 us                                                               | 19.7 us: 1.17x slower                                                   |
| richards                   | 58.1 ms                                                               | 68.2 ms: 1.17x slower                                                   |
| 2to3                       | 300 ms                                                                | 359 ms: 1.20x slower                                                    |
| django_template            | 41.8 ms                                                               | 50.1 ms: 1.20x slower                                                   |
| coverage                   | 84.1 ms                                                               | 101 ms: 1.20x slower                                                    |
| docutils                   | 2.92 sec                                                              | 3.54 sec: 1.21x slower                                                  |
| gc_traversal               | 4.33 ms                                                               | 5.28 ms: 1.22x slower                                                   |
| crypto_pyaes               | 86.5 ms                                                               | 106 ms: 1.22x slower                                                    |
| xml_etree_generate         | 104 ms                                                                | 128 ms: 1.23x slower                                                    |
| chameleon                  | 8.29 ms                                                               | 10.2 ms: 1.24x slower                                                   |
| go                         | 163 ms                                                                | 202 ms: 1.24x slower                                                    |
| tomli_loads                | 2.62 sec                                                              | 3.25 sec: 1.24x slower                                                  |
| flaskblogging              | 4.19 ms                                                               | 5.22 ms: 1.24x slower                                                   |
| pickle_pure_python         | 374 us                                                                | 467 us: 1.25x slower                                                    |
| python_startup             | 10.2 ms                                                               | 12.8 ms: 1.25x slower                                                   |
| regex_compile              | 137 ms                                                                | 171 ms: 1.25x slower                                                    |
| deepcopy_reduce            | 3.89 us                                                               | 4.88 us: 1.26x slower                                                   |
| genshi_xml                 | 62.2 ms                                                               | 78.5 ms: 1.26x slower                                                   |
| deepcopy                   | 435 us                                                                | 553 us: 1.27x slower                                                    |
| create_gc_cycles           | 1.87 ms                                                               | 2.39 ms: 1.28x slower                                                   |
| float                      | 89.6 ms                                                               | 117 ms: 1.30x slower                                                    |
| mako                       | 13.3 ms                                                               | 17.3 ms: 1.30x slower                                                   |
| unpickle_pure_python       | 278 us                                                                | 367 us: 1.32x slower                                                    |
| nqueens                    | 102 ms                                                                | 136 ms: 1.32x slower                                                    |
| fannkuch                   | 451 ms                                                                | 598 ms: 1.32x slower                                                    |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 8.35 ms: 1.33x slower                                                   |
| pprint_pformat             | 1.85 sec                                                              | 2.47 sec: 1.33x slower                                                  |
| genshi_text                | 28.2 ms                                                               | 37.6 ms: 1.33x slower                                                   |
| pprint_safe_repr           | 903 ms                                                                | 1.21 sec: 1.34x slower                                                  |
| nbody                      | 113 ms                                                                | 151 ms: 1.34x slower                                                    |
| async_generators           | 378 ms                                                                | 515 ms: 1.36x slower                                                    |
| telco                      | 7.80 ms                                                               | 10.8 ms: 1.38x slower                                                   |
| scimark_fft                | 402 ms                                                                | 558 ms: 1.39x slower                                                    |
| scimark_sor                | 145 ms                                                                | 202 ms: 1.39x slower                                                    |
| scimark_monte_carlo        | 83.2 ms                                                               | 119 ms: 1.43x slower                                                    |
| pyflate                    | 516 ms                                                                | 760 ms: 1.47x slower                                                    |
| spectral_norm              | 131 ms                                                                | 194 ms: 1.48x slower                                                    |
| logging_silent             | 133 ns                                                                | 197 ns: 1.49x slower                                                    |
| hexiom                     | 7.57 ms                                                               | 11.3 ms: 1.49x slower                                                   |
| scimark_lu                 | 140 ms                                                                | 211 ms: 1.51x slower                                                    |
| deepcopy_memo              | 49.0 us                                                               | 75.9 us: 1.55x slower                                                   |
| Geometric mean             | (ref)                                                                 | 1.10x slower                                                            |

Benchmark hidden because not significant (4): tornado_http, pickle_dict, pylint, dask
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.05x