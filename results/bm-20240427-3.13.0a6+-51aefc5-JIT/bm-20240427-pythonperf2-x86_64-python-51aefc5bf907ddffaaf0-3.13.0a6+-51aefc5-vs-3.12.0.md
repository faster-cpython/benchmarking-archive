# Results vs. 3.12.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.02x slower
- HPT reliability: 98.95%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 303 ms: 1.06x slower                                                         |
| chameleon      | 7.23 ms                                                      | 7.67 ms: 1.06x slower                                                        |
| docutils       | 2.87 sec                                                     | 3.09 sec: 1.08x slower                                                       |
| Geometric mean | (ref)                                                        | 1.05x slower                                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 540 ms                                                       | 421 ms: 1.28x faster                                                         |
| async_tree_none_tg         | 431 ms                                                       | 338 ms: 1.27x faster                                                         |
| async_tree_none            | 452 ms                                                       | 370 ms: 1.22x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 882 ms: 1.19x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 594 ms: 1.17x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 468 ms: 1.16x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 902 ms: 1.15x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 618 ms: 1.13x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.20x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 261 ms: 1.02x faster                                                         |
| float          | 76.6 ms                                                      | 76.1 ms: 1.01x faster                                                        |
| nbody          | 88.0 ms                                                      | 97.1 ms: 1.10x slower                                                        |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.53 ms: 1.01x faster                                                        |
| regex_compile  | 144 ms                                                       | 143 ms: 1.01x faster                                                         |
| regex_dna      | 239 ms                                                       | 241 ms: 1.01x slower                                                         |
| regex_v8       | 23.6 ms                                                      | 25.8 ms: 1.09x slower                                                        |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| tomli_loads          | 2.16 sec                                                     | 2.11 sec: 1.02x faster                                                       |
| xml_etree_iterparse  | 103 ms                                                       | 100 ms: 1.02x faster                                                         |
| xml_etree_generate   | 86.1 ms                                                      | 84.6 ms: 1.02x faster                                                        |
| unpickle             | 14.8 us                                                      | 14.9 us: 1.01x slower                                                        |
| pickle_pure_python   | 318 us                                                       | 320 us: 1.01x slower                                                         |
| json_loads           | 24.4 us                                                      | 24.6 us: 1.01x slower                                                        |
| xml_etree_parse      | 144 ms                                                       | 145 ms: 1.01x slower                                                         |
| pickle               | 10.5 us                                                      | 10.7 us: 1.02x slower                                                        |
| unpickle_list        | 4.66 us                                                      | 4.75 us: 1.02x slower                                                        |
| pickle_dict          | 32.5 us                                                      | 33.2 us: 1.02x slower                                                        |
| json_dumps           | 10.2 ms                                                      | 10.6 ms: 1.03x slower                                                        |
| unpickle_pure_python | 210 us                                                       | 221 us: 1.06x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                                 |

