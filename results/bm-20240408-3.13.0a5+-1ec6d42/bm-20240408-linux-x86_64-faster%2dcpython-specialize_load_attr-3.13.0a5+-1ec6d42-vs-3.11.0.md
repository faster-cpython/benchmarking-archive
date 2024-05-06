# Results vs. 3.11.0

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: 1ec6d42
- commit date: 2024-04-08
- overall geometric mean: 1.06x faster
- HPT reliability: 95.27%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 271 ms: 1.03x slower                                                             |
| chameleon      | 6.70 ms                                                | 7.01 ms: 1.05x slower                                                            |
| docutils       | 2.66 sec                                               | 2.83 sec: 1.06x slower                                                           |
| html5lib       | 64.8 ms                                                | 68.9 ms: 1.06x slower                                                            |
| tornado_http   | 98.1 ms                                                | 94.5 ms: 1.04x faster                                                            |
| Geometric mean | (ref)                                                  | 1.03x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 352 ms: 1.50x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 333 ms: 1.48x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.41x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 924 ms: 1.40x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 459 ms: 1.39x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 926 ms: 1.39x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 609 ms: 1.25x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 614 ms: 1.22x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.38x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 89.5 ms: 1.07x faster                                                            |
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                                             |
| float          | 78.9 ms                                                | 79.3 ms: 1.00x slower                                                            |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 136 ms: 1.04x faster                                                             |
| regex_effbot   | 3.51 ms                                                | 3.86 ms: 1.10x slower                                                            |
| regex_v8       | 22.9 ms                                                | 25.4 ms: 1.11x slower                                                            |
| regex_dna      | 205 ms                                                 | 232 ms: 1.13x slower                                                             |
| Geometric mean | (ref)                                                  | 1.07x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                            |
| unpickle_pure_python | 242 us                                                 | 226 us: 1.07x faster                                                             |
| tomli_loads          | 2.30 sec                                               | 2.16 sec: 1.07x faster                                                           |
| pickle_pure_python   | 320 us                                                 | 305 us: 1.05x faster                                                             |
| unpickle_list        | 5.21 us                                                | 5.00 us: 1.04x faster                                                            |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.03x faster                                                             |
| json_loads           | 29.2 us                                                | 28.7 us: 1.02x faster                                                            |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                             |
| pickle_dict          | 34.6 us                                                | 35.4 us: 1.02x slower                                                            |
| xml_etree_process    | 56.9 ms                                                | 60.5 ms: 1.06x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 87.9 ms: 1.08x slower                                                            |
| pickle               | 11.0 us                                                | 11.9 us: 1.08x slower                                                            |
| unpickle             | 13.8 us                                                | 15.2 us: 1.10x slower                                                            |
| pickle_list          | 4.59 us                                                | 5.35 us: 1.17x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.22x slower                                                            |
| python_startup_no_site | 6.01 ms                                                | 8.93 ms: 1.48x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.35x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml     | 53.4 ms                                                | 52.6 ms: 1.02x faster                                                            |
| mako           | 10.7 ms                                                | 11.0 ms: 1.03x slower                                                            |
| genshi_text    | 22.5 ms                                                | 23.8 ms: 1.06x slower                                                            |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240408-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-1ec6d42 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 114 us: 4.55x faster                                                             |
| generators                 | 74.9 ms                                                | 30.0 ms: 2.50x faster                                                            |
| asyncio_tcp                | 875 ms                                                 | 513 ms: 1.71x faster                                                             |
| pylint                     | 476 ms                                                 | 282 ms: 1.69x faster                                                             |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                           |
| async_tree_none            | 528 ms                                                 | 352 ms: 1.50x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 333 ms: 1.48x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.41x faster                                                             |
| comprehensions             | 23.6 us                                                | 16.8 us: 1.40x faster                                                            |
| async_tree_io_tg           | 1.29 sec                                               | 924 ms: 1.40x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 459 ms: 1.39x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 926 ms: 1.39x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 609 ms: 1.25x faster                                                             |
| coroutines                 | 27.0 ms                                                | 22.1 ms: 1.22x faster                                                            |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 614 ms: 1.22x faster                                                             |
| deltablue                  | 3.92 ms                                                | 3.27 ms: 1.20x faster                                                            |
| chaos                      | 71.9 ms                                                | 60.8 ms: 1.18x faster                                                            |
| raytrace                   | 309 ms                                                 | 265 ms: 1.16x faster                                                             |
| richards_super             | 61.9 ms                                                | 53.7 ms: 1.15x faster                                                            |
| sqlglot_parse              | 1.43 ms                                                | 1.30 ms: 1.11x faster                                                            |
| sqlglot_transpile          | 1.75 ms                                                | 1.60 ms: 1.09x faster                                                            |
| logging_silent             | 111 ns                                                 | 102 ns: 1.09x faster                                                             |
| sympy_sum                  | 169 ms                                                 | 157 ms: 1.07x faster                                                             |
| nbody                      | 96.0 ms                                                | 89.5 ms: 1.07x faster                                                            |
| unpickle_pure_python       | 242 us                                                 | 226 us: 1.07x faster                                                             |
| tomli_loads                | 2.30 sec                                               | 2.16 sec: 1.07x faster                                                           |
| gc_traversal               | 4.01 ms                                                | 3.76 ms: 1.07x faster                                                            |
| hexiom                     | 6.89 ms                                                | 6.47 ms: 1.06x faster                                                            |
| logging_simple             | 6.22 us                                                | 5.88 us: 1.06x faster                                                            |
| sympy_str                  | 297 ms                                                 | 281 ms: 1.06x faster                                                             |
| richards                   | 49.8 ms                                                | 47.4 ms: 1.05x faster                                                            |
| nqueens                    | 87.9 ms                                                | 83.7 ms: 1.05x faster                                                            |
| deepcopy_memo              | 40.2 us                                                | 38.2 us: 1.05x faster                                                            |
| pickle_pure_python         | 320 us                                                 | 305 us: 1.05x faster                                                             |
| mdp                        | 2.77 sec                                               | 2.65 sec: 1.05x faster                                                           |
| unpickle_list              | 5.21 us                                                | 5.00 us: 1.04x faster                                                            |
| sympy_integrate            | 21.5 ms                                                | 20.6 ms: 1.04x faster                                                            |
| regex_compile              | 141 ms                                                 | 136 ms: 1.04x faster                                                             |
| logging_format             | 6.81 us                                                | 6.55 us: 1.04x faster                                                            |
| scimark_monte_carlo        | 70.7 ms                                                | 68.1 ms: 1.04x faster                                                            |
| tornado_http               | 98.1 ms                                                | 94.5 ms: 1.04x faster                                                            |
| go                         | 149 ms                                                 | 144 ms: 1.03x faster                                                             |
| fannkuch                   | 405 ms                                                 | 393 ms: 1.03x faster                                                             |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.03x faster                                                             |
| sympy_expand               | 484 ms                                                 | 473 ms: 1.02x faster                                                             |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                                             |
| scimark_lu                 | 116 ms                                                 | 114 ms: 1.02x faster                                                             |
| genshi_xml                 | 53.4 ms                                                | 52.6 ms: 1.02x faster                                                            |
| json_loads                 | 29.2 us                                                | 28.7 us: 1.02x faster                                                            |
| crypto_pyaes               | 76.7 ms                                                | 76.0 ms: 1.01x faster                                                            |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                             |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.00x faster                                                            |
| pprint_pformat             | 1.55 sec                                               | 1.56 sec: 1.00x slower                                                           |
| float                      | 78.9 ms                                                | 79.3 ms: 1.00x slower                                                            |
| bench_thread_pool          | 834 us                                                 | 839 us: 1.00x slower                                                             |
| sqlglot_optimize           | 55.3 ms                                                | 55.9 ms: 1.01x slower                                                            |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.01x slower                                                             |
| pathlib                    | 18.5 ms                                                | 18.8 ms: 1.02x slower                                                            |
| pycparser                  | 1.19 sec                                               | 1.21 sec: 1.02x slower                                                           |
| pprint_safe_repr           | 747 ms                                                 | 761 ms: 1.02x slower                                                             |
| pickle_dict                | 34.6 us                                                | 35.4 us: 1.02x slower                                                            |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.15 ms: 1.02x slower                                                            |
| json                       | 5.24 ms                                                | 5.38 ms: 1.03x slower                                                            |
| 2to3                       | 264 ms                                                 | 271 ms: 1.03x slower                                                             |
| scimark_sor                | 121 ms                                                 | 125 ms: 1.03x slower                                                             |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                             |
| deepcopy_reduce            | 3.22 us                                                | 3.32 us: 1.03x slower                                                            |
| mako                       | 10.7 ms                                                | 11.0 ms: 1.03x slower                                                            |
| thrift                     | 784 us                                                 | 811 us: 1.03x slower                                                             |
| spectral_norm              | 108 ms                                                 | 112 ms: 1.03x slower                                                             |
| dulwich_log                | 64.6 ms                                                | 67.6 ms: 1.05x slower                                                            |
| chameleon                  | 6.70 ms                                                | 7.01 ms: 1.05x slower                                                            |
| scimark_fft                | 345 ms                                                 | 362 ms: 1.05x slower                                                             |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                            |
| genshi_text                | 22.5 ms                                                | 23.8 ms: 1.06x slower                                                            |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                                            |
| html5lib                   | 64.8 ms                                                | 68.9 ms: 1.06x slower                                                            |
| docutils                   | 2.66 sec                                               | 2.83 sec: 1.06x slower                                                           |
| xml_etree_process          | 56.9 ms                                                | 60.5 ms: 1.06x slower                                                            |
| pyflate                    | 434 ms                                                 | 469 ms: 1.08x slower                                                             |
| mypy2                      | 686 ms                                                 | 742 ms: 1.08x slower                                                             |
| xml_etree_generate         | 81.1 ms                                                | 87.9 ms: 1.08x slower                                                            |
| pickle                     | 11.0 us                                                | 11.9 us: 1.08x slower                                                            |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.10x slower                                                            |
| regex_effbot               | 3.51 ms                                                | 3.86 ms: 1.10x slower                                                            |
| regex_v8                   | 22.9 ms                                                | 25.4 ms: 1.11x slower                                                            |
| regex_dna                  | 205 ms                                                 | 232 ms: 1.13x slower                                                             |
| sqlite_synth               | 2.57 us                                                | 2.93 us: 1.14x slower                                                            |
| pickle_list                | 4.59 us                                                | 5.35 us: 1.17x slower                                                            |
| async_generators           | 374 ms                                                 | 448 ms: 1.20x slower                                                             |
| create_gc_cycles           | 1.43 ms                                                | 1.73 ms: 1.20x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.22x slower                                                            |
| coverage                   | 78.8 ms                                                | 97.2 ms: 1.23x slower                                                            |
| telco                      | 6.86 ms                                                | 8.54 ms: 1.25x slower                                                            |
| python_startup_no_site     | 6.01 ms                                                | 8.93 ms: 1.48x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                     |

Benchmark hidden because not significant (3): sqlglot_normalize, deepcopy, dask
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 95.27% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x