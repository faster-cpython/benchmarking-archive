# Results vs. 3.12.0

- fork: python
- ref: d9cfe7e565a6e2dc1574
- machine: linux-x86_64
- commit hash: d9cfe7e
- commit date: 2024-03-29
- overall geometric mean: 1.03x slower
- HPT reliability: 99.96%
- HPT 99th percentile: 1.01x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 300 ms: 1.05x slower                                                         |
| chameleon      | 7.23 ms                                                      | 7.43 ms: 1.03x slower                                                        |
| docutils       | 2.87 sec                                                     | 3.07 sec: 1.07x slower                                                       |
| tornado_http   | 121 ms                                                       | 124 ms: 1.03x slower                                                         |
| Geometric mean | (ref)                                                        | 1.04x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 341 ms: 1.26x faster                                                         |
| async_tree_memoization_tg  | 540 ms                                                       | 431 ms: 1.25x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 454 ms: 1.20x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 880 ms: 1.20x faster                                                         |
| async_tree_none            | 452 ms                                                       | 377 ms: 1.20x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 596 ms: 1.17x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 600 ms: 1.16x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 907 ms: 1.15x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.20x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 261 ms: 1.01x faster                                                         |
| float          | 76.6 ms                                                      | 79.5 ms: 1.04x slower                                                        |
| nbody          | 88.0 ms                                                      | 98.3 ms: 1.12x slower                                                        |
| Geometric mean | (ref)                                                        | 1.05x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.42 ms: 1.04x faster                                                        |
| regex_dna      | 239 ms                                                       | 244 ms: 1.02x slower                                                         |
| regex_compile  | 144 ms                                                       | 148 ms: 1.03x slower                                                         |
| regex_v8       | 23.6 ms                                                      | 26.1 ms: 1.10x slower                                                        |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| xml_etree_generate   | 86.1 ms                                                      | 83.9 ms: 1.03x faster                                                        |
| pickle_list          | 4.43 us                                                      | 4.38 us: 1.01x faster                                                        |
| unpickle_list        | 4.66 us                                                      | 4.62 us: 1.01x faster                                                        |
| pickle_pure_python   | 318 us                                                       | 316 us: 1.01x faster                                                         |
| xml_etree_iterparse  | 103 ms                                                       | 104 ms: 1.01x slower                                                         |
| pickle_dict          | 32.5 us                                                      | 33.0 us: 1.01x slower                                                        |
| json_dumps           | 10.2 ms                                                      | 10.5 ms: 1.03x slower                                                        |
| pickle               | 10.5 us                                                      | 10.9 us: 1.03x slower                                                        |
| unpickle             | 14.8 us                                                      | 15.5 us: 1.05x slower                                                        |
| json_loads           | 24.4 us                                                      | 25.8 us: 1.06x slower                                                        |
| unpickle_pure_python | 210 us                                                       | 235 us: 1.12x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.02x slower                                                                 |

Benchmark hidden because not significant (3): xml_etree_parse, xml_etree_process, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                        |
| python_startup_no_site | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.26x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 38.2 ms                                                      | 41.2 ms: 1.08x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.04x slower                                                                 |

