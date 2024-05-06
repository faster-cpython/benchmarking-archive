# Results vs. 3.11.0

- fork: python
- ref: 51aefc5bf907ddffaaf0
- machine: linux-x86_64
- commit hash: 51aefc5
- commit date: 2024-04-27
- overall geometric mean: 1.05x faster
- HPT reliability: 88.43%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 303 ms: 1.06x slower                                                         |
| chameleon      | 7.92 ms                                                      | 7.67 ms: 1.03x faster                                                        |
| docutils       | 2.85 sec                                                     | 3.09 sec: 1.08x slower                                                       |
| html5lib       | 72.2 ms                                                      | 73.8 ms: 1.02x slower                                                        |
| tornado_http   | 124 ms                                                       | 122 ms: 1.02x faster                                                         |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 421 ms: 1.42x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 338 ms: 1.40x faster                                                         |
| async_tree_none            | 518 ms                                                       | 370 ms: 1.40x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 468 ms: 1.34x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 882 ms: 1.31x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 902 ms: 1.30x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 594 ms: 1.26x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 618 ms: 1.22x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.33x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 74.9 ms                                                      | 76.1 ms: 1.02x slower                                                        |
| pidigits       | 251 ms                                                       | 261 ms: 1.04x slower                                                         |
| nbody          | 92.9 ms                                                      | 97.1 ms: 1.05x slower                                                        |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 143 ms: 1.09x faster                                                         |
| regex_v8       | 24.4 ms                                                      | 25.8 ms: 1.05x slower                                                        |
| regex_effbot   | 3.34 ms                                                      | 3.53 ms: 1.06x slower                                                        |
| regex_dna      | 227 ms                                                       | 241 ms: 1.06x slower                                                         |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                        |
| json_loads           | 28.9 us                                                      | 24.6 us: 1.18x faster                                                        |
| unpickle_pure_python | 238 us                                                       | 221 us: 1.08x faster                                                         |
| tomli_loads          | 2.25 sec                                                     | 2.11 sec: 1.07x faster                                                       |
| xml_etree_parse      | 155 ms                                                       | 145 ms: 1.06x faster                                                         |
| xml_etree_iterparse  | 107 ms                                                       | 100 ms: 1.06x faster                                                         |
| pickle_pure_python   | 316 us                                                       | 320 us: 1.01x slower                                                         |
| pickle_dict          | 32.3 us                                                      | 33.2 us: 1.03x slower                                                        |
| unpickle_list        | 4.60 us                                                      | 4.75 us: 1.03x slower                                                        |
| xml_etree_process    | 55.9 ms                                                      | 58.6 ms: 1.05x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 84.6 ms: 1.06x slower                                                        |
| pickle               | 9.89 us                                                      | 10.7 us: 1.08x slower                                                        |
| unpickle             | 13.3 us                                                      | 14.9 us: 1.12x slower                                                        |
| pickle_list          | 3.94 us                                                      | 4.44 us: 1.13x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 9.41 ms: 1.22x slower                                                        |
| python_startup         | 10.7 ms                                                      | 13.5 ms: 1.25x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.23x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 11.0 ms                                                      | 9.86 ms: 1.12x faster                                                        |
| django_template | 39.3 ms                                                      | 40.3 ms: 1.03x slower                                                        |
| genshi_xml      | 57.1 ms                                                      | 62.8 ms: 1.10x slower                                                        |
| genshi_text     | 25.5 ms                                                      | 29.1 ms: 1.14x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.04x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240427-pythonperf2-x86_64-python-51aefc5bf907ddffaaf0-3.13.0a6+-51aefc5 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 184 us: 2.89x faster                                                         |
| asyncio_tcp                | 747 ms                                                       | 374 ms: 2.00x faster                                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                       |
| generators                 | 54.6 ms                                                      | 34.6 ms: 1.58x faster                                                        |
| async_tree_memoization_tg  | 600 ms                                                       | 421 ms: 1.42x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 338 ms: 1.40x faster                                                         |
| async_tree_none            | 518 ms                                                       | 370 ms: 1.40x faster                                                         |
| pylint                     | 514 ms                                                       | 370 ms: 1.39x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 468 ms: 1.34x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 882 ms: 1.31x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 902 ms: 1.30x faster                                                         |
| comprehensions             | 25.1 us                                                      | 19.4 us: 1.29x faster                                                        |
| coroutines                 | 27.8 ms                                                      | 21.6 ms: 1.29x faster                                                        |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 594 ms: 1.26x faster                                                         |
| json_dumps                 | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                        |
| richards_super             | 63.6 ms                                                      | 52.2 ms: 1.22x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 618 ms: 1.22x faster                                                         |
| json_loads                 | 28.9 us                                                      | 24.6 us: 1.18x faster                                                        |
| chaos                      | 74.9 ms                                                      | 65.8 ms: 1.14x faster                                                        |
| sympy_sum                  | 186 ms                                                       | 164 ms: 1.13x faster                                                         |
| raytrace                   | 309 ms                                                       | 277 ms: 1.12x faster                                                         |
| mako                       | 11.0 ms                                                      | 9.86 ms: 1.12x faster                                                        |
| logging_simple             | 7.24 us                                                      | 6.57 us: 1.10x faster                                                        |
| regex_compile              | 156 ms                                                       | 143 ms: 1.09x faster                                                         |
| sympy_str                  | 337 ms                                                       | 311 ms: 1.08x faster                                                         |
| pathlib                    | 18.9 ms                                                      | 17.5 ms: 1.08x faster                                                        |
| fannkuch                   | 416 ms                                                       | 385 ms: 1.08x faster                                                         |
| unpickle_pure_python       | 238 us                                                       | 221 us: 1.08x faster                                                         |
| richards                   | 49.7 ms                                                      | 46.2 ms: 1.08x faster                                                        |
| logging_format             | 7.71 us                                                      | 7.17 us: 1.08x faster                                                        |
| mdp                        | 2.77 sec                                                     | 2.58 sec: 1.07x faster                                                       |
| crypto_pyaes               | 83.3 ms                                                      | 77.7 ms: 1.07x faster                                                        |
| sympy_expand               | 553 ms                                                       | 517 ms: 1.07x faster                                                         |
| tomli_loads                | 2.25 sec                                                     | 2.11 sec: 1.07x faster                                                       |
| xml_etree_parse            | 155 ms                                                       | 145 ms: 1.06x faster                                                         |
| xml_etree_iterparse        | 107 ms                                                       | 100 ms: 1.06x faster                                                         |
| pycparser                  | 1.31 sec                                                     | 1.24 sec: 1.06x faster                                                       |
| sqlglot_parse              | 1.51 ms                                                      | 1.43 ms: 1.06x faster                                                        |
| json                       | 5.58 ms                                                      | 5.34 ms: 1.05x faster                                                        |
| deltablue                  | 3.97 ms                                                      | 3.80 ms: 1.04x faster                                                        |
| thrift                     | 931 us                                                       | 892 us: 1.04x faster                                                         |
| spectral_norm              | 95.1 ms                                                      | 91.3 ms: 1.04x faster                                                        |
| sqlglot_transpile          | 1.91 ms                                                      | 1.84 ms: 1.04x faster                                                        |
| bench_thread_pool          | 1.00 ms                                                      | 964 us: 1.04x faster                                                         |
| chameleon                  | 7.92 ms                                                      | 7.67 ms: 1.03x faster                                                        |
| logging_silent             | 100 ns                                                       | 97.2 ns: 1.03x faster                                                        |
| dask                       | 410 ms                                                       | 400 ms: 1.02x faster                                                         |
| tornado_http               | 124 ms                                                       | 122 ms: 1.02x faster                                                         |
| sympy_integrate            | 25.8 ms                                                      | 25.5 ms: 1.01x faster                                                        |
| nqueens                    | 103 ms                                                       | 102 ms: 1.01x faster                                                         |
| dulwich_log                | 67.4 ms                                                      | 66.8 ms: 1.01x faster                                                        |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.07 ms: 1.00x slower                                                        |
| scimark_monte_carlo        | 69.8 ms                                                      | 70.3 ms: 1.01x slower                                                        |
| deepcopy                   | 391 us                                                       | 396 us: 1.01x slower                                                         |
| pickle_pure_python         | 316 us                                                       | 320 us: 1.01x slower                                                         |
| float                      | 74.9 ms                                                      | 76.1 ms: 1.02x slower                                                        |
| html5lib                   | 72.2 ms                                                      | 73.8 ms: 1.02x slower                                                        |
| scimark_lu                 | 114 ms                                                       | 117 ms: 1.02x slower                                                         |
| django_template            | 39.3 ms                                                      | 40.3 ms: 1.03x slower                                                        |
| pickle_dict                | 32.3 us                                                      | 33.2 us: 1.03x slower                                                        |
| sqlglot_normalize          | 122 ms                                                       | 125 ms: 1.03x slower                                                         |
| meteor_contest             | 131 ms                                                       | 134 ms: 1.03x slower                                                         |
| unpickle_list              | 4.60 us                                                      | 4.75 us: 1.03x slower                                                        |
| pidigits                   | 251 ms                                                       | 261 ms: 1.04x slower                                                         |
| nbody                      | 92.9 ms                                                      | 97.1 ms: 1.05x slower                                                        |
| hexiom                     | 6.98 ms                                                      | 7.30 ms: 1.05x slower                                                        |
| pprint_pformat             | 1.67 sec                                                     | 1.74 sec: 1.05x slower                                                       |
| xml_etree_process          | 55.9 ms                                                      | 58.6 ms: 1.05x slower                                                        |
| regex_v8                   | 24.4 ms                                                      | 25.8 ms: 1.05x slower                                                        |
| sqlite_synth               | 2.52 us                                                      | 2.66 us: 1.06x slower                                                        |
| 2to3                       | 287 ms                                                       | 303 ms: 1.06x slower                                                         |
| regex_effbot               | 3.34 ms                                                      | 3.53 ms: 1.06x slower                                                        |
| regex_dna                  | 227 ms                                                       | 241 ms: 1.06x slower                                                         |
| xml_etree_generate         | 79.7 ms                                                      | 84.6 ms: 1.06x slower                                                        |
| pprint_safe_repr           | 805 ms                                                       | 856 ms: 1.06x slower                                                         |
| pyflate                    | 449 ms                                                       | 478 ms: 1.06x slower                                                         |
| gc_traversal               | 4.15 ms                                                      | 4.42 ms: 1.07x slower                                                        |
| pickle                     | 9.89 us                                                      | 10.7 us: 1.08x slower                                                        |
| docutils                   | 2.85 sec                                                     | 3.09 sec: 1.08x slower                                                       |
| go                         | 158 ms                                                       | 171 ms: 1.09x slower                                                         |
| sqlglot_optimize           | 59.0 ms                                                      | 64.1 ms: 1.09x slower                                                        |
| genshi_xml                 | 57.1 ms                                                      | 62.8 ms: 1.10x slower                                                        |
| scimark_fft                | 281 ms                                                       | 311 ms: 1.11x slower                                                         |
| mypy2                      | 762 ms                                                       | 846 ms: 1.11x slower                                                         |
| unpickle                   | 13.3 us                                                      | 14.9 us: 1.12x slower                                                        |
| pickle_list                | 3.94 us                                                      | 4.44 us: 1.13x slower                                                        |
| genshi_text                | 25.5 ms                                                      | 29.1 ms: 1.14x slower                                                        |
| aiohttp                    | 986 us                                                       | 1.13 ms: 1.15x slower                                                        |
| gunicorn                   | 966 us                                                       | 1.12 ms: 1.15x slower                                                        |
| coverage                   | 66.1 ms                                                      | 76.6 ms: 1.16x slower                                                        |
| telco                      | 6.81 ms                                                      | 7.97 ms: 1.17x slower                                                        |
| async_generators           | 322 ms                                                       | 381 ms: 1.19x slower                                                         |
| create_gc_cycles           | 1.58 ms                                                      | 1.88 ms: 1.19x slower                                                        |
| python_startup_no_site     | 7.73 ms                                                      | 9.41 ms: 1.22x slower                                                        |
| python_startup             | 10.7 ms                                                      | 13.5 ms: 1.25x slower                                                        |
| scimark_sor                | 110 ms                                                       | 154 ms: 1.40x slower                                                         |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                                 |

Benchmark hidden because not significant (4): asyncio_websockets, deepcopy_memo, deepcopy_reduce, bench_mp_pool
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 88.43% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.11x