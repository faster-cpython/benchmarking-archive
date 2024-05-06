# Results vs. 3.12.0

- fork: mdboom
- ref: tier2_func_simple
- machine: linux-x86_64
- commit hash: 81bda60
- commit date: 2024-04-05
- overall geometric mean: 1.02x slower
- HPT reliability: 98.53%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 297 ms: 1.04x slower                                                      |
| chameleon      | 7.23 ms                                                      | 7.43 ms: 1.03x slower                                                     |
| docutils       | 2.87 sec                                                     | 3.08 sec: 1.08x slower                                                    |
| Geometric mean | (ref)                                                        | 1.04x slower                                                              |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 335 ms: 1.28x faster                                                      |
| async_tree_memoization_tg  | 540 ms                                                       | 425 ms: 1.27x faster                                                      |
| async_tree_memoization     | 544 ms                                                       | 446 ms: 1.22x faster                                                      |
| async_tree_io              | 1.04 sec                                                     | 856 ms: 1.22x faster                                                      |
| async_tree_io_tg           | 1.05 sec                                                     | 869 ms: 1.21x faster                                                      |
| async_tree_none            | 452 ms                                                       | 378 ms: 1.20x faster                                                      |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 593 ms: 1.18x faster                                                      |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 611 ms: 1.14x faster                                                      |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 76.6 ms                                                      | 75.2 ms: 1.02x faster                                                     |
| pidigits       | 265 ms                                                       | 262 ms: 1.01x faster                                                      |
| nbody          | 88.0 ms                                                      | 103 ms: 1.17x slower                                                      |
| Geometric mean | (ref)                                                        | 1.04x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.54 ms: 1.01x faster                                                     |
| regex_dna      | 239 ms                                                       | 241 ms: 1.01x slower                                                      |
| regex_compile  | 144 ms                                                       | 148 ms: 1.03x slower                                                      |
| regex_v8       | 23.6 ms                                                      | 26.6 ms: 1.12x slower                                                     |
| Geometric mean | (ref)                                                        | 1.04x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 30.8 us: 1.06x faster                                                     |
| xml_etree_generate   | 86.1 ms                                                      | 83.5 ms: 1.03x faster                                                     |
| xml_etree_iterparse  | 103 ms                                                       | 99.8 ms: 1.03x faster                                                     |
| pickle               | 10.5 us                                                      | 10.3 us: 1.02x faster                                                     |
| pickle_pure_python   | 318 us                                                       | 313 us: 1.02x faster                                                      |
| xml_etree_parse      | 144 ms                                                       | 142 ms: 1.01x faster                                                      |
| pickle_list          | 4.43 us                                                      | 4.38 us: 1.01x faster                                                     |
| xml_etree_process    | 58.4 ms                                                      | 58.0 ms: 1.01x faster                                                     |
| tomli_loads          | 2.16 sec                                                     | 2.15 sec: 1.01x faster                                                    |
| unpickle_list        | 4.66 us                                                      | 4.63 us: 1.01x faster                                                     |
| json_dumps           | 10.2 ms                                                      | 10.6 ms: 1.04x slower                                                     |
| json_loads           | 24.4 us                                                      | 25.4 us: 1.04x slower                                                     |
| unpickle_pure_python | 210 us                                                       | 230 us: 1.10x slower                                                      |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                              |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 13.4 ms: 1.16x slower                                                     |
| python_startup_no_site | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                     |
| Geometric mean         | (ref)                                                        | 1.26x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|-----------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako      | 10.0 ms                                                      | 10.1 ms: 1.01x slower                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 335 ms: 1.28x faster                                                      |
| typing_runtime_protocols   | 152 us                                                       | 118 us: 1.28x faster                                                      |
| async_tree_memoization_tg  | 540 ms                                                       | 425 ms: 1.27x faster                                                      |
| async_tree_memoization     | 544 ms                                                       | 446 ms: 1.22x faster                                                      |
| async_tree_io              | 1.04 sec                                                     | 856 ms: 1.22x faster                                                      |
| async_tree_io_tg           | 1.05 sec                                                     | 869 ms: 1.21x faster                                                      |
| async_tree_none            | 452 ms                                                       | 378 ms: 1.20x faster                                                      |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 593 ms: 1.18x faster                                                      |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 611 ms: 1.14x faster                                                      |
| comprehensions             | 21.9 us                                                      | 19.3 us: 1.14x faster                                                     |
| generators                 | 37.4 ms                                                      | 33.4 ms: 1.12x faster                                                     |
| raytrace                   | 298 ms                                                       | 270 ms: 1.11x faster                                                      |
| logging_format             | 7.48 us                                                      | 7.02 us: 1.07x faster                                                     |
| pickle_dict                | 32.5 us                                                      | 30.8 us: 1.06x faster                                                     |
| logging_simple             | 6.71 us                                                      | 6.36 us: 1.06x faster                                                     |
| crypto_pyaes               | 80.3 ms                                                      | 77.3 ms: 1.04x faster                                                     |
| sqlite_synth               | 2.77 us                                                      | 2.68 us: 1.04x faster                                                     |
| coroutines                 | 23.0 ms                                                      | 22.3 ms: 1.03x faster                                                     |
| xml_etree_generate         | 86.1 ms                                                      | 83.5 ms: 1.03x faster                                                     |
| xml_etree_iterparse        | 103 ms                                                       | 99.8 ms: 1.03x faster                                                     |
| pickle                     | 10.5 us                                                      | 10.3 us: 1.02x faster                                                     |
| async_generators           | 390 ms                                                       | 383 ms: 1.02x faster                                                      |
| float                      | 76.6 ms                                                      | 75.2 ms: 1.02x faster                                                     |
| pickle_pure_python         | 318 us                                                       | 313 us: 1.02x faster                                                      |
| asyncio_tcp                | 378 ms                                                       | 372 ms: 1.02x faster                                                      |
| xml_etree_parse            | 144 ms                                                       | 142 ms: 1.01x faster                                                      |
| pidigits                   | 265 ms                                                       | 262 ms: 1.01x faster                                                      |
| pickle_list                | 4.43 us                                                      | 4.38 us: 1.01x faster                                                     |
| regex_effbot               | 3.57 ms                                                      | 3.54 ms: 1.01x faster                                                     |
| xml_etree_process          | 58.4 ms                                                      | 58.0 ms: 1.01x faster                                                     |
| tomli_loads                | 2.16 sec                                                     | 2.15 sec: 1.01x faster                                                    |
| unpickle_list              | 4.66 us                                                      | 4.63 us: 1.01x faster                                                     |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.00x faster                                                    |
| scimark_monte_carlo        | 69.0 ms                                                      | 69.4 ms: 1.01x slower                                                     |
| regex_dna                  | 239 ms                                                       | 241 ms: 1.01x slower                                                      |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.24 ms: 1.01x slower                                                     |
| chaos                      | 64.0 ms                                                      | 64.7 ms: 1.01x slower                                                     |
| deepcopy_memo              | 36.8 us                                                      | 37.2 us: 1.01x slower                                                     |
| mako                       | 10.0 ms                                                      | 10.1 ms: 1.01x slower                                                     |
| asyncio_websockets         | 387 ms                                                       | 392 ms: 1.01x slower                                                      |
| sqlglot_transpile          | 1.78 ms                                                      | 1.80 ms: 1.01x slower                                                     |
| deepcopy_reduce            | 3.37 us                                                      | 3.43 us: 1.02x slower                                                     |
| richards_super             | 51.3 ms                                                      | 52.3 ms: 1.02x slower                                                     |
| spectral_norm              | 91.6 ms                                                      | 93.4 ms: 1.02x slower                                                     |
| sqlglot_parse              | 1.38 ms                                                      | 1.40 ms: 1.02x slower                                                     |
| sympy_sum                  | 162 ms                                                       | 165 ms: 1.02x slower                                                      |
| pathlib                    | 18.9 ms                                                      | 19.4 ms: 1.02x slower                                                     |
| sympy_str                  | 302 ms                                                       | 310 ms: 1.03x slower                                                      |
| mdp                        | 2.57 sec                                                     | 2.63 sec: 1.03x slower                                                    |
| regex_compile              | 144 ms                                                       | 148 ms: 1.03x slower                                                      |
| chameleon                  | 7.23 ms                                                      | 7.43 ms: 1.03x slower                                                     |
| dask                       | 392 ms                                                       | 403 ms: 1.03x slower                                                      |
| deepcopy                   | 368 us                                                       | 379 us: 1.03x slower                                                      |
| pprint_pformat             | 1.65 sec                                                     | 1.70 sec: 1.03x slower                                                    |
| logging_silent             | 94.4 ns                                                      | 97.2 ns: 1.03x slower                                                     |
| pprint_safe_repr           | 807 ms                                                       | 833 ms: 1.03x slower                                                      |
| meteor_contest             | 128 ms                                                       | 133 ms: 1.04x slower                                                      |
| dulwich_log                | 65.4 ms                                                      | 67.7 ms: 1.04x slower                                                     |
| json_dumps                 | 10.2 ms                                                      | 10.6 ms: 1.04x slower                                                     |
| 2to3                       | 285 ms                                                       | 297 ms: 1.04x slower                                                      |
| json_loads                 | 24.4 us                                                      | 25.4 us: 1.04x slower                                                     |
| scimark_fft                | 301 ms                                                       | 319 ms: 1.06x slower                                                      |
| sympy_integrate            | 23.9 ms                                                      | 25.4 ms: 1.06x slower                                                     |
| sqlglot_normalize          | 116 ms                                                       | 123 ms: 1.06x slower                                                      |
| sympy_expand               | 484 ms                                                       | 516 ms: 1.07x slower                                                      |
| json                       | 5.12 ms                                                      | 5.48 ms: 1.07x slower                                                     |
| docutils                   | 2.87 sec                                                     | 3.08 sec: 1.08x slower                                                    |
| gunicorn                   | 1.00 ms                                                      | 1.09 ms: 1.09x slower                                                     |
| sqlglot_optimize           | 57.5 ms                                                      | 62.9 ms: 1.09x slower                                                     |
| unpickle_pure_python       | 210 us                                                       | 230 us: 1.10x slower                                                      |
| aiohttp                    | 1.02 ms                                                      | 1.13 ms: 1.11x slower                                                     |
| nqueens                    | 89.9 ms                                                      | 100 ms: 1.12x slower                                                      |
| fannkuch                   | 350 ms                                                       | 393 ms: 1.12x slower                                                      |
| regex_v8                   | 23.6 ms                                                      | 26.6 ms: 1.12x slower                                                     |
| pyflate                    | 439 ms                                                       | 504 ms: 1.15x slower                                                      |
| python_startup             | 11.6 ms                                                      | 13.4 ms: 1.16x slower                                                     |
| deltablue                  | 3.24 ms                                                      | 3.75 ms: 1.16x slower                                                     |
| nbody                      | 88.0 ms                                                      | 103 ms: 1.17x slower                                                      |
| create_gc_cycles           | 1.59 ms                                                      | 1.87 ms: 1.18x slower                                                     |
| go                         | 150 ms                                                       | 177 ms: 1.18x slower                                                      |
| telco                      | 6.96 ms                                                      | 8.29 ms: 1.19x slower                                                     |
| scimark_lu                 | 98.8 ms                                                      | 118 ms: 1.19x slower                                                      |
| hexiom                     | 5.96 ms                                                      | 7.13 ms: 1.20x slower                                                     |
| coverage                   | 66.7 ms                                                      | 80.7 ms: 1.21x slower                                                     |
| gc_traversal               | 3.48 ms                                                      | 4.44 ms: 1.28x slower                                                     |
| python_startup_no_site     | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                     |
| scimark_sor                | 109 ms                                                       | 152 ms: 1.39x slower                                                      |
| Geometric mean             | (ref)                                                        | 1.02x slower                                                              |

Benchmark hidden because not significant (7): mypy2, bench_mp_pool, unpickle, richards, bench_thread_pool, tornado_http, pycparser
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240405-3.13.0a5+-81bda60-JIT/bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 98.53% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x