Benchmark hidden because not significant (1): mako

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 341 ms: 1.26x faster                                                         |
| async_tree_memoization_tg  | 540 ms                                                       | 431 ms: 1.25x faster                                                         |
| typing_runtime_protocols   | 152 us                                                       | 122 us: 1.24x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 454 ms: 1.20x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 880 ms: 1.20x faster                                                         |
| async_tree_none            | 452 ms                                                       | 377 ms: 1.20x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 596 ms: 1.17x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 600 ms: 1.16x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 907 ms: 1.15x faster                                                         |
| comprehensions             | 21.9 us                                                      | 19.7 us: 1.11x faster                                                        |
| generators                 | 37.4 ms                                                      | 34.6 ms: 1.08x faster                                                        |
| regex_effbot               | 3.57 ms                                                      | 3.42 ms: 1.04x faster                                                        |
| crypto_pyaes               | 80.3 ms                                                      | 77.5 ms: 1.04x faster                                                        |
| xml_etree_generate         | 86.1 ms                                                      | 83.9 ms: 1.03x faster                                                        |
| coroutines                 | 23.0 ms                                                      | 22.5 ms: 1.02x faster                                                        |
| sqlite_synth               | 2.77 us                                                      | 2.71 us: 1.02x faster                                                        |
| logging_format             | 7.48 us                                                      | 7.33 us: 1.02x faster                                                        |
| asyncio_tcp                | 378 ms                                                       | 372 ms: 1.02x faster                                                         |
| pidigits                   | 265 ms                                                       | 261 ms: 1.01x faster                                                         |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.15 ms: 1.01x faster                                                        |
| pickle_list                | 4.43 us                                                      | 4.38 us: 1.01x faster                                                        |
| unpickle_list              | 4.66 us                                                      | 4.62 us: 1.01x faster                                                        |
| pickle_pure_python         | 318 us                                                       | 316 us: 1.01x faster                                                         |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.01x faster                                                       |
| sympy_sum                  | 162 ms                                                       | 163 ms: 1.00x slower                                                         |
| sympy_str                  | 302 ms                                                       | 304 ms: 1.00x slower                                                         |
| deepcopy_reduce            | 3.37 us                                                      | 3.40 us: 1.01x slower                                                        |
| xml_etree_iterparse        | 103 ms                                                       | 104 ms: 1.01x slower                                                         |
| logging_simple             | 6.71 us                                                      | 6.80 us: 1.01x slower                                                        |
| pickle_dict                | 32.5 us                                                      | 33.0 us: 1.01x slower                                                        |
| spectral_norm              | 91.6 ms                                                      | 93.2 ms: 1.02x slower                                                        |
| mdp                        | 2.57 sec                                                     | 2.62 sec: 1.02x slower                                                       |
| meteor_contest             | 128 ms                                                       | 131 ms: 1.02x slower                                                         |
| regex_dna                  | 239 ms                                                       | 244 ms: 1.02x slower                                                         |
| tornado_http               | 121 ms                                                       | 124 ms: 1.03x slower                                                         |
| json_dumps                 | 10.2 ms                                                      | 10.5 ms: 1.03x slower                                                        |
| chameleon                  | 7.23 ms                                                      | 7.43 ms: 1.03x slower                                                        |
| pathlib                    | 18.9 ms                                                      | 19.4 ms: 1.03x slower                                                        |
| regex_compile              | 144 ms                                                       | 148 ms: 1.03x slower                                                         |
| logging_silent             | 94.4 ns                                                      | 97.2 ns: 1.03x slower                                                        |
| pickle                     | 10.5 us                                                      | 10.9 us: 1.03x slower                                                        |
| raytrace                   | 298 ms                                                       | 308 ms: 1.03x slower                                                         |
| scimark_fft                | 301 ms                                                       | 312 ms: 1.04x slower                                                         |
| float                      | 76.6 ms                                                      | 79.5 ms: 1.04x slower                                                        |
| sqlglot_transpile          | 1.78 ms                                                      | 1.84 ms: 1.04x slower                                                        |
| dask                       | 392 ms                                                       | 408 ms: 1.04x slower                                                         |
| pprint_safe_repr           | 807 ms                                                       | 841 ms: 1.04x slower                                                         |
| pprint_pformat             | 1.65 sec                                                     | 1.72 sec: 1.04x slower                                                       |
| deepcopy_memo              | 36.8 us                                                      | 38.3 us: 1.04x slower                                                        |
| pycparser                  | 1.23 sec                                                     | 1.29 sec: 1.04x slower                                                       |
| unpickle                   | 14.8 us                                                      | 15.5 us: 1.05x slower                                                        |
| sqlglot_parse              | 1.38 ms                                                      | 1.45 ms: 1.05x slower                                                        |
| 2to3                       | 285 ms                                                       | 300 ms: 1.05x slower                                                         |
| deepcopy                   | 368 us                                                       | 388 us: 1.05x slower                                                         |
| chaos                      | 64.0 ms                                                      | 67.5 ms: 1.05x slower                                                        |
| json                       | 5.12 ms                                                      | 5.41 ms: 1.06x slower                                                        |
| scimark_monte_carlo        | 69.0 ms                                                      | 72.9 ms: 1.06x slower                                                        |
| json_loads                 | 24.4 us                                                      | 25.8 us: 1.06x slower                                                        |
| sympy_integrate            | 23.9 ms                                                      | 25.3 ms: 1.06x slower                                                        |
| sympy_expand               | 484 ms                                                       | 512 ms: 1.06x slower                                                         |
| dulwich_log                | 65.4 ms                                                      | 69.8 ms: 1.07x slower                                                        |
| docutils                   | 2.87 sec                                                     | 3.07 sec: 1.07x slower                                                       |
| sqlglot_normalize          | 116 ms                                                       | 125 ms: 1.08x slower                                                         |
| django_template            | 38.2 ms                                                      | 41.2 ms: 1.08x slower                                                        |
| fannkuch                   | 350 ms                                                       | 379 ms: 1.08x slower                                                         |
| bench_mp_pool              | 4.76 ms                                                      | 5.16 ms: 1.08x slower                                                        |
| gunicorn                   | 1.00 ms                                                      | 1.10 ms: 1.10x slower                                                        |
| unpack_sequence            | 53.2 ns                                                      | 58.5 ns: 1.10x slower                                                        |
| aiohttp                    | 1.02 ms                                                      | 1.12 ms: 1.10x slower                                                        |
| regex_v8                   | 23.6 ms                                                      | 26.1 ms: 1.10x slower                                                        |
| sqlglot_optimize           | 57.5 ms                                                      | 63.6 ms: 1.11x slower                                                        |
| nbody                      | 88.0 ms                                                      | 98.3 ms: 1.12x slower                                                        |
| create_gc_cycles           | 1.59 ms                                                      | 1.79 ms: 1.12x slower                                                        |
| unpickle_pure_python       | 210 us                                                       | 235 us: 1.12x slower                                                         |
| richards_super             | 51.3 ms                                                      | 58.0 ms: 1.13x slower                                                        |
| richards                   | 45.7 ms                                                      | 51.9 ms: 1.14x slower                                                        |
| telco                      | 6.96 ms                                                      | 7.97 ms: 1.14x slower                                                        |
| nqueens                    | 89.9 ms                                                      | 103 ms: 1.15x slower                                                         |
| python_startup             | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                        |
| bench_thread_pool          | 950 us                                                       | 1.12 ms: 1.18x slower                                                        |
| pyflate                    | 439 ms                                                       | 519 ms: 1.18x slower                                                         |
| deltablue                  | 3.24 ms                                                      | 3.85 ms: 1.19x slower                                                        |
| go                         | 150 ms                                                       | 180 ms: 1.20x slower                                                         |
| scimark_lu                 | 98.8 ms                                                      | 120 ms: 1.21x slower                                                         |
| coverage                   | 66.7 ms                                                      | 83.0 ms: 1.24x slower                                                        |
| gc_traversal               | 3.48 ms                                                      | 4.38 ms: 1.26x slower                                                        |
| hexiom                     | 5.96 ms                                                      | 7.57 ms: 1.27x slower                                                        |
| python_startup_no_site     | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                        |
| scimark_sor                | 109 ms                                                       | 154 ms: 1.41x slower                                                         |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                                 |

Benchmark hidden because not significant (7): async_generators, xml_etree_parse, mako, asyncio_websockets, xml_etree_process, tomli_loads, mypy2
Ignored benchmarks (2) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240329-3.13.0a5+-d9cfe7e-JIT/bm-20240329-pythonperf2-x86_64-python-d9cfe7e565a6e2dc1574-3.13.0a5+-d9cfe7e.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.96% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 0.99x