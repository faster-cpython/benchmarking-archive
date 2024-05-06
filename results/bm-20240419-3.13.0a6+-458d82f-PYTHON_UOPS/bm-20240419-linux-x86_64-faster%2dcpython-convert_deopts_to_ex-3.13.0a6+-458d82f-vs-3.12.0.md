# Results vs. 3.12.0

- fork: faster-cpython
- ref: convert_deopts_to_ex
- machine: linux-x86_64
- commit hash: 458d82f
- commit date: 2024-04-19
- overall geometric mean: 1.07x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 305 ms: 1.11x slower                                                             |
| chameleon      | 7.41 ms                                                | 7.61 ms: 1.03x slower                                                            |
| docutils       | 2.77 sec                                               | 3.14 sec: 1.14x slower                                                           |
| Geometric mean | (ref)                                                  | 1.07x slower                                                                     |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 357 ms: 1.26x faster                                                             |
| async_tree_none            | 472 ms                                                 | 376 ms: 1.26x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 467 ms: 1.23x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 966 ms: 1.22x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 976 ms: 1.18x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 629 ms: 1.15x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 503 ms: 1.15x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 635 ms: 1.14x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.20x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                 | 192 ms: 1.02x slower                                                             |
| float          | 84.7 ms                                                | 89.2 ms: 1.05x slower                                                            |
| nbody          | 97.0 ms                                                | 122 ms: 1.26x slower                                                             |
| Geometric mean | (ref)                                                  | 1.11x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.61 ms                                                | 3.73 ms: 1.03x slower                                                            |
| regex_dna      | 212 ms                                                 | 224 ms: 1.06x slower                                                             |
| regex_v8       | 23.1 ms                                                | 25.2 ms: 1.09x slower                                                            |
| regex_compile  | 148 ms                                                 | 181 ms: 1.22x slower                                                             |
| Geometric mean | (ref)                                                  | 1.10x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_dict          | 35.5 us                                                | 32.8 us: 1.08x faster                                                            |
| pickle_list          | 5.08 us                                                | 4.83 us: 1.05x faster                                                            |
| xml_etree_parse      | 159 ms                                                 | 152 ms: 1.05x faster                                                             |
| pickle_pure_python   | 324 us                                                 | 316 us: 1.02x faster                                                             |
| json_loads           | 28.5 us                                                | 27.8 us: 1.02x faster                                                            |
| unpickle             | 15.9 us                                                | 15.6 us: 1.01x faster                                                            |
| unpickle_list        | 5.29 us                                                | 5.33 us: 1.01x slower                                                            |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                            |
| xml_etree_iterparse  | 107 ms                                                 | 111 ms: 1.04x slower                                                             |
| pickle               | 11.6 us                                                | 12.1 us: 1.04x slower                                                            |
| xml_etree_generate   | 89.2 ms                                                | 93.5 ms: 1.05x slower                                                            |
| xml_etree_process    | 61.7 ms                                                | 65.1 ms: 1.06x slower                                                            |
| tomli_loads          | 2.33 sec                                               | 2.55 sec: 1.10x slower                                                           |
| unpickle_pure_python | 230 us                                                 | 282 us: 1.23x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.02x slower                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.11 ms: 1.02x slower                                                            |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 13.6 ms: 1.14x slower                                                            |
| django_template | 34.6 ms                                                | 41.3 ms: 1.19x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.17x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 124 us: 1.28x faster                                                             |
| async_tree_none_tg         | 450 ms                                                 | 357 ms: 1.26x faster                                                             |
| async_tree_none            | 472 ms                                                 | 376 ms: 1.26x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 467 ms: 1.23x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 966 ms: 1.22x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 976 ms: 1.18x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 629 ms: 1.15x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 503 ms: 1.15x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 635 ms: 1.14x faster                                                             |
| pickle_dict                | 35.5 us                                                | 32.8 us: 1.08x faster                                                            |
| pickle_list                | 5.08 us                                                | 4.83 us: 1.05x faster                                                            |
| xml_etree_parse            | 159 ms                                                 | 152 ms: 1.05x faster                                                             |
| generators                 | 31.2 ms                                                | 29.8 ms: 1.05x faster                                                            |
| pathlib                    | 19.3 ms                                                | 18.7 ms: 1.04x faster                                                            |
| pickle_pure_python         | 324 us                                                 | 316 us: 1.02x faster                                                             |
| json_loads                 | 28.5 us                                                | 27.8 us: 1.02x faster                                                            |
| json                       | 5.26 ms                                                | 5.14 ms: 1.02x faster                                                            |
| unpickle                   | 15.9 us                                                | 15.6 us: 1.01x faster                                                            |
| gc_traversal               | 3.79 ms                                                | 3.80 ms: 1.00x slower                                                            |
| unpickle_list              | 5.29 us                                                | 5.33 us: 1.01x slower                                                            |
| async_generators           | 463 ms                                                 | 468 ms: 1.01x slower                                                             |
| logging_silent             | 104 ns                                                 | 106 ns: 1.02x slower                                                             |
| pidigits                   | 187 ms                                                 | 192 ms: 1.02x slower                                                             |
| python_startup_no_site     | 6.94 ms                                                | 7.11 ms: 1.02x slower                                                            |
| chameleon                  | 7.41 ms                                                | 7.61 ms: 1.03x slower                                                            |
| asyncio_websockets         | 551 ms                                                 | 568 ms: 1.03x slower                                                             |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                            |
| regex_effbot               | 3.61 ms                                                | 3.73 ms: 1.03x slower                                                            |
| deepcopy                   | 371 us                                                 | 384 us: 1.04x slower                                                             |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                                           |
| xml_etree_iterparse        | 107 ms                                                 | 111 ms: 1.04x slower                                                             |
| pickle                     | 11.6 us                                                | 12.1 us: 1.04x slower                                                            |
| logging_format             | 7.23 us                                                | 7.54 us: 1.04x slower                                                            |
| raytrace                   | 312 ms                                                 | 326 ms: 1.05x slower                                                             |
| dask                       | 372 ms                                                 | 389 ms: 1.05x slower                                                             |
| logging_simple             | 6.46 us                                                | 6.76 us: 1.05x slower                                                            |
| coroutines                 | 23.2 ms                                                | 24.3 ms: 1.05x slower                                                            |
| xml_etree_generate         | 89.2 ms                                                | 93.5 ms: 1.05x slower                                                            |
| bench_thread_pool          | 842 us                                                 | 886 us: 1.05x slower                                                             |
| sympy_sum                  | 169 ms                                                 | 178 ms: 1.05x slower                                                             |
| float                      | 84.7 ms                                                | 89.2 ms: 1.05x slower                                                            |
| deepcopy_memo              | 40.7 us                                                | 42.9 us: 1.05x slower                                                            |
| xml_etree_process          | 61.7 ms                                                | 65.1 ms: 1.06x slower                                                            |
| regex_dna                  | 212 ms                                                 | 224 ms: 1.06x slower                                                             |
| sqlite_synth               | 2.83 us                                                | 3.01 us: 1.06x slower                                                            |
| sqlglot_transpile          | 1.68 ms                                                | 1.81 ms: 1.07x slower                                                            |
| gunicorn                   | 1.24 ms                                                | 1.33 ms: 1.07x slower                                                            |
| pycparser                  | 1.18 sec                                               | 1.27 sec: 1.08x slower                                                           |
| mdp                        | 2.63 sec                                               | 2.84 sec: 1.08x slower                                                           |
| aiohttp                    | 1.15 ms                                                | 1.24 ms: 1.08x slower                                                            |
| sympy_str                  | 300 ms                                                 | 325 ms: 1.08x slower                                                             |
| sqlglot_parse              | 1.36 ms                                                | 1.48 ms: 1.09x slower                                                            |
| asyncio_tcp                | 491 ms                                                 | 533 ms: 1.09x slower                                                             |
| regex_v8                   | 23.1 ms                                                | 25.2 ms: 1.09x slower                                                            |
| tomli_loads                | 2.33 sec                                               | 2.55 sec: 1.10x slower                                                           |
| dulwich_log                | 68.5 ms                                                | 75.1 ms: 1.10x slower                                                            |
| comprehensions             | 21.8 us                                                | 23.9 us: 1.10x slower                                                            |
| sympy_integrate            | 21.4 ms                                                | 23.5 ms: 1.10x slower                                                            |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| meteor_contest             | 112 ms                                                 | 125 ms: 1.11x slower                                                             |
| 2to3                       | 274 ms                                                 | 305 ms: 1.11x slower                                                             |
| docutils                   | 2.77 sec                                               | 3.14 sec: 1.14x slower                                                           |
| sympy_expand               | 478 ms                                                 | 544 ms: 1.14x slower                                                             |
| sqlglot_normalize          | 110 ms                                                 | 126 ms: 1.14x slower                                                             |
| mako                       | 11.9 ms                                                | 13.6 ms: 1.14x slower                                                            |
| crypto_pyaes               | 81.9 ms                                                | 94.1 ms: 1.15x slower                                                            |
| sqlglot_optimize           | 54.8 ms                                                | 64.2 ms: 1.17x slower                                                            |
| scimark_monte_carlo        | 75.1 ms                                                | 88.3 ms: 1.18x slower                                                            |
| deltablue                  | 3.72 ms                                                | 4.37 ms: 1.18x slower                                                            |
| create_gc_cycles           | 1.48 ms                                                | 1.76 ms: 1.19x slower                                                            |
| django_template            | 34.6 ms                                                | 41.3 ms: 1.19x slower                                                            |
| scimark_fft                | 382 ms                                                 | 457 ms: 1.20x slower                                                             |
| fannkuch                   | 417 ms                                                 | 501 ms: 1.20x slower                                                             |
| chaos                      | 67.0 ms                                                | 80.9 ms: 1.21x slower                                                            |
| regex_compile              | 148 ms                                                 | 181 ms: 1.22x slower                                                             |
| richards_super             | 51.5 ms                                                | 62.9 ms: 1.22x slower                                                            |
| unpickle_pure_python       | 230 us                                                 | 282 us: 1.23x slower                                                             |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 6.20 ms: 1.23x slower                                                            |
| richards                   | 45.8 ms                                                | 56.3 ms: 1.23x slower                                                            |
| scimark_sor                | 129 ms                                                 | 159 ms: 1.24x slower                                                             |
| pyflate                    | 482 ms                                                 | 600 ms: 1.24x slower                                                             |
| spectral_norm              | 115 ms                                                 | 144 ms: 1.25x slower                                                             |
| pprint_safe_repr           | 776 ms                                                 | 974 ms: 1.26x slower                                                             |
| nbody                      | 97.0 ms                                                | 122 ms: 1.26x slower                                                             |
| telco                      | 7.10 ms                                                | 9.11 ms: 1.28x slower                                                            |
| pprint_pformat             | 1.57 sec                                               | 2.02 sec: 1.29x slower                                                           |
| nqueens                    | 83.3 ms                                                | 109 ms: 1.30x slower                                                             |
| coverage                   | 72.7 ms                                                | 97.9 ms: 1.35x slower                                                            |
| go                         | 139 ms                                                 | 191 ms: 1.37x slower                                                             |
| scimark_lu                 | 118 ms                                                 | 173 ms: 1.46x slower                                                             |
| hexiom                     | 6.41 ms                                                | 9.65 ms: 1.50x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.07x slower                                                                     |

Benchmark hidden because not significant (4): deepcopy_reduce, mypy2, tornado_http, bench_mp_pool
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240419-3.13.0a6+-458d82f-PYTHON_UOPS/bm-20240419-linux-x86_64-faster%2dcpython-convert_deopts_to_ex-3.13.0a6+-458d82f.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 0.97x