# Results vs. 3.12.0

- fork: mdboom
- ref: tier2_func_simple
- machine: linux-x86_64
- commit hash: 7a3c89e
- commit date: 2024-04-04
- overall geometric mean: 1.03x slower
- HPT reliability: 99.83%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 300 ms: 1.05x slower                                                      |
| chameleon      | 7.23 ms                                                      | 7.26 ms: 1.00x slower                                                     |
| docutils       | 2.87 sec                                                     | 3.07 sec: 1.07x slower                                                    |
| Geometric mean | (ref)                                                        | 1.03x slower                                                              |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 338 ms: 1.27x faster                                                      |
| async_tree_none            | 452 ms                                                       | 358 ms: 1.26x faster                                                      |
| async_tree_memoization_tg  | 540 ms                                                       | 437 ms: 1.24x faster                                                      |
| async_tree_memoization     | 544 ms                                                       | 440 ms: 1.23x faster                                                      |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 576 ms: 1.21x faster                                                      |
| async_tree_io              | 1.04 sec                                                     | 886 ms: 1.18x faster                                                      |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 595 ms: 1.17x faster                                                      |
| async_tree_io_tg           | 1.05 sec                                                     | 910 ms: 1.16x faster                                                      |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 261 ms: 1.01x faster                                                      |
| nbody          | 88.0 ms                                                      | 97.8 ms: 1.11x slower                                                     |
| Geometric mean | (ref)                                                        | 1.03x slower                                                              |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_dna      | 239 ms                                                       | 242 ms: 1.02x slower                                                      |
| regex_compile  | 144 ms                                                       | 148 ms: 1.03x slower                                                      |
| regex_effbot   | 3.57 ms                                                      | 3.72 ms: 1.04x slower                                                     |
| regex_v8       | 23.6 ms                                                      | 25.5 ms: 1.08x slower                                                     |
| Geometric mean | (ref)                                                        | 1.04x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pickle_pure_python   | 318 us                                                       | 305 us: 1.04x faster                                                      |
| xml_etree_generate   | 86.1 ms                                                      | 84.9 ms: 1.02x faster                                                     |
| xml_etree_parse      | 144 ms                                                       | 143 ms: 1.01x faster                                                      |
| unpickle_list        | 4.66 us                                                      | 4.63 us: 1.01x faster                                                     |
| pickle_dict          | 32.5 us                                                      | 32.9 us: 1.01x slower                                                     |
| xml_etree_process    | 58.4 ms                                                      | 59.0 ms: 1.01x slower                                                     |
| unpickle             | 14.8 us                                                      | 15.1 us: 1.02x slower                                                     |
| pickle               | 10.5 us                                                      | 10.9 us: 1.04x slower                                                     |
| json_loads           | 24.4 us                                                      | 25.3 us: 1.04x slower                                                     |
| json_dumps           | 10.2 ms                                                      | 10.8 ms: 1.06x slower                                                     |
| unpickle_pure_python | 210 us                                                       | 233 us: 1.11x slower                                                      |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                              |

