# Results vs. 3.12.0

- fork: Fidget-Spinner
- ref: tagged_evaluation_st
- machine: linux-x86_64
- commit hash: 4675ce8
- commit date: 2024-04-08
- overall geometric mean: 1.01x faster
- HPT reliability: 62.50%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.91x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 290 ms: 1.02x slower                                                                   |
| docutils       | 2.87 sec                                                     | 2.98 sec: 1.04x slower                                                                 |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                           |

Benchmark hidden because not significant (2): chameleon, tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 540 ms                                                       | 417 ms: 1.30x faster                                                                   |
| async_tree_none_tg         | 431 ms                                                       | 337 ms: 1.28x faster                                                                   |
| async_tree_none            | 452 ms                                                       | 368 ms: 1.23x faster                                                                   |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 573 ms: 1.22x faster                                                                   |
| async_tree_io_tg           | 1.05 sec                                                     | 880 ms: 1.20x faster                                                                   |
| async_tree_memoization     | 544 ms                                                       | 462 ms: 1.18x faster                                                                   |
| async_tree_io              | 1.04 sec                                                     | 902 ms: 1.16x faster                                                                   |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 610 ms: 1.14x faster                                                                   |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| nbody          | 88.0 ms                                                      | 85.5 ms: 1.03x faster                                                                  |
| float          | 76.6 ms                                                      | 75.4 ms: 1.02x faster                                                                  |
| pidigits       | 265 ms                                                       | 262 ms: 1.01x faster                                                                   |
| Geometric mean | (ref)                                                        | 1.02x faster                                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| regex_compile  | 144 ms                                                       | 143 ms: 1.01x faster                                                                   |
| regex_dna      | 239 ms                                                       | 243 ms: 1.02x slower                                                                   |
| regex_v8       | 23.6 ms                                                      | 25.4 ms: 1.08x slower                                                                  |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 30.7 us: 1.06x faster                                                                  |
| pickle_pure_python   | 318 us                                                       | 307 us: 1.04x faster                                                                   |
| unpickle_list        | 4.66 us                                                      | 4.55 us: 1.02x faster                                                                  |
| pickle               | 10.5 us                                                      | 10.3 us: 1.02x faster                                                                  |
| xml_etree_generate   | 86.1 ms                                                      | 84.8 ms: 1.02x faster                                                                  |
| xml_etree_process    | 58.4 ms                                                      | 58.6 ms: 1.00x slower                                                                  |
| unpickle             | 14.8 us                                                      | 14.9 us: 1.01x slower                                                                  |
| xml_etree_iterparse  | 103 ms                                                       | 105 ms: 1.02x slower                                                                   |
| xml_etree_parse      | 144 ms                                                       | 147 ms: 1.02x slower                                                                   |
| json_dumps           | 10.2 ms                                                      | 10.5 ms: 1.03x slower                                                                  |
| tomli_loads          | 2.16 sec                                                     | 2.23 sec: 1.04x slower                                                                 |
| json_loads           | 24.4 us                                                      | 25.5 us: 1.05x slower                                                                  |
| unpickle_pure_python | 210 us                                                       | 227 us: 1.08x slower                                                                   |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                                           |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 12.8 ms: 1.10x slower                                                                  |
| python_startup_no_site | 8.64 ms                                                      | 11.1 ms: 1.28x slower                                                                  |
| Geometric mean         | (ref)                                                        | 1.19x slower                                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|-----------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| mako      | 10.0 ms                                                      | 10.2 ms: 1.02x slower                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| comprehensions             | 21.9 us                                                      | 16.6 us: 1.32x faster                                                                  |
| async_tree_memoization_tg  | 540 ms                                                       | 417 ms: 1.30x faster                                                                   |
| typing_runtime_protocols   | 152 us                                                       | 118 us: 1.28x faster                                                                   |
| async_tree_none_tg         | 431 ms                                                       | 337 ms: 1.28x faster                                                                   |
| async_tree_none            | 452 ms                                                       | 368 ms: 1.23x faster                                                                   |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 573 ms: 1.22x faster                                                                   |
| async_tree_io_tg           | 1.05 sec                                                     | 880 ms: 1.20x faster                                                                   |
| raytrace                   | 298 ms                                                       | 251 ms: 1.19x faster                                                                   |
| async_tree_memoization     | 544 ms                                                       | 462 ms: 1.18x faster                                                                   |
| async_tree_io              | 1.04 sec                                                     | 902 ms: 1.16x faster                                                                   |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 610 ms: 1.14x faster                                                                   |
| crypto_pyaes               | 80.3 ms                                                      | 71.3 ms: 1.13x faster                                                                  |
| generators                 | 37.4 ms                                                      | 33.4 ms: 1.12x faster                                                                  |
| async_generators           | 390 ms                                                       | 353 ms: 1.10x faster                                                                   |
| chaos                      | 64.0 ms                                                      | 58.2 ms: 1.10x faster                                                                  |
| mypy2                      | 830 ms                                                       | 774 ms: 1.07x faster                                                                   |
| scimark_monte_carlo        | 69.0 ms                                                      | 64.7 ms: 1.07x faster                                                                  |
| pickle_dict                | 32.5 us                                                      | 30.7 us: 1.06x faster                                                                  |
| bench_thread_pool          | 950 us                                                       | 900 us: 1.05x faster                                                                   |
| sympy_sum                  | 162 ms                                                       | 155 ms: 1.05x faster                                                                   |
| pickle_pure_python         | 318 us                                                       | 307 us: 1.04x faster                                                                   |
| nqueens                    | 89.9 ms                                                      | 86.7 ms: 1.04x faster                                                                  |
| scimark_lu                 | 98.8 ms                                                      | 95.6 ms: 1.03x faster                                                                  |
| logging_format             | 7.48 us                                                      | 7.27 us: 1.03x faster                                                                  |
| nbody                      | 88.0 ms                                                      | 85.5 ms: 1.03x faster                                                                  |
| logging_simple             | 6.71 us                                                      | 6.52 us: 1.03x faster                                                                  |
| pprint_pformat             | 1.65 sec                                                     | 1.61 sec: 1.03x faster                                                                 |
| mdp                        | 2.57 sec                                                     | 2.50 sec: 1.03x faster                                                                 |
| asyncio_tcp                | 378 ms                                                       | 368 ms: 1.03x faster                                                                   |
| pprint_safe_repr           | 807 ms                                                       | 787 ms: 1.03x faster                                                                   |
| unpickle_list              | 4.66 us                                                      | 4.55 us: 1.02x faster                                                                  |
| pickle                     | 10.5 us                                                      | 10.3 us: 1.02x faster                                                                  |
| sympy_str                  | 302 ms                                                       | 296 ms: 1.02x faster                                                                   |
| sympy_integrate            | 23.9 ms                                                      | 23.5 ms: 1.02x faster                                                                  |
| coroutines                 | 23.0 ms                                                      | 22.6 ms: 1.02x faster                                                                  |
| sqlite_synth               | 2.77 us                                                      | 2.73 us: 1.02x faster                                                                  |
| xml_etree_generate         | 86.1 ms                                                      | 84.8 ms: 1.02x faster                                                                  |
| float                      | 76.6 ms                                                      | 75.4 ms: 1.02x faster                                                                  |
| pidigits                   | 265 ms                                                       | 262 ms: 1.01x faster                                                                   |
| regex_compile              | 144 ms                                                       | 143 ms: 1.01x faster                                                                   |
| meteor_contest             | 128 ms                                                       | 127 ms: 1.01x faster                                                                   |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.01x faster                                                                 |
| xml_etree_process          | 58.4 ms                                                      | 58.6 ms: 1.00x slower                                                                  |
| sqlglot_transpile          | 1.78 ms                                                      | 1.78 ms: 1.00x slower                                                                  |
| unpickle                   | 14.8 us                                                      | 14.9 us: 1.01x slower                                                                  |
| sqlglot_normalize          | 116 ms                                                       | 117 ms: 1.01x slower                                                                   |
| sqlglot_parse              | 1.38 ms                                                      | 1.40 ms: 1.02x slower                                                                  |
| 2to3                       | 285 ms                                                       | 290 ms: 1.02x slower                                                                   |
| sqlglot_optimize           | 57.5 ms                                                      | 58.4 ms: 1.02x slower                                                                  |
| deepcopy_reduce            | 3.37 us                                                      | 3.42 us: 1.02x slower                                                                  |
| pathlib                    | 18.9 ms                                                      | 19.2 ms: 1.02x slower                                                                  |
| xml_etree_iterparse        | 103 ms                                                       | 105 ms: 1.02x slower                                                                   |
| regex_dna                  | 239 ms                                                       | 243 ms: 1.02x slower                                                                   |
| mako                       | 10.0 ms                                                      | 10.2 ms: 1.02x slower                                                                  |
| deepcopy                   | 368 us                                                       | 377 us: 1.02x slower                                                                   |
| xml_etree_parse            | 144 ms                                                       | 147 ms: 1.02x slower                                                                   |
| logging_silent             | 94.4 ns                                                      | 96.7 ns: 1.02x slower                                                                  |
| spectral_norm              | 91.6 ms                                                      | 94.0 ms: 1.03x slower                                                                  |
| scimark_fft                | 301 ms                                                       | 309 ms: 1.03x slower                                                                   |
| json_dumps                 | 10.2 ms                                                      | 10.5 ms: 1.03x slower                                                                  |
| pycparser                  | 1.23 sec                                                     | 1.27 sec: 1.03x slower                                                                 |
| sympy_expand               | 484 ms                                                       | 500 ms: 1.03x slower                                                                   |
| tomli_loads                | 2.16 sec                                                     | 2.23 sec: 1.04x slower                                                                 |
| dulwich_log                | 65.4 ms                                                      | 67.8 ms: 1.04x slower                                                                  |
| gunicorn                   | 1.00 ms                                                      | 1.04 ms: 1.04x slower                                                                  |
| docutils                   | 2.87 sec                                                     | 2.98 sec: 1.04x slower                                                                 |
| aiohttp                    | 1.02 ms                                                      | 1.06 ms: 1.04x slower                                                                  |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.38 ms: 1.04x slower                                                                  |
| json_loads                 | 24.4 us                                                      | 25.5 us: 1.05x slower                                                                  |
| deltablue                  | 3.24 ms                                                      | 3.43 ms: 1.06x slower                                                                  |
| json                       | 5.12 ms                                                      | 5.50 ms: 1.07x slower                                                                  |
| regex_v8                   | 23.6 ms                                                      | 25.4 ms: 1.08x slower                                                                  |
| hexiom                     | 5.96 ms                                                      | 6.45 ms: 1.08x slower                                                                  |
| unpickle_pure_python       | 210 us                                                       | 227 us: 1.08x slower                                                                   |
| fannkuch                   | 350 ms                                                       | 380 ms: 1.09x slower                                                                   |
| python_startup             | 11.6 ms                                                      | 12.8 ms: 1.10x slower                                                                  |
| telco                      | 6.96 ms                                                      | 7.92 ms: 1.14x slower                                                                  |
| richards                   | 45.7 ms                                                      | 52.0 ms: 1.14x slower                                                                  |
| richards_super             | 51.3 ms                                                      | 58.6 ms: 1.14x slower                                                                  |
| pyflate                    | 439 ms                                                       | 502 ms: 1.14x slower                                                                   |
| go                         | 150 ms                                                       | 172 ms: 1.15x slower                                                                   |
| create_gc_cycles           | 1.59 ms                                                      | 1.89 ms: 1.19x slower                                                                  |
| scimark_sor                | 109 ms                                                       | 130 ms: 1.20x slower                                                                   |
| coverage                   | 66.7 ms                                                      | 82.1 ms: 1.23x slower                                                                  |
| python_startup_no_site     | 8.64 ms                                                      | 11.1 ms: 1.28x slower                                                                  |
| gc_traversal               | 3.48 ms                                                      | 4.65 ms: 1.34x slower                                                                  |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                                           |

Benchmark hidden because not significant (8): tornado_http, pickle_list, bench_mp_pool, regex_effbot, chameleon, deepcopy_memo, dask, asyncio_websockets
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240408-3.13.0a5+-4675ce8/bm-20240408-pythonperf2-x86_64-Fidget%2dSpinner-tagged_evaluation_st-3.13.0a5+-4675ce8.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 62.50% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.91x