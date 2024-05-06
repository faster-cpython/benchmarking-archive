# Results vs. 3.12.0

- fork: mdboom
- ref: dont_inline
- machine: linux-x86_64
- commit hash: c35ee28
- commit date: 2024-04-04
- overall geometric mean: 1.03x slower
- HPT reliability: 99.93%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 298 ms: 1.05x slower                                                |
| chameleon      | 7.23 ms                                                      | 7.46 ms: 1.03x slower                                               |
| docutils       | 2.87 sec                                                     | 3.10 sec: 1.08x slower                                              |
| Geometric mean | (ref)                                                        | 1.04x slower                                                        |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 334 ms: 1.29x faster                                                |
| async_tree_memoization_tg  | 540 ms                                                       | 425 ms: 1.27x faster                                                |
| async_tree_io_tg           | 1.05 sec                                                     | 864 ms: 1.22x faster                                                |
| async_tree_io              | 1.04 sec                                                     | 856 ms: 1.22x faster                                                |
| async_tree_memoization     | 544 ms                                                       | 447 ms: 1.22x faster                                                |
| async_tree_none            | 452 ms                                                       | 379 ms: 1.19x faster                                                |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 592 ms: 1.18x faster                                                |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 610 ms: 1.14x faster                                                |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| float          | 76.6 ms                                                      | 75.0 ms: 1.02x faster                                               |
| pidigits       | 265 ms                                                       | 261 ms: 1.02x faster                                                |
| nbody          | 88.0 ms                                                      | 95.1 ms: 1.08x slower                                               |
| Geometric mean | (ref)                                                        | 1.01x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.52 ms: 1.02x faster                                               |
| regex_dna      | 239 ms                                                       | 241 ms: 1.01x slower                                                |
| regex_compile  | 144 ms                                                       | 148 ms: 1.03x slower                                                |
| regex_v8       | 23.6 ms                                                      | 26.0 ms: 1.10x slower                                               |
| Geometric mean | (ref)                                                        | 1.03x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| xml_etree_generate   | 86.1 ms                                                      | 83.4 ms: 1.03x faster                                               |
| pickle_pure_python   | 318 us                                                       | 309 us: 1.03x faster                                                |
| unpickle_list        | 4.66 us                                                      | 4.54 us: 1.03x faster                                               |
| xml_etree_process    | 58.4 ms                                                      | 57.9 ms: 1.01x faster                                               |
| pickle_dict          | 32.5 us                                                      | 32.7 us: 1.00x slower                                               |
| xml_etree_parse      | 144 ms                                                       | 146 ms: 1.02x slower                                                |
| pickle               | 10.5 us                                                      | 10.7 us: 1.02x slower                                               |
| unpickle             | 14.8 us                                                      | 15.2 us: 1.02x slower                                               |
| json_dumps           | 10.2 ms                                                      | 10.6 ms: 1.03x slower                                               |
| json_loads           | 24.4 us                                                      | 25.5 us: 1.05x slower                                               |
| unpickle_pure_python | 210 us                                                       | 234 us: 1.12x slower                                                |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                        |

