# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_align
- machine: linux-aarch64
- commit hash: 0081bcd
- commit date: 2024-05-23
- overall geometric mean: 1.02x slower
- HPT reliability: 98.68%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240523-arminc-aarch64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 353 ms: 1.18x slower                                                  |
| chameleon      | 8.29 ms                                                               | 9.09 ms: 1.10x slower                                                 |
| docutils       | 2.92 sec                                                              | 3.54 sec: 1.21x slower                                                |
| html5lib       | 65.3 ms                                                               | 70.4 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.11x slower                                                          |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240523-arminc-aarch64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 509 ms: 1.38x faster                                                  |
| async_tree_memoization_tg  | 828 ms                                                                | 628 ms: 1.32x faster                                                  |
| async_tree_memoization     | 872 ms                                                                | 676 ms: 1.29x faster                                                  |
| async_tree_none_tg         | 620 ms                                                                | 485 ms: 1.28x faster                                                  |
| async_tree_io              | 1.61 sec                                                              | 1.26 sec: 1.27x faster                                                |
| async_tree_io_tg           | 1.54 sec                                                              | 1.22 sec: 1.26x faster                                                |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 831 ms: 1.15x faster                                                  |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 807 ms: 1.14x faster                                                  |
| Geometric mean             | (ref)                                                                 | 1.26x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240523-arminc-aarch64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 234 ms: 1.03x faster                                                  |
| float          | 89.6 ms                                                               | 91.0 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                                 | 1.01x faster                                                          |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240523-arminc-aarch64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 29.1 ms                                                               | 30.1 ms: 1.03x slower                                                 |
| regex_dna      | 239 ms                                                                | 251 ms: 1.05x slower                                                  |
| regex_effbot   | 4.25 ms                                                               | 4.90 ms: 1.15x slower                                                 |
| regex_compile  | 137 ms                                                                | 165 ms: 1.21x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.11x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240523-arminc-aarch64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 13.1 ms: 1.18x faster                                                 |
| xml_etree_parse      | 209 ms                                                                | 192 ms: 1.09x faster                                                  |
| unpickle_list        | 6.86 us                                                               | 6.35 us: 1.08x faster                                                 |
| unpickle_pure_python | 278 us                                                                | 272 us: 1.02x faster                                                  |
| xml_etree_iterparse  | 152 ms                                                                | 150 ms: 1.01x faster                                                  |
| pickle_list          | 5.01 us                                                               | 5.24 us: 1.05x slower                                                 |
| xml_etree_process    | 76.1 ms                                                               | 79.9 ms: 1.05x slower                                                 |
| xml_etree_generate   | 104 ms                                                                | 110 ms: 1.06x slower                                                  |
| json_loads           | 30.3 us                                                               | 32.3 us: 1.07x slower                                                 |
| pickle               | 12.8 us                                                               | 13.6 us: 1.07x slower                                                 |
| pickle_pure_python   | 374 us                                                                | 403 us: 1.08x slower                                                  |
| unpickle             | 16.9 us                                                               | 19.5 us: 1.16x slower                                                 |
| Geometric mean       | (ref)                                                                 | 1.01x slower                                                          |

