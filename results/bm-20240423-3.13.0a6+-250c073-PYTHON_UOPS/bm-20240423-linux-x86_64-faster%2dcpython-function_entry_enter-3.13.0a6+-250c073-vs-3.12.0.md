# Results vs. 3.12.0

- fork: faster-cpython
- ref: function_entry_enter
- machine: linux-x86_64
- commit hash: 250c073
- commit date: 2024-04-23
- overall geometric mean: 1.07x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 303 ms: 1.10x slower                                                             |
| chameleon      | 7.41 ms                                                | 8.01 ms: 1.08x slower                                                            |
| docutils       | 2.77 sec                                               | 3.09 sec: 1.12x slower                                                           |
| Geometric mean | (ref)                                                  | 1.08x slower                                                                     |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 353 ms: 1.27x faster                                                             |
| async_tree_none            | 472 ms                                                 | 375 ms: 1.26x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 463 ms: 1.24x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 972 ms: 1.22x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 966 ms: 1.20x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 628 ms: 1.16x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 502 ms: 1.15x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 638 ms: 1.14x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.20x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 91.1 ms: 1.08x slower                                                            |
| pidigits       | 187 ms                                                 | 212 ms: 1.13x slower                                                             |
| nbody          | 97.0 ms                                                | 123 ms: 1.27x slower                                                             |
| Geometric mean | (ref)                                                  | 1.16x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.61 ms                                                | 3.67 ms: 1.02x slower                                                            |
| regex_dna      | 212 ms                                                 | 224 ms: 1.06x slower                                                             |
| regex_v8       | 23.1 ms                                                | 25.1 ms: 1.08x slower                                                            |
| regex_compile  | 148 ms                                                 | 182 ms: 1.22x slower                                                             |
| Geometric mean | (ref)                                                  | 1.09x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_parse      | 159 ms                                                 | 151 ms: 1.05x faster                                                             |
| pickle_pure_python   | 324 us                                                 | 318 us: 1.02x faster                                                             |
| json_loads           | 28.5 us                                                | 28.2 us: 1.01x faster                                                            |
| pickle_list          | 5.08 us                                                | 5.12 us: 1.01x slower                                                            |
| unpickle_list        | 5.29 us                                                | 5.41 us: 1.02x slower                                                            |
| pickle               | 11.6 us                                                | 11.9 us: 1.03x slower                                                            |
| xml_etree_process    | 61.7 ms                                                | 64.0 ms: 1.04x slower                                                            |
| xml_etree_generate   | 89.2 ms                                                | 92.9 ms: 1.04x slower                                                            |
| json_dumps           | 10.4 ms                                                | 10.9 ms: 1.05x slower                                                            |
| xml_etree_iterparse  | 107 ms                                                 | 112 ms: 1.05x slower                                                             |
| tomli_loads          | 2.33 sec                                               | 2.53 sec: 1.09x slower                                                           |
| unpickle_pure_python | 230 us                                                 | 286 us: 1.24x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.03x slower                                                                     |

