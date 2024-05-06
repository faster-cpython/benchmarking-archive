# Results vs. 3.12.0

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: linux-x86_64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.03x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.01x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 300 ms: 1.05x slower                                                         |
| chameleon      | 7.23 ms                                                      | 7.58 ms: 1.05x slower                                                        |
| docutils       | 2.87 sec                                                     | 3.08 sec: 1.07x slower                                                       |
| tornado_http   | 121 ms                                                       | 124 ms: 1.03x slower                                                         |
| Geometric mean | (ref)                                                        | 1.05x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 338 ms: 1.28x faster                                                         |
| async_tree_none            | 452 ms                                                       | 358 ms: 1.26x faster                                                         |
| async_tree_memoization_tg  | 540 ms                                                       | 435 ms: 1.24x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 440 ms: 1.24x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 577 ms: 1.21x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 882 ms: 1.18x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 592 ms: 1.18x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 904 ms: 1.16x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.22x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 261 ms: 1.02x faster                                                         |
| float          | 76.6 ms                                                      | 78.5 ms: 1.02x slower                                                        |
| nbody          | 88.0 ms                                                      | 94.9 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_dna      | 239 ms                                                       | 242 ms: 1.02x slower                                                         |
| regex_compile  | 144 ms                                                       | 148 ms: 1.03x slower                                                         |
| regex_effbot   | 3.57 ms                                                      | 3.70 ms: 1.04x slower                                                        |
| regex_v8       | 23.6 ms                                                      | 25.6 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                        | 1.04x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| xml_etree_generate   | 86.1 ms                                                      | 84.1 ms: 1.02x faster                                                        |
| pickle_pure_python   | 318 us                                                       | 311 us: 1.02x faster                                                         |
| unpickle_list        | 4.66 us                                                      | 4.62 us: 1.01x faster                                                        |
| xml_etree_parse      | 144 ms                                                       | 143 ms: 1.00x faster                                                         |
| tomli_loads          | 2.16 sec                                                     | 2.17 sec: 1.01x slower                                                       |
| pickle_dict          | 32.5 us                                                      | 33.1 us: 1.02x slower                                                        |
| unpickle             | 14.8 us                                                      | 15.2 us: 1.03x slower                                                        |
| json_dumps           | 10.2 ms                                                      | 10.5 ms: 1.03x slower                                                        |
| pickle               | 10.5 us                                                      | 10.9 us: 1.04x slower                                                        |
| json_loads           | 24.4 us                                                      | 25.3 us: 1.04x slower                                                        |
| unpickle_pure_python | 210 us                                                       | 235 us: 1.12x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                                 |

