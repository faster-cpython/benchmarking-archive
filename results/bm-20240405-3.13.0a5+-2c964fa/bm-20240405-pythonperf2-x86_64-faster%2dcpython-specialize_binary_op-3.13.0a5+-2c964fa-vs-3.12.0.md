# Results vs. 3.12.0

- fork: faster-cpython
- ref: specialize_binary_op
- machine: linux-x86_64
- commit hash: 2c964fa
- commit date: 2024-04-05
- overall geometric mean: 1.00x faster
- HPT reliability: 65.60%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.91x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 288 ms: 1.01x slower                                                                   |
| chameleon      | 7.23 ms                                                      | 7.47 ms: 1.03x slower                                                                  |
| docutils       | 2.87 sec                                                     | 2.98 sec: 1.04x slower                                                                 |
| tornado_http   | 121 ms                                                       | 119 ms: 1.01x faster                                                                   |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 540 ms                                                       | 416 ms: 1.30x faster                                                                   |
| async_tree_none_tg         | 431 ms                                                       | 334 ms: 1.29x faster                                                                   |
| async_tree_none            | 452 ms                                                       | 366 ms: 1.23x faster                                                                   |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 573 ms: 1.22x faster                                                                   |
| async_tree_io_tg           | 1.05 sec                                                     | 885 ms: 1.19x faster                                                                   |
| async_tree_memoization     | 544 ms                                                       | 460 ms: 1.18x faster                                                                   |
| async_tree_io              | 1.04 sec                                                     | 907 ms: 1.15x faster                                                                   |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 607 ms: 1.15x faster                                                                   |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 262 ms: 1.01x faster                                                                   |
| nbody          | 88.0 ms                                                      | 91.4 ms: 1.04x slower                                                                  |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.48 ms: 1.03x faster                                                                  |
| regex_compile  | 144 ms                                                       | 141 ms: 1.02x faster                                                                   |
| regex_dna      | 239 ms                                                       | 240 ms: 1.00x slower                                                                   |
| regex_v8       | 23.6 ms                                                      | 25.4 ms: 1.08x slower                                                                  |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 30.4 us: 1.07x faster                                                                  |
| xml_etree_generate   | 86.1 ms                                                      | 82.6 ms: 1.04x faster                                                                  |
| pickle_pure_python   | 318 us                                                       | 307 us: 1.04x faster                                                                   |
| pickle_list          | 4.43 us                                                      | 4.29 us: 1.03x faster                                                                  |
| pickle               | 10.5 us                                                      | 10.2 us: 1.03x faster                                                                  |
| unpickle_list        | 4.66 us                                                      | 4.57 us: 1.02x faster                                                                  |
| xml_etree_process    | 58.4 ms                                                      | 57.6 ms: 1.01x faster                                                                  |
| xml_etree_iterparse  | 103 ms                                                       | 104 ms: 1.01x slower                                                                   |
| tomli_loads          | 2.16 sec                                                     | 2.20 sec: 1.02x slower                                                                 |
| unpickle             | 14.8 us                                                      | 15.2 us: 1.02x slower                                                                  |
| xml_etree_parse      | 144 ms                                                       | 148 ms: 1.03x slower                                                                   |
| json_dumps           | 10.2 ms                                                      | 10.6 ms: 1.04x slower                                                                  |
| json_loads           | 24.4 us                                                      | 25.5 us: 1.05x slower                                                                  |
| unpickle_pure_python | 210 us                                                       | 221 us: 1.06x slower                                                                   |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 12.8 ms: 1.10x slower                                                                  |
| python_startup_no_site | 8.64 ms                                                      | 11.0 ms: 1.28x slower                                                                  |
| Geometric mean         | (ref)                                                        | 1.19x slower                                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|-----------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| mako      | 10.0 ms                                                      | 10.3 ms: 1.03x slower                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------------:|
| comprehensions             | 21.9 us                                                      | 16.5 us: 1.33x faster                                                                  |
| typing_runtime_protocols   | 152 us                                                       | 116 us: 1.31x faster                                                                   |
| async_tree_memoization_tg  | 540 ms                                                       | 416 ms: 1.30x faster                                                                   |
| async_tree_none_tg         | 431 ms                                                       | 334 ms: 1.29x faster                                                                   |
| async_tree_none            | 452 ms                                                       | 366 ms: 1.23x faster                                                                   |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 573 ms: 1.22x faster                                                                   |
| async_tree_io_tg           | 1.05 sec                                                     | 885 ms: 1.19x faster                                                                   |
| async_tree_memoization     | 544 ms                                                       | 460 ms: 1.18x faster                                                                   |
| raytrace                   | 298 ms                                                       | 258 ms: 1.15x faster                                                                   |
| async_tree_io              | 1.04 sec                                                     | 907 ms: 1.15x faster                                                                   |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 607 ms: 1.15x faster                                                                   |
| generators                 | 37.4 ms                                                      | 32.9 ms: 1.14x faster                                                                  |
| crypto_pyaes               | 80.3 ms                                                      | 72.4 ms: 1.11x faster                                                                  |
| async_generators           | 390 ms                                                       | 359 ms: 1.09x faster                                                                   |
| mypy2                      | 830 ms                                                       | 766 ms: 1.08x faster                                                                   |
| pickle_dict                | 32.5 us                                                      | 30.4 us: 1.07x faster                                                                  |
| bench_thread_pool          | 950 us                                                       | 886 us: 1.07x faster                                                                   |
| sympy_sum                  | 162 ms                                                       | 153 ms: 1.06x faster                                                                   |
| chaos                      | 64.0 ms                                                      | 60.7 ms: 1.05x faster                                                                  |
| bench_mp_pool              | 4.76 ms                                                      | 4.55 ms: 1.05x faster                                                                  |
| xml_etree_generate         | 86.1 ms                                                      | 82.6 ms: 1.04x faster                                                                  |
| spectral_norm              | 91.6 ms                                                      | 88.4 ms: 1.04x faster                                                                  |
| pickle_pure_python         | 318 us                                                       | 307 us: 1.04x faster                                                                   |
| pprint_pformat             | 1.65 sec                                                     | 1.60 sec: 1.04x faster                                                                 |
| logging_format             | 7.48 us                                                      | 7.24 us: 1.03x faster                                                                  |
| logging_simple             | 6.71 us                                                      | 6.49 us: 1.03x faster                                                                  |
| pickle_list                | 4.43 us                                                      | 4.29 us: 1.03x faster                                                                  |
| pickle                     | 10.5 us                                                      | 10.2 us: 1.03x faster                                                                  |
| pprint_safe_repr           | 807 ms                                                       | 785 ms: 1.03x faster                                                                   |
| sympy_integrate            | 23.9 ms                                                      | 23.3 ms: 1.03x faster                                                                  |
| sympy_str                  | 302 ms                                                       | 294 ms: 1.03x faster                                                                   |
| regex_effbot               | 3.57 ms                                                      | 3.48 ms: 1.03x faster                                                                  |
| asyncio_tcp                | 378 ms                                                       | 369 ms: 1.02x faster                                                                   |
| mdp                        | 2.57 sec                                                     | 2.51 sec: 1.02x faster                                                                 |
| regex_compile              | 144 ms                                                       | 141 ms: 1.02x faster                                                                   |
| unpickle_list              | 4.66 us                                                      | 4.57 us: 1.02x faster                                                                  |
| tornado_http               | 121 ms                                                       | 119 ms: 1.01x faster                                                                   |
| xml_etree_process          | 58.4 ms                                                      | 57.6 ms: 1.01x faster                                                                  |
| pidigits                   | 265 ms                                                       | 262 ms: 1.01x faster                                                                   |
| coroutines                 | 23.0 ms                                                      | 22.7 ms: 1.01x faster                                                                  |
| sqlite_synth               | 2.77 us                                                      | 2.74 us: 1.01x faster                                                                  |
| scimark_monte_carlo        | 69.0 ms                                                      | 68.2 ms: 1.01x faster                                                                  |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.01x faster                                                                 |
| meteor_contest             | 128 ms                                                       | 127 ms: 1.01x faster                                                                   |
| nqueens                    | 89.9 ms                                                      | 89.5 ms: 1.00x faster                                                                  |
| regex_dna                  | 239 ms                                                       | 240 ms: 1.00x slower                                                                   |
| 2to3                       | 285 ms                                                       | 288 ms: 1.01x slower                                                                   |
| sqlglot_optimize           | 57.5 ms                                                      | 58.1 ms: 1.01x slower                                                                  |
| deepcopy_memo              | 36.8 us                                                      | 37.2 us: 1.01x slower                                                                  |
| pathlib                    | 18.9 ms                                                      | 19.1 ms: 1.01x slower                                                                  |
| asyncio_websockets         | 387 ms                                                       | 392 ms: 1.01x slower                                                                   |
| xml_etree_iterparse        | 103 ms                                                       | 104 ms: 1.01x slower                                                                   |
| deepcopy_reduce            | 3.37 us                                                      | 3.43 us: 1.02x slower                                                                  |
| tomli_loads                | 2.16 sec                                                     | 2.20 sec: 1.02x slower                                                                 |
| sqlglot_parse              | 1.38 ms                                                      | 1.41 ms: 1.02x slower                                                                  |
| sympy_expand               | 484 ms                                                       | 495 ms: 1.02x slower                                                                   |
| pycparser                  | 1.23 sec                                                     | 1.26 sec: 1.02x slower                                                                 |
| unpickle                   | 14.8 us                                                      | 15.2 us: 1.02x slower                                                                  |
| mako                       | 10.0 ms                                                      | 10.3 ms: 1.03x slower                                                                  |
| xml_etree_parse            | 144 ms                                                       | 148 ms: 1.03x slower                                                                   |
| deepcopy                   | 368 us                                                       | 379 us: 1.03x slower                                                                   |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.35 ms: 1.03x slower                                                                  |
| chameleon                  | 7.23 ms                                                      | 7.47 ms: 1.03x slower                                                                  |
| json_dumps                 | 10.2 ms                                                      | 10.6 ms: 1.04x slower                                                                  |
| nbody                      | 88.0 ms                                                      | 91.4 ms: 1.04x slower                                                                  |
| docutils                   | 2.87 sec                                                     | 2.98 sec: 1.04x slower                                                                 |
| dulwich_log                | 65.4 ms                                                      | 68.1 ms: 1.04x slower                                                                  |
| gunicorn                   | 1.00 ms                                                      | 1.04 ms: 1.04x slower                                                                  |
| json_loads                 | 24.4 us                                                      | 25.5 us: 1.05x slower                                                                  |
| aiohttp                    | 1.02 ms                                                      | 1.08 ms: 1.06x slower                                                                  |
| unpickle_pure_python       | 210 us                                                       | 221 us: 1.06x slower                                                                   |
| deltablue                  | 3.24 ms                                                      | 3.42 ms: 1.06x slower                                                                  |
| scimark_fft                | 301 ms                                                       | 320 ms: 1.06x slower                                                                   |
| json                       | 5.12 ms                                                      | 5.48 ms: 1.07x slower                                                                  |
| regex_v8                   | 23.6 ms                                                      | 25.4 ms: 1.08x slower                                                                  |
| fannkuch                   | 350 ms                                                       | 381 ms: 1.09x slower                                                                   |
| hexiom                     | 5.96 ms                                                      | 6.50 ms: 1.09x slower                                                                  |
| python_startup             | 11.6 ms                                                      | 12.8 ms: 1.10x slower                                                                  |
| richards                   | 45.7 ms                                                      | 51.7 ms: 1.13x slower                                                                  |
| richards_super             | 51.3 ms                                                      | 58.3 ms: 1.13x slower                                                                  |
| telco                      | 6.96 ms                                                      | 7.91 ms: 1.14x slower                                                                  |
| pyflate                    | 439 ms                                                       | 507 ms: 1.16x slower                                                                   |
| go                         | 150 ms                                                       | 173 ms: 1.16x slower                                                                   |
| create_gc_cycles           | 1.59 ms                                                      | 1.92 ms: 1.21x slower                                                                  |
| scimark_sor                | 109 ms                                                       | 139 ms: 1.28x slower                                                                   |
| python_startup_no_site     | 8.64 ms                                                      | 11.0 ms: 1.28x slower                                                                  |
| gc_traversal               | 3.48 ms                                                      | 4.60 ms: 1.32x slower                                                                  |
| coverage                   | 66.7 ms                                                      | 89.1 ms: 1.34x slower                                                                  |
| Geometric mean             | (ref)                                                        | 1.00x faster                                                                           |

Benchmark hidden because not significant (6): dask, logging_silent, float, sqlglot_transpile, scimark_lu, sqlglot_normalize
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240405-3.13.0a5+-2c964fa/bm-20240405-pythonperf2-x86_64-faster%2dcpython-specialize_binary_op-3.13.0a5+-2c964fa.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 65.60% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.91x