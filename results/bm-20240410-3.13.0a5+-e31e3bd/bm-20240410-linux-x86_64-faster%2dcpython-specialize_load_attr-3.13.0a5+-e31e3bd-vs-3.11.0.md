# Results vs. 3.11.0

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: e31e3bd
- commit date: 2024-04-10
- overall geometric mean: 1.06x faster
- HPT reliability: 96.58%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 273 ms: 1.03x slower                                                             |
| chameleon      | 6.70 ms                                                | 7.05 ms: 1.05x slower                                                            |
| docutils       | 2.66 sec                                               | 2.83 sec: 1.06x slower                                                           |
| html5lib       | 64.8 ms                                                | 67.8 ms: 1.05x slower                                                            |
| tornado_http   | 98.1 ms                                                | 93.9 ms: 1.04x faster                                                            |
| Geometric mean | (ref)                                                  | 1.03x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 352 ms: 1.50x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.47x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 928 ms: 1.39x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 936 ms: 1.38x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 463 ms: 1.38x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 612 ms: 1.22x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 88.2 ms: 1.09x faster                                                            |
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                                             |
| float          | 78.9 ms                                                | 78.6 ms: 1.00x faster                                                            |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 137 ms: 1.03x faster                                                             |
| regex_effbot   | 3.51 ms                                                | 3.75 ms: 1.07x slower                                                            |
| regex_dna      | 205 ms                                                 | 225 ms: 1.10x slower                                                             |
| regex_v8       | 22.9 ms                                                | 25.8 ms: 1.13x slower                                                            |
| Geometric mean | (ref)                                                  | 1.06x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                            |
| pickle_dict          | 34.6 us                                                | 32.1 us: 1.08x faster                                                            |
| tomli_loads          | 2.30 sec                                               | 2.17 sec: 1.06x faster                                                           |
| unpickle_pure_python | 242 us                                                 | 228 us: 1.06x faster                                                             |
| pickle_pure_python   | 320 us                                                 | 304 us: 1.05x faster                                                             |
| xml_etree_parse      | 164 ms                                                 | 159 ms: 1.03x faster                                                             |
| json_loads           | 29.2 us                                                | 28.8 us: 1.01x faster                                                            |
| unpickle_list        | 5.21 us                                                | 5.27 us: 1.01x slower                                                            |
| xml_etree_process    | 56.9 ms                                                | 60.6 ms: 1.07x slower                                                            |
| pickle_list          | 4.59 us                                                | 4.92 us: 1.07x slower                                                            |
| pickle               | 11.0 us                                                | 11.9 us: 1.08x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 88.0 ms: 1.09x slower                                                            |
| unpickle             | 13.8 us                                                | 15.9 us: 1.15x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.22x slower                                                            |
| python_startup_no_site | 6.01 ms                                                | 8.93 ms: 1.48x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.35x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako           | 10.7 ms                                                | 11.1 ms: 1.04x slower                                                            |
| genshi_text    | 22.5 ms                                                | 24.6 ms: 1.09x slower                                                            |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                     |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 117 us: 4.43x faster                                                             |
| generators                 | 74.9 ms                                                | 30.7 ms: 2.44x faster                                                            |
| asyncio_tcp                | 875 ms                                                 | 507 ms: 1.73x faster                                                             |
| pylint                     | 476 ms                                                 | 280 ms: 1.70x faster                                                             |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                           |
| async_tree_none            | 528 ms                                                 | 352 ms: 1.50x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.47x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                             |
| comprehensions             | 23.6 us                                                | 16.9 us: 1.39x faster                                                            |
| async_tree_io              | 1.29 sec                                               | 928 ms: 1.39x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 936 ms: 1.38x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 463 ms: 1.38x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 612 ms: 1.22x faster                                                             |
| coroutines                 | 27.0 ms                                                | 22.4 ms: 1.21x faster                                                            |
| deltablue                  | 3.92 ms                                                | 3.29 ms: 1.19x faster                                                            |
| chaos                      | 71.9 ms                                                | 60.5 ms: 1.19x faster                                                            |
| raytrace                   | 309 ms                                                 | 262 ms: 1.18x faster                                                             |
| richards_super             | 61.9 ms                                                | 54.0 ms: 1.15x faster                                                            |
| sqlglot_parse              | 1.43 ms                                                | 1.30 ms: 1.11x faster                                                            |
| sqlglot_transpile          | 1.75 ms                                                | 1.60 ms: 1.09x faster                                                            |
| nbody                      | 96.0 ms                                                | 88.2 ms: 1.09x faster                                                            |
| sympy_sum                  | 169 ms                                                 | 157 ms: 1.08x faster                                                             |
| pickle_dict                | 34.6 us                                                | 32.1 us: 1.08x faster                                                            |
| gc_traversal               | 4.01 ms                                                | 3.75 ms: 1.07x faster                                                            |
| hexiom                     | 6.89 ms                                                | 6.48 ms: 1.06x faster                                                            |
| tomli_loads                | 2.30 sec                                               | 2.17 sec: 1.06x faster                                                           |
| unpickle_pure_python       | 242 us                                                 | 228 us: 1.06x faster                                                             |
| nqueens                    | 87.9 ms                                                | 82.7 ms: 1.06x faster                                                            |
| logging_simple             | 6.22 us                                                | 5.86 us: 1.06x faster                                                            |
| logging_silent             | 111 ns                                                 | 105 ns: 1.06x faster                                                             |
| sympy_str                  | 297 ms                                                 | 282 ms: 1.06x faster                                                             |
| pickle_pure_python         | 320 us                                                 | 304 us: 1.05x faster                                                             |
| logging_format             | 6.81 us                                                | 6.49 us: 1.05x faster                                                            |
| sympy_integrate            | 21.5 ms                                                | 20.5 ms: 1.05x faster                                                            |
| tornado_http               | 98.1 ms                                                | 93.9 ms: 1.04x faster                                                            |
| scimark_monte_carlo        | 70.7 ms                                                | 67.8 ms: 1.04x faster                                                            |
| mdp                        | 2.77 sec                                               | 2.66 sec: 1.04x faster                                                           |
| richards                   | 49.8 ms                                                | 48.0 ms: 1.04x faster                                                            |
| crypto_pyaes               | 76.7 ms                                                | 74.0 ms: 1.04x faster                                                            |
| go                         | 149 ms                                                 | 144 ms: 1.03x faster                                                             |
| fannkuch                   | 405 ms                                                 | 392 ms: 1.03x faster                                                             |
| regex_compile              | 141 ms                                                 | 137 ms: 1.03x faster                                                             |
| deepcopy_memo              | 40.2 us                                                | 38.9 us: 1.03x faster                                                            |
| xml_etree_parse            | 164 ms                                                 | 159 ms: 1.03x faster                                                             |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                                             |
| deepcopy                   | 365 us                                                 | 358 us: 1.02x faster                                                             |
| sympy_expand               | 484 ms                                                 | 474 ms: 1.02x faster                                                             |
| pycparser                  | 1.19 sec                                               | 1.17 sec: 1.02x faster                                                           |
| json_loads                 | 29.2 us                                                | 28.8 us: 1.01x faster                                                            |
| pprint_pformat             | 1.55 sec                                               | 1.54 sec: 1.01x faster                                                           |
| sqlglot_normalize          | 113 ms                                                 | 112 ms: 1.00x faster                                                             |
| float                      | 78.9 ms                                                | 78.6 ms: 1.00x faster                                                            |
| sqlglot_optimize           | 55.3 ms                                                | 55.5 ms: 1.00x slower                                                            |
| bench_thread_pool          | 834 us                                                 | 837 us: 1.00x slower                                                             |
| unpickle_list              | 5.21 us                                                | 5.27 us: 1.01x slower                                                            |
| pprint_safe_repr           | 747 ms                                                 | 756 ms: 1.01x slower                                                             |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                                             |
| pathlib                    | 18.5 ms                                                | 18.8 ms: 1.02x slower                                                            |
| json                       | 5.24 ms                                                | 5.33 ms: 1.02x slower                                                            |
| scimark_lu                 | 116 ms                                                 | 119 ms: 1.02x slower                                                             |
| thrift                     | 784 us                                                 | 801 us: 1.02x slower                                                             |
| scimark_sor                | 121 ms                                                 | 124 ms: 1.02x slower                                                             |
| 2to3                       | 264 ms                                                 | 273 ms: 1.03x slower                                                             |
| spectral_norm              | 108 ms                                                 | 112 ms: 1.03x slower                                                             |
| asyncio_websockets         | 550 ms                                                 | 570 ms: 1.04x slower                                                             |
| dulwich_log                | 64.6 ms                                                | 67.1 ms: 1.04x slower                                                            |
| mako                       | 10.7 ms                                                | 11.1 ms: 1.04x slower                                                            |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.24 ms: 1.04x slower                                                            |
| html5lib                   | 64.8 ms                                                | 67.8 ms: 1.05x slower                                                            |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                            |
| chameleon                  | 6.70 ms                                                | 7.05 ms: 1.05x slower                                                            |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                                            |
| docutils                   | 2.66 sec                                               | 2.83 sec: 1.06x slower                                                           |
| xml_etree_process          | 56.9 ms                                                | 60.6 ms: 1.07x slower                                                            |
| regex_effbot               | 3.51 ms                                                | 3.75 ms: 1.07x slower                                                            |
| pickle_list                | 4.59 us                                                | 4.92 us: 1.07x slower                                                            |
| scimark_fft                | 345 ms                                                 | 372 ms: 1.08x slower                                                             |
| mypy2                      | 686 ms                                                 | 740 ms: 1.08x slower                                                             |
| pickle                     | 11.0 us                                                | 11.9 us: 1.08x slower                                                            |
| xml_etree_generate         | 81.1 ms                                                | 88.0 ms: 1.09x slower                                                            |
| genshi_text                | 22.5 ms                                                | 24.6 ms: 1.09x slower                                                            |
| regex_dna                  | 205 ms                                                 | 225 ms: 1.10x slower                                                             |
| pyflate                    | 434 ms                                                 | 481 ms: 1.11x slower                                                             |
| regex_v8                   | 22.9 ms                                                | 25.8 ms: 1.13x slower                                                            |
| unpickle                   | 13.8 us                                                | 15.9 us: 1.15x slower                                                            |
| sqlite_synth               | 2.57 us                                                | 2.96 us: 1.15x slower                                                            |
| async_generators           | 374 ms                                                 | 444 ms: 1.19x slower                                                             |
| create_gc_cycles           | 1.43 ms                                                | 1.72 ms: 1.20x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.22x slower                                                            |
| coverage                   | 78.8 ms                                                | 97.3 ms: 1.24x slower                                                            |
| telco                      | 6.86 ms                                                | 8.62 ms: 1.26x slower                                                            |
| python_startup_no_site     | 6.01 ms                                                | 8.93 ms: 1.48x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                     |

Benchmark hidden because not significant (5): bench_mp_pool, xml_etree_iterparse, deepcopy_reduce, genshi_xml, dask
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 96.58% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x