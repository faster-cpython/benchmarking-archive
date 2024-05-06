# Results vs. 3.12.0

- fork: mdboom
- ref: all_above_350
- machine: linux-x86_64
- commit hash: fd018ce
- commit date: 2024-04-04
- overall geometric mean: 1.03x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.01x slower
- Memory change: 0.98x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 302 ms: 1.06x slower                                                  |
| chameleon      | 7.23 ms                                                      | 7.34 ms: 1.02x slower                                                 |
| docutils       | 2.87 sec                                                     | 3.07 sec: 1.07x slower                                                |
| tornado_http   | 121 ms                                                       | 124 ms: 1.03x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 339 ms: 1.27x faster                                                  |
| async_tree_none            | 452 ms                                                       | 359 ms: 1.26x faster                                                  |
| async_tree_memoization_tg  | 540 ms                                                       | 433 ms: 1.25x faster                                                  |
| async_tree_memoization     | 544 ms                                                       | 442 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 578 ms: 1.21x faster                                                  |
| async_tree_io              | 1.04 sec                                                     | 889 ms: 1.17x faster                                                  |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 597 ms: 1.17x faster                                                  |
| async_tree_io_tg           | 1.05 sec                                                     | 910 ms: 1.16x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 261 ms: 1.01x faster                                                  |
| float          | 76.6 ms                                                      | 79.5 ms: 1.04x slower                                                 |
| nbody          | 88.0 ms                                                      | 94.6 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                        | 1.03x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 239 ms                                                       | 242 ms: 1.01x slower                                                  |
| regex_effbot   | 3.57 ms                                                      | 3.63 ms: 1.02x slower                                                 |
| regex_compile  | 144 ms                                                       | 150 ms: 1.04x slower                                                  |
| regex_v8       | 23.6 ms                                                      | 26.1 ms: 1.11x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 31.0 us: 1.05x faster                                                 |
| pickle_pure_python   | 318 us                                                       | 307 us: 1.04x faster                                                  |
| xml_etree_generate   | 86.1 ms                                                      | 83.6 ms: 1.03x faster                                                 |
| xml_etree_parse      | 144 ms                                                       | 142 ms: 1.02x faster                                                  |
| pickle               | 10.5 us                                                      | 10.5 us: 1.00x faster                                                 |
| unpickle_list        | 4.66 us                                                      | 4.71 us: 1.01x slower                                                 |
| unpickle             | 14.8 us                                                      | 15.0 us: 1.01x slower                                                 |
| json_loads           | 24.4 us                                                      | 25.3 us: 1.04x slower                                                 |
| tomli_loads          | 2.16 sec                                                     | 2.24 sec: 1.04x slower                                                |
| json_dumps           | 10.2 ms                                                      | 10.9 ms: 1.06x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 243 us: 1.16x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                          |

