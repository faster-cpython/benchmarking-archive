# Results vs. 3.12.0

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.04x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 267 ms: 1.03x faster                                                    |
| chameleon      | 7.41 ms                                                | 6.96 ms: 1.06x faster                                                   |
| docutils       | 2.77 sec                                               | 2.80 sec: 1.01x slower                                                  |
| tornado_http   | 103 ms                                                 | 94.4 ms: 1.09x faster                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 330 ms: 1.36x faster                                                    |
| async_tree_none            | 472 ms                                                 | 352 ms: 1.34x faster                                                    |
| async_tree_memoization_tg  | 575 ms                                                 | 436 ms: 1.32x faster                                                    |
| async_tree_io_tg           | 1.18 sec                                               | 935 ms: 1.26x faster                                                    |
| async_tree_io              | 1.16 sec                                               | 917 ms: 1.26x faster                                                    |
| async_tree_memoization     | 578 ms                                                 | 465 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 609 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 615 ms: 1.18x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 97.0 ms                                                | 87.4 ms: 1.11x faster                                                   |
| float          | 84.7 ms                                                | 78.8 ms: 1.07x faster                                                   |
| pidigits       | 187 ms                                                 | 194 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                  | 1.05x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 134 ms: 1.10x faster                                                    |
| regex_effbot   | 3.61 ms                                                | 3.85 ms: 1.07x slower                                                   |
| regex_dna      | 212 ms                                                 | 232 ms: 1.10x slower                                                    |
| regex_v8       | 23.1 ms                                                | 26.3 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                  | 1.05x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.14 sec: 1.09x faster                                                  |
| pickle_pure_python   | 324 us                                                 | 299 us: 1.08x faster                                                    |
| unpickle_pure_python | 230 us                                                 | 213 us: 1.08x faster                                                    |
| unpickle             | 15.9 us                                                | 15.0 us: 1.06x faster                                                   |
| json_loads           | 28.5 us                                                | 27.4 us: 1.04x faster                                                   |
| pickle_dict          | 35.5 us                                                | 34.4 us: 1.03x faster                                                   |
| xml_etree_generate   | 89.2 ms                                                | 86.7 ms: 1.03x faster                                                   |
| xml_etree_process    | 61.7 ms                                                | 60.2 ms: 1.03x faster                                                   |
| unpickle_list        | 5.29 us                                                | 5.19 us: 1.02x faster                                                   |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                   |
| pickle_list          | 5.08 us                                                | 5.21 us: 1.02x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                            |

