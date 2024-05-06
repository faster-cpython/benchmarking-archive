# Results vs. 3.12.0

- fork: faster-cpython
- ref: call_complex_paramet
- machine: linux-x86_64
- commit hash: 8623ee7
- commit date: 2024-04-10
- overall geometric mean: 1.00x slower
- HPT reliability: 66.29%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.91x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 292 ms: 1.02x slower                                                                   |
| chameleon      | 7.23 ms                                                      | 7.12 ms: 1.01x faster                                                                  |
| docutils       | 2.87 sec                                                     | 2.99 sec: 1.04x slower                                                                 |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                           |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 540 ms                                                       | 419 ms: 1.29x faster                                                                   |
| async_tree_none_tg         | 431 ms                                                       | 339 ms: 1.27x faster                                                                   |
| async_tree_none            | 452 ms                                                       | 369 ms: 1.22x faster                                                                   |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 573 ms: 1.22x faster                                                                   |
| async_tree_io_tg           | 1.05 sec                                                     | 885 ms: 1.19x faster                                                                   |
| async_tree_memoization     | 544 ms                                                       | 462 ms: 1.18x faster                                                                   |
| async_tree_io              | 1.04 sec                                                     | 905 ms: 1.15x faster                                                                   |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 609 ms: 1.14x faster                                                                   |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 262 ms: 1.01x faster                                                                   |
| float          | 76.6 ms                                                      | 77.2 ms: 1.01x slower                                                                  |
| nbody          | 88.0 ms                                                      | 90.0 ms: 1.02x slower                                                                  |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| regex_compile  | 144 ms                                                       | 142 ms: 1.01x faster                                                                   |
| regex_effbot   | 3.57 ms                                                      | 3.56 ms: 1.00x faster                                                                  |
| regex_dna      | 239 ms                                                       | 252 ms: 1.05x slower                                                                   |
| regex_v8       | 23.6 ms                                                      | 26.0 ms: 1.10x slower                                                                  |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| xml_etree_generate   | 86.1 ms                                                      | 84.5 ms: 1.02x faster                                                                  |
| unpickle_list        | 4.66 us                                                      | 4.60 us: 1.01x faster                                                                  |
| pickle_pure_python   | 318 us                                                       | 315 us: 1.01x faster                                                                   |
| pickle               | 10.5 us                                                      | 10.6 us: 1.01x slower                                                                  |
| unpickle             | 14.8 us                                                      | 14.9 us: 1.01x slower                                                                  |
| xml_etree_process    | 58.4 ms                                                      | 58.9 ms: 1.01x slower                                                                  |
| tomli_loads          | 2.16 sec                                                     | 2.19 sec: 1.01x slower                                                                 |
| xml_etree_parse      | 144 ms                                                       | 146 ms: 1.02x slower                                                                   |
| xml_etree_iterparse  | 103 ms                                                       | 105 ms: 1.02x slower                                                                   |
| json_dumps           | 10.2 ms                                                      | 10.5 ms: 1.03x slower                                                                  |
| pickle_dict          | 32.5 us                                                      | 33.6 us: 1.03x slower                                                                  |
| json_loads           | 24.4 us                                                      | 25.9 us: 1.06x slower                                                                  |
| unpickle_pure_python | 210 us                                                       | 225 us: 1.08x slower                                                                   |
| Geometric mean       | (ref)                                                        | 1.02x slower                                                                           |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 12.9 ms: 1.11x slower                                                                  |
| python_startup_no_site | 8.64 ms                                                      | 11.1 ms: 1.28x slower                                                                  |
| Geometric mean         | (ref)                                                        | 1.19x slower                                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|-----------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| mako      | 10.0 ms                                                      | 10.2 ms: 1.02x slower                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 152 us                                                       | 114 us: 1.34x faster                                                                   |
| comprehensions             | 21.9 us                                                      | 16.6 us: 1.32x faster                                                                  |
| async_tree_memoization_tg  | 540 ms                                                       | 419 ms: 1.29x faster                                                                   |
| async_tree_none_tg         | 431 ms                                                       | 339 ms: 1.27x faster                                                                   |
| async_tree_none            | 452 ms                                                       | 369 ms: 1.22x faster                                                                   |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 573 ms: 1.22x faster                                                                   |
| async_tree_io_tg           | 1.05 sec                                                     | 885 ms: 1.19x faster                                                                   |
| async_tree_memoization     | 544 ms                                                       | 462 ms: 1.18x faster                                                                   |
| raytrace                   | 298 ms                                                       | 258 ms: 1.15x faster                                                                   |
| async_tree_io              | 1.04 sec                                                     | 905 ms: 1.15x faster                                                                   |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 609 ms: 1.14x faster                                                                   |
| crypto_pyaes               | 80.3 ms                                                      | 71.8 ms: 1.12x faster                                                                  |
| generators                 | 37.4 ms                                                      | 33.6 ms: 1.11x faster                                                                  |
| mypy2                      | 830 ms                                                       | 772 ms: 1.07x faster                                                                   |
| async_generators           | 390 ms                                                       | 364 ms: 1.07x faster                                                                   |
| bench_thread_pool          | 950 us                                                       | 888 us: 1.07x faster                                                                   |
| chaos                      | 64.0 ms                                                      | 59.9 ms: 1.07x faster                                                                  |
| sympy_sum                  | 162 ms                                                       | 155 ms: 1.04x faster                                                                   |
| scimark_lu                 | 98.8 ms                                                      | 95.2 ms: 1.04x faster                                                                  |
| logging_format             | 7.48 us                                                      | 7.27 us: 1.03x faster                                                                  |
| coroutines                 | 23.0 ms                                                      | 22.4 ms: 1.03x faster                                                                  |
| sympy_integrate            | 23.9 ms                                                      | 23.4 ms: 1.02x faster                                                                  |
| pprint_pformat             | 1.65 sec                                                     | 1.62 sec: 1.02x faster                                                                 |
| sympy_str                  | 302 ms                                                       | 296 ms: 1.02x faster                                                                   |
| pprint_safe_repr           | 807 ms                                                       | 792 ms: 1.02x faster                                                                   |
| xml_etree_generate         | 86.1 ms                                                      | 84.5 ms: 1.02x faster                                                                  |
| logging_simple             | 6.71 us                                                      | 6.59 us: 1.02x faster                                                                  |
| asyncio_tcp                | 378 ms                                                       | 372 ms: 1.02x faster                                                                   |
| regex_compile              | 144 ms                                                       | 142 ms: 1.01x faster                                                                   |
| chameleon                  | 7.23 ms                                                      | 7.12 ms: 1.01x faster                                                                  |
| unpickle_list              | 4.66 us                                                      | 4.60 us: 1.01x faster                                                                  |
| sqlite_synth               | 2.77 us                                                      | 2.74 us: 1.01x faster                                                                  |
| scimark_fft                | 301 ms                                                       | 297 ms: 1.01x faster                                                                   |
| pickle_pure_python         | 318 us                                                       | 315 us: 1.01x faster                                                                   |
| pidigits                   | 265 ms                                                       | 262 ms: 1.01x faster                                                                   |
| mdp                        | 2.57 sec                                                     | 2.54 sec: 1.01x faster                                                                 |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.01x faster                                                                 |
| regex_effbot               | 3.57 ms                                                      | 3.56 ms: 1.00x faster                                                                  |
| meteor_contest             | 128 ms                                                       | 129 ms: 1.01x slower                                                                   |
| pickle                     | 10.5 us                                                      | 10.6 us: 1.01x slower                                                                  |
| float                      | 76.6 ms                                                      | 77.2 ms: 1.01x slower                                                                  |
| unpickle                   | 14.8 us                                                      | 14.9 us: 1.01x slower                                                                  |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.24 ms: 1.01x slower                                                                  |
| xml_etree_process          | 58.4 ms                                                      | 58.9 ms: 1.01x slower                                                                  |
| logging_silent             | 94.4 ns                                                      | 95.3 ns: 1.01x slower                                                                  |
| sqlglot_parse              | 1.38 ms                                                      | 1.40 ms: 1.01x slower                                                                  |
| tomli_loads                | 2.16 sec                                                     | 2.19 sec: 1.01x slower                                                                 |
| xml_etree_parse            | 144 ms                                                       | 146 ms: 1.02x slower                                                                   |
| scimark_monte_carlo        | 69.0 ms                                                      | 70.1 ms: 1.02x slower                                                                  |
| sqlglot_normalize          | 116 ms                                                       | 118 ms: 1.02x slower                                                                   |
| sqlglot_optimize           | 57.5 ms                                                      | 58.6 ms: 1.02x slower                                                                  |
| asyncio_websockets         | 387 ms                                                       | 395 ms: 1.02x slower                                                                   |
| mako                       | 10.0 ms                                                      | 10.2 ms: 1.02x slower                                                                  |
| xml_etree_iterparse        | 103 ms                                                       | 105 ms: 1.02x slower                                                                   |
| 2to3                       | 285 ms                                                       | 292 ms: 1.02x slower                                                                   |
| nbody                      | 88.0 ms                                                      | 90.0 ms: 1.02x slower                                                                  |
| deepcopy_memo              | 36.8 us                                                      | 37.8 us: 1.03x slower                                                                  |
| pathlib                    | 18.9 ms                                                      | 19.4 ms: 1.03x slower                                                                  |
| json_dumps                 | 10.2 ms                                                      | 10.5 ms: 1.03x slower                                                                  |
| pycparser                  | 1.23 sec                                                     | 1.27 sec: 1.03x slower                                                                 |
| sympy_expand               | 484 ms                                                       | 499 ms: 1.03x slower                                                                   |
| deepcopy_reduce            | 3.37 us                                                      | 3.48 us: 1.03x slower                                                                  |
| pickle_dict                | 32.5 us                                                      | 33.6 us: 1.03x slower                                                                  |
| spectral_norm              | 91.6 ms                                                      | 95.0 ms: 1.04x slower                                                                  |
| gunicorn                   | 1.00 ms                                                      | 1.04 ms: 1.04x slower                                                                  |
| dulwich_log                | 65.4 ms                                                      | 68.0 ms: 1.04x slower                                                                  |
| docutils                   | 2.87 sec                                                     | 2.99 sec: 1.04x slower                                                                 |
| deepcopy                   | 368 us                                                       | 387 us: 1.05x slower                                                                   |
| aiohttp                    | 1.02 ms                                                      | 1.07 ms: 1.05x slower                                                                  |
| regex_dna                  | 239 ms                                                       | 252 ms: 1.05x slower                                                                   |
| json_loads                 | 24.4 us                                                      | 25.9 us: 1.06x slower                                                                  |
| deltablue                  | 3.24 ms                                                      | 3.45 ms: 1.07x slower                                                                  |
| unpickle_pure_python       | 210 us                                                       | 225 us: 1.08x slower                                                                   |
| json                       | 5.12 ms                                                      | 5.53 ms: 1.08x slower                                                                  |
| hexiom                     | 5.96 ms                                                      | 6.45 ms: 1.08x slower                                                                  |
| regex_v8                   | 23.6 ms                                                      | 26.0 ms: 1.10x slower                                                                  |
| python_startup             | 11.6 ms                                                      | 12.9 ms: 1.11x slower                                                                  |
| fannkuch                   | 350 ms                                                       | 392 ms: 1.12x slower                                                                   |
| richards_super             | 51.3 ms                                                      | 58.2 ms: 1.13x slower                                                                  |
| go                         | 150 ms                                                       | 170 ms: 1.14x slower                                                                   |
| richards                   | 45.7 ms                                                      | 52.2 ms: 1.14x slower                                                                  |
| telco                      | 6.96 ms                                                      | 8.11 ms: 1.17x slower                                                                  |
| create_gc_cycles           | 1.59 ms                                                      | 1.87 ms: 1.18x slower                                                                  |
| pyflate                    | 439 ms                                                       | 523 ms: 1.19x slower                                                                   |
| coverage                   | 66.7 ms                                                      | 85.3 ms: 1.28x slower                                                                  |
| python_startup_no_site     | 8.64 ms                                                      | 11.1 ms: 1.28x slower                                                                  |
| scimark_sor                | 109 ms                                                       | 141 ms: 1.30x slower                                                                   |
| gc_traversal               | 3.48 ms                                                      | 4.68 ms: 1.35x slower                                                                  |
| Geometric mean             | (ref)                                                        | 1.00x slower                                                                           |

Benchmark hidden because not significant (6): bench_mp_pool, tornado_http, pickle_list, nqueens, sqlglot_transpile, dask
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240410-3.13.0a5+-8623ee7/bm-20240410-pythonperf2-x86_64-faster%2dcpython-call_complex_paramet-3.13.0a5+-8623ee7.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 66.29% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.91x