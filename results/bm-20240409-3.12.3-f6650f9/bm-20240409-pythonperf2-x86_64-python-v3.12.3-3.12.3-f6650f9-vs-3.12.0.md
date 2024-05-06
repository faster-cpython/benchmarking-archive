# Results vs. 3.12.0

- fork: python
- ref: v3.12.3
- machine: linux-x86_64
- commit hash: f6650f9
- commit date: 2024-04-09
- overall geometric mean: 1.01x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.91x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 279 ms: 1.02x faster                                         |
| docutils       | 2.87 sec                                                     | 2.85 sec: 1.01x faster                                       |
| tornado_http   | 121 ms                                                       | 120 ms: 1.01x faster                                         |
| Geometric mean | (ref)                                                        | 1.01x faster                                                 |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|--------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg   | 1.05 sec                                                     | 1.05 sec: 1.01x faster                                       |
| async_tree_none_tg | 431 ms                                                       | 428 ms: 1.01x faster                                         |
| Geometric mean     | (ref)                                                        | 1.00x faster                                                 |

Benchmark hidden because not significant (6): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_memoization_tg, async_tree_none, async_tree_io, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| nbody          | 88.0 ms                                                      | 86.3 ms: 1.02x faster                                        |
| pidigits       | 265 ms                                                       | 264 ms: 1.00x faster                                         |
| float          | 76.6 ms                                                      | 77.7 ms: 1.01x slower                                        |
| Geometric mean | (ref)                                                        | 1.00x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.45 ms: 1.04x faster                                        |
| regex_dna      | 239 ms                                                       | 237 ms: 1.01x faster                                         |
| regex_v8       | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                        |
| Geometric mean | (ref)                                                        | 1.01x faster                                                 |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 30.6 us: 1.06x faster                                        |
| pickle               | 10.5 us                                                      | 10.2 us: 1.04x faster                                        |
| unpickle_pure_python | 210 us                                                       | 205 us: 1.02x faster                                         |
| pickle_pure_python   | 318 us                                                       | 312 us: 1.02x faster                                         |
| unpickle             | 14.8 us                                                      | 14.7 us: 1.00x faster                                        |
| xml_etree_process    | 58.4 ms                                                      | 58.1 ms: 1.00x faster                                        |
| tomli_loads          | 2.16 sec                                                     | 2.17 sec: 1.01x slower                                       |
| xml_etree_generate   | 86.1 ms                                                      | 86.8 ms: 1.01x slower                                        |
| json_dumps           | 10.2 ms                                                      | 10.3 ms: 1.01x slower                                        |
| xml_etree_iterparse  | 103 ms                                                       | 105 ms: 1.02x slower                                         |
| unpickle_list        | 4.66 us                                                      | 4.78 us: 1.03x slower                                        |
| xml_etree_parse      | 144 ms                                                       | 149 ms: 1.04x slower                                         |
| json_loads           | 24.4 us                                                      | 28.2 us: 1.16x slower                                        |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                 |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 8.64 ms                                                      | 8.57 ms: 1.01x faster                                        |
| python_startup         | 11.6 ms                                                      | 11.6 ms: 1.00x faster                                        |
| Geometric mean         | (ref)                                                        | 1.00x faster                                                 |

Benchmarks with tag 'template':
===============================

Benchmark hidden because not significant (2): mako, django_template

All benchmarks:
===============

