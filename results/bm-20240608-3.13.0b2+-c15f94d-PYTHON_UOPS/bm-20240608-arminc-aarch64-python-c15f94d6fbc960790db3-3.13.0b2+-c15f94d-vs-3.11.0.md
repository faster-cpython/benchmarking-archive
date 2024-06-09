# Results vs. 3.11.0

- fork: python
- ref: c15f94d6fbc960790db3
- machine: linux-aarch64
- commit hash: c15f94d
- commit date: 2024-06-08
- overall geometric mean: 1.08x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.05x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 300 ms                                                                | 353 ms: 1.18x slower                                                     |
| chameleon      | 8.29 ms                                                               | 10.0 ms: 1.21x slower                                                    |
| docutils       | 2.92 sec                                                              | 3.50 sec: 1.20x slower                                                   |
| html5lib       | 65.3 ms                                                               | 72.1 ms: 1.11x slower                                                    |
| tornado_http   | 140 ms                                                                | 134 ms: 1.04x faster                                                     |
| Geometric mean | (ref)                                                                 | 1.13x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none            | 701 ms                                                                | 519 ms: 1.35x faster                                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 629 ms: 1.32x faster                                                     |
| async_tree_memoization     | 872 ms                                                                | 684 ms: 1.28x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.26 sec: 1.27x faster                                                   |
| async_tree_none_tg         | 620 ms                                                                | 491 ms: 1.26x faster                                                     |
| async_tree_io_tg           | 1.54 sec                                                              | 1.24 sec: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 793 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 828 ms: 1.15x faster                                                     |
| Geometric mean             | (ref)                                                                 | 1.25x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 242 ms                                                                | 236 ms: 1.03x faster                                                     |
| nbody          | 113 ms                                                                | 141 ms: 1.25x slower                                                     |
| float          | 89.6 ms                                                               | 113 ms: 1.26x slower                                                     |
| Geometric mean | (ref)                                                                 | 1.15x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 239 ms                                                                | 249 ms: 1.04x slower                                                     |
| regex_v8       | 29.1 ms                                                               | 31.0 ms: 1.07x slower                                                    |
| regex_effbot   | 4.25 ms                                                               | 4.87 ms: 1.14x slower                                                    |
| regex_compile  | 137 ms                                                                | 166 ms: 1.21x slower                                                     |
| Geometric mean | (ref)                                                                 | 1.11x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_dumps           | 15.4 ms                                                               | 13.7 ms: 1.13x faster                                                    |
| xml_etree_parse      | 209 ms                                                                | 189 ms: 1.11x faster                                                     |
| unpickle_list        | 6.86 us                                                               | 6.62 us: 1.04x faster                                                    |
| pickle_dict          | 37.6 us                                                               | 37.7 us: 1.00x slower                                                    |
| pickle               | 12.8 us                                                               | 13.4 us: 1.05x slower                                                    |
| json_loads           | 30.3 us                                                               | 32.2 us: 1.06x slower                                                    |
| xml_etree_iterparse  | 152 ms                                                                | 162 ms: 1.06x slower                                                     |
| pickle_list          | 5.01 us                                                               | 5.37 us: 1.07x slower                                                    |
| xml_etree_process    | 76.1 ms                                                               | 87.0 ms: 1.14x slower                                                    |
| unpickle             | 16.9 us                                                               | 19.9 us: 1.18x slower                                                    |
| xml_etree_generate   | 104 ms                                                                | 124 ms: 1.19x slower                                                     |
| tomli_loads          | 2.62 sec                                                              | 3.11 sec: 1.19x slower                                                   |
| pickle_pure_python   | 374 us                                                                | 448 us: 1.20x slower                                                     |
| unpickle_pure_python | 278 us                                                                | 348 us: 1.25x slower                                                     |
| Geometric mean       | (ref)                                                                 | 1.08x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.35 ms                                                               | 8.77 ms: 1.19x slower                                                    |
| python_startup         | 10.2 ms                                                               | 13.2 ms: 1.30x slower                                                    |
| Geometric mean         | (ref)                                                                 | 1.24x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 41.8 ms                                                               | 48.9 ms: 1.17x slower                                                    |
| genshi_xml      | 62.2 ms                                                               | 76.1 ms: 1.22x slower                                                    |
| mako            | 13.3 ms                                                               | 16.4 ms: 1.24x slower                                                    |
| genshi_text     | 28.2 ms                                                               | 36.2 ms: 1.28x slower                                                    |
| Geometric mean  | (ref)                                                                 | 1.23x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509 | bm-20240608-arminc-aarch64-python-c15f94d6fbc960790db3-3.13.0b2+-c15f94d |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| typing_runtime_protocols   | 653 us                                                                | 222 us: 2.95x faster                                                     |
| generators                 | 64.2 ms                                                               | 40.2 ms: 1.60x faster                                                    |
| asyncio_tcp                | 920 ms                                                                | 596 ms: 1.54x faster                                                     |
| asyncio_tcp_ssl            | 3.19 sec                                                              | 2.25 sec: 1.42x faster                                                   |
| async_tree_none            | 701 ms                                                                | 519 ms: 1.35x faster                                                     |
| async_tree_memoization_tg  | 828 ms                                                                | 629 ms: 1.32x faster                                                     |
| async_tree_memoization     | 872 ms                                                                | 684 ms: 1.28x faster                                                     |
| async_tree_io              | 1.61 sec                                                              | 1.26 sec: 1.27x faster                                                   |
| async_tree_none_tg         | 620 ms                                                                | 491 ms: 1.26x faster                                                     |
| async_tree_io_tg           | 1.54 sec                                                              | 1.24 sec: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 922 ms                                                                | 793 ms: 1.16x faster                                                     |
| async_tree_cpu_io_mixed    | 955 ms                                                                | 828 ms: 1.15x faster                                                     |
| json_dumps                 | 15.4 ms                                                               | 13.7 ms: 1.13x faster                                                    |
| xml_etree_parse            | 209 ms                                                                | 189 ms: 1.11x faster                                                     |
| coroutines                 | 33.3 ms                                                               | 30.4 ms: 1.10x faster                                                    |
| pathlib                    | 24.8 ms                                                               | 23.4 ms: 1.06x faster                                                    |
| tornado_http               | 140 ms                                                                | 134 ms: 1.04x faster                                                     |
| unpickle_list              | 6.86 us                                                               | 6.62 us: 1.04x faster                                                    |
| logging_simple             | 7.57 us                                                               | 7.32 us: 1.03x faster                                                    |
| raytrace                   | 351 ms                                                                | 340 ms: 1.03x faster                                                     |
| pidigits                   | 242 ms                                                                | 236 ms: 1.03x faster                                                     |
| logging_format             | 8.22 us                                                               | 8.02 us: 1.03x faster                                                    |
| pickle_dict                | 37.6 us                                                               | 37.7 us: 1.00x slower                                                    |
| asyncio_websockets         | 656 ms                                                                | 659 ms: 1.01x slower                                                     |
| comprehensions             | 29.0 us                                                               | 29.6 us: 1.02x slower                                                    |
| sympy_sum                  | 168 ms                                                                | 173 ms: 1.03x slower                                                     |
| sqlglot_parse              | 1.65 ms                                                               | 1.70 ms: 1.03x slower                                                    |
| regex_dna                  | 239 ms                                                                | 249 ms: 1.04x slower                                                     |
| dulwich_log                | 63.2 ms                                                               | 65.9 ms: 1.04x slower                                                    |
| pickle                     | 12.8 us                                                               | 13.4 us: 1.05x slower                                                    |
| richards_super             | 70.2 ms                                                               | 73.6 ms: 1.05x slower                                                    |
| json                       | 5.52 ms                                                               | 5.84 ms: 1.06x slower                                                    |
| mdp                        | 3.35 sec                                                              | 3.56 sec: 1.06x slower                                                   |
| json_loads                 | 30.3 us                                                               | 32.2 us: 1.06x slower                                                    |
| xml_etree_iterparse        | 152 ms                                                                | 162 ms: 1.06x slower                                                     |
| thrift                     | 910 us                                                                | 969 us: 1.06x slower                                                     |
| sympy_str                  | 295 ms                                                                | 314 ms: 1.06x slower                                                     |
| regex_v8                   | 29.1 ms                                                               | 31.0 ms: 1.07x slower                                                    |
| pickle_list                | 5.01 us                                                               | 5.37 us: 1.07x slower                                                    |
| sqlglot_transpile          | 2.00 ms                                                               | 2.15 ms: 1.08x slower                                                    |
| chaos                      | 78.8 ms                                                               | 85.2 ms: 1.08x slower                                                    |
| deltablue                  | 4.75 ms                                                               | 5.13 ms: 1.08x slower                                                    |
| sympy_expand               | 482 ms                                                                | 521 ms: 1.08x slower                                                     |
| bench_mp_pool              | 7.44 ms                                                               | 8.06 ms: 1.08x slower                                                    |
| pycparser                  | 1.25 sec                                                              | 1.36 sec: 1.09x slower                                                   |
| html5lib                   | 65.3 ms                                                               | 72.1 ms: 1.11x slower                                                    |
| sympy_integrate            | 23.2 ms                                                               | 26.0 ms: 1.12x slower                                                    |
| sqlite_synth               | 3.56 us                                                               | 3.99 us: 1.12x slower                                                    |
| aiohttp                    | 1.13 ms                                                               | 1.28 ms: 1.13x slower                                                    |
| sqlglot_normalize          | 132 ms                                                                | 150 ms: 1.13x slower                                                     |
| gunicorn                   | 1.19 ms                                                               | 1.35 ms: 1.14x slower                                                    |
| regex_effbot               | 4.25 ms                                                               | 4.87 ms: 1.14x slower                                                    |
| xml_etree_process          | 76.1 ms                                                               | 87.0 ms: 1.14x slower                                                    |
| richards                   | 58.1 ms                                                               | 66.4 ms: 1.14x slower                                                    |
| sqlglot_optimize           | 63.4 ms                                                               | 72.7 ms: 1.15x slower                                                    |
| meteor_contest             | 115 ms                                                                | 133 ms: 1.15x slower                                                     |
| django_template            | 41.8 ms                                                               | 48.9 ms: 1.17x slower                                                    |
| crypto_pyaes               | 86.5 ms                                                               | 101 ms: 1.17x slower                                                     |
| mypy2                      | 737 ms                                                                | 866 ms: 1.18x slower                                                     |
| 2to3                       | 300 ms                                                                | 353 ms: 1.18x slower                                                     |
| gc_traversal               | 4.33 ms                                                               | 5.10 ms: 1.18x slower                                                    |
| unpickle                   | 16.9 us                                                               | 19.9 us: 1.18x slower                                                    |
| xml_etree_generate         | 104 ms                                                                | 124 ms: 1.19x slower                                                     |
| tomli_loads                | 2.62 sec                                                              | 3.11 sec: 1.19x slower                                                   |
| python_startup_no_site     | 7.35 ms                                                               | 8.77 ms: 1.19x slower                                                    |
| coverage                   | 84.1 ms                                                               | 101 ms: 1.20x slower                                                     |
| pickle_pure_python         | 374 us                                                                | 448 us: 1.20x slower                                                     |
| docutils                   | 2.92 sec                                                              | 3.50 sec: 1.20x slower                                                   |
| flaskblogging              | 4.19 ms                                                               | 5.03 ms: 1.20x slower                                                    |
| go                         | 163 ms                                                                | 196 ms: 1.20x slower                                                     |
| chameleon                  | 8.29 ms                                                               | 10.0 ms: 1.21x slower                                                    |
| regex_compile              | 137 ms                                                                | 166 ms: 1.21x slower                                                     |
| fannkuch                   | 451 ms                                                                | 547 ms: 1.21x slower                                                     |
| genshi_xml                 | 62.2 ms                                                               | 76.1 ms: 1.22x slower                                                    |
| deepcopy_reduce            | 3.89 us                                                               | 4.78 us: 1.23x slower                                                    |
| deepcopy                   | 435 us                                                                | 539 us: 1.24x slower                                                     |
| mako                       | 13.3 ms                                                               | 16.4 ms: 1.24x slower                                                    |
| unpickle_pure_python       | 278 us                                                                | 348 us: 1.25x slower                                                     |
| nqueens                    | 102 ms                                                                | 128 ms: 1.25x slower                                                     |
| nbody                      | 113 ms                                                                | 141 ms: 1.25x slower                                                     |
| float                      | 89.6 ms                                                               | 113 ms: 1.26x slower                                                     |
| pprint_pformat             | 1.85 sec                                                              | 2.38 sec: 1.28x slower                                                   |
| scimark_sparse_mat_mult    | 6.29 ms                                                               | 8.05 ms: 1.28x slower                                                    |
| genshi_text                | 28.2 ms                                                               | 36.2 ms: 1.28x slower                                                    |
| pprint_safe_repr           | 903 ms                                                                | 1.16 sec: 1.29x slower                                                   |
| create_gc_cycles           | 1.87 ms                                                               | 2.41 ms: 1.29x slower                                                    |
| python_startup             | 10.2 ms                                                               | 13.2 ms: 1.30x slower                                                    |
| scimark_fft                | 402 ms                                                                | 543 ms: 1.35x slower                                                     |
| scimark_sor                | 145 ms                                                                | 199 ms: 1.37x slower                                                     |
| pyflate                    | 516 ms                                                                | 706 ms: 1.37x slower                                                     |
| telco                      | 7.80 ms                                                               | 10.8 ms: 1.38x slower                                                    |
| hexiom                     | 7.57 ms                                                               | 10.5 ms: 1.39x slower                                                    |
| scimark_monte_carlo        | 83.2 ms                                                               | 116 ms: 1.39x slower                                                     |
| spectral_norm              | 131 ms                                                                | 183 ms: 1.40x slower                                                     |
| logging_silent             | 133 ns                                                                | 188 ns: 1.42x slower                                                     |
| async_generators           | 378 ms                                                                | 538 ms: 1.42x slower                                                     |
| deepcopy_memo              | 49.0 us                                                               | 72.0 us: 1.47x slower                                                    |
| scimark_lu                 | 140 ms                                                                | 211 ms: 1.51x slower                                                     |
| Geometric mean             | (ref)                                                                 | 1.08x slower                                                             |

Benchmark hidden because not significant (3): pylint, bench_thread_pool, dask
Ignored benchmarks (2) of results/bm-20221024-3.11.0-deaf509/bm-20221024-arminc-aarch64-python-deaf509e8fc6e0363bd6-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.05x