# Results vs. 3.11.0

- fork: faster-cpython
- ref: flag_object_maybe_in
- machine: linux-x86_64
- commit hash: bb874c3
- commit date: 2024-06-07
- overall geometric mean: 1.06x faster
- HPT reliability: 87.81%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240607-linux-x86_64-faster%2dcpython-flag_object_maybe_in-3.14.0a0-bb874c3 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 272 ms: 1.03x slower                                                            |
| docutils       | 2.66 sec                                               | 2.78 sec: 1.04x slower                                                          |
| html5lib       | 64.8 ms                                                | 66.9 ms: 1.03x slower                                                           |
| tornado_http   | 98.1 ms                                                | 94.8 ms: 1.03x faster                                                           |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240607-linux-x86_64-faster%2dcpython-flag_object_maybe_in-3.14.0a0-bb874c3 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 344 ms: 1.43x faster                                                            |
| async_tree_memoization_tg  | 626 ms                                                 | 448 ms: 1.40x faster                                                            |
| async_tree_none            | 528 ms                                                 | 378 ms: 1.40x faster                                                            |
| async_tree_io_tg           | 1.29 sec                                               | 927 ms: 1.40x faster                                                            |
| async_tree_io              | 1.29 sec                                               | 957 ms: 1.34x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 478 ms: 1.34x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 596 ms: 1.28x faster                                                            |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 632 ms: 1.18x faster                                                            |
| Geometric mean             | (ref)                                                  | 1.34x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240607-linux-x86_64-faster%2dcpython-flag_object_maybe_in-3.14.0a0-bb874c3 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                                            |
| float          | 78.9 ms                                                | 79.7 ms: 1.01x slower                                                           |
| nbody          | 96.0 ms                                                | 97.0 ms: 1.01x slower                                                           |
| Geometric mean | (ref)                                                  | 1.00x slower                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240607-linux-x86_64-faster%2dcpython-flag_object_maybe_in-3.14.0a0-bb874c3 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 135 ms: 1.05x faster                                                            |
| regex_effbot   | 3.51 ms                                                | 3.74 ms: 1.07x slower                                                           |
| regex_v8       | 22.9 ms                                                | 24.8 ms: 1.08x slower                                                           |
| regex_dna      | 205 ms                                                 | 222 ms: 1.08x slower                                                            |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240607-linux-x86_64-faster%2dcpython-flag_object_maybe_in-3.14.0a0-bb874c3 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                           |
| unpickle_pure_python | 242 us                                                 | 223 us: 1.09x faster                                                            |
| tomli_loads          | 2.30 sec                                               | 2.21 sec: 1.04x faster                                                          |
| xml_etree_parse      | 164 ms                                                 | 159 ms: 1.03x faster                                                            |
| pickle_dict          | 34.6 us                                                | 33.7 us: 1.03x faster                                                           |
| pickle_pure_python   | 320 us                                                 | 312 us: 1.03x faster                                                            |
| json_loads           | 29.2 us                                                | 28.8 us: 1.01x faster                                                           |
| unpickle_list        | 5.21 us                                                | 5.38 us: 1.03x slower                                                           |
| pickle               | 11.0 us                                                | 11.6 us: 1.06x slower                                                           |
| xml_etree_process    | 56.9 ms                                                | 61.1 ms: 1.07x slower                                                           |
| xml_etree_generate   | 81.1 ms                                                | 87.3 ms: 1.08x slower                                                           |
| unpickle             | 13.8 us                                                | 15.2 us: 1.10x slower                                                           |
| pickle_list          | 4.59 us                                                | 5.15 us: 1.12x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                                    |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240607-linux-x86_64-faster%2dcpython-flag_object_maybe_in-3.14.0a0-bb874c3 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.12 ms: 1.18x slower                                                           |
| python_startup         | 8.56 ms                                                | 10.7 ms: 1.25x slower                                                           |
| Geometric mean         | (ref)                                                  | 1.22x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240607-linux-x86_64-faster%2dcpython-flag_object_maybe_in-3.14.0a0-bb874c3 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 52.1 ms: 1.02x faster                                                           |
| django_template | 33.5 ms                                                | 35.3 ms: 1.05x slower                                                           |
| genshi_text     | 22.5 ms                                                | 23.8 ms: 1.06x slower                                                           |
| mako            | 10.7 ms                                                | 11.5 ms: 1.08x slower                                                           |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240607-linux-x86_64-faster%2dcpython-flag_object_maybe_in-3.14.0a0-bb874c3 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 165 us: 3.15x faster                                                            |
| generators                 | 74.9 ms                                                | 29.6 ms: 2.53x faster                                                           |
| asyncio_tcp                | 875 ms                                                 | 500 ms: 1.75x faster                                                            |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                          |
| pylint                     | 476 ms                                                 | 316 ms: 1.51x faster                                                            |
| async_tree_none_tg         | 491 ms                                                 | 344 ms: 1.43x faster                                                            |
| comprehensions             | 23.6 us                                                | 16.8 us: 1.41x faster                                                           |
| async_tree_memoization_tg  | 626 ms                                                 | 448 ms: 1.40x faster                                                            |
| async_tree_none            | 528 ms                                                 | 378 ms: 1.40x faster                                                            |
| async_tree_io_tg           | 1.29 sec                                               | 927 ms: 1.40x faster                                                            |
| async_tree_io              | 1.29 sec                                               | 957 ms: 1.34x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 478 ms: 1.34x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 596 ms: 1.28x faster                                                            |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                           |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 632 ms: 1.18x faster                                                            |
| deltablue                  | 3.92 ms                                                | 3.34 ms: 1.17x faster                                                           |
| chaos                      | 71.9 ms                                                | 61.4 ms: 1.17x faster                                                           |
| coroutines                 | 27.0 ms                                                | 23.3 ms: 1.16x faster                                                           |
| pathlib                    | 18.5 ms                                                | 16.2 ms: 1.15x faster                                                           |
| raytrace                   | 309 ms                                                 | 273 ms: 1.13x faster                                                            |
| richards_super             | 61.9 ms                                                | 56.0 ms: 1.10x faster                                                           |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.09x faster                                                           |
| unpickle_pure_python       | 242 us                                                 | 223 us: 1.09x faster                                                            |
| hexiom                     | 6.89 ms                                                | 6.35 ms: 1.09x faster                                                           |
| logging_silent             | 111 ns                                                 | 102 ns: 1.08x faster                                                            |
| nqueens                    | 87.9 ms                                                | 81.2 ms: 1.08x faster                                                           |
| sympy_sum                  | 169 ms                                                 | 157 ms: 1.08x faster                                                            |
| sqlglot_transpile          | 1.75 ms                                                | 1.63 ms: 1.07x faster                                                           |
| mdp                        | 2.77 sec                                               | 2.59 sec: 1.07x faster                                                          |
| logging_simple             | 6.22 us                                                | 5.87 us: 1.06x faster                                                           |
| gc_traversal               | 4.01 ms                                                | 3.79 ms: 1.06x faster                                                           |
| sympy_str                  | 297 ms                                                 | 281 ms: 1.06x faster                                                            |
| logging_format             | 6.81 us                                                | 6.48 us: 1.05x faster                                                           |
| regex_compile              | 141 ms                                                 | 135 ms: 1.05x faster                                                            |
| tomli_loads                | 2.30 sec                                               | 2.21 sec: 1.04x faster                                                          |
| sympy_integrate            | 21.5 ms                                                | 20.7 ms: 1.04x faster                                                           |
| tornado_http               | 98.1 ms                                                | 94.8 ms: 1.03x faster                                                           |
| xml_etree_parse            | 164 ms                                                 | 159 ms: 1.03x faster                                                            |
| pickle_dict                | 34.6 us                                                | 33.7 us: 1.03x faster                                                           |
| pickle_pure_python         | 320 us                                                 | 312 us: 1.03x faster                                                            |
| genshi_xml                 | 53.4 ms                                                | 52.1 ms: 1.02x faster                                                           |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.02x faster                                                          |
| sympy_expand               | 484 ms                                                 | 475 ms: 1.02x faster                                                            |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                                            |
| sqlglot_normalize          | 113 ms                                                 | 111 ms: 1.02x faster                                                            |
| go                         | 149 ms                                                 | 146 ms: 1.01x faster                                                            |
| json_loads                 | 29.2 us                                                | 28.8 us: 1.01x faster                                                           |
| richards                   | 49.8 ms                                                | 49.4 ms: 1.01x faster                                                           |
| scimark_monte_carlo        | 70.7 ms                                                | 70.3 ms: 1.01x faster                                                           |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.00x faster                                                           |
| sqlglot_optimize           | 55.3 ms                                                | 55.6 ms: 1.01x slower                                                           |
| crypto_pyaes               | 76.7 ms                                                | 77.2 ms: 1.01x slower                                                           |
| bench_thread_pool          | 834 us                                                 | 840 us: 1.01x slower                                                            |
| pprint_pformat             | 1.55 sec                                               | 1.57 sec: 1.01x slower                                                          |
| float                      | 78.9 ms                                                | 79.7 ms: 1.01x slower                                                           |
| deepcopy                   | 365 us                                                 | 369 us: 1.01x slower                                                            |
| nbody                      | 96.0 ms                                                | 97.0 ms: 1.01x slower                                                           |
| fannkuch                   | 405 ms                                                 | 411 ms: 1.01x slower                                                            |
| dulwich_log                | 64.6 ms                                                | 65.6 ms: 1.02x slower                                                           |
| dask                       | 365 ms                                                 | 371 ms: 1.02x slower                                                            |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                                            |
| scimark_lu                 | 116 ms                                                 | 119 ms: 1.02x slower                                                            |
| deepcopy_reduce            | 3.22 us                                                | 3.29 us: 1.02x slower                                                           |
| json                       | 5.24 ms                                                | 5.38 ms: 1.03x slower                                                           |
| pprint_safe_repr           | 747 ms                                                 | 770 ms: 1.03x slower                                                            |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                            |
| 2to3                       | 264 ms                                                 | 272 ms: 1.03x slower                                                            |
| unpickle_list              | 5.21 us                                                | 5.38 us: 1.03x slower                                                           |
| html5lib                   | 64.8 ms                                                | 66.9 ms: 1.03x slower                                                           |
| thrift                     | 784 us                                                 | 810 us: 1.03x slower                                                            |
| docutils                   | 2.66 sec                                               | 2.78 sec: 1.04x slower                                                          |
| scimark_sor                | 121 ms                                                 | 127 ms: 1.05x slower                                                            |
| django_template            | 33.5 ms                                                | 35.3 ms: 1.05x slower                                                           |
| genshi_text                | 22.5 ms                                                | 23.8 ms: 1.06x slower                                                           |
| pickle                     | 11.0 us                                                | 11.6 us: 1.06x slower                                                           |
| regex_effbot               | 3.51 ms                                                | 3.74 ms: 1.07x slower                                                           |
| xml_etree_process          | 56.9 ms                                                | 61.1 ms: 1.07x slower                                                           |
| xml_etree_generate         | 81.1 ms                                                | 87.3 ms: 1.08x slower                                                           |
| mako                       | 10.7 ms                                                | 11.5 ms: 1.08x slower                                                           |
| regex_v8                   | 22.9 ms                                                | 24.8 ms: 1.08x slower                                                           |
| regex_dna                  | 205 ms                                                 | 222 ms: 1.08x slower                                                            |
| scimark_fft                | 345 ms                                                 | 376 ms: 1.09x slower                                                            |
| spectral_norm              | 108 ms                                                 | 118 ms: 1.09x slower                                                            |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.10x slower                                                           |
| pickle_list                | 4.59 us                                                | 5.15 us: 1.12x slower                                                           |
| sqlite_synth               | 2.57 us                                                | 2.93 us: 1.14x slower                                                           |
| coverage                   | 78.8 ms                                                | 92.4 ms: 1.17x slower                                                           |
| python_startup_no_site     | 6.01 ms                                                | 7.12 ms: 1.18x slower                                                           |
| pyflate                    | 434 ms                                                 | 514 ms: 1.18x slower                                                            |
| async_generators           | 374 ms                                                 | 449 ms: 1.20x slower                                                            |
| telco                      | 6.86 ms                                                | 8.41 ms: 1.23x slower                                                           |
| create_gc_cycles           | 1.43 ms                                                | 1.77 ms: 1.24x slower                                                           |
| python_startup             | 8.56 ms                                                | 10.7 ms: 1.25x slower                                                           |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                    |

Benchmark hidden because not significant (3): scimark_sparse_mat_mult, xml_etree_iterparse, deepcopy_memo
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, djangocms, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 87.81% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x