# Results vs. 3.12.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.12x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 0.93x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 285 ms                                                       | 326 ms: 1.14x slower                                                         |
| chameleon      | 7.23 ms                                                      | 7.94 ms: 1.10x slower                                                        |
| docutils       | 2.87 sec                                                     | 3.28 sec: 1.14x slower                                                       |
| tornado_http   | 121 ms                                                       | 126 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                        | 1.11x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 540 ms                                                       | 437 ms: 1.24x faster                                                         |
| async_tree_none_tg         | 431 ms                                                       | 349 ms: 1.24x faster                                                         |
| async_tree_none            | 452 ms                                                       | 386 ms: 1.17x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 906 ms: 1.16x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 603 ms: 1.16x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 927 ms: 1.12x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 485 ms: 1.12x faster                                                         |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 634 ms: 1.10x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.16x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 265 ms                                                       | 264 ms: 1.01x faster                                                         |
| float          | 76.6 ms                                                      | 92.8 ms: 1.21x slower                                                        |
| nbody          | 88.0 ms                                                      | 119 ms: 1.35x slower                                                         |
| Geometric mean | (ref)                                                        | 1.18x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_effbot   | 3.57 ms                                                      | 3.62 ms: 1.01x slower                                                        |
| regex_dna      | 239 ms                                                       | 245 ms: 1.03x slower                                                         |
| regex_v8       | 23.6 ms                                                      | 25.4 ms: 1.08x slower                                                        |
| regex_compile  | 144 ms                                                       | 199 ms: 1.38x slower                                                         |
| Geometric mean | (ref)                                                        | 1.12x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pickle_list          | 4.43 us                                                      | 4.37 us: 1.01x faster                                                        |
| unpickle_list        | 4.66 us                                                      | 4.62 us: 1.01x faster                                                        |
| pickle               | 10.5 us                                                      | 10.6 us: 1.01x slower                                                        |
| json_loads           | 24.4 us                                                      | 24.6 us: 1.01x slower                                                        |
| pickle_dict          | 32.5 us                                                      | 32.9 us: 1.01x slower                                                        |
| pickle_pure_python   | 318 us                                                       | 323 us: 1.02x slower                                                         |
| xml_etree_parse      | 144 ms                                                       | 146 ms: 1.02x slower                                                         |
| unpickle             | 14.8 us                                                      | 15.3 us: 1.03x slower                                                        |
| json_dumps           | 10.2 ms                                                      | 10.8 ms: 1.06x slower                                                        |
| xml_etree_generate   | 86.1 ms                                                      | 91.6 ms: 1.06x slower                                                        |
| xml_etree_iterparse  | 103 ms                                                       | 112 ms: 1.09x slower                                                         |
| xml_etree_process    | 58.4 ms                                                      | 64.2 ms: 1.10x slower                                                        |
| tomli_loads          | 2.16 sec                                                     | 2.86 sec: 1.33x slower                                                       |
| unpickle_pure_python | 210 us                                                       | 301 us: 1.43x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.08x slower                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 8.64 ms                                                      | 8.91 ms: 1.03x slower                                                        |
| python_startup         | 11.6 ms                                                      | 13.0 ms: 1.12x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.07x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 38.2 ms                                                      | 43.0 ms: 1.13x slower                                                        |
| mako            | 10.0 ms                                                      | 14.3 ms: 1.43x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.27x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 540 ms                                                       | 437 ms: 1.24x faster                                                         |
| async_tree_none_tg         | 431 ms                                                       | 349 ms: 1.24x faster                                                         |
| async_tree_none            | 452 ms                                                       | 386 ms: 1.17x faster                                                         |
| async_tree_io_tg           | 1.05 sec                                                     | 906 ms: 1.16x faster                                                         |
| async_tree_cpu_io_mixed_tg | 697 ms                                                       | 603 ms: 1.16x faster                                                         |
| async_tree_io              | 1.04 sec                                                     | 927 ms: 1.12x faster                                                         |
| async_tree_memoization     | 544 ms                                                       | 485 ms: 1.12x faster                                                         |
| generators                 | 37.4 ms                                                      | 33.8 ms: 1.11x faster                                                        |
| async_tree_cpu_io_mixed    | 696 ms                                                       | 634 ms: 1.10x faster                                                         |
| coroutines                 | 23.0 ms                                                      | 22.0 ms: 1.04x faster                                                        |
| pathlib                    | 18.9 ms                                                      | 18.3 ms: 1.04x faster                                                        |
| logging_format             | 7.48 us                                                      | 7.36 us: 1.02x faster                                                        |
| pickle_list                | 4.43 us                                                      | 4.37 us: 1.01x faster                                                        |
| unpickle_list              | 4.66 us                                                      | 4.62 us: 1.01x faster                                                        |
| pidigits                   | 265 ms                                                       | 264 ms: 1.01x faster                                                         |
| async_generators           | 390 ms                                                       | 393 ms: 1.01x slower                                                         |
| asyncio_websockets         | 387 ms                                                       | 390 ms: 1.01x slower                                                         |
| pickle                     | 10.5 us                                                      | 10.6 us: 1.01x slower                                                        |
| json_loads                 | 24.4 us                                                      | 24.6 us: 1.01x slower                                                        |
| asyncio_tcp_ssl            | 1.59 sec                                                     | 1.60 sec: 1.01x slower                                                       |
| pickle_dict                | 32.5 us                                                      | 32.9 us: 1.01x slower                                                        |
| logging_simple             | 6.71 us                                                      | 6.79 us: 1.01x slower                                                        |
| regex_effbot               | 3.57 ms                                                      | 3.62 ms: 1.01x slower                                                        |
| pickle_pure_python         | 318 us                                                       | 323 us: 1.02x slower                                                         |
| xml_etree_parse            | 144 ms                                                       | 146 ms: 1.02x slower                                                         |
| asyncio_tcp                | 378 ms                                                       | 387 ms: 1.02x slower                                                         |
| raytrace                   | 298 ms                                                       | 306 ms: 1.03x slower                                                         |
| regex_dna                  | 239 ms                                                       | 245 ms: 1.03x slower                                                         |
| python_startup_no_site     | 8.64 ms                                                      | 8.91 ms: 1.03x slower                                                        |
| bench_thread_pool          | 950 us                                                       | 980 us: 1.03x slower                                                         |
| sqlite_synth               | 2.77 us                                                      | 2.87 us: 1.03x slower                                                        |
| unpickle                   | 14.8 us                                                      | 15.3 us: 1.03x slower                                                        |
| tornado_http               | 121 ms                                                       | 126 ms: 1.04x slower                                                         |
| json_dumps                 | 10.2 ms                                                      | 10.8 ms: 1.06x slower                                                        |
| logging_silent             | 94.4 ns                                                      | 100 ns: 1.06x slower                                                         |
| xml_etree_generate         | 86.1 ms                                                      | 91.6 ms: 1.06x slower                                                        |
| dask                       | 392 ms                                                       | 417 ms: 1.06x slower                                                         |
| deepcopy_reduce            | 3.37 us                                                      | 3.59 us: 1.07x slower                                                        |
| mdp                        | 2.57 sec                                                     | 2.75 sec: 1.07x slower                                                       |
| json                       | 5.12 ms                                                      | 5.50 ms: 1.07x slower                                                        |
| regex_v8                   | 23.6 ms                                                      | 25.4 ms: 1.08x slower                                                        |
| pycparser                  | 1.23 sec                                                     | 1.34 sec: 1.09x slower                                                       |
| xml_etree_iterparse        | 103 ms                                                       | 112 ms: 1.09x slower                                                         |
| chameleon                  | 7.23 ms                                                      | 7.94 ms: 1.10x slower                                                        |
| sqlglot_transpile          | 1.78 ms                                                      | 1.95 ms: 1.10x slower                                                        |
| sympy_sum                  | 162 ms                                                       | 178 ms: 1.10x slower                                                         |
| xml_etree_process          | 58.4 ms                                                      | 64.2 ms: 1.10x slower                                                        |
| sympy_integrate            | 23.9 ms                                                      | 26.5 ms: 1.11x slower                                                        |
| deepcopy                   | 368 us                                                       | 410 us: 1.11x slower                                                         |
| python_startup             | 11.6 ms                                                      | 13.0 ms: 1.12x slower                                                        |
| meteor_contest             | 128 ms                                                       | 144 ms: 1.12x slower                                                         |
| sqlglot_parse              | 1.38 ms                                                      | 1.55 ms: 1.12x slower                                                        |
| django_template            | 38.2 ms                                                      | 43.0 ms: 1.13x slower                                                        |
| gunicorn                   | 1.00 ms                                                      | 1.13 ms: 1.13x slower                                                        |
| aiohttp                    | 1.02 ms                                                      | 1.15 ms: 1.13x slower                                                        |
| crypto_pyaes               | 80.3 ms                                                      | 91.3 ms: 1.14x slower                                                        |
| docutils                   | 2.87 sec                                                     | 3.28 sec: 1.14x slower                                                       |
| 2to3                       | 285 ms                                                       | 326 ms: 1.14x slower                                                         |
| sympy_str                  | 302 ms                                                       | 346 ms: 1.15x slower                                                         |
| sqlglot_normalize          | 116 ms                                                       | 133 ms: 1.15x slower                                                         |
| deepcopy_memo              | 36.8 us                                                      | 42.7 us: 1.16x slower                                                        |
| dulwich_log                | 65.4 ms                                                      | 76.8 ms: 1.17x slower                                                        |
| sympy_expand               | 484 ms                                                       | 577 ms: 1.19x slower                                                         |
| sqlglot_optimize           | 57.5 ms                                                      | 68.8 ms: 1.20x slower                                                        |
| coverage                   | 66.7 ms                                                      | 80.0 ms: 1.20x slower                                                        |
| chaos                      | 64.0 ms                                                      | 77.3 ms: 1.21x slower                                                        |
| float                      | 76.6 ms                                                      | 92.8 ms: 1.21x slower                                                        |
| richards                   | 45.7 ms                                                      | 55.6 ms: 1.22x slower                                                        |
| richards_super             | 51.3 ms                                                      | 62.7 ms: 1.22x slower                                                        |
| telco                      | 6.96 ms                                                      | 8.59 ms: 1.23x slower                                                        |
| comprehensions             | 21.9 us                                                      | 27.6 us: 1.26x slower                                                        |
| pprint_pformat             | 1.65 sec                                                     | 2.11 sec: 1.27x slower                                                       |
| pprint_safe_repr           | 807 ms                                                       | 1.04 sec: 1.28x slower                                                       |
| typing_runtime_protocols   | 152 us                                                       | 197 us: 1.30x slower                                                         |
| create_gc_cycles           | 1.59 ms                                                      | 2.07 ms: 1.30x slower                                                        |
| nqueens                    | 89.9 ms                                                      | 119 ms: 1.32x slower                                                         |
| tomli_loads                | 2.16 sec                                                     | 2.86 sec: 1.33x slower                                                       |
| deltablue                  | 3.24 ms                                                      | 4.36 ms: 1.35x slower                                                        |
| nbody                      | 88.0 ms                                                      | 119 ms: 1.35x slower                                                         |
| regex_compile              | 144 ms                                                       | 199 ms: 1.38x slower                                                         |
| go                         | 150 ms                                                       | 207 ms: 1.38x slower                                                         |
| fannkuch                   | 350 ms                                                       | 485 ms: 1.38x slower                                                         |
| gc_traversal               | 3.48 ms                                                      | 4.91 ms: 1.41x slower                                                        |
| scimark_fft                | 301 ms                                                       | 425 ms: 1.41x slower                                                         |
| pyflate                    | 439 ms                                                       | 621 ms: 1.42x slower                                                         |
| scimark_monte_carlo        | 69.0 ms                                                      | 97.9 ms: 1.42x slower                                                        |
| scimark_lu                 | 98.8 ms                                                      | 141 ms: 1.43x slower                                                         |
| mako                       | 10.0 ms                                                      | 14.3 ms: 1.43x slower                                                        |
| unpickle_pure_python       | 210 us                                                       | 301 us: 1.43x slower                                                         |
| scimark_sor                | 109 ms                                                       | 161 ms: 1.48x slower                                                         |
| scimark_sparse_mat_mult    | 4.21 ms                                                      | 6.28 ms: 1.49x slower                                                        |
| spectral_norm              | 91.6 ms                                                      | 144 ms: 1.57x slower                                                         |
| hexiom                     | 5.96 ms                                                      | 10.6 ms: 1.77x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.12x slower                                                                 |

Benchmark hidden because not significant (2): bench_mp_pool, mypy2
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-pythonperf2-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240427-3.13.0a6+-51aefc5-PYTHON_UOPS/bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 0.93x