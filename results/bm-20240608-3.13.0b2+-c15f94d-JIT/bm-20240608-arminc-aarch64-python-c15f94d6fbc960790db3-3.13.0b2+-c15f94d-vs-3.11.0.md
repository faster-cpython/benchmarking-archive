# Results vs. 3.11.0

- fork: python
- ref: c15f94d6fbc960790db3
- machine: linux-aarch64
- commit hash: c15f94d
- commit date: 2024-06-08
- overall geometric mean: 1.03x slower
- HPT reliability: 99.88%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 362 ms: 1.21x slower                                                     |
| chameleon      | 8.29 ms                                                               | 9.09 ms: 1.10x slower                                                    |
| docutils       | 2.92 sec                                                              | 3.54 sec: 1.21x slower                                                   |
| html5lib       | 65.3 ms                                                               | 72.6 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                                 | 1.13x slower                                                             |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 507 ms: 1.38x faster                                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 618 ms: 1.34x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.23 sec: 1.31x faster                                                   |
| async_tree_memoization     | 872 ms                                                                | 668 ms: 1.31x faster                                                     |
| async_tree_none_tg         | 620 ms                                                                | 481 ms: 1.29x faster                                                     |
| async_tree_io_tg           | 1.54 sec                                                              | 1.22 sec: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 798 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 827 ms: 1.16x faster                                                     |
| Geometric mean             | (ref)                                                                 | 1.27x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 235 ms: 1.03x faster                                                     |
| nbody          | 113 ms                                                                | 114 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                             |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 29.1 ms                                                               | 30.2 ms: 1.04x slower                                                    |
| regex_dna      | 239 ms                                                                | 260 ms: 1.09x slower                                                     |
| regex_effbot   | 4.25 ms                                                               | 4.97 ms: 1.17x slower                                                    |
| regex_compile  | 137 ms                                                                | 178 ms: 1.30x slower                                                     |
| Geometric mean | (ref)                                                                 | 1.14x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark          | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|--------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps         | 15.4 ms                                                               | 13.0 ms: 1.18x faster                                                    |
| xml_etree_parse    | 209 ms                                                                | 187 ms: 1.12x faster                                                     |
| unpickle_list      | 6.86 us                                                               | 6.59 us: 1.04x faster                                                    |
| tomli_loads        | 2.62 sec                                                              | 2.63 sec: 1.01x slower                                                   |
| pickle             | 12.8 us                                                               | 13.4 us: 1.05x slower                                                    |
| xml_etree_process  | 76.1 ms                                                               | 80.2 ms: 1.05x slower                                                    |
| pickle_list        | 5.01 us                                                               | 5.30 us: 1.06x slower                                                    |
| json_loads         | 30.3 us                                                               | 32.3 us: 1.06x slower                                                    |
| pickle_pure_python | 374 us                                                                | 398 us: 1.07x slower                                                     |
| xml_etree_generate | 104 ms                                                                | 113 ms: 1.09x slower                                                     |
| unpickle           | 16.9 us                                                               | 19.7 us: 1.17x slower                                                    |
| Geometric mean     | (ref)                                                                 | 1.01x slower                                                             |

