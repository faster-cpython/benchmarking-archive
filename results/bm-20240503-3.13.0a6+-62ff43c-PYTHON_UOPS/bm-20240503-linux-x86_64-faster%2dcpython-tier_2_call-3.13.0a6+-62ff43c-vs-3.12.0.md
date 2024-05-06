# Results vs. 3.12.0

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 62ff43c
- commit date: 2024-05-03
- overall geometric mean: 1.11x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 327 ms: 1.19x slower                                                    |
| chameleon      | 7.41 ms                                                | 8.06 ms: 1.09x slower                                                   |
| tornado_http   | 103 ms                                                 | 105 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                  | 1.10x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 358 ms: 1.26x faster                                                    |
| async_tree_none            | 472 ms                                                 | 380 ms: 1.24x faster                                                    |
| async_tree_memoization_tg  | 575 ms                                                 | 468 ms: 1.23x faster                                                    |
| async_tree_io_tg           | 1.18 sec                                               | 976 ms: 1.21x faster                                                    |
| async_tree_io              | 1.16 sec                                               | 985 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 631 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 640 ms: 1.13x faster                                                    |
| async_tree_memoization     | 578 ms                                                 | 512 ms: 1.13x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.19x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 187 ms                                                 | 196 ms: 1.05x slower                                                    |
| float          | 84.7 ms                                                | 90.6 ms: 1.07x slower                                                   |
| nbody          | 97.0 ms                                                | 122 ms: 1.26x slower                                                    |
| Geometric mean | (ref)                                                  | 1.12x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_effbot   | 3.61 ms                                                | 3.69 ms: 1.02x slower                                                   |
| regex_dna      | 212 ms                                                 | 227 ms: 1.07x slower                                                    |
| regex_v8       | 23.1 ms                                                | 25.6 ms: 1.11x slower                                                   |
| regex_compile  | 148 ms                                                 | 190 ms: 1.28x slower                                                    |
| Geometric mean | (ref)                                                  | 1.11x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| xml_etree_parse      | 159 ms                                                 | 152 ms: 1.05x faster                                                    |
| pickle_dict          | 35.5 us                                                | 34.0 us: 1.04x faster                                                   |
| json_loads           | 28.5 us                                                | 27.8 us: 1.02x faster                                                   |
| unpickle_list        | 5.29 us                                                | 5.23 us: 1.01x faster                                                   |
| pickle_list          | 5.08 us                                                | 5.13 us: 1.01x slower                                                   |
| pickle               | 11.6 us                                                | 11.9 us: 1.02x slower                                                   |
| xml_etree_iterparse  | 107 ms                                                 | 111 ms: 1.04x slower                                                    |
| json_dumps           | 10.4 ms                                                | 11.1 ms: 1.07x slower                                                   |
| xml_etree_generate   | 89.2 ms                                                | 97.6 ms: 1.09x slower                                                   |
| xml_etree_process    | 61.7 ms                                                | 68.4 ms: 1.11x slower                                                   |
| tomli_loads          | 2.33 sec                                               | 2.65 sec: 1.14x slower                                                  |
| unpickle_pure_python | 230 us                                                 | 285 us: 1.24x slower                                                    |
| pickle_pure_python   | 324 us                                                 | 405 us: 1.25x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                            |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.23 ms: 1.04x slower                                                   |
| python_startup         | 9.55 ms                                                | 10.7 ms: 1.12x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.08x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 14.0 ms: 1.18x slower                                                   |
| django_template | 34.6 ms                                                | 44.5 ms: 1.29x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.23x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 358 ms: 1.26x faster                                                    |
| async_tree_none            | 472 ms                                                 | 380 ms: 1.24x faster                                                    |
| async_tree_memoization_tg  | 575 ms                                                 | 468 ms: 1.23x faster                                                    |
| async_tree_io_tg           | 1.18 sec                                               | 976 ms: 1.21x faster                                                    |
| async_tree_io              | 1.16 sec                                               | 985 ms: 1.17x faster                                                    |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 631 ms: 1.15x faster                                                    |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 640 ms: 1.13x faster                                                    |
| async_tree_memoization     | 578 ms                                                 | 512 ms: 1.13x faster                                                    |
| xml_etree_parse            | 159 ms                                                 | 152 ms: 1.05x faster                                                    |
| gc_traversal               | 3.79 ms                                                | 3.62 ms: 1.05x faster                                                   |
| pickle_dict                | 35.5 us                                                | 34.0 us: 1.04x faster                                                   |
| pathlib                    | 19.3 ms                                                | 18.6 ms: 1.04x faster                                                   |
| json_loads                 | 28.5 us                                                | 27.8 us: 1.02x faster                                                   |
| generators                 | 31.2 ms                                                | 30.6 ms: 1.02x faster                                                   |
| unpickle_list              | 5.29 us                                                | 5.23 us: 1.01x faster                                                   |
| pickle_list                | 5.08 us                                                | 5.13 us: 1.01x slower                                                   |
| logging_format             | 7.23 us                                                | 7.30 us: 1.01x slower                                                   |
| logging_simple             | 6.46 us                                                | 6.55 us: 1.01x slower                                                   |
| async_generators           | 463 ms                                                 | 471 ms: 1.02x slower                                                    |
| regex_effbot               | 3.61 ms                                                | 3.69 ms: 1.02x slower                                                   |
| asyncio_websockets         | 551 ms                                                 | 563 ms: 1.02x slower                                                    |
| pickle                     | 11.6 us                                                | 11.9 us: 1.02x slower                                                   |
| tornado_http               | 103 ms                                                 | 105 ms: 1.03x slower                                                    |
| xml_etree_iterparse        | 107 ms                                                 | 111 ms: 1.04x slower                                                    |
| python_startup_no_site     | 6.94 ms                                                | 7.23 ms: 1.04x slower                                                   |
| pidigits                   | 187 ms                                                 | 196 ms: 1.05x slower                                                    |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.87 sec: 1.05x slower                                                  |
| dask                       | 372 ms                                                 | 393 ms: 1.06x slower                                                    |
| sqlite_synth               | 2.83 us                                                | 3.00 us: 1.06x slower                                                   |
| raytrace                   | 312 ms                                                 | 331 ms: 1.06x slower                                                    |
| mdp                        | 2.63 sec                                               | 2.81 sec: 1.07x slower                                                  |
| regex_dna                  | 212 ms                                                 | 227 ms: 1.07x slower                                                    |
| float                      | 84.7 ms                                                | 90.6 ms: 1.07x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 11.1 ms: 1.07x slower                                                   |
| coroutines                 | 23.2 ms                                                | 24.9 ms: 1.08x slower                                                   |
| asyncio_tcp                | 491 ms                                                 | 532 ms: 1.08x slower                                                    |
| bench_thread_pool          | 842 us                                                 | 914 us: 1.09x slower                                                    |
| chameleon                  | 7.41 ms                                                | 8.06 ms: 1.09x slower                                                   |
| sympy_sum                  | 169 ms                                                 | 184 ms: 1.09x slower                                                    |
| xml_etree_generate         | 89.2 ms                                                | 97.6 ms: 1.09x slower                                                   |
| meteor_contest             | 112 ms                                                 | 123 ms: 1.10x slower                                                    |
| dulwich_log                | 68.5 ms                                                | 75.5 ms: 1.10x slower                                                   |
| regex_v8                   | 23.1 ms                                                | 25.6 ms: 1.11x slower                                                   |
| gunicorn                   | 1.24 ms                                                | 1.38 ms: 1.11x slower                                                   |
| xml_etree_process          | 61.7 ms                                                | 68.4 ms: 1.11x slower                                                   |
| aiohttp                    | 1.15 ms                                                | 1.28 ms: 1.11x slower                                                   |
| python_startup             | 9.55 ms                                                | 10.7 ms: 1.12x slower                                                   |
| crypto_pyaes               | 81.9 ms                                                | 91.9 ms: 1.12x slower                                                   |
| tomli_loads                | 2.33 sec                                               | 2.65 sec: 1.14x slower                                                  |
| sympy_str                  | 300 ms                                                 | 344 ms: 1.15x slower                                                    |
| deepcopy_reduce            | 3.35 us                                                | 3.84 us: 1.15x slower                                                   |
| comprehensions             | 21.8 us                                                | 25.1 us: 1.15x slower                                                   |
| sympy_integrate            | 21.4 ms                                                | 24.8 ms: 1.16x slower                                                   |
| scimark_fft                | 382 ms                                                 | 443 ms: 1.16x slower                                                    |
| fannkuch                   | 417 ms                                                 | 487 ms: 1.17x slower                                                    |
| deltablue                  | 3.72 ms                                                | 4.37 ms: 1.18x slower                                                   |
| mako                       | 11.9 ms                                                | 14.0 ms: 1.18x slower                                                   |
| 2to3                       | 274 ms                                                 | 327 ms: 1.19x slower                                                    |
| scimark_monte_carlo        | 75.1 ms                                                | 90.1 ms: 1.20x slower                                                   |
| pycparser                  | 1.18 sec                                               | 1.42 sec: 1.20x slower                                                  |
| sympy_expand               | 478 ms                                                 | 578 ms: 1.21x slower                                                    |
| create_gc_cycles           | 1.48 ms                                                | 1.79 ms: 1.21x slower                                                   |
| sqlglot_optimize           | 54.8 ms                                                | 66.6 ms: 1.21x slower                                                   |
| sqlglot_transpile          | 1.68 ms                                                | 2.05 ms: 1.22x slower                                                   |
| spectral_norm              | 115 ms                                                 | 140 ms: 1.22x slower                                                    |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 6.17 ms: 1.22x slower                                                   |
| typing_runtime_protocols   | 158 us                                                 | 194 us: 1.23x slower                                                    |
| sqlglot_parse              | 1.36 ms                                                | 1.67 ms: 1.23x slower                                                   |
| scimark_sor                | 129 ms                                                 | 159 ms: 1.23x slower                                                    |
| deepcopy                   | 371 us                                                 | 459 us: 1.24x slower                                                    |
| unpickle_pure_python       | 230 us                                                 | 285 us: 1.24x slower                                                    |
| sqlglot_normalize          | 110 ms                                                 | 137 ms: 1.24x slower                                                    |
| pprint_safe_repr           | 776 ms                                                 | 968 ms: 1.25x slower                                                    |
| pickle_pure_python         | 324 us                                                 | 405 us: 1.25x slower                                                    |
| nbody                      | 97.0 ms                                                | 122 ms: 1.26x slower                                                    |
| chaos                      | 67.0 ms                                                | 84.4 ms: 1.26x slower                                                   |
| pyflate                    | 482 ms                                                 | 609 ms: 1.26x slower                                                    |
| deepcopy_memo              | 40.7 us                                                | 51.4 us: 1.26x slower                                                   |
| pprint_pformat             | 1.57 sec                                               | 1.99 sec: 1.27x slower                                                  |
| coverage                   | 72.7 ms                                                | 92.7 ms: 1.28x slower                                                   |
| regex_compile              | 148 ms                                                 | 190 ms: 1.28x slower                                                    |
| django_template            | 34.6 ms                                                | 44.5 ms: 1.29x slower                                                   |
| richards_super             | 51.5 ms                                                | 66.6 ms: 1.29x slower                                                   |
| richards                   | 45.8 ms                                                | 59.4 ms: 1.29x slower                                                   |
| go                         | 139 ms                                                 | 181 ms: 1.30x slower                                                    |
| nqueens                    | 83.3 ms                                                | 109 ms: 1.31x slower                                                    |
| telco                      | 7.10 ms                                                | 9.60 ms: 1.35x slower                                                   |
| logging_silent             | 104 ns                                                 | 146 ns: 1.40x slower                                                    |
| scimark_lu                 | 118 ms                                                 | 167 ms: 1.41x slower                                                    |
| hexiom                     | 6.41 ms                                                | 9.66 ms: 1.51x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.11x slower                                                            |

Benchmark hidden because not significant (4): unpickle, json, bench_mp_pool, mypy2
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: docutils, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240503-3.13.0a6+-62ff43c-PYTHON_UOPS/bm-20240503-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-62ff43c.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 0.97x