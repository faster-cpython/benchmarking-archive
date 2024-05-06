# Results vs. 3.12.0

- fork: faster-cpython
- ref: function_entry_enter
- machine: linux-x86_64
- commit hash: 6ccc646
- commit date: 2024-04-23
- overall geometric mean: 1.25x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.14x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 352 ms: 1.28x slower                                                             |
| chameleon      | 7.41 ms                                                | 10.0 ms: 1.35x slower                                                            |
| docutils       | 2.77 sec                                               | 3.61 sec: 1.31x slower                                                           |
| tornado_http   | 103 ms                                                 | 136 ms: 1.32x slower                                                             |
| Geometric mean | (ref)                                                  | 1.32x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 429 ms: 1.05x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 1.14 sec: 1.04x faster                                                           |
| async_tree_io              | 1.16 sec                                               | 1.11 sec: 1.04x faster                                                           |
| async_tree_none            | 472 ms                                                 | 457 ms: 1.03x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 714 ms: 1.02x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 608 ms: 1.05x slower                                                             |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                                     |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                 | 194 ms: 1.03x slower                                                             |
| float          | 84.7 ms                                                | 94.3 ms: 1.11x slower                                                            |
| nbody          | 97.0 ms                                                | 122 ms: 1.26x slower                                                             |
| Geometric mean | (ref)                                                  | 1.13x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.61 ms                                                | 3.72 ms: 1.03x slower                                                            |
| regex_dna      | 212 ms                                                 | 227 ms: 1.07x slower                                                             |
| regex_v8       | 23.1 ms                                                | 25.6 ms: 1.11x slower                                                            |
| regex_compile  | 148 ms                                                 | 231 ms: 1.56x slower                                                             |
| Geometric mean | (ref)                                                  | 1.17x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_parse      | 159 ms                                                 | 155 ms: 1.03x faster                                                             |
| pickle_dict          | 35.5 us                                                | 35.4 us: 1.00x faster                                                            |
| pickle_list          | 5.08 us                                                | 5.17 us: 1.02x slower                                                            |
| unpickle_list        | 5.29 us                                                | 5.42 us: 1.02x slower                                                            |
| pickle               | 11.6 us                                                | 12.0 us: 1.04x slower                                                            |
| xml_etree_iterparse  | 107 ms                                                 | 112 ms: 1.05x slower                                                             |
| json_dumps           | 10.4 ms                                                | 12.7 ms: 1.22x slower                                                            |
| xml_etree_generate   | 89.2 ms                                                | 111 ms: 1.24x slower                                                             |
| tomli_loads          | 2.33 sec                                               | 2.99 sec: 1.28x slower                                                           |
| xml_etree_process    | 61.7 ms                                                | 81.4 ms: 1.32x slower                                                            |
| unpickle_pure_python | 230 us                                                 | 337 us: 1.47x slower                                                             |
| pickle_pure_python   | 324 us                                                 | 500 us: 1.54x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.14x slower                                                                     |