Benchmark hidden because not significant (2): pickle_dict, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240523-arminc-aarch64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 10.2 ms                                                               | 14.9 ms: 1.46x slower                                                 |
| python_startup_no_site | 7.35 ms                                                               | 10.9 ms: 1.48x slower                                                 |
| Geometric mean         | (ref)                                                                 | 1.47x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240523-arminc-aarch64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 13.3 ms                                                               | 12.6 ms: 1.05x faster                                                 |
| django_template | 41.8 ms                                                               | 49.3 ms: 1.18x slower                                                 |
| genshi_text     | 28.2 ms                                                               | 33.2 ms: 1.18x slower                                                 |
| genshi_xml      | 62.2 ms                                                               | 80.0 ms: 1.29x slower                                                 |
| Geometric mean  | (ref)                                                                 | 1.14x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240523-arminc-aarch64-brandtbucher-justin_align-3.14.0a0-0081bcd |
|----------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 204 us: 3.20x faster                                                  |
| generators                 | 64.2 ms                                                               | 38.5 ms: 1.67x faster                                                 |
| asyncio_tcp                | 920 ms                                                                | 629 ms: 1.46x faster                                                  |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.29 sec: 1.40x faster                                                |
| async_tree_none            | 701 ms                                                                | 509 ms: 1.38x faster                                                  |
| async_tree_memoization_tg  | 828 ms                                                                | 628 ms: 1.32x faster                                                  |
| async_tree_memoization     | 872 ms                                                                | 676 ms: 1.29x faster                                                  |
| async_tree_none_tg         | 620 ms                                                                | 485 ms: 1.28x faster                                                  |
| async_tree_io              | 1.61 sec                                                              | 1.26 sec: 1.27x faster                                                |
| comprehensions             | 29.0 us                                                               | 23.0 us: 1.26x faster                                                 |
| async_tree_io_tg           | 1.54 sec                                                              | 1.22 sec: 1.26x faster                                                |
| json_dumps                 | 15.4 ms                                                               | 13.1 ms: 1.18x faster                                                 |
| richards_super             | 70.2 ms                                                               | 60.2 ms: 1.17x faster                                                 |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 831 ms: 1.15x faster                                                  |
| pathlib                    | 24.8 ms                                                               | 21.7 ms: 1.14x faster                                                 |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 807 ms: 1.14x faster                                                  |
| coroutines                 | 33.3 ms                                                               | 29.4 ms: 1.13x faster                                                 |
| richards                   | 58.1 ms                                                               | 52.7 ms: 1.10x faster                                                 |
| raytrace                   | 351 ms                                                                | 321 ms: 1.09x faster                                                  |
| xml_etree_parse            | 209 ms                                                                | 192 ms: 1.09x faster                                                  |
| unpickle_list              | 6.86 us                                                               | 6.35 us: 1.08x faster                                                 |
| mako                       | 13.3 ms                                                               | 12.6 ms: 1.05x faster                                                 |
| logging_simple             | 7.57 us                                                               | 7.22 us: 1.05x faster                                                 |
| sqlglot_parse              | 1.65 ms                                                               | 1.58 ms: 1.05x faster                                                 |
| logging_format             | 8.22 us                                                               | 7.89 us: 1.04x faster                                                 |
| deltablue                  | 4.75 ms                                                               | 4.57 ms: 1.04x faster                                                 |
| pidigits                   | 242 ms                                                                | 234 ms: 1.03x faster                                                  |
| fannkuch                   | 451 ms                                                                | 437 ms: 1.03x faster                                                  |
| bench_thread_pool          | 1.36 ms                                                               | 1.32 ms: 1.03x faster                                                 |
| unpickle_pure_python       | 278 us                                                                | 272 us: 1.02x faster                                                  |
| xml_etree_iterparse        | 152 ms                                                                | 150 ms: 1.01x faster                                                  |
| deepcopy_memo              | 49.0 us                                                               | 48.7 us: 1.01x faster                                                 |
| asyncio_websockets         | 656 ms                                                                | 666 ms: 1.02x slower                                                  |
| float                      | 89.6 ms                                                               | 91.0 ms: 1.02x slower                                                 |
| json                       | 5.52 ms                                                               | 5.62 ms: 1.02x slower                                                 |
| dask                       | 385 ms                                                                | 393 ms: 1.02x slower                                                  |
| logging_silent             | 133 ns                                                                | 136 ns: 1.03x slower                                                  |
| mdp                        | 3.35 sec                                                              | 3.46 sec: 1.03x slower                                                |
| regex_v8                   | 29.1 ms                                                               | 30.1 ms: 1.03x slower                                                 |
| pickle_list                | 5.01 us                                                               | 5.24 us: 1.05x slower                                                 |
| regex_dna                  | 239 ms                                                                | 251 ms: 1.05x slower                                                  |
| xml_etree_process          | 76.1 ms                                                               | 79.9 ms: 1.05x slower                                                 |
| xml_etree_generate         | 104 ms                                                                | 110 ms: 1.06x slower                                                  |
| sympy_str                  | 295 ms                                                                | 313 ms: 1.06x slower                                                  |
| json_loads                 | 30.3 us                                                               | 32.3 us: 1.07x slower                                                 |
| pickle                     | 12.8 us                                                               | 13.6 us: 1.07x slower                                                 |
| thrift                     | 910 us                                                                | 975 us: 1.07x slower                                                  |
| sympy_sum                  | 168 ms                                                                | 181 ms: 1.07x slower                                                  |
| sqlglot_normalize          | 132 ms                                                                | 142 ms: 1.08x slower                                                  |
| pycparser                  | 1.25 sec                                                              | 1.34 sec: 1.08x slower                                                |
| pickle_pure_python         | 374 us                                                                | 403 us: 1.08x slower                                                  |
| html5lib                   | 65.3 ms                                                               | 70.4 ms: 1.08x slower                                                 |
| go                         | 163 ms                                                                | 176 ms: 1.08x slower                                                  |
| sqlite_synth               | 3.56 us                                                               | 3.84 us: 1.08x slower                                                 |
| scimark_monte_carlo        | 83.2 ms                                                               | 90.0 ms: 1.08x slower                                                 |
| chaos                      | 78.8 ms                                                               | 85.6 ms: 1.09x slower                                                 |
| sqlglot_optimize           | 63.4 ms                                                               | 68.9 ms: 1.09x slower                                                 |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 6.87 ms: 1.09x slower                                                 |
| spectral_norm              | 131 ms                                                                | 143 ms: 1.09x slower                                                  |
| chameleon                  | 8.29 ms                                                               | 9.09 ms: 1.10x slower                                                 |
| dulwich_log                | 63.2 ms                                                               | 69.5 ms: 1.10x slower                                                 |
| sympy_expand               | 482 ms                                                                | 532 ms: 1.10x slower                                                  |
| sympy_integrate            | 23.2 ms                                                               | 25.6 ms: 1.11x slower                                                 |
| bench_mp_pool              | 7.44 ms                                                               | 8.28 ms: 1.11x slower                                                 |
| nqueens                    | 102 ms                                                                | 114 ms: 1.12x slower                                                  |
| scimark_fft                | 402 ms                                                                | 451 ms: 1.12x slower                                                  |
| deepcopy                   | 435 us                                                                | 492 us: 1.13x slower                                                  |
| hexiom                     | 7.57 ms                                                               | 8.67 ms: 1.15x slower                                                 |
| regex_effbot               | 4.25 ms                                                               | 4.90 ms: 1.15x slower                                                 |
| unpickle                   | 16.9 us                                                               | 19.5 us: 1.16x slower                                                 |
| 2to3                       | 300 ms                                                                | 353 ms: 1.18x slower                                                  |
| django_template            | 41.8 ms                                                               | 49.3 ms: 1.18x slower                                                 |
| genshi_text                | 28.2 ms                                                               | 33.2 ms: 1.18x slower                                                 |
| deepcopy_reduce            | 3.89 us                                                               | 4.61 us: 1.18x slower                                                 |
| pyflate                    | 516 ms                                                                | 613 ms: 1.19x slower                                                  |
| pprint_safe_repr           | 903 ms                                                                | 1.07 sec: 1.19x slower                                                |
| pprint_pformat             | 1.85 sec                                                              | 2.22 sec: 1.20x slower                                                |
| coverage                   | 84.1 ms                                                               | 101 ms: 1.20x slower                                                  |
| scimark_sor                | 145 ms                                                                | 175 ms: 1.21x slower                                                  |
| regex_compile              | 137 ms                                                                | 165 ms: 1.21x slower                                                  |
| docutils                   | 2.92 sec                                                              | 3.54 sec: 1.21x slower                                                |
| gc_traversal               | 4.33 ms                                                               | 5.27 ms: 1.22x slower                                                 |
| flaskblogging              | 4.19 ms                                                               | 5.23 ms: 1.25x slower                                                 |
| create_gc_cycles           | 1.87 ms                                                               | 2.37 ms: 1.27x slower                                                 |
| telco                      | 7.80 ms                                                               | 9.90 ms: 1.27x slower                                                 |
| scimark_lu                 | 140 ms                                                                | 179 ms: 1.28x slower                                                  |
| genshi_xml                 | 62.2 ms                                                               | 80.0 ms: 1.29x slower                                                 |
| async_generators           | 378 ms                                                                | 510 ms: 1.35x slower                                                  |
| python_startup             | 10.2 ms                                                               | 14.9 ms: 1.46x slower                                                 |
| python_startup_no_site     | 7.35 ms                                                               | 10.9 ms: 1.48x slower                                                 |
| Geometric mean             | (ref)                                                                 | 1.02x slower                                                          |

Benchmark hidden because not significant (8): tornado_http, pickle_dict, nbody, tomli_loads, crypto_pyaes, sqlglot_transpile, meteor_contest, pylint
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: aiohttp, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 98.68% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.14x