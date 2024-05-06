# Results vs. 3.12.0

- fork: faster-cpython
- ref: function_entry_enter
- machine: linux-x86_64
- commit hash: d04d9ac
- commit date: 2024-04-23
- overall geometric mean: 1.09x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 306 ms: 1.12x slower                                                             |
| chameleon      | 7.41 ms                                                | 8.10 ms: 1.09x slower                                                            |
| docutils       | 2.77 sec                                               | 3.13 sec: 1.13x slower                                                           |
| Geometric mean | (ref)                                                  | 1.09x slower                                                                     |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 356 ms: 1.26x faster                                                             |
| async_tree_none            | 472 ms                                                 | 380 ms: 1.24x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 467 ms: 1.23x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 971 ms: 1.22x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 975 ms: 1.19x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 626 ms: 1.16x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 638 ms: 1.14x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 508 ms: 1.14x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.20x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                 | 199 ms: 1.06x slower                                                             |
| float          | 84.7 ms                                                | 94.9 ms: 1.12x slower                                                            |
| nbody          | 97.0 ms                                                | 128 ms: 1.32x slower                                                             |
| Geometric mean | (ref)                                                  | 1.16x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.61 ms                                                | 3.69 ms: 1.02x slower                                                            |
| regex_dna      | 212 ms                                                 | 227 ms: 1.07x slower                                                             |
| regex_v8       | 23.1 ms                                                | 25.5 ms: 1.10x slower                                                            |
| regex_compile  | 148 ms                                                 | 186 ms: 1.26x slower                                                             |
| Geometric mean | (ref)                                                  | 1.11x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_parse      | 159 ms                                                 | 150 ms: 1.06x faster                                                             |
| unpickle             | 15.9 us                                                | 15.3 us: 1.04x faster                                                            |
| json_loads           | 28.5 us                                                | 27.8 us: 1.03x faster                                                            |
| pickle_pure_python   | 324 us                                                 | 321 us: 1.01x faster                                                             |
| pickle_dict          | 35.5 us                                                | 35.5 us: 1.00x faster                                                            |
| unpickle_list        | 5.29 us                                                | 5.35 us: 1.01x slower                                                            |
| pickle               | 11.6 us                                                | 11.9 us: 1.02x slower                                                            |
| json_dumps           | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                            |
| xml_etree_process    | 61.7 ms                                                | 65.6 ms: 1.06x slower                                                            |
| xml_etree_generate   | 89.2 ms                                                | 95.3 ms: 1.07x slower                                                            |
| xml_etree_iterparse  | 107 ms                                                 | 114 ms: 1.07x slower                                                             |
| tomli_loads          | 2.33 sec                                               | 2.62 sec: 1.12x slower                                                           |
| unpickle_pure_python | 230 us                                                 | 298 us: 1.30x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                                     |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.14 ms: 1.03x slower                                                            |
| python_startup         | 9.55 ms                                                | 10.6 ms: 1.11x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| django_template | 34.6 ms                                                | 41.5 ms: 1.20x slower                                                            |
| mako            | 11.9 ms                                                | 14.5 ms: 1.22x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.21x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 356 ms: 1.26x faster                                                             |
| async_tree_none            | 472 ms                                                 | 380 ms: 1.24x faster                                                             |
| typing_runtime_protocols   | 158 us                                                 | 128 us: 1.24x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 467 ms: 1.23x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 971 ms: 1.22x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 975 ms: 1.19x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 626 ms: 1.16x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 638 ms: 1.14x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 508 ms: 1.14x faster                                                             |
| xml_etree_parse            | 159 ms                                                 | 150 ms: 1.06x faster                                                             |
| pathlib                    | 19.3 ms                                                | 18.4 ms: 1.05x faster                                                            |
| unpickle                   | 15.9 us                                                | 15.3 us: 1.04x faster                                                            |
| generators                 | 31.2 ms                                                | 30.3 ms: 1.03x faster                                                            |
| json_loads                 | 28.5 us                                                | 27.8 us: 1.03x faster                                                            |
| json                       | 5.26 ms                                                | 5.20 ms: 1.01x faster                                                            |
| logging_format             | 7.23 us                                                | 7.16 us: 1.01x faster                                                            |
| pickle_pure_python         | 324 us                                                 | 321 us: 1.01x faster                                                             |
| pickle_dict                | 35.5 us                                                | 35.5 us: 1.00x faster                                                            |
| unpickle_list              | 5.29 us                                                | 5.35 us: 1.01x slower                                                            |
| regex_effbot               | 3.61 ms                                                | 3.69 ms: 1.02x slower                                                            |
| pickle                     | 11.6 us                                                | 11.9 us: 1.02x slower                                                            |
| asyncio_websockets         | 551 ms                                                 | 567 ms: 1.03x slower                                                             |
| python_startup_no_site     | 6.94 ms                                                | 7.14 ms: 1.03x slower                                                            |
| dask                       | 372 ms                                                 | 384 ms: 1.03x slower                                                             |
| deepcopy                   | 371 us                                                 | 384 us: 1.04x slower                                                             |
| json_dumps                 | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                            |
| async_generators           | 463 ms                                                 | 482 ms: 1.04x slower                                                             |
| gc_traversal               | 3.79 ms                                                | 3.96 ms: 1.04x slower                                                            |
| coroutines                 | 23.2 ms                                                | 24.2 ms: 1.05x slower                                                            |
| logging_silent             | 104 ns                                                 | 110 ns: 1.05x slower                                                             |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.88 sec: 1.05x slower                                                           |
| sympy_sum                  | 169 ms                                                 | 178 ms: 1.05x slower                                                             |
| raytrace                   | 312 ms                                                 | 330 ms: 1.06x slower                                                             |
| bench_thread_pool          | 842 us                                                 | 892 us: 1.06x slower                                                             |
| sqlite_synth               | 2.83 us                                                | 3.01 us: 1.06x slower                                                            |
| xml_etree_process          | 61.7 ms                                                | 65.6 ms: 1.06x slower                                                            |
| pidigits                   | 187 ms                                                 | 199 ms: 1.06x slower                                                             |
| gunicorn                   | 1.24 ms                                                | 1.32 ms: 1.07x slower                                                            |
| xml_etree_generate         | 89.2 ms                                                | 95.3 ms: 1.07x slower                                                            |
| xml_etree_iterparse        | 107 ms                                                 | 114 ms: 1.07x slower                                                             |
| regex_dna                  | 212 ms                                                 | 227 ms: 1.07x slower                                                             |
| aiohttp                    | 1.15 ms                                                | 1.23 ms: 1.07x slower                                                            |
| asyncio_tcp                | 491 ms                                                 | 528 ms: 1.08x slower                                                             |
| dulwich_log                | 68.5 ms                                                | 73.9 ms: 1.08x slower                                                            |
| sqlglot_transpile          | 1.68 ms                                                | 1.82 ms: 1.08x slower                                                            |
| meteor_contest             | 112 ms                                                 | 122 ms: 1.09x slower                                                             |
| chameleon                  | 7.41 ms                                                | 8.10 ms: 1.09x slower                                                            |
| pycparser                  | 1.18 sec                                               | 1.29 sec: 1.09x slower                                                           |
| sympy_str                  | 300 ms                                                 | 330 ms: 1.10x slower                                                             |
| regex_v8                   | 23.1 ms                                                | 25.5 ms: 1.10x slower                                                            |
| sqlglot_parse              | 1.36 ms                                                | 1.50 ms: 1.10x slower                                                            |
| python_startup             | 9.55 ms                                                | 10.6 ms: 1.11x slower                                                            |
| 2to3                       | 274 ms                                                 | 306 ms: 1.12x slower                                                             |
| float                      | 84.7 ms                                                | 94.9 ms: 1.12x slower                                                            |
| tomli_loads                | 2.33 sec                                               | 2.62 sec: 1.12x slower                                                           |
| sympy_integrate            | 21.4 ms                                                | 24.1 ms: 1.13x slower                                                            |
| docutils                   | 2.77 sec                                               | 3.13 sec: 1.13x slower                                                           |
| comprehensions             | 21.8 us                                                | 24.6 us: 1.13x slower                                                            |
| deepcopy_memo              | 40.7 us                                                | 46.1 us: 1.13x slower                                                            |
| sqlglot_normalize          | 110 ms                                                 | 126 ms: 1.14x slower                                                             |
| mdp                        | 2.63 sec                                               | 3.02 sec: 1.15x slower                                                           |
| sympy_expand               | 478 ms                                                 | 552 ms: 1.16x slower                                                             |
| crypto_pyaes               | 81.9 ms                                                | 95.3 ms: 1.16x slower                                                            |
| deltablue                  | 3.72 ms                                                | 4.33 ms: 1.17x slower                                                            |
| sqlglot_optimize           | 54.8 ms                                                | 64.5 ms: 1.18x slower                                                            |
| django_template            | 34.6 ms                                                | 41.5 ms: 1.20x slower                                                            |
| chaos                      | 67.0 ms                                                | 80.9 ms: 1.21x slower                                                            |
| create_gc_cycles           | 1.48 ms                                                | 1.79 ms: 1.21x slower                                                            |
| mako                       | 11.9 ms                                                | 14.5 ms: 1.22x slower                                                            |
| fannkuch                   | 417 ms                                                 | 511 ms: 1.22x slower                                                             |
| richards_super             | 51.5 ms                                                | 63.7 ms: 1.24x slower                                                            |
| scimark_fft                | 382 ms                                                 | 473 ms: 1.24x slower                                                             |
| scimark_sor                | 129 ms                                                 | 161 ms: 1.25x slower                                                             |
| richards                   | 45.8 ms                                                | 57.3 ms: 1.25x slower                                                            |
| scimark_monte_carlo        | 75.1 ms                                                | 93.9 ms: 1.25x slower                                                            |
| regex_compile              | 148 ms                                                 | 186 ms: 1.26x slower                                                             |
| pprint_safe_repr           | 776 ms                                                 | 983 ms: 1.27x slower                                                             |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 6.54 ms: 1.29x slower                                                            |
| unpickle_pure_python       | 230 us                                                 | 298 us: 1.30x slower                                                             |
| pprint_pformat             | 1.57 sec                                               | 2.04 sec: 1.30x slower                                                           |
| telco                      | 7.10 ms                                                | 9.36 ms: 1.32x slower                                                            |
| nbody                      | 97.0 ms                                                | 128 ms: 1.32x slower                                                             |
| pyflate                    | 482 ms                                                 | 639 ms: 1.33x slower                                                             |
| spectral_norm              | 115 ms                                                 | 153 ms: 1.33x slower                                                             |
| nqueens                    | 83.3 ms                                                | 111 ms: 1.34x slower                                                             |
| coverage                   | 72.7 ms                                                | 97.4 ms: 1.34x slower                                                            |
| go                         | 139 ms                                                 | 201 ms: 1.44x slower                                                             |
| scimark_lu                 | 118 ms                                                 | 170 ms: 1.44x slower                                                             |
| hexiom                     | 6.41 ms                                                | 10.1 ms: 1.57x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                                     |

Benchmark hidden because not significant (6): mypy2, logging_simple, pickle_list, deepcopy_reduce, bench_mp_pool, tornado_http
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240423-3.13.0a6+-d04d9ac-PYTHON_UOPS/bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-d04d9ac.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 0.98x