# Results vs. 3.11.0

- fork: faster-cpython
- ref: interpreter_reentry_
- machine: linux-x86_64
- commit hash: 8069375
- commit date: 2024-04-02
- overall geometric mean: 1.08x faster
- HPT reliability: 99.94%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 268 ms: 1.01x slower                                                             |
| chameleon      | 6.70 ms                                                | 6.81 ms: 1.02x slower                                                            |
| docutils       | 2.66 sec                                               | 2.77 sec: 1.04x slower                                                           |
| html5lib       | 64.8 ms                                                | 66.7 ms: 1.03x slower                                                            |
| tornado_http   | 98.1 ms                                                | 94.7 ms: 1.04x faster                                                            |
| Geometric mean | (ref)                                                  | 1.01x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_memoization     | 639 ms                                                 | 438 ms: 1.46x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 337 ms: 1.46x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 900 ms: 1.43x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 449 ms: 1.40x faster                                                             |
| async_tree_none            | 528 ms                                                 | 383 ms: 1.38x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 944 ms: 1.37x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 587 ms: 1.30x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 599 ms: 1.25x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.38x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 87.7 ms: 1.09x faster                                                            |
| float          | 78.9 ms                                                | 76.6 ms: 1.03x faster                                                            |
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                                             |
| Geometric mean | (ref)                                                  | 1.05x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 133 ms: 1.06x faster                                                             |
| regex_effbot   | 3.51 ms                                                | 3.65 ms: 1.04x slower                                                            |
| regex_dna      | 205 ms                                                 | 220 ms: 1.08x slower                                                             |
| regex_v8       | 22.9 ms                                                | 24.7 ms: 1.08x slower                                                            |
| Geometric mean | (ref)                                                  | 1.03x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                            |
| unpickle_pure_python | 242 us                                                 | 218 us: 1.11x faster                                                             |
| pickle_pure_python   | 320 us                                                 | 301 us: 1.06x faster                                                             |
| tomli_loads          | 2.30 sec                                               | 2.22 sec: 1.04x faster                                                           |
| json_loads           | 29.2 us                                                | 28.4 us: 1.03x faster                                                            |
| xml_etree_parse      | 164 ms                                                 | 161 ms: 1.02x faster                                                             |
| xml_etree_iterparse  | 108 ms                                                 | 106 ms: 1.02x faster                                                             |
| pickle_dict          | 34.6 us                                                | 34.0 us: 1.02x faster                                                            |
| unpickle_list        | 5.21 us                                                | 5.31 us: 1.02x slower                                                            |
| xml_etree_process    | 56.9 ms                                                | 59.5 ms: 1.05x slower                                                            |
| pickle               | 11.0 us                                                | 11.7 us: 1.06x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 86.4 ms: 1.07x slower                                                            |
| pickle_list          | 4.59 us                                                | 4.94 us: 1.08x slower                                                            |
| unpickle             | 13.8 us                                                | 16.2 us: 1.17x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.7 ms: 1.25x slower                                                            |
| python_startup_no_site | 6.01 ms                                                | 9.03 ms: 1.50x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.37x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 52.5 ms: 1.02x faster                                                            |
| mako            | 10.7 ms                                                | 10.9 ms: 1.02x slower                                                            |
| django_template | 33.5 ms                                                | 34.5 ms: 1.03x slower                                                            |
| genshi_text     | 22.5 ms                                                | 24.3 ms: 1.08x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-faster%2dcpython-interpreter_reentry_-3.13.0a5+-8069375 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 114 us: 4.54x faster                                                             |
| generators                 | 74.9 ms                                                | 30.0 ms: 2.49x faster                                                            |
| asyncio_tcp                | 875 ms                                                 | 500 ms: 1.75x faster                                                             |
| pylint                     | 476 ms                                                 | 280 ms: 1.70x faster                                                             |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.83 sec: 1.69x faster                                                           |
| async_tree_memoization     | 639 ms                                                 | 438 ms: 1.46x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 337 ms: 1.46x faster                                                             |
| comprehensions             | 23.6 us                                                | 16.4 us: 1.43x faster                                                            |
| async_tree_io              | 1.29 sec                                               | 900 ms: 1.43x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 449 ms: 1.40x faster                                                             |
| async_tree_none            | 528 ms                                                 | 383 ms: 1.38x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 944 ms: 1.37x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 587 ms: 1.30x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                            |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 599 ms: 1.25x faster                                                             |
| deltablue                  | 3.92 ms                                                | 3.17 ms: 1.24x faster                                                            |
| chaos                      | 71.9 ms                                                | 59.8 ms: 1.20x faster                                                            |
| coroutines                 | 27.0 ms                                                | 22.6 ms: 1.20x faster                                                            |
| richards_super             | 61.9 ms                                                | 51.8 ms: 1.19x faster                                                            |
| raytrace                   | 309 ms                                                 | 261 ms: 1.18x faster                                                             |
| hexiom                     | 6.89 ms                                                | 6.09 ms: 1.13x faster                                                            |
| sqlglot_parse              | 1.43 ms                                                | 1.27 ms: 1.13x faster                                                            |
| gc_traversal               | 4.01 ms                                                | 3.57 ms: 1.12x faster                                                            |
| unpickle_pure_python       | 242 us                                                 | 218 us: 1.11x faster                                                             |
| sqlglot_transpile          | 1.75 ms                                                | 1.59 ms: 1.10x faster                                                            |
| logging_silent             | 111 ns                                                 | 101 ns: 1.10x faster                                                             |
| sympy_sum                  | 169 ms                                                 | 153 ms: 1.10x faster                                                             |
| nbody                      | 96.0 ms                                                | 87.7 ms: 1.09x faster                                                            |
| richards                   | 49.8 ms                                                | 45.6 ms: 1.09x faster                                                            |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.61 ms: 1.09x faster                                                            |
| nqueens                    | 87.9 ms                                                | 80.7 ms: 1.09x faster                                                            |
| sympy_str                  | 297 ms                                                 | 274 ms: 1.09x faster                                                             |
| mdp                        | 2.77 sec                                               | 2.56 sec: 1.08x faster                                                           |
| sympy_integrate            | 21.5 ms                                                | 20.0 ms: 1.07x faster                                                            |
| go                         | 149 ms                                                 | 139 ms: 1.07x faster                                                             |
| deepcopy_memo              | 40.2 us                                                | 37.7 us: 1.07x faster                                                            |
| regex_compile              | 141 ms                                                 | 133 ms: 1.06x faster                                                             |
| pickle_pure_python         | 320 us                                                 | 301 us: 1.06x faster                                                             |
| scimark_monte_carlo        | 70.7 ms                                                | 66.8 ms: 1.06x faster                                                            |
| logging_format             | 6.81 us                                                | 6.45 us: 1.06x faster                                                            |
| logging_simple             | 6.22 us                                                | 5.90 us: 1.05x faster                                                            |
| djangocms                  | 33.5 us                                                | 31.9 us: 1.05x faster                                                            |
| sympy_expand               | 484 ms                                                 | 463 ms: 1.05x faster                                                             |
| deepcopy                   | 365 us                                                 | 350 us: 1.04x faster                                                             |
| sqlglot_normalize          | 113 ms                                                 | 108 ms: 1.04x faster                                                             |
| tomli_loads                | 2.30 sec                                               | 2.22 sec: 1.04x faster                                                           |
| tornado_http               | 98.1 ms                                                | 94.7 ms: 1.04x faster                                                            |
| float                      | 78.9 ms                                                | 76.6 ms: 1.03x faster                                                            |
| crypto_pyaes               | 76.7 ms                                                | 74.4 ms: 1.03x faster                                                            |
| json_loads                 | 29.2 us                                                | 28.4 us: 1.03x faster                                                            |
| deepcopy_reduce            | 3.22 us                                                | 3.13 us: 1.03x faster                                                            |
| scimark_lu                 | 116 ms                                                 | 113 ms: 1.03x faster                                                             |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                                             |
| fannkuch                   | 405 ms                                                 | 396 ms: 1.02x faster                                                             |
| xml_etree_parse            | 164 ms                                                 | 161 ms: 1.02x faster                                                             |
| xml_etree_iterparse        | 108 ms                                                 | 106 ms: 1.02x faster                                                             |
| genshi_xml                 | 53.4 ms                                                | 52.5 ms: 1.02x faster                                                            |
| pickle_dict                | 34.6 us                                                | 34.0 us: 1.02x faster                                                            |
| pprint_pformat             | 1.55 sec                                               | 1.53 sec: 1.01x faster                                                           |
| sqlglot_optimize           | 55.3 ms                                                | 54.5 ms: 1.01x faster                                                            |
| bench_thread_pool          | 834 us                                                 | 828 us: 1.01x faster                                                             |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                            |
| meteor_contest             | 109 ms                                                 | 108 ms: 1.01x faster                                                             |
| pathlib                    | 18.5 ms                                                | 18.7 ms: 1.01x slower                                                            |
| json                       | 5.24 ms                                                | 5.29 ms: 1.01x slower                                                            |
| 2to3                       | 264 ms                                                 | 268 ms: 1.01x slower                                                             |
| chameleon                  | 6.70 ms                                                | 6.81 ms: 1.02x slower                                                            |
| unpickle_list              | 5.21 us                                                | 5.31 us: 1.02x slower                                                            |
| mako                       | 10.7 ms                                                | 10.9 ms: 1.02x slower                                                            |
| django_template            | 33.5 ms                                                | 34.5 ms: 1.03x slower                                                            |
| html5lib                   | 64.8 ms                                                | 66.7 ms: 1.03x slower                                                            |
| thrift                     | 784 us                                                 | 810 us: 1.03x slower                                                             |
| asyncio_websockets         | 550 ms                                                 | 569 ms: 1.03x slower                                                             |
| dulwich_log                | 64.6 ms                                                | 66.8 ms: 1.03x slower                                                            |
| docutils                   | 2.66 sec                                               | 2.77 sec: 1.04x slower                                                           |
| scimark_fft                | 345 ms                                                 | 359 ms: 1.04x slower                                                             |
| regex_effbot               | 3.51 ms                                                | 3.65 ms: 1.04x slower                                                            |
| xml_etree_process          | 56.9 ms                                                | 59.5 ms: 1.05x slower                                                            |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                            |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                                            |
| pickle                     | 11.0 us                                                | 11.7 us: 1.06x slower                                                            |
| xml_etree_generate         | 81.1 ms                                                | 86.4 ms: 1.07x slower                                                            |
| mypy2                      | 686 ms                                                 | 734 ms: 1.07x slower                                                             |
| regex_dna                  | 205 ms                                                 | 220 ms: 1.08x slower                                                             |
| unpack_sequence            | 43.5 ns                                                | 46.8 ns: 1.08x slower                                                            |
| pickle_list                | 4.59 us                                                | 4.94 us: 1.08x slower                                                            |
| genshi_text                | 22.5 ms                                                | 24.3 ms: 1.08x slower                                                            |
| pyflate                    | 434 ms                                                 | 469 ms: 1.08x slower                                                             |
| regex_v8                   | 22.9 ms                                                | 24.7 ms: 1.08x slower                                                            |
| sqlite_synth               | 2.57 us                                                | 2.89 us: 1.12x slower                                                            |
| create_gc_cycles           | 1.43 ms                                                | 1.67 ms: 1.16x slower                                                            |
| unpickle                   | 13.8 us                                                | 16.2 us: 1.17x slower                                                            |
| async_generators           | 374 ms                                                 | 442 ms: 1.18x slower                                                             |
| coverage                   | 78.8 ms                                                | 97.3 ms: 1.24x slower                                                            |
| telco                      | 6.86 ms                                                | 8.54 ms: 1.24x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.7 ms: 1.25x slower                                                            |
| python_startup_no_site     | 6.01 ms                                                | 9.03 ms: 1.50x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                                     |

Benchmark hidden because not significant (5): pycparser, scimark_sor, pprint_safe_repr, spectral_norm, dask
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.94% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.02x