# Results vs. 3.12.0

- fork: faster-cpython
- ref: unify_tier_2_for_ite
- machine: linux-x86_64
- commit hash: 04feb78
- commit date: 2024-04-30
- overall geometric mean: 1.08x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 321 ms: 1.17x slower                                                             |
| chameleon      | 7.41 ms                                                | 7.94 ms: 1.07x slower                                                            |
| docutils       | 2.77 sec                                               | 3.19 sec: 1.15x slower                                                           |
| Geometric mean | (ref)                                                  | 1.10x slower                                                                     |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 350 ms: 1.28x faster                                                             |
| async_tree_none            | 472 ms                                                 | 373 ms: 1.27x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 457 ms: 1.26x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 958 ms: 1.23x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 964 ms: 1.20x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 620 ms: 1.17x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 499 ms: 1.16x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 633 ms: 1.15x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.21x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 91.9 ms: 1.08x slower                                                            |
| pidigits       | 187 ms                                                 | 213 ms: 1.14x slower                                                             |
| nbody          | 97.0 ms                                                | 125 ms: 1.29x slower                                                             |
| Geometric mean | (ref)                                                  | 1.17x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.61 ms                                                | 3.68 ms: 1.02x slower                                                            |
| regex_dna      | 212 ms                                                 | 221 ms: 1.04x slower                                                             |
| regex_v8       | 23.1 ms                                                | 25.0 ms: 1.08x slower                                                            |
| regex_compile  | 148 ms                                                 | 181 ms: 1.22x slower                                                             |
| Geometric mean | (ref)                                                  | 1.09x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_parse      | 159 ms                                                 | 153 ms: 1.04x faster                                                             |
| json_loads           | 28.5 us                                                | 27.7 us: 1.03x faster                                                            |
| pickle_list          | 5.08 us                                                | 5.02 us: 1.01x faster                                                            |
| pickle_dict          | 35.5 us                                                | 35.2 us: 1.01x faster                                                            |
| pickle_pure_python   | 324 us                                                 | 321 us: 1.01x faster                                                             |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                            |
| unpickle             | 15.9 us                                                | 16.5 us: 1.04x slower                                                            |
| xml_etree_iterparse  | 107 ms                                                 | 111 ms: 1.04x slower                                                             |
| pickle               | 11.6 us                                                | 12.1 us: 1.05x slower                                                            |
| xml_etree_generate   | 89.2 ms                                                | 96.3 ms: 1.08x slower                                                            |
| tomli_loads          | 2.33 sec                                               | 2.54 sec: 1.09x slower                                                           |
| xml_etree_process    | 61.7 ms                                                | 67.5 ms: 1.09x slower                                                            |
| unpickle_pure_python | 230 us                                                 | 286 us: 1.24x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                                     |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.17 ms: 1.03x slower                                                            |
| python_startup         | 9.55 ms                                                | 10.6 ms: 1.11x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 14.0 ms: 1.17x slower                                                            |
| django_template | 34.6 ms                                                | 40.7 ms: 1.18x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.17x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 350 ms: 1.28x faster                                                             |
| async_tree_none            | 472 ms                                                 | 373 ms: 1.27x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 457 ms: 1.26x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 958 ms: 1.23x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 964 ms: 1.20x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 620 ms: 1.17x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 499 ms: 1.16x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 633 ms: 1.15x faster                                                             |
| pathlib                    | 19.3 ms                                                | 18.2 ms: 1.06x faster                                                            |
| xml_etree_parse            | 159 ms                                                 | 153 ms: 1.04x faster                                                             |
| json_loads                 | 28.5 us                                                | 27.7 us: 1.03x faster                                                            |
| logging_format             | 7.23 us                                                | 7.09 us: 1.02x faster                                                            |
| json                       | 5.26 ms                                                | 5.16 ms: 1.02x faster                                                            |
| pickle_list                | 5.08 us                                                | 5.02 us: 1.01x faster                                                            |
| pickle_dict                | 35.5 us                                                | 35.2 us: 1.01x faster                                                            |
| pickle_pure_python         | 324 us                                                 | 321 us: 1.01x faster                                                             |
| deepcopy_reduce            | 3.35 us                                                | 3.38 us: 1.01x slower                                                            |
| regex_effbot               | 3.61 ms                                                | 3.68 ms: 1.02x slower                                                            |
| async_generators           | 463 ms                                                 | 476 ms: 1.03x slower                                                             |
| asyncio_websockets         | 551 ms                                                 | 567 ms: 1.03x slower                                                             |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                            |
| logging_silent             | 104 ns                                                 | 108 ns: 1.03x slower                                                             |
| python_startup_no_site     | 6.94 ms                                                | 7.17 ms: 1.03x slower                                                            |
| dask                       | 372 ms                                                 | 386 ms: 1.04x slower                                                             |
| unpickle                   | 15.9 us                                                | 16.5 us: 1.04x slower                                                            |
| xml_etree_iterparse        | 107 ms                                                 | 111 ms: 1.04x slower                                                             |
| regex_dna                  | 212 ms                                                 | 221 ms: 1.04x slower                                                             |
| pickle                     | 11.6 us                                                | 12.1 us: 1.05x slower                                                            |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.87 sec: 1.05x slower                                                           |
| coroutines                 | 23.2 ms                                                | 24.3 ms: 1.05x slower                                                            |
| deepcopy                   | 371 us                                                 | 389 us: 1.05x slower                                                             |
| sympy_sum                  | 169 ms                                                 | 179 ms: 1.06x slower                                                             |
| sqlite_synth               | 2.83 us                                                | 3.03 us: 1.07x slower                                                            |
| gc_traversal               | 3.79 ms                                                | 4.06 ms: 1.07x slower                                                            |
| raytrace                   | 312 ms                                                 | 334 ms: 1.07x slower                                                             |
| mdp                        | 2.63 sec                                               | 2.82 sec: 1.07x slower                                                           |
| chameleon                  | 7.41 ms                                                | 7.94 ms: 1.07x slower                                                            |
| asyncio_tcp                | 491 ms                                                 | 528 ms: 1.08x slower                                                             |
| regex_v8                   | 23.1 ms                                                | 25.0 ms: 1.08x slower                                                            |
| xml_etree_generate         | 89.2 ms                                                | 96.3 ms: 1.08x slower                                                            |
| meteor_contest             | 112 ms                                                 | 122 ms: 1.08x slower                                                             |
| sqlglot_transpile          | 1.68 ms                                                | 1.82 ms: 1.08x slower                                                            |
| bench_thread_pool          | 842 us                                                 | 912 us: 1.08x slower                                                             |
| float                      | 84.7 ms                                                | 91.9 ms: 1.08x slower                                                            |
| pycparser                  | 1.18 sec                                               | 1.28 sec: 1.09x slower                                                           |
| gunicorn                   | 1.24 ms                                                | 1.35 ms: 1.09x slower                                                            |
| tomli_loads                | 2.33 sec                                               | 2.54 sec: 1.09x slower                                                           |
| xml_etree_process          | 61.7 ms                                                | 67.5 ms: 1.09x slower                                                            |
| aiohttp                    | 1.15 ms                                                | 1.26 ms: 1.09x slower                                                            |
| crypto_pyaes               | 81.9 ms                                                | 89.6 ms: 1.10x slower                                                            |
| dulwich_log                | 68.5 ms                                                | 75.1 ms: 1.10x slower                                                            |
| sqlglot_parse              | 1.36 ms                                                | 1.49 ms: 1.10x slower                                                            |
| sympy_str                  | 300 ms                                                 | 332 ms: 1.11x slower                                                             |
| python_startup             | 9.55 ms                                                | 10.6 ms: 1.11x slower                                                            |
| deepcopy_memo              | 40.7 us                                                | 45.5 us: 1.12x slower                                                            |
| comprehensions             | 21.8 us                                                | 24.6 us: 1.13x slower                                                            |
| sympy_integrate            | 21.4 ms                                                | 24.2 ms: 1.13x slower                                                            |
| pidigits                   | 187 ms                                                 | 213 ms: 1.14x slower                                                             |
| docutils                   | 2.77 sec                                               | 3.19 sec: 1.15x slower                                                           |
| fannkuch                   | 417 ms                                                 | 481 ms: 1.15x slower                                                             |
| deltablue                  | 3.72 ms                                                | 4.29 ms: 1.15x slower                                                            |
| scimark_fft                | 382 ms                                                 | 445 ms: 1.17x slower                                                             |
| sqlglot_normalize          | 110 ms                                                 | 129 ms: 1.17x slower                                                             |
| 2to3                       | 274 ms                                                 | 321 ms: 1.17x slower                                                             |
| chaos                      | 67.0 ms                                                | 78.6 ms: 1.17x slower                                                            |
| sympy_expand               | 478 ms                                                 | 561 ms: 1.17x slower                                                             |
| mako                       | 11.9 ms                                                | 14.0 ms: 1.17x slower                                                            |
| django_template            | 34.6 ms                                                | 40.7 ms: 1.18x slower                                                            |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.97 ms: 1.18x slower                                                            |
| sqlglot_optimize           | 54.8 ms                                                | 65.0 ms: 1.19x slower                                                            |
| scimark_monte_carlo        | 75.1 ms                                                | 89.5 ms: 1.19x slower                                                            |
| spectral_norm              | 115 ms                                                 | 137 ms: 1.19x slower                                                             |
| typing_runtime_protocols   | 158 us                                                 | 190 us: 1.20x slower                                                             |
| create_gc_cycles           | 1.48 ms                                                | 1.78 ms: 1.21x slower                                                            |
| regex_compile              | 148 ms                                                 | 181 ms: 1.22x slower                                                             |
| pyflate                    | 482 ms                                                 | 595 ms: 1.23x slower                                                             |
| scimark_sor                | 129 ms                                                 | 159 ms: 1.23x slower                                                             |
| unpickle_pure_python       | 230 us                                                 | 286 us: 1.24x slower                                                             |
| pprint_safe_repr           | 776 ms                                                 | 965 ms: 1.24x slower                                                             |
| pprint_pformat             | 1.57 sec                                               | 2.00 sec: 1.27x slower                                                           |
| nbody                      | 97.0 ms                                                | 125 ms: 1.29x slower                                                             |
| coverage                   | 72.7 ms                                                | 93.6 ms: 1.29x slower                                                            |
| richards_super             | 51.5 ms                                                | 66.5 ms: 1.29x slower                                                            |
| richards                   | 45.8 ms                                                | 59.7 ms: 1.30x slower                                                            |
| nqueens                    | 83.3 ms                                                | 109 ms: 1.30x slower                                                             |
| telco                      | 7.10 ms                                                | 9.32 ms: 1.31x slower                                                            |
| scimark_lu                 | 118 ms                                                 | 168 ms: 1.42x slower                                                             |
| go                         | 139 ms                                                 | 203 ms: 1.46x slower                                                             |
| hexiom                     | 6.41 ms                                                | 9.77 ms: 1.52x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.08x slower                                                                     |

Benchmark hidden because not significant (6): logging_simple, unpickle_list, bench_mp_pool, generators, tornado_http, mypy2
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240430-3.13.0a6+-04feb78-PYTHON_UOPS/bm-20240430-linux-x86_64-faster%2dcpython-unify_tier_2_for_ite-3.13.0a6+-04feb78.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 0.98x