Benchmark hidden because not significant (2): unpickle, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.18 ms: 1.03x slower                                                            |
| python_startup         | 9.55 ms                                                | 10.7 ms: 1.12x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 13.8 ms: 1.16x slower                                                            |
| django_template | 34.6 ms                                                | 60.9 ms: 1.76x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.43x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 429 ms: 1.05x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 1.14 sec: 1.04x faster                                                           |
| async_tree_io              | 1.16 sec                                               | 1.11 sec: 1.04x faster                                                           |
| async_tree_none            | 472 ms                                                 | 457 ms: 1.03x faster                                                             |
| xml_etree_parse            | 159 ms                                                 | 155 ms: 1.03x faster                                                             |
| typing_runtime_protocols   | 158 us                                                 | 154 us: 1.02x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 714 ms: 1.02x faster                                                             |
| pickle_dict                | 35.5 us                                                | 35.4 us: 1.00x faster                                                            |
| generators                 | 31.2 ms                                                | 31.7 ms: 1.01x slower                                                            |
| pickle_list                | 5.08 us                                                | 5.17 us: 1.02x slower                                                            |
| unpickle_list              | 5.29 us                                                | 5.42 us: 1.02x slower                                                            |
| regex_effbot               | 3.61 ms                                                | 3.72 ms: 1.03x slower                                                            |
| json                       | 5.26 ms                                                | 5.42 ms: 1.03x slower                                                            |
| pidigits                   | 187 ms                                                 | 194 ms: 1.03x slower                                                             |
| python_startup_no_site     | 6.94 ms                                                | 7.18 ms: 1.03x slower                                                            |
| asyncio_websockets         | 551 ms                                                 | 571 ms: 1.04x slower                                                             |
| pickle                     | 11.6 us                                                | 12.0 us: 1.04x slower                                                            |
| bench_mp_pool              | 24.0 ms                                                | 25.0 ms: 1.04x slower                                                            |
| xml_etree_iterparse        | 107 ms                                                 | 112 ms: 1.05x slower                                                             |
| async_tree_memoization     | 578 ms                                                 | 608 ms: 1.05x slower                                                             |
| gc_traversal               | 3.79 ms                                                | 4.03 ms: 1.06x slower                                                            |
| regex_dna                  | 212 ms                                                 | 227 ms: 1.07x slower                                                             |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.91 sec: 1.07x slower                                                           |
| pathlib                    | 19.3 ms                                                | 20.8 ms: 1.08x slower                                                            |
| async_generators           | 463 ms                                                 | 504 ms: 1.09x slower                                                             |
| meteor_contest             | 112 ms                                                 | 123 ms: 1.10x slower                                                             |
| coroutines                 | 23.2 ms                                                | 25.5 ms: 1.10x slower                                                            |
| regex_v8                   | 23.1 ms                                                | 25.6 ms: 1.11x slower                                                            |
| float                      | 84.7 ms                                                | 94.3 ms: 1.11x slower                                                            |
| python_startup             | 9.55 ms                                                | 10.7 ms: 1.12x slower                                                            |
| sqlite_synth               | 2.83 us                                                | 3.16 us: 1.12x slower                                                            |
| mdp                        | 2.63 sec                                               | 2.99 sec: 1.14x slower                                                           |
| crypto_pyaes               | 81.9 ms                                                | 93.4 ms: 1.14x slower                                                            |
| comprehensions             | 21.8 us                                                | 25.2 us: 1.16x slower                                                            |
| mako                       | 11.9 ms                                                | 13.8 ms: 1.16x slower                                                            |
| asyncio_tcp                | 491 ms                                                 | 569 ms: 1.16x slower                                                             |
| bench_thread_pool          | 842 us                                                 | 998 us: 1.19x slower                                                             |
| mypy2                      | 830 ms                                                 | 994 ms: 1.20x slower                                                             |
| scimark_fft                | 382 ms                                                 | 458 ms: 1.20x slower                                                             |
| fannkuch                   | 417 ms                                                 | 505 ms: 1.21x slower                                                             |
| create_gc_cycles           | 1.48 ms                                                | 1.80 ms: 1.22x slower                                                            |
| json_dumps                 | 10.4 ms                                                | 12.7 ms: 1.22x slower                                                            |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 6.19 ms: 1.22x slower                                                            |
| scimark_monte_carlo        | 75.1 ms                                                | 93.1 ms: 1.24x slower                                                            |
| xml_etree_generate         | 89.2 ms                                                | 111 ms: 1.24x slower                                                             |
| spectral_norm              | 115 ms                                                 | 144 ms: 1.25x slower                                                             |
| nbody                      | 97.0 ms                                                | 122 ms: 1.26x slower                                                             |
| sympy_sum                  | 169 ms                                                 | 216 ms: 1.28x slower                                                             |
| tomli_loads                | 2.33 sec                                               | 2.99 sec: 1.28x slower                                                           |
| 2to3                       | 274 ms                                                 | 352 ms: 1.28x slower                                                             |
| dask                       | 372 ms                                                 | 481 ms: 1.29x slower                                                             |
| gunicorn                   | 1.24 ms                                                | 1.61 ms: 1.30x slower                                                            |
| aiohttp                    | 1.15 ms                                                | 1.50 ms: 1.30x slower                                                            |
| docutils                   | 2.77 sec                                               | 3.61 sec: 1.31x slower                                                           |
| xml_etree_process          | 61.7 ms                                                | 81.4 ms: 1.32x slower                                                            |
| sympy_integrate            | 21.4 ms                                                | 28.3 ms: 1.32x slower                                                            |
| tornado_http               | 103 ms                                                 | 136 ms: 1.32x slower                                                             |
| sympy_str                  | 300 ms                                                 | 403 ms: 1.35x slower                                                             |
| deepcopy_memo              | 40.7 us                                                | 55.0 us: 1.35x slower                                                            |
| pyflate                    | 482 ms                                                 | 652 ms: 1.35x slower                                                             |
| chameleon                  | 7.41 ms                                                | 10.0 ms: 1.35x slower                                                            |
| coverage                   | 72.7 ms                                                | 98.5 ms: 1.35x slower                                                            |
| telco                      | 7.10 ms                                                | 9.65 ms: 1.36x slower                                                            |
| dulwich_log                | 68.5 ms                                                | 93.7 ms: 1.37x slower                                                            |
| pycparser                  | 1.18 sec                                               | 1.61 sec: 1.37x slower                                                           |
| logging_silent             | 104 ns                                                 | 147 ns: 1.41x slower                                                             |
| sympy_expand               | 478 ms                                                 | 679 ms: 1.42x slower                                                             |
| unpickle_pure_python       | 230 us                                                 | 337 us: 1.47x slower                                                             |
| sqlglot_optimize           | 54.8 ms                                                | 81.2 ms: 1.48x slower                                                            |
| deepcopy                   | 371 us                                                 | 553 us: 1.49x slower                                                             |
| sqlglot_transpile          | 1.68 ms                                                | 2.52 ms: 1.49x slower                                                            |
| sqlglot_parse              | 1.36 ms                                                | 2.04 ms: 1.50x slower                                                            |
| sqlglot_normalize          | 110 ms                                                 | 166 ms: 1.51x slower                                                             |
| raytrace                   | 312 ms                                                 | 474 ms: 1.52x slower                                                             |
| deepcopy_reduce            | 3.35 us                                                | 5.09 us: 1.52x slower                                                            |
| chaos                      | 67.0 ms                                                | 103 ms: 1.54x slower                                                             |
| scimark_sor                | 129 ms                                                 | 199 ms: 1.54x slower                                                             |
| pickle_pure_python         | 324 us                                                 | 500 us: 1.54x slower                                                             |
| regex_compile              | 148 ms                                                 | 231 ms: 1.56x slower                                                             |
| pprint_safe_repr           | 776 ms                                                 | 1.24 sec: 1.60x slower                                                           |
| scimark_lu                 | 118 ms                                                 | 190 ms: 1.61x slower                                                             |
| logging_format             | 7.23 us                                                | 11.7 us: 1.61x slower                                                            |
| logging_simple             | 6.46 us                                                | 10.5 us: 1.63x slower                                                            |
| richards_super             | 51.5 ms                                                | 84.5 ms: 1.64x slower                                                            |
| pprint_pformat             | 1.57 sec                                               | 2.58 sec: 1.64x slower                                                           |
| go                         | 139 ms                                                 | 230 ms: 1.65x slower                                                             |
| richards                   | 45.8 ms                                                | 76.0 ms: 1.66x slower                                                            |
| nqueens                    | 83.3 ms                                                | 139 ms: 1.67x slower                                                             |
| hexiom                     | 6.41 ms                                                | 10.8 ms: 1.69x slower                                                            |
| deltablue                  | 3.72 ms                                                | 6.30 ms: 1.70x slower                                                            |
| django_template            | 34.6 ms                                                | 60.9 ms: 1.76x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.25x slower                                                                     |

Benchmark hidden because not significant (4): async_tree_memoization_tg, unpickle, json_loads, async_tree_cpu_io_mixed
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240423-3.13.0a6+-6ccc646-PYTHON_UOPS/bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-6ccc646.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.19x
- 95% likely to have a slowdown of 1.17x
- 99% likely to have a slowdown of 1.14x

# Memory
- memory change: 0.98x