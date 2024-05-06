# Results vs. 3.11.0

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: 99be8f6
- commit date: 2024-04-08
- overall geometric mean: 1.07x faster
- HPT reliability: 99.02%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 271 ms: 1.03x slower                                                             |
| chameleon      | 6.70 ms                                                | 6.87 ms: 1.03x slower                                                            |
| docutils       | 2.66 sec                                               | 2.83 sec: 1.06x slower                                                           |
| html5lib       | 64.8 ms                                                | 67.8 ms: 1.05x slower                                                            |
| tornado_http   | 98.1 ms                                                | 94.5 ms: 1.04x faster                                                            |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 350 ms: 1.51x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 333 ms: 1.48x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 918 ms: 1.41x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 918 ms: 1.40x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 459 ms: 1.39x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 603 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 607 ms: 1.23x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.39x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 89.4 ms: 1.07x faster                                                            |
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                                             |
| float          | 78.9 ms                                                | 77.5 ms: 1.02x faster                                                            |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 135 ms: 1.05x faster                                                             |
| regex_v8       | 22.9 ms                                                | 25.0 ms: 1.09x slower                                                            |
| regex_effbot   | 3.51 ms                                                | 3.85 ms: 1.10x slower                                                            |
| regex_dna      | 205 ms                                                 | 225 ms: 1.10x slower                                                             |
| Geometric mean | (ref)                                                  | 1.06x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.25x faster                                                            |
| unpickle_pure_python | 242 us                                                 | 225 us: 1.08x faster                                                             |
| pickle_pure_python   | 320 us                                                 | 300 us: 1.07x faster                                                             |
| tomli_loads          | 2.30 sec                                               | 2.17 sec: 1.06x faster                                                           |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.02x faster                                                             |
| json_loads           | 29.2 us                                                | 28.6 us: 1.02x faster                                                            |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                             |
| unpickle_list        | 5.21 us                                                | 5.27 us: 1.01x slower                                                            |
| pickle_dict          | 34.6 us                                                | 35.1 us: 1.01x slower                                                            |
| pickle               | 11.0 us                                                | 11.7 us: 1.07x slower                                                            |
| xml_etree_process    | 56.9 ms                                                | 60.9 ms: 1.07x slower                                                            |
| unpickle             | 13.8 us                                                | 14.9 us: 1.08x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 88.3 ms: 1.09x slower                                                            |
| pickle_list          | 4.59 us                                                | 5.14 us: 1.12x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.6 ms: 1.23x slower                                                            |
| python_startup_no_site | 6.01 ms                                                | 9.00 ms: 1.50x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.36x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml     | 53.4 ms                                                | 52.3 ms: 1.02x faster                                                            |
| mako           | 10.7 ms                                                | 10.9 ms: 1.02x slower                                                            |
| genshi_text    | 22.5 ms                                                | 24.2 ms: 1.08x slower                                                            |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-99be8f6 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 117 us: 4.43x faster                                                             |
| generators                 | 74.9 ms                                                | 29.7 ms: 2.52x faster                                                            |
| asyncio_tcp                | 875 ms                                                 | 503 ms: 1.74x faster                                                             |
| pylint                     | 476 ms                                                 | 279 ms: 1.71x faster                                                             |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                           |
| async_tree_none            | 528 ms                                                 | 350 ms: 1.51x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 333 ms: 1.48x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 442 ms: 1.42x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 918 ms: 1.41x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 918 ms: 1.40x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 459 ms: 1.39x faster                                                             |
| comprehensions             | 23.6 us                                                | 17.0 us: 1.39x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 603 ms: 1.26x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.25x faster                                                            |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 607 ms: 1.23x faster                                                             |
| deltablue                  | 3.92 ms                                                | 3.22 ms: 1.22x faster                                                            |
| chaos                      | 71.9 ms                                                | 60.1 ms: 1.20x faster                                                            |
| raytrace                   | 309 ms                                                 | 263 ms: 1.17x faster                                                             |
| richards_super             | 61.9 ms                                                | 53.0 ms: 1.17x faster                                                            |
| coroutines                 | 27.0 ms                                                | 24.1 ms: 1.12x faster                                                            |
| sqlglot_parse              | 1.43 ms                                                | 1.29 ms: 1.11x faster                                                            |
| logging_silent             | 111 ns                                                 | 101 ns: 1.10x faster                                                             |
| sqlglot_transpile          | 1.75 ms                                                | 1.59 ms: 1.10x faster                                                            |
| deepcopy_memo              | 40.2 us                                                | 36.9 us: 1.09x faster                                                            |
| logging_simple             | 6.22 us                                                | 5.73 us: 1.09x faster                                                            |
| logging_format             | 6.81 us                                                | 6.29 us: 1.08x faster                                                            |
| hexiom                     | 6.89 ms                                                | 6.36 ms: 1.08x faster                                                            |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.08x faster                                                             |
| unpickle_pure_python       | 242 us                                                 | 225 us: 1.08x faster                                                             |
| nbody                      | 96.0 ms                                                | 89.4 ms: 1.07x faster                                                            |
| nqueens                    | 87.9 ms                                                | 82.2 ms: 1.07x faster                                                            |
| pickle_pure_python         | 320 us                                                 | 300 us: 1.07x faster                                                             |
| sympy_str                  | 297 ms                                                 | 279 ms: 1.07x faster                                                             |
| tomli_loads                | 2.30 sec                                               | 2.17 sec: 1.06x faster                                                           |
| richards                   | 49.8 ms                                                | 47.0 ms: 1.06x faster                                                            |
| sympy_integrate            | 21.5 ms                                                | 20.3 ms: 1.06x faster                                                            |
| regex_compile              | 141 ms                                                 | 135 ms: 1.05x faster                                                             |
| tornado_http               | 98.1 ms                                                | 94.5 ms: 1.04x faster                                                            |
| deepcopy                   | 365 us                                                 | 353 us: 1.03x faster                                                             |
| pycparser                  | 1.19 sec                                               | 1.15 sec: 1.03x faster                                                           |
| scimark_monte_carlo        | 70.7 ms                                                | 68.5 ms: 1.03x faster                                                            |
| fannkuch                   | 405 ms                                                 | 394 ms: 1.03x faster                                                             |
| sympy_expand               | 484 ms                                                 | 471 ms: 1.03x faster                                                             |
| crypto_pyaes               | 76.7 ms                                                | 74.9 ms: 1.02x faster                                                            |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.02x faster                                                             |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                                             |
| genshi_xml                 | 53.4 ms                                                | 52.3 ms: 1.02x faster                                                            |
| json_loads                 | 29.2 us                                                | 28.6 us: 1.02x faster                                                            |
| float                      | 78.9 ms                                                | 77.5 ms: 1.02x faster                                                            |
| go                         | 149 ms                                                 | 146 ms: 1.02x faster                                                             |
| sqlglot_normalize          | 113 ms                                                 | 111 ms: 1.01x faster                                                             |
| mdp                        | 2.77 sec                                               | 2.73 sec: 1.01x faster                                                           |
| pprint_pformat             | 1.55 sec                                               | 1.54 sec: 1.01x faster                                                           |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                             |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                            |
| deepcopy_reduce            | 3.22 us                                                | 3.20 us: 1.01x faster                                                            |
| pprint_safe_repr           | 747 ms                                                 | 751 ms: 1.01x slower                                                             |
| pathlib                    | 18.5 ms                                                | 18.6 ms: 1.01x slower                                                            |
| unpickle_list              | 5.21 us                                                | 5.27 us: 1.01x slower                                                            |
| scimark_sor                | 121 ms                                                 | 123 ms: 1.01x slower                                                             |
| pickle_dict                | 34.6 us                                                | 35.1 us: 1.01x slower                                                            |
| mako                       | 10.7 ms                                                | 10.9 ms: 1.02x slower                                                            |
| json                       | 5.24 ms                                                | 5.38 ms: 1.03x slower                                                            |
| chameleon                  | 6.70 ms                                                | 6.87 ms: 1.03x slower                                                            |
| 2to3                       | 264 ms                                                 | 271 ms: 1.03x slower                                                             |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                                             |
| meteor_contest             | 109 ms                                                 | 113 ms: 1.03x slower                                                             |
| html5lib                   | 64.8 ms                                                | 67.8 ms: 1.05x slower                                                            |
| dulwich_log                | 64.6 ms                                                | 67.8 ms: 1.05x slower                                                            |
| thrift                     | 784 us                                                 | 823 us: 1.05x slower                                                             |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                            |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                                            |
| docutils                   | 2.66 sec                                               | 2.83 sec: 1.06x slower                                                           |
| spectral_norm              | 108 ms                                                 | 115 ms: 1.07x slower                                                             |
| pickle                     | 11.0 us                                                | 11.7 us: 1.07x slower                                                            |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.36 ms: 1.07x slower                                                            |
| xml_etree_process          | 56.9 ms                                                | 60.9 ms: 1.07x slower                                                            |
| unpickle                   | 13.8 us                                                | 14.9 us: 1.08x slower                                                            |
| genshi_text                | 22.5 ms                                                | 24.2 ms: 1.08x slower                                                            |
| mypy2                      | 686 ms                                                 | 738 ms: 1.08x slower                                                             |
| scimark_fft                | 345 ms                                                 | 375 ms: 1.08x slower                                                             |
| xml_etree_generate         | 81.1 ms                                                | 88.3 ms: 1.09x slower                                                            |
| regex_v8                   | 22.9 ms                                                | 25.0 ms: 1.09x slower                                                            |
| regex_effbot               | 3.51 ms                                                | 3.85 ms: 1.10x slower                                                            |
| regex_dna                  | 205 ms                                                 | 225 ms: 1.10x slower                                                             |
| pyflate                    | 434 ms                                                 | 480 ms: 1.11x slower                                                             |
| pickle_list                | 4.59 us                                                | 5.14 us: 1.12x slower                                                            |
| sqlite_synth               | 2.57 us                                                | 2.93 us: 1.14x slower                                                            |
| async_generators           | 374 ms                                                 | 443 ms: 1.19x slower                                                             |
| create_gc_cycles           | 1.43 ms                                                | 1.74 ms: 1.21x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.6 ms: 1.23x slower                                                            |
| telco                      | 6.86 ms                                                | 8.61 ms: 1.26x slower                                                            |
| coverage                   | 78.8 ms                                                | 99.5 ms: 1.26x slower                                                            |
| python_startup_no_site     | 6.01 ms                                                | 9.00 ms: 1.50x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                                     |

Benchmark hidden because not significant (5): scimark_lu, gc_traversal, sqlglot_optimize, bench_thread_pool, dask
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.02% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x