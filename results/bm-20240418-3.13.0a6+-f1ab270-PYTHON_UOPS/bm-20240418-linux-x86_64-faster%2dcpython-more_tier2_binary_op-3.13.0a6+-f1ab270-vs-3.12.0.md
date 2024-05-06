# Results vs. 3.12.0

- fork: faster-cpython
- ref: more_tier2_binary_op
- machine: linux-x86_64
- commit hash: f1ab270
- commit date: 2024-04-18
- overall geometric mean: 1.20x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 330 ms: 1.20x slower                                                             |
| chameleon      | 7.41 ms                                                | 8.18 ms: 1.10x slower                                                            |
| docutils       | 2.77 sec                                               | 3.27 sec: 1.18x slower                                                           |
| Geometric mean | (ref)                                                  | 1.12x slower                                                                     |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 371 ms: 1.21x faster                                                             |
| async_tree_none            | 472 ms                                                 | 397 ms: 1.19x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 485 ms: 1.19x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 1.02 sec: 1.16x faster                                                           |
| async_tree_io              | 1.16 sec                                               | 1.01 sec: 1.15x faster                                                           |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 651 ms: 1.12x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 661 ms: 1.10x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 530 ms: 1.09x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.15x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                 | 202 ms: 1.08x slower                                                             |
| float          | 84.7 ms                                                | 135 ms: 1.59x slower                                                             |
| nbody          | 97.0 ms                                                | 209 ms: 2.15x slower                                                             |
| Geometric mean | (ref)                                                  | 1.55x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_dna      | 212 ms                                                 | 226 ms: 1.06x slower                                                             |
| regex_v8       | 23.1 ms                                                | 25.8 ms: 1.11x slower                                                            |
| regex_compile  | 148 ms                                                 | 220 ms: 1.48x slower                                                             |
| Geometric mean | (ref)                                                  | 1.15x slower                                                                     |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| unpickle_list        | 5.29 us                                                | 5.08 us: 1.04x faster                                                            |
| pickle_dict          | 35.5 us                                                | 34.4 us: 1.03x faster                                                            |
| xml_etree_parse      | 159 ms                                                 | 154 ms: 1.03x faster                                                             |
| pickle_pure_python   | 324 us                                                 | 316 us: 1.02x faster                                                             |
| pickle_list          | 5.08 us                                                | 4.97 us: 1.02x faster                                                            |
| json_loads           | 28.5 us                                                | 27.9 us: 1.02x faster                                                            |
| pickle               | 11.6 us                                                | 11.7 us: 1.01x slower                                                            |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                            |
| unpickle             | 15.9 us                                                | 17.0 us: 1.07x slower                                                            |
| xml_etree_process    | 61.7 ms                                                | 70.8 ms: 1.15x slower                                                            |
| xml_etree_generate   | 89.2 ms                                                | 104 ms: 1.17x slower                                                             |
| xml_etree_iterparse  | 107 ms                                                 | 130 ms: 1.22x slower                                                             |
| tomli_loads          | 2.33 sec                                               | 3.52 sec: 1.51x slower                                                           |
| unpickle_pure_python | 230 us                                                 | 404 us: 1.76x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.12 ms: 1.03x slower                                                            |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| django_template | 34.6 ms                                                | 43.3 ms: 1.25x slower                                                            |
| mako            | 11.9 ms                                                | 21.1 ms: 1.78x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.49x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 130 us: 1.21x faster                                                             |
| async_tree_none_tg         | 450 ms                                                 | 371 ms: 1.21x faster                                                             |
| async_tree_none            | 472 ms                                                 | 397 ms: 1.19x faster                                                             |
| async_tree_memoization_tg  | 575 ms                                                 | 485 ms: 1.19x faster                                                             |
| async_tree_io_tg           | 1.18 sec                                               | 1.02 sec: 1.16x faster                                                           |
| async_tree_io              | 1.16 sec                                               | 1.01 sec: 1.15x faster                                                           |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 651 ms: 1.12x faster                                                             |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 661 ms: 1.10x faster                                                             |
| async_tree_memoization     | 578 ms                                                 | 530 ms: 1.09x faster                                                             |
| generators                 | 31.2 ms                                                | 29.7 ms: 1.05x faster                                                            |
| pathlib                    | 19.3 ms                                                | 18.5 ms: 1.05x faster                                                            |
| unpickle_list              | 5.29 us                                                | 5.08 us: 1.04x faster                                                            |
| pickle_dict                | 35.5 us                                                | 34.4 us: 1.03x faster                                                            |
| xml_etree_parse            | 159 ms                                                 | 154 ms: 1.03x faster                                                             |
| coroutines                 | 23.2 ms                                                | 22.5 ms: 1.03x faster                                                            |
| pickle_pure_python         | 324 us                                                 | 316 us: 1.02x faster                                                             |
| pickle_list                | 5.08 us                                                | 4.97 us: 1.02x faster                                                            |
| json_loads                 | 28.5 us                                                | 27.9 us: 1.02x faster                                                            |
| json                       | 5.26 ms                                                | 5.16 ms: 1.02x faster                                                            |
| pickle                     | 11.6 us                                                | 11.7 us: 1.01x slower                                                            |
| deepcopy_reduce            | 3.35 us                                                | 3.39 us: 1.01x slower                                                            |
| logging_simple             | 6.46 us                                                | 6.58 us: 1.02x slower                                                            |
| logging_format             | 7.23 us                                                | 7.39 us: 1.02x slower                                                            |
| python_startup_no_site     | 6.94 ms                                                | 7.12 ms: 1.03x slower                                                            |
| gc_traversal               | 3.79 ms                                                | 3.90 ms: 1.03x slower                                                            |
| asyncio_websockets         | 551 ms                                                 | 567 ms: 1.03x slower                                                             |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                            |
| dask                       | 372 ms                                                 | 388 ms: 1.04x slower                                                             |
| logging_silent             | 104 ns                                                 | 109 ns: 1.05x slower                                                             |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.87 sec: 1.05x slower                                                           |
| asyncio_tcp                | 491 ms                                                 | 514 ms: 1.05x slower                                                             |
| deepcopy                   | 371 us                                                 | 395 us: 1.06x slower                                                             |
| regex_dna                  | 212 ms                                                 | 226 ms: 1.06x slower                                                             |
| unpickle                   | 15.9 us                                                | 17.0 us: 1.07x slower                                                            |
| gunicorn                   | 1.24 ms                                                | 1.34 ms: 1.08x slower                                                            |
| pidigits                   | 187 ms                                                 | 202 ms: 1.08x slower                                                             |
| async_generators           | 463 ms                                                 | 503 ms: 1.09x slower                                                             |
| aiohttp                    | 1.15 ms                                                | 1.25 ms: 1.09x slower                                                            |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                            |
| bench_thread_pool          | 842 us                                                 | 928 us: 1.10x slower                                                             |
| chameleon                  | 7.41 ms                                                | 8.18 ms: 1.10x slower                                                            |
| dulwich_log                | 68.5 ms                                                | 75.8 ms: 1.11x slower                                                            |
| sqlite_synth               | 2.83 us                                                | 3.15 us: 1.11x slower                                                            |
| regex_v8                   | 23.1 ms                                                | 25.8 ms: 1.11x slower                                                            |
| sympy_sum                  | 169 ms                                                 | 191 ms: 1.13x slower                                                             |
| mdp                        | 2.63 sec                                               | 3.01 sec: 1.14x slower                                                           |
| pycparser                  | 1.18 sec                                               | 1.35 sec: 1.14x slower                                                           |
| xml_etree_process          | 61.7 ms                                                | 70.8 ms: 1.15x slower                                                            |
| sympy_str                  | 300 ms                                                 | 347 ms: 1.16x slower                                                             |
| sympy_expand               | 478 ms                                                 | 556 ms: 1.16x slower                                                             |
| xml_etree_generate         | 89.2 ms                                                | 104 ms: 1.17x slower                                                             |
| sqlglot_transpile          | 1.68 ms                                                | 1.97 ms: 1.17x slower                                                            |
| docutils                   | 2.77 sec                                               | 3.27 sec: 1.18x slower                                                           |
| sympy_integrate            | 21.4 ms                                                | 25.3 ms: 1.18x slower                                                            |
| sqlglot_parse              | 1.36 ms                                                | 1.63 ms: 1.20x slower                                                            |
| 2to3                       | 274 ms                                                 | 330 ms: 1.20x slower                                                             |
| sqlglot_normalize          | 110 ms                                                 | 133 ms: 1.21x slower                                                             |
| raytrace                   | 312 ms                                                 | 378 ms: 1.21x slower                                                             |
| create_gc_cycles           | 1.48 ms                                                | 1.79 ms: 1.21x slower                                                            |
| xml_etree_iterparse        | 107 ms                                                 | 130 ms: 1.22x slower                                                             |
| deepcopy_memo              | 40.7 us                                                | 49.9 us: 1.23x slower                                                            |
| django_template            | 34.6 ms                                                | 43.3 ms: 1.25x slower                                                            |
| sqlglot_optimize           | 54.8 ms                                                | 70.4 ms: 1.28x slower                                                            |
| meteor_contest             | 112 ms                                                 | 145 ms: 1.29x slower                                                             |
| scimark_sor                | 129 ms                                                 | 174 ms: 1.35x slower                                                             |
| deltablue                  | 3.72 ms                                                | 5.02 ms: 1.35x slower                                                            |
| coverage                   | 72.7 ms                                                | 98.5 ms: 1.35x slower                                                            |
| telco                      | 7.10 ms                                                | 9.78 ms: 1.38x slower                                                            |
| regex_compile              | 148 ms                                                 | 220 ms: 1.48x slower                                                             |
| tomli_loads                | 2.33 sec                                               | 3.52 sec: 1.51x slower                                                           |
| chaos                      | 67.0 ms                                                | 103 ms: 1.54x slower                                                             |
| crypto_pyaes               | 81.9 ms                                                | 128 ms: 1.57x slower                                                             |
| richards_super             | 51.5 ms                                                | 81.6 ms: 1.58x slower                                                            |
| float                      | 84.7 ms                                                | 135 ms: 1.59x slower                                                             |
| pprint_safe_repr           | 776 ms                                                 | 1.25 sec: 1.62x slower                                                           |
| go                         | 139 ms                                                 | 229 ms: 1.64x slower                                                             |
| richards                   | 45.8 ms                                                | 75.2 ms: 1.64x slower                                                            |
| scimark_fft                | 382 ms                                                 | 633 ms: 1.66x slower                                                             |
| pprint_pformat             | 1.57 sec                                               | 2.60 sec: 1.66x slower                                                           |
| comprehensions             | 21.8 us                                                | 36.1 us: 1.66x slower                                                            |
| unpickle_pure_python       | 230 us                                                 | 404 us: 1.76x slower                                                             |
| scimark_lu                 | 118 ms                                                 | 208 ms: 1.76x slower                                                             |
| mako                       | 11.9 ms                                                | 21.1 ms: 1.78x slower                                                            |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 9.00 ms: 1.78x slower                                                            |
| pyflate                    | 482 ms                                                 | 878 ms: 1.82x slower                                                             |
| fannkuch                   | 417 ms                                                 | 764 ms: 1.83x slower                                                             |
| nqueens                    | 83.3 ms                                                | 153 ms: 1.83x slower                                                             |
| scimark_monte_carlo        | 75.1 ms                                                | 139 ms: 1.85x slower                                                             |
| spectral_norm              | 115 ms                                                 | 242 ms: 2.11x slower                                                             |
| nbody                      | 97.0 ms                                                | 209 ms: 2.15x slower                                                             |
| hexiom                     | 6.41 ms                                                | 15.1 ms: 2.36x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.20x slower                                                                     |

Benchmark hidden because not significant (4): bench_mp_pool, regex_effbot, mypy2, tornado_http
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240418-3.13.0a6+-f1ab270-PYTHON_UOPS/bm-20240418-linux-x86_64-faster%2dcpython-more_tier2_binary_op-3.13.0a6+-f1ab270.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 0.97x