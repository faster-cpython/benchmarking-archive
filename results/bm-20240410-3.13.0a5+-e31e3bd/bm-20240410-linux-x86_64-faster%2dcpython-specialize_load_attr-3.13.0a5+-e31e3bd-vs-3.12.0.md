# Results vs. 3.12.0

- fork: faster-cpython
- ref: specialize_load_attr
- machine: linux-x86_64
- commit hash: e31e3bd
- commit date: 2024-04-10
- overall geometric mean: 1.04x faster
- HPT reliability: 99.85%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 273 ms: 1.01x faster                                                             |
| chameleon      | 7.41 ms                                                | 7.05 ms: 1.05x faster                                                            |
| docutils       | 2.77 sec                                               | 2.83 sec: 1.02x slower                                                           |
| tornado_http   | 103 ms                                                 | 93.9 ms: 1.09x faster                                                            |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                                             |
| async_tree_none            | 472 ms                                                 | 352 ms: 1.34x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 441 ms: 1.30x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 936 ms: 1.26x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 463 ms: 1.25x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 928 ms: 1.25x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 605 ms: 1.20x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 612 ms: 1.19x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 88.2 ms: 1.10x faster                                                            |
| float          | 84.7 ms                                                | 78.6 ms: 1.08x faster                                                            |
| pidigits       | 187 ms                                                 | 190 ms: 1.01x slower                                                             |
| Geometric mean | (ref)                                                  | 1.05x faster                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 137 ms: 1.09x faster                                                             |
| regex_effbot   | 3.61 ms                                                | 3.75 ms: 1.04x slower                                                            |
| regex_dna      | 212 ms                                                 | 225 ms: 1.06x slower                                                             |
| regex_v8       | 23.1 ms                                                | 25.8 ms: 1.11x slower                                                            |
| Geometric mean | (ref)                                                  | 1.03x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pickle_dict          | 35.5 us                                                | 32.1 us: 1.11x faster                                                            |
| tomli_loads          | 2.33 sec                                               | 2.17 sec: 1.07x faster                                                           |
| pickle_pure_python   | 324 us                                                 | 304 us: 1.07x faster                                                             |
| pickle_list          | 5.08 us                                                | 4.92 us: 1.03x faster                                                            |
| xml_etree_process    | 61.7 ms                                                | 60.6 ms: 1.02x faster                                                            |
| xml_etree_generate   | 89.2 ms                                                | 88.0 ms: 1.01x faster                                                            |
| unpickle_pure_python | 230 us                                                 | 228 us: 1.01x faster                                                             |
| xml_etree_iterparse  | 107 ms                                                 | 108 ms: 1.01x slower                                                             |
| json_loads           | 28.5 us                                                | 28.8 us: 1.01x slower                                                            |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                            |
| pickle               | 11.6 us                                                | 11.9 us: 1.03x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                     |

