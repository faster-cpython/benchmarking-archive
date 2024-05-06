# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a2
- machine: linux-aarch64
- commit hash: 9c4347e
- commit date: 2023-11-22
- overall geometric mean: 1.05x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.01x faster
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20231122-arminc-aarch64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 303 ms: 1.01x slower                                         |
| chameleon      | 8.29 ms                                                               | 8.96 ms: 1.08x slower                                        |
| docutils       | 2.92 sec                                                              | 2.88 sec: 1.02x faster                                       |
| tornado_http   | 140 ms                                                                | 135 ms: 1.03x faster                                         |
| Geometric mean | (ref)                                                                 | 1.01x slower                                                 |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20231122-arminc-aarch64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 572 ms: 1.23x faster                                         |
| async_tree_memoization     | 872 ms                                                                | 736 ms: 1.19x faster                                         |
| async_tree_io              | 1.61 sec                                                              | 1.44 sec: 1.11x faster                                       |
| async_tree_memoization_tg  | 828 ms                                                                | 763 ms: 1.09x faster                                         |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 882 ms: 1.08x faster                                         |
| async_tree_none_tg         | 620 ms                                                                | 590 ms: 1.05x faster                                         |
| async_tree_io_tg           | 1.54 sec                                                              | 1.47 sec: 1.04x faster                                       |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 907 ms: 1.02x faster                                         |
| Geometric mean             | (ref)                                                                 | 1.10x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20231122-arminc-aarch64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| nbody          | 113 ms                                                                | 105 ms: 1.07x faster                                         |
| pidigits       | 242 ms                                                                | 234 ms: 1.03x faster                                         |
| float          | 89.6 ms                                                               | 90.6 ms: 1.01x slower                                        |
| Geometric mean | (ref)                                                                 | 1.03x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20231122-arminc-aarch64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 137 ms                                                                | 129 ms: 1.06x faster                                         |
| regex_dna      | 239 ms                                                                | 246 ms: 1.03x slower                                         |
| regex_v8       | 29.1 ms                                                               | 30.0 ms: 1.03x slower                                        |
| regex_effbot   | 4.25 ms                                                               | 4.61 ms: 1.08x slower                                        |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20231122-arminc-aarch64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 12.4 ms: 1.24x faster                                        |
| unpickle_list        | 6.86 us                                                               | 6.12 us: 1.12x faster                                        |
| unpickle_pure_python | 278 us                                                                | 253 us: 1.10x faster                                         |
| pickle_pure_python   | 374 us                                                                | 346 us: 1.08x faster                                         |
| xml_etree_parse      | 209 ms                                                                | 196 ms: 1.07x faster                                         |
| tomli_loads          | 2.62 sec                                                              | 2.57 sec: 1.02x faster                                       |
| xml_etree_iterparse  | 152 ms                                                                | 149 ms: 1.02x faster                                         |
| pickle_dict          | 37.6 us                                                               | 37.5 us: 1.00x faster                                        |
| json_loads           | 30.3 us                                                               | 30.8 us: 1.02x slower                                        |
| pickle_list          | 5.01 us                                                               | 5.19 us: 1.04x slower                                        |
| xml_etree_process    | 76.1 ms                                                               | 79.5 ms: 1.05x slower                                        |
| pickle               | 12.8 us                                                               | 13.5 us: 1.05x slower                                        |
| xml_etree_generate   | 104 ms                                                                | 113 ms: 1.09x slower                                         |
| unpickle             | 16.9 us                                                               | 18.7 us: 1.11x slower                                        |
| Geometric mean       | (ref)                                                                 | 1.02x faster                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20231122-arminc-aarch64-python-v3.13.0a2-3.13.0a2-9c4347e |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 10.2 ms                                                               | 12.6 ms: 1.23x slower                                        |
| python_startup_no_site | 7.35 ms                                                               | 10.9 ms: 1.48x slower                                        |
| Geometric mean         | (ref)                                                                 | 1.35x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20231122-arminc-aarch64-python-v3.13.0a2-3.13.0a2-9c4347e |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| mako            | 13.3 ms                                                               | 12.8 ms: 1.03x faster                                        |
| genshi_xml      | 62.2 ms                                                               | 60.7 ms: 1.03x faster                                        |
| django_template | 41.8 ms                                                               | 40.9 ms: 1.02x faster                                        |
| genshi_text     | 28.2 ms                                                               | 27.9 ms: 1.01x faster                                        |
| Geometric mean  | (ref)                                                                 | 1.02x faster                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20231122-arminc-aarch64-python-v3.13.0a2-3.13.0a2-9c4347e |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 138 us: 4.72x faster                                         |
| asyncio_tcp                | 920 ms                                                                | 551 ms: 1.67x faster                                         |
| generators                 | 64.2 ms                                                               | 39.5 ms: 1.63x faster                                        |
| comprehensions             | 29.0 us                                                               | 19.7 us: 1.47x faster                                        |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.21 sec: 1.44x faster                                       |
| json_dumps                 | 15.4 ms                                                               | 12.4 ms: 1.24x faster                                        |
| async_tree_none            | 701 ms                                                                | 572 ms: 1.23x faster                                         |
| sqlglot_parse              | 1.65 ms                                                               | 1.37 ms: 1.21x faster                                        |
| sympy_sum                  | 168 ms                                                                | 140 ms: 1.20x faster                                         |
| deltablue                  | 4.75 ms                                                               | 4.00 ms: 1.19x faster                                        |
| async_tree_memoization     | 872 ms                                                                | 736 ms: 1.19x faster                                         |
| pylint                     | 397 ms                                                                | 336 ms: 1.18x faster                                         |
| chaos                      | 78.8 ms                                                               | 66.9 ms: 1.18x faster                                        |
| raytrace                   | 351 ms                                                                | 299 ms: 1.17x faster                                         |
| sqlglot_transpile          | 2.00 ms                                                               | 1.72 ms: 1.16x faster                                        |
| richards_super             | 70.2 ms                                                               | 60.7 ms: 1.16x faster                                        |
| coroutines                 | 33.3 ms                                                               | 29.2 ms: 1.14x faster                                        |
| sympy_integrate            | 23.2 ms                                                               | 20.4 ms: 1.13x faster                                        |
| sympy_str                  | 295 ms                                                                | 260 ms: 1.13x faster                                         |
| unpickle_list              | 6.86 us                                                               | 6.12 us: 1.12x faster                                        |
| crypto_pyaes               | 86.5 ms                                                               | 77.5 ms: 1.12x faster                                        |
| richards                   | 58.1 ms                                                               | 52.2 ms: 1.11x faster                                        |
| async_tree_io              | 1.61 sec                                                              | 1.44 sec: 1.11x faster                                       |
| unpickle_pure_python       | 278 us                                                                | 253 us: 1.10x faster                                         |
| async_tree_memoization_tg  | 828 ms                                                                | 763 ms: 1.09x faster                                         |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 882 ms: 1.08x faster                                         |
| pickle_pure_python         | 374 us                                                                | 346 us: 1.08x faster                                         |
| bench_mp_pool              | 7.44 ms                                                               | 6.91 ms: 1.08x faster                                        |
| hexiom                     | 7.57 ms                                                               | 7.03 ms: 1.08x faster                                        |
| sympy_expand               | 482 ms                                                                | 448 ms: 1.08x faster                                         |
| nbody                      | 113 ms                                                                | 105 ms: 1.07x faster                                         |
| sqlglot_normalize          | 132 ms                                                                | 123 ms: 1.07x faster                                         |
| xml_etree_parse            | 209 ms                                                                | 196 ms: 1.07x faster                                         |
| logging_simple             | 7.57 us                                                               | 7.12 us: 1.06x faster                                        |
| dulwich_log                | 63.2 ms                                                               | 59.4 ms: 1.06x faster                                        |
| logging_format             | 8.22 us                                                               | 7.74 us: 1.06x faster                                        |
| regex_compile              | 137 ms                                                                | 129 ms: 1.06x faster                                         |
| async_tree_none_tg         | 620 ms                                                                | 590 ms: 1.05x faster                                         |
| nqueens                    | 102 ms                                                                | 97.6 ms: 1.05x faster                                        |
| sqlglot_optimize           | 63.4 ms                                                               | 60.6 ms: 1.05x faster                                        |
| async_tree_io_tg           | 1.54 sec                                                              | 1.47 sec: 1.04x faster                                       |
| bench_thread_pool          | 1.36 ms                                                               | 1.31 ms: 1.04x faster                                        |
| pathlib                    | 24.8 ms                                                               | 23.9 ms: 1.04x faster                                        |
| pidigits                   | 242 ms                                                                | 234 ms: 1.03x faster                                         |
| mako                       | 13.3 ms                                                               | 12.8 ms: 1.03x faster                                        |
| tornado_http               | 140 ms                                                                | 135 ms: 1.03x faster                                         |
| scimark_monte_carlo        | 83.2 ms                                                               | 81.1 ms: 1.03x faster                                        |
| genshi_xml                 | 62.2 ms                                                               | 60.7 ms: 1.03x faster                                        |
| django_template            | 41.8 ms                                                               | 40.9 ms: 1.02x faster                                        |
| logging_silent             | 133 ns                                                                | 130 ns: 1.02x faster                                         |
| spectral_norm              | 131 ms                                                                | 129 ms: 1.02x faster                                         |
| go                         | 163 ms                                                                | 160 ms: 1.02x faster                                         |
| tomli_loads                | 2.62 sec                                                              | 2.57 sec: 1.02x faster                                       |
| aiohttp                    | 1.13 ms                                                               | 1.11 ms: 1.02x faster                                        |
| deepcopy_memo              | 49.0 us                                                               | 48.2 us: 1.02x faster                                        |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 907 ms: 1.02x faster                                         |
| xml_etree_iterparse        | 152 ms                                                                | 149 ms: 1.02x faster                                         |
| docutils                   | 2.92 sec                                                              | 2.88 sec: 1.02x faster                                       |
| meteor_contest             | 115 ms                                                                | 114 ms: 1.01x faster                                         |
| genshi_text                | 28.2 ms                                                               | 27.9 ms: 1.01x faster                                        |
| mdp                        | 3.35 sec                                                              | 3.33 sec: 1.01x faster                                       |
| json                       | 5.52 ms                                                               | 5.49 ms: 1.01x faster                                        |
| deepcopy                   | 435 us                                                                | 433 us: 1.00x faster                                         |
| pickle_dict                | 37.6 us                                                               | 37.5 us: 1.00x faster                                        |
| scimark_lu                 | 140 ms                                                                | 141 ms: 1.00x slower                                         |
| 2to3                       | 300 ms                                                                | 303 ms: 1.01x slower                                         |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.34 ms: 1.01x slower                                        |
| deepcopy_reduce            | 3.89 us                                                               | 3.93 us: 1.01x slower                                        |
| float                      | 89.6 ms                                                               | 90.6 ms: 1.01x slower                                        |
| pprint_pformat             | 1.85 sec                                                              | 1.88 sec: 1.01x slower                                       |
| thrift                     | 910 us                                                                | 923 us: 1.01x slower                                         |
| fannkuch                   | 451 ms                                                                | 458 ms: 1.01x slower                                         |
| pprint_safe_repr           | 903 ms                                                                | 916 ms: 1.01x slower                                         |
| json_loads                 | 30.3 us                                                               | 30.8 us: 1.02x slower                                        |
| gc_traversal               | 4.33 ms                                                               | 4.44 ms: 1.02x slower                                        |
| regex_dna                  | 239 ms                                                                | 246 ms: 1.03x slower                                         |
| regex_v8                   | 29.1 ms                                                               | 30.0 ms: 1.03x slower                                        |
| pickle_list                | 5.01 us                                                               | 5.19 us: 1.04x slower                                        |
| xml_etree_process          | 76.1 ms                                                               | 79.5 ms: 1.05x slower                                        |
| pickle                     | 12.8 us                                                               | 13.5 us: 1.05x slower                                        |
| sqlite_synth               | 3.56 us                                                               | 3.77 us: 1.06x slower                                        |
| scimark_fft                | 402 ms                                                                | 428 ms: 1.06x slower                                         |
| chameleon                  | 8.29 ms                                                               | 8.96 ms: 1.08x slower                                        |
| regex_effbot               | 4.25 ms                                                               | 4.61 ms: 1.08x slower                                        |
| xml_etree_generate         | 104 ms                                                                | 113 ms: 1.09x slower                                         |
| flaskblogging              | 4.19 ms                                                               | 4.57 ms: 1.09x slower                                        |
| pyflate                    | 516 ms                                                                | 565 ms: 1.09x slower                                         |
| unpickle                   | 16.9 us                                                               | 18.7 us: 1.11x slower                                        |
| scimark_sor                | 145 ms                                                                | 162 ms: 1.12x slower                                         |
| coverage                   | 84.1 ms                                                               | 99.8 ms: 1.19x slower                                        |
| mypy2                      | 737 ms                                                                | 892 ms: 1.21x slower                                         |
| python_startup             | 10.2 ms                                                               | 12.6 ms: 1.23x slower                                        |
| telco                      | 7.80 ms                                                               | 9.69 ms: 1.24x slower                                        |
| async_generators           | 378 ms                                                                | 480 ms: 1.27x slower                                         |
| python_startup_no_site     | 7.35 ms                                                               | 10.9 ms: 1.48x slower                                        |
| Geometric mean             | (ref)                                                                 | 1.05x faster                                                 |

Benchmark hidden because not significant (5): asyncio_websockets, gunicorn, html5lib, create_gc_cycles, pycparser
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 0.98x