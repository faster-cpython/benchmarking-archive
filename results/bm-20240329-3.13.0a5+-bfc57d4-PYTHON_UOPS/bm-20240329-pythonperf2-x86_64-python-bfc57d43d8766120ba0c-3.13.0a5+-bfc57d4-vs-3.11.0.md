# Results vs. 3.11.0

- fork: python
- ref: bfc57d43d8766120ba0c
- machine: linux-x86_64
- commit hash: bfc57d4
- commit date: 2024-03-29
- overall geometric mean: 1.06x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 325 ms: 1.13x slower                                                         |
| chameleon      | 7.92 ms                                                      | 8.14 ms: 1.03x slower                                                        |
| docutils       | 2.85 sec                                                     | 3.28 sec: 1.15x slower                                                       |
| html5lib       | 72.2 ms                                                      | 80.4 ms: 1.11x slower                                                        |
| tornado_http   | 124 ms                                                       | 129 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                        | 1.09x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 518 ms                                                       | 383 ms: 1.35x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 470 ms: 1.34x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 359 ms: 1.32x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 461 ms: 1.30x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 923 ms: 1.27x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 606 ms: 1.24x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 944 ms: 1.22x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 629 ms: 1.20x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.28x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 265 ms: 1.05x slower                                                         |
| float          | 74.9 ms                                                      | 102 ms: 1.36x slower                                                         |
| nbody          | 92.9 ms                                                      | 129 ms: 1.39x slower                                                         |
| Geometric mean | (ref)                                                        | 1.26x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_effbot   | 3.34 ms                                                      | 3.47 ms: 1.04x slower                                                        |
| regex_v8       | 24.4 ms                                                      | 25.9 ms: 1.06x slower                                                        |
| regex_dna      | 227 ms                                                       | 242 ms: 1.06x slower                                                         |
| regex_compile  | 156 ms                                                       | 209 ms: 1.34x slower                                                         |
| Geometric mean | (ref)                                                        | 1.12x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.9 ms: 1.22x faster                                                        |
| json_loads           | 28.9 us                                                      | 25.8 us: 1.12x faster                                                        |
| xml_etree_parse      | 155 ms                                                       | 146 ms: 1.06x faster                                                         |
| pickle_pure_python   | 316 us                                                       | 328 us: 1.04x slower                                                         |
| xml_etree_iterparse  | 107 ms                                                       | 113 ms: 1.06x slower                                                         |
| pickle_dict          | 32.3 us                                                      | 35.2 us: 1.09x slower                                                        |
| pickle               | 9.89 us                                                      | 10.9 us: 1.10x slower                                                        |
| unpickle             | 13.3 us                                                      | 14.8 us: 1.11x slower                                                        |
| pickle_list          | 3.94 us                                                      | 4.46 us: 1.13x slower                                                        |
| xml_etree_process    | 55.9 ms                                                      | 63.4 ms: 1.14x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 92.4 ms: 1.16x slower                                                        |
| tomli_loads          | 2.25 sec                                                     | 2.98 sec: 1.32x slower                                                       |
| unpickle_pure_python | 238 us                                                       | 319 us: 1.34x slower                                                         |
| Geometric mean       | (ref)                                                        | 1.07x slower                                                                 |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 12.9 ms: 1.20x slower                                                        |
| python_startup_no_site | 7.73 ms                                                      | 11.2 ms: 1.45x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.32x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| genshi_text     | 25.5 ms                                                      | 27.0 ms: 1.06x slower                                                        |
| django_template | 39.3 ms                                                      | 42.3 ms: 1.08x slower                                                        |
| genshi_xml      | 57.1 ms                                                      | 61.9 ms: 1.08x slower                                                        |
| mako            | 11.0 ms                                                      | 14.4 ms: 1.31x slower                                                        |
| Geometric mean  | (ref)                                                        | 1.13x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240329-pythonperf2-x86_64-python-bfc57d43d8766120ba0c-3.13.0a5+-bfc57d4 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 128 us: 4.15x faster                                                         |
| asyncio_tcp                | 747 ms                                                       | 379 ms: 1.97x faster                                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.60 sec: 1.92x faster                                                       |
| generators                 | 54.6 ms                                                      | 34.9 ms: 1.57x faster                                                        |
| pylint                     | 514 ms                                                       | 351 ms: 1.47x faster                                                         |
| async_tree_none            | 518 ms                                                       | 383 ms: 1.35x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 470 ms: 1.34x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 359 ms: 1.32x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 461 ms: 1.30x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 923 ms: 1.27x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 606 ms: 1.24x faster                                                         |
| coroutines                 | 27.8 ms                                                      | 22.5 ms: 1.24x faster                                                        |
| async_tree_io_tg           | 1.15 sec                                                     | 944 ms: 1.22x faster                                                         |
| json_dumps                 | 13.3 ms                                                      | 10.9 ms: 1.22x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 629 ms: 1.20x faster                                                         |
| json_loads                 | 28.9 us                                                      | 25.8 us: 1.12x faster                                                        |
| xml_etree_parse            | 155 ms                                                       | 146 ms: 1.06x faster                                                         |
| logging_simple             | 7.24 us                                                      | 6.93 us: 1.05x faster                                                        |
| thrift                     | 931 us                                                       | 900 us: 1.03x faster                                                         |
| sympy_sum                  | 186 ms                                                       | 181 ms: 1.02x faster                                                         |
| mdp                        | 2.77 sec                                                     | 2.71 sec: 1.02x faster                                                       |
| logging_format             | 7.71 us                                                      | 7.60 us: 1.01x faster                                                        |
| dask                       | 410 ms                                                       | 418 ms: 1.02x slower                                                         |
| chameleon                  | 7.92 ms                                                      | 8.14 ms: 1.03x slower                                                        |
| deepcopy                   | 391 us                                                       | 405 us: 1.03x slower                                                         |
| tornado_http               | 124 ms                                                       | 129 ms: 1.04x slower                                                         |
| chaos                      | 74.9 ms                                                      | 77.7 ms: 1.04x slower                                                        |
| pickle_pure_python         | 316 us                                                       | 328 us: 1.04x slower                                                         |
| deepcopy_reduce            | 3.40 us                                                      | 3.53 us: 1.04x slower                                                        |
| logging_silent             | 100 ns                                                       | 104 ns: 1.04x slower                                                         |
| sympy_str                  | 337 ms                                                       | 350 ms: 1.04x slower                                                         |
| regex_effbot               | 3.34 ms                                                      | 3.47 ms: 1.04x slower                                                        |
| deltablue                  | 3.97 ms                                                      | 4.15 ms: 1.05x slower                                                        |
| sympy_integrate            | 25.8 ms                                                      | 27.0 ms: 1.05x slower                                                        |
| pidigits                   | 251 ms                                                       | 265 ms: 1.05x slower                                                         |
| gc_traversal               | 4.15 ms                                                      | 4.39 ms: 1.06x slower                                                        |
| genshi_text                | 25.5 ms                                                      | 27.0 ms: 1.06x slower                                                        |
| regex_v8                   | 24.4 ms                                                      | 25.9 ms: 1.06x slower                                                        |
| sympy_expand               | 553 ms                                                       | 587 ms: 1.06x slower                                                         |
| xml_etree_iterparse        | 107 ms                                                       | 113 ms: 1.06x slower                                                         |
| regex_dna                  | 227 ms                                                       | 242 ms: 1.06x slower                                                         |
| sqlglot_parse              | 1.51 ms                                                      | 1.61 ms: 1.07x slower                                                        |
| sqlglot_transpile          | 1.91 ms                                                      | 2.04 ms: 1.07x slower                                                        |
| comprehensions             | 25.1 us                                                      | 26.8 us: 1.07x slower                                                        |
| richards_super             | 63.6 ms                                                      | 68.0 ms: 1.07x slower                                                        |
| django_template            | 39.3 ms                                                      | 42.3 ms: 1.08x slower                                                        |
| sqlglot_normalize          | 122 ms                                                       | 131 ms: 1.08x slower                                                         |
| genshi_xml                 | 57.1 ms                                                      | 61.9 ms: 1.08x slower                                                        |
| pickle_dict                | 32.3 us                                                      | 35.2 us: 1.09x slower                                                        |
| meteor_contest             | 131 ms                                                       | 143 ms: 1.10x slower                                                         |
| pickle                     | 9.89 us                                                      | 10.9 us: 1.10x slower                                                        |
| pathlib                    | 18.9 ms                                                      | 21.0 ms: 1.11x slower                                                        |
| bench_mp_pool              | 4.70 ms                                                      | 5.22 ms: 1.11x slower                                                        |
| crypto_pyaes               | 83.3 ms                                                      | 92.5 ms: 1.11x slower                                                        |
| html5lib                   | 72.2 ms                                                      | 80.4 ms: 1.11x slower                                                        |
| unpickle                   | 13.3 us                                                      | 14.8 us: 1.11x slower                                                        |
| pycparser                  | 1.31 sec                                                     | 1.47 sec: 1.12x slower                                                       |
| pickle_list                | 3.94 us                                                      | 4.46 us: 1.13x slower                                                        |
| 2to3                       | 287 ms                                                       | 325 ms: 1.13x slower                                                         |
| mypy2                      | 762 ms                                                       | 865 ms: 1.14x slower                                                         |
| xml_etree_process          | 55.9 ms                                                      | 63.4 ms: 1.14x slower                                                        |
| raytrace                   | 309 ms                                                       | 352 ms: 1.14x slower                                                         |
| bench_thread_pool          | 1.00 ms                                                      | 1.14 ms: 1.14x slower                                                        |
| dulwich_log                | 67.4 ms                                                      | 77.3 ms: 1.15x slower                                                        |
| gunicorn                   | 966 us                                                       | 1.11 ms: 1.15x slower                                                        |
| docutils                   | 2.85 sec                                                     | 3.28 sec: 1.15x slower                                                       |
| sqlite_synth               | 2.52 us                                                      | 2.91 us: 1.15x slower                                                        |
| xml_etree_generate         | 79.7 ms                                                      | 92.4 ms: 1.16x slower                                                        |
| sqlglot_optimize           | 59.0 ms                                                      | 68.5 ms: 1.16x slower                                                        |
| aiohttp                    | 986 us                                                       | 1.15 ms: 1.16x slower                                                        |
| create_gc_cycles           | 1.58 ms                                                      | 1.84 ms: 1.17x slower                                                        |
| nqueens                    | 103 ms                                                       | 122 ms: 1.19x slower                                                         |
| python_startup             | 10.7 ms                                                      | 12.9 ms: 1.20x slower                                                        |
| deepcopy_memo              | 37.5 us                                                      | 45.4 us: 1.21x slower                                                        |
| fannkuch                   | 416 ms                                                       | 507 ms: 1.22x slower                                                         |
| richards                   | 49.7 ms                                                      | 61.1 ms: 1.23x slower                                                        |
| pprint_pformat             | 1.67 sec                                                     | 2.06 sec: 1.24x slower                                                       |
| async_generators           | 322 ms                                                       | 400 ms: 1.24x slower                                                         |
| telco                      | 6.81 ms                                                      | 8.54 ms: 1.25x slower                                                        |
| pprint_safe_repr           | 805 ms                                                       | 1.01 sec: 1.26x slower                                                       |
| coverage                   | 66.1 ms                                                      | 83.9 ms: 1.27x slower                                                        |
| go                         | 158 ms                                                       | 204 ms: 1.29x slower                                                         |
| mako                       | 11.0 ms                                                      | 14.4 ms: 1.31x slower                                                        |
| tomli_loads                | 2.25 sec                                                     | 2.98 sec: 1.32x slower                                                       |
| scimark_lu                 | 114 ms                                                       | 152 ms: 1.33x slower                                                         |
| unpickle_pure_python       | 238 us                                                       | 319 us: 1.34x slower                                                         |
| regex_compile              | 156 ms                                                       | 209 ms: 1.34x slower                                                         |
| float                      | 74.9 ms                                                      | 102 ms: 1.36x slower                                                         |
| nbody                      | 92.9 ms                                                      | 129 ms: 1.39x slower                                                         |
| unpack_sequence            | 45.7 ns                                                      | 64.4 ns: 1.41x slower                                                        |
| python_startup_no_site     | 7.73 ms                                                      | 11.2 ms: 1.45x slower                                                        |
| scimark_monte_carlo        | 69.8 ms                                                      | 102 ms: 1.46x slower                                                         |
| pyflate                    | 449 ms                                                       | 666 ms: 1.48x slower                                                         |
| scimark_sor                | 110 ms                                                       | 167 ms: 1.52x slower                                                         |
| hexiom                     | 6.98 ms                                                      | 11.0 ms: 1.57x slower                                                        |
| scimark_fft                | 281 ms                                                       | 446 ms: 1.59x slower                                                         |
| spectral_norm              | 95.1 ms                                                      | 158 ms: 1.66x slower                                                         |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 6.79 ms: 1.67x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.06x slower                                                                 |

Benchmark hidden because not significant (3): unpickle_list, asyncio_websockets, json
Ignored benchmarks (3) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.02x