Benchmark hidden because not significant (3): unpickle_list, xml_etree_parse, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| python_startup_no_site | 6.94 ms                                                | 8.93 ms: 1.29x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.19x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|-----------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| mako      | 11.9 ms                                                | 11.1 ms: 1.07x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 117 us: 1.35x faster                                                             |
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                                             |
| async_tree_none            | 472 ms                                                 | 352 ms: 1.34x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 441 ms: 1.30x faster                                                             |
| comprehensions             | 21.8 us                                                | 16.9 us: 1.28x faster                                                            |
| async_tree_io_tg           | 1.18 sec                                               | 936 ms: 1.26x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 463 ms: 1.25x faster                                                             |
| async_tree_io              | 1.16 sec                                               | 928 ms: 1.25x faster                                                             |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 605 ms: 1.20x faster                                                             |
| raytrace                   | 312 ms                                                 | 262 ms: 1.19x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 612 ms: 1.19x faster                                                             |
| deltablue                  | 3.72 ms                                                | 3.29 ms: 1.13x faster                                                            |
| mypy2                      | 830 ms                                                 | 740 ms: 1.12x faster                                                             |
| logging_format             | 7.23 us                                                | 6.49 us: 1.11x faster                                                            |
| scimark_monte_carlo        | 75.1 ms                                                | 67.8 ms: 1.11x faster                                                            |
| chaos                      | 67.0 ms                                                | 60.5 ms: 1.11x faster                                                            |
| pickle_dict                | 35.5 us                                                | 32.1 us: 1.11x faster                                                            |
| crypto_pyaes               | 81.9 ms                                                | 74.0 ms: 1.11x faster                                                            |
| logging_simple             | 6.46 us                                                | 5.86 us: 1.10x faster                                                            |
| nbody                      | 97.0 ms                                                | 88.2 ms: 1.10x faster                                                            |
| tornado_http               | 103 ms                                                 | 93.9 ms: 1.09x faster                                                            |
| regex_compile              | 148 ms                                                 | 137 ms: 1.09x faster                                                             |
| sympy_sum                  | 169 ms                                                 | 157 ms: 1.08x faster                                                             |
| float                      | 84.7 ms                                                | 78.6 ms: 1.08x faster                                                            |
| tomli_loads                | 2.33 sec                                               | 2.17 sec: 1.07x faster                                                           |
| mako                       | 11.9 ms                                                | 11.1 ms: 1.07x faster                                                            |
| pickle_pure_python         | 324 us                                                 | 304 us: 1.07x faster                                                             |
| fannkuch                   | 417 ms                                                 | 392 ms: 1.06x faster                                                             |
| sympy_str                  | 300 ms                                                 | 282 ms: 1.06x faster                                                             |
| sqlglot_transpile          | 1.68 ms                                                | 1.60 ms: 1.05x faster                                                            |
| chameleon                  | 7.41 ms                                                | 7.05 ms: 1.05x faster                                                            |
| sqlglot_parse              | 1.36 ms                                                | 1.30 ms: 1.05x faster                                                            |
| deepcopy_memo              | 40.7 us                                                | 38.9 us: 1.05x faster                                                            |
| sympy_integrate            | 21.4 ms                                                | 20.5 ms: 1.04x faster                                                            |
| async_generators           | 463 ms                                                 | 444 ms: 1.04x faster                                                             |
| deepcopy_reduce            | 3.35 us                                                | 3.22 us: 1.04x faster                                                            |
| scimark_sor                | 129 ms                                                 | 124 ms: 1.04x faster                                                             |
| deepcopy                   | 371 us                                                 | 358 us: 1.04x faster                                                             |
| coroutines                 | 23.2 ms                                                | 22.4 ms: 1.04x faster                                                            |
| pickle_list                | 5.08 us                                                | 4.92 us: 1.03x faster                                                            |
| spectral_norm              | 115 ms                                                 | 112 ms: 1.03x faster                                                             |
| pathlib                    | 19.3 ms                                                | 18.8 ms: 1.03x faster                                                            |
| scimark_fft                | 382 ms                                                 | 372 ms: 1.03x faster                                                             |
| pprint_safe_repr           | 776 ms                                                 | 756 ms: 1.03x faster                                                             |
| dulwich_log                | 68.5 ms                                                | 67.1 ms: 1.02x faster                                                            |
| xml_etree_process          | 61.7 ms                                                | 60.6 ms: 1.02x faster                                                            |
| generators                 | 31.2 ms                                                | 30.7 ms: 1.02x faster                                                            |
| pprint_pformat             | 1.57 sec                                               | 1.54 sec: 1.02x faster                                                           |
| meteor_contest             | 112 ms                                                 | 111 ms: 1.02x faster                                                             |
| xml_etree_generate         | 89.2 ms                                                | 88.0 ms: 1.01x faster                                                            |
| gc_traversal               | 3.79 ms                                                | 3.75 ms: 1.01x faster                                                            |
| unpickle_pure_python       | 230 us                                                 | 228 us: 1.01x faster                                                             |
| pycparser                  | 1.18 sec                                               | 1.17 sec: 1.01x faster                                                           |
| sympy_expand               | 478 ms                                                 | 474 ms: 1.01x faster                                                             |
| nqueens                    | 83.3 ms                                                | 82.7 ms: 1.01x faster                                                            |
| 2to3                       | 274 ms                                                 | 273 ms: 1.01x faster                                                             |
| bench_thread_pool          | 842 us                                                 | 837 us: 1.01x faster                                                             |
| pyflate                    | 482 ms                                                 | 481 ms: 1.00x faster                                                             |
| logging_silent             | 104 ns                                                 | 105 ns: 1.00x slower                                                             |
| xml_etree_iterparse        | 107 ms                                                 | 108 ms: 1.01x slower                                                             |
| json_loads                 | 28.5 us                                                | 28.8 us: 1.01x slower                                                            |
| hexiom                     | 6.41 ms                                                | 6.48 ms: 1.01x slower                                                            |
| sqlglot_optimize           | 54.8 ms                                                | 55.5 ms: 1.01x slower                                                            |
| mdp                        | 2.63 sec                                               | 2.66 sec: 1.01x slower                                                           |
| pidigits                   | 187 ms                                                 | 190 ms: 1.01x slower                                                             |
| json                       | 5.26 ms                                                | 5.33 ms: 1.01x slower                                                            |
| sqlglot_normalize          | 110 ms                                                 | 112 ms: 1.02x slower                                                             |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                            |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.02x slower                                                            |
| docutils                   | 2.77 sec                                               | 2.83 sec: 1.02x slower                                                           |
| gunicorn                   | 1.24 ms                                                | 1.27 ms: 1.02x slower                                                            |
| pickle                     | 11.6 us                                                | 11.9 us: 1.03x slower                                                            |
| go                         | 139 ms                                                 | 144 ms: 1.03x slower                                                             |
| asyncio_websockets         | 551 ms                                                 | 570 ms: 1.03x slower                                                             |
| asyncio_tcp                | 491 ms                                                 | 507 ms: 1.03x slower                                                             |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.85 sec: 1.04x slower                                                           |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.24 ms: 1.04x slower                                                            |
| regex_effbot               | 3.61 ms                                                | 3.75 ms: 1.04x slower                                                            |
| sqlite_synth               | 2.83 us                                                | 2.96 us: 1.04x slower                                                            |
| richards                   | 45.8 ms                                                | 48.0 ms: 1.05x slower                                                            |
| richards_super             | 51.5 ms                                                | 54.0 ms: 1.05x slower                                                            |
| regex_dna                  | 212 ms                                                 | 225 ms: 1.06x slower                                                             |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| regex_v8                   | 23.1 ms                                                | 25.8 ms: 1.11x slower                                                            |
| create_gc_cycles           | 1.48 ms                                                | 1.72 ms: 1.17x slower                                                            |
| telco                      | 7.10 ms                                                | 8.62 ms: 1.21x slower                                                            |
| python_startup_no_site     | 6.94 ms                                                | 8.93 ms: 1.29x slower                                                            |
| coverage                   | 72.7 ms                                                | 97.3 ms: 1.34x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                                     |

Benchmark hidden because not significant (6): dask, bench_mp_pool, unpickle_list, xml_etree_parse, unpickle, scimark_lu
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240410-3.13.0a5+-e31e3bd/bm-20240410-linux-x86_64-faster%2dcpython-specialize_load_attr-3.13.0a5+-e31e3bd.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.85% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.96x