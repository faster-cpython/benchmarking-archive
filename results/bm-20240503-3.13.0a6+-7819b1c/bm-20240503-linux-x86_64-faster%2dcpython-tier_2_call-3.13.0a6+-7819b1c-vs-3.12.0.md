# Results vs. 3.12.0

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 7819b1c
- commit date: 2024-05-03
- overall geometric mean: 1.04x faster
- HPT reliability: 99.96%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 270 ms: 1.01x faster                                                    |
| chameleon      | 7.41 ms                                                | 6.96 ms: 1.06x faster                                                   |
| docutils       | 2.77 sec                                               | 2.82 sec: 1.02x slower                                                  |
| tornado_http   | 103 ms                                                 | 94.1 ms: 1.09x faster                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 334 ms: 1.35x faster                                                    |
| async_tree_none            | 472 ms                                                 | 353 ms: 1.34x faster                                                    |
| async_tree_memoization_tg  | 575 ms                                                 | 440 ms: 1.31x faster                                                    |
| async_tree_memoization     | 578 ms                                                 | 457 ms: 1.26x faster                                                    |
| async_tree_io              | 1.16 sec                                               | 923 ms: 1.25x faster                                                    |
| async_tree_io_tg           | 1.18 sec                                               | 951 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 610 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 617 ms: 1.18x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 85.7 ms: 1.13x faster                                                   |
| float          | 84.7 ms                                                | 79.2 ms: 1.07x faster                                                   |
| pidigits       | 187 ms                                                 | 190 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                  | 1.06x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 134 ms: 1.11x faster                                                    |
| regex_effbot   | 3.61 ms                                                | 3.84 ms: 1.06x slower                                                   |
| regex_dna      | 212 ms                                                 | 229 ms: 1.08x slower                                                    |
| regex_v8       | 23.1 ms                                                | 25.9 ms: 1.12x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.17 sec: 1.07x faster                                                  |
| unpickle_pure_python | 230 us                                                 | 216 us: 1.07x faster                                                    |
| pickle_pure_python   | 324 us                                                 | 305 us: 1.06x faster                                                    |
| unpickle             | 15.9 us                                                | 15.2 us: 1.05x faster                                                   |
| json_loads           | 28.5 us                                                | 27.6 us: 1.03x faster                                                   |
| unpickle_list        | 5.29 us                                                | 5.14 us: 1.03x faster                                                   |
| xml_etree_generate   | 89.2 ms                                                | 88.0 ms: 1.01x faster                                                   |
| xml_etree_parse      | 159 ms                                                 | 158 ms: 1.01x faster                                                    |
| xml_etree_process    | 61.7 ms                                                | 61.1 ms: 1.01x faster                                                   |
| xml_etree_iterparse  | 107 ms                                                 | 106 ms: 1.01x faster                                                    |
| pickle_dict          | 35.5 us                                                | 35.7 us: 1.00x slower                                                   |
| pickle               | 11.6 us                                                | 11.8 us: 1.01x slower                                                   |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                   |
| pickle_list          | 5.08 us                                                | 5.32 us: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.09 ms: 1.02x slower                                                   |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako           | 11.9 ms                                                | 10.8 ms: 1.10x faster                                                   |
| Geometric mean | (ref)                                                  | 1.05x faster                                                            |

