# Results vs. 3.11.0

- fork: python
- ref: v3.13.0b2
- machine: linux-aarch64
- commit hash: 3a83b17
- commit date: 2024-06-05
- overall geometric mean: 1.03x slower
- HPT reliability: 99.82%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 360 ms: 1.20x slower                                         |
| chameleon      | 8.29 ms                                                               | 9.18 ms: 1.11x slower                                        |
| docutils       | 2.92 sec                                                              | 3.52 sec: 1.21x slower                                       |
| html5lib       | 65.3 ms                                                               | 71.7 ms: 1.10x slower                                        |
| Geometric mean | (ref)                                                                 | 1.12x slower                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 508 ms: 1.38x faster                                         |
| async_tree_memoization_tg  | 828 ms                                                                | 620 ms: 1.34x faster                                         |
| async_tree_memoization     | 872 ms                                                                | 671 ms: 1.30x faster                                         |
| async_tree_io              | 1.61 sec                                                              | 1.25 sec: 1.29x faster                                       |
| async_tree_none_tg         | 620 ms                                                                | 485 ms: 1.28x faster                                         |
| async_tree_io_tg           | 1.54 sec                                                              | 1.23 sec: 1.25x faster                                       |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 818 ms: 1.17x faster                                         |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 806 ms: 1.14x faster                                         |
| Geometric mean             | (ref)                                                                 | 1.27x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 235 ms: 1.03x faster                                         |
| float          | 89.6 ms                                                               | 88.7 ms: 1.01x faster                                        |
| nbody          | 113 ms                                                                | 116 ms: 1.03x slower                                         |
| Geometric mean | (ref)                                                                 | 1.00x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_dna      | 239 ms                                                                | 247 ms: 1.03x slower                                         |
| regex_v8       | 29.1 ms                                                               | 30.4 ms: 1.04x slower                                        |
| regex_effbot   | 4.25 ms                                                               | 4.86 ms: 1.14x slower                                        |
| regex_compile  | 137 ms                                                                | 175 ms: 1.28x slower                                         |
| Geometric mean | (ref)                                                                 | 1.12x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|---------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| json_dumps          | 15.4 ms                                                               | 13.3 ms: 1.16x faster                                        |
| xml_etree_parse     | 209 ms                                                                | 188 ms: 1.11x faster                                         |
| unpickle_list       | 6.86 us                                                               | 6.58 us: 1.04x faster                                        |
| xml_etree_iterparse | 152 ms                                                                | 148 ms: 1.02x faster                                         |
| tomli_loads         | 2.62 sec                                                              | 2.64 sec: 1.01x slower                                       |
| xml_etree_process   | 76.1 ms                                                               | 80.3 ms: 1.05x slower                                        |
| pickle_list         | 5.01 us                                                               | 5.30 us: 1.06x slower                                        |
| pickle              | 12.8 us                                                               | 13.5 us: 1.06x slower                                        |
| json_loads          | 30.3 us                                                               | 32.1 us: 1.06x slower                                        |
| pickle_pure_python  | 374 us                                                                | 398 us: 1.07x slower                                         |
| xml_etree_generate  | 104 ms                                                                | 114 ms: 1.10x slower                                         |
| unpickle            | 16.9 us                                                               | 19.7 us: 1.17x slower                                        |
| Geometric mean      | (ref)                                                                 | 1.02x slower                                                 |

