# Results vs. 3.11.0

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: 846a7ef
- commit date: 2024-05-01
- overall geometric mean: 1.07x faster
- HPT reliability: 98.21%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 272 ms: 1.03x slower                                                             |
| chameleon      | 6.70 ms                                                | 7.03 ms: 1.05x slower                                                            |
| docutils       | 2.66 sec                                               | 2.82 sec: 1.06x slower                                                           |
| html5lib       | 64.8 ms                                                | 69.5 ms: 1.07x slower                                                            |
| tornado_http   | 98.1 ms                                                | 93.7 ms: 1.05x faster                                                            |
| Geometric mean | (ref)                                                  | 1.03x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 353 ms: 1.50x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 341 ms: 1.44x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 914 ms: 1.41x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 459 ms: 1.39x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 452 ms: 1.39x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 937 ms: 1.38x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 614 ms: 1.24x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 610 ms: 1.23x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 89.6 ms: 1.07x faster                                                            |
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                                             |
| float          | 78.9 ms                                                | 78.2 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 134 ms: 1.05x faster                                                             |
| regex_v8       | 22.9 ms                                                | 24.4 ms: 1.07x slower                                                            |
| regex_effbot   | 3.51 ms                                                | 3.77 ms: 1.07x slower                                                            |
| regex_dna      | 205 ms                                                 | 221 ms: 1.08x slower                                                             |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.8 ms: 1.23x faster                                                            |
| unpickle_pure_python | 242 us                                                 | 218 us: 1.11x faster                                                             |
| tomli_loads          | 2.30 sec                                               | 2.16 sec: 1.07x faster                                                           |
| xml_etree_parse      | 164 ms                                                 | 158 ms: 1.04x faster                                                             |
| json_loads           | 29.2 us                                                | 28.6 us: 1.02x faster                                                            |
| unpickle_list        | 5.21 us                                                | 5.18 us: 1.01x faster                                                            |
| pickle_pure_python   | 320 us                                                 | 318 us: 1.00x faster                                                             |
| pickle_dict          | 34.6 us                                                | 34.8 us: 1.01x slower                                                            |
| pickle               | 11.0 us                                                | 11.6 us: 1.06x slower                                                            |
| unpickle             | 13.8 us                                                | 15.0 us: 1.08x slower                                                            |
| xml_etree_process    | 56.9 ms                                                | 61.8 ms: 1.09x slower                                                            |
| pickle_list          | 4.59 us                                                | 5.00 us: 1.09x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 88.4 ms: 1.09x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                                     |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.09 ms: 1.18x slower                                                            |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 50.6 ms: 1.06x faster                                                            |
| genshi_text     | 22.5 ms                                                | 23.3 ms: 1.03x slower                                                            |
| django_template | 33.5 ms                                                | 34.9 ms: 1.04x slower                                                            |
| mako            | 10.7 ms                                                | 11.4 ms: 1.07x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-846a7ef |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 161 us: 3.23x faster                                                             |
| generators                 | 74.9 ms                                                | 29.2 ms: 2.56x faster                                                            |
| asyncio_tcp                | 875 ms                                                 | 511 ms: 1.71x faster                                                             |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                           |
| async_tree_none            | 528 ms                                                 | 353 ms: 1.50x faster                                                             |
| pylint                     | 476 ms                                                 | 319 ms: 1.49x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 341 ms: 1.44x faster                                                             |
| comprehensions             | 23.6 us                                                | 16.7 us: 1.41x faster                                                            |
| async_tree_io              | 1.29 sec                                               | 914 ms: 1.41x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 459 ms: 1.39x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 452 ms: 1.39x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 937 ms: 1.38x faster                                                             |
| go                         | 149 ms                                                 | 119 ms: 1.25x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 614 ms: 1.24x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 10.8 ms: 1.23x faster                                                            |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 610 ms: 1.23x faster                                                             |
| deltablue                  | 3.92 ms                                                | 3.23 ms: 1.22x faster                                                            |
| coroutines                 | 27.0 ms                                                | 22.5 ms: 1.20x faster                                                            |
| chaos                      | 71.9 ms                                                | 60.1 ms: 1.20x faster                                                            |
| raytrace                   | 309 ms                                                 | 266 ms: 1.16x faster                                                             |
| richards_super             | 61.9 ms                                                | 53.7 ms: 1.15x faster                                                            |
| nqueens                    | 87.9 ms                                                | 78.9 ms: 1.11x faster                                                            |
| sqlglot_parse              | 1.43 ms                                                | 1.29 ms: 1.11x faster                                                            |
| unpickle_pure_python       | 242 us                                                 | 218 us: 1.11x faster                                                             |
| sympy_sum                  | 169 ms                                                 | 154 ms: 1.10x faster                                                             |
| hexiom                     | 6.89 ms                                                | 6.28 ms: 1.10x faster                                                            |
| sqlglot_transpile          | 1.75 ms                                                | 1.60 ms: 1.10x faster                                                            |
| logging_simple             | 6.22 us                                                | 5.78 us: 1.08x faster                                                            |
| logging_silent             | 111 ns                                                 | 103 ns: 1.08x faster                                                             |
| nbody                      | 96.0 ms                                                | 89.6 ms: 1.07x faster                                                            |
| mdp                        | 2.77 sec                                               | 2.59 sec: 1.07x faster                                                           |
| gc_traversal               | 4.01 ms                                                | 3.75 ms: 1.07x faster                                                            |
| djangocms                  | 33.5 us                                                | 31.4 us: 1.07x faster                                                            |
| tomli_loads                | 2.30 sec                                               | 2.16 sec: 1.07x faster                                                           |
| sympy_str                  | 297 ms                                                 | 279 ms: 1.06x faster                                                             |
| genshi_xml                 | 53.4 ms                                                | 50.6 ms: 1.06x faster                                                            |
| logging_format             | 6.81 us                                                | 6.44 us: 1.06x faster                                                            |
| sympy_integrate            | 21.5 ms                                                | 20.3 ms: 1.06x faster                                                            |
| deepcopy_memo              | 40.2 us                                                | 38.1 us: 1.05x faster                                                            |
| pathlib                    | 18.5 ms                                                | 17.6 ms: 1.05x faster                                                            |
| regex_compile              | 141 ms                                                 | 134 ms: 1.05x faster                                                             |
| tornado_http               | 98.1 ms                                                | 93.7 ms: 1.05x faster                                                            |
| richards                   | 49.8 ms                                                | 47.9 ms: 1.04x faster                                                            |
| xml_etree_parse            | 164 ms                                                 | 158 ms: 1.04x faster                                                             |
| deepcopy                   | 365 us                                                 | 354 us: 1.03x faster                                                             |
| pycparser                  | 1.19 sec                                               | 1.15 sec: 1.03x faster                                                           |
| sympy_expand               | 484 ms                                                 | 473 ms: 1.02x faster                                                             |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                                             |
| json_loads                 | 29.2 us                                                | 28.6 us: 1.02x faster                                                            |
| scimark_lu                 | 116 ms                                                 | 114 ms: 1.02x faster                                                             |
| sqlglot_normalize          | 113 ms                                                 | 111 ms: 1.02x faster                                                             |
| float                      | 78.9 ms                                                | 78.2 ms: 1.01x faster                                                            |
| fannkuch                   | 405 ms                                                 | 402 ms: 1.01x faster                                                             |
| pprint_pformat             | 1.55 sec                                               | 1.54 sec: 1.01x faster                                                           |
| unpickle_list              | 5.21 us                                                | 5.18 us: 1.01x faster                                                            |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                            |
| pickle_pure_python         | 320 us                                                 | 318 us: 1.00x faster                                                             |
| sqlglot_optimize           | 55.3 ms                                                | 55.1 ms: 1.00x faster                                                            |
| bench_thread_pool          | 834 us                                                 | 831 us: 1.00x faster                                                             |
| deepcopy_reduce            | 3.22 us                                                | 3.23 us: 1.00x slower                                                            |
| pprint_safe_repr           | 747 ms                                                 | 751 ms: 1.01x slower                                                             |
| pickle_dict                | 34.6 us                                                | 34.8 us: 1.01x slower                                                            |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                                             |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.10 ms: 1.01x slower                                                            |
| dulwich_log                | 64.6 ms                                                | 66.1 ms: 1.02x slower                                                            |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.02x slower                                                             |
| 2to3                       | 264 ms                                                 | 272 ms: 1.03x slower                                                             |
| json                       | 5.24 ms                                                | 5.39 ms: 1.03x slower                                                            |
| genshi_text                | 22.5 ms                                                | 23.3 ms: 1.03x slower                                                            |
| django_template            | 33.5 ms                                                | 34.9 ms: 1.04x slower                                                            |
| spectral_norm              | 108 ms                                                 | 113 ms: 1.04x slower                                                             |
| scimark_monte_carlo        | 70.7 ms                                                | 73.9 ms: 1.04x slower                                                            |
| chameleon                  | 6.70 ms                                                | 7.03 ms: 1.05x slower                                                            |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                            |
| pickle                     | 11.0 us                                                | 11.6 us: 1.06x slower                                                            |
| docutils                   | 2.66 sec                                               | 2.82 sec: 1.06x slower                                                           |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                                            |
| thrift                     | 784 us                                                 | 833 us: 1.06x slower                                                             |
| scimark_fft                | 345 ms                                                 | 367 ms: 1.06x slower                                                             |
| regex_v8                   | 22.9 ms                                                | 24.4 ms: 1.07x slower                                                            |
| html5lib                   | 64.8 ms                                                | 69.5 ms: 1.07x slower                                                            |
| mako                       | 10.7 ms                                                | 11.4 ms: 1.07x slower                                                            |
| regex_effbot               | 3.51 ms                                                | 3.77 ms: 1.07x slower                                                            |
| mypy2                      | 686 ms                                                 | 739 ms: 1.08x slower                                                             |
| regex_dna                  | 205 ms                                                 | 221 ms: 1.08x slower                                                             |
| unpickle                   | 13.8 us                                                | 15.0 us: 1.08x slower                                                            |
| xml_etree_process          | 56.9 ms                                                | 61.8 ms: 1.09x slower                                                            |
| crypto_pyaes               | 76.7 ms                                                | 83.5 ms: 1.09x slower                                                            |
| scimark_sor                | 121 ms                                                 | 132 ms: 1.09x slower                                                             |
| pickle_list                | 4.59 us                                                | 5.00 us: 1.09x slower                                                            |
| xml_etree_generate         | 81.1 ms                                                | 88.4 ms: 1.09x slower                                                            |
| pyflate                    | 434 ms                                                 | 476 ms: 1.10x slower                                                             |
| sqlite_synth               | 2.57 us                                                | 2.96 us: 1.15x slower                                                            |
| python_startup_no_site     | 6.01 ms                                                | 7.09 ms: 1.18x slower                                                            |
| async_generators           | 374 ms                                                 | 446 ms: 1.19x slower                                                             |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| coverage                   | 78.8 ms                                                | 96.8 ms: 1.23x slower                                                            |
| telco                      | 6.86 ms                                                | 8.62 ms: 1.26x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                                     |

Benchmark hidden because not significant (2): xml_etree_iterparse, dask
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 98.21% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x