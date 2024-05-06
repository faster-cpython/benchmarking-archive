# Results vs. 3.11.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.05x slower
- HPT reliability: 99.96%
- HPT 99th percentile: 1.02x slower
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 326 ms: 1.14x slower                                                         |
| docutils       | 2.85 sec                                                     | 3.28 sec: 1.15x slower                                                       |
| html5lib       | 72.2 ms                                                      | 80.4 ms: 1.11x slower                                                        |
| tornado_http   | 124 ms                                                       | 126 ms: 1.01x slower                                                         |
| Geometric mean | (ref)                                                        | 1.08x slower                                                                 |

Benchmark hidden because not significant (1): chameleon

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 437 ms: 1.37x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 349 ms: 1.36x faster                                                         |
| async_tree_none            | 518 ms                                                       | 386 ms: 1.34x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 485 ms: 1.30x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 906 ms: 1.27x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 927 ms: 1.26x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 603 ms: 1.24x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 634 ms: 1.19x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 264 ms: 1.05x slower                                                         |
| float          | 74.9 ms                                                      | 92.8 ms: 1.24x slower                                                        |
| nbody          | 92.9 ms                                                      | 119 ms: 1.28x slower                                                         |
| Geometric mean | (ref)                                                        | 1.18x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                      | 25.4 ms: 1.04x slower                                                        |
| regex_dna      | 227 ms                                                       | 245 ms: 1.08x slower                                                         |
| regex_effbot   | 3.34 ms                                                      | 3.62 ms: 1.08x slower                                                        |
| regex_compile  | 156 ms                                                       | 199 ms: 1.27x slower                                                         |
| Geometric mean | (ref)                                                        | 1.12x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.8 ms: 1.22x faster                                                        |
| json_loads           | 28.9 us                                                      | 24.6 us: 1.18x faster                                                        |
| xml_etree_parse      | 155 ms                                                       | 146 ms: 1.06x faster                                                         |
| pickle_dict          | 32.3 us                                                      | 32.9 us: 1.02x slower                                                        |
| pickle_pure_python   | 316 us                                                       | 323 us: 1.02x slower                                                         |
| xml_etree_iterparse  | 107 ms                                                       | 112 ms: 1.05x slower                                                         |
| pickle               | 9.89 us                                                      | 10.6 us: 1.07x slower                                                        |
| pickle_list          | 3.94 us                                                      | 4.37 us: 1.11x slower                                                        |
| xml_etree_process    | 55.9 ms                                                      | 64.2 ms: 1.15x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 91.6 ms: 1.15x slower                                                        |
| unpickle             | 13.3 us                                                      | 15.3 us: 1.15x slower                                                        |
| unpickle_pure_python | 238 us                                                       | 301 us: 1.26x slower                                                         |
| tomli_loads          | 2.25 sec                                                     | 2.86 sec: 1.27x slower                                                       |
| Geometric mean       | (ref)                                                        | 1.05x slower                                                                 |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 8.91 ms: 1.15x slower                                                        |
| python_startup         | 10.7 ms                                                      | 13.0 ms: 1.21x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.18x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| django_template | 39.3 ms                                                      | 43.0 ms: 1.09x slower                                                        |
| genshi_xml      | 57.1 ms                                                      | 65.8 ms: 1.15x slower                                                        |
| genshi_text     | 25.5 ms                                                      | 31.8 ms: 1.25x slower                                                        |
| mako            | 11.0 ms                                                      | 14.3 ms: 1.30x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.20x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 197 us: 2.70x faster                                                         |
| asyncio_tcp                | 747 ms                                                       | 387 ms: 1.93x faster                                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.60 sec: 1.91x faster                                                       |
| generators                 | 54.6 ms                                                      | 33.8 ms: 1.62x faster                                                        |
| async_tree_memoization_tg  | 600 ms                                                       | 437 ms: 1.37x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 349 ms: 1.36x faster                                                         |
| pylint                     | 514 ms                                                       | 378 ms: 1.36x faster                                                         |
| async_tree_none            | 518 ms                                                       | 386 ms: 1.34x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 485 ms: 1.30x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 906 ms: 1.27x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 927 ms: 1.26x faster                                                         |
| coroutines                 | 27.8 ms                                                      | 22.0 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 603 ms: 1.24x faster                                                         |
| json_dumps                 | 13.3 ms                                                      | 10.8 ms: 1.22x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 634 ms: 1.19x faster                                                         |
| json_loads                 | 28.9 us                                                      | 24.6 us: 1.18x faster                                                        |
| logging_simple             | 7.24 us                                                      | 6.79 us: 1.07x faster                                                        |
| xml_etree_parse            | 155 ms                                                       | 146 ms: 1.06x faster                                                         |
| logging_format             | 7.71 us                                                      | 7.36 us: 1.05x faster                                                        |
| sympy_sum                  | 186 ms                                                       | 178 ms: 1.04x faster                                                         |
| thrift                     | 931 us                                                       | 895 us: 1.04x faster                                                         |
| pathlib                    | 18.9 ms                                                      | 18.3 ms: 1.04x faster                                                        |
| bench_thread_pool          | 1.00 ms                                                      | 980 us: 1.02x faster                                                         |
| json                       | 5.58 ms                                                      | 5.50 ms: 1.02x faster                                                        |
| richards_super             | 63.6 ms                                                      | 62.7 ms: 1.02x faster                                                        |
| raytrace                   | 309 ms                                                       | 306 ms: 1.01x faster                                                         |
| mdp                        | 2.77 sec                                                     | 2.75 sec: 1.01x faster                                                       |
| tornado_http               | 124 ms                                                       | 126 ms: 1.01x slower                                                         |
| pickle_dict                | 32.3 us                                                      | 32.9 us: 1.02x slower                                                        |
| dask                       | 410 ms                                                       | 417 ms: 1.02x slower                                                         |
| sqlglot_transpile          | 1.91 ms                                                      | 1.95 ms: 1.02x slower                                                        |
| sqlglot_parse              | 1.51 ms                                                      | 1.55 ms: 1.02x slower                                                        |
| pickle_pure_python         | 316 us                                                       | 323 us: 1.02x slower                                                         |
| pycparser                  | 1.31 sec                                                     | 1.34 sec: 1.03x slower                                                       |
| sympy_str                  | 337 ms                                                       | 346 ms: 1.03x slower                                                         |
| sympy_integrate            | 25.8 ms                                                      | 26.5 ms: 1.03x slower                                                        |
| chaos                      | 74.9 ms                                                      | 77.3 ms: 1.03x slower                                                        |
| regex_v8                   | 24.4 ms                                                      | 25.4 ms: 1.04x slower                                                        |
| sympy_expand               | 553 ms                                                       | 577 ms: 1.04x slower                                                         |
| xml_etree_iterparse        | 107 ms                                                       | 112 ms: 1.05x slower                                                         |
| pidigits                   | 251 ms                                                       | 264 ms: 1.05x slower                                                         |
| deepcopy                   | 391 us                                                       | 410 us: 1.05x slower                                                         |
| deepcopy_reduce            | 3.40 us                                                      | 3.59 us: 1.06x slower                                                        |
| pickle                     | 9.89 us                                                      | 10.6 us: 1.07x slower                                                        |
| regex_dna                  | 227 ms                                                       | 245 ms: 1.08x slower                                                         |
| regex_effbot               | 3.34 ms                                                      | 3.62 ms: 1.08x slower                                                        |
| sqlglot_normalize          | 122 ms                                                       | 133 ms: 1.09x slower                                                         |
| django_template            | 39.3 ms                                                      | 43.0 ms: 1.09x slower                                                        |
| crypto_pyaes               | 83.3 ms                                                      | 91.3 ms: 1.10x slower                                                        |
| deltablue                  | 3.97 ms                                                      | 4.36 ms: 1.10x slower                                                        |
| comprehensions             | 25.1 us                                                      | 27.6 us: 1.10x slower                                                        |
| meteor_contest             | 131 ms                                                       | 144 ms: 1.10x slower                                                         |
| pickle_list                | 3.94 us                                                      | 4.37 us: 1.11x slower                                                        |
| html5lib                   | 72.2 ms                                                      | 80.4 ms: 1.11x slower                                                        |
| richards                   | 49.7 ms                                                      | 55.6 ms: 1.12x slower                                                        |
| sqlite_synth               | 2.52 us                                                      | 2.87 us: 1.14x slower                                                        |
| deepcopy_memo              | 37.5 us                                                      | 42.7 us: 1.14x slower                                                        |
| 2to3                       | 287 ms                                                       | 326 ms: 1.14x slower                                                         |
| dulwich_log                | 67.4 ms                                                      | 76.8 ms: 1.14x slower                                                        |
| mypy2                      | 762 ms                                                       | 868 ms: 1.14x slower                                                         |
| xml_etree_process          | 55.9 ms                                                      | 64.2 ms: 1.15x slower                                                        |
| xml_etree_generate         | 79.7 ms                                                      | 91.6 ms: 1.15x slower                                                        |
| docutils                   | 2.85 sec                                                     | 3.28 sec: 1.15x slower                                                       |
| python_startup_no_site     | 7.73 ms                                                      | 8.91 ms: 1.15x slower                                                        |
| genshi_xml                 | 57.1 ms                                                      | 65.8 ms: 1.15x slower                                                        |
| unpickle                   | 13.3 us                                                      | 15.3 us: 1.15x slower                                                        |
| nqueens                    | 103 ms                                                       | 119 ms: 1.16x slower                                                         |
| fannkuch                   | 416 ms                                                       | 485 ms: 1.17x slower                                                         |
| sqlglot_optimize           | 59.0 ms                                                      | 68.8 ms: 1.17x slower                                                        |
| aiohttp                    | 986 us                                                       | 1.15 ms: 1.17x slower                                                        |
| gunicorn                   | 966 us                                                       | 1.13 ms: 1.17x slower                                                        |
| gc_traversal               | 4.15 ms                                                      | 4.91 ms: 1.18x slower                                                        |
| python_startup             | 10.7 ms                                                      | 13.0 ms: 1.21x slower                                                        |
| coverage                   | 66.1 ms                                                      | 80.0 ms: 1.21x slower                                                        |
| async_generators           | 322 ms                                                       | 393 ms: 1.22x slower                                                         |
| scimark_lu                 | 114 ms                                                       | 141 ms: 1.24x slower                                                         |
| float                      | 74.9 ms                                                      | 92.8 ms: 1.24x slower                                                        |
| genshi_text                | 25.5 ms                                                      | 31.8 ms: 1.25x slower                                                        |
| unpickle_pure_python       | 238 us                                                       | 301 us: 1.26x slower                                                         |
| telco                      | 6.81 ms                                                      | 8.59 ms: 1.26x slower                                                        |
| pprint_pformat             | 1.67 sec                                                     | 2.11 sec: 1.27x slower                                                       |
| tomli_loads                | 2.25 sec                                                     | 2.86 sec: 1.27x slower                                                       |
| regex_compile              | 156 ms                                                       | 199 ms: 1.27x slower                                                         |
| nbody                      | 92.9 ms                                                      | 119 ms: 1.28x slower                                                         |
| pprint_safe_repr           | 805 ms                                                       | 1.04 sec: 1.29x slower                                                       |
| mako                       | 11.0 ms                                                      | 14.3 ms: 1.30x slower                                                        |
| create_gc_cycles           | 1.58 ms                                                      | 2.07 ms: 1.31x slower                                                        |
| go                         | 158 ms                                                       | 207 ms: 1.31x slower                                                         |
| pyflate                    | 449 ms                                                       | 621 ms: 1.38x slower                                                         |
| scimark_monte_carlo        | 69.8 ms                                                      | 97.9 ms: 1.40x slower                                                        |
| scimark_sor                | 110 ms                                                       | 161 ms: 1.47x slower                                                         |
| hexiom                     | 6.98 ms                                                      | 10.6 ms: 1.51x slower                                                        |
| scimark_fft                | 281 ms                                                       | 425 ms: 1.52x slower                                                         |
| spectral_norm              | 95.1 ms                                                      | 144 ms: 1.52x slower                                                         |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 6.28 ms: 1.55x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.05x slower                                                                 |

Benchmark hidden because not significant (5): asyncio_websockets, logging_silent, bench_mp_pool, chameleon, unpickle_list
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.96% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.02x

# Memory
- memory change: 1.04x