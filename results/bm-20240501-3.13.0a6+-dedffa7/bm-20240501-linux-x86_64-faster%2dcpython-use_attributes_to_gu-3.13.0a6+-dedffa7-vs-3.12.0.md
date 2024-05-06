# Results vs. 3.12.0

- fork: faster-cpython
- ref: use_attributes_to_gu
- machine: linux-x86_64
- commit hash: dedffa7
- commit date: 2024-05-01
- overall geometric mean: 1.03x faster
- HPT reliability: 99.05%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 272 ms: 1.01x faster                                                             |
| docutils       | 2.77 sec                                               | 2.81 sec: 1.02x slower                                                           |
| tornado_http   | 103 ms                                                 | 93.8 ms: 1.09x faster                                                            |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                     |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 337 ms: 1.33x faster                                                             |
| async_tree_none            | 472 ms                                                 | 354 ms: 1.33x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 443 ms: 1.30x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 459 ms: 1.26x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 948 ms: 1.25x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 928 ms: 1.25x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 610 ms: 1.19x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 614 ms: 1.18x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 88.4 ms: 1.10x faster                                                            |
| float          | 84.7 ms                                                | 79.1 ms: 1.07x faster                                                            |
| pidigits       | 187 ms                                                 | 195 ms: 1.04x slower                                                             |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 134 ms: 1.11x faster                                                             |
| regex_effbot   | 3.61 ms                                                | 3.71 ms: 1.03x slower                                                            |
| regex_dna      | 212 ms                                                 | 225 ms: 1.06x slower                                                             |
| regex_v8       | 23.1 ms                                                | 25.6 ms: 1.11x slower                                                            |
| Geometric mean | (ref)                                                  | 1.02x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.16 sec: 1.08x faster                                                           |
| unpickle             | 15.9 us                                                | 15.1 us: 1.05x faster                                                            |
| pickle_pure_python   | 324 us                                                 | 311 us: 1.04x faster                                                             |
| unpickle_pure_python | 230 us                                                 | 221 us: 1.04x faster                                                             |
| json_loads           | 28.5 us                                                | 28.4 us: 1.00x faster                                                            |
| pickle_list          | 5.08 us                                                | 5.12 us: 1.01x slower                                                            |
| xml_etree_process    | 61.7 ms                                                | 62.3 ms: 1.01x slower                                                            |
| pickle_dict          | 35.5 us                                                | 35.9 us: 1.01x slower                                                            |
| unpickle_list        | 5.29 us                                                | 5.35 us: 1.01x slower                                                            |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                            |
| xml_etree_generate   | 89.2 ms                                                | 90.3 ms: 1.01x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                     |