| Benchmark                | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9 |
|--------------------------|:------------------------------------------------------------:|:------------------------------------------------------------:|
| comprehensions           | 21.9 us                                                      | 16.6 us: 1.32x faster                                        |
| typing_runtime_protocols | 152 us                                                       | 125 us: 1.22x faster                                         |
| mypy2                    | 830 ms                                                       | 734 ms: 1.13x faster                                         |
| bench_mp_pool            | 4.76 ms                                                      | 4.41 ms: 1.08x faster                                        |
| sympy_sum                | 162 ms                                                       | 152 ms: 1.07x faster                                         |
| pickle_dict              | 32.5 us                                                      | 30.6 us: 1.06x faster                                        |
| sympy_str                | 302 ms                                                       | 287 ms: 1.05x faster                                         |
| fannkuch                 | 350 ms                                                       | 333 ms: 1.05x faster                                         |
| richards                 | 45.7 ms                                                      | 43.8 ms: 1.04x faster                                        |
| sympy_integrate          | 23.9 ms                                                      | 23.0 ms: 1.04x faster                                        |
| create_gc_cycles         | 1.59 ms                                                      | 1.53 ms: 1.04x faster                                        |
| pickle                   | 10.5 us                                                      | 10.2 us: 1.04x faster                                        |
| regex_effbot             | 3.57 ms                                                      | 3.45 ms: 1.04x faster                                        |
| richards_super           | 51.3 ms                                                      | 49.6 ms: 1.03x faster                                        |
| deepcopy_memo            | 36.8 us                                                      | 35.6 us: 1.03x faster                                        |
| logging_format           | 7.48 us                                                      | 7.26 us: 1.03x faster                                        |
| mdp                      | 2.57 sec                                                     | 2.50 sec: 1.03x faster                                       |
| chaos                    | 64.0 ms                                                      | 62.3 ms: 1.03x faster                                        |
| nqueens                  | 89.9 ms                                                      | 87.7 ms: 1.02x faster                                        |
| unpickle_pure_python     | 210 us                                                       | 205 us: 1.02x faster                                         |
| async_generators         | 390 ms                                                       | 381 ms: 1.02x faster                                         |
| go                       | 150 ms                                                       | 146 ms: 1.02x faster                                         |
| 2to3                     | 285 ms                                                       | 279 ms: 1.02x faster                                         |
| hexiom                   | 5.96 ms                                                      | 5.84 ms: 1.02x faster                                        |
| pickle_pure_python       | 318 us                                                       | 312 us: 1.02x faster                                         |
| nbody                    | 88.0 ms                                                      | 86.3 ms: 1.02x faster                                        |
| scimark_monte_carlo      | 69.0 ms                                                      | 67.8 ms: 1.02x faster                                        |
| pprint_pformat           | 1.65 sec                                                     | 1.63 sec: 1.02x faster                                       |
| crypto_pyaes             | 80.3 ms                                                      | 79.1 ms: 1.02x faster                                        |
| deepcopy                 | 368 us                                                       | 363 us: 1.02x faster                                         |
| pyflate                  | 439 ms                                                       | 432 ms: 1.02x faster                                         |
| asyncio_tcp_ssl          | 1.59 sec                                                     | 1.56 sec: 1.02x faster                                       |
| deepcopy_reduce          | 3.37 us                                                      | 3.32 us: 1.02x faster                                        |
| tornado_http             | 121 ms                                                       | 120 ms: 1.01x faster                                         |
| logging_silent           | 94.4 ns                                                      | 93.1 ns: 1.01x faster                                        |
| scimark_fft              | 301 ms                                                       | 297 ms: 1.01x faster                                         |
| generators               | 37.4 ms                                                      | 36.9 ms: 1.01x faster                                        |
| pprint_safe_repr         | 807 ms                                                       | 797 ms: 1.01x faster                                         |
| sqlalchemy_imperative    | 18.7 ms                                                      | 18.5 ms: 1.01x faster                                        |
| sqlite_synth             | 2.77 us                                                      | 2.74 us: 1.01x faster                                        |
| logging_simple           | 6.71 us                                                      | 6.65 us: 1.01x faster                                        |
| dulwich_log              | 65.4 ms                                                      | 64.8 ms: 1.01x faster                                        |
| regex_dna                | 239 ms                                                       | 237 ms: 1.01x faster                                         |
| pathlib                  | 18.9 ms                                                      | 18.7 ms: 1.01x faster                                        |
| python_startup_no_site   | 8.64 ms                                                      | 8.57 ms: 1.01x faster                                        |
| docutils                 | 2.87 sec                                                     | 2.85 sec: 1.01x faster                                       |
| async_tree_io_tg         | 1.05 sec                                                     | 1.05 sec: 1.01x faster                                       |
| scimark_sor              | 109 ms                                                       | 108 ms: 1.01x faster                                         |
| async_tree_none_tg       | 431 ms                                                       | 428 ms: 1.01x faster                                         |
| meteor_contest           | 128 ms                                                       | 127 ms: 1.01x faster                                         |
| unpickle                 | 14.8 us                                                      | 14.7 us: 1.00x faster                                        |
| xml_etree_process        | 58.4 ms                                                      | 58.1 ms: 1.00x faster                                        |
| pidigits                 | 265 ms                                                       | 264 ms: 1.00x faster                                         |
| sympy_expand             | 484 ms                                                       | 483 ms: 1.00x faster                                         |
| python_startup           | 11.6 ms                                                      | 11.6 ms: 1.00x faster                                        |
| tomli_loads              | 2.16 sec                                                     | 2.17 sec: 1.01x slower                                       |
| regex_v8                 | 23.6 ms                                                      | 23.8 ms: 1.01x slower                                        |
| xml_etree_generate       | 86.1 ms                                                      | 86.8 ms: 1.01x slower                                        |
| json_dumps               | 10.2 ms                                                      | 10.3 ms: 1.01x slower                                        |
| sqlglot_optimize         | 57.5 ms                                                      | 58.0 ms: 1.01x slower                                        |
| float                    | 76.6 ms                                                      | 77.7 ms: 1.01x slower                                        |
| raytrace                 | 298 ms                                                       | 302 ms: 1.01x slower                                         |
| xml_etree_iterparse      | 103 ms                                                       | 105 ms: 1.02x slower                                         |
| unpickle_list            | 4.66 us                                                      | 4.78 us: 1.03x slower                                        |
| spectral_norm            | 91.6 ms                                                      | 94.6 ms: 1.03x slower                                        |
| pycparser                | 1.23 sec                                                     | 1.28 sec: 1.03x slower                                       |
| scimark_sparse_mat_mult  | 4.21 ms                                                      | 4.37 ms: 1.04x slower                                        |
| xml_etree_parse          | 144 ms                                                       | 149 ms: 1.04x slower                                         |
| gc_traversal             | 3.48 ms                                                      | 3.72 ms: 1.07x slower                                        |
| json                     | 5.12 ms                                                      | 5.56 ms: 1.09x slower                                        |
| json_loads               | 24.4 us                                                      | 28.2 us: 1.16x slower                                        |
| Geometric mean           | (ref)                                                        | 1.01x faster                                                 |

Benchmark hidden because not significant (26): dask, async_tree_cpu_io_mixed_tg, coroutines, async_tree_cpu_io_mixed, mako, django_template, async_tree_memoization_tg, pickle_list, sqlglot_transpile, coverage, telco, deltablue, async_tree_none, chameleon, sqlglot_parse, sqlglot_normalize, regex_compile, asyncio_tcp, async_tree_io, aiohttp, sqlalchemy_declarative, gunicorn, scimark_lu, async_tree_memoization, asyncio_websockets, bench_thread_pool
Ignored benchmarks (1) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: unpack_sequence
Ignored benchmarks (5) of results/bm-20240409-3.12.3-f6650f9/bm-20240409-pythonperf2-x86_64-python-v3.12.3-3.12.3-f6650f9.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.91x