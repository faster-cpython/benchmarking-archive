# Results vs. 3.12.0

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: a7b858b
- commit date: 2024-05-02
- overall geometric mean: 1.04x faster
- HPT reliability: 99.94%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 272 ms: 1.01x faster                                                             |
| chameleon      | 7.41 ms                                                | 7.22 ms: 1.03x faster                                                            |
| docutils       | 2.77 sec                                               | 2.82 sec: 1.02x slower                                                           |
| tornado_http   | 103 ms                                                 | 93.2 ms: 1.10x faster                                                            |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 472 ms                                                 | 352 ms: 1.34x faster                                                             |
| async_tree_none_tg         | 450 ms                                                 | 341 ms: 1.32x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 450 ms: 1.28x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 462 ms: 1.25x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 927 ms: 1.25x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 960 ms: 1.23x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 613 ms: 1.18x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 614 ms: 1.18x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.25x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 89.5 ms: 1.08x faster                                                            |
| float          | 84.7 ms                                                | 78.9 ms: 1.07x faster                                                            |
| pidigits       | 187 ms                                                 | 193 ms: 1.03x slower                                                             |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 135 ms: 1.10x faster                                                             |
| regex_dna      | 212 ms                                                 | 224 ms: 1.06x slower                                                             |
| regex_v8       | 23.1 ms                                                | 24.6 ms: 1.06x slower                                                            |
| Geometric mean | (ref)                                                  | 1.01x slower                                                                     |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.13 sec: 1.09x faster                                                           |
| unpickle_pure_python | 230 us                                                 | 220 us: 1.05x faster                                                             |
| unpickle             | 15.9 us                                                | 15.5 us: 1.02x faster                                                            |
| unpickle_list        | 5.29 us                                                | 5.19 us: 1.02x faster                                                            |
| xml_etree_generate   | 89.2 ms                                                | 88.0 ms: 1.01x faster                                                            |
| pickle_pure_python   | 324 us                                                 | 320 us: 1.01x faster                                                             |
| xml_etree_process    | 61.7 ms                                                | 61.0 ms: 1.01x faster                                                            |
| pickle_dict          | 35.5 us                                                | 35.9 us: 1.01x slower                                                            |
| pickle_list          | 5.08 us                                                | 5.16 us: 1.01x slower                                                            |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                            |
| pickle               | 11.6 us                                                | 11.9 us: 1.03x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (3): xml_etree_iterparse, json_loads, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.11 ms: 1.02x slower                                                            |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 11.3 ms: 1.05x faster                                                            |
| django_template | 34.6 ms                                                | 34.7 ms: 1.00x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 472 ms                                                 | 352 ms: 1.34x faster                                                             |
| async_tree_none_tg         | 450 ms                                                 | 341 ms: 1.32x faster                                                             |
| comprehensions             | 21.8 us                                                | 16.7 us: 1.31x faster                                                            |
| async_tree_memoization_tg  | 575 ms                                                 | 450 ms: 1.28x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 462 ms: 1.25x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 927 ms: 1.25x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 960 ms: 1.23x faster                                                             |
| raytrace                   | 312 ms                                                 | 262 ms: 1.19x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 613 ms: 1.18x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 614 ms: 1.18x faster                                                             |
| go                         | 139 ms                                                 | 119 ms: 1.17x faster                                                             |
| deltablue                  | 3.72 ms                                                | 3.23 ms: 1.15x faster                                                            |
| logging_format             | 7.23 us                                                | 6.33 us: 1.14x faster                                                            |
| logging_simple             | 6.46 us                                                | 5.70 us: 1.13x faster                                                            |
| mypy2                      | 830 ms                                                 | 739 ms: 1.12x faster                                                             |
| chaos                      | 67.0 ms                                                | 60.5 ms: 1.11x faster                                                            |
| tornado_http               | 103 ms                                                 | 93.2 ms: 1.10x faster                                                            |
| pathlib                    | 19.3 ms                                                | 17.6 ms: 1.10x faster                                                            |
| regex_compile              | 148 ms                                                 | 135 ms: 1.10x faster                                                             |
| sympy_sum                  | 169 ms                                                 | 155 ms: 1.09x faster                                                             |
| tomli_loads                | 2.33 sec                                               | 2.13 sec: 1.09x faster                                                           |
| nbody                      | 97.0 ms                                                | 89.5 ms: 1.08x faster                                                            |
| deepcopy_memo              | 40.7 us                                                | 37.6 us: 1.08x faster                                                            |
| float                      | 84.7 ms                                                | 78.9 ms: 1.07x faster                                                            |
| sympy_str                  | 300 ms                                                 | 280 ms: 1.07x faster                                                             |
| generators                 | 31.2 ms                                                | 29.4 ms: 1.06x faster                                                            |
| fannkuch                   | 417 ms                                                 | 394 ms: 1.06x faster                                                             |
| sympy_integrate            | 21.4 ms                                                | 20.3 ms: 1.06x faster                                                            |
| mako                       | 11.9 ms                                                | 11.3 ms: 1.05x faster                                                            |
| sqlglot_parse              | 1.36 ms                                                | 1.29 ms: 1.05x faster                                                            |
| deepcopy_reduce            | 3.35 us                                                | 3.18 us: 1.05x faster                                                            |
| sqlglot_transpile          | 1.68 ms                                                | 1.60 ms: 1.05x faster                                                            |
| async_generators           | 463 ms                                                 | 442 ms: 1.05x faster                                                             |
| dulwich_log                | 68.5 ms                                                | 65.5 ms: 1.05x faster                                                            |
| nqueens                    | 83.3 ms                                                | 79.6 ms: 1.05x faster                                                            |
| unpickle_pure_python       | 230 us                                                 | 220 us: 1.05x faster                                                             |
| coroutines                 | 23.2 ms                                                | 22.2 ms: 1.04x faster                                                            |
| meteor_contest             | 112 ms                                                 | 108 ms: 1.04x faster                                                             |
| deepcopy                   | 371 us                                                 | 358 us: 1.04x faster                                                             |
| scimark_fft                | 382 ms                                                 | 368 ms: 1.04x faster                                                             |
| logging_silent             | 104 ns                                                 | 101 ns: 1.03x faster                                                             |
| hexiom                     | 6.41 ms                                                | 6.22 ms: 1.03x faster                                                            |
| chameleon                  | 7.41 ms                                                | 7.22 ms: 1.03x faster                                                            |
| pyflate                    | 482 ms                                                 | 470 ms: 1.03x faster                                                             |
| unpickle                   | 15.9 us                                                | 15.5 us: 1.02x faster                                                            |
| spectral_norm              | 115 ms                                                 | 112 ms: 1.02x faster                                                             |
| pycparser                  | 1.18 sec                                               | 1.15 sec: 1.02x faster                                                           |
| scimark_lu                 | 118 ms                                                 | 116 ms: 1.02x faster                                                             |
| pprint_safe_repr           | 776 ms                                                 | 761 ms: 1.02x faster                                                             |
| unpickle_list              | 5.29 us                                                | 5.19 us: 1.02x faster                                                            |
| bench_thread_pool          | 842 us                                                 | 828 us: 1.02x faster                                                             |
| xml_etree_generate         | 89.2 ms                                                | 88.0 ms: 1.01x faster                                                            |
| scimark_monte_carlo        | 75.1 ms                                                | 74.2 ms: 1.01x faster                                                            |
| pickle_pure_python         | 324 us                                                 | 320 us: 1.01x faster                                                             |
| xml_etree_process          | 61.7 ms                                                | 61.0 ms: 1.01x faster                                                            |
| sympy_expand               | 478 ms                                                 | 473 ms: 1.01x faster                                                             |
| pprint_pformat             | 1.57 sec                                               | 1.55 sec: 1.01x faster                                                           |
| 2to3                       | 274 ms                                                 | 272 ms: 1.01x faster                                                             |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                            |
| gc_traversal               | 3.79 ms                                                | 3.81 ms: 1.00x slower                                                            |
| django_template            | 34.6 ms                                                | 34.7 ms: 1.00x slower                                                            |
| pickle_dict                | 35.5 us                                                | 35.9 us: 1.01x slower                                                            |
| sqlglot_optimize           | 54.8 ms                                                | 55.5 ms: 1.01x slower                                                            |
| json                       | 5.26 ms                                                | 5.33 ms: 1.01x slower                                                            |
| pickle_list                | 5.08 us                                                | 5.16 us: 1.01x slower                                                            |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.02x slower                                                            |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                            |
| docutils                   | 2.77 sec                                               | 2.82 sec: 1.02x slower                                                           |
| gunicorn                   | 1.24 ms                                                | 1.26 ms: 1.02x slower                                                            |
| asyncio_websockets         | 551 ms                                                 | 563 ms: 1.02x slower                                                             |
| crypto_pyaes               | 81.9 ms                                                | 83.7 ms: 1.02x slower                                                            |
| python_startup_no_site     | 6.94 ms                                                | 7.11 ms: 1.02x slower                                                            |
| sqlite_synth               | 2.83 us                                                | 2.90 us: 1.02x slower                                                            |
| pickle                     | 11.6 us                                                | 11.9 us: 1.03x slower                                                            |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.20 ms: 1.03x slower                                                            |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                                           |
| pidigits                   | 187 ms                                                 | 193 ms: 1.03x slower                                                             |
| asyncio_tcp                | 491 ms                                                 | 506 ms: 1.03x slower                                                             |
| scimark_sor                | 129 ms                                                 | 134 ms: 1.03x slower                                                             |
| richards                   | 45.8 ms                                                | 47.4 ms: 1.04x slower                                                            |
| richards_super             | 51.5 ms                                                | 53.5 ms: 1.04x slower                                                            |
| typing_runtime_protocols   | 158 us                                                 | 165 us: 1.04x slower                                                             |
| regex_dna                  | 212 ms                                                 | 224 ms: 1.06x slower                                                             |
| mdp                        | 2.63 sec                                               | 2.79 sec: 1.06x slower                                                           |
| regex_v8                   | 23.1 ms                                                | 24.6 ms: 1.06x slower                                                            |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| create_gc_cycles           | 1.48 ms                                                | 1.76 ms: 1.19x slower                                                            |
| telco                      | 7.10 ms                                                | 8.50 ms: 1.20x slower                                                            |
| coverage                   | 72.7 ms                                                | 93.8 ms: 1.29x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                                     |

Benchmark hidden because not significant (6): dask, xml_etree_iterparse, json_loads, xml_etree_parse, sqlglot_normalize, regex_effbot
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240502-3.13.0a6+-a7b858b/bm-20240502-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-a7b858b.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.94% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.96x