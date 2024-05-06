# Results vs. 3.12.0

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: dcee362
- commit date: 2024-04-03
- overall geometric mean: 1.11x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x slower
- Memory change: 0.92x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 316 ms: 1.11x slower                                                    |
| chameleon      | 7.23 ms                                                      | 7.77 ms: 1.08x slower                                                   |
| docutils       | 2.87 sec                                                     | 3.24 sec: 1.13x slower                                                  |
| tornado_http   | 121 ms                                                       | 129 ms: 1.06x slower                                                    |
| Geometric mean | (ref)                                                        | 1.09x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 354 ms: 1.22x faster                                                    |
| async_tree_memoization_tg  | 540 ms                                                       | 447 ms: 1.21x faster                                                    |
| async_tree_io_tg           | 1.05 sec                                                     | 892 ms: 1.18x faster                                                    |
| async_tree_memoization     | 544 ms                                                       | 463 ms: 1.17x faster                                                    |
| async_tree_io              | 1.04 sec                                                     | 912 ms: 1.14x faster                                                    |
| async_tree_none            | 452 ms                                                       | 395 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 612 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 628 ms: 1.11x faster                                                    |
| Geometric mean             | (ref)                                                        | 1.16x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 266 ms: 1.00x slower                                                    |
| float          | 76.6 ms                                                      | 91.6 ms: 1.20x slower                                                   |
| nbody          | 88.0 ms                                                      | 114 ms: 1.30x slower                                                    |
| Geometric mean | (ref)                                                        | 1.16x slower                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_dna      | 239 ms                                                       | 236 ms: 1.01x faster                                                    |
| regex_v8       | 23.6 ms                                                      | 25.6 ms: 1.08x slower                                                   |
| regex_compile  | 144 ms                                                       | 196 ms: 1.36x slower                                                    |
| Geometric mean | (ref)                                                        | 1.10x slower                                                            |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 31.2 us: 1.04x faster                                                   |
| pickle               | 10.5 us                                                      | 10.4 us: 1.01x faster                                                   |
| pickle_list          | 4.43 us                                                      | 4.38 us: 1.01x faster                                                   |
| unpickle_list        | 4.66 us                                                      | 4.77 us: 1.02x slower                                                   |
| pickle_pure_python   | 318 us                                                       | 326 us: 1.03x slower                                                    |
| json_loads           | 24.4 us                                                      | 25.3 us: 1.04x slower                                                   |
| json_dumps           | 10.2 ms                                                      | 10.7 ms: 1.04x slower                                                   |
| xml_etree_generate   | 86.1 ms                                                      | 90.3 ms: 1.05x slower                                                   |
| xml_etree_iterparse  | 103 ms                                                       | 108 ms: 1.05x slower                                                    |
| xml_etree_process    | 58.4 ms                                                      | 62.5 ms: 1.07x slower                                                   |
| tomli_loads          | 2.16 sec                                                     | 2.74 sec: 1.27x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 293 us: 1.40x slower                                                    |
| Geometric mean       | (ref)                                                        | 1.06x slower                                                            |