Benchmark hidden because not significant (3): xml_etree_iterparse, xml_etree_parse, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.11 ms: 1.03x slower                                                   |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.9 ms: 1.09x faster                                                   |
| django_template | 34.6 ms                                                | 34.4 ms: 1.01x faster                                                   |
| Geometric mean  | (ref)                                                  | 1.05x faster                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 330 ms: 1.36x faster                                                    |
| async_tree_none            | 472 ms                                                 | 352 ms: 1.34x faster                                                    |
| async_tree_memoization_tg  | 575 ms                                                 | 436 ms: 1.32x faster                                                    |
| comprehensions             | 21.8 us                                                | 16.9 us: 1.29x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 935 ms: 1.26x faster                                                    |
| async_tree_io              | 1.16 sec                                               | 917 ms: 1.26x faster                                                    |
| async_tree_memoization     | 578 ms                                                 | 465 ms: 1.24x faster                                                    |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 609 ms: 1.19x faster                                                    |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 615 ms: 1.18x faster                                                    |
| raytrace                   | 312 ms                                                 | 267 ms: 1.17x faster                                                    |
| deltablue                  | 3.72 ms                                                | 3.22 ms: 1.15x faster                                                   |
| logging_format             | 7.23 us                                                | 6.42 us: 1.13x faster                                                   |
| mypy2                      | 830 ms                                                 | 737 ms: 1.13x faster                                                    |
| scimark_monte_carlo        | 75.1 ms                                                | 67.2 ms: 1.12x faster                                                   |
| chaos                      | 67.0 ms                                                | 60.3 ms: 1.11x faster                                                   |
| nbody                      | 97.0 ms                                                | 87.4 ms: 1.11x faster                                                   |
| logging_simple             | 6.46 us                                                | 5.83 us: 1.11x faster                                                   |
| regex_compile              | 148 ms                                                 | 134 ms: 1.10x faster                                                    |
| pathlib                    | 19.3 ms                                                | 17.6 ms: 1.10x faster                                                   |
| sympy_sum                  | 169 ms                                                 | 155 ms: 1.09x faster                                                    |
| mako                       | 11.9 ms                                                | 10.9 ms: 1.09x faster                                                   |
| fannkuch                   | 417 ms                                                 | 383 ms: 1.09x faster                                                    |
| tomli_loads                | 2.33 sec                                               | 2.14 sec: 1.09x faster                                                  |
| crypto_pyaes               | 81.9 ms                                                | 75.2 ms: 1.09x faster                                                   |
| tornado_http               | 103 ms                                                 | 94.4 ms: 1.09x faster                                                   |
| logging_silent             | 104 ns                                                 | 96.3 ns: 1.08x faster                                                   |
| sympy_str                  | 300 ms                                                 | 276 ms: 1.08x faster                                                    |
| pickle_pure_python         | 324 us                                                 | 299 us: 1.08x faster                                                    |
| unpickle_pure_python       | 230 us                                                 | 213 us: 1.08x faster                                                    |
| float                      | 84.7 ms                                                | 78.8 ms: 1.07x faster                                                   |
| gc_traversal               | 3.79 ms                                                | 3.55 ms: 1.07x faster                                                   |
| chameleon                  | 7.41 ms                                                | 6.96 ms: 1.06x faster                                                   |
| sympy_integrate            | 21.4 ms                                                | 20.2 ms: 1.06x faster                                                   |
| unpickle                   | 15.9 us                                                | 15.0 us: 1.06x faster                                                   |
| sqlglot_transpile          | 1.68 ms                                                | 1.59 ms: 1.06x faster                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.29 ms: 1.05x faster                                                   |
| async_generators           | 463 ms                                                 | 440 ms: 1.05x faster                                                    |
| generators                 | 31.2 ms                                                | 29.8 ms: 1.05x faster                                                   |
| scimark_fft                | 382 ms                                                 | 365 ms: 1.05x faster                                                    |
| deepcopy                   | 371 us                                                 | 355 us: 1.05x faster                                                    |
| pprint_safe_repr           | 776 ms                                                 | 742 ms: 1.05x faster                                                    |
| hexiom                     | 6.41 ms                                                | 6.15 ms: 1.04x faster                                                   |
| deepcopy_reduce            | 3.35 us                                                | 3.21 us: 1.04x faster                                                   |
| deepcopy_memo              | 40.7 us                                                | 39.1 us: 1.04x faster                                                   |
| pyflate                    | 482 ms                                                 | 464 ms: 1.04x faster                                                    |
| json_loads                 | 28.5 us                                                | 27.4 us: 1.04x faster                                                   |
| scimark_sor                | 129 ms                                                 | 124 ms: 1.04x faster                                                    |
| dulwich_log                | 68.5 ms                                                | 66.0 ms: 1.04x faster                                                   |
| pprint_pformat             | 1.57 sec                                               | 1.52 sec: 1.03x faster                                                  |
| pickle_dict                | 35.5 us                                                | 34.4 us: 1.03x faster                                                   |
| xml_etree_generate         | 89.2 ms                                                | 86.7 ms: 1.03x faster                                                   |
| json                       | 5.26 ms                                                | 5.12 ms: 1.03x faster                                                   |
| xml_etree_process          | 61.7 ms                                                | 60.2 ms: 1.03x faster                                                   |
| 2to3                       | 274 ms                                                 | 267 ms: 1.03x faster                                                    |
| coroutines                 | 23.2 ms                                                | 22.6 ms: 1.02x faster                                                   |
| sympy_expand               | 478 ms                                                 | 467 ms: 1.02x faster                                                    |
| meteor_contest             | 112 ms                                                 | 110 ms: 1.02x faster                                                    |
| nqueens                    | 83.3 ms                                                | 81.6 ms: 1.02x faster                                                   |
| unpickle_list              | 5.29 us                                                | 5.19 us: 1.02x faster                                                   |
| bench_thread_pool          | 842 us                                                 | 829 us: 1.02x faster                                                    |
| sqlglot_normalize          | 110 ms                                                 | 109 ms: 1.01x faster                                                    |
| dask                       | 372 ms                                                 | 367 ms: 1.01x faster                                                    |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                   |
| django_template            | 34.6 ms                                                | 34.4 ms: 1.01x faster                                                   |
| sqlglot_optimize           | 54.8 ms                                                | 54.7 ms: 1.00x faster                                                   |
| spectral_norm              | 115 ms                                                 | 116 ms: 1.01x slower                                                    |
| docutils                   | 2.77 sec                                               | 2.80 sec: 1.01x slower                                                  |
| pycparser                  | 1.18 sec                                               | 1.20 sec: 1.02x slower                                                  |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.02x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                   |
| go                         | 139 ms                                                 | 142 ms: 1.02x slower                                                    |
| gunicorn                   | 1.24 ms                                                | 1.27 ms: 1.02x slower                                                   |
| asyncio_websockets         | 551 ms                                                 | 563 ms: 1.02x slower                                                    |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.17 ms: 1.02x slower                                                   |
| pickle_list                | 5.08 us                                                | 5.21 us: 1.02x slower                                                   |
| python_startup_no_site     | 6.94 ms                                                | 7.11 ms: 1.03x slower                                                   |
| richards                   | 45.8 ms                                                | 47.0 ms: 1.03x slower                                                   |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.84 sec: 1.03x slower                                                  |
| asyncio_tcp                | 491 ms                                                 | 506 ms: 1.03x slower                                                    |
| richards_super             | 51.5 ms                                                | 53.2 ms: 1.03x slower                                                   |
| typing_runtime_protocols   | 158 us                                                 | 163 us: 1.03x slower                                                    |
| pidigits                   | 187 ms                                                 | 194 ms: 1.03x slower                                                    |
| sqlite_synth               | 2.83 us                                                | 2.95 us: 1.04x slower                                                   |
| mdp                        | 2.63 sec                                               | 2.79 sec: 1.06x slower                                                  |
| regex_effbot               | 3.61 ms                                                | 3.85 ms: 1.07x slower                                                   |
| regex_dna                  | 212 ms                                                 | 232 ms: 1.10x slower                                                    |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                   |
| regex_v8                   | 23.1 ms                                                | 26.3 ms: 1.14x slower                                                   |
| create_gc_cycles           | 1.48 ms                                                | 1.75 ms: 1.18x slower                                                   |
| telco                      | 7.10 ms                                                | 8.49 ms: 1.20x slower                                                   |
| coverage                   | 72.7 ms                                                | 98.6 ms: 1.36x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                            |

Benchmark hidden because not significant (4): scimark_lu, xml_etree_iterparse, xml_etree_parse, pickle
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240426-3.13.0a6+-65aa34a/bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 0.96x