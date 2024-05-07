# Results vs. 3.11.0

- fork: faster-cpython
- ref: no_globals_builtins_
- machine: linux-x86_64
- commit hash: a701af9
- commit date: 2024-05-07
- overall geometric mean: 1.02x faster
- HPT reliability: 91.42%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240507-linux-x86_64-faster%2dcpython-no_globals_builtins_-3.13.0a6+-a701af9 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 281 ms: 1.06x slower                                                             |
| chameleon      | 6.70 ms                                                | 7.11 ms: 1.06x slower                                                            |
| docutils       | 2.66 sec                                               | 3.00 sec: 1.13x slower                                                           |
| html5lib       | 64.8 ms                                                | 68.7 ms: 1.06x slower                                                            |
| tornado_http   | 98.1 ms                                                | 97.5 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                  | 1.06x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240507-linux-x86_64-faster%2dcpython-no_globals_builtins_-3.13.0a6+-a701af9 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 372 ms: 1.42x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 348 ms: 1.41x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 460 ms: 1.36x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 946 ms: 1.36x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 486 ms: 1.31x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 598 ms: 1.27x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 1.03 sec: 1.26x faster                                                           |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 633 ms: 1.18x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.32x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240507-linux-x86_64-faster%2dcpython-no_globals_builtins_-3.13.0a6+-a701af9 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 81.2 ms: 1.18x faster                                                            |
| float          | 78.9 ms                                                | 71.7 ms: 1.10x faster                                                            |
| pidigits       | 194 ms                                                 | 188 ms: 1.03x faster                                                             |
| Geometric mean | (ref)                                                  | 1.10x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240507-linux-x86_64-faster%2dcpython-no_globals_builtins_-3.13.0a6+-a701af9 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 140 ms: 1.01x faster                                                             |
| regex_effbot   | 3.51 ms                                                | 3.73 ms: 1.06x slower                                                            |
| regex_dna      | 205 ms                                                 | 228 ms: 1.11x slower                                                             |
| regex_v8       | 22.9 ms                                                | 25.7 ms: 1.12x slower                                                            |
| Geometric mean | (ref)                                                  | 1.07x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240507-linux-x86_64-faster%2dcpython-no_globals_builtins_-3.13.0a6+-a701af9 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.3 ms: 1.30x faster                                                            |
| tomli_loads          | 2.30 sec                                               | 1.98 sec: 1.16x faster                                                           |
| unpickle_pure_python | 242 us                                                 | 222 us: 1.09x faster                                                             |
| xml_etree_iterparse  | 108 ms                                                 | 101 ms: 1.07x faster                                                             |
| xml_etree_parse      | 164 ms                                                 | 154 ms: 1.07x faster                                                             |
| pickle_pure_python   | 320 us                                                 | 301 us: 1.06x faster                                                             |
| pickle_dict          | 34.6 us                                                | 33.1 us: 1.04x faster                                                            |
| json_loads           | 29.2 us                                                | 28.8 us: 1.01x faster                                                            |
| unpickle_list        | 5.21 us                                                | 5.30 us: 1.02x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 83.7 ms: 1.03x slower                                                            |
| xml_etree_process    | 56.9 ms                                                | 58.9 ms: 1.04x slower                                                            |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                                            |
| pickle_list          | 4.59 us                                                | 5.05 us: 1.10x slower                                                            |
| unpickle             | 13.8 us                                                | 15.7 us: 1.14x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240507-linux-x86_64-faster%2dcpython-no_globals_builtins_-3.13.0a6+-a701af9 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.65 ms: 1.27x slower                                                            |
| python_startup         | 8.56 ms                                                | 11.2 ms: 1.30x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.29x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240507-linux-x86_64-faster%2dcpython-no_globals_builtins_-3.13.0a6+-a701af9 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 9.60 ms: 1.11x faster                                                            |
| django_template | 33.5 ms                                                | 36.9 ms: 1.10x slower                                                            |
| genshi_xml      | 53.4 ms                                                | 59.0 ms: 1.10x slower                                                            |
| genshi_text     | 22.5 ms                                                | 25.1 ms: 1.12x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.05x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240507-linux-x86_64-faster%2dcpython-no_globals_builtins_-3.13.0a6+-a701af9 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 174 us: 2.98x faster                                                             |
| generators                 | 74.9 ms                                                | 30.3 ms: 2.47x faster                                                            |
| asyncio_tcp                | 875 ms                                                 | 519 ms: 1.69x faster                                                             |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.68x faster                                                           |
| async_tree_none            | 528 ms                                                 | 372 ms: 1.42x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 348 ms: 1.41x faster                                                             |
| comprehensions             | 23.6 us                                                | 16.8 us: 1.40x faster                                                            |
| async_tree_memoization_tg  | 626 ms                                                 | 460 ms: 1.36x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 946 ms: 1.36x faster                                                             |
| pylint                     | 476 ms                                                 | 357 ms: 1.33x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 486 ms: 1.31x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 10.3 ms: 1.30x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 598 ms: 1.27x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 1.03 sec: 1.26x faster                                                           |
| richards_super             | 61.9 ms                                                | 49.5 ms: 1.25x faster                                                            |
| chaos                      | 71.9 ms                                                | 59.3 ms: 1.21x faster                                                            |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 633 ms: 1.18x faster                                                             |
| nbody                      | 96.0 ms                                                | 81.2 ms: 1.18x faster                                                            |
| coroutines                 | 27.0 ms                                                | 23.1 ms: 1.17x faster                                                            |
| tomli_loads                | 2.30 sec                                               | 1.98 sec: 1.16x faster                                                           |
| richards                   | 49.8 ms                                                | 43.1 ms: 1.15x faster                                                            |
| crypto_pyaes               | 76.7 ms                                                | 68.2 ms: 1.12x faster                                                            |
| mako                       | 10.7 ms                                                | 9.60 ms: 1.11x faster                                                            |
| raytrace                   | 309 ms                                                 | 279 ms: 1.11x faster                                                             |
| scimark_monte_carlo        | 70.7 ms                                                | 64.2 ms: 1.10x faster                                                            |
| float                      | 78.9 ms                                                | 71.7 ms: 1.10x faster                                                            |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.57 ms: 1.10x faster                                                            |
| fannkuch                   | 405 ms                                                 | 369 ms: 1.10x faster                                                             |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.10x faster                                                            |
| scimark_fft                | 345 ms                                                 | 316 ms: 1.09x faster                                                             |
| unpickle_pure_python       | 242 us                                                 | 222 us: 1.09x faster                                                             |
| deepcopy_memo              | 40.2 us                                                | 37.2 us: 1.08x faster                                                            |
| spectral_norm              | 108 ms                                                 | 100 ms: 1.08x faster                                                             |
| sqlglot_transpile          | 1.75 ms                                                | 1.63 ms: 1.07x faster                                                            |
| logging_simple             | 6.22 us                                                | 5.81 us: 1.07x faster                                                            |
| xml_etree_iterparse        | 108 ms                                                 | 101 ms: 1.07x faster                                                             |
| xml_etree_parse            | 164 ms                                                 | 154 ms: 1.07x faster                                                             |
| logging_format             | 6.81 us                                                | 6.40 us: 1.06x faster                                                            |
| pickle_pure_python         | 320 us                                                 | 301 us: 1.06x faster                                                             |
| mdp                        | 2.77 sec                                               | 2.61 sec: 1.06x faster                                                           |
| logging_silent             | 111 ns                                                 | 106 ns: 1.05x faster                                                             |
| pathlib                    | 18.5 ms                                                | 17.6 ms: 1.05x faster                                                            |
| hexiom                     | 6.89 ms                                                | 6.58 ms: 1.05x faster                                                            |
| pickle_dict                | 34.6 us                                                | 33.1 us: 1.04x faster                                                            |
| gc_traversal               | 4.01 ms                                                | 3.84 ms: 1.04x faster                                                            |
| deltablue                  | 3.92 ms                                                | 3.76 ms: 1.04x faster                                                            |
| pidigits                   | 194 ms                                                 | 188 ms: 1.03x faster                                                             |
| djangocms                  | 33.5 us                                                | 32.5 us: 1.03x faster                                                            |
| pprint_safe_repr           | 747 ms                                                 | 727 ms: 1.03x faster                                                             |
| pprint_pformat             | 1.55 sec                                               | 1.52 sec: 1.03x faster                                                           |
| nqueens                    | 87.9 ms                                                | 86.7 ms: 1.01x faster                                                            |
| json_loads                 | 29.2 us                                                | 28.8 us: 1.01x faster                                                            |
| regex_compile              | 141 ms                                                 | 140 ms: 1.01x faster                                                             |
| tornado_http               | 98.1 ms                                                | 97.5 ms: 1.01x faster                                                            |
| json                       | 5.24 ms                                                | 5.29 ms: 1.01x slower                                                            |
| sympy_str                  | 297 ms                                                 | 300 ms: 1.01x slower                                                             |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                                             |
| deepcopy                   | 365 us                                                 | 370 us: 1.01x slower                                                             |
| unpickle_list              | 5.21 us                                                | 5.30 us: 1.02x slower                                                            |
| sqlglot_normalize          | 113 ms                                                 | 115 ms: 1.02x slower                                                             |
| pycparser                  | 1.19 sec                                               | 1.21 sec: 1.02x slower                                                           |
| sympy_sum                  | 169 ms                                                 | 173 ms: 1.02x slower                                                             |
| sqlglot_optimize           | 55.3 ms                                                | 56.9 ms: 1.03x slower                                                            |
| thrift                     | 784 us                                                 | 809 us: 1.03x slower                                                             |
| xml_etree_generate         | 81.1 ms                                                | 83.7 ms: 1.03x slower                                                            |
| xml_etree_process          | 56.9 ms                                                | 58.9 ms: 1.04x slower                                                            |
| asyncio_websockets         | 550 ms                                                 | 570 ms: 1.04x slower                                                             |
| dask                       | 365 ms                                                 | 380 ms: 1.04x slower                                                             |
| bench_thread_pool          | 834 us                                                 | 869 us: 1.04x slower                                                             |
| pyflate                    | 434 ms                                                 | 453 ms: 1.05x slower                                                             |
| sympy_expand               | 484 ms                                                 | 511 ms: 1.05x slower                                                             |
| sympy_integrate            | 21.5 ms                                                | 22.7 ms: 1.06x slower                                                            |
| html5lib                   | 64.8 ms                                                | 68.7 ms: 1.06x slower                                                            |
| chameleon                  | 6.70 ms                                                | 7.11 ms: 1.06x slower                                                            |
| 2to3                       | 264 ms                                                 | 281 ms: 1.06x slower                                                             |
| regex_effbot               | 3.51 ms                                                | 3.73 ms: 1.06x slower                                                            |
| scimark_lu                 | 116 ms                                                 | 124 ms: 1.07x slower                                                             |
| scimark_sor                | 121 ms                                                 | 130 ms: 1.07x slower                                                             |
| dulwich_log                | 64.6 ms                                                | 70.1 ms: 1.09x slower                                                            |
| pickle                     | 11.0 us                                                | 12.0 us: 1.09x slower                                                            |
| coverage                   | 78.8 ms                                                | 86.3 ms: 1.10x slower                                                            |
| django_template            | 33.5 ms                                                | 36.9 ms: 1.10x slower                                                            |
| pickle_list                | 4.59 us                                                | 5.05 us: 1.10x slower                                                            |
| genshi_xml                 | 53.4 ms                                                | 59.0 ms: 1.10x slower                                                            |
| sqlite_synth               | 2.57 us                                                | 2.84 us: 1.11x slower                                                            |
| regex_dna                  | 205 ms                                                 | 228 ms: 1.11x slower                                                             |
| genshi_text                | 22.5 ms                                                | 25.1 ms: 1.12x slower                                                            |
| regex_v8                   | 22.9 ms                                                | 25.7 ms: 1.12x slower                                                            |
| aiohttp                    | 1.12 ms                                                | 1.25 ms: 1.12x slower                                                            |
| gunicorn                   | 1.20 ms                                                | 1.35 ms: 1.13x slower                                                            |
| docutils                   | 2.66 sec                                               | 3.00 sec: 1.13x slower                                                           |
| unpickle                   | 13.8 us                                                | 15.7 us: 1.14x slower                                                            |
| mypy2                      | 686 ms                                                 | 820 ms: 1.20x slower                                                             |
| async_generators           | 374 ms                                                 | 465 ms: 1.24x slower                                                             |
| create_gc_cycles           | 1.43 ms                                                | 1.82 ms: 1.27x slower                                                            |
| python_startup_no_site     | 6.01 ms                                                | 7.65 ms: 1.27x slower                                                            |
| flaskblogging              | 7.28 ms                                                | 9.31 ms: 1.28x slower                                                            |
| python_startup             | 8.56 ms                                                | 11.2 ms: 1.30x slower                                                            |
| telco                      | 6.86 ms                                                | 172 ms: 25.02x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                                     |

Benchmark hidden because not significant (3): bench_mp_pool, go, deepcopy_reduce
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 91.42% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.12x