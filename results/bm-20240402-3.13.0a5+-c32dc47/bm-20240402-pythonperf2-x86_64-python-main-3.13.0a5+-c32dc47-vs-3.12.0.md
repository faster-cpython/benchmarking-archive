# Results vs. 3.12.0

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: c32dc47
- commit date: 2024-04-02
- overall geometric mean: 1.01x faster
- HPT reliability: 94.64%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.91x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 288 ms: 1.01x slower                                         |
| chameleon      | 7.23 ms                                                      | 7.15 ms: 1.01x faster                                        |
| docutils       | 2.87 sec                                                     | 2.97 sec: 1.04x slower                                       |
| Geometric mean | (ref)                                                        | 1.01x slower                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_memoization_tg  | 540 ms                                                       | 413 ms: 1.31x faster                                         |
| async_tree_none_tg         | 431 ms                                                       | 334 ms: 1.29x faster                                         |
| async_tree_none            | 452 ms                                                       | 363 ms: 1.24x faster                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 854 ms: 1.23x faster                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 573 ms: 1.22x faster                                         |
| async_tree_memoization     | 544 ms                                                       | 457 ms: 1.19x faster                                         |
| async_tree_io              | 1.04 sec                                                     | 883 ms: 1.18x faster                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 607 ms: 1.15x faster                                         |
| Geometric mean             | (ref)                                                        | 1.22x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| nbody          | 88.0 ms                                                      | 85.3 ms: 1.03x faster                                        |
| float          | 76.6 ms                                                      | 75.3 ms: 1.02x faster                                        |
| pidigits       | 265 ms                                                       | 263 ms: 1.01x faster                                         |
| Geometric mean | (ref)                                                        | 1.02x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_dna      | 239 ms                                                       | 230 ms: 1.04x faster                                         |
| regex_compile  | 144 ms                                                       | 141 ms: 1.02x faster                                         |
| regex_effbot   | 3.57 ms                                                      | 3.56 ms: 1.00x faster                                        |
| regex_v8       | 23.6 ms                                                      | 25.7 ms: 1.09x slower                                        |
| Geometric mean | (ref)                                                        | 1.01x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| xml_etree_generate   | 86.1 ms                                                      | 82.4 ms: 1.05x faster                                        |
| pickle_pure_python   | 318 us                                                       | 305 us: 1.04x faster                                         |
| xml_etree_process    | 58.4 ms                                                      | 57.5 ms: 1.02x faster                                        |
| xml_etree_parse      | 144 ms                                                       | 142 ms: 1.01x faster                                         |
| unpickle_list        | 4.66 us                                                      | 4.62 us: 1.01x faster                                        |
| unpickle_pure_python | 210 us                                                       | 210 us: 1.00x slower                                         |
| unpickle             | 14.8 us                                                      | 14.9 us: 1.01x slower                                        |
| xml_etree_iterparse  | 103 ms                                                       | 104 ms: 1.01x slower                                         |
| tomli_loads          | 2.16 sec                                                     | 2.19 sec: 1.02x slower                                       |
| pickle_dict          | 32.5 us                                                      | 33.1 us: 1.02x slower                                        |
| pickle_list          | 4.43 us                                                      | 4.53 us: 1.02x slower                                        |
| json_dumps           | 10.2 ms                                                      | 10.5 ms: 1.02x slower                                        |
| json_loads           | 24.4 us                                                      | 25.6 us: 1.05x slower                                        |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                 |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 12.9 ms: 1.11x slower                                        |
| python_startup_no_site | 8.64 ms                                                      | 11.1 ms: 1.29x slower                                        |
| Geometric mean         | (ref)                                                        | 1.20x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|-----------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| mako      | 10.0 ms                                                      | 10.3 ms: 1.03x slower                                        |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| typing_runtime_protocols   | 152 us                                                       | 114 us: 1.33x faster                                         |
| async_tree_memoization_tg  | 540 ms                                                       | 413 ms: 1.31x faster                                         |
| comprehensions             | 21.9 us                                                      | 16.8 us: 1.30x faster                                        |
| async_tree_none_tg         | 431 ms                                                       | 334 ms: 1.29x faster                                         |
| async_tree_none            | 452 ms                                                       | 363 ms: 1.24x faster                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 854 ms: 1.23x faster                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 573 ms: 1.22x faster                                         |
| async_tree_memoization     | 544 ms                                                       | 457 ms: 1.19x faster                                         |
| raytrace                   | 298 ms                                                       | 251 ms: 1.19x faster                                         |
| async_tree_io              | 1.04 sec                                                     | 883 ms: 1.18x faster                                         |
| unpack_sequence            | 53.2 ns                                                      | 45.9 ns: 1.16x faster                                        |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 607 ms: 1.15x faster                                         |
| generators                 | 37.4 ms                                                      | 33.1 ms: 1.13x faster                                        |
| crypto_pyaes               | 80.3 ms                                                      | 72.4 ms: 1.11x faster                                        |
| async_generators           | 390 ms                                                       | 356 ms: 1.10x faster                                         |
| chaos                      | 64.0 ms                                                      | 58.6 ms: 1.09x faster                                        |
| bench_thread_pool          | 950 us                                                       | 880 us: 1.08x faster                                         |
| mypy2                      | 830 ms                                                       | 771 ms: 1.08x faster                                         |
| scimark_monte_carlo        | 69.0 ms                                                      | 64.4 ms: 1.07x faster                                        |
| bench_mp_pool              | 4.76 ms                                                      | 4.47 ms: 1.06x faster                                        |
| sympy_sum                  | 162 ms                                                       | 153 ms: 1.06x faster                                         |
| scimark_lu                 | 98.8 ms                                                      | 93.7 ms: 1.05x faster                                        |
| xml_etree_generate         | 86.1 ms                                                      | 82.4 ms: 1.05x faster                                        |
| pickle_pure_python         | 318 us                                                       | 305 us: 1.04x faster                                         |
| sympy_str                  | 302 ms                                                       | 291 ms: 1.04x faster                                         |
| pprint_safe_repr           | 807 ms                                                       | 780 ms: 1.04x faster                                         |
| regex_dna                  | 239 ms                                                       | 230 ms: 1.04x faster                                         |
| sqlite_synth               | 2.77 us                                                      | 2.68 us: 1.03x faster                                        |
| nbody                      | 88.0 ms                                                      | 85.3 ms: 1.03x faster                                        |
| pprint_pformat             | 1.65 sec                                                     | 1.60 sec: 1.03x faster                                       |
| sympy_integrate            | 23.9 ms                                                      | 23.2 ms: 1.03x faster                                        |
| mdp                        | 2.57 sec                                                     | 2.51 sec: 1.02x faster                                       |
| regex_compile              | 144 ms                                                       | 141 ms: 1.02x faster                                         |
| nqueens                    | 89.9 ms                                                      | 88.0 ms: 1.02x faster                                        |
| asyncio_tcp                | 378 ms                                                       | 371 ms: 1.02x faster                                         |
| sqlglot_transpile          | 1.78 ms                                                      | 1.74 ms: 1.02x faster                                        |
| coroutines                 | 23.0 ms                                                      | 22.6 ms: 1.02x faster                                        |
| float                      | 76.6 ms                                                      | 75.3 ms: 1.02x faster                                        |
| meteor_contest             | 128 ms                                                       | 126 ms: 1.02x faster                                         |
| xml_etree_process          | 58.4 ms                                                      | 57.5 ms: 1.02x faster                                        |
| xml_etree_parse            | 144 ms                                                       | 142 ms: 1.01x faster                                         |
| sqlglot_parse              | 1.38 ms                                                      | 1.36 ms: 1.01x faster                                        |
| logging_simple             | 6.71 us                                                      | 6.62 us: 1.01x faster                                        |
| deepcopy_memo              | 36.8 us                                                      | 36.3 us: 1.01x faster                                        |
| chameleon                  | 7.23 ms                                                      | 7.15 ms: 1.01x faster                                        |
| pycparser                  | 1.23 sec                                                     | 1.22 sec: 1.01x faster                                       |
| logging_format             | 7.48 us                                                      | 7.41 us: 1.01x faster                                        |
| pidigits                   | 265 ms                                                       | 263 ms: 1.01x faster                                         |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.01x faster                                       |
| unpickle_list              | 4.66 us                                                      | 4.62 us: 1.01x faster                                        |
| logging_silent             | 94.4 ns                                                      | 93.8 ns: 1.01x faster                                        |
| deepcopy_reduce            | 3.37 us                                                      | 3.35 us: 1.01x faster                                        |
| regex_effbot               | 3.57 ms                                                      | 3.56 ms: 1.00x faster                                        |
| unpickle_pure_python       | 210 us                                                       | 210 us: 1.00x slower                                         |
| unpickle                   | 14.8 us                                                      | 14.9 us: 1.01x slower                                        |
| sqlglot_normalize          | 116 ms                                                       | 117 ms: 1.01x slower                                         |
| spectral_norm              | 91.6 ms                                                      | 92.3 ms: 1.01x slower                                        |
| xml_etree_iterparse        | 103 ms                                                       | 104 ms: 1.01x slower                                         |
| 2to3                       | 285 ms                                                       | 288 ms: 1.01x slower                                         |
| sqlglot_optimize           | 57.5 ms                                                      | 58.2 ms: 1.01x slower                                        |
| pathlib                    | 18.9 ms                                                      | 19.2 ms: 1.01x slower                                        |
| sympy_expand               | 484 ms                                                       | 491 ms: 1.01x slower                                         |
| tomli_loads                | 2.16 sec                                                     | 2.19 sec: 1.02x slower                                       |
| pickle_dict                | 32.5 us                                                      | 33.1 us: 1.02x slower                                        |
| asyncio_websockets         | 387 ms                                                       | 395 ms: 1.02x slower                                         |
| pickle_list                | 4.43 us                                                      | 4.53 us: 1.02x slower                                        |
| json_dumps                 | 10.2 ms                                                      | 10.5 ms: 1.02x slower                                        |
| mako                       | 10.0 ms                                                      | 10.3 ms: 1.03x slower                                        |
| gunicorn                   | 1.00 ms                                                      | 1.04 ms: 1.04x slower                                        |
| docutils                   | 2.87 sec                                                     | 2.97 sec: 1.04x slower                                       |
| deltablue                  | 3.24 ms                                                      | 3.39 ms: 1.05x slower                                        |
| aiohttp                    | 1.02 ms                                                      | 1.07 ms: 1.05x slower                                        |
| json_loads                 | 24.4 us                                                      | 25.6 us: 1.05x slower                                        |
| dulwich_log                | 65.4 ms                                                      | 69.0 ms: 1.05x slower                                        |
| fannkuch                   | 350 ms                                                       | 371 ms: 1.06x slower                                         |
| hexiom                     | 5.96 ms                                                      | 6.38 ms: 1.07x slower                                        |
| regex_v8                   | 23.6 ms                                                      | 25.7 ms: 1.09x slower                                        |
| json                       | 5.12 ms                                                      | 5.58 ms: 1.09x slower                                        |
| richards                   | 45.7 ms                                                      | 50.1 ms: 1.09x slower                                        |
| richards_super             | 51.3 ms                                                      | 57.0 ms: 1.11x slower                                        |
| python_startup             | 11.6 ms                                                      | 12.9 ms: 1.11x slower                                        |
| go                         | 150 ms                                                       | 170 ms: 1.14x slower                                         |
| pyflate                    | 439 ms                                                       | 500 ms: 1.14x slower                                         |
| telco                      | 6.96 ms                                                      | 8.04 ms: 1.15x slower                                        |
| create_gc_cycles           | 1.59 ms                                                      | 1.94 ms: 1.22x slower                                        |
| coverage                   | 66.7 ms                                                      | 81.9 ms: 1.23x slower                                        |
| python_startup_no_site     | 8.64 ms                                                      | 11.1 ms: 1.29x slower                                        |
| scimark_sor                | 109 ms                                                       | 142 ms: 1.30x slower                                         |
| gc_traversal               | 3.48 ms                                                      | 4.64 ms: 1.33x slower                                        |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                 |

Benchmark hidden because not significant (6): tornado_http, deepcopy, dask, scimark_fft, pickle, scimark_sparse_mat_mult
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240402-3.13.0a5+-c32dc47/bm-20240402-pythonperf2-x86_64-python-main-3.13.0a5+-c32dc47.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 94.64% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.91x