Benchmark hidden because not significant (3): xml_etree_iterparse, pickle_list, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 13.6 ms: 1.17x slower                                                        |
| python_startup_no_site | 8.64 ms                                                      | 11.8 ms: 1.37x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.26x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 38.2 ms                                                      | 40.1 ms: 1.05x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                                 |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 338 ms: 1.28x faster                                                         |
| async_tree_none            | 452 ms                                                       | 358 ms: 1.26x faster                                                         |
| async_tree_memoization_tg  | 540 ms                                                       | 435 ms: 1.24x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 440 ms: 1.24x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 577 ms: 1.21x faster                                                         |
| typing_runtime_protocols   | 152 us                                                       | 128 us: 1.19x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 882 ms: 1.18x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 592 ms: 1.18x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 904 ms: 1.16x faster                                                         |
| generators                 | 37.4 ms                                                      | 33.6 ms: 1.11x faster                                                        |
| comprehensions             | 21.9 us                                                      | 20.1 us: 1.09x faster                                                        |
| crypto_pyaes               | 80.3 ms                                                      | 77.1 ms: 1.04x faster                                                        |
| logging_format             | 7.48 us                                                      | 7.24 us: 1.03x faster                                                        |
| sqlite_synth               | 2.77 us                                                      | 2.70 us: 1.03x faster                                                        |
| xml_etree_generate         | 86.1 ms                                                      | 84.1 ms: 1.02x faster                                                        |
| pickle_pure_python         | 318 us                                                       | 311 us: 1.02x faster                                                         |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.11 ms: 1.02x faster                                                        |
| asyncio_tcp                | 378 ms                                                       | 371 ms: 1.02x faster                                                         |
| logging_simple             | 6.71 us                                                      | 6.61 us: 1.02x faster                                                        |
| pidigits                   | 265 ms                                                       | 261 ms: 1.02x faster                                                         |
| coroutines                 | 23.0 ms                                                      | 22.7 ms: 1.01x faster                                                        |
| unpickle_list              | 4.66 us                                                      | 4.62 us: 1.01x faster                                                        |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.01x faster                                                       |
| sympy_sum                  | 162 ms                                                       | 161 ms: 1.00x faster                                                         |
| xml_etree_parse            | 144 ms                                                       | 143 ms: 1.00x faster                                                         |
| sympy_str                  | 302 ms                                                       | 304 ms: 1.01x slower                                                         |
| tomli_loads                | 2.16 sec                                                     | 2.17 sec: 1.01x slower                                                       |
| async_generators           | 390 ms                                                       | 395 ms: 1.01x slower                                                         |
| regex_dna                  | 239 ms                                                       | 242 ms: 1.02x slower                                                         |
| spectral_norm              | 91.6 ms                                                      | 93.2 ms: 1.02x slower                                                        |
| pickle_dict                | 32.5 us                                                      | 33.1 us: 1.02x slower                                                        |
| mdp                        | 2.57 sec                                                     | 2.62 sec: 1.02x slower                                                       |
| raytrace                   | 298 ms                                                       | 304 ms: 1.02x slower                                                         |
| pycparser                  | 1.23 sec                                                     | 1.26 sec: 1.02x slower                                                       |
| float                      | 76.6 ms                                                      | 78.5 ms: 1.02x slower                                                        |
| dask                       | 392 ms                                                       | 402 ms: 1.03x slower                                                         |
| unpickle                   | 14.8 us                                                      | 15.2 us: 1.03x slower                                                        |
| tornado_http               | 121 ms                                                       | 124 ms: 1.03x slower                                                         |
| json_dumps                 | 10.2 ms                                                      | 10.5 ms: 1.03x slower                                                        |
| regex_compile              | 144 ms                                                       | 148 ms: 1.03x slower                                                         |
| sqlglot_transpile          | 1.78 ms                                                      | 1.83 ms: 1.03x slower                                                        |
| deepcopy_reduce            | 3.37 us                                                      | 3.48 us: 1.03x slower                                                        |
| pprint_pformat             | 1.65 sec                                                     | 1.71 sec: 1.03x slower                                                       |
| pprint_safe_repr           | 807 ms                                                       | 836 ms: 1.04x slower                                                         |
| regex_effbot               | 3.57 ms                                                      | 3.70 ms: 1.04x slower                                                        |
| pickle                     | 10.5 us                                                      | 10.9 us: 1.04x slower                                                        |
| sqlglot_parse              | 1.38 ms                                                      | 1.43 ms: 1.04x slower                                                        |
| json_loads                 | 24.4 us                                                      | 25.3 us: 1.04x slower                                                        |
| logging_silent             | 94.4 ns                                                      | 98.3 ns: 1.04x slower                                                        |
| bench_mp_pool              | 4.76 ms                                                      | 4.97 ms: 1.04x slower                                                        |
| pathlib                    | 18.9 ms                                                      | 19.8 ms: 1.05x slower                                                        |
| meteor_contest             | 128 ms                                                       | 134 ms: 1.05x slower                                                         |
| chameleon                  | 7.23 ms                                                      | 7.58 ms: 1.05x slower                                                        |
| django_template            | 38.2 ms                                                      | 40.1 ms: 1.05x slower                                                        |
| 2to3                       | 285 ms                                                       | 300 ms: 1.05x slower                                                         |
| scimark_fft                | 301 ms                                                       | 318 ms: 1.06x slower                                                         |
| scimark_monte_carlo        | 69.0 ms                                                      | 72.9 ms: 1.06x slower                                                        |
| sympy_integrate            | 23.9 ms                                                      | 25.3 ms: 1.06x slower                                                        |
| dulwich_log                | 65.4 ms                                                      | 69.2 ms: 1.06x slower                                                        |
| sympy_expand               | 484 ms                                                       | 513 ms: 1.06x slower                                                         |
| chaos                      | 64.0 ms                                                      | 67.9 ms: 1.06x slower                                                        |
| json                       | 5.12 ms                                                      | 5.44 ms: 1.06x slower                                                        |
| docutils                   | 2.87 sec                                                     | 3.08 sec: 1.07x slower                                                       |
| nbody                      | 88.0 ms                                                      | 94.9 ms: 1.08x slower                                                        |
| sqlglot_normalize          | 116 ms                                                       | 125 ms: 1.08x slower                                                         |
| deepcopy                   | 368 us                                                       | 398 us: 1.08x slower                                                         |
| fannkuch                   | 350 ms                                                       | 379 ms: 1.08x slower                                                         |
| regex_v8                   | 23.6 ms                                                      | 25.6 ms: 1.08x slower                                                        |
| deepcopy_memo              | 36.8 us                                                      | 39.9 us: 1.08x slower                                                        |
| gunicorn                   | 1.00 ms                                                      | 1.09 ms: 1.09x slower                                                        |
| sqlglot_optimize           | 57.5 ms                                                      | 63.1 ms: 1.10x slower                                                        |
| aiohttp                    | 1.02 ms                                                      | 1.12 ms: 1.10x slower                                                        |
| unpack_sequence            | 53.2 ns                                                      | 58.9 ns: 1.11x slower                                                        |
| richards                   | 45.7 ms                                                      | 51.3 ms: 1.12x slower                                                        |
| unpickle_pure_python       | 210 us                                                       | 235 us: 1.12x slower                                                         |
| create_gc_cycles           | 1.59 ms                                                      | 1.80 ms: 1.13x slower                                                        |
| richards_super             | 51.3 ms                                                      | 58.4 ms: 1.14x slower                                                        |
| nqueens                    | 89.9 ms                                                      | 103 ms: 1.14x slower                                                         |
| telco                      | 6.96 ms                                                      | 8.00 ms: 1.15x slower                                                        |
| deltablue                  | 3.24 ms                                                      | 3.75 ms: 1.16x slower                                                        |
| python_startup             | 11.6 ms                                                      | 13.6 ms: 1.17x slower                                                        |
| pyflate                    | 439 ms                                                       | 514 ms: 1.17x slower                                                         |
| go                         | 150 ms                                                       | 175 ms: 1.17x slower                                                         |
| bench_thread_pool          | 950 us                                                       | 1.13 ms: 1.19x slower                                                        |
| coverage                   | 66.7 ms                                                      | 82.4 ms: 1.24x slower                                                        |
| hexiom                     | 5.96 ms                                                      | 7.59 ms: 1.27x slower                                                        |
| scimark_lu                 | 98.8 ms                                                      | 127 ms: 1.29x slower                                                         |
| gc_traversal               | 3.48 ms                                                      | 4.57 ms: 1.31x slower                                                        |
| python_startup_no_site     | 8.64 ms                                                      | 11.8 ms: 1.37x slower                                                        |
| scimark_sor                | 109 ms                                                       | 154 ms: 1.41x slower                                                         |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                                 |

Benchmark hidden because not significant (6): xml_etree_iterparse, pickle_list, xml_etree_process, asyncio_websockets, mypy2, mako
Ignored benchmarks (2) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240329-3.13.0a5+-bfc57d4-JIT/bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 0.99x