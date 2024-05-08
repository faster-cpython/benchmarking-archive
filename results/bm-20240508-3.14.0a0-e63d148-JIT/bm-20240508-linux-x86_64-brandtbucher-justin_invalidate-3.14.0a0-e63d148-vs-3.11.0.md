# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_invalidate
- machine: linux-x86_64
- commit hash: e63d148
- commit date: 2024-05-08
- overall geometric mean: 1.01x faster
- HPT reliability: 88.49%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-justin_invalidate-3.14.0a0-e63d148 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 302 ms: 1.14x slower                                                     |
| chameleon      | 6.70 ms                                                | 7.17 ms: 1.07x slower                                                    |
| docutils       | 2.66 sec                                               | 3.34 sec: 1.26x slower                                                   |
| html5lib       | 64.8 ms                                                | 72.1 ms: 1.11x slower                                                    |
| tornado_http   | 98.1 ms                                                | 103 ms: 1.05x slower                                                     |
| Geometric mean | (ref)                                                  | 1.12x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-justin_invalidate-3.14.0a0-e63d148 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 379 ms: 1.39x faster                                                     |
| async_tree_none_tg         | 491 ms                                                 | 358 ms: 1.37x faster                                                     |
| async_tree_io              | 1.29 sec                                               | 962 ms: 1.34x faster                                                     |
| async_tree_memoization_tg  | 626 ms                                                 | 478 ms: 1.31x faster                                                     |
| async_tree_io_tg           | 1.29 sec                                               | 996 ms: 1.30x faster                                                     |
| async_tree_memoization     | 639 ms                                                 | 494 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 599 ms: 1.27x faster                                                     |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 635 ms: 1.18x faster                                                     |
| Geometric mean             | (ref)                                                  | 1.31x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-justin_invalidate-3.14.0a0-e63d148 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 80.8 ms: 1.19x faster                                                    |
| float          | 78.9 ms                                                | 72.8 ms: 1.08x faster                                                    |
| pidigits       | 194 ms                                                 | 188 ms: 1.03x faster                                                     |
| Geometric mean | (ref)                                                  | 1.10x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-justin_invalidate-3.14.0a0-e63d148 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 140 ms: 1.01x faster                                                     |
| regex_dna      | 205 ms                                                 | 219 ms: 1.07x slower                                                     |
| regex_effbot   | 3.51 ms                                                | 3.84 ms: 1.09x slower                                                    |
| regex_v8       | 22.9 ms                                                | 25.4 ms: 1.11x slower                                                    |
| Geometric mean | (ref)                                                  | 1.07x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-justin_invalidate-3.14.0a0-e63d148 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.3 ms: 1.30x faster                                                    |
| tomli_loads          | 2.30 sec                                               | 1.99 sec: 1.16x faster                                                   |
| unpickle_pure_python | 242 us                                                 | 225 us: 1.08x faster                                                     |
| pickle_pure_python   | 320 us                                                 | 300 us: 1.06x faster                                                     |
| xml_etree_parse      | 164 ms                                                 | 157 ms: 1.05x faster                                                     |
| pickle_dict          | 34.6 us                                                | 33.5 us: 1.03x faster                                                    |
| json_loads           | 29.2 us                                                | 28.9 us: 1.01x faster                                                    |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                     |
| unpickle_list        | 5.21 us                                                | 5.39 us: 1.03x slower                                                    |
| pickle               | 11.0 us                                                | 11.7 us: 1.07x slower                                                    |
| xml_etree_process    | 56.9 ms                                                | 60.9 ms: 1.07x slower                                                    |
| xml_etree_generate   | 81.1 ms                                                | 88.2 ms: 1.09x slower                                                    |
| unpickle             | 13.8 us                                                | 15.6 us: 1.13x slower                                                    |
| pickle_list          | 4.59 us                                                | 5.21 us: 1.13x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-justin_invalidate-3.14.0a0-e63d148 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.67 ms: 1.28x slower                                                    |
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.29x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.28x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-justin_invalidate-3.14.0a0-e63d148 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 9.50 ms: 1.12x faster                                                    |
| django_template | 33.5 ms                                                | 36.6 ms: 1.09x slower                                                    |
| genshi_text     | 22.5 ms                                                | 25.8 ms: 1.15x slower                                                    |
| genshi_xml      | 53.4 ms                                                | 61.6 ms: 1.15x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.06x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-justin_invalidate-3.14.0a0-e63d148 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 179 us: 2.90x faster                                                     |
| generators                 | 74.9 ms                                                | 30.0 ms: 2.50x faster                                                    |
| asyncio_tcp                | 875 ms                                                 | 520 ms: 1.68x faster                                                     |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                   |
| comprehensions             | 23.6 us                                                | 16.9 us: 1.39x faster                                                    |
| async_tree_none            | 528 ms                                                 | 379 ms: 1.39x faster                                                     |
| async_tree_none_tg         | 491 ms                                                 | 358 ms: 1.37x faster                                                     |
| async_tree_io              | 1.29 sec                                               | 962 ms: 1.34x faster                                                     |
| async_tree_memoization_tg  | 626 ms                                                 | 478 ms: 1.31x faster                                                     |
| pylint                     | 476 ms                                                 | 366 ms: 1.30x faster                                                     |
| async_tree_io_tg           | 1.29 sec                                               | 996 ms: 1.30x faster                                                     |
| json_dumps                 | 13.3 ms                                                | 10.3 ms: 1.30x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 494 ms: 1.29x faster                                                     |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 599 ms: 1.27x faster                                                     |
| richards_super             | 61.9 ms                                                | 49.4 ms: 1.25x faster                                                    |
| chaos                      | 71.9 ms                                                | 59.7 ms: 1.20x faster                                                    |
| nbody                      | 96.0 ms                                                | 80.8 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 635 ms: 1.18x faster                                                     |
| tomli_loads                | 2.30 sec                                               | 1.99 sec: 1.16x faster                                                   |
| richards                   | 49.8 ms                                                | 43.4 ms: 1.15x faster                                                    |
| coroutines                 | 27.0 ms                                                | 23.9 ms: 1.13x faster                                                    |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.47 ms: 1.13x faster                                                    |
| mako                       | 10.7 ms                                                | 9.50 ms: 1.12x faster                                                    |
| raytrace                   | 309 ms                                                 | 275 ms: 1.12x faster                                                     |
| fannkuch                   | 405 ms                                                 | 364 ms: 1.11x faster                                                     |
| scimark_monte_carlo        | 70.7 ms                                                | 63.7 ms: 1.11x faster                                                    |
| scimark_fft                | 345 ms                                                 | 313 ms: 1.10x faster                                                     |
| crypto_pyaes               | 76.7 ms                                                | 69.6 ms: 1.10x faster                                                    |
| float                      | 78.9 ms                                                | 72.8 ms: 1.08x faster                                                    |
| unpickle_pure_python       | 242 us                                                 | 225 us: 1.08x faster                                                     |
| deltablue                  | 3.92 ms                                                | 3.67 ms: 1.07x faster                                                    |
| pickle_pure_python         | 320 us                                                 | 300 us: 1.06x faster                                                     |
| logging_simple             | 6.22 us                                                | 5.85 us: 1.06x faster                                                    |
| mdp                        | 2.77 sec                                               | 2.61 sec: 1.06x faster                                                   |
| deepcopy_memo              | 40.2 us                                                | 37.8 us: 1.06x faster                                                    |
| spectral_norm              | 108 ms                                                 | 102 ms: 1.06x faster                                                     |
| logging_silent             | 111 ns                                                 | 106 ns: 1.05x faster                                                     |
| xml_etree_parse            | 164 ms                                                 | 157 ms: 1.05x faster                                                     |
| logging_format             | 6.81 us                                                | 6.53 us: 1.04x faster                                                    |
| pprint_pformat             | 1.55 sec                                               | 1.49 sec: 1.04x faster                                                   |
| gc_traversal               | 4.01 ms                                                | 3.86 ms: 1.04x faster                                                    |
| pathlib                    | 18.5 ms                                                | 17.9 ms: 1.03x faster                                                    |
| sqlglot_parse              | 1.43 ms                                                | 1.39 ms: 1.03x faster                                                    |
| pickle_dict                | 34.6 us                                                | 33.5 us: 1.03x faster                                                    |
| pidigits                   | 194 ms                                                 | 188 ms: 1.03x faster                                                     |
| hexiom                     | 6.89 ms                                                | 6.68 ms: 1.03x faster                                                    |
| pprint_safe_repr           | 747 ms                                                 | 725 ms: 1.03x faster                                                     |
| nqueens                    | 87.9 ms                                                | 86.5 ms: 1.02x faster                                                    |
| json_loads                 | 29.2 us                                                | 28.9 us: 1.01x faster                                                    |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                     |
| regex_compile              | 141 ms                                                 | 140 ms: 1.01x faster                                                     |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                                     |
| sympy_sum                  | 169 ms                                                 | 170 ms: 1.01x slower                                                     |
| sqlglot_transpile          | 1.75 ms                                                | 1.77 ms: 1.01x slower                                                    |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                                     |
| sympy_str                  | 297 ms                                                 | 302 ms: 1.02x slower                                                     |
| deepcopy                   | 365 us                                                 | 372 us: 1.02x slower                                                     |
| pyflate                    | 434 ms                                                 | 444 ms: 1.02x slower                                                     |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                     |
| unpickle_list              | 5.21 us                                                | 5.39 us: 1.03x slower                                                    |
| bench_thread_pool          | 834 us                                                 | 872 us: 1.04x slower                                                     |
| tornado_http               | 98.1 ms                                                | 103 ms: 1.05x slower                                                     |
| sympy_integrate            | 21.5 ms                                                | 22.6 ms: 1.05x slower                                                    |
| sympy_expand               | 484 ms                                                 | 513 ms: 1.06x slower                                                     |
| scimark_lu                 | 116 ms                                                 | 124 ms: 1.07x slower                                                     |
| pickle                     | 11.0 us                                                | 11.7 us: 1.07x slower                                                    |
| deepcopy_reduce            | 3.22 us                                                | 3.43 us: 1.07x slower                                                    |
| pycparser                  | 1.19 sec                                               | 1.27 sec: 1.07x slower                                                   |
| xml_etree_process          | 56.9 ms                                                | 60.9 ms: 1.07x slower                                                    |
| chameleon                  | 6.70 ms                                                | 7.17 ms: 1.07x slower                                                    |
| regex_dna                  | 205 ms                                                 | 219 ms: 1.07x slower                                                     |
| thrift                     | 784 us                                                 | 840 us: 1.07x slower                                                     |
| dulwich_log                | 64.6 ms                                                | 69.6 ms: 1.08x slower                                                    |
| sqlglot_optimize           | 55.3 ms                                                | 59.9 ms: 1.08x slower                                                    |
| xml_etree_generate         | 81.1 ms                                                | 88.2 ms: 1.09x slower                                                    |
| scimark_sor                | 121 ms                                                 | 132 ms: 1.09x slower                                                     |
| coverage                   | 78.8 ms                                                | 85.7 ms: 1.09x slower                                                    |
| django_template            | 33.5 ms                                                | 36.6 ms: 1.09x slower                                                    |
| regex_effbot               | 3.51 ms                                                | 3.84 ms: 1.09x slower                                                    |
| regex_v8                   | 22.9 ms                                                | 25.4 ms: 1.11x slower                                                    |
| html5lib                   | 64.8 ms                                                | 72.1 ms: 1.11x slower                                                    |
| sqlite_synth               | 2.57 us                                                | 2.86 us: 1.11x slower                                                    |
| dask                       | 365 ms                                                 | 410 ms: 1.12x slower                                                     |
| aiohttp                    | 1.12 ms                                                | 1.26 ms: 1.13x slower                                                    |
| unpickle                   | 13.8 us                                                | 15.6 us: 1.13x slower                                                    |
| pickle_list                | 4.59 us                                                | 5.21 us: 1.13x slower                                                    |
| gunicorn                   | 1.20 ms                                                | 1.36 ms: 1.14x slower                                                    |
| 2to3                       | 264 ms                                                 | 302 ms: 1.14x slower                                                     |
| genshi_text                | 22.5 ms                                                | 25.8 ms: 1.15x slower                                                    |
| genshi_xml                 | 53.4 ms                                                | 61.6 ms: 1.15x slower                                                    |
| async_generators           | 374 ms                                                 | 468 ms: 1.25x slower                                                     |
| docutils                   | 2.66 sec                                               | 3.34 sec: 1.26x slower                                                   |
| python_startup_no_site     | 6.01 ms                                                | 7.67 ms: 1.28x slower                                                    |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.29x slower                                                    |
| create_gc_cycles           | 1.43 ms                                                | 1.87 ms: 1.30x slower                                                    |
| flaskblogging              | 7.28 ms                                                | 10.0 ms: 1.38x slower                                                    |
| telco                      | 6.86 ms                                                | 174 ms: 25.39x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (3): bench_mp_pool, go, json
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: djangocms, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 88.49% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.15x