# Results vs. 3.12.0

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: linux-x86_64
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.01x faster
- HPT reliability: 77.89%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.92x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 287 ms: 1.01x slower                                                                 |
| chameleon      | 7.23 ms                                                      | 7.29 ms: 1.01x slower                                                                |
| docutils       | 2.87 sec                                                     | 2.99 sec: 1.04x slower                                                               |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                         |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 540 ms                                                       | 418 ms: 1.29x faster                                                                 |
| async_tree_none_tg         | 431 ms                                                       | 336 ms: 1.28x faster                                                                 |
| async_tree_none            | 452 ms                                                       | 368 ms: 1.23x faster                                                                 |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 577 ms: 1.21x faster                                                                 |
| async_tree_io_tg           | 1.05 sec                                                     | 880 ms: 1.20x faster                                                                 |
| async_tree_memoization     | 544 ms                                                       | 464 ms: 1.17x faster                                                                 |
| async_tree_io              | 1.04 sec                                                     | 900 ms: 1.16x faster                                                                 |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 613 ms: 1.14x faster                                                                 |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 262 ms: 1.01x faster                                                                 |
| float          | 76.6 ms                                                      | 77.2 ms: 1.01x slower                                                                |
| Geometric mean | (ref)                                                        | 1.01x faster                                                                         |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.47 ms: 1.03x faster                                                                |
| regex_compile  | 144 ms                                                       | 143 ms: 1.01x faster                                                                 |
| regex_dna      | 239 ms                                                       | 238 ms: 1.00x faster                                                                 |
| regex_v8       | 23.6 ms                                                      | 26.0 ms: 1.10x slower                                                                |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| pickle_pure_python   | 318 us                                                       | 310 us: 1.03x faster                                                                 |
| unpickle_pure_python | 210 us                                                       | 204 us: 1.03x faster                                                                 |
| unpickle_list        | 4.66 us                                                      | 4.56 us: 1.02x faster                                                                |
| xml_etree_generate   | 86.1 ms                                                      | 85.1 ms: 1.01x faster                                                                |
| pickle               | 10.5 us                                                      | 10.5 us: 1.00x faster                                                                |
| tomli_loads          | 2.16 sec                                                     | 2.18 sec: 1.01x slower                                                               |
| xml_etree_parse      | 144 ms                                                       | 146 ms: 1.01x slower                                                                 |
| json_loads           | 24.4 us                                                      | 24.8 us: 1.02x slower                                                                |
| xml_etree_process    | 58.4 ms                                                      | 59.6 ms: 1.02x slower                                                                |
| pickle_dict          | 32.5 us                                                      | 33.3 us: 1.02x slower                                                                |
| json_dumps           | 10.2 ms                                                      | 10.6 ms: 1.04x slower                                                                |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                                         |

