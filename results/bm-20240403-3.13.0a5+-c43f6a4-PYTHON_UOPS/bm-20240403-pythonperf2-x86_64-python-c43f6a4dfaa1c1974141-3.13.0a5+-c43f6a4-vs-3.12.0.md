# Results vs. 3.12.0

- fork: python
- ref: c43f6a4dfaa1c1974141
- machine: linux-x86_64
- commit hash: c43f6a4
- commit date: 2024-04-03
- overall geometric mean: 1.13x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 0.92x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 320 ms: 1.12x slower                                                         |
| chameleon      | 7.23 ms                                                      | 8.00 ms: 1.11x slower                                                        |
| docutils       | 2.87 sec                                                     | 3.29 sec: 1.15x slower                                                       |
| tornado_http   | 121 ms                                                       | 128 ms: 1.05x slower                                                         |
| Geometric mean | (ref)                                                        | 1.11x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 346 ms: 1.25x faster                                                         |
| async_tree_memoization_tg  | 540 ms                                                       | 436 ms: 1.24x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 882 ms: 1.19x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 459 ms: 1.18x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 601 ms: 1.16x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 905 ms: 1.15x faster                                                         |
| async_tree_none            | 452 ms                                                       | 394 ms: 1.15x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 623 ms: 1.12x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.18x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 76.6 ms                                                      | 101 ms: 1.31x slower                                                         |
| nbody          | 88.0 ms                                                      | 130 ms: 1.48x slower                                                         |
| Geometric mean | (ref)                                                        | 1.25x slower                                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.54 ms: 1.01x faster                                                        |
| regex_dna      | 239 ms                                                       | 239 ms: 1.00x slower                                                         |
| regex_v8       | 23.6 ms                                                      | 26.6 ms: 1.12x slower                                                        |
| regex_compile  | 144 ms                                                       | 208 ms: 1.45x slower                                                         |
| Geometric mean | (ref)                                                        | 1.13x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 32.7 us: 1.00x slower                                                        |
| pickle_list          | 4.43 us                                                      | 4.46 us: 1.01x slower                                                        |
| pickle_pure_python   | 318 us                                                       | 324 us: 1.02x slower                                                         |
| xml_etree_parse      | 144 ms                                                       | 147 ms: 1.02x slower                                                         |
| unpickle_list        | 4.66 us                                                      | 4.77 us: 1.02x slower                                                        |
| unpickle             | 14.8 us                                                      | 15.3 us: 1.03x slower                                                        |
| pickle               | 10.5 us                                                      | 10.8 us: 1.03x slower                                                        |
| json_loads           | 24.4 us                                                      | 25.2 us: 1.04x slower                                                        |
| json_dumps           | 10.2 ms                                                      | 10.7 ms: 1.04x slower                                                        |
| xml_etree_generate   | 86.1 ms                                                      | 93.8 ms: 1.09x slower                                                        |
| xml_etree_process    | 58.4 ms                                                      | 64.6 ms: 1.11x slower                                                        |
| xml_etree_iterparse  | 103 ms                                                       | 114 ms: 1.11x slower                                                         |
| tomli_loads          | 2.16 sec                                                     | 2.89 sec: 1.34x slower                                                       |
| unpickle_pure_python | 210 us                                                       | 310 us: 1.48x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 12.9 ms: 1.11x slower                                                        |
| python_startup_no_site | 8.64 ms                                                      | 11.2 ms: 1.29x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.20x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|-----------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako      | 10.0 ms                                                      | 14.0 ms: 1.40x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 346 ms: 1.25x faster                                                         |
| async_tree_memoization_tg  | 540 ms                                                       | 436 ms: 1.24x faster                                                         |
| typing_runtime_protocols   | 152 us                                                       | 126 us: 1.20x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 882 ms: 1.19x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 459 ms: 1.18x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 601 ms: 1.16x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 905 ms: 1.15x faster                                                         |
| async_tree_none            | 452 ms                                                       | 394 ms: 1.15x faster                                                         |
| generators                 | 37.4 ms                                                      | 33.0 ms: 1.14x faster                                                        |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 623 ms: 1.12x faster                                                         |
| coroutines                 | 23.0 ms                                                      | 22.3 ms: 1.03x faster                                                        |
| logging_format             | 7.48 us                                                      | 7.33 us: 1.02x faster                                                        |
| logging_simple             | 6.71 us                                                      | 6.63 us: 1.01x faster                                                        |
| regex_effbot               | 3.57 ms                                                      | 3.54 ms: 1.01x faster                                                        |
| regex_dna                  | 239 ms                                                       | 239 ms: 1.00x slower                                                         |
| pickle_dict                | 32.5 us                                                      | 32.7 us: 1.00x slower                                                        |
| pickle_list                | 4.43 us                                                      | 4.46 us: 1.01x slower                                                        |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.60 sec: 1.01x slower                                                       |
| pickle_pure_python         | 318 us                                                       | 324 us: 1.02x slower                                                         |
| asyncio_websockets         | 387 ms                                                       | 395 ms: 1.02x slower                                                         |
| xml_etree_parse            | 144 ms                                                       | 147 ms: 1.02x slower                                                         |
| unpickle_list              | 4.66 us                                                      | 4.77 us: 1.02x slower                                                        |
| unpickle                   | 14.8 us                                                      | 15.3 us: 1.03x slower                                                        |
| pickle                     | 10.5 us                                                      | 10.8 us: 1.03x slower                                                        |
| sqlite_synth               | 2.77 us                                                      | 2.87 us: 1.03x slower                                                        |
| json_loads                 | 24.4 us                                                      | 25.2 us: 1.04x slower                                                        |
| bench_mp_pool              | 4.76 ms                                                      | 4.97 ms: 1.04x slower                                                        |
| mdp                        | 2.57 sec                                                     | 2.68 sec: 1.04x slower                                                       |
| json_dumps                 | 10.2 ms                                                      | 10.7 ms: 1.04x slower                                                        |
| json                       | 5.12 ms                                                      | 5.38 ms: 1.05x slower                                                        |
| logging_silent             | 94.4 ns                                                      | 99.4 ns: 1.05x slower                                                        |
| tornado_http               | 121 ms                                                       | 128 ms: 1.05x slower                                                         |
| dask                       | 392 ms                                                       | 416 ms: 1.06x slower                                                         |
| deepcopy_reduce            | 3.37 us                                                      | 3.59 us: 1.07x slower                                                        |
| pathlib                    | 18.9 ms                                                      | 20.3 ms: 1.07x slower                                                        |
| xml_etree_generate         | 86.1 ms                                                      | 93.8 ms: 1.09x slower                                                        |
| pycparser                  | 1.23 sec                                                     | 1.36 sec: 1.10x slower                                                       |
| xml_etree_process          | 58.4 ms                                                      | 64.6 ms: 1.11x slower                                                        |
| chameleon                  | 7.23 ms                                                      | 8.00 ms: 1.11x slower                                                        |
| sympy_sum                  | 162 ms                                                       | 180 ms: 1.11x slower                                                         |
| python_startup             | 11.6 ms                                                      | 12.9 ms: 1.11x slower                                                        |
| xml_etree_iterparse        | 103 ms                                                       | 114 ms: 1.11x slower                                                         |
| aiohttp                    | 1.02 ms                                                      | 1.13 ms: 1.11x slower                                                        |
| gunicorn                   | 1.00 ms                                                      | 1.12 ms: 1.12x slower                                                        |
| meteor_contest             | 128 ms                                                       | 143 ms: 1.12x slower                                                         |
| sqlglot_transpile          | 1.78 ms                                                      | 1.99 ms: 1.12x slower                                                        |
| sqlglot_normalize          | 116 ms                                                       | 130 ms: 1.12x slower                                                         |
| 2to3                       | 285 ms                                                       | 320 ms: 1.12x slower                                                         |
| sympy_integrate            | 23.9 ms                                                      | 26.9 ms: 1.12x slower                                                        |
| regex_v8                   | 23.6 ms                                                      | 26.6 ms: 1.12x slower                                                        |
| raytrace                   | 298 ms                                                       | 336 ms: 1.13x slower                                                         |
| deepcopy                   | 368 us                                                       | 417 us: 1.13x slower                                                         |
| sqlglot_parse              | 1.38 ms                                                      | 1.57 ms: 1.14x slower                                                        |
| crypto_pyaes               | 80.3 ms                                                      | 92.2 ms: 1.15x slower                                                        |
| docutils                   | 2.87 sec                                                     | 3.29 sec: 1.15x slower                                                       |
| sympy_str                  | 302 ms                                                       | 350 ms: 1.16x slower                                                         |
| sqlglot_optimize           | 57.5 ms                                                      | 67.5 ms: 1.17x slower                                                        |
| chaos                      | 64.0 ms                                                      | 75.9 ms: 1.19x slower                                                        |
| dulwich_log                | 65.4 ms                                                      | 77.8 ms: 1.19x slower                                                        |
| telco                      | 6.96 ms                                                      | 8.29 ms: 1.19x slower                                                        |
| bench_thread_pool          | 950 us                                                       | 1.14 ms: 1.20x slower                                                        |
| sympy_expand               | 484 ms                                                       | 584 ms: 1.21x slower                                                         |
| create_gc_cycles           | 1.59 ms                                                      | 1.94 ms: 1.22x slower                                                        |
| pprint_pformat             | 1.65 sec                                                     | 2.01 sec: 1.22x slower                                                       |
| pprint_safe_repr           | 807 ms                                                       | 983 ms: 1.22x slower                                                         |
| comprehensions             | 21.9 us                                                      | 26.7 us: 1.22x slower                                                        |
| deepcopy_memo              | 36.8 us                                                      | 45.1 us: 1.23x slower                                                        |
| deltablue                  | 3.24 ms                                                      | 3.97 ms: 1.23x slower                                                        |
| gc_traversal               | 3.48 ms                                                      | 4.35 ms: 1.25x slower                                                        |
| python_startup_no_site     | 8.64 ms                                                      | 11.2 ms: 1.29x slower                                                        |
| float                      | 76.6 ms                                                      | 101 ms: 1.31x slower                                                         |
| richards_super             | 51.3 ms                                                      | 67.4 ms: 1.31x slower                                                        |
| coverage                   | 66.7 ms                                                      | 87.6 ms: 1.31x slower                                                        |
| richards                   | 45.7 ms                                                      | 61.0 ms: 1.33x slower                                                        |
| tomli_loads                | 2.16 sec                                                     | 2.89 sec: 1.34x slower                                                       |
| nqueens                    | 89.9 ms                                                      | 122 ms: 1.36x slower                                                         |
| go                         | 150 ms                                                       | 205 ms: 1.37x slower                                                         |
| mako                       | 10.0 ms                                                      | 14.0 ms: 1.40x slower                                                        |
| scimark_monte_carlo        | 69.0 ms                                                      | 99.0 ms: 1.44x slower                                                        |
| regex_compile              | 144 ms                                                       | 208 ms: 1.45x slower                                                         |
| scimark_fft                | 301 ms                                                       | 437 ms: 1.45x slower                                                         |
| nbody                      | 88.0 ms                                                      | 130 ms: 1.48x slower                                                         |
| unpickle_pure_python       | 210 us                                                       | 310 us: 1.48x slower                                                         |
| pyflate                    | 439 ms                                                       | 649 ms: 1.48x slower                                                         |
| fannkuch                   | 350 ms                                                       | 520 ms: 1.49x slower                                                         |
| scimark_lu                 | 98.8 ms                                                      | 149 ms: 1.51x slower                                                         |
| scimark_sor                | 109 ms                                                       | 172 ms: 1.58x slower                                                         |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 6.68 ms: 1.59x slower                                                        |
| spectral_norm              | 91.6 ms                                                      | 154 ms: 1.68x slower                                                         |
| hexiom                     | 5.96 ms                                                      | 10.8 ms: 1.81x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.13x slower                                                                 |

Benchmark hidden because not significant (4): pidigits, async_generators, asyncio_tcp, mypy2
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240403-3.13.0a5+-c43f6a4-PYTHON_UOPS/bm-20240403-pythonperf2-x86_64-python-c43f6a4dfaa1c1974141-3.13.0a5+-c43f6a4.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 0.92x