Benchmark hidden because not significant (2): unpickle, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.18 ms: 1.03x slower                                                            |
| python_startup         | 9.55 ms                                                | 10.6 ms: 1.11x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 13.7 ms: 1.15x slower                                                            |
| django_template | 34.6 ms                                                | 40.9 ms: 1.18x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.17x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 123 us: 1.28x faster                                                             |
| async_tree_none_tg         | 450 ms                                                 | 353 ms: 1.27x faster                                                             |
| async_tree_none            | 472 ms                                                 | 375 ms: 1.26x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 463 ms: 1.24x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 972 ms: 1.22x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 966 ms: 1.20x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 628 ms: 1.16x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 502 ms: 1.15x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 638 ms: 1.14x faster                                                             |
| xml_etree_parse            | 159 ms                                                 | 151 ms: 1.05x faster                                                             |
| pathlib                    | 19.3 ms                                                | 18.4 ms: 1.05x faster                                                            |
| generators                 | 31.2 ms                                                | 30.2 ms: 1.03x faster                                                            |
| pickle_pure_python         | 324 us                                                 | 318 us: 1.02x faster                                                             |
| json_loads                 | 28.5 us                                                | 28.2 us: 1.01x faster                                                            |
| logging_simple             | 6.46 us                                                | 6.40 us: 1.01x faster                                                            |
| logging_silent             | 104 ns                                                 | 104 ns: 1.01x faster                                                             |
| pickle_list                | 5.08 us                                                | 5.12 us: 1.01x slower                                                            |
| logging_format             | 7.23 us                                                | 7.28 us: 1.01x slower                                                            |
| regex_effbot               | 3.61 ms                                                | 3.67 ms: 1.02x slower                                                            |
| unpickle_list              | 5.29 us                                                | 5.41 us: 1.02x slower                                                            |
| async_generators           | 463 ms                                                 | 475 ms: 1.03x slower                                                             |
| pickle                     | 11.6 us                                                | 11.9 us: 1.03x slower                                                            |
| deepcopy                   | 371 us                                                 | 381 us: 1.03x slower                                                             |
| asyncio_websockets         | 551 ms                                                 | 567 ms: 1.03x slower                                                             |
| raytrace                   | 312 ms                                                 | 322 ms: 1.03x slower                                                             |
| python_startup_no_site     | 6.94 ms                                                | 7.18 ms: 1.03x slower                                                            |
| coroutines                 | 23.2 ms                                                | 24.0 ms: 1.03x slower                                                            |
| dask                       | 372 ms                                                 | 385 ms: 1.04x slower                                                             |
| xml_etree_process          | 61.7 ms                                                | 64.0 ms: 1.04x slower                                                            |
| xml_etree_generate         | 89.2 ms                                                | 92.9 ms: 1.04x slower                                                            |
| gc_traversal               | 3.79 ms                                                | 3.96 ms: 1.04x slower                                                            |
| bench_thread_pool          | 842 us                                                 | 880 us: 1.05x slower                                                             |
| json_dumps                 | 10.4 ms                                                | 10.9 ms: 1.05x slower                                                            |
| xml_etree_iterparse        | 107 ms                                                 | 112 ms: 1.05x slower                                                             |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.87 sec: 1.05x slower                                                           |
| sqlite_synth               | 2.83 us                                                | 2.99 us: 1.05x slower                                                            |
| sympy_sum                  | 169 ms                                                 | 178 ms: 1.05x slower                                                             |
| regex_dna                  | 212 ms                                                 | 224 ms: 1.06x slower                                                             |
| mdp                        | 2.63 sec                                               | 2.78 sec: 1.06x slower                                                           |
| comprehensions             | 21.8 us                                                | 23.2 us: 1.07x slower                                                            |
| gunicorn                   | 1.24 ms                                                | 1.33 ms: 1.07x slower                                                            |
| dulwich_log                | 68.5 ms                                                | 73.2 ms: 1.07x slower                                                            |
| aiohttp                    | 1.15 ms                                                | 1.23 ms: 1.07x slower                                                            |
| asyncio_tcp                | 491 ms                                                 | 528 ms: 1.08x slower                                                             |
| float                      | 84.7 ms                                                | 91.1 ms: 1.08x slower                                                            |
| sqlglot_transpile          | 1.68 ms                                                | 1.82 ms: 1.08x slower                                                            |
| pycparser                  | 1.18 sec                                               | 1.27 sec: 1.08x slower                                                           |
| chameleon                  | 7.41 ms                                                | 8.01 ms: 1.08x slower                                                            |
| regex_v8                   | 23.1 ms                                                | 25.1 ms: 1.08x slower                                                            |
| meteor_contest             | 112 ms                                                 | 122 ms: 1.08x slower                                                             |
| tomli_loads                | 2.33 sec                                               | 2.53 sec: 1.09x slower                                                           |
| sympy_str                  | 300 ms                                                 | 326 ms: 1.09x slower                                                             |
| deepcopy_memo              | 40.7 us                                                | 44.6 us: 1.10x slower                                                            |
| sqlglot_parse              | 1.36 ms                                                | 1.50 ms: 1.10x slower                                                            |
| 2to3                       | 274 ms                                                 | 303 ms: 1.10x slower                                                             |
| python_startup             | 9.55 ms                                                | 10.6 ms: 1.11x slower                                                            |
| sympy_integrate            | 21.4 ms                                                | 23.9 ms: 1.12x slower                                                            |
| docutils                   | 2.77 sec                                               | 3.09 sec: 1.12x slower                                                           |
| crypto_pyaes               | 81.9 ms                                                | 92.5 ms: 1.13x slower                                                            |
| pidigits                   | 187 ms                                                 | 212 ms: 1.13x slower                                                             |
| deltablue                  | 3.72 ms                                                | 4.21 ms: 1.13x slower                                                            |
| sqlglot_normalize          | 110 ms                                                 | 125 ms: 1.13x slower                                                             |
| sympy_expand               | 478 ms                                                 | 550 ms: 1.15x slower                                                             |
| mako                       | 11.9 ms                                                | 13.7 ms: 1.15x slower                                                            |
| sqlglot_optimize           | 54.8 ms                                                | 63.5 ms: 1.16x slower                                                            |
| chaos                      | 67.0 ms                                                | 78.9 ms: 1.18x slower                                                            |
| django_template            | 34.6 ms                                                | 40.9 ms: 1.18x slower                                                            |
| fannkuch                   | 417 ms                                                 | 498 ms: 1.19x slower                                                             |
| scimark_fft                | 382 ms                                                 | 460 ms: 1.20x slower                                                             |
| scimark_monte_carlo        | 75.1 ms                                                | 90.5 ms: 1.20x slower                                                            |
| create_gc_cycles           | 1.48 ms                                                | 1.78 ms: 1.21x slower                                                            |
| richards_super             | 51.5 ms                                                | 62.3 ms: 1.21x slower                                                            |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 6.12 ms: 1.21x slower                                                            |
| richards                   | 45.8 ms                                                | 55.6 ms: 1.21x slower                                                            |
| scimark_sor                | 129 ms                                                 | 157 ms: 1.22x slower                                                             |
| regex_compile              | 148 ms                                                 | 182 ms: 1.22x slower                                                             |
| pprint_safe_repr           | 776 ms                                                 | 952 ms: 1.23x slower                                                             |
| pyflate                    | 482 ms                                                 | 595 ms: 1.23x slower                                                             |
| spectral_norm              | 115 ms                                                 | 142 ms: 1.24x slower                                                             |
| unpickle_pure_python       | 230 us                                                 | 286 us: 1.24x slower                                                             |
| pprint_pformat             | 1.57 sec                                               | 1.97 sec: 1.26x slower                                                           |
| nbody                      | 97.0 ms                                                | 123 ms: 1.27x slower                                                             |
| nqueens                    | 83.3 ms                                                | 108 ms: 1.29x slower                                                             |
| telco                      | 7.10 ms                                                | 9.30 ms: 1.31x slower                                                            |
| coverage                   | 72.7 ms                                                | 97.3 ms: 1.34x slower                                                            |
| go                         | 139 ms                                                 | 193 ms: 1.38x slower                                                             |
| scimark_lu                 | 118 ms                                                 | 168 ms: 1.42x slower                                                             |
| hexiom                     | 6.41 ms                                                | 9.53 ms: 1.49x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.07x slower                                                                     |

Benchmark hidden because not significant (7): mypy2, unpickle, pickle_dict, bench_mp_pool, deepcopy_reduce, tornado_http, json
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240423-3.13.0a6+-250c073-PYTHON_UOPS/bm-20240423-linux-x86_64-faster%2dcpython-function_entry_enter-3.13.0a6+-250c073.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 0.98x