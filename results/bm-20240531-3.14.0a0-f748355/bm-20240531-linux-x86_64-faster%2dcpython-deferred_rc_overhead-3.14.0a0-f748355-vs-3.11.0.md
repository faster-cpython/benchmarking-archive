# Results vs. 3.11.0

- fork: faster-cpython
- ref: deferred_rc_overhead
- machine: linux-x86_64
- commit hash: f748355
- commit date: 2024-05-31
- overall geometric mean: 1.07x faster
- HPT reliability: 99.12%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240531-linux-x86_64-faster%2dcpython-deferred_rc_overhead-3.14.0a0-f748355 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 270 ms: 1.02x slower                                                            |
| docutils       | 2.66 sec                                               | 2.79 sec: 1.05x slower                                                          |
| html5lib       | 64.8 ms                                                | 67.4 ms: 1.04x slower                                                           |
| tornado_http   | 98.1 ms                                                | 93.9 ms: 1.04x faster                                                           |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240531-linux-x86_64-faster%2dcpython-deferred_rc_overhead-3.14.0a0-f748355 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 350 ms: 1.40x faster                                                            |
| async_tree_memoization_tg  | 626 ms                                                 | 447 ms: 1.40x faster                                                            |
| async_tree_io_tg           | 1.29 sec                                               | 934 ms: 1.39x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 468 ms: 1.36x faster                                                            |
| async_tree_none            | 528 ms                                                 | 388 ms: 1.36x faster                                                            |
| async_tree_io              | 1.29 sec                                               | 947 ms: 1.36x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 583 ms: 1.31x faster                                                            |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 621 ms: 1.21x faster                                                            |
| Geometric mean             | (ref)                                                  | 1.35x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240531-linux-x86_64-faster%2dcpython-deferred_rc_overhead-3.14.0a0-f748355 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 89.1 ms: 1.08x faster                                                           |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                            |
| float          | 78.9 ms                                                | 79.5 ms: 1.01x slower                                                           |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240531-linux-x86_64-faster%2dcpython-deferred_rc_overhead-3.14.0a0-f748355 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 134 ms: 1.05x faster                                                            |
| regex_effbot   | 3.51 ms                                                | 3.62 ms: 1.03x slower                                                           |
| regex_dna      | 205 ms                                                 | 228 ms: 1.11x slower                                                            |
| regex_v8       | 22.9 ms                                                | 26.0 ms: 1.13x slower                                                           |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240531-linux-x86_64-faster%2dcpython-deferred_rc_overhead-3.14.0a0-f748355 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                           |
| unpickle_pure_python | 242 us                                                 | 218 us: 1.11x faster                                                            |
| tomli_loads          | 2.30 sec                                               | 2.18 sec: 1.06x faster                                                          |
| pickle_pure_python   | 320 us                                                 | 303 us: 1.06x faster                                                            |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.03x faster                                                            |
| xml_etree_iterparse  | 108 ms                                                 | 106 ms: 1.01x faster                                                            |
| json_loads           | 29.2 us                                                | 28.8 us: 1.01x faster                                                           |
| pickle_dict          | 34.6 us                                                | 35.9 us: 1.04x slower                                                           |
| unpickle_list        | 5.21 us                                                | 5.41 us: 1.04x slower                                                           |
| xml_etree_process    | 56.9 ms                                                | 60.3 ms: 1.06x slower                                                           |
| xml_etree_generate   | 81.1 ms                                                | 87.1 ms: 1.08x slower                                                           |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                                           |
| unpickle             | 13.8 us                                                | 15.5 us: 1.12x slower                                                           |
| pickle_list          | 4.59 us                                                | 5.30 us: 1.16x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.00x slower                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240531-linux-x86_64-faster%2dcpython-deferred_rc_overhead-3.14.0a0-f748355 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.07 ms: 1.18x slower                                                           |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                           |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240531-linux-x86_64-faster%2dcpython-deferred_rc_overhead-3.14.0a0-f748355 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 50.6 ms: 1.06x faster                                                           |
| genshi_text     | 22.5 ms                                                | 23.3 ms: 1.03x slower                                                           |
| django_template | 33.5 ms                                                | 35.3 ms: 1.05x slower                                                           |
| mako            | 10.7 ms                                                | 11.7 ms: 1.09x slower                                                           |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240531-linux-x86_64-faster%2dcpython-deferred_rc_overhead-3.14.0a0-f748355 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 165 us: 3.14x faster                                                            |
| generators                 | 74.9 ms                                                | 27.8 ms: 2.69x faster                                                           |
| asyncio_tcp                | 875 ms                                                 | 505 ms: 1.73x faster                                                            |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                          |
| pylint                     | 476 ms                                                 | 316 ms: 1.51x faster                                                            |
| async_tree_none_tg         | 491 ms                                                 | 350 ms: 1.40x faster                                                            |
| async_tree_memoization_tg  | 626 ms                                                 | 447 ms: 1.40x faster                                                            |
| comprehensions             | 23.6 us                                                | 16.8 us: 1.40x faster                                                           |
| async_tree_io_tg           | 1.29 sec                                               | 934 ms: 1.39x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 468 ms: 1.36x faster                                                            |
| async_tree_none            | 528 ms                                                 | 388 ms: 1.36x faster                                                            |
| async_tree_io              | 1.29 sec                                               | 947 ms: 1.36x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 583 ms: 1.31x faster                                                            |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                           |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 621 ms: 1.21x faster                                                            |
| deltablue                  | 3.92 ms                                                | 3.27 ms: 1.20x faster                                                           |
| coroutines                 | 27.0 ms                                                | 22.6 ms: 1.20x faster                                                           |
| chaos                      | 71.9 ms                                                | 60.9 ms: 1.18x faster                                                           |
| raytrace                   | 309 ms                                                 | 265 ms: 1.16x faster                                                            |
| logging_silent             | 111 ns                                                 | 97.2 ns: 1.14x faster                                                           |
| pathlib                    | 18.5 ms                                                | 16.2 ms: 1.14x faster                                                           |
| richards_super             | 61.9 ms                                                | 55.2 ms: 1.12x faster                                                           |
| gc_traversal               | 4.01 ms                                                | 3.59 ms: 1.12x faster                                                           |
| hexiom                     | 6.89 ms                                                | 6.21 ms: 1.11x faster                                                           |
| unpickle_pure_python       | 242 us                                                 | 218 us: 1.11x faster                                                            |
| logging_simple             | 6.22 us                                                | 5.68 us: 1.10x faster                                                           |
| sympy_sum                  | 169 ms                                                 | 155 ms: 1.09x faster                                                            |
| sqlglot_parse              | 1.43 ms                                                | 1.32 ms: 1.09x faster                                                           |
| sqlglot_transpile          | 1.75 ms                                                | 1.62 ms: 1.08x faster                                                           |
| logging_format             | 6.81 us                                                | 6.31 us: 1.08x faster                                                           |
| nbody                      | 96.0 ms                                                | 89.1 ms: 1.08x faster                                                           |
| mdp                        | 2.77 sec                                               | 2.58 sec: 1.07x faster                                                          |
| nqueens                    | 87.9 ms                                                | 82.4 ms: 1.07x faster                                                           |
| sympy_str                  | 297 ms                                                 | 280 ms: 1.06x faster                                                            |
| tomli_loads                | 2.30 sec                                               | 2.18 sec: 1.06x faster                                                          |
| genshi_xml                 | 53.4 ms                                                | 50.6 ms: 1.06x faster                                                           |
| pickle_pure_python         | 320 us                                                 | 303 us: 1.06x faster                                                            |
| regex_compile              | 141 ms                                                 | 134 ms: 1.05x faster                                                            |
| sympy_integrate            | 21.5 ms                                                | 20.4 ms: 1.05x faster                                                           |
| tornado_http               | 98.1 ms                                                | 93.9 ms: 1.04x faster                                                           |
| sympy_expand               | 484 ms                                                 | 469 ms: 1.03x faster                                                            |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.03x faster                                                            |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                            |
| sqlglot_normalize          | 113 ms                                                 | 110 ms: 1.02x faster                                                            |
| deepcopy_memo              | 40.2 us                                                | 39.3 us: 1.02x faster                                                           |
| go                         | 149 ms                                                 | 146 ms: 1.02x faster                                                            |
| xml_etree_iterparse        | 108 ms                                                 | 106 ms: 1.01x faster                                                            |
| json_loads                 | 29.2 us                                                | 28.8 us: 1.01x faster                                                           |
| richards                   | 49.8 ms                                                | 49.1 ms: 1.01x faster                                                           |
| crypto_pyaes               | 76.7 ms                                                | 75.9 ms: 1.01x faster                                                           |
| scimark_monte_carlo        | 70.7 ms                                                | 70.1 ms: 1.01x faster                                                           |
| pprint_pformat             | 1.55 sec                                               | 1.54 sec: 1.01x faster                                                          |
| bench_thread_pool          | 834 us                                                 | 830 us: 1.01x faster                                                            |
| scimark_lu                 | 116 ms                                                 | 116 ms: 1.00x faster                                                            |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.00x faster                                                           |
| sqlglot_optimize           | 55.3 ms                                                | 55.1 ms: 1.00x faster                                                           |
| deepcopy                   | 365 us                                                 | 366 us: 1.00x slower                                                            |
| pprint_safe_repr           | 747 ms                                                 | 752 ms: 1.01x slower                                                            |
| float                      | 78.9 ms                                                | 79.5 ms: 1.01x slower                                                           |
| json                       | 5.24 ms                                                | 5.31 ms: 1.01x slower                                                           |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                                            |
| dulwich_log                | 64.6 ms                                                | 65.8 ms: 1.02x slower                                                           |
| thrift                     | 784 us                                                 | 801 us: 1.02x slower                                                            |
| pycparser                  | 1.19 sec                                               | 1.21 sec: 1.02x slower                                                          |
| 2to3                       | 264 ms                                                 | 270 ms: 1.02x slower                                                            |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.15 ms: 1.03x slower                                                           |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                                            |
| deepcopy_reduce            | 3.22 us                                                | 3.31 us: 1.03x slower                                                           |
| regex_effbot               | 3.51 ms                                                | 3.62 ms: 1.03x slower                                                           |
| genshi_text                | 22.5 ms                                                | 23.3 ms: 1.03x slower                                                           |
| scimark_sor                | 121 ms                                                 | 126 ms: 1.03x slower                                                            |
| pickle_dict                | 34.6 us                                                | 35.9 us: 1.04x slower                                                           |
| unpickle_list              | 5.21 us                                                | 5.41 us: 1.04x slower                                                           |
| html5lib                   | 64.8 ms                                                | 67.4 ms: 1.04x slower                                                           |
| docutils                   | 2.66 sec                                               | 2.79 sec: 1.05x slower                                                          |
| django_template            | 33.5 ms                                                | 35.3 ms: 1.05x slower                                                           |
| xml_etree_process          | 56.9 ms                                                | 60.3 ms: 1.06x slower                                                           |
| spectral_norm              | 108 ms                                                 | 116 ms: 1.07x slower                                                            |
| xml_etree_generate         | 81.1 ms                                                | 87.1 ms: 1.08x slower                                                           |
| pyflate                    | 434 ms                                                 | 467 ms: 1.08x slower                                                            |
| scimark_fft                | 345 ms                                                 | 374 ms: 1.08x slower                                                            |
| mako                       | 10.7 ms                                                | 11.7 ms: 1.09x slower                                                           |
| pickle                     | 11.0 us                                                | 12.0 us: 1.09x slower                                                           |
| regex_dna                  | 205 ms                                                 | 228 ms: 1.11x slower                                                            |
| unpickle                   | 13.8 us                                                | 15.5 us: 1.12x slower                                                           |
| regex_v8                   | 22.9 ms                                                | 26.0 ms: 1.13x slower                                                           |
| sqlite_synth               | 2.57 us                                                | 2.95 us: 1.15x slower                                                           |
| pickle_list                | 4.59 us                                                | 5.30 us: 1.16x slower                                                           |
| coverage                   | 78.8 ms                                                | 92.3 ms: 1.17x slower                                                           |
| python_startup_no_site     | 6.01 ms                                                | 7.07 ms: 1.18x slower                                                           |
| async_generators           | 374 ms                                                 | 447 ms: 1.20x slower                                                            |
| telco                      | 6.86 ms                                                | 8.45 ms: 1.23x slower                                                           |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                           |
| create_gc_cycles           | 1.43 ms                                                | 1.78 ms: 1.24x slower                                                           |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                                    |

Benchmark hidden because not significant (1): fannkuch
Ignored benchmarks (10) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, dask, djangocms, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.12% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x