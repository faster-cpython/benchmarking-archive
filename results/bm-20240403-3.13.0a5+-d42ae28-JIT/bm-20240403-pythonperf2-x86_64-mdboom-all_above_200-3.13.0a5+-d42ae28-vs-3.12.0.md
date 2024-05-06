# Results vs. 3.12.0

- fork: mdboom
- ref: all_above_200
- machine: linux-x86_64
- commit hash: d42ae28
- commit date: 2024-04-03
- overall geometric mean: 1.03x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 302 ms: 1.06x slower                                                  |
| chameleon      | 7.23 ms                                                      | 7.31 ms: 1.01x slower                                                 |
| docutils       | 2.87 sec                                                     | 3.06 sec: 1.07x slower                                                |
| tornado_http   | 121 ms                                                       | 124 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 339 ms: 1.27x faster                                                  |
| async_tree_memoization_tg  | 540 ms                                                       | 429 ms: 1.26x faster                                                  |
| async_tree_memoization     | 544 ms                                                       | 452 ms: 1.20x faster                                                  |
| async_tree_io_tg           | 1.05 sec                                                     | 879 ms: 1.20x faster                                                  |
| async_tree_none            | 452 ms                                                       | 377 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 592 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 602 ms: 1.16x faster                                                  |
| async_tree_io              | 1.04 sec                                                     | 906 ms: 1.15x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.20x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 264 ms: 1.01x faster                                                  |
| float          | 76.6 ms                                                      | 77.7 ms: 1.01x slower                                                 |
| nbody          | 88.0 ms                                                      | 94.7 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                        | 1.03x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.50 ms: 1.02x faster                                                 |
| regex_dna      | 239 ms                                                       | 247 ms: 1.03x slower                                                  |
| regex_compile  | 144 ms                                                       | 150 ms: 1.04x slower                                                  |
| regex_v8       | 23.6 ms                                                      | 25.9 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 318 us                                                       | 310 us: 1.03x faster                                                  |
| unpickle             | 14.8 us                                                      | 14.6 us: 1.01x faster                                                 |
| unpickle_list        | 4.66 us                                                      | 4.60 us: 1.01x faster                                                 |
| xml_etree_generate   | 86.1 ms                                                      | 85.5 ms: 1.01x faster                                                 |
| xml_etree_process    | 58.4 ms                                                      | 58.9 ms: 1.01x slower                                                 |
| xml_etree_iterparse  | 103 ms                                                       | 104 ms: 1.01x slower                                                  |
| xml_etree_parse      | 144 ms                                                       | 146 ms: 1.01x slower                                                  |
| pickle_dict          | 32.5 us                                                      | 33.1 us: 1.02x slower                                                 |
| tomli_loads          | 2.16 sec                                                     | 2.21 sec: 1.02x slower                                                |
| json_dumps           | 10.2 ms                                                      | 10.7 ms: 1.05x slower                                                 |
| pickle               | 10.5 us                                                      | 11.1 us: 1.06x slower                                                 |
| json_loads           | 24.4 us                                                      | 25.8 us: 1.06x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 241 us: 1.15x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.02x slower                                                          |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 13.6 ms: 1.17x slower                                                 |
| python_startup_no_site | 8.64 ms                                                      | 11.8 ms: 1.37x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.26x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 10.0 ms                                                      | 9.84 ms: 1.02x faster                                                 |
| django_template | 38.2 ms                                                      | 40.1 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 339 ms: 1.27x faster                                                  |
| async_tree_memoization_tg  | 540 ms                                                       | 429 ms: 1.26x faster                                                  |
| typing_runtime_protocols   | 152 us                                                       | 123 us: 1.24x faster                                                  |
| async_tree_memoization     | 544 ms                                                       | 452 ms: 1.20x faster                                                  |
| async_tree_io_tg           | 1.05 sec                                                     | 879 ms: 1.20x faster                                                  |
| async_tree_none            | 452 ms                                                       | 377 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 592 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 602 ms: 1.16x faster                                                  |
| async_tree_io              | 1.04 sec                                                     | 906 ms: 1.15x faster                                                  |
| comprehensions             | 21.9 us                                                      | 19.5 us: 1.12x faster                                                 |
| generators                 | 37.4 ms                                                      | 34.4 ms: 1.09x faster                                                 |
| crypto_pyaes               | 80.3 ms                                                      | 77.9 ms: 1.03x faster                                                 |
| pickle_pure_python         | 318 us                                                       | 310 us: 1.03x faster                                                  |
| sqlite_synth               | 2.77 us                                                      | 2.70 us: 1.03x faster                                                 |
| asyncio_tcp                | 378 ms                                                       | 369 ms: 1.02x faster                                                  |
| logging_format             | 7.48 us                                                      | 7.31 us: 1.02x faster                                                 |
| coroutines                 | 23.0 ms                                                      | 22.5 ms: 1.02x faster                                                 |
| regex_effbot               | 3.57 ms                                                      | 3.50 ms: 1.02x faster                                                 |
| mako                       | 10.0 ms                                                      | 9.84 ms: 1.02x faster                                                 |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.14 ms: 1.02x faster                                                 |
| unpickle                   | 14.8 us                                                      | 14.6 us: 1.01x faster                                                 |
| unpickle_list              | 4.66 us                                                      | 4.60 us: 1.01x faster                                                 |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.01x faster                                                |
| xml_etree_generate         | 86.1 ms                                                      | 85.5 ms: 1.01x faster                                                 |
| pidigits                   | 265 ms                                                       | 264 ms: 1.01x faster                                                  |
| sympy_sum                  | 162 ms                                                       | 161 ms: 1.00x faster                                                  |
| sympy_str                  | 302 ms                                                       | 304 ms: 1.00x slower                                                  |
| xml_etree_process          | 58.4 ms                                                      | 58.9 ms: 1.01x slower                                                 |
| deepcopy_reduce            | 3.37 us                                                      | 3.41 us: 1.01x slower                                                 |
| xml_etree_iterparse        | 103 ms                                                       | 104 ms: 1.01x slower                                                  |
| chameleon                  | 7.23 ms                                                      | 7.31 ms: 1.01x slower                                                 |
| float                      | 76.6 ms                                                      | 77.7 ms: 1.01x slower                                                 |
| xml_etree_parse            | 144 ms                                                       | 146 ms: 1.01x slower                                                  |
| pickle_dict                | 32.5 us                                                      | 33.1 us: 1.02x slower                                                 |
| tornado_http               | 121 ms                                                       | 124 ms: 1.02x slower                                                  |
| sqlglot_transpile          | 1.78 ms                                                      | 1.81 ms: 1.02x slower                                                 |
| async_generators           | 390 ms                                                       | 398 ms: 1.02x slower                                                  |
| pathlib                    | 18.9 ms                                                      | 19.3 ms: 1.02x slower                                                 |
| tomli_loads                | 2.16 sec                                                     | 2.21 sec: 1.02x slower                                                |
| mdp                        | 2.57 sec                                                     | 2.63 sec: 1.02x slower                                                |
| pprint_safe_repr           | 807 ms                                                       | 828 ms: 1.03x slower                                                  |
| dask                       | 392 ms                                                       | 403 ms: 1.03x slower                                                  |
| pprint_pformat             | 1.65 sec                                                     | 1.70 sec: 1.03x slower                                                |
| sqlglot_parse              | 1.38 ms                                                      | 1.42 ms: 1.03x slower                                                 |
| logging_silent             | 94.4 ns                                                      | 97.3 ns: 1.03x slower                                                 |
| regex_dna                  | 239 ms                                                       | 247 ms: 1.03x slower                                                  |
| raytrace                   | 298 ms                                                       | 309 ms: 1.04x slower                                                  |
| pycparser                  | 1.23 sec                                                     | 1.28 sec: 1.04x slower                                                |
| regex_compile              | 144 ms                                                       | 150 ms: 1.04x slower                                                  |
| scimark_fft                | 301 ms                                                       | 314 ms: 1.04x slower                                                  |
| bench_mp_pool              | 4.76 ms                                                      | 4.98 ms: 1.05x slower                                                 |
| meteor_contest             | 128 ms                                                       | 134 ms: 1.05x slower                                                  |
| json_dumps                 | 10.2 ms                                                      | 10.7 ms: 1.05x slower                                                 |
| spectral_norm              | 91.6 ms                                                      | 96.2 ms: 1.05x slower                                                 |
| django_template            | 38.2 ms                                                      | 40.1 ms: 1.05x slower                                                 |
| sympy_integrate            | 23.9 ms                                                      | 25.1 ms: 1.05x slower                                                 |
| pickle                     | 10.5 us                                                      | 11.1 us: 1.06x slower                                                 |
| sympy_expand               | 484 ms                                                       | 512 ms: 1.06x slower                                                  |
| json_loads                 | 24.4 us                                                      | 25.8 us: 1.06x slower                                                 |
| chaos                      | 64.0 ms                                                      | 67.7 ms: 1.06x slower                                                 |
| 2to3                       | 285 ms                                                       | 302 ms: 1.06x slower                                                  |
| json                       | 5.12 ms                                                      | 5.42 ms: 1.06x slower                                                 |
| deepcopy                   | 368 us                                                       | 391 us: 1.06x slower                                                  |
| sqlglot_normalize          | 116 ms                                                       | 123 ms: 1.07x slower                                                  |
| docutils                   | 2.87 sec                                                     | 3.06 sec: 1.07x slower                                                |
| scimark_monte_carlo        | 69.0 ms                                                      | 73.7 ms: 1.07x slower                                                 |
| dulwich_log                | 65.4 ms                                                      | 69.9 ms: 1.07x slower                                                 |
| nbody                      | 88.0 ms                                                      | 94.7 ms: 1.08x slower                                                 |
| deepcopy_memo              | 36.8 us                                                      | 39.6 us: 1.08x slower                                                 |
| aiohttp                    | 1.02 ms                                                      | 1.11 ms: 1.09x slower                                                 |
| sqlglot_optimize           | 57.5 ms                                                      | 62.9 ms: 1.10x slower                                                 |
| regex_v8                   | 23.6 ms                                                      | 25.9 ms: 1.10x slower                                                 |
| gunicorn                   | 1.00 ms                                                      | 1.10 ms: 1.10x slower                                                 |
| richards                   | 45.7 ms                                                      | 51.2 ms: 1.12x slower                                                 |
| fannkuch                   | 350 ms                                                       | 396 ms: 1.13x slower                                                  |
| create_gc_cycles           | 1.59 ms                                                      | 1.81 ms: 1.14x slower                                                 |
| richards_super             | 51.3 ms                                                      | 58.9 ms: 1.15x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 241 us: 1.15x slower                                                  |
| pyflate                    | 439 ms                                                       | 506 ms: 1.15x slower                                                  |
| deltablue                  | 3.24 ms                                                      | 3.77 ms: 1.17x slower                                                 |
| python_startup             | 11.6 ms                                                      | 13.6 ms: 1.17x slower                                                 |
| nqueens                    | 89.9 ms                                                      | 105 ms: 1.17x slower                                                  |
| telco                      | 6.96 ms                                                      | 8.19 ms: 1.18x slower                                                 |
| bench_thread_pool          | 950 us                                                       | 1.12 ms: 1.18x slower                                                 |
| go                         | 150 ms                                                       | 178 ms: 1.19x slower                                                  |
| scimark_lu                 | 98.8 ms                                                      | 120 ms: 1.21x slower                                                  |
| coverage                   | 66.7 ms                                                      | 81.6 ms: 1.22x slower                                                 |
| hexiom                     | 5.96 ms                                                      | 7.70 ms: 1.29x slower                                                 |
| python_startup_no_site     | 8.64 ms                                                      | 11.8 ms: 1.37x slower                                                 |
| gc_traversal               | 3.48 ms                                                      | 4.85 ms: 1.39x slower                                                 |
| scimark_sor                | 109 ms                                                       | 153 ms: 1.40x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                          |

Benchmark hidden because not significant (4): mypy2, asyncio_websockets, logging_simple, pickle_list
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240403-3.13.0a5+-d42ae28-JIT/bm-20240403-pythonperf2-x86_64-mdboom-all_above_200-3.13.0a5+-d42ae28.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 0.98x