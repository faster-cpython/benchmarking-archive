# Results vs. 3.11.0

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: 5032ad9
- commit date: 2024-05-01
- overall geometric mean: 1.06x faster
- HPT reliability: 98.27%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 272 ms: 1.03x slower                                                             |
| chameleon      | 6.70 ms                                                | 7.26 ms: 1.08x slower                                                            |
| docutils       | 2.66 sec                                               | 2.82 sec: 1.06x slower                                                           |
| html5lib       | 64.8 ms                                                | 68.6 ms: 1.06x slower                                                            |
| tornado_http   | 98.1 ms                                                | 93.6 ms: 1.05x faster                                                            |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 356 ms: 1.48x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.46x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 920 ms: 1.40x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 929 ms: 1.39x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 468 ms: 1.37x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 610 ms: 1.25x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 613 ms: 1.22x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 88.3 ms: 1.09x faster                                                            |
| pidigits       | 194 ms                                                 | 191 ms: 1.02x faster                                                             |
| float          | 78.9 ms                                                | 77.9 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 134 ms: 1.05x faster                                                             |
| regex_effbot   | 3.51 ms                                                | 3.89 ms: 1.11x slower                                                            |
| regex_v8       | 22.9 ms                                                | 25.8 ms: 1.13x slower                                                            |
| regex_dna      | 205 ms                                                 | 230 ms: 1.13x slower                                                             |
| Geometric mean | (ref)                                                  | 1.08x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                            |
| unpickle_pure_python | 242 us                                                 | 217 us: 1.12x faster                                                             |
| tomli_loads          | 2.30 sec                                               | 2.17 sec: 1.06x faster                                                           |
| xml_etree_parse      | 164 ms                                                 | 158 ms: 1.04x faster                                                             |
| pickle_pure_python   | 320 us                                                 | 311 us: 1.03x faster                                                             |
| json_loads           | 29.2 us                                                | 28.4 us: 1.03x faster                                                            |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                             |
| pickle_dict          | 34.6 us                                                | 34.7 us: 1.00x slower                                                            |
| unpickle_list        | 5.21 us                                                | 5.28 us: 1.01x slower                                                            |
| xml_etree_process    | 56.9 ms                                                | 61.8 ms: 1.09x slower                                                            |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 89.0 ms: 1.10x slower                                                            |
| pickle_list          | 4.59 us                                                | 5.05 us: 1.10x slower                                                            |
| unpickle             | 13.8 us                                                | 15.3 us: 1.11x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.09 ms: 1.18x slower                                                            |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 51.4 ms: 1.04x faster                                                            |
| genshi_text     | 22.5 ms                                                | 23.0 ms: 1.02x slower                                                            |
| django_template | 33.5 ms                                                | 34.6 ms: 1.03x slower                                                            |
| mako            | 10.7 ms                                                | 11.5 ms: 1.07x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-5032ad9 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 164 us: 3.16x faster                                                             |
| generators                 | 74.9 ms                                                | 29.1 ms: 2.57x faster                                                            |
| asyncio_tcp                | 875 ms                                                 | 511 ms: 1.71x faster                                                             |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                           |
| pylint                     | 476 ms                                                 | 319 ms: 1.49x faster                                                             |
| async_tree_none            | 528 ms                                                 | 356 ms: 1.48x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.46x faster                                                             |
| comprehensions             | 23.6 us                                                | 16.4 us: 1.44x faster                                                            |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 920 ms: 1.40x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 929 ms: 1.39x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 468 ms: 1.37x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 610 ms: 1.25x faster                                                             |
| coroutines                 | 27.0 ms                                                | 22.0 ms: 1.23x faster                                                            |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 613 ms: 1.22x faster                                                             |
| deltablue                  | 3.92 ms                                                | 3.22 ms: 1.22x faster                                                            |
| chaos                      | 71.9 ms                                                | 60.6 ms: 1.19x faster                                                            |
| raytrace                   | 309 ms                                                 | 267 ms: 1.16x faster                                                             |
| richards_super             | 61.9 ms                                                | 54.6 ms: 1.13x faster                                                            |
| logging_silent             | 111 ns                                                 | 98.1 ns: 1.13x faster                                                            |
| hexiom                     | 6.89 ms                                                | 6.16 ms: 1.12x faster                                                            |
| unpickle_pure_python       | 242 us                                                 | 217 us: 1.12x faster                                                             |
| sqlglot_parse              | 1.43 ms                                                | 1.29 ms: 1.11x faster                                                            |
| nqueens                    | 87.9 ms                                                | 79.6 ms: 1.10x faster                                                            |
| sqlglot_transpile          | 1.75 ms                                                | 1.60 ms: 1.09x faster                                                            |
| sympy_sum                  | 169 ms                                                 | 155 ms: 1.09x faster                                                             |
| nbody                      | 96.0 ms                                                | 88.3 ms: 1.09x faster                                                            |
| logging_simple             | 6.22 us                                                | 5.80 us: 1.07x faster                                                            |
| sympy_str                  | 297 ms                                                 | 278 ms: 1.07x faster                                                             |
| logging_format             | 6.81 us                                                | 6.39 us: 1.07x faster                                                            |
| tomli_loads                | 2.30 sec                                               | 2.17 sec: 1.06x faster                                                           |
| deepcopy_memo              | 40.2 us                                                | 38.0 us: 1.06x faster                                                            |
| pathlib                    | 18.5 ms                                                | 17.6 ms: 1.06x faster                                                            |
| sympy_integrate            | 21.5 ms                                                | 20.3 ms: 1.06x faster                                                            |
| regex_compile              | 141 ms                                                 | 134 ms: 1.05x faster                                                             |
| djangocms                  | 33.5 us                                                | 31.9 us: 1.05x faster                                                            |
| tornado_http               | 98.1 ms                                                | 93.6 ms: 1.05x faster                                                            |
| genshi_xml                 | 53.4 ms                                                | 51.4 ms: 1.04x faster                                                            |
| xml_etree_parse            | 164 ms                                                 | 158 ms: 1.04x faster                                                             |
| richards                   | 49.8 ms                                                | 48.3 ms: 1.03x faster                                                            |
| sympy_expand               | 484 ms                                                 | 470 ms: 1.03x faster                                                             |
| go                         | 149 ms                                                 | 144 ms: 1.03x faster                                                             |
| pickle_pure_python         | 320 us                                                 | 311 us: 1.03x faster                                                             |
| json_loads                 | 29.2 us                                                | 28.4 us: 1.03x faster                                                            |
| sqlglot_normalize          | 113 ms                                                 | 110 ms: 1.03x faster                                                             |
| mdp                        | 2.77 sec                                               | 2.72 sec: 1.02x faster                                                           |
| pidigits                   | 194 ms                                                 | 191 ms: 1.02x faster                                                             |
| crypto_pyaes               | 76.7 ms                                                | 75.6 ms: 1.01x faster                                                            |
| bench_thread_pool          | 834 us                                                 | 824 us: 1.01x faster                                                             |
| float                      | 78.9 ms                                                | 77.9 ms: 1.01x faster                                                            |
| deepcopy                   | 365 us                                                 | 361 us: 1.01x faster                                                             |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                             |
| sqlglot_optimize           | 55.3 ms                                                | 54.9 ms: 1.01x faster                                                            |
| gc_traversal               | 4.01 ms                                                | 3.98 ms: 1.01x faster                                                            |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                            |
| fannkuch                   | 405 ms                                                 | 403 ms: 1.00x faster                                                             |
| pickle_dict                | 34.6 us                                                | 34.7 us: 1.00x slower                                                            |
| scimark_lu                 | 116 ms                                                 | 118 ms: 1.01x slower                                                             |
| unpickle_list              | 5.21 us                                                | 5.28 us: 1.01x slower                                                            |
| pprint_safe_repr           | 747 ms                                                 | 758 ms: 1.01x slower                                                             |
| spectral_norm              | 108 ms                                                 | 110 ms: 1.02x slower                                                             |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                                             |
| dulwich_log                | 64.6 ms                                                | 65.6 ms: 1.02x slower                                                            |
| genshi_text                | 22.5 ms                                                | 23.0 ms: 1.02x slower                                                            |
| pycparser                  | 1.19 sec                                               | 1.21 sec: 1.02x slower                                                           |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                                             |
| json                       | 5.24 ms                                                | 5.37 ms: 1.02x slower                                                            |
| 2to3                       | 264 ms                                                 | 272 ms: 1.03x slower                                                             |
| django_template            | 33.5 ms                                                | 34.6 ms: 1.03x slower                                                            |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.21 ms: 1.04x slower                                                            |
| thrift                     | 784 us                                                 | 814 us: 1.04x slower                                                             |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                            |
| html5lib                   | 64.8 ms                                                | 68.6 ms: 1.06x slower                                                            |
| docutils                   | 2.66 sec                                               | 2.82 sec: 1.06x slower                                                           |
| gunicorn                   | 1.20 ms                                                | 1.28 ms: 1.07x slower                                                            |
| mako                       | 10.7 ms                                                | 11.5 ms: 1.07x slower                                                            |
| mypy2                      | 686 ms                                                 | 738 ms: 1.08x slower                                                             |
| scimark_sor                | 121 ms                                                 | 131 ms: 1.08x slower                                                             |
| chameleon                  | 6.70 ms                                                | 7.26 ms: 1.08x slower                                                            |
| xml_etree_process          | 56.9 ms                                                | 61.8 ms: 1.09x slower                                                            |
| pickle                     | 11.0 us                                                | 12.0 us: 1.09x slower                                                            |
| scimark_fft                | 345 ms                                                 | 377 ms: 1.09x slower                                                             |
| xml_etree_generate         | 81.1 ms                                                | 89.0 ms: 1.10x slower                                                            |
| pickle_list                | 4.59 us                                                | 5.05 us: 1.10x slower                                                            |
| unpickle                   | 13.8 us                                                | 15.3 us: 1.11x slower                                                            |
| pyflate                    | 434 ms                                                 | 480 ms: 1.11x slower                                                             |
| regex_effbot               | 3.51 ms                                                | 3.89 ms: 1.11x slower                                                            |
| regex_v8                   | 22.9 ms                                                | 25.8 ms: 1.13x slower                                                            |
| regex_dna                  | 205 ms                                                 | 230 ms: 1.13x slower                                                             |
| sqlite_synth               | 2.57 us                                                | 2.95 us: 1.15x slower                                                            |
| python_startup_no_site     | 6.01 ms                                                | 7.09 ms: 1.18x slower                                                            |
| coverage                   | 78.8 ms                                                | 93.0 ms: 1.18x slower                                                            |
| async_generators           | 374 ms                                                 | 445 ms: 1.19x slower                                                             |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| telco                      | 6.86 ms                                                | 8.53 ms: 1.24x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                     |

Benchmark hidden because not significant (4): scimark_monte_carlo, pprint_pformat, deepcopy_reduce, dask
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 98.27% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x