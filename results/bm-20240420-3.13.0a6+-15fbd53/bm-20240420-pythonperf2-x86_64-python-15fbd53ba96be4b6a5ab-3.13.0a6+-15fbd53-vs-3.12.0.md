# Results vs. 3.12.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.01x faster
- HPT reliability: 80.95%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.91x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 285 ms: 1.00x faster                                                         |
| chameleon      | 7.23 ms                                                      | 7.57 ms: 1.05x slower                                                        |
| docutils       | 2.87 sec                                                     | 2.97 sec: 1.04x slower                                                       |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 540 ms                                                       | 421 ms: 1.28x faster                                                         |
| async_tree_none_tg         | 431 ms                                                       | 340 ms: 1.27x faster                                                         |
| async_tree_none            | 452 ms                                                       | 373 ms: 1.21x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 578 ms: 1.21x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 882 ms: 1.19x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 466 ms: 1.17x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 898 ms: 1.16x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 618 ms: 1.13x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.20x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 76.6 ms                                                      | 75.4 ms: 1.02x faster                                                        |
| nbody          | 88.0 ms                                                      | 86.9 ms: 1.01x faster                                                        |
| pidigits       | 265 ms                                                       | 263 ms: 1.01x faster                                                         |
| Geometric mean | (ref)                                                        | 1.01x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.51 ms: 1.02x faster                                                        |
| regex_compile  | 144 ms                                                       | 143 ms: 1.00x faster                                                         |
| regex_dna      | 239 ms                                                       | 242 ms: 1.02x slower                                                         |
| regex_v8       | 23.6 ms                                                      | 25.2 ms: 1.07x slower                                                        |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 30.8 us: 1.06x faster                                                        |
| pickle_pure_python   | 318 us                                                       | 307 us: 1.04x faster                                                         |
| xml_etree_generate   | 86.1 ms                                                      | 83.8 ms: 1.03x faster                                                        |
| pickle               | 10.5 us                                                      | 10.2 us: 1.03x faster                                                        |
| unpickle_pure_python | 210 us                                                       | 211 us: 1.01x slower                                                         |
| unpickle             | 14.8 us                                                      | 14.9 us: 1.01x slower                                                        |
| xml_etree_process    | 58.4 ms                                                      | 58.9 ms: 1.01x slower                                                        |
| tomli_loads          | 2.16 sec                                                     | 2.19 sec: 1.02x slower                                                       |
| json_loads           | 24.4 us                                                      | 24.7 us: 1.02x slower                                                        |
| unpickle_list        | 4.66 us                                                      | 4.81 us: 1.03x slower                                                        |
| xml_etree_iterparse  | 103 ms                                                       | 106 ms: 1.03x slower                                                         |
| json_dumps           | 10.2 ms                                                      | 10.6 ms: 1.04x slower                                                        |
| xml_etree_parse      | 144 ms                                                       | 151 ms: 1.05x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                                 |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 8.64 ms                                                      | 8.88 ms: 1.03x slower                                                        |
| python_startup         | 11.6 ms                                                      | 12.9 ms: 1.11x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 38.2 ms                                                      | 37.9 ms: 1.01x faster                                                        |
| mako            | 10.0 ms                                                      | 10.1 ms: 1.01x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.00x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| comprehensions             | 21.9 us                                                      | 17.0 us: 1.29x faster                                                        |
| typing_runtime_protocols   | 152 us                                                       | 118 us: 1.29x faster                                                         |
| async_tree_memoization_tg  | 540 ms                                                       | 421 ms: 1.28x faster                                                         |
| async_tree_none_tg         | 431 ms                                                       | 340 ms: 1.27x faster                                                         |
| async_tree_none            | 452 ms                                                       | 373 ms: 1.21x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 578 ms: 1.21x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 882 ms: 1.19x faster                                                         |
| raytrace                   | 298 ms                                                       | 254 ms: 1.17x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 466 ms: 1.17x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 898 ms: 1.16x faster                                                         |
| scimark_monte_carlo        | 69.0 ms                                                      | 60.3 ms: 1.14x faster                                                        |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 618 ms: 1.13x faster                                                         |
| generators                 | 37.4 ms                                                      | 33.4 ms: 1.12x faster                                                        |
| crypto_pyaes               | 80.3 ms                                                      | 72.2 ms: 1.11x faster                                                        |
| chaos                      | 64.0 ms                                                      | 58.5 ms: 1.09x faster                                                        |
| pathlib                    | 18.9 ms                                                      | 17.3 ms: 1.09x faster                                                        |
| coroutines                 | 23.0 ms                                                      | 21.1 ms: 1.09x faster                                                        |
| async_generators           | 390 ms                                                       | 359 ms: 1.09x faster                                                         |
| mypy2                      | 830 ms                                                       | 773 ms: 1.07x faster                                                         |
| logging_simple             | 6.71 us                                                      | 6.26 us: 1.07x faster                                                        |
| logging_format             | 7.48 us                                                      | 7.03 us: 1.07x faster                                                        |
| bench_thread_pool          | 950 us                                                       | 896 us: 1.06x faster                                                         |
| pickle_dict                | 32.5 us                                                      | 30.8 us: 1.06x faster                                                        |
| sympy_sum                  | 162 ms                                                       | 155 ms: 1.05x faster                                                         |
| bench_mp_pool              | 4.76 ms                                                      | 4.58 ms: 1.04x faster                                                        |
| nqueens                    | 89.9 ms                                                      | 86.6 ms: 1.04x faster                                                        |
| pickle_pure_python         | 318 us                                                       | 307 us: 1.04x faster                                                         |
| scimark_fft                | 301 ms                                                       | 291 ms: 1.03x faster                                                         |
| scimark_lu                 | 98.8 ms                                                      | 95.8 ms: 1.03x faster                                                        |
| xml_etree_generate         | 86.1 ms                                                      | 83.8 ms: 1.03x faster                                                        |
| pickle                     | 10.5 us                                                      | 10.2 us: 1.03x faster                                                        |
| sympy_integrate            | 23.9 ms                                                      | 23.3 ms: 1.03x faster                                                        |
| mdp                        | 2.57 sec                                                     | 2.50 sec: 1.03x faster                                                       |
| sqlite_synth               | 2.77 us                                                      | 2.72 us: 1.02x faster                                                        |
| sympy_str                  | 302 ms                                                       | 296 ms: 1.02x faster                                                         |
| pprint_pformat             | 1.65 sec                                                     | 1.62 sec: 1.02x faster                                                       |
| float                      | 76.6 ms                                                      | 75.4 ms: 1.02x faster                                                        |
| regex_effbot               | 3.57 ms                                                      | 3.51 ms: 1.02x faster                                                        |
| pycparser                  | 1.23 sec                                                     | 1.22 sec: 1.02x faster                                                       |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.15 ms: 1.01x faster                                                        |
| nbody                      | 88.0 ms                                                      | 86.9 ms: 1.01x faster                                                        |
| pprint_safe_repr           | 807 ms                                                       | 800 ms: 1.01x faster                                                         |
| pidigits                   | 265 ms                                                       | 263 ms: 1.01x faster                                                         |
| sqlglot_transpile          | 1.78 ms                                                      | 1.76 ms: 1.01x faster                                                        |
| django_template            | 38.2 ms                                                      | 37.9 ms: 1.01x faster                                                        |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.01x faster                                                       |
| regex_compile              | 144 ms                                                       | 143 ms: 1.00x faster                                                         |
| meteor_contest             | 128 ms                                                       | 128 ms: 1.00x faster                                                         |
| 2to3                       | 285 ms                                                       | 285 ms: 1.00x faster                                                         |
| unpickle_pure_python       | 210 us                                                       | 211 us: 1.01x slower                                                         |
| unpickle                   | 14.8 us                                                      | 14.9 us: 1.01x slower                                                        |
| deltablue                  | 3.24 ms                                                      | 3.26 ms: 1.01x slower                                                        |
| xml_etree_process          | 58.4 ms                                                      | 58.9 ms: 1.01x slower                                                        |
| mako                       | 10.0 ms                                                      | 10.1 ms: 1.01x slower                                                        |
| asyncio_websockets         | 387 ms                                                       | 392 ms: 1.01x slower                                                         |
| tomli_loads                | 2.16 sec                                                     | 2.19 sec: 1.02x slower                                                       |
| json_loads                 | 24.4 us                                                      | 24.7 us: 1.02x slower                                                        |
| regex_dna                  | 239 ms                                                       | 242 ms: 1.02x slower                                                         |
| dulwich_log                | 65.4 ms                                                      | 66.8 ms: 1.02x slower                                                        |
| python_startup_no_site     | 8.64 ms                                                      | 8.88 ms: 1.03x slower                                                        |
| sqlglot_normalize          | 116 ms                                                       | 119 ms: 1.03x slower                                                         |
| deepcopy_memo              | 36.8 us                                                      | 38.0 us: 1.03x slower                                                        |
| sqlglot_optimize           | 57.5 ms                                                      | 59.3 ms: 1.03x slower                                                        |
| fannkuch                   | 350 ms                                                       | 361 ms: 1.03x slower                                                         |
| unpickle_list              | 4.66 us                                                      | 4.81 us: 1.03x slower                                                        |
| gunicorn                   | 1.00 ms                                                      | 1.03 ms: 1.03x slower                                                        |
| xml_etree_iterparse        | 103 ms                                                       | 106 ms: 1.03x slower                                                         |
| json_dumps                 | 10.2 ms                                                      | 10.6 ms: 1.04x slower                                                        |
| docutils                   | 2.87 sec                                                     | 2.97 sec: 1.04x slower                                                       |
| deepcopy_reduce            | 3.37 us                                                      | 3.50 us: 1.04x slower                                                        |
| go                         | 150 ms                                                       | 156 ms: 1.04x slower                                                         |
| aiohttp                    | 1.02 ms                                                      | 1.06 ms: 1.04x slower                                                        |
| sympy_expand               | 484 ms                                                       | 506 ms: 1.05x slower                                                         |
| xml_etree_parse            | 144 ms                                                       | 151 ms: 1.05x slower                                                         |
| chameleon                  | 7.23 ms                                                      | 7.57 ms: 1.05x slower                                                        |
| json                       | 5.12 ms                                                      | 5.44 ms: 1.06x slower                                                        |
| regex_v8                   | 23.6 ms                                                      | 25.2 ms: 1.07x slower                                                        |
| spectral_norm              | 91.6 ms                                                      | 97.9 ms: 1.07x slower                                                        |
| deepcopy                   | 368 us                                                       | 397 us: 1.08x slower                                                         |
| pyflate                    | 439 ms                                                       | 474 ms: 1.08x slower                                                         |
| scimark_sor                | 109 ms                                                       | 120 ms: 1.10x slower                                                         |
| python_startup             | 11.6 ms                                                      | 12.9 ms: 1.11x slower                                                        |
| richards                   | 45.7 ms                                                      | 50.9 ms: 1.11x slower                                                        |
| richards_super             | 51.3 ms                                                      | 57.6 ms: 1.12x slower                                                        |
| telco                      | 6.96 ms                                                      | 8.13 ms: 1.17x slower                                                        |
| create_gc_cycles           | 1.59 ms                                                      | 1.93 ms: 1.21x slower                                                        |
| coverage                   | 66.7 ms                                                      | 82.9 ms: 1.24x slower                                                        |
| gc_traversal               | 3.48 ms                                                      | 4.58 ms: 1.32x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                                 |

Benchmark hidden because not significant (7): tornado_http, pickle_list, logging_silent, sqlglot_parse, asyncio_tcp, hexiom, dask
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240420-3.13.0a6+-15fbd53/bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 80.95% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.91x