Benchmark hidden because not significant (3): xml_etree_iterparse, unpickle_pure_python, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 11.1 ms: 1.51x slower                                                    |
| python_startup         | 10.2 ms                                                               | 15.5 ms: 1.52x slower                                                    |
| Geometric mean         | (ref)                                                                 | 1.52x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 13.3 ms                                                               | 13.0 ms: 1.02x faster                                                    |
| genshi_text     | 28.2 ms                                                               | 33.9 ms: 1.20x slower                                                    |
| django_template | 41.8 ms                                                               | 50.5 ms: 1.21x slower                                                    |
| genshi_xml      | 62.2 ms                                                               | 82.6 ms: 1.33x slower                                                    |
| Geometric mean  | (ref)                                                                 | 1.17x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 209 us: 3.13x faster                                                     |
| generators                 | 64.2 ms                                                               | 39.7 ms: 1.62x faster                                                    |
| asyncio_tcp                | 920 ms                                                                | 630 ms: 1.46x faster                                                     |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.28 sec: 1.40x faster                                                   |
| async_tree_none            | 701 ms                                                                | 507 ms: 1.38x faster                                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 618 ms: 1.34x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.23 sec: 1.31x faster                                                   |
| async_tree_memoization     | 872 ms                                                                | 668 ms: 1.31x faster                                                     |
| async_tree_none_tg         | 620 ms                                                                | 481 ms: 1.29x faster                                                     |
| async_tree_io_tg           | 1.54 sec                                                              | 1.22 sec: 1.25x faster                                                   |
| comprehensions             | 29.0 us                                                               | 23.1 us: 1.25x faster                                                    |
| json_dumps                 | 15.4 ms                                                               | 13.0 ms: 1.18x faster                                                    |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 798 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 827 ms: 1.16x faster                                                     |
| coroutines                 | 33.3 ms                                                               | 28.9 ms: 1.15x faster                                                    |
| xml_etree_parse            | 209 ms                                                                | 187 ms: 1.12x faster                                                     |
| richards_super             | 70.2 ms                                                               | 62.8 ms: 1.12x faster                                                    |
| raytrace                   | 351 ms                                                                | 322 ms: 1.09x faster                                                     |
| pathlib                    | 24.8 ms                                                               | 23.2 ms: 1.07x faster                                                    |
| richards                   | 58.1 ms                                                               | 55.7 ms: 1.04x faster                                                    |
| deltablue                  | 4.75 ms                                                               | 4.55 ms: 1.04x faster                                                    |
| unpickle_list              | 6.86 us                                                               | 6.59 us: 1.04x faster                                                    |
| sqlglot_parse              | 1.65 ms                                                               | 1.58 ms: 1.04x faster                                                    |
| pidigits                   | 242 ms                                                                | 235 ms: 1.03x faster                                                     |
| logging_format             | 8.22 us                                                               | 7.98 us: 1.03x faster                                                    |
| logging_simple             | 7.57 us                                                               | 7.35 us: 1.03x faster                                                    |
| mako                       | 13.3 ms                                                               | 13.0 ms: 1.02x faster                                                    |
| bench_thread_pool          | 1.36 ms                                                               | 1.33 ms: 1.02x faster                                                    |
| tomli_loads                | 2.62 sec                                                              | 2.63 sec: 1.01x slower                                                   |
| meteor_contest             | 115 ms                                                                | 117 ms: 1.01x slower                                                     |
| nbody                      | 113 ms                                                                | 114 ms: 1.01x slower                                                     |
| asyncio_websockets         | 656 ms                                                                | 666 ms: 1.02x slower                                                     |
| dask                       | 385 ms                                                                | 392 ms: 1.02x slower                                                     |
| fannkuch                   | 451 ms                                                                | 462 ms: 1.02x slower                                                     |
| crypto_pyaes               | 86.5 ms                                                               | 88.8 ms: 1.03x slower                                                    |
| mdp                        | 3.35 sec                                                              | 3.45 sec: 1.03x slower                                                   |
| json                       | 5.52 ms                                                               | 5.71 ms: 1.03x slower                                                    |
| regex_v8                   | 29.1 ms                                                               | 30.2 ms: 1.04x slower                                                    |
| pickle                     | 12.8 us                                                               | 13.4 us: 1.05x slower                                                    |
| logging_silent             | 133 ns                                                                | 139 ns: 1.05x slower                                                     |
| xml_etree_process          | 76.1 ms                                                               | 80.2 ms: 1.05x slower                                                    |
| pickle_list                | 5.01 us                                                               | 5.30 us: 1.06x slower                                                    |
| pylint                     | 397 ms                                                                | 421 ms: 1.06x slower                                                     |
| json_loads                 | 30.3 us                                                               | 32.3 us: 1.06x slower                                                    |
| pickle_pure_python         | 374 us                                                                | 398 us: 1.07x slower                                                     |
| thrift                     | 910 us                                                                | 974 us: 1.07x slower                                                     |
| sqlite_synth               | 3.56 us                                                               | 3.81 us: 1.07x slower                                                    |
| sqlglot_normalize          | 132 ms                                                                | 142 ms: 1.08x slower                                                     |
| scimark_monte_carlo        | 83.2 ms                                                               | 90.0 ms: 1.08x slower                                                    |
| regex_dna                  | 239 ms                                                                | 260 ms: 1.09x slower                                                     |
| xml_etree_generate         | 104 ms                                                                | 113 ms: 1.09x slower                                                     |
| sqlglot_optimize           | 63.4 ms                                                               | 69.3 ms: 1.09x slower                                                    |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.89 ms: 1.10x slower                                                    |
| chameleon                  | 8.29 ms                                                               | 9.09 ms: 1.10x slower                                                    |
| sympy_str                  | 295 ms                                                                | 323 ms: 1.10x slower                                                     |
| go                         | 163 ms                                                                | 179 ms: 1.10x slower                                                     |
| sympy_sum                  | 168 ms                                                                | 185 ms: 1.10x slower                                                     |
| pycparser                  | 1.25 sec                                                              | 1.38 sec: 1.10x slower                                                   |
| bench_mp_pool              | 7.44 ms                                                               | 8.22 ms: 1.11x slower                                                    |
| sympy_integrate            | 23.2 ms                                                               | 25.6 ms: 1.11x slower                                                    |
| html5lib                   | 65.3 ms                                                               | 72.6 ms: 1.11x slower                                                    |
| chaos                      | 78.8 ms                                                               | 88.0 ms: 1.12x slower                                                    |
| spectral_norm              | 131 ms                                                                | 147 ms: 1.13x slower                                                     |
| dulwich_log                | 63.2 ms                                                               | 71.8 ms: 1.14x slower                                                    |
| sympy_expand               | 482 ms                                                                | 547 ms: 1.14x slower                                                     |
| nqueens                    | 102 ms                                                                | 117 ms: 1.14x slower                                                     |
| deepcopy                   | 435 us                                                                | 495 us: 1.14x slower                                                     |
| scimark_fft                | 402 ms                                                                | 460 ms: 1.14x slower                                                     |
| gunicorn                   | 1.19 ms                                                               | 1.36 ms: 1.14x slower                                                    |
| pyflate                    | 516 ms                                                                | 596 ms: 1.16x slower                                                     |
| aiohttp                    | 1.13 ms                                                               | 1.32 ms: 1.16x slower                                                    |
| unpickle                   | 16.9 us                                                               | 19.7 us: 1.17x slower                                                    |
| regex_effbot               | 4.25 ms                                                               | 4.97 ms: 1.17x slower                                                    |
| deepcopy_reduce            | 3.89 us                                                               | 4.60 us: 1.18x slower                                                    |
| coverage                   | 84.1 ms                                                               | 99.5 ms: 1.18x slower                                                    |
| gc_traversal               | 4.33 ms                                                               | 5.16 ms: 1.19x slower                                                    |
| hexiom                     | 7.57 ms                                                               | 9.05 ms: 1.19x slower                                                    |
| genshi_text                | 28.2 ms                                                               | 33.9 ms: 1.20x slower                                                    |
| scimark_sor                | 145 ms                                                                | 175 ms: 1.20x slower                                                     |
| 2to3                       | 300 ms                                                                | 362 ms: 1.21x slower                                                     |
| django_template            | 41.8 ms                                                               | 50.5 ms: 1.21x slower                                                    |
| docutils                   | 2.92 sec                                                              | 3.54 sec: 1.21x slower                                                   |
| flaskblogging              | 4.19 ms                                                               | 5.14 ms: 1.22x slower                                                    |
| pprint_safe_repr           | 903 ms                                                                | 1.11 sec: 1.23x slower                                                   |
| pprint_pformat             | 1.85 sec                                                              | 2.32 sec: 1.25x slower                                                   |
| create_gc_cycles           | 1.87 ms                                                               | 2.39 ms: 1.28x slower                                                    |
| mypy2                      | 737 ms                                                                | 948 ms: 1.29x slower                                                     |
| telco                      | 7.80 ms                                                               | 10.1 ms: 1.30x slower                                                    |
| regex_compile              | 137 ms                                                                | 178 ms: 1.30x slower                                                     |
| scimark_lu                 | 140 ms                                                                | 184 ms: 1.31x slower                                                     |
| genshi_xml                 | 62.2 ms                                                               | 82.6 ms: 1.33x slower                                                    |
| async_generators           | 378 ms                                                                | 522 ms: 1.38x slower                                                     |
| python_startup_no_site     | 7.35 ms                                                               | 11.1 ms: 1.51x slower                                                    |
| python_startup             | 10.2 ms                                                               | 15.5 ms: 1.52x slower                                                    |
| Geometric mean             | (ref)                                                                 | 1.03x slower                                                             |

Benchmark hidden because not significant (7): xml_etree_iterparse, unpickle_pure_python, sqlglot_transpile, pickle_dict, deepcopy_memo, float, tornado_http
Ignored benchmarks (2) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.88% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.14x