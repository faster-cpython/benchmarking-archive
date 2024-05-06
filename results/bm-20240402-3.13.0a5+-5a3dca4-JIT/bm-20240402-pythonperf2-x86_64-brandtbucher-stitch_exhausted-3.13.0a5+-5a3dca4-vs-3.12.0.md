# Results vs. 3.12.0

- fork: brandtbucher
- ref: stitch_exhausted
- machine: linux-x86_64
- commit hash: 5a3dca4
- commit date: 2024-04-02
- overall geometric mean: 1.04x slower
- HPT reliability: 99.96%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 306 ms: 1.07x slower                                                           |
| chameleon      | 7.23 ms                                                      | 7.57 ms: 1.05x slower                                                          |
| docutils       | 2.87 sec                                                     | 3.13 sec: 1.09x slower                                                         |
| tornado_http   | 121 ms                                                       | 124 ms: 1.02x slower                                                           |
| Geometric mean | (ref)                                                        | 1.06x slower                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 340 ms: 1.27x faster                                                           |
| async_tree_none            | 452 ms                                                       | 362 ms: 1.25x faster                                                           |
| async_tree_memoization_tg  | 540 ms                                                       | 437 ms: 1.24x faster                                                           |
| async_tree_memoization     | 544 ms                                                       | 445 ms: 1.22x faster                                                           |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 579 ms: 1.20x faster                                                           |
| async_tree_io              | 1.04 sec                                                     | 891 ms: 1.17x faster                                                           |
| async_tree_io_tg           | 1.05 sec                                                     | 910 ms: 1.16x faster                                                           |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 601 ms: 1.16x faster                                                           |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 261 ms: 1.01x faster                                                           |
| float          | 76.6 ms                                                      | 79.0 ms: 1.03x slower                                                          |
| nbody          | 88.0 ms                                                      | 96.8 ms: 1.10x slower                                                          |
| Geometric mean | (ref)                                                        | 1.04x slower                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_dna      | 239 ms                                                       | 240 ms: 1.01x slower                                                           |
| regex_effbot   | 3.57 ms                                                      | 3.60 ms: 1.01x slower                                                          |
| regex_compile  | 144 ms                                                       | 146 ms: 1.01x slower                                                           |
| regex_v8       | 23.6 ms                                                      | 25.7 ms: 1.09x slower                                                          |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| xml_etree_generate   | 86.1 ms                                                      | 82.7 ms: 1.04x faster                                                          |
| pickle_pure_python   | 318 us                                                       | 308 us: 1.03x faster                                                           |
| xml_etree_iterparse  | 103 ms                                                       | 102 ms: 1.01x faster                                                           |
| xml_etree_parse      | 144 ms                                                       | 142 ms: 1.01x faster                                                           |
| unpickle_list        | 4.66 us                                                      | 4.61 us: 1.01x faster                                                          |
| pickle_dict          | 32.5 us                                                      | 33.0 us: 1.01x slower                                                          |
| pickle_list          | 4.43 us                                                      | 4.50 us: 1.02x slower                                                          |
| unpickle             | 14.8 us                                                      | 15.1 us: 1.02x slower                                                          |
| json_loads           | 24.4 us                                                      | 25.4 us: 1.04x slower                                                          |
| pickle               | 10.5 us                                                      | 11.0 us: 1.05x slower                                                          |
| json_dumps           | 10.2 ms                                                      | 10.7 ms: 1.05x slower                                                          |
| unpickle_pure_python | 210 us                                                       | 230 us: 1.10x slower                                                           |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                                   |