Benchmark hidden because not significant (2): unpickle_pure_python, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 10.9 ms: 1.48x slower                                        |
| python_startup         | 10.2 ms                                                               | 15.3 ms: 1.50x slower                                        |
| Geometric mean         | (ref)                                                                 | 1.49x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| mako            | 13.3 ms                                                               | 13.0 ms: 1.02x faster                                        |
| django_template | 41.8 ms                                                               | 49.6 ms: 1.19x slower                                        |
| genshi_text     | 28.2 ms                                                               | 35.4 ms: 1.26x slower                                        |
| genshi_xml      | 62.2 ms                                                               | 83.4 ms: 1.34x slower                                        |
| Geometric mean  | (ref)                                                                 | 1.18x slower                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 207 us: 3.16x faster                                         |
| generators                 | 64.2 ms                                                               | 39.6 ms: 1.62x faster                                        |
| asyncio_tcp                | 920 ms                                                                | 618 ms: 1.49x faster                                         |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.25 sec: 1.42x faster                                       |
| async_tree_none            | 701 ms                                                                | 508 ms: 1.38x faster                                         |
| async_tree_memoization_tg  | 828 ms                                                                | 620 ms: 1.34x faster                                         |
| async_tree_memoization     | 872 ms                                                                | 671 ms: 1.30x faster                                         |
| async_tree_io              | 1.61 sec                                                              | 1.25 sec: 1.29x faster                                       |
| async_tree_none_tg         | 620 ms                                                                | 485 ms: 1.28x faster                                         |
| async_tree_io_tg           | 1.54 sec                                                              | 1.23 sec: 1.25x faster                                       |
| comprehensions             | 29.0 us                                                               | 23.2 us: 1.25x faster                                        |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 818 ms: 1.17x faster                                         |
| json_dumps                 | 15.4 ms                                                               | 13.3 ms: 1.16x faster                                        |
| coroutines                 | 33.3 ms                                                               | 28.8 ms: 1.16x faster                                        |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 806 ms: 1.14x faster                                         |
| xml_etree_parse            | 209 ms                                                                | 188 ms: 1.11x faster                                         |
| richards_super             | 70.2 ms                                                               | 63.4 ms: 1.11x faster                                        |
| raytrace                   | 351 ms                                                                | 321 ms: 1.09x faster                                         |
| pathlib                    | 24.8 ms                                                               | 23.2 ms: 1.07x faster                                        |
| unpickle_list              | 6.86 us                                                               | 6.58 us: 1.04x faster                                        |
| sqlglot_parse              | 1.65 ms                                                               | 1.58 ms: 1.04x faster                                        |
| deltablue                  | 4.75 ms                                                               | 4.58 ms: 1.04x faster                                        |
| logging_simple             | 7.57 us                                                               | 7.31 us: 1.04x faster                                        |
| richards                   | 58.1 ms                                                               | 56.2 ms: 1.03x faster                                        |
| pidigits                   | 242 ms                                                                | 235 ms: 1.03x faster                                         |
| bench_thread_pool          | 1.36 ms                                                               | 1.32 ms: 1.03x faster                                        |
| xml_etree_iterparse        | 152 ms                                                                | 148 ms: 1.02x faster                                         |
| mako                       | 13.3 ms                                                               | 13.0 ms: 1.02x faster                                        |
| logging_format             | 8.22 us                                                               | 8.05 us: 1.02x faster                                        |
| float                      | 89.6 ms                                                               | 88.7 ms: 1.01x faster                                        |
| asyncio_websockets         | 656 ms                                                                | 659 ms: 1.01x slower                                         |
| tomli_loads                | 2.62 sec                                                              | 2.64 sec: 1.01x slower                                       |
| deepcopy_memo              | 49.0 us                                                               | 49.7 us: 1.01x slower                                        |
| meteor_contest             | 115 ms                                                                | 118 ms: 1.02x slower                                         |
| dask                       | 385 ms                                                                | 393 ms: 1.02x slower                                         |
| mdp                        | 3.35 sec                                                              | 3.44 sec: 1.02x slower                                       |
| fannkuch                   | 451 ms                                                                | 463 ms: 1.03x slower                                         |
| nbody                      | 113 ms                                                                | 116 ms: 1.03x slower                                         |
| crypto_pyaes               | 86.5 ms                                                               | 89.1 ms: 1.03x slower                                        |
| regex_dna                  | 239 ms                                                                | 247 ms: 1.03x slower                                         |
| json                       | 5.52 ms                                                               | 5.74 ms: 1.04x slower                                        |
| regex_v8                   | 29.1 ms                                                               | 30.4 ms: 1.04x slower                                        |
| xml_etree_process          | 76.1 ms                                                               | 80.3 ms: 1.05x slower                                        |
| pickle_list                | 5.01 us                                                               | 5.30 us: 1.06x slower                                        |
| pickle                     | 12.8 us                                                               | 13.5 us: 1.06x slower                                        |
| json_loads                 | 30.3 us                                                               | 32.1 us: 1.06x slower                                        |
| thrift                     | 910 us                                                                | 965 us: 1.06x slower                                         |
| sqlite_synth               | 3.56 us                                                               | 3.78 us: 1.06x slower                                        |
| logging_silent             | 133 ns                                                                | 141 ns: 1.06x slower                                         |
| pickle_pure_python         | 374 us                                                                | 398 us: 1.07x slower                                         |
| scimark_monte_carlo        | 83.2 ms                                                               | 89.0 ms: 1.07x slower                                        |
| pycparser                  | 1.25 sec                                                              | 1.35 sec: 1.08x slower                                       |
| sympy_sum                  | 168 ms                                                                | 183 ms: 1.09x slower                                         |
| sympy_str                  | 295 ms                                                                | 321 ms: 1.09x slower                                         |
| sqlglot_normalize          | 132 ms                                                                | 144 ms: 1.09x slower                                         |
| xml_etree_generate         | 104 ms                                                                | 114 ms: 1.10x slower                                         |
| html5lib                   | 65.3 ms                                                               | 71.7 ms: 1.10x slower                                        |
| sqlglot_optimize           | 63.4 ms                                                               | 69.8 ms: 1.10x slower                                        |
| go                         | 163 ms                                                                | 180 ms: 1.10x slower                                         |
| sympy_integrate            | 23.2 ms                                                               | 25.5 ms: 1.10x slower                                        |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.94 ms: 1.10x slower                                        |
| chaos                      | 78.8 ms                                                               | 87.1 ms: 1.10x slower                                        |
| chameleon                  | 8.29 ms                                                               | 9.18 ms: 1.11x slower                                        |
| bench_mp_pool              | 7.44 ms                                                               | 8.24 ms: 1.11x slower                                        |
| sympy_expand               | 482 ms                                                                | 538 ms: 1.12x slower                                         |
| dulwich_log                | 63.2 ms                                                               | 71.0 ms: 1.12x slower                                        |
| aiohttp                    | 1.13 ms                                                               | 1.28 ms: 1.13x slower                                        |
| spectral_norm              | 131 ms                                                                | 149 ms: 1.14x slower                                         |
| scimark_fft                | 402 ms                                                                | 459 ms: 1.14x slower                                         |
| regex_effbot               | 4.25 ms                                                               | 4.86 ms: 1.14x slower                                        |
| nqueens                    | 102 ms                                                                | 117 ms: 1.14x slower                                         |
| gunicorn                   | 1.19 ms                                                               | 1.36 ms: 1.14x slower                                        |
| deepcopy                   | 435 us                                                                | 502 us: 1.15x slower                                         |
| pyflate                    | 516 ms                                                                | 596 ms: 1.16x slower                                         |
| coverage                   | 84.1 ms                                                               | 98.1 ms: 1.17x slower                                        |
| unpickle                   | 16.9 us                                                               | 19.7 us: 1.17x slower                                        |
| gc_traversal               | 4.33 ms                                                               | 5.08 ms: 1.17x slower                                        |
| hexiom                     | 7.57 ms                                                               | 8.89 ms: 1.17x slower                                        |
| django_template            | 41.8 ms                                                               | 49.6 ms: 1.19x slower                                        |
| scimark_sor                | 145 ms                                                                | 174 ms: 1.19x slower                                         |
| 2to3                       | 300 ms                                                                | 360 ms: 1.20x slower                                         |
| deepcopy_reduce            | 3.89 us                                                               | 4.68 us: 1.20x slower                                        |
| docutils                   | 2.92 sec                                                              | 3.52 sec: 1.21x slower                                       |
| pprint_safe_repr           | 903 ms                                                                | 1.11 sec: 1.23x slower                                       |
| flaskblogging              | 4.19 ms                                                               | 5.16 ms: 1.23x slower                                        |
| pprint_pformat             | 1.85 sec                                                              | 2.31 sec: 1.25x slower                                       |
| genshi_text                | 28.2 ms                                                               | 35.4 ms: 1.26x slower                                        |
| mypy2                      | 737 ms                                                                | 929 ms: 1.26x slower                                         |
| create_gc_cycles           | 1.87 ms                                                               | 2.38 ms: 1.27x slower                                        |
| regex_compile              | 137 ms                                                                | 175 ms: 1.28x slower                                         |
| telco                      | 7.80 ms                                                               | 10.1 ms: 1.30x slower                                        |
| scimark_lu                 | 140 ms                                                                | 183 ms: 1.30x slower                                         |
| genshi_xml                 | 62.2 ms                                                               | 83.4 ms: 1.34x slower                                        |
| async_generators           | 378 ms                                                                | 508 ms: 1.34x slower                                         |
| python_startup_no_site     | 7.35 ms                                                               | 10.9 ms: 1.48x slower                                        |
| python_startup             | 10.2 ms                                                               | 15.3 ms: 1.50x slower                                        |
| Geometric mean             | (ref)                                                                 | 1.03x slower                                                 |

Benchmark hidden because not significant (5): tornado_http, unpickle_pure_python, pickle_dict, sqlglot_transpile, pylint
Ignored benchmarks (2) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17-JIT/bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser

# HPT report

- Reliability score: 99.82% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.13x