Benchmark hidden because not significant (2): unpickle, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 13.0 ms: 1.12x slower                                                   |
| python_startup_no_site | 8.64 ms                                                      | 11.2 ms: 1.30x slower                                                   |
| Geometric mean         | (ref)                                                        | 1.20x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|-----------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| mako      | 10.0 ms                                                      | 13.2 ms: 1.32x slower                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 354 ms: 1.22x faster                                                    |
| async_tree_memoization_tg  | 540 ms                                                       | 447 ms: 1.21x faster                                                    |
| typing_runtime_protocols   | 152 us                                                       | 127 us: 1.20x faster                                                    |
| async_tree_io_tg           | 1.05 sec                                                     | 892 ms: 1.18x faster                                                    |
| async_tree_memoization     | 544 ms                                                       | 463 ms: 1.17x faster                                                    |
| async_tree_io              | 1.04 sec                                                     | 912 ms: 1.14x faster                                                    |
| async_tree_none            | 452 ms                                                       | 395 ms: 1.14x faster                                                    |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 612 ms: 1.14x faster                                                    |
| generators                 | 37.4 ms                                                      | 33.7 ms: 1.11x faster                                                   |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 628 ms: 1.11x faster                                                    |
| pickle_dict                | 32.5 us                                                      | 31.2 us: 1.04x faster                                                   |
| logging_format             | 7.48 us                                                      | 7.29 us: 1.03x faster                                                   |
| coroutines                 | 23.0 ms                                                      | 22.6 ms: 1.02x faster                                                   |
| logging_simple             | 6.71 us                                                      | 6.59 us: 1.02x faster                                                   |
| pickle                     | 10.5 us                                                      | 10.4 us: 1.01x faster                                                   |
| async_generators           | 390 ms                                                       | 385 ms: 1.01x faster                                                    |
| pickle_list                | 4.43 us                                                      | 4.38 us: 1.01x faster                                                   |
| regex_dna                  | 239 ms                                                       | 236 ms: 1.01x faster                                                    |
| pidigits                   | 265 ms                                                       | 266 ms: 1.00x slower                                                    |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.60 sec: 1.01x slower                                                  |
| asyncio_websockets         | 387 ms                                                       | 392 ms: 1.01x slower                                                    |
| asyncio_tcp                | 378 ms                                                       | 383 ms: 1.01x slower                                                    |
| raytrace                   | 298 ms                                                       | 304 ms: 1.02x slower                                                    |
| unpickle_list              | 4.66 us                                                      | 4.77 us: 1.02x slower                                                   |
| pickle_pure_python         | 318 us                                                       | 326 us: 1.03x slower                                                    |
| mdp                        | 2.57 sec                                                     | 2.67 sec: 1.04x slower                                                  |
| json_loads                 | 24.4 us                                                      | 25.3 us: 1.04x slower                                                   |
| json_dumps                 | 10.2 ms                                                      | 10.7 ms: 1.04x slower                                                   |
| xml_etree_generate         | 86.1 ms                                                      | 90.3 ms: 1.05x slower                                                   |
| xml_etree_iterparse        | 103 ms                                                       | 108 ms: 1.05x slower                                                    |
| json                       | 5.12 ms                                                      | 5.43 ms: 1.06x slower                                                   |
| tornado_http               | 121 ms                                                       | 129 ms: 1.06x slower                                                    |
| dask                       | 392 ms                                                       | 419 ms: 1.07x slower                                                    |
| xml_etree_process          | 58.4 ms                                                      | 62.5 ms: 1.07x slower                                                   |
| chameleon                  | 7.23 ms                                                      | 7.77 ms: 1.08x slower                                                   |
| regex_v8                   | 23.6 ms                                                      | 25.6 ms: 1.08x slower                                                   |
| deepcopy_reduce            | 3.37 us                                                      | 3.66 us: 1.09x slower                                                   |
| pathlib                    | 18.9 ms                                                      | 20.6 ms: 1.09x slower                                                   |
| pycparser                  | 1.23 sec                                                     | 1.35 sec: 1.09x slower                                                  |
| crypto_pyaes               | 80.3 ms                                                      | 87.7 ms: 1.09x slower                                                   |
| logging_silent             | 94.4 ns                                                      | 103 ns: 1.09x slower                                                    |
| sqlglot_transpile          | 1.78 ms                                                      | 1.95 ms: 1.10x slower                                                   |
| sympy_integrate            | 23.9 ms                                                      | 26.5 ms: 1.11x slower                                                   |
| 2to3                       | 285 ms                                                       | 316 ms: 1.11x slower                                                    |
| meteor_contest             | 128 ms                                                       | 142 ms: 1.11x slower                                                    |
| sympy_sum                  | 162 ms                                                       | 180 ms: 1.11x slower                                                    |
| python_startup             | 11.6 ms                                                      | 13.0 ms: 1.12x slower                                                   |
| sqlglot_normalize          | 116 ms                                                       | 129 ms: 1.12x slower                                                    |
| gunicorn                   | 1.00 ms                                                      | 1.12 ms: 1.12x slower                                                   |
| aiohttp                    | 1.02 ms                                                      | 1.14 ms: 1.12x slower                                                   |
| comprehensions             | 21.9 us                                                      | 24.7 us: 1.13x slower                                                   |
| sqlglot_parse              | 1.38 ms                                                      | 1.55 ms: 1.13x slower                                                   |
| docutils                   | 2.87 sec                                                     | 3.24 sec: 1.13x slower                                                  |
| deepcopy                   | 368 us                                                       | 417 us: 1.13x slower                                                    |
| chaos                      | 64.0 ms                                                      | 72.5 ms: 1.13x slower                                                   |
| sympy_str                  | 302 ms                                                       | 347 ms: 1.15x slower                                                    |
| create_gc_cycles           | 1.59 ms                                                      | 1.85 ms: 1.16x slower                                                   |
| sqlglot_optimize           | 57.5 ms                                                      | 67.0 ms: 1.17x slower                                                   |
| dulwich_log                | 65.4 ms                                                      | 77.1 ms: 1.18x slower                                                   |
| richards                   | 45.7 ms                                                      | 54.2 ms: 1.18x slower                                                   |
| richards_super             | 51.3 ms                                                      | 60.9 ms: 1.19x slower                                                   |
| deepcopy_memo              | 36.8 us                                                      | 43.7 us: 1.19x slower                                                   |
| sympy_expand               | 484 ms                                                       | 577 ms: 1.19x slower                                                    |
| float                      | 76.6 ms                                                      | 91.6 ms: 1.20x slower                                                   |
| pprint_pformat             | 1.65 sec                                                     | 1.98 sec: 1.20x slower                                                  |
| pprint_safe_repr           | 807 ms                                                       | 971 ms: 1.20x slower                                                    |
| telco                      | 6.96 ms                                                      | 8.59 ms: 1.23x slower                                                   |
| tomli_loads                | 2.16 sec                                                     | 2.74 sec: 1.27x slower                                                  |
| nqueens                    | 89.9 ms                                                      | 114 ms: 1.27x slower                                                    |
| deltablue                  | 3.24 ms                                                      | 4.14 ms: 1.28x slower                                                   |
| nbody                      | 88.0 ms                                                      | 114 ms: 1.30x slower                                                    |
| python_startup_no_site     | 8.64 ms                                                      | 11.2 ms: 1.30x slower                                                   |
| coverage                   | 66.7 ms                                                      | 87.8 ms: 1.32x slower                                                   |
| mako                       | 10.0 ms                                                      | 13.2 ms: 1.32x slower                                                   |
| fannkuch                   | 350 ms                                                       | 466 ms: 1.33x slower                                                    |
| scimark_monte_carlo        | 69.0 ms                                                      | 92.2 ms: 1.34x slower                                                   |
| scimark_fft                | 301 ms                                                       | 404 ms: 1.34x slower                                                    |
| gc_traversal               | 3.48 ms                                                      | 4.69 ms: 1.35x slower                                                   |
| regex_compile              | 144 ms                                                       | 196 ms: 1.36x slower                                                    |
| scimark_lu                 | 98.8 ms                                                      | 135 ms: 1.37x slower                                                    |
| pyflate                    | 439 ms                                                       | 604 ms: 1.38x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 293 us: 1.40x slower                                                    |
| go                         | 150 ms                                                       | 210 ms: 1.40x slower                                                    |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 6.14 ms: 1.46x slower                                                   |
| scimark_sor                | 109 ms                                                       | 159 ms: 1.46x slower                                                    |
| spectral_norm              | 91.6 ms                                                      | 140 ms: 1.53x slower                                                    |
| hexiom                     | 5.96 ms                                                      | 9.76 ms: 1.64x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.11x slower                                                            |

Benchmark hidden because not significant (7): unpickle, xml_etree_parse, bench_mp_pool, regex_effbot, sqlite_synth, bench_thread_pool, mypy2
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240403-3.13.0a5+-dcee362-PYTHON_UOPS/bm-20240403-pythonperf2-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 0.92x