Benchmark hidden because not significant (2): xml_etree_process, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup         | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                          |
| python_startup_no_site | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                          |
| Geometric mean         | (ref)                                                        | 1.26x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 10.0 ms                                                      | 9.90 ms: 1.01x faster                                                          |
| django_template | 38.2 ms                                                      | 40.9 ms: 1.07x slower                                                          |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none_tg         | 431 ms                                                       | 340 ms: 1.27x faster                                                           |
| async_tree_none            | 452 ms                                                       | 362 ms: 1.25x faster                                                           |
| typing_runtime_protocols   | 152 us                                                       | 123 us: 1.24x faster                                                           |
| async_tree_memoization_tg  | 540 ms                                                       | 437 ms: 1.24x faster                                                           |
| async_tree_memoization     | 544 ms                                                       | 445 ms: 1.22x faster                                                           |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 579 ms: 1.20x faster                                                           |
| async_tree_io              | 1.04 sec                                                     | 891 ms: 1.17x faster                                                           |
| async_tree_io_tg           | 1.05 sec                                                     | 910 ms: 1.16x faster                                                           |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 601 ms: 1.16x faster                                                           |
| generators                 | 37.4 ms                                                      | 33.5 ms: 1.12x faster                                                          |
| comprehensions             | 21.9 us                                                      | 20.2 us: 1.08x faster                                                          |
| xml_etree_generate         | 86.1 ms                                                      | 82.7 ms: 1.04x faster                                                          |
| coroutines                 | 23.0 ms                                                      | 22.2 ms: 1.04x faster                                                          |
| pickle_pure_python         | 318 us                                                       | 308 us: 1.03x faster                                                           |
| sqlite_synth               | 2.77 us                                                      | 2.70 us: 1.03x faster                                                          |
| logging_format             | 7.48 us                                                      | 7.32 us: 1.02x faster                                                          |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.14 ms: 1.02x faster                                                          |
| crypto_pyaes               | 80.3 ms                                                      | 79.1 ms: 1.02x faster                                                          |
| pidigits                   | 265 ms                                                       | 261 ms: 1.01x faster                                                           |
| logging_simple             | 6.71 us                                                      | 6.63 us: 1.01x faster                                                          |
| xml_etree_iterparse        | 103 ms                                                       | 102 ms: 1.01x faster                                                           |
| xml_etree_parse            | 144 ms                                                       | 142 ms: 1.01x faster                                                           |
| mako                       | 10.0 ms                                                      | 9.90 ms: 1.01x faster                                                          |
| unpickle_list              | 4.66 us                                                      | 4.61 us: 1.01x faster                                                          |
| asyncio_tcp                | 378 ms                                                       | 375 ms: 1.01x faster                                                           |
| asyncio_websockets         | 387 ms                                                       | 384 ms: 1.01x faster                                                           |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.00x faster                                                         |
| regex_dna                  | 239 ms                                                       | 240 ms: 1.01x slower                                                           |
| async_generators           | 390 ms                                                       | 393 ms: 1.01x slower                                                           |
| regex_effbot               | 3.57 ms                                                      | 3.60 ms: 1.01x slower                                                          |
| regex_compile              | 144 ms                                                       | 146 ms: 1.01x slower                                                           |
| pickle_dict                | 32.5 us                                                      | 33.0 us: 1.01x slower                                                          |
| sympy_sum                  | 162 ms                                                       | 165 ms: 1.01x slower                                                           |
| pickle_list                | 4.43 us                                                      | 4.50 us: 1.02x slower                                                          |
| unpickle                   | 14.8 us                                                      | 15.1 us: 1.02x slower                                                          |
| tornado_http               | 121 ms                                                       | 124 ms: 1.02x slower                                                           |
| sympy_str                  | 302 ms                                                       | 310 ms: 1.02x slower                                                           |
| spectral_norm              | 91.6 ms                                                      | 94.0 ms: 1.03x slower                                                          |
| float                      | 76.6 ms                                                      | 79.0 ms: 1.03x slower                                                          |
| mdp                        | 2.57 sec                                                     | 2.65 sec: 1.03x slower                                                         |
| sqlglot_transpile          | 1.78 ms                                                      | 1.84 ms: 1.03x slower                                                          |
| pprint_safe_repr           | 807 ms                                                       | 836 ms: 1.04x slower                                                           |
| logging_silent             | 94.4 ns                                                      | 97.7 ns: 1.04x slower                                                          |
| sqlglot_parse              | 1.38 ms                                                      | 1.43 ms: 1.04x slower                                                          |
| dask                       | 392 ms                                                       | 407 ms: 1.04x slower                                                           |
| deepcopy_memo              | 36.8 us                                                      | 38.4 us: 1.04x slower                                                          |
| json_loads                 | 24.4 us                                                      | 25.4 us: 1.04x slower                                                          |
| pprint_pformat             | 1.65 sec                                                     | 1.73 sec: 1.04x slower                                                         |
| deepcopy_reduce            | 3.37 us                                                      | 3.52 us: 1.05x slower                                                          |
| chameleon                  | 7.23 ms                                                      | 7.57 ms: 1.05x slower                                                          |
| pycparser                  | 1.23 sec                                                     | 1.29 sec: 1.05x slower                                                         |
| pickle                     | 10.5 us                                                      | 11.0 us: 1.05x slower                                                          |
| pathlib                    | 18.9 ms                                                      | 19.8 ms: 1.05x slower                                                          |
| json_dumps                 | 10.2 ms                                                      | 10.7 ms: 1.05x slower                                                          |
| meteor_contest             | 128 ms                                                       | 135 ms: 1.05x slower                                                           |
| scimark_fft                | 301 ms                                                       | 317 ms: 1.05x slower                                                           |
| bench_mp_pool              | 4.76 ms                                                      | 5.01 ms: 1.05x slower                                                          |
| dulwich_log                | 65.4 ms                                                      | 68.9 ms: 1.05x slower                                                          |
| raytrace                   | 298 ms                                                       | 316 ms: 1.06x slower                                                           |
| 2to3                       | 285 ms                                                       | 306 ms: 1.07x slower                                                           |
| django_template            | 38.2 ms                                                      | 40.9 ms: 1.07x slower                                                          |
| json                       | 5.12 ms                                                      | 5.51 ms: 1.08x slower                                                          |
| chaos                      | 64.0 ms                                                      | 69.0 ms: 1.08x slower                                                          |
| sympy_expand               | 484 ms                                                       | 526 ms: 1.09x slower                                                           |
| deepcopy                   | 368 us                                                       | 401 us: 1.09x slower                                                           |
| regex_v8                   | 23.6 ms                                                      | 25.7 ms: 1.09x slower                                                          |
| sympy_integrate            | 23.9 ms                                                      | 26.1 ms: 1.09x slower                                                          |
| docutils                   | 2.87 sec                                                     | 3.13 sec: 1.09x slower                                                         |
| fannkuch                   | 350 ms                                                       | 383 ms: 1.09x slower                                                           |
| sqlglot_normalize          | 116 ms                                                       | 127 ms: 1.10x slower                                                           |
| unpickle_pure_python       | 210 us                                                       | 230 us: 1.10x slower                                                           |
| nbody                      | 88.0 ms                                                      | 96.8 ms: 1.10x slower                                                          |
| scimark_monte_carlo        | 69.0 ms                                                      | 75.9 ms: 1.10x slower                                                          |
| richards                   | 45.7 ms                                                      | 50.5 ms: 1.10x slower                                                          |
| unpack_sequence            | 53.2 ns                                                      | 59.5 ns: 1.12x slower                                                          |
| richards_super             | 51.3 ms                                                      | 57.6 ms: 1.12x slower                                                          |
| gunicorn                   | 1.00 ms                                                      | 1.12 ms: 1.12x slower                                                          |
| aiohttp                    | 1.02 ms                                                      | 1.15 ms: 1.13x slower                                                          |
| sqlglot_optimize           | 57.5 ms                                                      | 64.7 ms: 1.13x slower                                                          |
| create_gc_cycles           | 1.59 ms                                                      | 1.81 ms: 1.14x slower                                                          |
| python_startup             | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                          |
| telco                      | 6.96 ms                                                      | 8.11 ms: 1.17x slower                                                          |
| deltablue                  | 3.24 ms                                                      | 3.79 ms: 1.17x slower                                                          |
| nqueens                    | 89.9 ms                                                      | 106 ms: 1.18x slower                                                           |
| go                         | 150 ms                                                       | 177 ms: 1.18x slower                                                           |
| bench_thread_pool          | 950 us                                                       | 1.13 ms: 1.19x slower                                                          |
| pyflate                    | 439 ms                                                       | 528 ms: 1.20x slower                                                           |
| scimark_lu                 | 98.8 ms                                                      | 119 ms: 1.21x slower                                                           |
| gc_traversal               | 3.48 ms                                                      | 4.35 ms: 1.25x slower                                                          |
| coverage                   | 66.7 ms                                                      | 84.3 ms: 1.26x slower                                                          |
| hexiom                     | 5.96 ms                                                      | 7.73 ms: 1.30x slower                                                          |
| python_startup_no_site     | 8.64 ms                                                      | 11.8 ms: 1.36x slower                                                          |
| scimark_sor                | 109 ms                                                       | 156 ms: 1.43x slower                                                           |
| Geometric mean             | (ref)                                                        | 1.04x slower                                                                   |

Benchmark hidden because not significant (3): xml_etree_process, tomli_loads, mypy2
Ignored benchmarks (2) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (5) of results/bm-20240402-3.13.0a5+-5a3dca4-JIT/bm-20240402-pythonperf2-x86_64-brandtbucher-stitch_exhausted-3.13.0a5+-5a3dca4.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.96% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.00x