Benchmark hidden because not significant (3): pickle_list, tomli_loads, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                     |
| python_startup_no_site | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                     |
| Geometric mean         | (ref)                                                        | 1.26x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 38.2 ms                                                      | 39.9 ms: 1.04x slower                                                     |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                              |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 338 ms: 1.27x faster                                                      |
| typing_runtime_protocols   | 152 us                                                       | 120 us: 1.27x faster                                                      |
| async_tree_none            | 452 ms                                                       | 358 ms: 1.26x faster                                                      |
| async_tree_memoization_tg  | 540 ms                                                       | 437 ms: 1.24x faster                                                      |
| async_tree_memoization     | 544 ms                                                       | 440 ms: 1.23x faster                                                      |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 576 ms: 1.21x faster                                                      |
| async_tree_io              | 1.04 sec                                                     | 886 ms: 1.18x faster                                                      |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 595 ms: 1.17x faster                                                      |
| async_tree_io_tg           | 1.05 sec                                                     | 910 ms: 1.16x faster                                                      |
| generators                 | 37.4 ms                                                      | 33.5 ms: 1.12x faster                                                     |
| comprehensions             | 21.9 us                                                      | 19.7 us: 1.11x faster                                                     |
| pickle_pure_python         | 318 us                                                       | 305 us: 1.04x faster                                                      |
| crypto_pyaes               | 80.3 ms                                                      | 77.4 ms: 1.04x faster                                                     |
| coroutines                 | 23.0 ms                                                      | 22.4 ms: 1.03x faster                                                     |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.09 ms: 1.03x faster                                                     |
| logging_format             | 7.48 us                                                      | 7.29 us: 1.03x faster                                                     |
| sqlite_synth               | 2.77 us                                                      | 2.70 us: 1.03x faster                                                     |
| asyncio_tcp                | 378 ms                                                       | 372 ms: 1.02x faster                                                      |
| xml_etree_generate         | 86.1 ms                                                      | 84.9 ms: 1.02x faster                                                     |
| pidigits                   | 265 ms                                                       | 261 ms: 1.01x faster                                                      |
| async_generators           | 390 ms                                                       | 385 ms: 1.01x faster                                                      |
| logging_simple             | 6.71 us                                                      | 6.64 us: 1.01x faster                                                     |
| xml_etree_parse            | 144 ms                                                       | 143 ms: 1.01x faster                                                      |
| unpickle_list              | 4.66 us                                                      | 4.63 us: 1.01x faster                                                     |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.01x faster                                                    |
| sympy_sum                  | 162 ms                                                       | 161 ms: 1.00x faster                                                      |
| chameleon                  | 7.23 ms                                                      | 7.26 ms: 1.00x slower                                                     |
| sqlglot_transpile          | 1.78 ms                                                      | 1.79 ms: 1.01x slower                                                     |
| pickle_dict                | 32.5 us                                                      | 32.9 us: 1.01x slower                                                     |
| xml_etree_process          | 58.4 ms                                                      | 59.0 ms: 1.01x slower                                                     |
| pycparser                  | 1.23 sec                                                     | 1.25 sec: 1.01x slower                                                    |
| regex_dna                  | 239 ms                                                       | 242 ms: 1.02x slower                                                      |
| sqlglot_parse              | 1.38 ms                                                      | 1.40 ms: 1.02x slower                                                     |
| unpickle                   | 14.8 us                                                      | 15.1 us: 1.02x slower                                                     |
| deepcopy_reduce            | 3.37 us                                                      | 3.45 us: 1.02x slower                                                     |
| raytrace                   | 298 ms                                                       | 305 ms: 1.02x slower                                                      |
| logging_silent             | 94.4 ns                                                      | 97.0 ns: 1.03x slower                                                     |
| pathlib                    | 18.9 ms                                                      | 19.4 ms: 1.03x slower                                                     |
| spectral_norm              | 91.6 ms                                                      | 94.3 ms: 1.03x slower                                                     |
| regex_compile              | 144 ms                                                       | 148 ms: 1.03x slower                                                      |
| mdp                        | 2.57 sec                                                     | 2.65 sec: 1.03x slower                                                    |
| pprint_safe_repr           | 807 ms                                                       | 834 ms: 1.03x slower                                                      |
| meteor_contest             | 128 ms                                                       | 132 ms: 1.03x slower                                                      |
| dask                       | 392 ms                                                       | 406 ms: 1.04x slower                                                      |
| pprint_pformat             | 1.65 sec                                                     | 1.71 sec: 1.04x slower                                                    |
| pickle                     | 10.5 us                                                      | 10.9 us: 1.04x slower                                                     |
| scimark_fft                | 301 ms                                                       | 313 ms: 1.04x slower                                                      |
| deepcopy_memo              | 36.8 us                                                      | 38.2 us: 1.04x slower                                                     |
| json_loads                 | 24.4 us                                                      | 25.3 us: 1.04x slower                                                     |
| regex_effbot               | 3.57 ms                                                      | 3.72 ms: 1.04x slower                                                     |
| chaos                      | 64.0 ms                                                      | 66.6 ms: 1.04x slower                                                     |
| deepcopy                   | 368 us                                                       | 384 us: 1.04x slower                                                      |
| sympy_integrate            | 23.9 ms                                                      | 25.0 ms: 1.04x slower                                                     |
| django_template            | 38.2 ms                                                      | 39.9 ms: 1.04x slower                                                     |
| sympy_expand               | 484 ms                                                       | 507 ms: 1.05x slower                                                      |
| json                       | 5.12 ms                                                      | 5.37 ms: 1.05x slower                                                     |
| 2to3                       | 285 ms                                                       | 300 ms: 1.05x slower                                                      |
| sqlglot_normalize          | 116 ms                                                       | 122 ms: 1.06x slower                                                      |
| json_dumps                 | 10.2 ms                                                      | 10.8 ms: 1.06x slower                                                     |
| dulwich_log                | 65.4 ms                                                      | 69.7 ms: 1.07x slower                                                     |
| scimark_monte_carlo        | 69.0 ms                                                      | 73.7 ms: 1.07x slower                                                     |
| docutils                   | 2.87 sec                                                     | 3.07 sec: 1.07x slower                                                    |
| bench_mp_pool              | 4.76 ms                                                      | 5.14 ms: 1.08x slower                                                     |
| regex_v8                   | 23.6 ms                                                      | 25.5 ms: 1.08x slower                                                     |
| gunicorn                   | 1.00 ms                                                      | 1.09 ms: 1.09x slower                                                     |
| sqlglot_optimize           | 57.5 ms                                                      | 62.8 ms: 1.09x slower                                                     |
| fannkuch                   | 350 ms                                                       | 384 ms: 1.10x slower                                                      |
| richards                   | 45.7 ms                                                      | 50.2 ms: 1.10x slower                                                     |
| aiohttp                    | 1.02 ms                                                      | 1.12 ms: 1.10x slower                                                     |
| nbody                      | 88.0 ms                                                      | 97.8 ms: 1.11x slower                                                     |
| richards_super             | 51.3 ms                                                      | 57.1 ms: 1.11x slower                                                     |
| unpickle_pure_python       | 210 us                                                       | 233 us: 1.11x slower                                                      |
| create_gc_cycles           | 1.59 ms                                                      | 1.79 ms: 1.13x slower                                                     |
| pyflate                    | 439 ms                                                       | 496 ms: 1.13x slower                                                      |
| nqueens                    | 89.9 ms                                                      | 103 ms: 1.14x slower                                                      |
| deltablue                  | 3.24 ms                                                      | 3.72 ms: 1.15x slower                                                     |
| go                         | 150 ms                                                       | 173 ms: 1.15x slower                                                      |
| python_startup             | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                     |
| bench_thread_pool          | 950 us                                                       | 1.12 ms: 1.18x slower                                                     |
| telco                      | 6.96 ms                                                      | 8.22 ms: 1.18x slower                                                     |
| scimark_lu                 | 98.8 ms                                                      | 119 ms: 1.21x slower                                                      |
| coverage                   | 66.7 ms                                                      | 80.6 ms: 1.21x slower                                                     |
| gc_traversal               | 3.48 ms                                                      | 4.35 ms: 1.25x slower                                                     |
| hexiom                     | 5.96 ms                                                      | 7.52 ms: 1.26x slower                                                     |
| python_startup_no_site     | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                     |
| scimark_sor                | 109 ms                                                       | 153 ms: 1.40x slower                                                      |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                              |

Benchmark hidden because not significant (9): mypy2, pickle_list, mako, float, sympy_str, tomli_loads, asyncio_websockets, xml_etree_iterparse, tornado_http
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240404-3.13.0a5+-7a3c89e-JIT/bm-20240404-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-7a3c89e.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.83% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.98x