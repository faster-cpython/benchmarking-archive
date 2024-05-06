# Results vs. 3.11.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.09x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 286 ms: 1.00x faster                                                         |
| chameleon      | 7.92 ms                                                      | 7.51 ms: 1.05x faster                                                        |
| docutils       | 2.85 sec                                                     | 3.00 sec: 1.05x slower                                                       |
| html5lib       | 72.2 ms                                                      | 73.2 ms: 1.01x slower                                                        |
| tornado_http   | 124 ms                                                       | 120 ms: 1.04x faster                                                         |
| Geometric mean | (ref)                                                        | 1.01x faster                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 417 ms: 1.44x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 336 ms: 1.41x faster                                                         |
| async_tree_none            | 518 ms                                                       | 369 ms: 1.40x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 466 ms: 1.35x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 883 ms: 1.31x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 576 ms: 1.30x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 907 ms: 1.29x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 616 ms: 1.22x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.34x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 92.9 ms                                                      | 85.7 ms: 1.08x faster                                                        |
| float          | 74.9 ms                                                      | 76.6 ms: 1.02x slower                                                        |
| pidigits       | 251 ms                                                       | 263 ms: 1.05x slower                                                         |
| Geometric mean | (ref)                                                        | 1.00x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 145 ms: 1.08x faster                                                         |
| regex_dna      | 227 ms                                                       | 236 ms: 1.04x slower                                                         |
| regex_effbot   | 3.34 ms                                                      | 3.47 ms: 1.04x slower                                                        |
| regex_v8       | 24.4 ms                                                      | 25.7 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                        | 1.01x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                        |
| json_loads           | 28.9 us                                                      | 24.5 us: 1.18x faster                                                        |
| unpickle_pure_python | 238 us                                                       | 210 us: 1.13x faster                                                         |
| xml_etree_parse      | 155 ms                                                       | 144 ms: 1.08x faster                                                         |
| pickle_dict          | 32.3 us                                                      | 31.0 us: 1.04x faster                                                        |
| xml_etree_iterparse  | 107 ms                                                       | 103 ms: 1.03x faster                                                         |
| tomli_loads          | 2.25 sec                                                     | 2.19 sec: 1.03x faster                                                       |
| pickle_pure_python   | 316 us                                                       | 308 us: 1.03x faster                                                         |
| unpickle_list        | 4.60 us                                                      | 4.72 us: 1.03x slower                                                        |
| pickle               | 9.89 us                                                      | 10.2 us: 1.03x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 84.8 ms: 1.06x slower                                                        |
| xml_etree_process    | 55.9 ms                                                      | 59.8 ms: 1.07x slower                                                        |
| pickle_list          | 3.94 us                                                      | 4.42 us: 1.12x slower                                                        |
| unpickle             | 13.3 us                                                      | 15.5 us: 1.17x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 8.84 ms: 1.14x slower                                                        |
| python_startup         | 10.7 ms                                                      | 12.9 ms: 1.20x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.17x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 10.3 ms: 1.07x faster                                                        |
| django_template | 39.3 ms                                                      | 38.4 ms: 1.02x faster                                                        |
| genshi_text     | 25.5 ms                                                      | 26.0 ms: 1.02x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.02x faster                                                                 |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 169 us: 3.15x faster                                                         |
| asyncio_tcp                | 747 ms                                                       | 372 ms: 2.01x faster                                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.57 sec: 1.95x faster                                                       |
| generators                 | 54.6 ms                                                      | 33.0 ms: 1.66x faster                                                        |
| pylint                     | 514 ms                                                       | 344 ms: 1.49x faster                                                         |
| comprehensions             | 25.1 us                                                      | 16.9 us: 1.48x faster                                                        |
| async_tree_memoization_tg  | 600 ms                                                       | 417 ms: 1.44x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 336 ms: 1.41x faster                                                         |
| async_tree_none            | 518 ms                                                       | 369 ms: 1.40x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 466 ms: 1.35x faster                                                         |
| coroutines                 | 27.8 ms                                                      | 20.6 ms: 1.35x faster                                                        |
| async_tree_io_tg           | 1.15 sec                                                     | 883 ms: 1.31x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 576 ms: 1.30x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 907 ms: 1.29x faster                                                         |
| chaos                      | 74.9 ms                                                      | 59.2 ms: 1.27x faster                                                        |
| json_dumps                 | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                        |
| deltablue                  | 3.97 ms                                                      | 3.20 ms: 1.24x faster                                                        |
| raytrace                   | 309 ms                                                       | 249 ms: 1.24x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 616 ms: 1.22x faster                                                         |
| sympy_sum                  | 186 ms                                                       | 154 ms: 1.21x faster                                                         |
| scimark_lu                 | 114 ms                                                       | 95.7 ms: 1.19x faster                                                        |
| json_loads                 | 28.9 us                                                      | 24.5 us: 1.18x faster                                                        |
| nqueens                    | 103 ms                                                       | 87.0 ms: 1.18x faster                                                        |
| fannkuch                   | 416 ms                                                       | 353 ms: 1.18x faster                                                         |
| hexiom                     | 6.98 ms                                                      | 6.02 ms: 1.16x faster                                                        |
| crypto_pyaes               | 83.3 ms                                                      | 72.3 ms: 1.15x faster                                                        |
| scimark_monte_carlo        | 69.8 ms                                                      | 60.7 ms: 1.15x faster                                                        |
| sympy_str                  | 337 ms                                                       | 296 ms: 1.14x faster                                                         |
| unpickle_pure_python       | 238 us                                                       | 210 us: 1.13x faster                                                         |
| bench_thread_pool          | 1.00 ms                                                      | 886 us: 1.13x faster                                                         |
| sympy_integrate            | 25.8 ms                                                      | 23.2 ms: 1.11x faster                                                        |
| mdp                        | 2.77 sec                                                     | 2.50 sec: 1.11x faster                                                       |
| richards_super             | 63.6 ms                                                      | 57.6 ms: 1.10x faster                                                        |
| sympy_expand               | 553 ms                                                       | 502 ms: 1.10x faster                                                         |
| pathlib                    | 18.9 ms                                                      | 17.2 ms: 1.10x faster                                                        |
| logging_simple             | 7.24 us                                                      | 6.58 us: 1.10x faster                                                        |
| nbody                      | 92.9 ms                                                      | 85.7 ms: 1.08x faster                                                        |
| sqlglot_parse              | 1.51 ms                                                      | 1.40 ms: 1.08x faster                                                        |
| regex_compile              | 156 ms                                                       | 145 ms: 1.08x faster                                                         |
| logging_format             | 7.71 us                                                      | 7.15 us: 1.08x faster                                                        |
| xml_etree_parse            | 155 ms                                                       | 144 ms: 1.08x faster                                                         |
| logging_silent             | 100 ns                                                       | 93.4 ns: 1.07x faster                                                        |
| sqlglot_transpile          | 1.91 ms                                                      | 1.78 ms: 1.07x faster                                                        |
| mako                       | 11.0 ms                                                      | 10.3 ms: 1.07x faster                                                        |
| chameleon                  | 7.92 ms                                                      | 7.51 ms: 1.05x faster                                                        |
| pickle_dict                | 32.3 us                                                      | 31.0 us: 1.04x faster                                                        |
| pycparser                  | 1.31 sec                                                     | 1.26 sec: 1.04x faster                                                       |
| sqlglot_normalize          | 122 ms                                                       | 117 ms: 1.04x faster                                                         |
| dask                       | 410 ms                                                       | 393 ms: 1.04x faster                                                         |
| tornado_http               | 124 ms                                                       | 120 ms: 1.04x faster                                                         |
| thrift                     | 931 us                                                       | 896 us: 1.04x faster                                                         |
| xml_etree_iterparse        | 107 ms                                                       | 103 ms: 1.03x faster                                                         |
| json                       | 5.58 ms                                                      | 5.41 ms: 1.03x faster                                                        |
| meteor_contest             | 131 ms                                                       | 127 ms: 1.03x faster                                                         |
| tomli_loads                | 2.25 sec                                                     | 2.19 sec: 1.03x faster                                                       |
| pickle_pure_python         | 316 us                                                       | 308 us: 1.03x faster                                                         |
| pprint_pformat             | 1.67 sec                                                     | 1.63 sec: 1.02x faster                                                       |
| dulwich_log                | 67.4 ms                                                      | 65.9 ms: 1.02x faster                                                        |
| django_template            | 39.3 ms                                                      | 38.4 ms: 1.02x faster                                                        |
| sqlglot_optimize           | 59.0 ms                                                      | 58.3 ms: 1.01x faster                                                        |
| pprint_safe_repr           | 805 ms                                                       | 798 ms: 1.01x faster                                                         |
| deepcopy                   | 391 us                                                       | 388 us: 1.01x faster                                                         |
| 2to3                       | 287 ms                                                       | 286 ms: 1.00x faster                                                         |
| deepcopy_memo              | 37.5 us                                                      | 38.0 us: 1.01x slower                                                        |
| html5lib                   | 72.2 ms                                                      | 73.2 ms: 1.01x slower                                                        |
| mypy2                      | 762 ms                                                       | 774 ms: 1.02x slower                                                         |
| genshi_text                | 25.5 ms                                                      | 26.0 ms: 1.02x slower                                                        |
| float                      | 74.9 ms                                                      | 76.6 ms: 1.02x slower                                                        |
| richards                   | 49.7 ms                                                      | 50.9 ms: 1.03x slower                                                        |
| unpickle_list              | 4.60 us                                                      | 4.72 us: 1.03x slower                                                        |
| spectral_norm              | 95.1 ms                                                      | 98.1 ms: 1.03x slower                                                        |
| pickle                     | 9.89 us                                                      | 10.2 us: 1.03x slower                                                        |
| regex_dna                  | 227 ms                                                       | 236 ms: 1.04x slower                                                         |
| deepcopy_reduce            | 3.40 us                                                      | 3.52 us: 1.04x slower                                                        |
| regex_effbot               | 3.34 ms                                                      | 3.47 ms: 1.04x slower                                                        |
| pidigits                   | 251 ms                                                       | 263 ms: 1.05x slower                                                         |
| regex_v8                   | 24.4 ms                                                      | 25.7 ms: 1.05x slower                                                        |
| docutils                   | 2.85 sec                                                     | 3.00 sec: 1.05x slower                                                       |
| xml_etree_generate         | 79.7 ms                                                      | 84.8 ms: 1.06x slower                                                        |
| xml_etree_process          | 55.9 ms                                                      | 59.8 ms: 1.07x slower                                                        |
| pyflate                    | 449 ms                                                       | 483 ms: 1.07x slower                                                         |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.37 ms: 1.08x slower                                                        |
| gunicorn                   | 966 us                                                       | 1.04 ms: 1.08x slower                                                        |
| aiohttp                    | 986 us                                                       | 1.06 ms: 1.08x slower                                                        |
| scimark_sor                | 110 ms                                                       | 118 ms: 1.08x slower                                                         |
| sqlite_synth               | 2.52 us                                                      | 2.73 us: 1.08x slower                                                        |
| scimark_fft                | 281 ms                                                       | 308 ms: 1.10x slower                                                         |
| async_generators           | 322 ms                                                       | 358 ms: 1.11x slower                                                         |
| pickle_list                | 3.94 us                                                      | 4.42 us: 1.12x slower                                                        |
| python_startup_no_site     | 7.73 ms                                                      | 8.84 ms: 1.14x slower                                                        |
| gc_traversal               | 4.15 ms                                                      | 4.75 ms: 1.15x slower                                                        |
| telco                      | 6.81 ms                                                      | 7.90 ms: 1.16x slower                                                        |
| unpickle                   | 13.3 us                                                      | 15.5 us: 1.17x slower                                                        |
| coverage                   | 66.1 ms                                                      | 78.1 ms: 1.18x slower                                                        |
| python_startup             | 10.7 ms                                                      | 12.9 ms: 1.20x slower                                                        |
| create_gc_cycles           | 1.58 ms                                                      | 1.98 ms: 1.26x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.09x faster                                                                 |

Benchmark hidden because not significant (4): bench_mp_pool, asyncio_websockets, go, genshi_xml
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.03x