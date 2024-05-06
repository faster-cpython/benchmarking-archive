# Results vs. 3.12.0

- fork: mdboom
- ref: dont_inline
- machine: linux-x86_64
- commit hash: c35ee28
- commit date: 2024-04-04
- overall geometric mean: 1.02x faster
- HPT reliability: 80.24%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 277 ms: 1.01x slower                                          |
| chameleon      | 7.41 ms                                                | 6.86 ms: 1.08x faster                                         |
| docutils       | 2.77 sec                                               | 2.92 sec: 1.06x slower                                        |
| tornado_http   | 103 ms                                                 | 96.1 ms: 1.07x faster                                         |
| Geometric mean | (ref)                                                  | 1.02x faster                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                          |
| async_tree_none            | 472 ms                                                 | 355 ms: 1.33x faster                                          |
| async_tree_memoization_tg  | 575 ms                                                 | 442 ms: 1.30x faster                                          |
| async_tree_io_tg           | 1.18 sec                                               | 938 ms: 1.26x faster                                          |
| async_tree_memoization     | 578 ms                                                 | 458 ms: 1.26x faster                                          |
| async_tree_io              | 1.16 sec                                               | 932 ms: 1.24x faster                                          |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 602 ms: 1.21x faster                                          |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 611 ms: 1.19x faster                                          |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| float          | 84.7 ms                                                | 76.9 ms: 1.10x faster                                         |
| nbody          | 97.0 ms                                                | 91.1 ms: 1.06x faster                                         |
| pidigits       | 187 ms                                                 | 207 ms: 1.10x slower                                          |
| Geometric mean | (ref)                                                  | 1.02x faster                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 147 ms: 1.01x faster                                          |
| regex_effbot   | 3.61 ms                                                | 3.78 ms: 1.05x slower                                         |
| regex_dna      | 212 ms                                                 | 233 ms: 1.10x slower                                          |
| regex_v8       | 23.1 ms                                                | 25.8 ms: 1.12x slower                                         |
| Geometric mean | (ref)                                                  | 1.06x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.07 sec: 1.13x faster                                        |
| pickle_pure_python   | 324 us                                                 | 306 us: 1.06x faster                                          |
| pickle_dict          | 35.5 us                                                | 33.9 us: 1.05x faster                                         |
| xml_etree_process    | 61.7 ms                                                | 59.6 ms: 1.04x faster                                         |
| xml_etree_generate   | 89.2 ms                                                | 86.5 ms: 1.03x faster                                         |
| pickle_list          | 5.08 us                                                | 4.96 us: 1.02x faster                                         |
| json_dumps           | 10.4 ms                                                | 10.4 ms: 1.00x slower                                         |
| pickle               | 11.6 us                                                | 11.7 us: 1.01x slower                                         |
| xml_etree_parse      | 159 ms                                                 | 162 ms: 1.01x slower                                          |
| unpickle             | 15.9 us                                                | 16.2 us: 1.02x slower                                         |
| unpickle_pure_python | 230 us                                                 | 239 us: 1.04x slower                                          |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                  |

