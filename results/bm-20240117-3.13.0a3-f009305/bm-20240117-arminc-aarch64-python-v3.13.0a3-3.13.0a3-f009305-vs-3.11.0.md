# Results vs. 3.11.0

- fork: python
- ref: v3.13.0a3
- machine: linux-aarch64
- commit hash: f009305
- commit date: 2024-01-17
- overall geometric mean: 1.05x faster
- HPT reliability: 99.87%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240117-arminc-aarch64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 305 ms: 1.02x slower                                         |
| chameleon      | 8.29 ms                                                               | 8.98 ms: 1.08x slower                                        |
| docutils       | 2.92 sec                                                              | 2.90 sec: 1.01x faster                                       |
| tornado_http   | 140 ms                                                                | 137 ms: 1.02x faster                                         |
| Geometric mean | (ref)                                                                 | 1.02x slower                                                 |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240117-arminc-aarch64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 582 ms: 1.20x faster                                         |
| async_tree_memoization     | 872 ms                                                                | 745 ms: 1.17x faster                                         |
| async_tree_memoization_tg  | 828 ms                                                                | 736 ms: 1.13x faster                                         |
| async_tree_io              | 1.61 sec                                                              | 1.45 sec: 1.11x faster                                       |
| async_tree_none_tg         | 620 ms                                                                | 574 ms: 1.08x faster                                         |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 888 ms: 1.08x faster                                         |
| async_tree_io_tg           | 1.54 sec                                                              | 1.44 sec: 1.07x faster                                       |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 895 ms: 1.03x faster                                         |
| Geometric mean             | (ref)                                                                 | 1.11x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240117-arminc-aarch64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| nbody          | 113 ms                                                                | 104 ms: 1.08x faster                                         |
| pidigits       | 242 ms                                                                | 233 ms: 1.04x faster                                         |
| float          | 89.6 ms                                                               | 91.0 ms: 1.02x slower                                        |
| Geometric mean | (ref)                                                                 | 1.03x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240117-arminc-aarch64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 137 ms                                                                | 125 ms: 1.09x faster                                         |
| regex_v8       | 29.1 ms                                                               | 30.1 ms: 1.04x slower                                        |
| regex_dna      | 239 ms                                                                | 255 ms: 1.07x slower                                         |
| regex_effbot   | 4.25 ms                                                               | 4.65 ms: 1.09x slower                                        |
| Geometric mean | (ref)                                                                 | 1.03x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240117-arminc-aarch64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 12.5 ms: 1.24x faster                                        |
| unpickle_pure_python | 278 us                                                                | 256 us: 1.09x faster                                         |
| pickle_pure_python   | 374 us                                                                | 347 us: 1.08x faster                                         |
| unpickle_list        | 6.86 us                                                               | 6.45 us: 1.06x faster                                        |
| xml_etree_parse      | 209 ms                                                                | 206 ms: 1.01x faster                                         |
| tomli_loads          | 2.62 sec                                                              | 2.59 sec: 1.01x faster                                       |
| pickle_dict          | 37.6 us                                                               | 37.3 us: 1.01x faster                                        |
| json_loads           | 30.3 us                                                               | 31.1 us: 1.03x slower                                        |
| pickle               | 12.8 us                                                               | 13.4 us: 1.05x slower                                        |
| pickle_list          | 5.01 us                                                               | 5.28 us: 1.05x slower                                        |
| xml_etree_process    | 76.1 ms                                                               | 80.2 ms: 1.05x slower                                        |
| xml_etree_generate   | 104 ms                                                                | 114 ms: 1.10x slower                                         |
| unpickle             | 16.9 us                                                               | 19.6 us: 1.16x slower                                        |
| Geometric mean       | (ref)                                                                 | 1.00x faster                                                 |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240117-arminc-aarch64-python-v3.13.0a3-3.13.0a3-f009305 |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 10.2 ms                                                               | 12.1 ms: 1.18x slower                                        |
| python_startup_no_site | 7.35 ms                                                               | 10.3 ms: 1.40x slower                                        |
| Geometric mean         | (ref)                                                                 | 1.29x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240117-arminc-aarch64-python-v3.13.0a3-3.13.0a3-f009305 |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_text     | 28.2 ms                                                               | 27.3 ms: 1.03x faster                                        |
| mako            | 13.3 ms                                                               | 12.9 ms: 1.03x faster                                        |
| django_template | 41.8 ms                                                               | 40.7 ms: 1.03x faster                                        |
| genshi_xml      | 62.2 ms                                                               | 60.8 ms: 1.02x faster                                        |
| Geometric mean  | (ref)                                                                 | 1.03x faster                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240117-arminc-aarch64-python-v3.13.0a3-3.13.0a3-f009305 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 135 us: 4.85x faster                                         |
| generators                 | 64.2 ms                                                               | 36.0 ms: 1.78x faster                                        |
| asyncio_tcp                | 920 ms                                                                | 562 ms: 1.64x faster                                         |
| comprehensions             | 29.0 us                                                               | 19.8 us: 1.47x faster                                        |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.22 sec: 1.44x faster                                       |
| json_dumps                 | 15.4 ms                                                               | 12.5 ms: 1.24x faster                                        |
| sympy_sum                  | 168 ms                                                                | 139 ms: 1.21x faster                                         |
| sqlglot_parse              | 1.65 ms                                                               | 1.36 ms: 1.21x faster                                        |
| async_tree_none            | 701 ms                                                                | 582 ms: 1.20x faster                                         |
| pylint                     | 397 ms                                                                | 333 ms: 1.19x faster                                         |
| deltablue                  | 4.75 ms                                                               | 3.98 ms: 1.19x faster                                        |
| raytrace                   | 351 ms                                                                | 296 ms: 1.18x faster                                         |
| chaos                      | 78.8 ms                                                               | 66.7 ms: 1.18x faster                                        |
| async_tree_memoization     | 872 ms                                                                | 745 ms: 1.17x faster                                         |
| sqlglot_transpile          | 2.00 ms                                                               | 1.72 ms: 1.16x faster                                        |
| richards_super             | 70.2 ms                                                               | 60.9 ms: 1.15x faster                                        |
| sympy_str                  | 295 ms                                                                | 259 ms: 1.14x faster                                         |
| coroutines                 | 33.3 ms                                                               | 29.4 ms: 1.13x faster                                        |
| sympy_integrate            | 23.2 ms                                                               | 20.5 ms: 1.13x faster                                        |
| async_tree_memoization_tg  | 828 ms                                                                | 736 ms: 1.13x faster                                         |
| crypto_pyaes               | 86.5 ms                                                               | 77.3 ms: 1.12x faster                                        |
| async_tree_io              | 1.61 sec                                                              | 1.45 sec: 1.11x faster                                       |
| regex_compile              | 137 ms                                                                | 125 ms: 1.09x faster                                         |
| unpickle_pure_python       | 278 us                                                                | 256 us: 1.09x faster                                         |
| nbody                      | 113 ms                                                                | 104 ms: 1.08x faster                                         |
| async_tree_none_tg         | 620 ms                                                                | 574 ms: 1.08x faster                                         |
| pickle_pure_python         | 374 us                                                                | 347 us: 1.08x faster                                         |
| sqlglot_normalize          | 132 ms                                                                | 123 ms: 1.08x faster                                         |
| sympy_expand               | 482 ms                                                                | 448 ms: 1.08x faster                                         |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 888 ms: 1.08x faster                                         |
| async_tree_io_tg           | 1.54 sec                                                              | 1.44 sec: 1.07x faster                                       |
| bench_mp_pool              | 7.44 ms                                                               | 6.98 ms: 1.07x faster                                        |
| unpickle_list              | 6.86 us                                                               | 6.45 us: 1.06x faster                                        |
| nqueens                    | 102 ms                                                                | 96.4 ms: 1.06x faster                                        |
| hexiom                     | 7.57 ms                                                               | 7.14 ms: 1.06x faster                                        |
| richards                   | 58.1 ms                                                               | 55.0 ms: 1.06x faster                                        |
| sqlglot_optimize           | 63.4 ms                                                               | 60.7 ms: 1.04x faster                                        |
| logging_simple             | 7.57 us                                                               | 7.26 us: 1.04x faster                                        |
| pidigits                   | 242 ms                                                                | 233 ms: 1.04x faster                                         |
| bench_thread_pool          | 1.36 ms                                                               | 1.31 ms: 1.04x faster                                        |
| dulwich_log                | 63.2 ms                                                               | 61.3 ms: 1.03x faster                                        |
| genshi_text                | 28.2 ms                                                               | 27.3 ms: 1.03x faster                                        |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 895 ms: 1.03x faster                                         |
| pathlib                    | 24.8 ms                                                               | 24.1 ms: 1.03x faster                                        |
| mako                       | 13.3 ms                                                               | 12.9 ms: 1.03x faster                                        |
| django_template            | 41.8 ms                                                               | 40.7 ms: 1.03x faster                                        |
| logging_format             | 8.22 us                                                               | 8.00 us: 1.03x faster                                        |
| scimark_lu                 | 140 ms                                                                | 137 ms: 1.02x faster                                         |
| genshi_xml                 | 62.2 ms                                                               | 60.8 ms: 1.02x faster                                        |
| meteor_contest             | 115 ms                                                                | 113 ms: 1.02x faster                                         |
| spectral_norm              | 131 ms                                                                | 129 ms: 1.02x faster                                         |
| tornado_http               | 140 ms                                                                | 137 ms: 1.02x faster                                         |
| xml_etree_parse            | 209 ms                                                                | 206 ms: 1.01x faster                                         |
| go                         | 163 ms                                                                | 161 ms: 1.01x faster                                         |
| mdp                        | 3.35 sec                                                              | 3.32 sec: 1.01x faster                                       |
| tomli_loads                | 2.62 sec                                                              | 2.59 sec: 1.01x faster                                       |
| pickle_dict                | 37.6 us                                                               | 37.3 us: 1.01x faster                                        |
| docutils                   | 2.92 sec                                                              | 2.90 sec: 1.01x faster                                       |
| scimark_monte_carlo        | 83.2 ms                                                               | 83.5 ms: 1.00x slower                                        |
| asyncio_websockets         | 656 ms                                                                | 658 ms: 1.00x slower                                         |
| deepcopy_memo              | 49.0 us                                                               | 49.3 us: 1.01x slower                                        |
| gc_traversal               | 4.33 ms                                                               | 4.36 ms: 1.01x slower                                        |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.34 ms: 1.01x slower                                        |
| fannkuch                   | 451 ms                                                                | 456 ms: 1.01x slower                                         |
| json                       | 5.52 ms                                                               | 5.59 ms: 1.01x slower                                        |
| logging_silent             | 133 ns                                                                | 134 ns: 1.01x slower                                         |
| 2to3                       | 300 ms                                                                | 305 ms: 1.02x slower                                         |
| float                      | 89.6 ms                                                               | 91.0 ms: 1.02x slower                                        |
| thrift                     | 910 us                                                                | 925 us: 1.02x slower                                         |
| create_gc_cycles           | 1.87 ms                                                               | 1.91 ms: 1.02x slower                                        |
| pycparser                  | 1.25 sec                                                              | 1.27 sec: 1.02x slower                                       |
| deepcopy                   | 435 us                                                                | 444 us: 1.02x slower                                         |
| json_loads                 | 30.3 us                                                               | 31.1 us: 1.03x slower                                        |
| aiohttp                    | 1.13 ms                                                               | 1.16 ms: 1.03x slower                                        |
| pprint_pformat             | 1.85 sec                                                              | 1.91 sec: 1.03x slower                                       |
| regex_v8                   | 29.1 ms                                                               | 30.1 ms: 1.04x slower                                        |
| pprint_safe_repr           | 903 ms                                                                | 936 ms: 1.04x slower                                         |
| deepcopy_reduce            | 3.89 us                                                               | 4.04 us: 1.04x slower                                        |
| pickle                     | 12.8 us                                                               | 13.4 us: 1.05x slower                                        |
| pickle_list                | 5.01 us                                                               | 5.28 us: 1.05x slower                                        |
| sqlite_synth               | 3.56 us                                                               | 3.75 us: 1.05x slower                                        |
| xml_etree_process          | 76.1 ms                                                               | 80.2 ms: 1.05x slower                                        |
| regex_dna                  | 239 ms                                                                | 255 ms: 1.07x slower                                         |
| scimark_fft                | 402 ms                                                                | 430 ms: 1.07x slower                                         |
| chameleon                  | 8.29 ms                                                               | 8.98 ms: 1.08x slower                                        |
| flaskblogging              | 4.19 ms                                                               | 4.56 ms: 1.09x slower                                        |
| pyflate                    | 516 ms                                                                | 562 ms: 1.09x slower                                         |
| regex_effbot               | 4.25 ms                                                               | 4.65 ms: 1.09x slower                                        |
| xml_etree_generate         | 104 ms                                                                | 114 ms: 1.10x slower                                         |
| scimark_sor                | 145 ms                                                                | 163 ms: 1.12x slower                                         |
| unpickle                   | 16.9 us                                                               | 19.6 us: 1.16x slower                                        |
| python_startup             | 10.2 ms                                                               | 12.1 ms: 1.18x slower                                        |
| coverage                   | 84.1 ms                                                               | 102 ms: 1.22x slower                                         |
| mypy2                      | 737 ms                                                                | 899 ms: 1.22x slower                                         |
| telco                      | 7.80 ms                                                               | 9.69 ms: 1.24x slower                                        |
| async_generators           | 378 ms                                                                | 480 ms: 1.27x slower                                         |
| python_startup_no_site     | 7.35 ms                                                               | 10.3 ms: 1.40x slower                                        |
| Geometric mean             | (ref)                                                                 | 1.05x faster                                                 |

Benchmark hidden because not significant (3): xml_etree_iterparse, gunicorn, html5lib
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: dask, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.87% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.99x