Benchmark hidden because not significant (3): unpickle, pickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| python_startup_no_site | 8.64 ms                                                      | 8.84 ms: 1.02x slower                                                                |
| python_startup         | 11.6 ms                                                      | 12.9 ms: 1.11x slower                                                                |
| Geometric mean         | (ref)                                                        | 1.06x slower                                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| django_template | 38.2 ms                                                      | 38.8 ms: 1.02x slower                                                                |
| mako            | 10.0 ms                                                      | 10.5 ms: 1.05x slower                                                                |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------------:|
| comprehensions             | 21.9 us                                                      | 16.8 us: 1.30x faster                                                                |
| async_tree_memoization_tg  | 540 ms                                                       | 418 ms: 1.29x faster                                                                 |
| typing_runtime_protocols   | 152 us                                                       | 118 us: 1.29x faster                                                                 |
| async_tree_none_tg         | 431 ms                                                       | 336 ms: 1.28x faster                                                                 |
| async_tree_none            | 452 ms                                                       | 368 ms: 1.23x faster                                                                 |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 577 ms: 1.21x faster                                                                 |
| async_tree_io_tg           | 1.05 sec                                                     | 880 ms: 1.20x faster                                                                 |
| raytrace                   | 298 ms                                                       | 253 ms: 1.18x faster                                                                 |
| async_tree_memoization     | 544 ms                                                       | 464 ms: 1.17x faster                                                                 |
| async_tree_io              | 1.04 sec                                                     | 900 ms: 1.16x faster                                                                 |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 613 ms: 1.14x faster                                                                 |
| generators                 | 37.4 ms                                                      | 33.1 ms: 1.13x faster                                                                |
| crypto_pyaes               | 80.3 ms                                                      | 72.6 ms: 1.11x faster                                                                |
| pathlib                    | 18.9 ms                                                      | 17.1 ms: 1.10x faster                                                                |
| async_generators           | 390 ms                                                       | 356 ms: 1.10x faster                                                                 |
| scimark_monte_carlo        | 69.0 ms                                                      | 63.2 ms: 1.09x faster                                                                |
| chaos                      | 64.0 ms                                                      | 58.6 ms: 1.09x faster                                                                |
| coroutines                 | 23.0 ms                                                      | 21.2 ms: 1.09x faster                                                                |
| logging_format             | 7.48 us                                                      | 6.91 us: 1.08x faster                                                                |
| bench_thread_pool          | 950 us                                                       | 884 us: 1.07x faster                                                                 |
| mypy2                      | 830 ms                                                       | 774 ms: 1.07x faster                                                                 |
| logging_simple             | 6.71 us                                                      | 6.32 us: 1.06x faster                                                                |
| bench_mp_pool              | 4.76 ms                                                      | 4.50 ms: 1.06x faster                                                                |
| sympy_sum                  | 162 ms                                                       | 154 ms: 1.05x faster                                                                 |
| nqueens                    | 89.9 ms                                                      | 86.6 ms: 1.04x faster                                                                |
| sympy_integrate            | 23.9 ms                                                      | 23.1 ms: 1.03x faster                                                                |
| regex_effbot               | 3.57 ms                                                      | 3.47 ms: 1.03x faster                                                                |
| mdp                        | 2.57 sec                                                     | 2.50 sec: 1.03x faster                                                               |
| pickle_pure_python         | 318 us                                                       | 310 us: 1.03x faster                                                                 |
| unpickle_pure_python       | 210 us                                                       | 204 us: 1.03x faster                                                                 |
| unpickle_list              | 4.66 us                                                      | 4.56 us: 1.02x faster                                                                |
| sympy_str                  | 302 ms                                                       | 298 ms: 1.02x faster                                                                 |
| asyncio_tcp                | 378 ms                                                       | 373 ms: 1.01x faster                                                                 |
| xml_etree_generate         | 86.1 ms                                                      | 85.1 ms: 1.01x faster                                                                |
| pidigits                   | 265 ms                                                       | 262 ms: 1.01x faster                                                                 |
| pprint_pformat             | 1.65 sec                                                     | 1.64 sec: 1.01x faster                                                               |
| scimark_fft                | 301 ms                                                       | 298 ms: 1.01x faster                                                                 |
| regex_compile              | 144 ms                                                       | 143 ms: 1.01x faster                                                                 |
| pprint_safe_repr           | 807 ms                                                       | 801 ms: 1.01x faster                                                                 |
| meteor_contest             | 128 ms                                                       | 127 ms: 1.01x faster                                                                 |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.01x faster                                                               |
| regex_dna                  | 239 ms                                                       | 238 ms: 1.00x faster                                                                 |
| pickle                     | 10.5 us                                                      | 10.5 us: 1.00x faster                                                                |
| 2to3                       | 285 ms                                                       | 287 ms: 1.01x slower                                                                 |
| sqlglot_transpile          | 1.78 ms                                                      | 1.79 ms: 1.01x slower                                                                |
| float                      | 76.6 ms                                                      | 77.2 ms: 1.01x slower                                                                |
| chameleon                  | 7.23 ms                                                      | 7.29 ms: 1.01x slower                                                                |
| tomli_loads                | 2.16 sec                                                     | 2.18 sec: 1.01x slower                                                               |
| xml_etree_parse            | 144 ms                                                       | 146 ms: 1.01x slower                                                                 |
| deepcopy_reduce            | 3.37 us                                                      | 3.42 us: 1.01x slower                                                                |
| sqlglot_normalize          | 116 ms                                                       | 117 ms: 1.02x slower                                                                 |
| django_template            | 38.2 ms                                                      | 38.8 ms: 1.02x slower                                                                |
| json_loads                 | 24.4 us                                                      | 24.8 us: 1.02x slower                                                                |
| xml_etree_process          | 58.4 ms                                                      | 59.6 ms: 1.02x slower                                                                |
| sqlglot_parse              | 1.38 ms                                                      | 1.41 ms: 1.02x slower                                                                |
| python_startup_no_site     | 8.64 ms                                                      | 8.84 ms: 1.02x slower                                                                |
| asyncio_websockets         | 387 ms                                                       | 396 ms: 1.02x slower                                                                 |
| hexiom                     | 5.96 ms                                                      | 6.10 ms: 1.02x slower                                                                |
| pickle_dict                | 32.5 us                                                      | 33.3 us: 1.02x slower                                                                |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.32 ms: 1.03x slower                                                                |
| deltablue                  | 3.24 ms                                                      | 3.32 ms: 1.03x slower                                                                |
| sqlglot_optimize           | 57.5 ms                                                      | 59.0 ms: 1.03x slower                                                                |
| deepcopy                   | 368 us                                                       | 379 us: 1.03x slower                                                                 |
| deepcopy_memo              | 36.8 us                                                      | 37.9 us: 1.03x slower                                                                |
| fannkuch                   | 350 ms                                                       | 361 ms: 1.03x slower                                                                 |
| go                         | 150 ms                                                       | 155 ms: 1.03x slower                                                                 |
| dulwich_log                | 65.4 ms                                                      | 67.7 ms: 1.04x slower                                                                |
| json_dumps                 | 10.2 ms                                                      | 10.6 ms: 1.04x slower                                                                |
| pycparser                  | 1.23 sec                                                     | 1.28 sec: 1.04x slower                                                               |
| sympy_expand               | 484 ms                                                       | 504 ms: 1.04x slower                                                                 |
| docutils                   | 2.87 sec                                                     | 2.99 sec: 1.04x slower                                                               |
| gunicorn                   | 1.00 ms                                                      | 1.05 ms: 1.05x slower                                                                |
| mako                       | 10.0 ms                                                      | 10.5 ms: 1.05x slower                                                                |
| aiohttp                    | 1.02 ms                                                      | 1.07 ms: 1.05x slower                                                                |
| spectral_norm              | 91.6 ms                                                      | 96.6 ms: 1.05x slower                                                                |
| pyflate                    | 439 ms                                                       | 468 ms: 1.07x slower                                                                 |
| json                       | 5.12 ms                                                      | 5.46 ms: 1.07x slower                                                                |
| scimark_sor                | 109 ms                                                       | 119 ms: 1.09x slower                                                                 |
| regex_v8                   | 23.6 ms                                                      | 26.0 ms: 1.10x slower                                                                |
| python_startup             | 11.6 ms                                                      | 12.9 ms: 1.11x slower                                                                |
| richards                   | 45.7 ms                                                      | 51.5 ms: 1.13x slower                                                                |
| richards_super             | 51.3 ms                                                      | 58.0 ms: 1.13x slower                                                                |
| telco                      | 6.96 ms                                                      | 8.06 ms: 1.16x slower                                                                |
| create_gc_cycles           | 1.59 ms                                                      | 1.93 ms: 1.21x slower                                                                |
| gc_traversal               | 3.48 ms                                                      | 4.42 ms: 1.27x slower                                                                |
| coverage                   | 66.7 ms                                                      | 86.3 ms: 1.29x slower                                                                |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                                         |

Benchmark hidden because not significant (9): nbody, tornado_http, unpickle, dask, scimark_lu, sqlite_synth, pickle_list, logging_silent, xml_etree_iterparse
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240422-3.13.0a6+-a6d4fd4/bm-20240422-pythonperf2-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 77.89% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.92x