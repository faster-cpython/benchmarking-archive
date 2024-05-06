# Results vs. 3.11.0

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: a7b858b
- commit date: 2024-05-02
- overall geometric mean: 1.07x faster
- HPT reliability: 96.25%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 272 ms: 1.03x slower                                                             |
| chameleon      | 6.70 ms                                                | 7.22 ms: 1.08x slower                                                            |
| docutils       | 2.66 sec                                               | 2.82 sec: 1.06x slower                                                           |
| html5lib       | 64.8 ms                                                | 70.3 ms: 1.08x slower                                                            |
| tornado_http   | 98.1 ms                                                | 93.2 ms: 1.05x faster                                                            |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 352 ms: 1.50x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 341 ms: 1.44x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 450 ms: 1.39x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 927 ms: 1.39x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 960 ms: 1.35x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 614 ms: 1.24x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 613 ms: 1.22x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.36x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 89.5 ms: 1.07x faster                                                            |
| pidigits       | 194 ms                                                 | 193 ms: 1.01x faster                                                             |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                     |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 135 ms: 1.05x faster                                                             |
| regex_effbot   | 3.51 ms                                                | 3.62 ms: 1.03x slower                                                            |
| regex_v8       | 22.9 ms                                                | 24.6 ms: 1.07x slower                                                            |
| regex_dna      | 205 ms                                                 | 224 ms: 1.10x slower                                                             |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                            |
| unpickle_pure_python | 242 us                                                 | 220 us: 1.10x faster                                                             |
| tomli_loads          | 2.30 sec                                               | 2.13 sec: 1.08x faster                                                           |
| xml_etree_parse      | 164 ms                                                 | 159 ms: 1.03x faster                                                             |
| json_loads           | 29.2 us                                                | 28.5 us: 1.02x faster                                                            |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                             |
| unpickle_list        | 5.21 us                                                | 5.19 us: 1.00x faster                                                            |
| pickle_dict          | 34.6 us                                                | 35.9 us: 1.04x slower                                                            |
| xml_etree_process    | 56.9 ms                                                | 61.0 ms: 1.07x slower                                                            |
| pickle               | 11.0 us                                                | 11.9 us: 1.08x slower                                                            |
| xml_etree_generate   | 81.1 ms                                                | 88.0 ms: 1.09x slower                                                            |
| unpickle             | 13.8 us                                                | 15.5 us: 1.12x slower                                                            |
| pickle_list          | 4.59 us                                                | 5.16 us: 1.12x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.00x slower                                                                     |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.11 ms: 1.18x slower                                                            |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 50.8 ms: 1.05x faster                                                            |
| genshi_text     | 22.5 ms                                                | 23.0 ms: 1.02x slower                                                            |
| django_template | 33.5 ms                                                | 34.7 ms: 1.04x slower                                                            |
| mako            | 10.7 ms                                                | 11.3 ms: 1.06x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 165 us: 3.15x faster                                                             |
| generators                 | 74.9 ms                                                | 29.4 ms: 2.55x faster                                                            |
| asyncio_tcp                | 875 ms                                                 | 506 ms: 1.73x faster                                                             |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                           |
| pylint                     | 476 ms                                                 | 318 ms: 1.50x faster                                                             |
| async_tree_none            | 528 ms                                                 | 352 ms: 1.50x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 341 ms: 1.44x faster                                                             |
| comprehensions             | 23.6 us                                                | 16.7 us: 1.42x faster                                                            |
| async_tree_memoization_tg  | 626 ms                                                 | 450 ms: 1.39x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 927 ms: 1.39x faster                                                             |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 960 ms: 1.35x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                            |
| go                         | 149 ms                                                 | 119 ms: 1.25x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 614 ms: 1.24x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 613 ms: 1.22x faster                                                             |
| coroutines                 | 27.0 ms                                                | 22.2 ms: 1.22x faster                                                            |
| deltablue                  | 3.92 ms                                                | 3.23 ms: 1.21x faster                                                            |
| chaos                      | 71.9 ms                                                | 60.5 ms: 1.19x faster                                                            |
| raytrace                   | 309 ms                                                 | 262 ms: 1.18x faster                                                             |
| richards_super             | 61.9 ms                                                | 53.5 ms: 1.16x faster                                                            |
| sqlglot_parse              | 1.43 ms                                                | 1.29 ms: 1.11x faster                                                            |
| hexiom                     | 6.89 ms                                                | 6.22 ms: 1.11x faster                                                            |
| nqueens                    | 87.9 ms                                                | 79.6 ms: 1.10x faster                                                            |
| logging_silent             | 111 ns                                                 | 101 ns: 1.10x faster                                                             |
| unpickle_pure_python       | 242 us                                                 | 220 us: 1.10x faster                                                             |
| sqlglot_transpile          | 1.75 ms                                                | 1.60 ms: 1.09x faster                                                            |
| sympy_sum                  | 169 ms                                                 | 155 ms: 1.09x faster                                                             |
| logging_simple             | 6.22 us                                                | 5.70 us: 1.09x faster                                                            |
| tomli_loads                | 2.30 sec                                               | 2.13 sec: 1.08x faster                                                           |
| djangocms                  | 33.5 us                                                | 31.2 us: 1.08x faster                                                            |
| logging_format             | 6.81 us                                                | 6.33 us: 1.08x faster                                                            |
| nbody                      | 96.0 ms                                                | 89.5 ms: 1.07x faster                                                            |
| deepcopy_memo              | 40.2 us                                                | 37.6 us: 1.07x faster                                                            |
| sympy_str                  | 297 ms                                                 | 280 ms: 1.06x faster                                                             |
| sympy_integrate            | 21.5 ms                                                | 20.3 ms: 1.06x faster                                                            |
| pathlib                    | 18.5 ms                                                | 17.6 ms: 1.05x faster                                                            |
| gc_traversal               | 4.01 ms                                                | 3.81 ms: 1.05x faster                                                            |
| tornado_http               | 98.1 ms                                                | 93.2 ms: 1.05x faster                                                            |
| genshi_xml                 | 53.4 ms                                                | 50.8 ms: 1.05x faster                                                            |
| richards                   | 49.8 ms                                                | 47.4 ms: 1.05x faster                                                            |
| regex_compile              | 141 ms                                                 | 135 ms: 1.05x faster                                                             |
| xml_etree_parse            | 164 ms                                                 | 159 ms: 1.03x faster                                                             |
| fannkuch                   | 405 ms                                                 | 394 ms: 1.03x faster                                                             |
| pycparser                  | 1.19 sec                                               | 1.15 sec: 1.03x faster                                                           |
| json_loads                 | 29.2 us                                                | 28.5 us: 1.02x faster                                                            |
| sympy_expand               | 484 ms                                                 | 473 ms: 1.02x faster                                                             |
| sqlglot_normalize          | 113 ms                                                 | 110 ms: 1.02x faster                                                             |
| deepcopy                   | 365 us                                                 | 358 us: 1.02x faster                                                             |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                             |
| deepcopy_reduce            | 3.22 us                                                | 3.18 us: 1.01x faster                                                            |
| bench_thread_pool          | 834 us                                                 | 828 us: 1.01x faster                                                             |
| meteor_contest             | 109 ms                                                 | 108 ms: 1.01x faster                                                             |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                            |
| scimark_lu                 | 116 ms                                                 | 116 ms: 1.01x faster                                                             |
| pidigits                   | 194 ms                                                 | 193 ms: 1.01x faster                                                             |
| unpickle_list              | 5.21 us                                                | 5.19 us: 1.00x faster                                                            |
| sqlglot_optimize           | 55.3 ms                                                | 55.5 ms: 1.00x slower                                                            |
| mdp                        | 2.77 sec                                               | 2.79 sec: 1.00x slower                                                           |
| dulwich_log                | 64.6 ms                                                | 65.5 ms: 1.01x slower                                                            |
| json                       | 5.24 ms                                                | 5.33 ms: 1.02x slower                                                            |
| pprint_safe_repr           | 747 ms                                                 | 761 ms: 1.02x slower                                                             |
| genshi_text                | 22.5 ms                                                | 23.0 ms: 1.02x slower                                                            |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                                             |
| 2to3                       | 264 ms                                                 | 272 ms: 1.03x slower                                                             |
| regex_effbot               | 3.51 ms                                                | 3.62 ms: 1.03x slower                                                            |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.20 ms: 1.03x slower                                                            |
| django_template            | 33.5 ms                                                | 34.7 ms: 1.04x slower                                                            |
| pickle_dict                | 34.6 us                                                | 35.9 us: 1.04x slower                                                            |
| spectral_norm              | 108 ms                                                 | 112 ms: 1.04x slower                                                             |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                            |
| thrift                     | 784 us                                                 | 823 us: 1.05x slower                                                             |
| scimark_monte_carlo        | 70.7 ms                                                | 74.2 ms: 1.05x slower                                                            |
| gunicorn                   | 1.20 ms                                                | 1.26 ms: 1.05x slower                                                            |
| docutils                   | 2.66 sec                                               | 2.82 sec: 1.06x slower                                                           |
| mako                       | 10.7 ms                                                | 11.3 ms: 1.06x slower                                                            |
| scimark_fft                | 345 ms                                                 | 368 ms: 1.07x slower                                                             |
| xml_etree_process          | 56.9 ms                                                | 61.0 ms: 1.07x slower                                                            |
| regex_v8                   | 22.9 ms                                                | 24.6 ms: 1.07x slower                                                            |
| chameleon                  | 6.70 ms                                                | 7.22 ms: 1.08x slower                                                            |
| mypy2                      | 686 ms                                                 | 739 ms: 1.08x slower                                                             |
| pickle                     | 11.0 us                                                | 11.9 us: 1.08x slower                                                            |
| pyflate                    | 434 ms                                                 | 470 ms: 1.08x slower                                                             |
| html5lib                   | 64.8 ms                                                | 70.3 ms: 1.08x slower                                                            |
| xml_etree_generate         | 81.1 ms                                                | 88.0 ms: 1.09x slower                                                            |
| crypto_pyaes               | 76.7 ms                                                | 83.7 ms: 1.09x slower                                                            |
| regex_dna                  | 205 ms                                                 | 224 ms: 1.10x slower                                                             |
| scimark_sor                | 121 ms                                                 | 134 ms: 1.10x slower                                                             |
| unpickle                   | 13.8 us                                                | 15.5 us: 1.12x slower                                                            |
| pickle_list                | 4.59 us                                                | 5.16 us: 1.12x slower                                                            |
| sqlite_synth               | 2.57 us                                                | 2.90 us: 1.13x slower                                                            |
| python_startup_no_site     | 6.01 ms                                                | 7.11 ms: 1.18x slower                                                            |
| async_generators           | 374 ms                                                 | 442 ms: 1.18x slower                                                             |
| coverage                   | 78.8 ms                                                | 93.8 ms: 1.19x slower                                                            |
| create_gc_cycles           | 1.43 ms                                                | 1.76 ms: 1.23x slower                                                            |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                            |
| telco                      | 6.86 ms                                                | 8.50 ms: 1.24x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                                     |

Benchmark hidden because not significant (4): pprint_pformat, float, pickle_pure_python, dask
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 96.25% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x