Benchmark hidden because not significant (3): xml_etree_iterparse, unpickle_list, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 11.1 ms: 1.16x slower                                         |
| python_startup_no_site | 6.94 ms                                                | 9.52 ms: 1.37x slower                                         |
| Geometric mean         | (ref)                                                  | 1.26x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|-----------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| mako      | 11.9 ms                                                | 10.8 ms: 1.10x faster                                         |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 114 us: 1.38x faster                                          |
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                          |
| async_tree_none            | 472 ms                                                 | 355 ms: 1.33x faster                                          |
| async_tree_memoization_tg  | 575 ms                                                 | 442 ms: 1.30x faster                                          |
| async_tree_io_tg           | 1.18 sec                                               | 938 ms: 1.26x faster                                          |
| async_tree_memoization     | 578 ms                                                 | 458 ms: 1.26x faster                                          |
| async_tree_io              | 1.16 sec                                               | 932 ms: 1.24x faster                                          |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 602 ms: 1.21x faster                                          |
| comprehensions             | 21.8 us                                                | 18.1 us: 1.20x faster                                         |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 611 ms: 1.19x faster                                          |
| tomli_loads                | 2.33 sec                                               | 2.07 sec: 1.13x faster                                        |
| raytrace                   | 312 ms                                                 | 279 ms: 1.12x faster                                          |
| scimark_fft                | 382 ms                                                 | 343 ms: 1.11x faster                                          |
| mako                       | 11.9 ms                                                | 10.8 ms: 1.10x faster                                         |
| float                      | 84.7 ms                                                | 76.9 ms: 1.10x faster                                         |
| logging_format             | 7.23 us                                                | 6.62 us: 1.09x faster                                         |
| scimark_monte_carlo        | 75.1 ms                                                | 68.8 ms: 1.09x faster                                         |
| crypto_pyaes               | 81.9 ms                                                | 75.5 ms: 1.08x faster                                         |
| chaos                      | 67.0 ms                                                | 61.8 ms: 1.08x faster                                         |
| chameleon                  | 7.41 ms                                                | 6.86 ms: 1.08x faster                                         |
| deltablue                  | 3.72 ms                                                | 3.45 ms: 1.08x faster                                         |
| logging_simple             | 6.46 us                                                | 5.99 us: 1.08x faster                                         |
| tornado_http               | 103 ms                                                 | 96.1 ms: 1.07x faster                                         |
| nbody                      | 97.0 ms                                                | 91.1 ms: 1.06x faster                                         |
| pickle_pure_python         | 324 us                                                 | 306 us: 1.06x faster                                          |
| generators                 | 31.2 ms                                                | 29.5 ms: 1.06x faster                                         |
| deepcopy_memo              | 40.7 us                                                | 38.8 us: 1.05x faster                                         |
| pickle_dict                | 35.5 us                                                | 33.9 us: 1.05x faster                                         |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.84 ms: 1.04x faster                                         |
| fannkuch                   | 417 ms                                                 | 401 ms: 1.04x faster                                          |
| deepcopy                   | 371 us                                                 | 358 us: 1.04x faster                                          |
| pprint_safe_repr           | 776 ms                                                 | 748 ms: 1.04x faster                                          |
| xml_etree_process          | 61.7 ms                                                | 59.6 ms: 1.04x faster                                         |
| pprint_pformat             | 1.57 sec                                               | 1.52 sec: 1.03x faster                                        |
| sqlglot_transpile          | 1.68 ms                                                | 1.63 ms: 1.03x faster                                         |
| xml_etree_generate         | 89.2 ms                                                | 86.5 ms: 1.03x faster                                         |
| sqlglot_parse              | 1.36 ms                                                | 1.32 ms: 1.03x faster                                         |
| pickle_list                | 5.08 us                                                | 4.96 us: 1.02x faster                                         |
| pathlib                    | 19.3 ms                                                | 18.9 ms: 1.02x faster                                         |
| deepcopy_reduce            | 3.35 us                                                | 3.27 us: 1.02x faster                                         |
| coroutines                 | 23.2 ms                                                | 22.7 ms: 1.02x faster                                         |
| logging_silent             | 104 ns                                                 | 103 ns: 1.02x faster                                          |
| sympy_str                  | 300 ms                                                 | 295 ms: 1.02x faster                                          |
| sympy_sum                  | 169 ms                                                 | 167 ms: 1.01x faster                                          |
| pyflate                    | 482 ms                                                 | 476 ms: 1.01x faster                                          |
| regex_compile              | 148 ms                                                 | 147 ms: 1.01x faster                                          |
| meteor_contest             | 112 ms                                                 | 112 ms: 1.00x faster                                          |
| json_dumps                 | 10.4 ms                                                | 10.4 ms: 1.00x slower                                         |
| pickle                     | 11.6 us                                                | 11.7 us: 1.01x slower                                         |
| richards                   | 45.8 ms                                                | 46.3 ms: 1.01x slower                                         |
| 2to3                       | 274 ms                                                 | 277 ms: 1.01x slower                                          |
| xml_etree_parse            | 159 ms                                                 | 162 ms: 1.01x slower                                          |
| sqlite_synth               | 2.83 us                                                | 2.88 us: 1.01x slower                                         |
| bench_thread_pool          | 842 us                                                 | 858 us: 1.02x slower                                          |
| json                       | 5.26 ms                                                | 5.36 ms: 1.02x slower                                         |
| sympy_integrate            | 21.4 ms                                                | 21.9 ms: 1.02x slower                                         |
| richards_super             | 51.5 ms                                                | 52.7 ms: 1.02x slower                                         |
| unpickle                   | 15.9 us                                                | 16.2 us: 1.02x slower                                         |
| sqlglot_normalize          | 110 ms                                                 | 113 ms: 1.02x slower                                          |
| asyncio_websockets         | 551 ms                                                 | 566 ms: 1.03x slower                                          |
| pycparser                  | 1.18 sec                                               | 1.21 sec: 1.03x slower                                        |
| sympy_expand               | 478 ms                                                 | 493 ms: 1.03x slower                                          |
| dulwich_log                | 68.5 ms                                                | 70.9 ms: 1.03x slower                                         |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                        |
| unpickle_pure_python       | 230 us                                                 | 239 us: 1.04x slower                                          |
| regex_effbot               | 3.61 ms                                                | 3.78 ms: 1.05x slower                                         |
| asyncio_tcp                | 491 ms                                                 | 515 ms: 1.05x slower                                          |
| scimark_sor                | 129 ms                                                 | 136 ms: 1.05x slower                                          |
| gunicorn                   | 1.24 ms                                                | 1.31 ms: 1.05x slower                                         |
| sqlglot_optimize           | 54.8 ms                                                | 57.7 ms: 1.05x slower                                         |
| aiohttp                    | 1.15 ms                                                | 1.21 ms: 1.05x slower                                         |
| docutils                   | 2.77 sec                                               | 2.92 sec: 1.06x slower                                        |
| mdp                        | 2.63 sec                                               | 2.83 sec: 1.07x slower                                        |
| regex_dna                  | 212 ms                                                 | 233 ms: 1.10x slower                                          |
| pidigits                   | 187 ms                                                 | 207 ms: 1.10x slower                                          |
| nqueens                    | 83.3 ms                                                | 92.2 ms: 1.11x slower                                         |
| hexiom                     | 6.41 ms                                                | 7.10 ms: 1.11x slower                                         |
| go                         | 139 ms                                                 | 154 ms: 1.11x slower                                          |
| regex_v8                   | 23.1 ms                                                | 25.8 ms: 1.12x slower                                         |
| scimark_lu                 | 118 ms                                                 | 133 ms: 1.13x slower                                          |
| python_startup             | 9.55 ms                                                | 11.1 ms: 1.16x slower                                         |
| create_gc_cycles           | 1.48 ms                                                | 1.75 ms: 1.19x slower                                         |
| telco                      | 7.10 ms                                                | 8.49 ms: 1.20x slower                                         |
| python_startup_no_site     | 6.94 ms                                                | 9.52 ms: 1.37x slower                                         |
| coverage                   | 72.7 ms                                                | 100 ms: 1.38x slower                                          |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                  |

Benchmark hidden because not significant (9): mypy2, async_generators, xml_etree_iterparse, gc_traversal, unpickle_list, bench_mp_pool, json_loads, spectral_norm, dask
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240404-3.13.0a5+-c35ee28-JIT/bm-20240404-linux-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 80.24% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x