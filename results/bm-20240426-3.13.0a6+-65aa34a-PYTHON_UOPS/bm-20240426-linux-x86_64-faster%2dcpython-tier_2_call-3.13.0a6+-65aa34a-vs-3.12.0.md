# Results vs. 3.12.0

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.09x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 305 ms: 1.11x slower                                                    |
| chameleon      | 7.41 ms                                                | 7.57 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x slower                                                            |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 347 ms: 1.30x faster                                                    |
| async_tree_none            | 472 ms                                                 | 372 ms: 1.27x faster                                                    |
| async_tree_memoization_tg  | 575 ms                                                 | 459 ms: 1.25x faster                                                    |
| async_tree_io_tg           | 1.18 sec                                               | 964 ms: 1.23x faster                                                    |
| async_tree_io              | 1.16 sec                                               | 957 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 619 ms: 1.17x faster                                                    |
| async_tree_memoization     | 578 ms                                                 | 503 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 634 ms: 1.14x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.21x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 187 ms                                                 | 191 ms: 1.02x slower                                                    |
| float          | 84.7 ms                                                | 91.7 ms: 1.08x slower                                                   |
| nbody          | 97.0 ms                                                | 129 ms: 1.33x slower                                                    |
| Geometric mean | (ref)                                                  | 1.14x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.61 ms                                                | 3.70 ms: 1.03x slower                                                   |
| regex_dna      | 212 ms                                                 | 224 ms: 1.06x slower                                                    |
| regex_v8       | 23.1 ms                                                | 24.8 ms: 1.07x slower                                                   |
| regex_compile  | 148 ms                                                 | 182 ms: 1.22x slower                                                    |
| Geometric mean | (ref)                                                  | 1.09x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_parse      | 159 ms                                                 | 151 ms: 1.06x faster                                                    |
| unpickle             | 15.9 us                                                | 15.4 us: 1.03x faster                                                   |
| json_loads           | 28.5 us                                                | 27.7 us: 1.03x faster                                                   |
| unpickle_list        | 5.29 us                                                | 5.17 us: 1.02x faster                                                   |
| pickle_pure_python   | 324 us                                                 | 321 us: 1.01x faster                                                    |
| pickle_dict          | 35.5 us                                                | 35.2 us: 1.01x faster                                                   |
| pickle_list          | 5.08 us                                                | 5.15 us: 1.01x slower                                                   |
| xml_etree_iterparse  | 107 ms                                                 | 110 ms: 1.03x slower                                                    |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                   |
| xml_etree_generate   | 89.2 ms                                                | 92.7 ms: 1.04x slower                                                   |
| pickle               | 11.6 us                                                | 12.1 us: 1.04x slower                                                   |
| xml_etree_process    | 61.7 ms                                                | 65.2 ms: 1.06x slower                                                   |
| tomli_loads          | 2.33 sec                                               | 2.54 sec: 1.09x slower                                                  |
| unpickle_pure_python | 230 us                                                 | 295 us: 1.28x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.03x slower                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.13 ms: 1.03x slower                                                   |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 13.9 ms: 1.17x slower                                                   |
| django_template | 34.6 ms                                                | 41.4 ms: 1.20x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.18x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 347 ms: 1.30x faster                                                    |
| async_tree_none            | 472 ms                                                 | 372 ms: 1.27x faster                                                    |
| async_tree_memoization_tg  | 575 ms                                                 | 459 ms: 1.25x faster                                                    |
| async_tree_io_tg           | 1.18 sec                                               | 964 ms: 1.23x faster                                                    |
| async_tree_io              | 1.16 sec                                               | 957 ms: 1.21x faster                                                    |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 619 ms: 1.17x faster                                                    |
| async_tree_memoization     | 578 ms                                                 | 503 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 634 ms: 1.14x faster                                                    |
| xml_etree_parse            | 159 ms                                                 | 151 ms: 1.06x faster                                                    |
| generators                 | 31.2 ms                                                | 29.6 ms: 1.05x faster                                                   |
| pathlib                    | 19.3 ms                                                | 18.5 ms: 1.05x faster                                                   |
| logging_silent             | 104 ns                                                 | 101 ns: 1.04x faster                                                    |
| unpickle                   | 15.9 us                                                | 15.4 us: 1.03x faster                                                   |
| json_loads                 | 28.5 us                                                | 27.7 us: 1.03x faster                                                   |
| unpickle_list              | 5.29 us                                                | 5.17 us: 1.02x faster                                                   |
| pickle_pure_python         | 324 us                                                 | 321 us: 1.01x faster                                                    |
| pickle_dict                | 35.5 us                                                | 35.2 us: 1.01x faster                                                   |
| pickle_list                | 5.08 us                                                | 5.15 us: 1.01x slower                                                   |
| deepcopy_reduce            | 3.35 us                                                | 3.41 us: 1.02x slower                                                   |
| pidigits                   | 187 ms                                                 | 191 ms: 1.02x slower                                                    |
| chameleon                  | 7.41 ms                                                | 7.57 ms: 1.02x slower                                                   |
| regex_effbot               | 3.61 ms                                                | 3.70 ms: 1.03x slower                                                   |
| python_startup_no_site     | 6.94 ms                                                | 7.13 ms: 1.03x slower                                                   |
| asyncio_websockets         | 551 ms                                                 | 568 ms: 1.03x slower                                                    |
| async_generators           | 463 ms                                                 | 477 ms: 1.03x slower                                                    |
| xml_etree_iterparse        | 107 ms                                                 | 110 ms: 1.03x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                   |
| xml_etree_generate         | 89.2 ms                                                | 92.7 ms: 1.04x slower                                                   |
| pickle                     | 11.6 us                                                | 12.1 us: 1.04x slower                                                   |
| dask                       | 372 ms                                                 | 390 ms: 1.05x slower                                                    |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.87 sec: 1.05x slower                                                  |
| coroutines                 | 23.2 ms                                                | 24.3 ms: 1.05x slower                                                   |
| raytrace                   | 312 ms                                                 | 330 ms: 1.06x slower                                                    |
| regex_dna                  | 212 ms                                                 | 224 ms: 1.06x slower                                                    |
| xml_etree_process          | 61.7 ms                                                | 65.2 ms: 1.06x slower                                                   |
| logging_format             | 7.23 us                                                | 7.66 us: 1.06x slower                                                   |
| gc_traversal               | 3.79 ms                                                | 4.05 ms: 1.07x slower                                                   |
| sympy_sum                  | 169 ms                                                 | 180 ms: 1.07x slower                                                    |
| logging_simple             | 6.46 us                                                | 6.90 us: 1.07x slower                                                   |
| bench_thread_pool          | 842 us                                                 | 902 us: 1.07x slower                                                    |
| regex_v8                   | 23.1 ms                                                | 24.8 ms: 1.07x slower                                                   |
| gunicorn                   | 1.24 ms                                                | 1.34 ms: 1.08x slower                                                   |
| dulwich_log                | 68.5 ms                                                | 73.9 ms: 1.08x slower                                                   |
| aiohttp                    | 1.15 ms                                                | 1.24 ms: 1.08x slower                                                   |
| deepcopy                   | 371 us                                                 | 401 us: 1.08x slower                                                    |
| asyncio_tcp                | 491 ms                                                 | 530 ms: 1.08x slower                                                    |
| sqlite_synth               | 2.83 us                                                | 3.06 us: 1.08x slower                                                   |
| float                      | 84.7 ms                                                | 91.7 ms: 1.08x slower                                                   |
| pycparser                  | 1.18 sec                                               | 1.28 sec: 1.08x slower                                                  |
| meteor_contest             | 112 ms                                                 | 123 ms: 1.09x slower                                                    |
| tomli_loads                | 2.33 sec                                               | 2.54 sec: 1.09x slower                                                  |
| sqlglot_transpile          | 1.68 ms                                                | 1.85 ms: 1.10x slower                                                   |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                   |
| sympy_str                  | 300 ms                                                 | 331 ms: 1.11x slower                                                    |
| sympy_integrate            | 21.4 ms                                                | 23.8 ms: 1.11x slower                                                   |
| 2to3                       | 274 ms                                                 | 305 ms: 1.11x slower                                                    |
| sqlglot_parse              | 1.36 ms                                                | 1.52 ms: 1.11x slower                                                   |
| comprehensions             | 21.8 us                                                | 24.7 us: 1.14x slower                                                   |
| crypto_pyaes               | 81.9 ms                                                | 93.6 ms: 1.14x slower                                                   |
| mdp                        | 2.63 sec                                               | 3.01 sec: 1.15x slower                                                  |
| sympy_expand               | 478 ms                                                 | 549 ms: 1.15x slower                                                    |
| deepcopy_memo              | 40.7 us                                                | 47.3 us: 1.16x slower                                                   |
| mako                       | 11.9 ms                                                | 13.9 ms: 1.17x slower                                                   |
| sqlglot_normalize          | 110 ms                                                 | 129 ms: 1.17x slower                                                    |
| scimark_fft                | 382 ms                                                 | 454 ms: 1.19x slower                                                    |
| sqlglot_optimize           | 54.8 ms                                                | 65.3 ms: 1.19x slower                                                   |
| chaos                      | 67.0 ms                                                | 79.8 ms: 1.19x slower                                                   |
| fannkuch                   | 417 ms                                                 | 499 ms: 1.20x slower                                                    |
| deltablue                  | 3.72 ms                                                | 4.45 ms: 1.20x slower                                                   |
| django_template            | 34.6 ms                                                | 41.4 ms: 1.20x slower                                                   |
| create_gc_cycles           | 1.48 ms                                                | 1.78 ms: 1.21x slower                                                   |
| scimark_sor                | 129 ms                                                 | 157 ms: 1.22x slower                                                    |
| regex_compile              | 148 ms                                                 | 182 ms: 1.22x slower                                                    |
| scimark_monte_carlo        | 75.1 ms                                                | 92.1 ms: 1.23x slower                                                   |
| pyflate                    | 482 ms                                                 | 592 ms: 1.23x slower                                                    |
| pprint_safe_repr           | 776 ms                                                 | 953 ms: 1.23x slower                                                    |
| richards_super             | 51.5 ms                                                | 63.5 ms: 1.23x slower                                                   |
| richards                   | 45.8 ms                                                | 56.7 ms: 1.24x slower                                                   |
| typing_runtime_protocols   | 158 us                                                 | 196 us: 1.24x slower                                                    |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 6.32 ms: 1.25x slower                                                   |
| spectral_norm              | 115 ms                                                 | 144 ms: 1.26x slower                                                    |
| pprint_pformat             | 1.57 sec                                               | 1.98 sec: 1.26x slower                                                  |
| unpickle_pure_python       | 230 us                                                 | 295 us: 1.28x slower                                                    |
| telco                      | 7.10 ms                                                | 9.32 ms: 1.31x slower                                                   |
| nqueens                    | 83.3 ms                                                | 111 ms: 1.33x slower                                                    |
| nbody                      | 97.0 ms                                                | 129 ms: 1.33x slower                                                    |
| coverage                   | 72.7 ms                                                | 97.6 ms: 1.34x slower                                                   |
| scimark_lu                 | 118 ms                                                 | 168 ms: 1.42x slower                                                    |
| go                         | 139 ms                                                 | 212 ms: 1.52x slower                                                    |
| hexiom                     | 6.41 ms                                                | 10.2 ms: 1.59x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                            |

Benchmark hidden because not significant (3): json, tornado_http, bench_mp_pool
Ignored benchmarks (5) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: docutils, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240426-3.13.0a6+-65aa34a-PYTHON_UOPS/bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a.json: djangocms, genshi_text, genshi_xml, html5lib, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 0.97x