Benchmark hidden because not significant (1): django_template

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 334 ms: 1.35x faster                                                    |
| async_tree_none            | 472 ms                                                 | 353 ms: 1.34x faster                                                    |
| comprehensions             | 21.8 us                                                | 16.5 us: 1.32x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 440 ms: 1.31x faster                                                    |
| async_tree_memoization     | 578 ms                                                 | 457 ms: 1.26x faster                                                    |
| async_tree_io              | 1.16 sec                                               | 923 ms: 1.25x faster                                                    |
| async_tree_io_tg           | 1.18 sec                                               | 951 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 610 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 617 ms: 1.18x faster                                                    |
| raytrace                   | 312 ms                                                 | 265 ms: 1.18x faster                                                    |
| deltablue                  | 3.72 ms                                                | 3.24 ms: 1.15x faster                                                   |
| logging_format             | 7.23 us                                                | 6.34 us: 1.14x faster                                                   |
| nbody                      | 97.0 ms                                                | 85.7 ms: 1.13x faster                                                   |
| mypy2                      | 830 ms                                                 | 738 ms: 1.12x faster                                                    |
| logging_simple             | 6.46 us                                                | 5.76 us: 1.12x faster                                                   |
| pathlib                    | 19.3 ms                                                | 17.4 ms: 1.11x faster                                                   |
| scimark_monte_carlo        | 75.1 ms                                                | 67.6 ms: 1.11x faster                                                   |
| regex_compile              | 148 ms                                                 | 134 ms: 1.11x faster                                                    |
| chaos                      | 67.0 ms                                                | 60.6 ms: 1.10x faster                                                   |
| crypto_pyaes               | 81.9 ms                                                | 74.1 ms: 1.10x faster                                                   |
| mako                       | 11.9 ms                                                | 10.8 ms: 1.10x faster                                                   |
| tornado_http               | 103 ms                                                 | 94.1 ms: 1.09x faster                                                   |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.08x faster                                                    |
| generators                 | 31.2 ms                                                | 29.0 ms: 1.08x faster                                                   |
| tomli_loads                | 2.33 sec                                               | 2.17 sec: 1.07x faster                                                  |
| sympy_str                  | 300 ms                                                 | 279 ms: 1.07x faster                                                    |
| float                      | 84.7 ms                                                | 79.2 ms: 1.07x faster                                                   |
| unpickle_pure_python       | 230 us                                                 | 216 us: 1.07x faster                                                    |
| fannkuch                   | 417 ms                                                 | 392 ms: 1.06x faster                                                    |
| chameleon                  | 7.41 ms                                                | 6.96 ms: 1.06x faster                                                   |
| pickle_pure_python         | 324 us                                                 | 305 us: 1.06x faster                                                    |
| deepcopy_memo              | 40.7 us                                                | 38.5 us: 1.06x faster                                                   |
| sympy_integrate            | 21.4 ms                                                | 20.4 ms: 1.05x faster                                                   |
| nqueens                    | 83.3 ms                                                | 79.3 ms: 1.05x faster                                                   |
| async_generators           | 463 ms                                                 | 442 ms: 1.05x faster                                                    |
| hexiom                     | 6.41 ms                                                | 6.12 ms: 1.05x faster                                                   |
| unpickle                   | 15.9 us                                                | 15.2 us: 1.05x faster                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.30 ms: 1.04x faster                                                   |
| sqlglot_transpile          | 1.68 ms                                                | 1.61 ms: 1.04x faster                                                   |
| deepcopy                   | 371 us                                                 | 359 us: 1.03x faster                                                    |
| json_loads                 | 28.5 us                                                | 27.6 us: 1.03x faster                                                   |
| pprint_safe_repr           | 776 ms                                                 | 753 ms: 1.03x faster                                                    |
| scimark_fft                | 382 ms                                                 | 371 ms: 1.03x faster                                                    |
| unpickle_list              | 5.29 us                                                | 5.14 us: 1.03x faster                                                   |
| logging_silent             | 104 ns                                                 | 102 ns: 1.03x faster                                                    |
| deepcopy_reduce            | 3.35 us                                                | 3.27 us: 1.02x faster                                                   |
| dulwich_log                | 68.5 ms                                                | 67.0 ms: 1.02x faster                                                   |
| pprint_pformat             | 1.57 sec                                               | 1.54 sec: 1.02x faster                                                  |
| scimark_lu                 | 118 ms                                                 | 116 ms: 1.02x faster                                                    |
| coroutines                 | 23.2 ms                                                | 22.8 ms: 1.02x faster                                                   |
| gc_traversal               | 3.79 ms                                                | 3.74 ms: 1.02x faster                                                   |
| 2to3                       | 274 ms                                                 | 270 ms: 1.01x faster                                                    |
| sympy_expand               | 478 ms                                                 | 471 ms: 1.01x faster                                                    |
| bench_thread_pool          | 842 us                                                 | 831 us: 1.01x faster                                                    |
| xml_etree_generate         | 89.2 ms                                                | 88.0 ms: 1.01x faster                                                   |
| dask                       | 372 ms                                                 | 367 ms: 1.01x faster                                                    |
| pyflate                    | 482 ms                                                 | 477 ms: 1.01x faster                                                    |
| xml_etree_parse            | 159 ms                                                 | 158 ms: 1.01x faster                                                    |
| xml_etree_process          | 61.7 ms                                                | 61.1 ms: 1.01x faster                                                   |
| meteor_contest             | 112 ms                                                 | 111 ms: 1.01x faster                                                    |
| xml_etree_iterparse        | 107 ms                                                 | 106 ms: 1.01x faster                                                    |
| sqlglot_normalize          | 110 ms                                                 | 110 ms: 1.01x faster                                                    |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.00x faster                                                   |
| pickle_dict                | 35.5 us                                                | 35.7 us: 1.00x slower                                                   |
| spectral_norm              | 115 ms                                                 | 116 ms: 1.01x slower                                                    |
| pidigits                   | 187 ms                                                 | 190 ms: 1.01x slower                                                    |
| pickle                     | 11.6 us                                                | 11.8 us: 1.01x slower                                                   |
| docutils                   | 2.77 sec                                               | 2.82 sec: 1.02x slower                                                  |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.15 ms: 1.02x slower                                                   |
| python_startup_no_site     | 6.94 ms                                                | 7.09 ms: 1.02x slower                                                   |
| asyncio_websockets         | 551 ms                                                 | 564 ms: 1.02x slower                                                    |
| pycparser                  | 1.18 sec                                               | 1.21 sec: 1.02x slower                                                  |
| aiohttp                    | 1.15 ms                                                | 1.18 ms: 1.02x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                   |
| scimark_sor                | 129 ms                                                 | 132 ms: 1.03x slower                                                    |
| gunicorn                   | 1.24 ms                                                | 1.28 ms: 1.03x slower                                                   |
| asyncio_tcp                | 491 ms                                                 | 506 ms: 1.03x slower                                                    |
| sqlite_synth               | 2.83 us                                                | 2.92 us: 1.03x slower                                                   |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                                  |
| go                         | 139 ms                                                 | 144 ms: 1.03x slower                                                    |
| richards                   | 45.8 ms                                                | 47.9 ms: 1.05x slower                                                   |
| mdp                        | 2.63 sec                                               | 2.75 sec: 1.05x slower                                                  |
| pickle_list                | 5.08 us                                                | 5.32 us: 1.05x slower                                                   |
| typing_runtime_protocols   | 158 us                                                 | 166 us: 1.05x slower                                                    |
| richards_super             | 51.5 ms                                                | 54.2 ms: 1.05x slower                                                   |
| regex_effbot               | 3.61 ms                                                | 3.84 ms: 1.06x slower                                                   |
| regex_dna                  | 212 ms                                                 | 229 ms: 1.08x slower                                                    |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                   |
| regex_v8                   | 23.1 ms                                                | 25.9 ms: 1.12x slower                                                   |
| create_gc_cycles           | 1.48 ms                                                | 1.75 ms: 1.18x slower                                                   |
| telco                      | 7.10 ms                                                | 8.55 ms: 1.20x slower                                                   |
| coverage                   | 72.7 ms                                                | 92.5 ms: 1.27x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                            |

Benchmark hidden because not significant (3): json, django_template, sqlglot_optimize
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (7) of results/bm-20240503-3.13.0a6+-7819b1c/bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-7819b1c.json: djangocms, flaskblogging, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.96% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.96x