Benchmark hidden because not significant (3): xml_etree_process, xml_etree_iterparse, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                 |
| python_startup_no_site | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.26x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 10.0 ms                                                      | 9.87 ms: 1.01x faster                                                 |
| django_template | 38.2 ms                                                      | 40.9 ms: 1.07x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 339 ms: 1.27x faster                                                  |
| typing_runtime_protocols   | 152 us                                                       | 120 us: 1.26x faster                                                  |
| async_tree_none            | 452 ms                                                       | 359 ms: 1.26x faster                                                  |
| async_tree_memoization_tg  | 540 ms                                                       | 433 ms: 1.25x faster                                                  |
| async_tree_memoization     | 544 ms                                                       | 442 ms: 1.23x faster                                                  |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 578 ms: 1.21x faster                                                  |
| async_tree_io              | 1.04 sec                                                     | 889 ms: 1.17x faster                                                  |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 597 ms: 1.17x faster                                                  |
| async_tree_io_tg           | 1.05 sec                                                     | 910 ms: 1.16x faster                                                  |
| comprehensions             | 21.9 us                                                      | 19.7 us: 1.11x faster                                                 |
| generators                 | 37.4 ms                                                      | 33.6 ms: 1.11x faster                                                 |
| pickle_dict                | 32.5 us                                                      | 31.0 us: 1.05x faster                                                 |
| logging_format             | 7.48 us                                                      | 7.15 us: 1.05x faster                                                 |
| coroutines                 | 23.0 ms                                                      | 22.1 ms: 1.04x faster                                                 |
| pickle_pure_python         | 318 us                                                       | 307 us: 1.04x faster                                                  |
| xml_etree_generate         | 86.1 ms                                                      | 83.6 ms: 1.03x faster                                                 |
| crypto_pyaes               | 80.3 ms                                                      | 78.7 ms: 1.02x faster                                                 |
| sqlite_synth               | 2.77 us                                                      | 2.72 us: 1.02x faster                                                 |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.13 ms: 1.02x faster                                                 |
| xml_etree_parse            | 144 ms                                                       | 142 ms: 1.02x faster                                                  |
| pidigits                   | 265 ms                                                       | 261 ms: 1.01x faster                                                  |
| logging_simple             | 6.71 us                                                      | 6.62 us: 1.01x faster                                                 |
| asyncio_tcp                | 378 ms                                                       | 373 ms: 1.01x faster                                                  |
| mako                       | 10.0 ms                                                      | 9.87 ms: 1.01x faster                                                 |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.01x faster                                                |
| pickle                     | 10.5 us                                                      | 10.5 us: 1.00x faster                                                 |
| sympy_str                  | 302 ms                                                       | 304 ms: 1.01x slower                                                  |
| unpickle_list              | 4.66 us                                                      | 4.71 us: 1.01x slower                                                 |
| regex_dna                  | 239 ms                                                       | 242 ms: 1.01x slower                                                  |
| unpickle                   | 14.8 us                                                      | 15.0 us: 1.01x slower                                                 |
| regex_effbot               | 3.57 ms                                                      | 3.63 ms: 1.02x slower                                                 |
| chameleon                  | 7.23 ms                                                      | 7.34 ms: 1.02x slower                                                 |
| sqlglot_transpile          | 1.78 ms                                                      | 1.82 ms: 1.02x slower                                                 |
| tornado_http               | 121 ms                                                       | 124 ms: 1.03x slower                                                  |
| dask                       | 392 ms                                                       | 402 ms: 1.03x slower                                                  |
| pycparser                  | 1.23 sec                                                     | 1.27 sec: 1.03x slower                                                |
| logging_silent             | 94.4 ns                                                      | 97.4 ns: 1.03x slower                                                 |
| pathlib                    | 18.9 ms                                                      | 19.5 ms: 1.03x slower                                                 |
| mdp                        | 2.57 sec                                                     | 2.66 sec: 1.03x slower                                                |
| raytrace                   | 298 ms                                                       | 308 ms: 1.03x slower                                                  |
| sqlglot_parse              | 1.38 ms                                                      | 1.43 ms: 1.04x slower                                                 |
| deepcopy_memo              | 36.8 us                                                      | 38.1 us: 1.04x slower                                                 |
| float                      | 76.6 ms                                                      | 79.5 ms: 1.04x slower                                                 |
| json_loads                 | 24.4 us                                                      | 25.3 us: 1.04x slower                                                 |
| regex_compile              | 144 ms                                                       | 150 ms: 1.04x slower                                                  |
| tomli_loads                | 2.16 sec                                                     | 2.24 sec: 1.04x slower                                                |
| spectral_norm              | 91.6 ms                                                      | 95.4 ms: 1.04x slower                                                 |
| pprint_pformat             | 1.65 sec                                                     | 1.72 sec: 1.04x slower                                                |
| json                       | 5.12 ms                                                      | 5.34 ms: 1.04x slower                                                 |
| pprint_safe_repr           | 807 ms                                                       | 843 ms: 1.04x slower                                                  |
| chaos                      | 64.0 ms                                                      | 67.0 ms: 1.05x slower                                                 |
| deepcopy                   | 368 us                                                       | 387 us: 1.05x slower                                                  |
| meteor_contest             | 128 ms                                                       | 135 ms: 1.06x slower                                                  |
| sympy_integrate            | 23.9 ms                                                      | 25.3 ms: 1.06x slower                                                 |
| 2to3                       | 285 ms                                                       | 302 ms: 1.06x slower                                                  |
| json_dumps                 | 10.2 ms                                                      | 10.9 ms: 1.06x slower                                                 |
| sympy_expand               | 484 ms                                                       | 515 ms: 1.06x slower                                                  |
| dulwich_log                | 65.4 ms                                                      | 69.6 ms: 1.06x slower                                                 |
| scimark_fft                | 301 ms                                                       | 321 ms: 1.07x slower                                                  |
| docutils                   | 2.87 sec                                                     | 3.07 sec: 1.07x slower                                                |
| django_template            | 38.2 ms                                                      | 40.9 ms: 1.07x slower                                                 |
| nbody                      | 88.0 ms                                                      | 94.6 ms: 1.08x slower                                                 |
| bench_mp_pool              | 4.76 ms                                                      | 5.13 ms: 1.08x slower                                                 |
| sqlglot_normalize          | 116 ms                                                       | 125 ms: 1.08x slower                                                  |
| scimark_monte_carlo        | 69.0 ms                                                      | 74.8 ms: 1.08x slower                                                 |
| gunicorn                   | 1.00 ms                                                      | 1.09 ms: 1.08x slower                                                 |
| aiohttp                    | 1.02 ms                                                      | 1.11 ms: 1.09x slower                                                 |
| regex_v8                   | 23.6 ms                                                      | 26.1 ms: 1.11x slower                                                 |
| sqlglot_optimize           | 57.5 ms                                                      | 63.9 ms: 1.11x slower                                                 |
| fannkuch                   | 350 ms                                                       | 392 ms: 1.12x slower                                                  |
| create_gc_cycles           | 1.59 ms                                                      | 1.79 ms: 1.13x slower                                                 |
| richards                   | 45.7 ms                                                      | 52.4 ms: 1.15x slower                                                 |
| richards_super             | 51.3 ms                                                      | 58.9 ms: 1.15x slower                                                 |
| pyflate                    | 439 ms                                                       | 507 ms: 1.16x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 243 us: 1.16x slower                                                  |
| python_startup             | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                 |
| telco                      | 6.96 ms                                                      | 8.10 ms: 1.16x slower                                                 |
| bench_thread_pool          | 950 us                                                       | 1.11 ms: 1.16x slower                                                 |
| deltablue                  | 3.24 ms                                                      | 3.79 ms: 1.17x slower                                                 |
| nqueens                    | 89.9 ms                                                      | 106 ms: 1.18x slower                                                  |
| go                         | 150 ms                                                       | 178 ms: 1.19x slower                                                  |
| coverage                   | 66.7 ms                                                      | 80.3 ms: 1.20x slower                                                 |
| gc_traversal               | 3.48 ms                                                      | 4.36 ms: 1.25x slower                                                 |
| scimark_lu                 | 98.8 ms                                                      | 125 ms: 1.27x slower                                                  |
| hexiom                     | 5.96 ms                                                      | 7.74 ms: 1.30x slower                                                 |
| python_startup_no_site     | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                 |
| scimark_sor                | 109 ms                                                       | 155 ms: 1.42x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                          |

Benchmark hidden because not significant (8): asyncio_websockets, xml_etree_process, deepcopy_reduce, xml_etree_iterparse, mypy2, async_generators, sympy_sum, pickle_list
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240404-3.13.0a5+-fd018ce-JIT/bm-20240404-pythonperf2-x86_64-mdboom-all_above_350-3.13.0a5+-fd018ce.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 0.98x