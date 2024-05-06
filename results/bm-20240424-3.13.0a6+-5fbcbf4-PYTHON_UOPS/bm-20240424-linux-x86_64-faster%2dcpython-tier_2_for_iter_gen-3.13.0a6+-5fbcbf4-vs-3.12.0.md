# Results vs. 3.12.0

- fork: faster-cpython
- ref: tier_2_for_iter_gen
- machine: linux-x86_64
- commit hash: 5fbcbf4
- commit date: 2024-04-24
- overall geometric mean: 1.06x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 302 ms: 1.10x slower                                                            |
| chameleon      | 7.41 ms                                                | 7.46 ms: 1.01x slower                                                           |
| docutils       | 2.77 sec                                               | 3.07 sec: 1.11x slower                                                          |
| tornado_http   | 103 ms                                                 | 101 ms: 1.01x faster                                                            |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                    |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 350 ms: 1.28x faster                                                            |
| async_tree_none            | 472 ms                                                 | 373 ms: 1.27x faster                                                            |
| async_tree_memoization_tg  | 575 ms                                                 | 461 ms: 1.25x faster                                                            |
| async_tree_io_tg           | 1.18 sec                                               | 962 ms: 1.23x faster                                                            |
| async_tree_io              | 1.16 sec                                               | 972 ms: 1.19x faster                                                            |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 626 ms: 1.16x faster                                                            |
| async_tree_memoization     | 578 ms                                                 | 500 ms: 1.16x faster                                                            |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 636 ms: 1.14x faster                                                            |
| Geometric mean             | (ref)                                                  | 1.21x faster                                                                    |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                 | 195 ms: 1.04x slower                                                            |
| float          | 84.7 ms                                                | 88.4 ms: 1.04x slower                                                           |
| nbody          | 97.0 ms                                                | 122 ms: 1.26x slower                                                            |
| Geometric mean | (ref)                                                  | 1.11x slower                                                                    |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| regex_effbot   | 3.61 ms                                                | 3.64 ms: 1.01x slower                                                           |
| regex_dna      | 212 ms                                                 | 227 ms: 1.07x slower                                                            |
| regex_v8       | 23.1 ms                                                | 25.4 ms: 1.10x slower                                                           |
| regex_compile  | 148 ms                                                 | 178 ms: 1.20x slower                                                            |
| Geometric mean | (ref)                                                  | 1.09x slower                                                                    |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| xml_etree_parse      | 159 ms                                                 | 153 ms: 1.04x faster                                                            |
| json_loads           | 28.5 us                                                | 27.6 us: 1.03x faster                                                           |
| pickle_pure_python   | 324 us                                                 | 314 us: 1.03x faster                                                            |
| unpickle_list        | 5.29 us                                                | 5.15 us: 1.03x faster                                                           |
| pickle_list          | 5.08 us                                                | 5.03 us: 1.01x faster                                                           |
| pickle_dict          | 35.5 us                                                | 35.4 us: 1.00x faster                                                           |
| pickle               | 11.6 us                                                | 11.8 us: 1.02x slower                                                           |
| json_dumps           | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                           |
| xml_etree_iterparse  | 107 ms                                                 | 111 ms: 1.04x slower                                                            |
| xml_etree_process    | 61.7 ms                                                | 64.4 ms: 1.04x slower                                                           |
| xml_etree_generate   | 89.2 ms                                                | 93.3 ms: 1.05x slower                                                           |
| unpickle             | 15.9 us                                                | 16.7 us: 1.05x slower                                                           |
| tomli_loads          | 2.33 sec                                               | 2.49 sec: 1.07x slower                                                          |
| unpickle_pure_python | 230 us                                                 | 281 us: 1.22x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.03x slower                                                                    |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.13 ms: 1.03x slower                                                           |
| python_startup         | 9.55 ms                                                | 10.6 ms: 1.11x slower                                                           |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                                    |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 13.1 ms: 1.10x slower                                                           |
| django_template | 34.6 ms                                                | 39.5 ms: 1.14x slower                                                           |
| Geometric mean  | (ref)                                                  | 1.12x slower                                                                    |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 350 ms: 1.28x faster                                                            |
| typing_runtime_protocols   | 158 us                                                 | 123 us: 1.28x faster                                                            |
| async_tree_none            | 472 ms                                                 | 373 ms: 1.27x faster                                                            |
| async_tree_memoization_tg  | 575 ms                                                 | 461 ms: 1.25x faster                                                            |
| async_tree_io_tg           | 1.18 sec                                               | 962 ms: 1.23x faster                                                            |
| async_tree_io              | 1.16 sec                                               | 972 ms: 1.19x faster                                                            |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 626 ms: 1.16x faster                                                            |
| async_tree_memoization     | 578 ms                                                 | 500 ms: 1.16x faster                                                            |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 636 ms: 1.14x faster                                                            |
| pathlib                    | 19.3 ms                                                | 18.3 ms: 1.06x faster                                                           |
| xml_etree_parse            | 159 ms                                                 | 153 ms: 1.04x faster                                                            |
| json_loads                 | 28.5 us                                                | 27.6 us: 1.03x faster                                                           |
| pickle_pure_python         | 324 us                                                 | 314 us: 1.03x faster                                                            |
| unpickle_list              | 5.29 us                                                | 5.15 us: 1.03x faster                                                           |
| coroutines                 | 23.2 ms                                                | 22.6 ms: 1.03x faster                                                           |
| gc_traversal               | 3.79 ms                                                | 3.72 ms: 1.02x faster                                                           |
| logging_simple             | 6.46 us                                                | 6.36 us: 1.02x faster                                                           |
| tornado_http               | 103 ms                                                 | 101 ms: 1.01x faster                                                            |
| generators                 | 31.2 ms                                                | 30.8 ms: 1.01x faster                                                           |
| logging_format             | 7.23 us                                                | 7.15 us: 1.01x faster                                                           |
| pickle_list                | 5.08 us                                                | 5.03 us: 1.01x faster                                                           |
| deepcopy_reduce            | 3.35 us                                                | 3.32 us: 1.01x faster                                                           |
| pickle_dict                | 35.5 us                                                | 35.4 us: 1.00x faster                                                           |
| chameleon                  | 7.41 ms                                                | 7.46 ms: 1.01x slower                                                           |
| regex_effbot               | 3.61 ms                                                | 3.64 ms: 1.01x slower                                                           |
| deepcopy                   | 371 us                                                 | 376 us: 1.01x slower                                                            |
| pickle                     | 11.6 us                                                | 11.8 us: 1.02x slower                                                           |
| async_generators           | 463 ms                                                 | 473 ms: 1.02x slower                                                            |
| raytrace                   | 312 ms                                                 | 319 ms: 1.02x slower                                                            |
| dask                       | 372 ms                                                 | 381 ms: 1.02x slower                                                            |
| python_startup_no_site     | 6.94 ms                                                | 7.13 ms: 1.03x slower                                                           |
| asyncio_websockets         | 551 ms                                                 | 567 ms: 1.03x slower                                                            |
| comprehensions             | 21.8 us                                                | 22.6 us: 1.04x slower                                                           |
| json_dumps                 | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                           |
| pidigits                   | 187 ms                                                 | 195 ms: 1.04x slower                                                            |
| xml_etree_iterparse        | 107 ms                                                 | 111 ms: 1.04x slower                                                            |
| float                      | 84.7 ms                                                | 88.4 ms: 1.04x slower                                                           |
| xml_etree_process          | 61.7 ms                                                | 64.4 ms: 1.04x slower                                                           |
| sympy_sum                  | 169 ms                                                 | 177 ms: 1.05x slower                                                            |
| xml_etree_generate         | 89.2 ms                                                | 93.3 ms: 1.05x slower                                                           |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.87 sec: 1.05x slower                                                          |
| asyncio_tcp                | 491 ms                                                 | 515 ms: 1.05x slower                                                            |
| unpickle                   | 15.9 us                                                | 16.7 us: 1.05x slower                                                           |
| sqlite_synth               | 2.83 us                                                | 3.00 us: 1.06x slower                                                           |
| bench_thread_pool          | 842 us                                                 | 893 us: 1.06x slower                                                            |
| deepcopy_memo              | 40.7 us                                                | 43.2 us: 1.06x slower                                                           |
| meteor_contest             | 112 ms                                                 | 120 ms: 1.07x slower                                                            |
| tomli_loads                | 2.33 sec                                               | 2.49 sec: 1.07x slower                                                          |
| sqlglot_transpile          | 1.68 ms                                                | 1.80 ms: 1.07x slower                                                           |
| gunicorn                   | 1.24 ms                                                | 1.33 ms: 1.07x slower                                                           |
| regex_dna                  | 212 ms                                                 | 227 ms: 1.07x slower                                                            |
| mdp                        | 2.63 sec                                               | 2.83 sec: 1.07x slower                                                          |
| sympy_str                  | 300 ms                                                 | 322 ms: 1.07x slower                                                            |
| dulwich_log                | 68.5 ms                                                | 73.6 ms: 1.07x slower                                                           |
| pycparser                  | 1.18 sec                                               | 1.27 sec: 1.08x slower                                                          |
| sympy_integrate            | 21.4 ms                                                | 23.0 ms: 1.08x slower                                                           |
| aiohttp                    | 1.15 ms                                                | 1.24 ms: 1.08x slower                                                           |
| sqlglot_parse              | 1.36 ms                                                | 1.47 ms: 1.08x slower                                                           |
| crypto_pyaes               | 81.9 ms                                                | 89.8 ms: 1.10x slower                                                           |
| regex_v8                   | 23.1 ms                                                | 25.4 ms: 1.10x slower                                                           |
| 2to3                       | 274 ms                                                 | 302 ms: 1.10x slower                                                            |
| mako                       | 11.9 ms                                                | 13.1 ms: 1.10x slower                                                           |
| python_startup             | 9.55 ms                                                | 10.6 ms: 1.11x slower                                                           |
| docutils                   | 2.77 sec                                               | 3.07 sec: 1.11x slower                                                          |
| deltablue                  | 3.72 ms                                                | 4.14 ms: 1.11x slower                                                           |
| sympy_expand               | 478 ms                                                 | 534 ms: 1.12x slower                                                            |
| sqlglot_normalize          | 110 ms                                                 | 123 ms: 1.12x slower                                                            |
| scimark_sor                | 129 ms                                                 | 147 ms: 1.14x slower                                                            |
| django_template            | 34.6 ms                                                | 39.5 ms: 1.14x slower                                                           |
| sqlglot_optimize           | 54.8 ms                                                | 63.3 ms: 1.15x slower                                                           |
| fannkuch                   | 417 ms                                                 | 483 ms: 1.16x slower                                                            |
| scimark_fft                | 382 ms                                                 | 443 ms: 1.16x slower                                                            |
| scimark_monte_carlo        | 75.1 ms                                                | 87.4 ms: 1.16x slower                                                           |
| chaos                      | 67.0 ms                                                | 78.9 ms: 1.18x slower                                                           |
| pyflate                    | 482 ms                                                 | 571 ms: 1.18x slower                                                            |
| create_gc_cycles           | 1.48 ms                                                | 1.77 ms: 1.20x slower                                                           |
| regex_compile              | 148 ms                                                 | 178 ms: 1.20x slower                                                            |
| richards_super             | 51.5 ms                                                | 62.0 ms: 1.20x slower                                                           |
| richards                   | 45.8 ms                                                | 55.3 ms: 1.21x slower                                                           |
| spectral_norm              | 115 ms                                                 | 140 ms: 1.22x slower                                                            |
| pprint_safe_repr           | 776 ms                                                 | 944 ms: 1.22x slower                                                            |
| unpickle_pure_python       | 230 us                                                 | 281 us: 1.22x slower                                                            |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 6.21 ms: 1.23x slower                                                           |
| pprint_pformat             | 1.57 sec                                               | 1.97 sec: 1.26x slower                                                          |
| nbody                      | 97.0 ms                                                | 122 ms: 1.26x slower                                                            |
| nqueens                    | 83.3 ms                                                | 106 ms: 1.28x slower                                                            |
| telco                      | 7.10 ms                                                | 9.15 ms: 1.29x slower                                                           |
| go                         | 139 ms                                                 | 184 ms: 1.32x slower                                                            |
| coverage                   | 72.7 ms                                                | 99.0 ms: 1.36x slower                                                           |
| scimark_lu                 | 118 ms                                                 | 163 ms: 1.38x slower                                                            |
| hexiom                     | 6.41 ms                                                | 9.27 ms: 1.45x slower                                                           |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                                    |

Benchmark hidden because not significant (4): mypy2, json, bench_mp_pool, logging_silent
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240424-3.13.0a6+-5fbcbf4-PYTHON_UOPS/bm-20240424-linux-x86_64-faster%2dcpython-tier_2_for_iter_gen-3.13.0a6+-5fbcbf4.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 0.97x