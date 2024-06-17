# Results vs. 3.11.0

- fork: python
- ref: v3.13.0b2
- machine: linux-aarch64
- commit hash: 3a83b17
- commit date: 2024-06-05
- overall geometric mean: 1.05x faster
- HPT reliability: 99.80%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 305 ms: 1.02x slower                                         |
| chameleon      | 8.29 ms                                                               | 8.95 ms: 1.08x slower                                        |
| docutils       | 2.92 sec                                                              | 3.10 sec: 1.06x slower                                       |
| tornado_http   | 140 ms                                                                | 128 ms: 1.09x faster                                         |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                 |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 492 ms: 1.42x faster                                         |
| async_tree_memoization_tg  | 828 ms                                                                | 604 ms: 1.37x faster                                         |
| async_tree_memoization     | 872 ms                                                                | 645 ms: 1.35x faster                                         |
| async_tree_io              | 1.61 sec                                                              | 1.22 sec: 1.31x faster                                       |
| async_tree_none_tg         | 620 ms                                                                | 476 ms: 1.30x faster                                         |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 763 ms: 1.21x faster                                         |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 791 ms: 1.21x faster                                         |
| async_tree_io_tg           | 1.54 sec                                                              | 1.27 sec: 1.21x faster                                       |
| Geometric mean             | (ref)                                                                 | 1.30x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 234 ms: 1.03x faster                                         |
| nbody          | 113 ms                                                                | 114 ms: 1.01x slower                                         |
| float          | 89.6 ms                                                               | 91.4 ms: 1.02x slower                                        |
| Geometric mean | (ref)                                                                 | 1.00x slower                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 137 ms                                                                | 128 ms: 1.07x faster                                         |
| regex_v8       | 29.1 ms                                                               | 31.1 ms: 1.07x slower                                        |
| regex_dna      | 239 ms                                                                | 259 ms: 1.08x slower                                         |
| regex_effbot   | 4.25 ms                                                               | 4.98 ms: 1.17x slower                                        |
| Geometric mean | (ref)                                                                 | 1.06x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 13.1 ms: 1.18x faster                                        |
| unpickle_pure_python | 278 us                                                                | 251 us: 1.11x faster                                         |
| xml_etree_parse      | 209 ms                                                                | 191 ms: 1.09x faster                                         |
| unpickle_list        | 6.86 us                                                               | 6.52 us: 1.05x faster                                        |
| pickle_pure_python   | 374 us                                                                | 359 us: 1.04x faster                                         |
| xml_etree_iterparse  | 152 ms                                                                | 147 ms: 1.04x faster                                         |
| tomli_loads          | 2.62 sec                                                              | 2.57 sec: 1.02x faster                                       |
| pickle               | 12.8 us                                                               | 13.4 us: 1.05x slower                                        |
| pickle_list          | 5.01 us                                                               | 5.27 us: 1.05x slower                                        |
| json_loads           | 30.3 us                                                               | 32.1 us: 1.06x slower                                        |
| xml_etree_process    | 76.1 ms                                                               | 80.8 ms: 1.06x slower                                        |
| xml_etree_generate   | 104 ms                                                                | 114 ms: 1.09x slower                                         |
| unpickle             | 16.9 us                                                               | 19.8 us: 1.17x slower                                        |
| Geometric mean       | (ref)                                                                 | 1.00x faster                                                 |

