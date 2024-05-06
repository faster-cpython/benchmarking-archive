# Results vs. 3.12.0

- fork: faster-cpython
- ref: return_gen_tier_2
- machine: linux-x86_64
- commit hash: fad1c67
- commit date: 2024-04-23
- overall geometric mean: 1.06x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 301 ms: 1.10x slower                                                          |
| chameleon      | 7.41 ms                                                | 7.62 ms: 1.03x slower                                                         |
| docutils       | 2.77 sec                                               | 3.07 sec: 1.11x slower                                                        |
| Geometric mean | (ref)                                                  | 1.06x slower                                                                  |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 351 ms: 1.28x faster                                                          |
| async_tree_none            | 472 ms                                                 | 373 ms: 1.26x faster                                                          |
| async_tree_memoization_tg  | 575 ms                                                 | 459 ms: 1.25x faster                                                          |
| async_tree_io_tg           | 1.18 sec                                               | 969 ms: 1.22x faster                                                          |
| async_tree_io              | 1.16 sec                                               | 966 ms: 1.20x faster                                                          |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 623 ms: 1.17x faster                                                          |
| async_tree_memoization     | 578 ms                                                 | 499 ms: 1.16x faster                                                          |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 632 ms: 1.15x faster                                                          |
| Geometric mean             | (ref)                                                  | 1.21x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 89.3 ms: 1.05x slower                                                         |
| pidigits       | 187 ms                                                 | 218 ms: 1.16x slower                                                          |
| nbody          | 97.0 ms                                                | 120 ms: 1.24x slower                                                          |
| Geometric mean | (ref)                                                  | 1.15x slower                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_effbot   | 3.61 ms                                                | 3.69 ms: 1.02x slower                                                         |
| regex_dna      | 212 ms                                                 | 228 ms: 1.08x slower                                                          |
| regex_v8       | 23.1 ms                                                | 25.4 ms: 1.10x slower                                                         |
| regex_compile  | 148 ms                                                 | 179 ms: 1.20x slower                                                          |
| Geometric mean | (ref)                                                  | 1.10x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_loads           | 28.5 us                                                | 27.5 us: 1.04x faster                                                         |
| xml_etree_parse      | 159 ms                                                 | 154 ms: 1.03x faster                                                          |
| pickle_pure_python   | 324 us                                                 | 314 us: 1.03x faster                                                          |
| pickle_dict          | 35.5 us                                                | 35.0 us: 1.01x faster                                                         |
| unpickle             | 15.9 us                                                | 15.7 us: 1.01x faster                                                         |
| unpickle_list        | 5.29 us                                                | 5.26 us: 1.01x faster                                                         |
| pickle_list          | 5.08 us                                                | 5.19 us: 1.02x slower                                                         |
| xml_etree_iterparse  | 107 ms                                                 | 110 ms: 1.03x slower                                                          |
| pickle               | 11.6 us                                                | 11.9 us: 1.03x slower                                                         |
| xml_etree_process    | 61.7 ms                                                | 64.2 ms: 1.04x slower                                                         |
| json_dumps           | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                         |
| xml_etree_generate   | 89.2 ms                                                | 93.3 ms: 1.05x slower                                                         |
| tomli_loads          | 2.33 sec                                               | 2.53 sec: 1.09x slower                                                        |
| unpickle_pure_python | 230 us                                                 | 283 us: 1.23x slower                                                          |
| Geometric mean       | (ref)                                                  | 1.03x slower                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.15 ms: 1.03x slower                                                         |
| python_startup         | 9.55 ms                                                | 10.6 ms: 1.10x slower                                                         |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| django_template | 34.6 ms                                                | 39.8 ms: 1.15x slower                                                         |
| mako            | 11.9 ms                                                | 13.8 ms: 1.16x slower                                                         |
| Geometric mean  | (ref)                                                  | 1.15x slower                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 123 us: 1.28x faster                                                          |
| async_tree_none_tg         | 450 ms                                                 | 351 ms: 1.28x faster                                                          |
| async_tree_none            | 472 ms                                                 | 373 ms: 1.26x faster                                                          |
| async_tree_memoization_tg  | 575 ms                                                 | 459 ms: 1.25x faster                                                          |
| async_tree_io_tg           | 1.18 sec                                               | 969 ms: 1.22x faster                                                          |
| async_tree_io              | 1.16 sec                                               | 966 ms: 1.20x faster                                                          |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 623 ms: 1.17x faster                                                          |
| async_tree_memoization     | 578 ms                                                 | 499 ms: 1.16x faster                                                          |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 632 ms: 1.15x faster                                                          |
| pathlib                    | 19.3 ms                                                | 18.2 ms: 1.06x faster                                                         |
| gc_traversal               | 3.79 ms                                                | 3.64 ms: 1.04x faster                                                         |
| json_loads                 | 28.5 us                                                | 27.5 us: 1.04x faster                                                         |
| generators                 | 31.2 ms                                                | 30.2 ms: 1.04x faster                                                         |
| xml_etree_parse            | 159 ms                                                 | 154 ms: 1.03x faster                                                          |
| pickle_pure_python         | 324 us                                                 | 314 us: 1.03x faster                                                          |
| deepcopy_reduce            | 3.35 us                                                | 3.28 us: 1.02x faster                                                         |
| coroutines                 | 23.2 ms                                                | 22.8 ms: 1.01x faster                                                         |
| pickle_dict                | 35.5 us                                                | 35.0 us: 1.01x faster                                                         |
| unpickle                   | 15.9 us                                                | 15.7 us: 1.01x faster                                                         |
| logging_simple             | 6.46 us                                                | 6.40 us: 1.01x faster                                                         |
| logging_format             | 7.23 us                                                | 7.17 us: 1.01x faster                                                         |
| unpickle_list              | 5.29 us                                                | 5.26 us: 1.01x faster                                                         |
| logging_silent             | 104 ns                                                 | 105 ns: 1.00x slower                                                          |
| asyncio_websockets         | 551 ms                                                 | 555 ms: 1.01x slower                                                          |
| deepcopy                   | 371 us                                                 | 376 us: 1.01x slower                                                          |
| pickle_list                | 5.08 us                                                | 5.19 us: 1.02x slower                                                         |
| regex_effbot               | 3.61 ms                                                | 3.69 ms: 1.02x slower                                                         |
| raytrace                   | 312 ms                                                 | 319 ms: 1.02x slower                                                          |
| dask                       | 372 ms                                                 | 382 ms: 1.03x slower                                                          |
| xml_etree_iterparse        | 107 ms                                                 | 110 ms: 1.03x slower                                                          |
| chameleon                  | 7.41 ms                                                | 7.62 ms: 1.03x slower                                                         |
| python_startup_no_site     | 6.94 ms                                                | 7.15 ms: 1.03x slower                                                         |
| pickle                     | 11.6 us                                                | 11.9 us: 1.03x slower                                                         |
| async_generators           | 463 ms                                                 | 478 ms: 1.03x slower                                                          |
| xml_etree_process          | 61.7 ms                                                | 64.2 ms: 1.04x slower                                                         |
| comprehensions             | 21.8 us                                                | 22.6 us: 1.04x slower                                                         |
| json_dumps                 | 10.4 ms                                                | 10.8 ms: 1.04x slower                                                         |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.87 sec: 1.05x slower                                                        |
| xml_etree_generate         | 89.2 ms                                                | 93.3 ms: 1.05x slower                                                         |
| bench_thread_pool          | 842 us                                                 | 883 us: 1.05x slower                                                          |
| sympy_sum                  | 169 ms                                                 | 177 ms: 1.05x slower                                                          |
| float                      | 84.7 ms                                                | 89.3 ms: 1.05x slower                                                         |
| asyncio_tcp                | 491 ms                                                 | 517 ms: 1.05x slower                                                          |
| sqlite_synth               | 2.83 us                                                | 3.00 us: 1.06x slower                                                         |
| mdp                        | 2.63 sec                                               | 2.79 sec: 1.06x slower                                                        |
| meteor_contest             | 112 ms                                                 | 119 ms: 1.06x slower                                                          |
| sympy_str                  | 300 ms                                                 | 321 ms: 1.07x slower                                                          |
| sqlglot_transpile          | 1.68 ms                                                | 1.80 ms: 1.07x slower                                                         |
| deepcopy_memo              | 40.7 us                                                | 43.8 us: 1.07x slower                                                         |
| gunicorn                   | 1.24 ms                                                | 1.33 ms: 1.07x slower                                                         |
| regex_dna                  | 212 ms                                                 | 228 ms: 1.08x slower                                                          |
| dulwich_log                | 68.5 ms                                                | 73.8 ms: 1.08x slower                                                         |
| sympy_integrate            | 21.4 ms                                                | 23.1 ms: 1.08x slower                                                         |
| pycparser                  | 1.18 sec                                               | 1.27 sec: 1.08x slower                                                        |
| aiohttp                    | 1.15 ms                                                | 1.25 ms: 1.08x slower                                                         |
| sqlglot_parse              | 1.36 ms                                                | 1.48 ms: 1.09x slower                                                         |
| tomli_loads                | 2.33 sec                                               | 2.53 sec: 1.09x slower                                                        |
| 2to3                       | 274 ms                                                 | 301 ms: 1.10x slower                                                          |
| regex_v8                   | 23.1 ms                                                | 25.4 ms: 1.10x slower                                                         |
| python_startup             | 9.55 ms                                                | 10.6 ms: 1.10x slower                                                         |
| docutils                   | 2.77 sec                                               | 3.07 sec: 1.11x slower                                                        |
| deltablue                  | 3.72 ms                                                | 4.15 ms: 1.12x slower                                                         |
| sympy_expand               | 478 ms                                                 | 534 ms: 1.12x slower                                                          |
| sqlglot_normalize          | 110 ms                                                 | 123 ms: 1.12x slower                                                          |
| crypto_pyaes               | 81.9 ms                                                | 92.0 ms: 1.12x slower                                                         |
| scimark_fft                | 382 ms                                                 | 436 ms: 1.14x slower                                                          |
| scimark_monte_carlo        | 75.1 ms                                                | 86.0 ms: 1.14x slower                                                         |
| django_template            | 34.6 ms                                                | 39.8 ms: 1.15x slower                                                         |
| sqlglot_optimize           | 54.8 ms                                                | 63.3 ms: 1.16x slower                                                         |
| scimark_sor                | 129 ms                                                 | 149 ms: 1.16x slower                                                          |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.85 ms: 1.16x slower                                                         |
| mako                       | 11.9 ms                                                | 13.8 ms: 1.16x slower                                                         |
| pidigits                   | 187 ms                                                 | 218 ms: 1.16x slower                                                          |
| fannkuch                   | 417 ms                                                 | 487 ms: 1.17x slower                                                          |
| chaos                      | 67.0 ms                                                | 78.4 ms: 1.17x slower                                                         |
| create_gc_cycles           | 1.48 ms                                                | 1.76 ms: 1.20x slower                                                         |
| richards_super             | 51.5 ms                                                | 61.8 ms: 1.20x slower                                                         |
| spectral_norm              | 115 ms                                                 | 138 ms: 1.20x slower                                                          |
| regex_compile              | 148 ms                                                 | 179 ms: 1.20x slower                                                          |
| pprint_safe_repr           | 776 ms                                                 | 939 ms: 1.21x slower                                                          |
| richards                   | 45.8 ms                                                | 55.6 ms: 1.21x slower                                                         |
| pyflate                    | 482 ms                                                 | 588 ms: 1.22x slower                                                          |
| unpickle_pure_python       | 230 us                                                 | 283 us: 1.23x slower                                                          |
| nbody                      | 97.0 ms                                                | 120 ms: 1.24x slower                                                          |
| pprint_pformat             | 1.57 sec                                               | 1.94 sec: 1.24x slower                                                        |
| nqueens                    | 83.3 ms                                                | 105 ms: 1.26x slower                                                          |
| telco                      | 7.10 ms                                                | 9.13 ms: 1.29x slower                                                         |
| go                         | 139 ms                                                 | 185 ms: 1.32x slower                                                          |
| coverage                   | 72.7 ms                                                | 99.3 ms: 1.37x slower                                                         |
| scimark_lu                 | 118 ms                                                 | 163 ms: 1.38x slower                                                          |
| hexiom                     | 6.41 ms                                                | 9.45 ms: 1.47x slower                                                         |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                                  |

Benchmark hidden because not significant (4): mypy2, tornado_http, json, bench_mp_pool
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240423-3.13.0a6+-fad1c67-PYTHON_UOPS/bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 0.97x