Benchmark hidden because not significant (2): xml_etree_process, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 8.64 ms                                                      | 9.41 ms: 1.09x slower                                                        |
| python_startup         | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.12x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.0 ms                                                      | 9.86 ms: 1.01x faster                                                        |
| django_template | 38.2 ms                                                      | 40.3 ms: 1.06x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 540 ms                                                       | 421 ms: 1.28x faster                                                         |
| async_tree_none_tg         | 431 ms                                                       | 338 ms: 1.27x faster                                                         |
| async_tree_none            | 452 ms                                                       | 370 ms: 1.22x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 882 ms: 1.19x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 594 ms: 1.17x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 468 ms: 1.16x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 902 ms: 1.15x faster                                                         |
| comprehensions             | 21.9 us                                                      | 19.4 us: 1.13x faster                                                        |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 618 ms: 1.13x faster                                                         |
| generators                 | 37.4 ms                                                      | 34.6 ms: 1.08x faster                                                        |
| pathlib                    | 18.9 ms                                                      | 17.5 ms: 1.08x faster                                                        |
| raytrace                   | 298 ms                                                       | 277 ms: 1.07x faster                                                         |
| coroutines                 | 23.0 ms                                                      | 21.6 ms: 1.07x faster                                                        |
| logging_format             | 7.48 us                                                      | 7.17 us: 1.04x faster                                                        |
| sqlite_synth               | 2.77 us                                                      | 2.66 us: 1.04x faster                                                        |
| crypto_pyaes               | 80.3 ms                                                      | 77.7 ms: 1.03x faster                                                        |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 4.07 ms: 1.03x faster                                                        |
| tomli_loads                | 2.16 sec                                                     | 2.11 sec: 1.02x faster                                                       |
| xml_etree_iterparse        | 103 ms                                                       | 100 ms: 1.02x faster                                                         |
| async_generators           | 390 ms                                                       | 381 ms: 1.02x faster                                                         |
| logging_simple             | 6.71 us                                                      | 6.57 us: 1.02x faster                                                        |
| xml_etree_generate         | 86.1 ms                                                      | 84.6 ms: 1.02x faster                                                        |
| pidigits                   | 265 ms                                                       | 261 ms: 1.02x faster                                                         |
| mako                       | 10.0 ms                                                      | 9.86 ms: 1.01x faster                                                        |
| regex_effbot               | 3.57 ms                                                      | 3.53 ms: 1.01x faster                                                        |
| asyncio_tcp                | 378 ms                                                       | 374 ms: 1.01x faster                                                         |
| float                      | 76.6 ms                                                      | 76.1 ms: 1.01x faster                                                        |
| regex_compile              | 144 ms                                                       | 143 ms: 1.01x faster                                                         |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.58 sec: 1.01x faster                                                       |
| spectral_norm              | 91.6 ms                                                      | 91.3 ms: 1.00x faster                                                        |
| mdp                        | 2.57 sec                                                     | 2.58 sec: 1.00x slower                                                       |
| unpickle                   | 14.8 us                                                      | 14.9 us: 1.01x slower                                                        |
| pickle_pure_python         | 318 us                                                       | 320 us: 1.01x slower                                                         |
| asyncio_websockets         | 387 ms                                                       | 390 ms: 1.01x slower                                                         |
| json_loads                 | 24.4 us                                                      | 24.6 us: 1.01x slower                                                        |
| richards                   | 45.7 ms                                                      | 46.2 ms: 1.01x slower                                                        |
| regex_dna                  | 239 ms                                                       | 241 ms: 1.01x slower                                                         |
| sympy_sum                  | 162 ms                                                       | 164 ms: 1.01x slower                                                         |
| xml_etree_parse            | 144 ms                                                       | 145 ms: 1.01x slower                                                         |
| deepcopy_reduce            | 3.37 us                                                      | 3.42 us: 1.01x slower                                                        |
| richards_super             | 51.3 ms                                                      | 52.2 ms: 1.02x slower                                                        |
| pickle                     | 10.5 us                                                      | 10.7 us: 1.02x slower                                                        |
| scimark_monte_carlo        | 69.0 ms                                                      | 70.3 ms: 1.02x slower                                                        |
| unpickle_list              | 4.66 us                                                      | 4.75 us: 1.02x slower                                                        |
| dask                       | 392 ms                                                       | 400 ms: 1.02x slower                                                         |
| pickle_dict                | 32.5 us                                                      | 33.2 us: 1.02x slower                                                        |
| deepcopy_memo              | 36.8 us                                                      | 37.6 us: 1.02x slower                                                        |
| dulwich_log                | 65.4 ms                                                      | 66.8 ms: 1.02x slower                                                        |
| sympy_str                  | 302 ms                                                       | 311 ms: 1.03x slower                                                         |
| chaos                      | 64.0 ms                                                      | 65.8 ms: 1.03x slower                                                        |
| logging_silent             | 94.4 ns                                                      | 97.2 ns: 1.03x slower                                                        |
| scimark_fft                | 301 ms                                                       | 311 ms: 1.03x slower                                                         |
| json_dumps                 | 10.2 ms                                                      | 10.6 ms: 1.03x slower                                                        |
| sqlglot_transpile          | 1.78 ms                                                      | 1.84 ms: 1.04x slower                                                        |
| sqlglot_parse              | 1.38 ms                                                      | 1.43 ms: 1.04x slower                                                        |
| json                       | 5.12 ms                                                      | 5.34 ms: 1.04x slower                                                        |
| meteor_contest             | 128 ms                                                       | 134 ms: 1.05x slower                                                         |
| pprint_pformat             | 1.65 sec                                                     | 1.74 sec: 1.05x slower                                                       |
| django_template            | 38.2 ms                                                      | 40.3 ms: 1.06x slower                                                        |
| unpickle_pure_python       | 210 us                                                       | 221 us: 1.06x slower                                                         |
| pprint_safe_repr           | 807 ms                                                       | 856 ms: 1.06x slower                                                         |
| chameleon                  | 7.23 ms                                                      | 7.67 ms: 1.06x slower                                                        |
| 2to3                       | 285 ms                                                       | 303 ms: 1.06x slower                                                         |
| sympy_integrate            | 23.9 ms                                                      | 25.5 ms: 1.07x slower                                                        |
| sympy_expand               | 484 ms                                                       | 517 ms: 1.07x slower                                                         |
| deepcopy                   | 368 us                                                       | 396 us: 1.07x slower                                                         |
| docutils                   | 2.87 sec                                                     | 3.09 sec: 1.08x slower                                                       |
| sqlglot_normalize          | 116 ms                                                       | 125 ms: 1.08x slower                                                         |
| python_startup_no_site     | 8.64 ms                                                      | 9.41 ms: 1.09x slower                                                        |
| regex_v8                   | 23.6 ms                                                      | 25.8 ms: 1.09x slower                                                        |
| pyflate                    | 439 ms                                                       | 478 ms: 1.09x slower                                                         |
| fannkuch                   | 350 ms                                                       | 385 ms: 1.10x slower                                                         |
| nbody                      | 88.0 ms                                                      | 97.1 ms: 1.10x slower                                                        |
| aiohttp                    | 1.02 ms                                                      | 1.13 ms: 1.11x slower                                                        |
| gunicorn                   | 1.00 ms                                                      | 1.12 ms: 1.11x slower                                                        |
| sqlglot_optimize           | 57.5 ms                                                      | 64.1 ms: 1.12x slower                                                        |
| nqueens                    | 89.9 ms                                                      | 102 ms: 1.13x slower                                                         |
| go                         | 150 ms                                                       | 171 ms: 1.14x slower                                                         |
| telco                      | 6.96 ms                                                      | 7.97 ms: 1.14x slower                                                        |
| coverage                   | 66.7 ms                                                      | 76.6 ms: 1.15x slower                                                        |
| python_startup             | 11.6 ms                                                      | 13.5 ms: 1.16x slower                                                        |
| deltablue                  | 3.24 ms                                                      | 3.80 ms: 1.17x slower                                                        |
| scimark_lu                 | 98.8 ms                                                      | 117 ms: 1.18x slower                                                         |
| create_gc_cycles           | 1.59 ms                                                      | 1.88 ms: 1.18x slower                                                        |
| typing_runtime_protocols   | 152 us                                                       | 184 us: 1.21x slower                                                         |
| hexiom                     | 5.96 ms                                                      | 7.30 ms: 1.22x slower                                                        |
| gc_traversal               | 3.48 ms                                                      | 4.42 ms: 1.27x slower                                                        |
| scimark_sor                | 109 ms                                                       | 154 ms: 1.41x slower                                                         |
| Geometric mean             | (ref)                                                        | 1.02x slower                                                                 |

Benchmark hidden because not significant (7): bench_mp_pool, pycparser, xml_etree_process, pickle_list, tornado_http, bench_thread_pool, mypy2
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240427-3.13.0a6+-51aefc5-JIT/bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 98.95% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x