Benchmark hidden because not significant (1): pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 8.60 ms: 1.17x slower                                        |
| python_startup         | 10.2 ms                                                               | 13.0 ms: 1.27x slower                                        |
| Geometric mean         | (ref)                                                                 | 1.22x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_xml      | 62.2 ms                                                               | 60.4 ms: 1.03x faster                                        |
| genshi_text     | 28.2 ms                                                               | 27.4 ms: 1.03x faster                                        |
| mako            | 13.3 ms                                                               | 13.2 ms: 1.01x faster                                        |
| django_template | 41.8 ms                                                               | 42.3 ms: 1.01x slower                                        |
| Geometric mean  | (ref)                                                                 | 1.01x faster                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 193 us: 3.38x faster                                         |
| generators                 | 64.2 ms                                                               | 37.1 ms: 1.73x faster                                        |
| asyncio_tcp                | 920 ms                                                                | 584 ms: 1.58x faster                                         |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.21 sec: 1.44x faster                                       |
| async_tree_none            | 701 ms                                                                | 492 ms: 1.42x faster                                         |
| comprehensions             | 29.0 us                                                               | 20.5 us: 1.41x faster                                        |
| async_tree_memoization_tg  | 828 ms                                                                | 604 ms: 1.37x faster                                         |
| async_tree_memoization     | 872 ms                                                                | 645 ms: 1.35x faster                                         |
| async_tree_io              | 1.61 sec                                                              | 1.22 sec: 1.31x faster                                       |
| async_tree_none_tg         | 620 ms                                                                | 476 ms: 1.30x faster                                         |
| deltablue                  | 4.75 ms                                                               | 3.88 ms: 1.22x faster                                        |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 763 ms: 1.21x faster                                         |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 791 ms: 1.21x faster                                         |
| async_tree_io_tg           | 1.54 sec                                                              | 1.27 sec: 1.21x faster                                       |
| raytrace                   | 351 ms                                                                | 297 ms: 1.18x faster                                         |
| pylint                     | 397 ms                                                                | 337 ms: 1.18x faster                                         |
| json_dumps                 | 15.4 ms                                                               | 13.1 ms: 1.18x faster                                        |
| sympy_sum                  | 168 ms                                                                | 144 ms: 1.17x faster                                         |
| sqlglot_transpile          | 2.00 ms                                                               | 1.71 ms: 1.17x faster                                        |
| sqlglot_parse              | 1.65 ms                                                               | 1.42 ms: 1.16x faster                                        |
| chaos                      | 78.8 ms                                                               | 68.3 ms: 1.15x faster                                        |
| coroutines                 | 33.3 ms                                                               | 29.0 ms: 1.15x faster                                        |
| richards_super             | 70.2 ms                                                               | 62.3 ms: 1.13x faster                                        |
| sympy_integrate            | 23.2 ms                                                               | 20.9 ms: 1.11x faster                                        |
| sympy_str                  | 295 ms                                                                | 265 ms: 1.11x faster                                         |
| unpickle_pure_python       | 278 us                                                                | 251 us: 1.11x faster                                         |
| xml_etree_parse            | 209 ms                                                                | 191 ms: 1.09x faster                                         |
| tornado_http               | 140 ms                                                                | 128 ms: 1.09x faster                                         |
| pathlib                    | 24.8 ms                                                               | 22.8 ms: 1.09x faster                                        |
| dulwich_log                | 63.2 ms                                                               | 58.5 ms: 1.08x faster                                        |
| bench_thread_pool          | 1.36 ms                                                               | 1.26 ms: 1.08x faster                                        |
| hexiom                     | 7.57 ms                                                               | 7.08 ms: 1.07x faster                                        |
| regex_compile              | 137 ms                                                                | 128 ms: 1.07x faster                                         |
| bench_mp_pool              | 7.44 ms                                                               | 7.03 ms: 1.06x faster                                        |
| crypto_pyaes               | 86.5 ms                                                               | 82.0 ms: 1.06x faster                                        |
| sympy_expand               | 482 ms                                                                | 457 ms: 1.05x faster                                         |
| unpickle_list              | 6.86 us                                                               | 6.52 us: 1.05x faster                                        |
| logging_simple             | 7.57 us                                                               | 7.21 us: 1.05x faster                                        |
| logging_format             | 8.22 us                                                               | 7.82 us: 1.05x faster                                        |
| pickle_pure_python         | 374 us                                                                | 359 us: 1.04x faster                                         |
| richards                   | 58.1 ms                                                               | 55.9 ms: 1.04x faster                                        |
| dask                       | 385 ms                                                                | 370 ms: 1.04x faster                                         |
| nqueens                    | 102 ms                                                                | 98.9 ms: 1.04x faster                                        |
| xml_etree_iterparse        | 152 ms                                                                | 147 ms: 1.04x faster                                         |
| pidigits                   | 242 ms                                                                | 234 ms: 1.03x faster                                         |
| genshi_xml                 | 62.2 ms                                                               | 60.4 ms: 1.03x faster                                        |
| genshi_text                | 28.2 ms                                                               | 27.4 ms: 1.03x faster                                        |
| pycparser                  | 1.25 sec                                                              | 1.22 sec: 1.02x faster                                       |
| tomli_loads                | 2.62 sec                                                              | 2.57 sec: 1.02x faster                                       |
| meteor_contest             | 115 ms                                                                | 113 ms: 1.02x faster                                         |
| go                         | 163 ms                                                                | 161 ms: 1.01x faster                                         |
| scimark_monte_carlo        | 83.2 ms                                                               | 82.3 ms: 1.01x faster                                        |
| mako                       | 13.3 ms                                                               | 13.2 ms: 1.01x faster                                        |
| mdp                        | 3.35 sec                                                              | 3.33 sec: 1.01x faster                                       |
| logging_silent             | 133 ns                                                                | 133 ns: 1.01x slower                                         |
| scimark_lu                 | 140 ms                                                                | 141 ms: 1.01x slower                                         |
| nbody                      | 113 ms                                                                | 114 ms: 1.01x slower                                         |
| django_template            | 41.8 ms                                                               | 42.3 ms: 1.01x slower                                        |
| 2to3                       | 300 ms                                                                | 305 ms: 1.02x slower                                         |
| float                      | 89.6 ms                                                               | 91.4 ms: 1.02x slower                                        |
| json                       | 5.52 ms                                                               | 5.64 ms: 1.02x slower                                        |
| deepcopy                   | 435 us                                                                | 448 us: 1.03x slower                                         |
| pprint_safe_repr           | 903 ms                                                                | 933 ms: 1.03x slower                                         |
| deepcopy_memo              | 49.0 us                                                               | 50.8 us: 1.04x slower                                        |
| deepcopy_reduce            | 3.89 us                                                               | 4.04 us: 1.04x slower                                        |
| pprint_pformat             | 1.85 sec                                                              | 1.93 sec: 1.04x slower                                       |
| mypy2                      | 737 ms                                                                | 767 ms: 1.04x slower                                         |
| aiohttp                    | 1.13 ms                                                               | 1.18 ms: 1.04x slower                                        |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.55 ms: 1.04x slower                                        |
| pickle                     | 12.8 us                                                               | 13.4 us: 1.05x slower                                        |
| pickle_list                | 5.01 us                                                               | 5.27 us: 1.05x slower                                        |
| thrift                     | 910 us                                                                | 962 us: 1.06x slower                                         |
| json_loads                 | 30.3 us                                                               | 32.1 us: 1.06x slower                                        |
| docutils                   | 2.92 sec                                                              | 3.10 sec: 1.06x slower                                       |
| xml_etree_process          | 76.1 ms                                                               | 80.8 ms: 1.06x slower                                        |
| regex_v8                   | 29.1 ms                                                               | 31.1 ms: 1.07x slower                                        |
| spectral_norm              | 131 ms                                                                | 141 ms: 1.08x slower                                         |
| pyflate                    | 516 ms                                                                | 557 ms: 1.08x slower                                         |
| chameleon                  | 8.29 ms                                                               | 8.95 ms: 1.08x slower                                        |
| regex_dna                  | 239 ms                                                                | 259 ms: 1.08x slower                                         |
| xml_etree_generate         | 104 ms                                                                | 114 ms: 1.09x slower                                         |
| scimark_sor                | 145 ms                                                                | 159 ms: 1.10x slower                                         |
| sqlite_synth               | 3.56 us                                                               | 3.90 us: 1.10x slower                                        |
| scimark_fft                | 402 ms                                                                | 445 ms: 1.11x slower                                         |
| flaskblogging              | 4.19 ms                                                               | 4.70 ms: 1.12x slower                                        |
| coverage                   | 84.1 ms                                                               | 98.4 ms: 1.17x slower                                        |
| regex_effbot               | 4.25 ms                                                               | 4.98 ms: 1.17x slower                                        |
| python_startup_no_site     | 7.35 ms                                                               | 8.60 ms: 1.17x slower                                        |
| unpickle                   | 16.9 us                                                               | 19.8 us: 1.17x slower                                        |
| gc_traversal               | 4.33 ms                                                               | 5.17 ms: 1.20x slower                                        |
| create_gc_cycles           | 1.87 ms                                                               | 2.33 ms: 1.25x slower                                        |
| python_startup             | 10.2 ms                                                               | 13.0 ms: 1.27x slower                                        |
| telco                      | 7.80 ms                                                               | 10.0 ms: 1.28x slower                                        |
| async_generators           | 378 ms                                                                | 488 ms: 1.29x slower                                         |
| Geometric mean             | (ref)                                                                 | 1.05x faster                                                 |

Benchmark hidden because not significant (7): sqlglot_normalize, sqlglot_optimize, gunicorn, fannkuch, pickle_dict, asyncio_websockets, html5lib
Ignored benchmarks (2) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (1) of results/bm-20240605-3.13.0b2-3a83b17/bm-20240605-arminc-aarch64-python-v3.13.0b2-3.13.0b2-3a83b17.json: bpe_tokeniser

# HPT report

- Reliability score: 99.80% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x