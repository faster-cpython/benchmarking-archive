# Results vs. 3.12.0

- fork: mdboom
- ref: all_above_300
- machine: linux-x86_64
- commit hash: 4759358
- commit date: 2024-04-03
- overall geometric mean: 1.04x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 301 ms: 1.06x slower                                                  |
| docutils       | 2.87 sec                                                     | 3.05 sec: 1.06x slower                                                |
| tornado_http   | 121 ms                                                       | 125 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x slower                                                          |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 343 ms: 1.26x faster                                                  |
| async_tree_memoization_tg  | 540 ms                                                       | 432 ms: 1.25x faster                                                  |
| async_tree_memoization     | 544 ms                                                       | 455 ms: 1.20x faster                                                  |
| async_tree_io_tg           | 1.05 sec                                                     | 886 ms: 1.19x faster                                                  |
| async_tree_none            | 452 ms                                                       | 380 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 593 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 600 ms: 1.16x faster                                                  |
| async_tree_io              | 1.04 sec                                                     | 909 ms: 1.15x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.19x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 261 ms: 1.01x faster                                                  |
| float          | 76.6 ms                                                      | 79.5 ms: 1.04x slower                                                 |
| nbody          | 88.0 ms                                                      | 95.4 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.50 ms: 1.02x faster                                                 |
| regex_dna      | 239 ms                                                       | 246 ms: 1.03x slower                                                  |
| regex_compile  | 144 ms                                                       | 149 ms: 1.04x slower                                                  |
| regex_v8       | 23.6 ms                                                      | 25.9 ms: 1.09x slower                                                 |
| Geometric mean | (ref)                                                        | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 318 us                                                       | 308 us: 1.03x faster                                                  |
| xml_etree_generate   | 86.1 ms                                                      | 84.3 ms: 1.02x faster                                                 |
| xml_etree_parse      | 144 ms                                                       | 142 ms: 1.01x faster                                                  |
| xml_etree_iterparse  | 103 ms                                                       | 102 ms: 1.01x faster                                                  |
| pickle_list          | 4.43 us                                                      | 4.38 us: 1.01x faster                                                 |
| xml_etree_process    | 58.4 ms                                                      | 58.0 ms: 1.01x faster                                                 |
| pickle_dict          | 32.5 us                                                      | 32.7 us: 1.00x slower                                                 |
| unpickle             | 14.8 us                                                      | 14.9 us: 1.01x slower                                                 |
| unpickle_list        | 4.66 us                                                      | 4.71 us: 1.01x slower                                                 |
| tomli_loads          | 2.16 sec                                                     | 2.21 sec: 1.02x slower                                                |
| pickle               | 10.5 us                                                      | 10.8 us: 1.03x slower                                                 |
| json_loads           | 24.4 us                                                      | 25.3 us: 1.04x slower                                                 |
| json_dumps           | 10.2 ms                                                      | 10.8 ms: 1.06x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 241 us: 1.15x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.02x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                 |
| python_startup_no_site | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.26x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 10.0 ms                                                      | 9.92 ms: 1.01x faster                                                 |
| django_template | 38.2 ms                                                      | 40.2 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 152 us                                                       | 120 us: 1.27x faster                                                  |
| async_tree_none_tg         | 431 ms                                                       | 343 ms: 1.26x faster                                                  |
| async_tree_memoization_tg  | 540 ms                                                       | 432 ms: 1.25x faster                                                  |
| async_tree_memoization     | 544 ms                                                       | 455 ms: 1.20x faster                                                  |
| async_tree_io_tg           | 1.05 sec                                                     | 886 ms: 1.19x faster                                                  |
| async_tree_none            | 452 ms                                                       | 380 ms: 1.19x faster                                                  |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 593 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 600 ms: 1.16x faster                                                  |
| async_tree_io              | 1.04 sec                                                     | 909 ms: 1.15x faster                                                  |
| generators                 | 37.4 ms                                                      | 33.4 ms: 1.12x faster                                                 |
| comprehensions             | 21.9 us                                                      | 19.8 us: 1.11x faster                                                 |
| logging_format             | 7.48 us                                                      | 7.15 us: 1.05x faster                                                 |
| pickle_pure_python         | 318 us                                                       | 308 us: 1.03x faster                                                  |
| sqlite_synth               | 2.77 us                                                      | 2.70 us: 1.03x faster                                                 |
| crypto_pyaes               | 80.3 ms                                                      | 78.7 ms: 1.02x faster                                                 |
| xml_etree_generate         | 86.1 ms                                                      | 84.3 ms: 1.02x faster                                                 |
| asyncio_tcp                | 378 ms                                                       | 370 ms: 1.02x faster                                                  |
| regex_effbot               | 3.57 ms                                                      | 3.50 ms: 1.02x faster                                                 |
| coroutines                 | 23.0 ms                                                      | 22.6 ms: 1.02x faster                                                 |
| pidigits                   | 265 ms                                                       | 261 ms: 1.01x faster                                                  |
| xml_etree_parse            | 144 ms                                                       | 142 ms: 1.01x faster                                                  |
| xml_etree_iterparse        | 103 ms                                                       | 102 ms: 1.01x faster                                                  |
| pickle_list                | 4.43 us                                                      | 4.38 us: 1.01x faster                                                 |
| mako                       | 10.0 ms                                                      | 9.92 ms: 1.01x faster                                                 |
| logging_simple             | 6.71 us                                                      | 6.66 us: 1.01x faster                                                 |
| xml_etree_process          | 58.4 ms                                                      | 58.0 ms: 1.01x faster                                                 |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.01x faster                                                |
| pickle_dict                | 32.5 us                                                      | 32.7 us: 1.00x slower                                                 |
| sympy_sum                  | 162 ms                                                       | 163 ms: 1.01x slower                                                  |
| unpickle                   | 14.8 us                                                      | 14.9 us: 1.01x slower                                                 |
| async_generators           | 390 ms                                                       | 394 ms: 1.01x slower                                                  |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.25 ms: 1.01x slower                                                 |
| unpickle_list              | 4.66 us                                                      | 4.71 us: 1.01x slower                                                 |
| sympy_str                  | 302 ms                                                       | 305 ms: 1.01x slower                                                  |
| mdp                        | 2.57 sec                                                     | 2.62 sec: 1.02x slower                                                |
| tomli_loads                | 2.16 sec                                                     | 2.21 sec: 1.02x slower                                                |
| raytrace                   | 298 ms                                                       | 306 ms: 1.03x slower                                                  |
| dask                       | 392 ms                                                       | 403 ms: 1.03x slower                                                  |
| pickle                     | 10.5 us                                                      | 10.8 us: 1.03x slower                                                 |
| pathlib                    | 18.9 ms                                                      | 19.4 ms: 1.03x slower                                                 |
| sqlglot_transpile          | 1.78 ms                                                      | 1.83 ms: 1.03x slower                                                 |
| regex_dna                  | 239 ms                                                       | 246 ms: 1.03x slower                                                  |
| tornado_http               | 121 ms                                                       | 125 ms: 1.03x slower                                                  |
| logging_silent             | 94.4 ns                                                      | 97.7 ns: 1.04x slower                                                 |
| regex_compile              | 144 ms                                                       | 149 ms: 1.04x slower                                                  |
| float                      | 76.6 ms                                                      | 79.5 ms: 1.04x slower                                                 |
| json_loads                 | 24.4 us                                                      | 25.3 us: 1.04x slower                                                 |
| sqlglot_parse              | 1.38 ms                                                      | 1.43 ms: 1.04x slower                                                 |
| pycparser                  | 1.23 sec                                                     | 1.29 sec: 1.04x slower                                                |
| deepcopy_memo              | 36.8 us                                                      | 38.4 us: 1.04x slower                                                 |
| json                       | 5.12 ms                                                      | 5.36 ms: 1.05x slower                                                 |
| meteor_contest             | 128 ms                                                       | 135 ms: 1.05x slower                                                  |
| django_template            | 38.2 ms                                                      | 40.2 ms: 1.05x slower                                                 |
| json_dumps                 | 10.2 ms                                                      | 10.8 ms: 1.06x slower                                                 |
| spectral_norm              | 91.6 ms                                                      | 96.8 ms: 1.06x slower                                                 |
| sympy_integrate            | 23.9 ms                                                      | 25.3 ms: 1.06x slower                                                 |
| 2to3                       | 285 ms                                                       | 301 ms: 1.06x slower                                                  |
| deepcopy                   | 368 us                                                       | 390 us: 1.06x slower                                                  |
| pprint_pformat             | 1.65 sec                                                     | 1.75 sec: 1.06x slower                                                |
| sympy_expand               | 484 ms                                                       | 513 ms: 1.06x slower                                                  |
| chaos                      | 64.0 ms                                                      | 67.9 ms: 1.06x slower                                                 |
| dulwich_log                | 65.4 ms                                                      | 69.4 ms: 1.06x slower                                                 |
| pprint_safe_repr           | 807 ms                                                       | 858 ms: 1.06x slower                                                  |
| docutils                   | 2.87 sec                                                     | 3.05 sec: 1.06x slower                                                |
| scimark_fft                | 301 ms                                                       | 320 ms: 1.06x slower                                                  |
| sqlglot_normalize          | 116 ms                                                       | 123 ms: 1.06x slower                                                  |
| scimark_monte_carlo        | 69.0 ms                                                      | 74.8 ms: 1.08x slower                                                 |
| nbody                      | 88.0 ms                                                      | 95.4 ms: 1.09x slower                                                 |
| gunicorn                   | 1.00 ms                                                      | 1.09 ms: 1.09x slower                                                 |
| regex_v8                   | 23.6 ms                                                      | 25.9 ms: 1.09x slower                                                 |
| aiohttp                    | 1.02 ms                                                      | 1.12 ms: 1.10x slower                                                 |
| bench_mp_pool              | 4.76 ms                                                      | 5.22 ms: 1.10x slower                                                 |
| sqlglot_optimize           | 57.5 ms                                                      | 63.2 ms: 1.10x slower                                                 |
| fannkuch                   | 350 ms                                                       | 393 ms: 1.12x slower                                                  |
| create_gc_cycles           | 1.59 ms                                                      | 1.80 ms: 1.13x slower                                                 |
| richards                   | 45.7 ms                                                      | 51.9 ms: 1.13x slower                                                 |
| richards_super             | 51.3 ms                                                      | 58.3 ms: 1.14x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 241 us: 1.15x slower                                                  |
| telco                      | 6.96 ms                                                      | 8.03 ms: 1.15x slower                                                 |
| python_startup             | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                 |
| deltablue                  | 3.24 ms                                                      | 3.76 ms: 1.16x slower                                                 |
| bench_thread_pool          | 950 us                                                       | 1.13 ms: 1.19x slower                                                 |
| nqueens                    | 89.9 ms                                                      | 107 ms: 1.19x slower                                                  |
| pyflate                    | 439 ms                                                       | 525 ms: 1.20x slower                                                  |
| go                         | 150 ms                                                       | 180 ms: 1.20x slower                                                  |
| gc_traversal               | 3.48 ms                                                      | 4.37 ms: 1.26x slower                                                 |
| scimark_lu                 | 98.8 ms                                                      | 126 ms: 1.27x slower                                                  |
| hexiom                     | 5.96 ms                                                      | 7.75 ms: 1.30x slower                                                 |
| coverage                   | 66.7 ms                                                      | 88.1 ms: 1.32x slower                                                 |
| python_startup_no_site     | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                 |
| scimark_sor                | 109 ms                                                       | 155 ms: 1.42x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.04x slower                                                          |

Benchmark hidden because not significant (4): mypy2, chameleon, deepcopy_reduce, asyncio_websockets
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240403-3.13.0a5+-4759358-JIT/bm-20240403-pythonperf2-x86_64-mdboom-all_above_300-3.13.0a5+-4759358.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 0.98x