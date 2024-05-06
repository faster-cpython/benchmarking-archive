# Results vs. 3.11.0

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 198ceb6
- commit date: 2024-04-03
- overall geometric mean: 1.06x faster
- HPT reliability: 97.05%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 266 ms: 1.01x slower                                                             |
| chameleon      | 6.70 ms                                                | 6.86 ms: 1.02x slower                                                            |
| docutils       | 2.66 sec                                               | 2.78 sec: 1.04x slower                                                           |
| html5lib       | 64.8 ms                                                | 66.1 ms: 1.02x slower                                                            |
| tornado_http   | 98.1 ms                                                | 95.6 ms: 1.03x faster                                                            |
| Geometric mean | (ref)                                                  | 1.01x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 626 ms                                                 | 439 ms: 1.43x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 919 ms: 1.41x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 350 ms: 1.40x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 920 ms: 1.40x faster                                                             |
| async_tree_none            | 528 ms                                                 | 378 ms: 1.40x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 463 ms: 1.38x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 594 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.36x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 191 ms: 1.02x faster                                                             |
| float          | 78.9 ms                                                | 80.8 ms: 1.02x slower                                                            |
| nbody          | 96.0 ms                                                | 120 ms: 1.25x slower                                                             |
| Geometric mean | (ref)                                                  | 1.08x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 135 ms: 1.05x faster                                                             |
| regex_effbot   | 3.51 ms                                                | 3.73 ms: 1.07x slower                                                            |
| regex_dna      | 205 ms                                                 | 223 ms: 1.09x slower                                                             |
| regex_v8       | 22.9 ms                                                | 25.3 ms: 1.11x slower                                                            |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                            |
| unpickle_pure_python | 242 us                                                 | 215 us: 1.12x faster                                                             |
| pickle_pure_python   | 320 us                                                 | 301 us: 1.06x faster                                                             |
| json_loads           | 29.2 us                                                | 28.5 us: 1.02x faster                                                            |
| tomli_loads          | 2.30 sec                                               | 2.26 sec: 1.02x faster                                                           |
| xml_etree_parse      | 164 ms                                                 | 161 ms: 1.02x faster                                                             |
| pickle_dict          | 34.6 us                                                | 34.0 us: 1.02x faster                                                            |
| unpickle_list        | 5.21 us                                                | 5.33 us: 1.02x slower                                                            |
| xml_etree_process    | 56.9 ms                                                | 59.6 ms: 1.05x slower                                                            |
| pickle               | 11.0 us                                                | 11.6 us: 1.06x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 85.9 ms: 1.06x slower                                                            |
| pickle_list          | 4.59 us                                                | 4.93 us: 1.07x slower                                                            |
| unpickle             | 13.8 us                                                | 16.1 us: 1.17x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| python_startup_no_site | 6.01 ms                                                | 8.89 ms: 1.48x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.35x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 51.2 ms: 1.04x faster                                                            |
| mako            | 10.7 ms                                                | 10.9 ms: 1.03x slower                                                            |
| django_template | 33.5 ms                                                | 35.1 ms: 1.05x slower                                                            |
| genshi_text     | 22.5 ms                                                | 23.7 ms: 1.05x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-198ceb6 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 111 us: 4.67x faster                                                             |
| generators                 | 74.9 ms                                                | 30.4 ms: 2.47x faster                                                            |
| asyncio_tcp                | 875 ms                                                 | 500 ms: 1.75x faster                                                             |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.83 sec: 1.70x faster                                                           |
| pylint                     | 476 ms                                                 | 319 ms: 1.49x faster                                                             |
| comprehensions             | 23.6 us                                                | 16.5 us: 1.43x faster                                                            |
| async_tree_memoization_tg  | 626 ms                                                 | 439 ms: 1.43x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 919 ms: 1.41x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 350 ms: 1.40x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 920 ms: 1.40x faster                                                             |
| async_tree_none            | 528 ms                                                 | 378 ms: 1.40x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 463 ms: 1.38x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 594 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 10.7 ms: 1.25x faster                                                            |
| deltablue                  | 3.92 ms                                                | 3.23 ms: 1.22x faster                                                            |
| richards_super             | 61.9 ms                                                | 51.7 ms: 1.20x faster                                                            |
| hexiom                     | 6.89 ms                                                | 6.13 ms: 1.12x faster                                                            |
| unpickle_pure_python       | 242 us                                                 | 215 us: 1.12x faster                                                             |
| coroutines                 | 27.0 ms                                                | 24.1 ms: 1.12x faster                                                            |
| logging_silent             | 111 ns                                                 | 99.9 ns: 1.11x faster                                                            |
| sympy_sum                  | 169 ms                                                 | 152 ms: 1.11x faster                                                             |
| sqlglot_parse              | 1.43 ms                                                | 1.30 ms: 1.10x faster                                                            |
| sqlglot_transpile          | 1.75 ms                                                | 1.60 ms: 1.09x faster                                                            |
| richards                   | 49.8 ms                                                | 45.7 ms: 1.09x faster                                                            |
| sympy_str                  | 297 ms                                                 | 273 ms: 1.09x faster                                                             |
| gc_traversal               | 4.01 ms                                                | 3.73 ms: 1.08x faster                                                            |
| sympy_integrate            | 21.5 ms                                                | 20.0 ms: 1.07x faster                                                            |
| raytrace                   | 309 ms                                                 | 288 ms: 1.07x faster                                                             |
| pickle_pure_python         | 320 us                                                 | 301 us: 1.06x faster                                                             |
| deepcopy_memo              | 40.2 us                                                | 37.9 us: 1.06x faster                                                            |
| nqueens                    | 87.9 ms                                                | 83.0 ms: 1.06x faster                                                            |
| djangocms                  | 33.5 us                                                | 31.9 us: 1.05x faster                                                            |
| logging_simple             | 6.22 us                                                | 5.91 us: 1.05x faster                                                            |
| regex_compile              | 141 ms                                                 | 135 ms: 1.05x faster                                                             |
| chaos                      | 71.9 ms                                                | 68.7 ms: 1.05x faster                                                            |
| mdp                        | 2.77 sec                                               | 2.66 sec: 1.04x faster                                                           |
| sympy_expand               | 484 ms                                                 | 464 ms: 1.04x faster                                                             |
| go                         | 149 ms                                                 | 142 ms: 1.04x faster                                                             |
| genshi_xml                 | 53.4 ms                                                | 51.2 ms: 1.04x faster                                                            |
| logging_format             | 6.81 us                                                | 6.56 us: 1.04x faster                                                            |
| pprint_pformat             | 1.55 sec                                               | 1.51 sec: 1.03x faster                                                           |
| deepcopy                   | 365 us                                                 | 355 us: 1.03x faster                                                             |
| sqlglot_normalize          | 113 ms                                                 | 110 ms: 1.03x faster                                                             |
| tornado_http               | 98.1 ms                                                | 95.6 ms: 1.03x faster                                                            |
| json_loads                 | 29.2 us                                                | 28.5 us: 1.02x faster                                                            |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.02x faster                                                           |
| tomli_loads                | 2.30 sec                                               | 2.26 sec: 1.02x faster                                                           |
| xml_etree_parse            | 164 ms                                                 | 161 ms: 1.02x faster                                                             |
| pprint_safe_repr           | 747 ms                                                 | 734 ms: 1.02x faster                                                             |
| pickle_dict                | 34.6 us                                                | 34.0 us: 1.02x faster                                                            |
| pidigits                   | 194 ms                                                 | 191 ms: 1.02x faster                                                             |
| deepcopy_reduce            | 3.22 us                                                | 3.17 us: 1.01x faster                                                            |
| crypto_pyaes               | 76.7 ms                                                | 75.9 ms: 1.01x faster                                                            |
| bench_thread_pool          | 834 us                                                 | 827 us: 1.01x faster                                                             |
| meteor_contest             | 109 ms                                                 | 108 ms: 1.01x faster                                                             |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                            |
| sqlglot_optimize           | 55.3 ms                                                | 55.2 ms: 1.00x faster                                                            |
| create_gc_cycles           | 1.43 ms                                                | 1.44 ms: 1.00x slower                                                            |
| 2to3                       | 264 ms                                                 | 266 ms: 1.01x slower                                                             |
| pathlib                    | 18.5 ms                                                | 18.8 ms: 1.01x slower                                                            |
| json                       | 5.24 ms                                                | 5.33 ms: 1.02x slower                                                            |
| html5lib                   | 64.8 ms                                                | 66.1 ms: 1.02x slower                                                            |
| scimark_lu                 | 116 ms                                                 | 119 ms: 1.02x slower                                                             |
| unpickle_list              | 5.21 us                                                | 5.33 us: 1.02x slower                                                            |
| float                      | 78.9 ms                                                | 80.8 ms: 1.02x slower                                                            |
| chameleon                  | 6.70 ms                                                | 6.86 ms: 1.02x slower                                                            |
| mako                       | 10.7 ms                                                | 10.9 ms: 1.03x slower                                                            |
| thrift                     | 784 us                                                 | 806 us: 1.03x slower                                                             |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                                             |
| scimark_monte_carlo        | 70.7 ms                                                | 72.8 ms: 1.03x slower                                                            |
| docutils                   | 2.66 sec                                               | 2.78 sec: 1.04x slower                                                           |
| django_template            | 33.5 ms                                                | 35.1 ms: 1.05x slower                                                            |
| xml_etree_process          | 56.9 ms                                                | 59.6 ms: 1.05x slower                                                            |
| genshi_text                | 22.5 ms                                                | 23.7 ms: 1.05x slower                                                            |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                            |
| dulwich_log                | 64.6 ms                                                | 68.2 ms: 1.06x slower                                                            |
| pickle                     | 11.0 us                                                | 11.6 us: 1.06x slower                                                            |
| xml_etree_generate         | 81.1 ms                                                | 85.9 ms: 1.06x slower                                                            |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                                            |
| regex_effbot               | 3.51 ms                                                | 3.73 ms: 1.07x slower                                                            |
| pickle_list                | 4.59 us                                                | 4.93 us: 1.07x slower                                                            |
| mypy2                      | 686 ms                                                 | 739 ms: 1.08x slower                                                             |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.45 ms: 1.08x slower                                                            |
| regex_dna                  | 205 ms                                                 | 223 ms: 1.09x slower                                                             |
| regex_v8                   | 22.9 ms                                                | 25.3 ms: 1.11x slower                                                            |
| scimark_sor                | 121 ms                                                 | 134 ms: 1.11x slower                                                             |
| pyflate                    | 434 ms                                                 | 482 ms: 1.11x slower                                                             |
| sqlite_synth               | 2.57 us                                                | 2.94 us: 1.14x slower                                                            |
| unpickle                   | 13.8 us                                                | 16.1 us: 1.17x slower                                                            |
| async_generators           | 374 ms                                                 | 441 ms: 1.18x slower                                                             |
| scimark_fft                | 345 ms                                                 | 422 ms: 1.22x slower                                                             |
| telco                      | 6.86 ms                                                | 8.41 ms: 1.23x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| coverage                   | 78.8 ms                                                | 98.1 ms: 1.25x slower                                                            |
| nbody                      | 96.0 ms                                                | 120 ms: 1.25x slower                                                             |
| spectral_norm              | 108 ms                                                 | 140 ms: 1.30x slower                                                             |
| python_startup_no_site     | 6.01 ms                                                | 8.89 ms: 1.48x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                     |

Benchmark hidden because not significant (3): fannkuch, xml_etree_iterparse, dask
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 97.05% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.01x