Benchmark hidden because not significant (3): xml_etree_parse, pickle, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.08 ms: 1.02x slower                                                            |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 11.3 ms: 1.05x faster                                                            |
| django_template | 34.6 ms                                                | 35.1 ms: 1.01x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 337 ms: 1.33x faster                                                             |
| async_tree_none            | 472 ms                                                 | 354 ms: 1.33x faster                                                             |
| comprehensions             | 21.8 us                                                | 16.5 us: 1.32x faster                                                            |
| async_tree_memoization_tg  | 575 ms                                                 | 443 ms: 1.30x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 459 ms: 1.26x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 948 ms: 1.25x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 928 ms: 1.25x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 610 ms: 1.19x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 614 ms: 1.18x faster                                                             |
| raytrace                   | 312 ms                                                 | 266 ms: 1.18x faster                                                             |
| deltablue                  | 3.72 ms                                                | 3.23 ms: 1.15x faster                                                            |
| mypy2                      | 830 ms                                                 | 737 ms: 1.13x faster                                                             |
| logging_format             | 7.23 us                                                | 6.42 us: 1.13x faster                                                            |
| logging_simple             | 6.46 us                                                | 5.79 us: 1.12x faster                                                            |
| regex_compile              | 148 ms                                                 | 134 ms: 1.11x faster                                                             |
| chaos                      | 67.0 ms                                                | 60.6 ms: 1.11x faster                                                            |
| pathlib                    | 19.3 ms                                                | 17.5 ms: 1.10x faster                                                            |
| nbody                      | 97.0 ms                                                | 88.4 ms: 1.10x faster                                                            |
| tornado_http               | 103 ms                                                 | 93.8 ms: 1.09x faster                                                            |
| sympy_sum                  | 169 ms                                                 | 155 ms: 1.09x faster                                                             |
| crypto_pyaes               | 81.9 ms                                                | 75.6 ms: 1.08x faster                                                            |
| tomli_loads                | 2.33 sec                                               | 2.16 sec: 1.08x faster                                                           |
| scimark_monte_carlo        | 75.1 ms                                                | 70.0 ms: 1.07x faster                                                            |
| float                      | 84.7 ms                                                | 79.1 ms: 1.07x faster                                                            |
| generators                 | 31.2 ms                                                | 29.2 ms: 1.07x faster                                                            |
| sympy_str                  | 300 ms                                                 | 281 ms: 1.07x faster                                                             |
| deepcopy_memo              | 40.7 us                                                | 38.7 us: 1.05x faster                                                            |
| unpickle                   | 15.9 us                                                | 15.1 us: 1.05x faster                                                            |
| mako                       | 11.9 ms                                                | 11.3 ms: 1.05x faster                                                            |
| sympy_integrate            | 21.4 ms                                                | 20.4 ms: 1.05x faster                                                            |
| nqueens                    | 83.3 ms                                                | 79.6 ms: 1.05x faster                                                            |
| sqlglot_parse              | 1.36 ms                                                | 1.30 ms: 1.05x faster                                                            |
| sqlglot_transpile          | 1.68 ms                                                | 1.61 ms: 1.05x faster                                                            |
| pickle_pure_python         | 324 us                                                 | 311 us: 1.04x faster                                                             |
| unpickle_pure_python       | 230 us                                                 | 221 us: 1.04x faster                                                             |
| async_generators           | 463 ms                                                 | 445 ms: 1.04x faster                                                             |
| dulwich_log                | 68.5 ms                                                | 65.9 ms: 1.04x faster                                                            |
| fannkuch                   | 417 ms                                                 | 402 ms: 1.04x faster                                                             |
| deepcopy_reduce            | 3.35 us                                                | 3.23 us: 1.04x faster                                                            |
| spectral_norm              | 115 ms                                                 | 111 ms: 1.03x faster                                                             |
| mdp                        | 2.63 sec                                               | 2.57 sec: 1.02x faster                                                           |
| deepcopy                   | 371 us                                                 | 364 us: 1.02x faster                                                             |
| pprint_safe_repr           | 776 ms                                                 | 761 ms: 1.02x faster                                                             |
| bench_thread_pool          | 842 us                                                 | 826 us: 1.02x faster                                                             |
| coroutines                 | 23.2 ms                                                | 22.8 ms: 1.02x faster                                                            |
| scimark_fft                | 382 ms                                                 | 377 ms: 1.01x faster                                                             |
| sympy_expand               | 478 ms                                                 | 472 ms: 1.01x faster                                                             |
| hexiom                     | 6.41 ms                                                | 6.33 ms: 1.01x faster                                                            |
| 2to3                       | 274 ms                                                 | 272 ms: 1.01x faster                                                             |
| meteor_contest             | 112 ms                                                 | 111 ms: 1.01x faster                                                             |
| pprint_pformat             | 1.57 sec                                               | 1.56 sec: 1.01x faster                                                           |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                            |
| json_loads                 | 28.5 us                                                | 28.4 us: 1.00x faster                                                            |
| sqlglot_optimize           | 54.8 ms                                                | 55.2 ms: 1.01x slower                                                            |
| pickle_list                | 5.08 us                                                | 5.12 us: 1.01x slower                                                            |
| xml_etree_process          | 61.7 ms                                                | 62.3 ms: 1.01x slower                                                            |
| pickle_dict                | 35.5 us                                                | 35.9 us: 1.01x slower                                                            |
| unpickle_list              | 5.29 us                                                | 5.35 us: 1.01x slower                                                            |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                            |
| xml_etree_generate         | 89.2 ms                                                | 90.3 ms: 1.01x slower                                                            |
| pyflate                    | 482 ms                                                 | 489 ms: 1.01x slower                                                             |
| django_template            | 34.6 ms                                                | 35.1 ms: 1.01x slower                                                            |
| logging_silent             | 104 ns                                                 | 106 ns: 1.02x slower                                                             |
| docutils                   | 2.77 sec                                               | 2.81 sec: 1.02x slower                                                           |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.02x slower                                                            |
| python_startup_no_site     | 6.94 ms                                                | 7.08 ms: 1.02x slower                                                            |
| asyncio_websockets         | 551 ms                                                 | 564 ms: 1.02x slower                                                             |
| gunicorn                   | 1.24 ms                                                | 1.27 ms: 1.02x slower                                                            |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.19 ms: 1.03x slower                                                            |
| regex_effbot               | 3.61 ms                                                | 3.71 ms: 1.03x slower                                                            |
| pycparser                  | 1.18 sec                                               | 1.21 sec: 1.03x slower                                                           |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                                           |
| scimark_sor                | 129 ms                                                 | 134 ms: 1.03x slower                                                             |
| asyncio_tcp                | 491 ms                                                 | 508 ms: 1.04x slower                                                             |
| sqlite_synth               | 2.83 us                                                | 2.94 us: 1.04x slower                                                            |
| pidigits                   | 187 ms                                                 | 195 ms: 1.04x slower                                                             |
| typing_runtime_protocols   | 158 us                                                 | 165 us: 1.04x slower                                                             |
| go                         | 139 ms                                                 | 146 ms: 1.05x slower                                                             |
| gc_traversal               | 3.79 ms                                                | 3.98 ms: 1.05x slower                                                            |
| json                       | 5.26 ms                                                | 5.53 ms: 1.05x slower                                                            |
| regex_dna                  | 212 ms                                                 | 225 ms: 1.06x slower                                                             |
| richards                   | 45.8 ms                                                | 49.0 ms: 1.07x slower                                                            |
| richards_super             | 51.5 ms                                                | 55.6 ms: 1.08x slower                                                            |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| regex_v8                   | 23.1 ms                                                | 25.6 ms: 1.11x slower                                                            |
| create_gc_cycles           | 1.48 ms                                                | 1.75 ms: 1.19x slower                                                            |
| telco                      | 7.10 ms                                                | 8.52 ms: 1.20x slower                                                            |
| coverage                   | 72.7 ms                                                | 93.8 ms: 1.29x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                                     |

Benchmark hidden because not significant (7): dask, xml_etree_parse, scimark_lu, pickle, chameleon, sqlglot_normalize, xml_etree_iterparse
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240501-3.13.0a6+-dedffa7/bm-20240501-linux-x86_64-faster%2dcpython-use_attributes_to_gu-3.13.0a6+-dedffa7.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.05% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.96x