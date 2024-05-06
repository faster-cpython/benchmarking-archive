# Results vs. 3.11.0

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 2c964fa
- commit date: 2024-04-05
- overall geometric mean: 1.07x faster
- HPT reliability: 99.88%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 267 ms: 1.01x slower                                                             |
| chameleon      | 6.70 ms                                                | 6.93 ms: 1.03x slower                                                            |
| docutils       | 2.66 sec                                               | 2.79 sec: 1.05x slower                                                           |
| html5lib       | 64.8 ms                                                | 67.2 ms: 1.04x slower                                                            |
| tornado_http   | 98.1 ms                                                | 94.3 ms: 1.04x faster                                                            |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 351 ms: 1.51x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.46x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 444 ms: 1.41x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 912 ms: 1.41x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 460 ms: 1.39x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 934 ms: 1.39x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 600 ms: 1.27x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 605 ms: 1.24x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.38x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 78.9 ms                                                | 78.2 ms: 1.01x faster                                                            |
| pidigits       | 194 ms                                                 | 216 ms: 1.11x slower                                                             |
| Geometric mean | (ref)                                                  | 1.03x slower                                                                     |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 135 ms: 1.05x faster                                                             |
| regex_effbot   | 3.51 ms                                                | 3.69 ms: 1.05x slower                                                            |
| regex_v8       | 22.9 ms                                                | 24.4 ms: 1.06x slower                                                            |
| regex_dna      | 205 ms                                                 | 218 ms: 1.07x slower                                                             |
| Geometric mean | (ref)                                                  | 1.03x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                            |
| unpickle_pure_python | 242 us                                                 | 221 us: 1.10x faster                                                             |
| tomli_loads          | 2.30 sec                                               | 2.19 sec: 1.05x faster                                                           |
| pickle_pure_python   | 320 us                                                 | 305 us: 1.05x faster                                                             |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.02x faster                                                             |
| json_loads           | 29.2 us                                                | 28.5 us: 1.02x faster                                                            |
| unpickle_list        | 5.21 us                                                | 5.11 us: 1.02x faster                                                            |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                             |
| pickle_dict          | 34.6 us                                                | 35.3 us: 1.02x slower                                                            |
| xml_etree_process    | 56.9 ms                                                | 59.8 ms: 1.05x slower                                                            |
| pickle               | 11.0 us                                                | 11.7 us: 1.06x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 86.7 ms: 1.07x slower                                                            |
| pickle_list          | 4.59 us                                                | 4.93 us: 1.07x slower                                                            |
| unpickle             | 13.8 us                                                | 15.0 us: 1.08x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| python_startup_no_site | 6.01 ms                                                | 8.97 ms: 1.49x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.36x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml     | 53.4 ms                                                | 52.4 ms: 1.02x faster                                                            |
| genshi_text    | 22.5 ms                                                | 23.8 ms: 1.06x slower                                                            |
| Geometric mean | (ref)                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 114 us: 4.54x faster                                                             |
| generators                 | 74.9 ms                                                | 29.3 ms: 2.56x faster                                                            |
| asyncio_tcp                | 875 ms                                                 | 506 ms: 1.73x faster                                                             |
| pylint                     | 476 ms                                                 | 277 ms: 1.72x faster                                                             |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                           |
| async_tree_none            | 528 ms                                                 | 351 ms: 1.51x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.46x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 444 ms: 1.41x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 912 ms: 1.41x faster                                                             |
| comprehensions             | 23.6 us                                                | 16.8 us: 1.40x faster                                                            |
| async_tree_memoization     | 639 ms                                                 | 460 ms: 1.39x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 934 ms: 1.39x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 600 ms: 1.27x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 605 ms: 1.24x faster                                                             |
| deltablue                  | 3.92 ms                                                | 3.22 ms: 1.22x faster                                                            |
| coroutines                 | 27.0 ms                                                | 22.9 ms: 1.18x faster                                                            |
| richards_super             | 61.9 ms                                                | 52.7 ms: 1.17x faster                                                            |
| raytrace                   | 309 ms                                                 | 265 ms: 1.16x faster                                                             |
| chaos                      | 71.9 ms                                                | 62.8 ms: 1.14x faster                                                            |
| sqlglot_parse              | 1.43 ms                                                | 1.29 ms: 1.11x faster                                                            |
| sqlglot_transpile          | 1.75 ms                                                | 1.59 ms: 1.10x faster                                                            |
| crypto_pyaes               | 76.7 ms                                                | 69.9 ms: 1.10x faster                                                            |
| unpickle_pure_python       | 242 us                                                 | 221 us: 1.10x faster                                                             |
| sympy_sum                  | 169 ms                                                 | 154 ms: 1.09x faster                                                             |
| hexiom                     | 6.89 ms                                                | 6.30 ms: 1.09x faster                                                            |
| nqueens                    | 87.9 ms                                                | 81.0 ms: 1.08x faster                                                            |
| mdp                        | 2.77 sec                                               | 2.58 sec: 1.08x faster                                                           |
| logging_simple             | 6.22 us                                                | 5.81 us: 1.07x faster                                                            |
| sympy_str                  | 297 ms                                                 | 279 ms: 1.07x faster                                                             |
| logging_silent             | 111 ns                                                 | 105 ns: 1.06x faster                                                             |
| richards                   | 49.8 ms                                                | 47.0 ms: 1.06x faster                                                            |
| sympy_integrate            | 21.5 ms                                                | 20.3 ms: 1.06x faster                                                            |
| logging_format             | 6.81 us                                                | 6.47 us: 1.05x faster                                                            |
| tomli_loads                | 2.30 sec                                               | 2.19 sec: 1.05x faster                                                           |
| pickle_pure_python         | 320 us                                                 | 305 us: 1.05x faster                                                             |
| spectral_norm              | 108 ms                                                 | 103 ms: 1.05x faster                                                             |
| regex_compile              | 141 ms                                                 | 135 ms: 1.05x faster                                                             |
| deepcopy_memo              | 40.2 us                                                | 38.4 us: 1.05x faster                                                            |
| sympy_expand               | 484 ms                                                 | 465 ms: 1.04x faster                                                             |
| tornado_http               | 98.1 ms                                                | 94.3 ms: 1.04x faster                                                            |
| pycparser                  | 1.19 sec                                               | 1.14 sec: 1.04x faster                                                           |
| deepcopy                   | 365 us                                                 | 352 us: 1.04x faster                                                             |
| go                         | 149 ms                                                 | 144 ms: 1.03x faster                                                             |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.87 ms: 1.03x faster                                                            |
| pprint_pformat             | 1.55 sec                                               | 1.51 sec: 1.03x faster                                                           |
| scimark_lu                 | 116 ms                                                 | 113 ms: 1.03x faster                                                             |
| deepcopy_reduce            | 3.22 us                                                | 3.14 us: 1.02x faster                                                            |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.02x faster                                                             |
| json_loads                 | 29.2 us                                                | 28.5 us: 1.02x faster                                                            |
| fannkuch                   | 405 ms                                                 | 397 ms: 1.02x faster                                                             |
| genshi_xml                 | 53.4 ms                                                | 52.4 ms: 1.02x faster                                                            |
| unpickle_list              | 5.21 us                                                | 5.11 us: 1.02x faster                                                            |
| gc_traversal               | 4.01 ms                                                | 3.97 ms: 1.01x faster                                                            |
| pprint_safe_repr           | 747 ms                                                 | 739 ms: 1.01x faster                                                             |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                             |
| float                      | 78.9 ms                                                | 78.2 ms: 1.01x faster                                                            |
| bench_thread_pool          | 834 us                                                 | 827 us: 1.01x faster                                                             |
| sqlglot_normalize          | 113 ms                                                 | 112 ms: 1.01x faster                                                             |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                            |
| sqlglot_optimize           | 55.3 ms                                                | 55.1 ms: 1.00x faster                                                            |
| scimark_sor                | 121 ms                                                 | 122 ms: 1.00x slower                                                             |
| 2to3                       | 264 ms                                                 | 267 ms: 1.01x slower                                                             |
| pathlib                    | 18.5 ms                                                | 18.8 ms: 1.01x slower                                                            |
| pickle_dict                | 34.6 us                                                | 35.3 us: 1.02x slower                                                            |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                                             |
| thrift                     | 784 us                                                 | 806 us: 1.03x slower                                                             |
| chameleon                  | 6.70 ms                                                | 6.93 ms: 1.03x slower                                                            |
| html5lib                   | 64.8 ms                                                | 67.2 ms: 1.04x slower                                                            |
| json                       | 5.24 ms                                                | 5.45 ms: 1.04x slower                                                            |
| dulwich_log                | 64.6 ms                                                | 67.3 ms: 1.04x slower                                                            |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                            |
| docutils                   | 2.66 sec                                               | 2.79 sec: 1.05x slower                                                           |
| gunicorn                   | 1.20 ms                                                | 1.26 ms: 1.05x slower                                                            |
| xml_etree_process          | 56.9 ms                                                | 59.8 ms: 1.05x slower                                                            |
| regex_effbot               | 3.51 ms                                                | 3.69 ms: 1.05x slower                                                            |
| genshi_text                | 22.5 ms                                                | 23.8 ms: 1.06x slower                                                            |
| pickle                     | 11.0 us                                                | 11.7 us: 1.06x slower                                                            |
| regex_v8                   | 22.9 ms                                                | 24.4 ms: 1.06x slower                                                            |
| regex_dna                  | 205 ms                                                 | 218 ms: 1.07x slower                                                             |
| mypy2                      | 686 ms                                                 | 733 ms: 1.07x slower                                                             |
| xml_etree_generate         | 81.1 ms                                                | 86.7 ms: 1.07x slower                                                            |
| pickle_list                | 4.59 us                                                | 4.93 us: 1.07x slower                                                            |
| pyflate                    | 434 ms                                                 | 469 ms: 1.08x slower                                                             |
| unpickle                   | 13.8 us                                                | 15.0 us: 1.08x slower                                                            |
| scimark_fft                | 345 ms                                                 | 375 ms: 1.09x slower                                                             |
| pidigits                   | 194 ms                                                 | 216 ms: 1.11x slower                                                             |
| sqlite_synth               | 2.57 us                                                | 2.92 us: 1.13x slower                                                            |
| async_generators           | 374 ms                                                 | 440 ms: 1.18x slower                                                             |
| create_gc_cycles           | 1.43 ms                                                | 1.76 ms: 1.23x slower                                                            |
| telco                      | 6.86 ms                                                | 8.43 ms: 1.23x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| coverage                   | 78.8 ms                                                | 98.2 ms: 1.25x slower                                                            |
| python_startup_no_site     | 6.01 ms                                                | 8.97 ms: 1.49x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                                     |

Benchmark hidden because not significant (5): scimark_monte_carlo, nbody, mako, meteor_contest, dask
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.88% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x