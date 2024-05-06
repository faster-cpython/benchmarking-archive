# Results vs. 3.11.0

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: 08a7899
- commit date: 2024-04-09
- overall geometric mean: 1.07x faster
- HPT reliability: 98.09%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 270 ms: 1.02x slower                                                             |
| chameleon      | 6.70 ms                                                | 6.81 ms: 1.02x slower                                                            |
| docutils       | 2.66 sec                                               | 2.81 sec: 1.06x slower                                                           |
| html5lib       | 64.8 ms                                                | 67.2 ms: 1.04x slower                                                            |
| tornado_http   | 98.1 ms                                                | 94.7 ms: 1.04x faster                                                            |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 351 ms: 1.51x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 333 ms: 1.47x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 440 ms: 1.42x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 924 ms: 1.40x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 921 ms: 1.40x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 461 ms: 1.38x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 603 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 606 ms: 1.24x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.38x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 88.8 ms: 1.08x faster                                                            |
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                                             |
| float          | 78.9 ms                                                | 78.5 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 134 ms: 1.05x faster                                                             |
| regex_effbot   | 3.51 ms                                                | 3.69 ms: 1.05x slower                                                            |
| regex_dna      | 205 ms                                                 | 225 ms: 1.10x slower                                                             |
| regex_v8       | 22.9 ms                                                | 25.9 ms: 1.13x slower                                                            |
| Geometric mean | (ref)                                                  | 1.06x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                            |
| unpickle_pure_python | 242 us                                                 | 220 us: 1.10x faster                                                             |
| tomli_loads          | 2.30 sec                                               | 2.11 sec: 1.09x faster                                                           |
| pickle_pure_python   | 320 us                                                 | 299 us: 1.07x faster                                                             |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.02x faster                                                             |
| json_loads           | 29.2 us                                                | 28.7 us: 1.02x faster                                                            |
| pickle_dict          | 34.6 us                                                | 35.0 us: 1.01x slower                                                            |
| unpickle_list        | 5.21 us                                                | 5.35 us: 1.03x slower                                                            |
| xml_etree_process    | 56.9 ms                                                | 60.8 ms: 1.07x slower                                                            |
| pickle               | 11.0 us                                                | 11.9 us: 1.08x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 88.0 ms: 1.09x slower                                                            |
| pickle_list          | 4.59 us                                                | 5.00 us: 1.09x slower                                                            |
| unpickle             | 13.8 us                                                | 15.2 us: 1.10x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.6 ms: 1.23x slower                                                            |
| python_startup_no_site | 6.01 ms                                                | 9.00 ms: 1.50x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.36x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml     | 53.4 ms                                                | 51.7 ms: 1.03x faster                                                            |
| mako           | 10.7 ms                                                | 10.8 ms: 1.01x slower                                                            |
| genshi_text    | 22.5 ms                                                | 23.3 ms: 1.03x slower                                                            |
| Geometric mean | (ref)                                                  | 1.00x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240409-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-08a7899 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 114 us: 4.54x faster                                                             |
| generators                 | 74.9 ms                                                | 29.3 ms: 2.55x faster                                                            |
| asyncio_tcp                | 875 ms                                                 | 508 ms: 1.72x faster                                                             |
| pylint                     | 476 ms                                                 | 278 ms: 1.71x faster                                                             |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                           |
| async_tree_none            | 528 ms                                                 | 351 ms: 1.51x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 333 ms: 1.47x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 440 ms: 1.42x faster                                                             |
| comprehensions             | 23.6 us                                                | 16.8 us: 1.40x faster                                                            |
| async_tree_io_tg           | 1.29 sec                                               | 924 ms: 1.40x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 921 ms: 1.40x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 461 ms: 1.38x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 603 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 606 ms: 1.24x faster                                                             |
| deltablue                  | 3.92 ms                                                | 3.18 ms: 1.23x faster                                                            |
| coroutines                 | 27.0 ms                                                | 22.4 ms: 1.21x faster                                                            |
| chaos                      | 71.9 ms                                                | 60.0 ms: 1.20x faster                                                            |
| richards_super             | 61.9 ms                                                | 52.9 ms: 1.17x faster                                                            |
| raytrace                   | 309 ms                                                 | 264 ms: 1.17x faster                                                             |
| sqlglot_parse              | 1.43 ms                                                | 1.28 ms: 1.12x faster                                                            |
| logging_silent             | 111 ns                                                 | 99.8 ns: 1.11x faster                                                            |
| logging_simple             | 6.22 us                                                | 5.64 us: 1.10x faster                                                            |
| sqlglot_transpile          | 1.75 ms                                                | 1.59 ms: 1.10x faster                                                            |
| unpickle_pure_python       | 242 us                                                 | 220 us: 1.10x faster                                                             |
| hexiom                     | 6.89 ms                                                | 6.26 ms: 1.10x faster                                                            |
| tomli_loads                | 2.30 sec                                               | 2.11 sec: 1.09x faster                                                           |
| logging_format             | 6.81 us                                                | 6.28 us: 1.08x faster                                                            |
| nbody                      | 96.0 ms                                                | 88.8 ms: 1.08x faster                                                            |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.08x faster                                                             |
| deepcopy_memo              | 40.2 us                                                | 37.2 us: 1.08x faster                                                            |
| nqueens                    | 87.9 ms                                                | 81.5 ms: 1.08x faster                                                            |
| gc_traversal               | 4.01 ms                                                | 3.74 ms: 1.07x faster                                                            |
| pickle_pure_python         | 320 us                                                 | 299 us: 1.07x faster                                                             |
| richards                   | 49.8 ms                                                | 46.7 ms: 1.07x faster                                                            |
| sympy_str                  | 297 ms                                                 | 279 ms: 1.06x faster                                                             |
| scimark_monte_carlo        | 70.7 ms                                                | 66.9 ms: 1.06x faster                                                            |
| regex_compile              | 141 ms                                                 | 134 ms: 1.05x faster                                                             |
| sympy_integrate            | 21.5 ms                                                | 20.4 ms: 1.05x faster                                                            |
| go                         | 149 ms                                                 | 142 ms: 1.05x faster                                                             |
| sympy_expand               | 484 ms                                                 | 467 ms: 1.04x faster                                                             |
| tornado_http               | 98.1 ms                                                | 94.7 ms: 1.04x faster                                                            |
| genshi_xml                 | 53.4 ms                                                | 51.7 ms: 1.03x faster                                                            |
| deepcopy                   | 365 us                                                 | 355 us: 1.03x faster                                                             |
| fannkuch                   | 405 ms                                                 | 395 ms: 1.03x faster                                                             |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                                             |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.02x faster                                                             |
| sqlglot_normalize          | 113 ms                                                 | 111 ms: 1.02x faster                                                             |
| json_loads                 | 29.2 us                                                | 28.7 us: 1.02x faster                                                            |
| deepcopy_reduce            | 3.22 us                                                | 3.17 us: 1.01x faster                                                            |
| scimark_lu                 | 116 ms                                                 | 115 ms: 1.01x faster                                                             |
| crypto_pyaes               | 76.7 ms                                                | 75.9 ms: 1.01x faster                                                            |
| pprint_pformat             | 1.55 sec                                               | 1.54 sec: 1.01x faster                                                           |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                            |
| float                      | 78.9 ms                                                | 78.5 ms: 1.01x faster                                                            |
| mdp                        | 2.77 sec                                               | 2.79 sec: 1.01x slower                                                           |
| pprint_safe_repr           | 747 ms                                                 | 754 ms: 1.01x slower                                                             |
| scimark_sor                | 121 ms                                                 | 123 ms: 1.01x slower                                                             |
| mako                       | 10.7 ms                                                | 10.8 ms: 1.01x slower                                                            |
| pickle_dict                | 34.6 us                                                | 35.0 us: 1.01x slower                                                            |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                                             |
| spectral_norm              | 108 ms                                                 | 110 ms: 1.01x slower                                                             |
| pathlib                    | 18.5 ms                                                | 18.8 ms: 1.01x slower                                                            |
| chameleon                  | 6.70 ms                                                | 6.81 ms: 1.02x slower                                                            |
| json                       | 5.24 ms                                                | 5.32 ms: 1.02x slower                                                            |
| 2to3                       | 264 ms                                                 | 270 ms: 1.02x slower                                                             |
| unpickle_list              | 5.21 us                                                | 5.35 us: 1.03x slower                                                            |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                                             |
| genshi_text                | 22.5 ms                                                | 23.3 ms: 1.03x slower                                                            |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.21 ms: 1.04x slower                                                            |
| html5lib                   | 64.8 ms                                                | 67.2 ms: 1.04x slower                                                            |
| dulwich_log                | 64.6 ms                                                | 67.2 ms: 1.04x slower                                                            |
| thrift                     | 784 us                                                 | 816 us: 1.04x slower                                                             |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                            |
| regex_effbot               | 3.51 ms                                                | 3.69 ms: 1.05x slower                                                            |
| docutils                   | 2.66 sec                                               | 2.81 sec: 1.06x slower                                                           |
| scimark_fft                | 345 ms                                                 | 365 ms: 1.06x slower                                                             |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                                            |
| xml_etree_process          | 56.9 ms                                                | 60.8 ms: 1.07x slower                                                            |
| mypy2                      | 686 ms                                                 | 739 ms: 1.08x slower                                                             |
| pickle                     | 11.0 us                                                | 11.9 us: 1.08x slower                                                            |
| xml_etree_generate         | 81.1 ms                                                | 88.0 ms: 1.09x slower                                                            |
| pickle_list                | 4.59 us                                                | 5.00 us: 1.09x slower                                                            |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.10x slower                                                            |
| pyflate                    | 434 ms                                                 | 477 ms: 1.10x slower                                                             |
| regex_dna                  | 205 ms                                                 | 225 ms: 1.10x slower                                                             |
| regex_v8                   | 22.9 ms                                                | 25.9 ms: 1.13x slower                                                            |
| sqlite_synth               | 2.57 us                                                | 2.94 us: 1.14x slower                                                            |
| async_generators           | 374 ms                                                 | 447 ms: 1.20x slower                                                             |
| create_gc_cycles           | 1.43 ms                                                | 1.73 ms: 1.21x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.6 ms: 1.23x slower                                                            |
| telco                      | 6.86 ms                                                | 8.52 ms: 1.24x slower                                                            |
| coverage                   | 78.8 ms                                                | 98.2 ms: 1.25x slower                                                            |
| python_startup_no_site     | 6.01 ms                                                | 9.00 ms: 1.50x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                                     |

Benchmark hidden because not significant (5): xml_etree_iterparse, sqlglot_optimize, bench_thread_pool, dask, pycparser
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 98.09% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x