Benchmark hidden because not significant (3): pickle_list, tomli_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                               |
| python_startup_no_site | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                               |
| Geometric mean         | (ref)                                                        | 1.26x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|-----------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako      | 10.0 ms                                                      | 9.85 ms: 1.02x faster                                               |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 334 ms: 1.29x faster                                                |
| async_tree_memoization_tg  | 540 ms                                                       | 425 ms: 1.27x faster                                                |
| typing_runtime_protocols   | 152 us                                                       | 120 us: 1.26x faster                                                |
| async_tree_io_tg           | 1.05 sec                                                     | 864 ms: 1.22x faster                                                |
| async_tree_io              | 1.04 sec                                                     | 856 ms: 1.22x faster                                                |
| async_tree_memoization     | 544 ms                                                       | 447 ms: 1.22x faster                                                |
| async_tree_none            | 452 ms                                                       | 379 ms: 1.19x faster                                                |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 592 ms: 1.18x faster                                                |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 610 ms: 1.14x faster                                                |
| comprehensions             | 21.9 us                                                      | 19.5 us: 1.12x faster                                               |
| generators                 | 37.4 ms                                                      | 33.4 ms: 1.12x faster                                               |
| crypto_pyaes               | 80.3 ms                                                      | 76.7 ms: 1.05x faster                                               |
| logging_format             | 7.48 us                                                      | 7.15 us: 1.05x faster                                               |
| sqlite_synth               | 2.77 us                                                      | 2.68 us: 1.04x faster                                               |
| xml_etree_generate         | 86.1 ms                                                      | 83.4 ms: 1.03x faster                                               |
| logging_simple             | 6.71 us                                                      | 6.52 us: 1.03x faster                                               |
| pickle_pure_python         | 318 us                                                       | 309 us: 1.03x faster                                                |
| unpickle_list              | 4.66 us                                                      | 4.54 us: 1.03x faster                                               |
| raytrace                   | 298 ms                                                       | 291 ms: 1.03x faster                                                |
| float                      | 76.6 ms                                                      | 75.0 ms: 1.02x faster                                               |
| asyncio_tcp                | 378 ms                                                       | 370 ms: 1.02x faster                                                |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.13 ms: 1.02x faster                                               |
| mako                       | 10.0 ms                                                      | 9.85 ms: 1.02x faster                                               |
| regex_effbot               | 3.57 ms                                                      | 3.52 ms: 1.02x faster                                               |
| pidigits                   | 265 ms                                                       | 261 ms: 1.02x faster                                                |
| xml_etree_process          | 58.4 ms                                                      | 57.9 ms: 1.01x faster                                               |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.00x faster                                              |
| pickle_dict                | 32.5 us                                                      | 32.7 us: 1.00x slower                                               |
| scimark_monte_carlo        | 69.0 ms                                                      | 69.5 ms: 1.01x slower                                               |
| regex_dna                  | 239 ms                                                       | 241 ms: 1.01x slower                                                |
| mdp                        | 2.57 sec                                                     | 2.59 sec: 1.01x slower                                              |
| sympy_str                  | 302 ms                                                       | 305 ms: 1.01x slower                                                |
| sympy_sum                  | 162 ms                                                       | 164 ms: 1.01x slower                                                |
| asyncio_websockets         | 387 ms                                                       | 393 ms: 1.01x slower                                                |
| xml_etree_parse            | 144 ms                                                       | 146 ms: 1.02x slower                                                |
| sqlglot_parse              | 1.38 ms                                                      | 1.40 ms: 1.02x slower                                               |
| async_generators           | 390 ms                                                       | 397 ms: 1.02x slower                                                |
| deepcopy_reduce            | 3.37 us                                                      | 3.43 us: 1.02x slower                                               |
| pickle                     | 10.5 us                                                      | 10.7 us: 1.02x slower                                               |
| coroutines                 | 23.0 ms                                                      | 23.4 ms: 1.02x slower                                               |
| sqlglot_transpile          | 1.78 ms                                                      | 1.81 ms: 1.02x slower                                               |
| spectral_norm              | 91.6 ms                                                      | 93.7 ms: 1.02x slower                                               |
| unpickle                   | 14.8 us                                                      | 15.2 us: 1.02x slower                                               |
| dask                       | 392 ms                                                       | 403 ms: 1.03x slower                                                |
| regex_compile              | 144 ms                                                       | 148 ms: 1.03x slower                                                |
| chameleon                  | 7.23 ms                                                      | 7.46 ms: 1.03x slower                                               |
| pathlib                    | 18.9 ms                                                      | 19.5 ms: 1.03x slower                                               |
| json_dumps                 | 10.2 ms                                                      | 10.6 ms: 1.03x slower                                               |
| pprint_pformat             | 1.65 sec                                                     | 1.71 sec: 1.03x slower                                              |
| meteor_contest             | 128 ms                                                       | 133 ms: 1.03x slower                                                |
| logging_silent             | 94.4 ns                                                      | 97.8 ns: 1.04x slower                                               |
| pprint_safe_repr           | 807 ms                                                       | 836 ms: 1.04x slower                                                |
| scimark_fft                | 301 ms                                                       | 313 ms: 1.04x slower                                                |
| deepcopy_memo              | 36.8 us                                                      | 38.4 us: 1.04x slower                                               |
| 2to3                       | 285 ms                                                       | 298 ms: 1.05x slower                                                |
| json_loads                 | 24.4 us                                                      | 25.5 us: 1.05x slower                                               |
| bench_mp_pool              | 4.76 ms                                                      | 5.00 ms: 1.05x slower                                               |
| dulwich_log                | 65.4 ms                                                      | 68.7 ms: 1.05x slower                                               |
| deepcopy                   | 368 us                                                       | 390 us: 1.06x slower                                                |
| sympy_expand               | 484 ms                                                       | 513 ms: 1.06x slower                                                |
| sqlglot_normalize          | 116 ms                                                       | 123 ms: 1.06x slower                                                |
| sympy_integrate            | 23.9 ms                                                      | 25.4 ms: 1.06x slower                                               |
| json                       | 5.12 ms                                                      | 5.47 ms: 1.07x slower                                               |
| docutils                   | 2.87 sec                                                     | 3.10 sec: 1.08x slower                                              |
| nbody                      | 88.0 ms                                                      | 95.1 ms: 1.08x slower                                               |
| sqlglot_optimize           | 57.5 ms                                                      | 62.7 ms: 1.09x slower                                               |
| regex_v8                   | 23.6 ms                                                      | 26.0 ms: 1.10x slower                                               |
| fannkuch                   | 350 ms                                                       | 384 ms: 1.10x slower                                                |
| gunicorn                   | 1.00 ms                                                      | 1.10 ms: 1.10x slower                                               |
| aiohttp                    | 1.02 ms                                                      | 1.13 ms: 1.11x slower                                               |
| richards                   | 45.7 ms                                                      | 50.8 ms: 1.11x slower                                               |
| richards_super             | 51.3 ms                                                      | 57.0 ms: 1.11x slower                                               |
| pyflate                    | 439 ms                                                       | 487 ms: 1.11x slower                                                |
| deltablue                  | 3.24 ms                                                      | 3.61 ms: 1.11x slower                                               |
| unpickle_pure_python       | 210 us                                                       | 234 us: 1.12x slower                                                |
| nqueens                    | 89.9 ms                                                      | 103 ms: 1.14x slower                                                |
| telco                      | 6.96 ms                                                      | 8.01 ms: 1.15x slower                                               |
| bench_thread_pool          | 950 us                                                       | 1.10 ms: 1.16x slower                                               |
| python_startup             | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                               |
| go                         | 150 ms                                                       | 175 ms: 1.17x slower                                                |
| create_gc_cycles           | 1.59 ms                                                      | 1.86 ms: 1.17x slower                                               |
| hexiom                     | 5.96 ms                                                      | 7.39 ms: 1.24x slower                                               |
| scimark_lu                 | 98.8 ms                                                      | 124 ms: 1.25x slower                                                |
| gc_traversal               | 3.48 ms                                                      | 4.41 ms: 1.27x slower                                               |
| coverage                   | 66.7 ms                                                      | 86.4 ms: 1.30x slower                                               |
| python_startup_no_site     | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                               |
| scimark_sor                | 109 ms                                                       | 153 ms: 1.40x slower                                                |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                        |

Benchmark hidden because not significant (7): mypy2, chaos, pickle_list, tomli_loads, tornado_http, xml_etree_iterparse, pycparser
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240404-3.13.0a5+-c35ee28-JIT/bm-20240404-pythonperf2-x86_64-mdboom-dont_inline-3.13.0a5+-c35ee28.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.93% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x