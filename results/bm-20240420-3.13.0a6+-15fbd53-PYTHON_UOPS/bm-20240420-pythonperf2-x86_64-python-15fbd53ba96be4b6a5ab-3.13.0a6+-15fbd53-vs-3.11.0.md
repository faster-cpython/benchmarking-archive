# Results vs. 3.11.0

- fork: python
- ref: 15fbd53ba96be4b6a5ab
- machine: linux-x86_64
- commit hash: 15fbd53
- commit date: 2024-04-20
- overall geometric mean: 1.01x slower
- HPT reliability: 99.80%
- HPT 99th percentile: 1.01x slower
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 314 ms: 1.09x slower                                                         |
| chameleon      | 7.92 ms                                                      | 8.34 ms: 1.05x slower                                                        |
| docutils       | 2.85 sec                                                     | 3.24 sec: 1.14x slower                                                       |
| html5lib       | 72.2 ms                                                      | 79.0 ms: 1.09x slower                                                        |
| tornado_http   | 124 ms                                                       | 127 ms: 1.02x slower                                                         |
| Geometric mean | (ref)                                                        | 1.08x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 600 ms                                                       | 438 ms: 1.37x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 352 ms: 1.35x faster                                                         |
| async_tree_none            | 518 ms                                                       | 384 ms: 1.35x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 478 ms: 1.32x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 900 ms: 1.28x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 919 ms: 1.27x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 604 ms: 1.24x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 631 ms: 1.19x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 263 ms: 1.05x slower                                                         |
| float          | 74.9 ms                                                      | 84.7 ms: 1.13x slower                                                        |
| nbody          | 92.9 ms                                                      | 110 ms: 1.18x slower                                                         |
| Geometric mean | (ref)                                                        | 1.12x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                      | 25.6 ms: 1.05x slower                                                        |
| regex_dna      | 227 ms                                                       | 242 ms: 1.06x slower                                                         |
| regex_effbot   | 3.34 ms                                                      | 3.63 ms: 1.09x slower                                                        |
| regex_compile  | 156 ms                                                       | 194 ms: 1.24x slower                                                         |
| Geometric mean | (ref)                                                        | 1.11x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                        |
| json_loads           | 28.9 us                                                      | 24.5 us: 1.18x faster                                                        |
| pickle_dict          | 32.3 us                                                      | 30.6 us: 1.06x faster                                                        |
| xml_etree_parse      | 155 ms                                                       | 149 ms: 1.04x faster                                                         |
| pickle_pure_python   | 316 us                                                       | 320 us: 1.01x slower                                                         |
| xml_etree_iterparse  | 107 ms                                                       | 110 ms: 1.03x slower                                                         |
| pickle               | 9.89 us                                                      | 10.4 us: 1.06x slower                                                        |
| xml_etree_process    | 55.9 ms                                                      | 61.2 ms: 1.10x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 88.5 ms: 1.11x slower                                                        |
| pickle_list          | 3.94 us                                                      | 4.52 us: 1.15x slower                                                        |
| unpickle             | 13.3 us                                                      | 15.3 us: 1.15x slower                                                        |
| unpickle_pure_python | 238 us                                                       | 283 us: 1.19x slower                                                         |
| tomli_loads          | 2.25 sec                                                     | 2.73 sec: 1.22x slower                                                       |
| Geometric mean       | (ref)                                                        | 1.03x slower                                                                 |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 7.73 ms                                                      | 8.90 ms: 1.15x slower                                                        |
| python_startup         | 10.7 ms                                                      | 12.9 ms: 1.20x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.18x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_xml      | 57.1 ms                                                      | 60.2 ms: 1.05x slower                                                        |
| django_template | 39.3 ms                                                      | 41.5 ms: 1.06x slower                                                        |
| genshi_text     | 25.5 ms                                                      | 27.5 ms: 1.08x slower                                                        |
| mako            | 11.0 ms                                                      | 13.0 ms: 1.18x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.09x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240420-pythonperf2-x86_64-python-15fbd53ba96be4b6a5ab-3.13.0a6+-15fbd53 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 126 us: 4.23x faster                                                         |
| asyncio_tcp                | 747 ms                                                       | 378 ms: 1.97x faster                                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.60 sec: 1.92x faster                                                       |
| generators                 | 54.6 ms                                                      | 34.0 ms: 1.61x faster                                                        |
| pylint                     | 514 ms                                                       | 370 ms: 1.39x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 438 ms: 1.37x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 352 ms: 1.35x faster                                                         |
| async_tree_none            | 518 ms                                                       | 384 ms: 1.35x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 478 ms: 1.32x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 900 ms: 1.28x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 919 ms: 1.27x faster                                                         |
| coroutines                 | 27.8 ms                                                      | 22.2 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 604 ms: 1.24x faster                                                         |
| json_dumps                 | 13.3 ms                                                      | 10.7 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 631 ms: 1.19x faster                                                         |
| json_loads                 | 28.9 us                                                      | 24.5 us: 1.18x faster                                                        |
| richards_super             | 63.6 ms                                                      | 59.6 ms: 1.07x faster                                                        |
| pathlib                    | 18.9 ms                                                      | 17.8 ms: 1.06x faster                                                        |
| logging_simple             | 7.24 us                                                      | 6.86 us: 1.06x faster                                                        |
| pickle_dict                | 32.3 us                                                      | 30.6 us: 1.06x faster                                                        |
| mdp                        | 2.77 sec                                                     | 2.63 sec: 1.05x faster                                                       |
| comprehensions             | 25.1 us                                                      | 23.9 us: 1.05x faster                                                        |
| sympy_sum                  | 186 ms                                                       | 178 ms: 1.04x faster                                                         |
| xml_etree_parse            | 155 ms                                                       | 149 ms: 1.04x faster                                                         |
| bench_thread_pool          | 1.00 ms                                                      | 965 us: 1.04x faster                                                         |
| json                       | 5.58 ms                                                      | 5.39 ms: 1.04x faster                                                        |
| thrift                     | 931 us                                                       | 899 us: 1.04x faster                                                         |
| raytrace                   | 309 ms                                                       | 299 ms: 1.04x faster                                                         |
| logging_silent             | 100 ns                                                       | 98.1 ns: 1.02x faster                                                        |
| chaos                      | 74.9 ms                                                      | 73.3 ms: 1.02x faster                                                        |
| logging_format             | 7.71 us                                                      | 7.55 us: 1.02x faster                                                        |
| pickle_pure_python         | 316 us                                                       | 320 us: 1.01x slower                                                         |
| sympy_integrate            | 25.8 ms                                                      | 26.2 ms: 1.02x slower                                                        |
| sqlglot_transpile          | 1.91 ms                                                      | 1.95 ms: 1.02x slower                                                        |
| sympy_str                  | 337 ms                                                       | 343 ms: 1.02x slower                                                         |
| tornado_http               | 124 ms                                                       | 127 ms: 1.02x slower                                                         |
| deepcopy_reduce            | 3.40 us                                                      | 3.47 us: 1.02x slower                                                        |
| sqlglot_parse              | 1.51 ms                                                      | 1.55 ms: 1.03x slower                                                        |
| pycparser                  | 1.31 sec                                                     | 1.34 sec: 1.03x slower                                                       |
| crypto_pyaes               | 83.3 ms                                                      | 85.5 ms: 1.03x slower                                                        |
| xml_etree_iterparse        | 107 ms                                                       | 110 ms: 1.03x slower                                                         |
| deepcopy                   | 391 us                                                       | 404 us: 1.03x slower                                                         |
| sympy_expand               | 553 ms                                                       | 573 ms: 1.04x slower                                                         |
| deltablue                  | 3.97 ms                                                      | 4.12 ms: 1.04x slower                                                        |
| sqlglot_normalize          | 122 ms                                                       | 127 ms: 1.04x slower                                                         |
| pidigits                   | 251 ms                                                       | 263 ms: 1.05x slower                                                         |
| regex_v8                   | 24.4 ms                                                      | 25.6 ms: 1.05x slower                                                        |
| meteor_contest             | 131 ms                                                       | 137 ms: 1.05x slower                                                         |
| chameleon                  | 7.92 ms                                                      | 8.34 ms: 1.05x slower                                                        |
| genshi_xml                 | 57.1 ms                                                      | 60.2 ms: 1.05x slower                                                        |
| pickle                     | 9.89 us                                                      | 10.4 us: 1.06x slower                                                        |
| django_template            | 39.3 ms                                                      | 41.5 ms: 1.06x slower                                                        |
| regex_dna                  | 227 ms                                                       | 242 ms: 1.06x slower                                                         |
| gc_traversal               | 4.15 ms                                                      | 4.44 ms: 1.07x slower                                                        |
| richards                   | 49.7 ms                                                      | 53.3 ms: 1.07x slower                                                        |
| genshi_text                | 25.5 ms                                                      | 27.5 ms: 1.08x slower                                                        |
| nqueens                    | 103 ms                                                       | 111 ms: 1.09x slower                                                         |
| regex_effbot               | 3.34 ms                                                      | 3.63 ms: 1.09x slower                                                        |
| html5lib                   | 72.2 ms                                                      | 79.0 ms: 1.09x slower                                                        |
| 2to3                       | 287 ms                                                       | 314 ms: 1.09x slower                                                         |
| xml_etree_process          | 55.9 ms                                                      | 61.2 ms: 1.10x slower                                                        |
| deepcopy_memo              | 37.5 us                                                      | 41.4 us: 1.10x slower                                                        |
| fannkuch                   | 416 ms                                                       | 459 ms: 1.10x slower                                                         |
| dulwich_log                | 67.4 ms                                                      | 74.8 ms: 1.11x slower                                                        |
| xml_etree_generate         | 79.7 ms                                                      | 88.5 ms: 1.11x slower                                                        |
| mypy2                      | 762 ms                                                       | 846 ms: 1.11x slower                                                         |
| sqlite_synth               | 2.52 us                                                      | 2.82 us: 1.12x slower                                                        |
| sqlglot_optimize           | 59.0 ms                                                      | 66.5 ms: 1.13x slower                                                        |
| float                      | 74.9 ms                                                      | 84.7 ms: 1.13x slower                                                        |
| docutils                   | 2.85 sec                                                     | 3.24 sec: 1.14x slower                                                       |
| pickle_list                | 3.94 us                                                      | 4.52 us: 1.15x slower                                                        |
| aiohttp                    | 986 us                                                       | 1.13 ms: 1.15x slower                                                        |
| python_startup_no_site     | 7.73 ms                                                      | 8.90 ms: 1.15x slower                                                        |
| unpickle                   | 13.3 us                                                      | 15.3 us: 1.15x slower                                                        |
| gunicorn                   | 966 us                                                       | 1.12 ms: 1.16x slower                                                        |
| nbody                      | 92.9 ms                                                      | 110 ms: 1.18x slower                                                         |
| mako                       | 11.0 ms                                                      | 13.0 ms: 1.18x slower                                                        |
| unpickle_pure_python       | 238 us                                                       | 283 us: 1.19x slower                                                         |
| python_startup             | 10.7 ms                                                      | 12.9 ms: 1.20x slower                                                        |
| pprint_pformat             | 1.67 sec                                                     | 2.01 sec: 1.20x slower                                                       |
| tomli_loads                | 2.25 sec                                                     | 2.73 sec: 1.22x slower                                                       |
| pprint_safe_repr           | 805 ms                                                       | 981 ms: 1.22x slower                                                         |
| async_generators           | 322 ms                                                       | 392 ms: 1.22x slower                                                         |
| scimark_lu                 | 114 ms                                                       | 140 ms: 1.23x slower                                                         |
| create_gc_cycles           | 1.58 ms                                                      | 1.94 ms: 1.23x slower                                                        |
| coverage                   | 66.1 ms                                                      | 81.8 ms: 1.24x slower                                                        |
| regex_compile              | 156 ms                                                       | 194 ms: 1.24x slower                                                         |
| telco                      | 6.81 ms                                                      | 8.67 ms: 1.27x slower                                                        |
| scimark_monte_carlo        | 69.8 ms                                                      | 90.3 ms: 1.29x slower                                                        |
| go                         | 158 ms                                                       | 204 ms: 1.29x slower                                                         |
| pyflate                    | 449 ms                                                       | 587 ms: 1.31x slower                                                         |
| hexiom                     | 6.98 ms                                                      | 9.39 ms: 1.35x slower                                                        |
| scimark_fft                | 281 ms                                                       | 396 ms: 1.41x slower                                                         |
| scimark_sor                | 110 ms                                                       | 159 ms: 1.45x slower                                                         |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 5.95 ms: 1.46x slower                                                        |
| spectral_norm              | 95.1 ms                                                      | 140 ms: 1.47x slower                                                         |
| Geometric mean             | (ref)                                                        | 1.01x slower                                                                 |

Benchmark hidden because not significant (4): unpickle_list, dask, asyncio_websockets, bench_mp_pool
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.80% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.01x

# Memory
- memory change: 1.04x