# Results vs. 3.11.0

- fork: mdboom
- ref: tier2_func_simple
- machine: linux-x86_64
- commit hash: 81bda60
- commit date: 2024-04-05
- overall geometric mean: 1.06x faster
- HPT reliability: 93.60%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 297 ms: 1.04x slower                                                      |
| chameleon      | 7.92 ms                                                      | 7.43 ms: 1.07x faster                                                     |
| docutils       | 2.85 sec                                                     | 3.08 sec: 1.08x slower                                                    |
| html5lib       | 72.2 ms                                                      | 73.0 ms: 1.01x slower                                                     |
| tornado_http   | 124 ms                                                       | 121 ms: 1.02x faster                                                      |
| Geometric mean | (ref)                                                        | 1.01x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_none_tg         | 474 ms                                                       | 335 ms: 1.42x faster                                                      |
| async_tree_memoization_tg  | 600 ms                                                       | 425 ms: 1.41x faster                                                      |
| async_tree_memoization     | 629 ms                                                       | 446 ms: 1.41x faster                                                      |
| async_tree_none            | 518 ms                                                       | 378 ms: 1.37x faster                                                      |
| async_tree_io              | 1.17 sec                                                     | 856 ms: 1.37x faster                                                      |
| async_tree_io_tg           | 1.15 sec                                                     | 869 ms: 1.33x faster                                                      |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 593 ms: 1.27x faster                                                      |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 611 ms: 1.23x faster                                                      |
| Geometric mean             | (ref)                                                        | 1.35x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 251 ms                                                       | 262 ms: 1.04x slower                                                      |
| nbody          | 92.9 ms                                                      | 103 ms: 1.11x slower                                                      |
| Geometric mean | (ref)                                                        | 1.05x slower                                                              |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 148 ms: 1.06x faster                                                      |
| regex_dna      | 227 ms                                                       | 241 ms: 1.06x slower                                                      |
| regex_effbot   | 3.34 ms                                                      | 3.54 ms: 1.06x slower                                                     |
| regex_v8       | 24.4 ms                                                      | 26.6 ms: 1.09x slower                                                     |
| Geometric mean | (ref)                                                        | 1.04x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                     |
| json_loads           | 28.9 us                                                      | 25.4 us: 1.14x faster                                                     |
| xml_etree_parse      | 155 ms                                                       | 142 ms: 1.09x faster                                                      |
| xml_etree_iterparse  | 107 ms                                                       | 99.8 ms: 1.07x faster                                                     |
| pickle_dict          | 32.3 us                                                      | 30.8 us: 1.05x faster                                                     |
| tomli_loads          | 2.25 sec                                                     | 2.15 sec: 1.05x faster                                                    |
| unpickle_pure_python | 238 us                                                       | 230 us: 1.04x faster                                                      |
| pickle_pure_python   | 316 us                                                       | 313 us: 1.01x faster                                                      |
| unpickle_list        | 4.60 us                                                      | 4.63 us: 1.01x slower                                                     |
| xml_etree_process    | 55.9 ms                                                      | 58.0 ms: 1.04x slower                                                     |
| pickle               | 9.89 us                                                      | 10.3 us: 1.04x slower                                                     |
| xml_etree_generate   | 79.7 ms                                                      | 83.5 ms: 1.05x slower                                                     |
| pickle_list          | 3.94 us                                                      | 4.38 us: 1.11x slower                                                     |
| unpickle             | 13.3 us                                                      | 14.8 us: 1.11x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.02x faster                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 13.4 ms: 1.25x slower                                                     |
| python_startup_no_site | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                                     |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| mako           | 11.0 ms                                                      | 10.1 ms: 1.09x faster                                                     |
| genshi_xml     | 57.1 ms                                                      | 56.4 ms: 1.01x faster                                                     |
| genshi_text    | 25.5 ms                                                      | 26.1 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                        | 1.02x faster                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-pythonperf2-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 118 us: 4.50x faster                                                      |
| asyncio_tcp                | 747 ms                                                       | 372 ms: 2.01x faster                                                      |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                    |
| generators                 | 54.6 ms                                                      | 33.4 ms: 1.63x faster                                                     |
| pylint                     | 514 ms                                                       | 335 ms: 1.54x faster                                                      |
| async_tree_none_tg         | 474 ms                                                       | 335 ms: 1.42x faster                                                      |
| async_tree_memoization_tg  | 600 ms                                                       | 425 ms: 1.41x faster                                                      |
| async_tree_memoization     | 629 ms                                                       | 446 ms: 1.41x faster                                                      |
| async_tree_none            | 518 ms                                                       | 378 ms: 1.37x faster                                                      |
| async_tree_io              | 1.17 sec                                                     | 856 ms: 1.37x faster                                                      |
| async_tree_io_tg           | 1.15 sec                                                     | 869 ms: 1.33x faster                                                      |
| comprehensions             | 25.1 us                                                      | 19.3 us: 1.30x faster                                                     |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 593 ms: 1.27x faster                                                      |
| json_dumps                 | 13.3 ms                                                      | 10.6 ms: 1.25x faster                                                     |
| coroutines                 | 27.8 ms                                                      | 22.3 ms: 1.25x faster                                                     |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 611 ms: 1.23x faster                                                      |
| richards_super             | 63.6 ms                                                      | 52.3 ms: 1.22x faster                                                     |
| chaos                      | 74.9 ms                                                      | 64.7 ms: 1.16x faster                                                     |
| raytrace                   | 309 ms                                                       | 270 ms: 1.15x faster                                                      |
| logging_simple             | 7.24 us                                                      | 6.36 us: 1.14x faster                                                     |
| json_loads                 | 28.9 us                                                      | 25.4 us: 1.14x faster                                                     |
| sympy_sum                  | 186 ms                                                       | 165 ms: 1.12x faster                                                      |
| logging_format             | 7.71 us                                                      | 7.02 us: 1.10x faster                                                     |
| xml_etree_parse            | 155 ms                                                       | 142 ms: 1.09x faster                                                      |
| sympy_str                  | 337 ms                                                       | 310 ms: 1.09x faster                                                      |
| richards                   | 49.7 ms                                                      | 45.7 ms: 1.09x faster                                                     |
| mako                       | 11.0 ms                                                      | 10.1 ms: 1.09x faster                                                     |
| sqlglot_parse              | 1.51 ms                                                      | 1.40 ms: 1.08x faster                                                     |
| crypto_pyaes               | 83.3 ms                                                      | 77.3 ms: 1.08x faster                                                     |
| sympy_expand               | 553 ms                                                       | 516 ms: 1.07x faster                                                      |
| xml_etree_iterparse        | 107 ms                                                       | 99.8 ms: 1.07x faster                                                     |
| chameleon                  | 7.92 ms                                                      | 7.43 ms: 1.07x faster                                                     |
| sqlglot_transpile          | 1.91 ms                                                      | 1.80 ms: 1.06x faster                                                     |
| thrift                     | 931 us                                                       | 880 us: 1.06x faster                                                      |
| deltablue                  | 3.97 ms                                                      | 3.75 ms: 1.06x faster                                                     |
| fannkuch                   | 416 ms                                                       | 393 ms: 1.06x faster                                                      |
| regex_compile              | 156 ms                                                       | 148 ms: 1.06x faster                                                      |
| pycparser                  | 1.31 sec                                                     | 1.24 sec: 1.05x faster                                                    |
| mdp                        | 2.77 sec                                                     | 2.63 sec: 1.05x faster                                                    |
| bench_thread_pool          | 1.00 ms                                                      | 951 us: 1.05x faster                                                      |
| pickle_dict                | 32.3 us                                                      | 30.8 us: 1.05x faster                                                     |
| tomli_loads                | 2.25 sec                                                     | 2.15 sec: 1.05x faster                                                    |
| unpickle_pure_python       | 238 us                                                       | 230 us: 1.04x faster                                                      |
| logging_silent             | 100 ns                                                       | 97.2 ns: 1.03x faster                                                     |
| deepcopy                   | 391 us                                                       | 379 us: 1.03x faster                                                      |
| tornado_http               | 124 ms                                                       | 121 ms: 1.02x faster                                                      |
| nqueens                    | 103 ms                                                       | 100 ms: 1.02x faster                                                      |
| json                       | 5.58 ms                                                      | 5.48 ms: 1.02x faster                                                     |
| spectral_norm              | 95.1 ms                                                      | 93.4 ms: 1.02x faster                                                     |
| dask                       | 410 ms                                                       | 403 ms: 1.02x faster                                                      |
| sympy_integrate            | 25.8 ms                                                      | 25.4 ms: 1.02x faster                                                     |
| genshi_xml                 | 57.1 ms                                                      | 56.4 ms: 1.01x faster                                                     |
| pickle_pure_python         | 316 us                                                       | 313 us: 1.01x faster                                                      |
| deepcopy_memo              | 37.5 us                                                      | 37.2 us: 1.01x faster                                                     |
| scimark_monte_carlo        | 69.8 ms                                                      | 69.4 ms: 1.01x faster                                                     |
| unpickle_list              | 4.60 us                                                      | 4.63 us: 1.01x slower                                                     |
| deepcopy_reduce            | 3.40 us                                                      | 3.43 us: 1.01x slower                                                     |
| html5lib                   | 72.2 ms                                                      | 73.0 ms: 1.01x slower                                                     |
| sqlglot_normalize          | 122 ms                                                       | 123 ms: 1.01x slower                                                      |
| meteor_contest             | 131 ms                                                       | 133 ms: 1.02x slower                                                      |
| pathlib                    | 18.9 ms                                                      | 19.4 ms: 1.02x slower                                                     |
| hexiom                     | 6.98 ms                                                      | 7.13 ms: 1.02x slower                                                     |
| pprint_pformat             | 1.67 sec                                                     | 1.70 sec: 1.02x slower                                                    |
| genshi_text                | 25.5 ms                                                      | 26.1 ms: 1.02x slower                                                     |
| scimark_lu                 | 114 ms                                                       | 118 ms: 1.03x slower                                                      |
| pprint_safe_repr           | 805 ms                                                       | 833 ms: 1.03x slower                                                      |
| 2to3                       | 287 ms                                                       | 297 ms: 1.04x slower                                                      |
| xml_etree_process          | 55.9 ms                                                      | 58.0 ms: 1.04x slower                                                     |
| pidigits                   | 251 ms                                                       | 262 ms: 1.04x slower                                                      |
| pickle                     | 9.89 us                                                      | 10.3 us: 1.04x slower                                                     |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.24 ms: 1.04x slower                                                     |
| xml_etree_generate         | 79.7 ms                                                      | 83.5 ms: 1.05x slower                                                     |
| regex_dna                  | 227 ms                                                       | 241 ms: 1.06x slower                                                      |
| regex_effbot               | 3.34 ms                                                      | 3.54 ms: 1.06x slower                                                     |
| sqlite_synth               | 2.52 us                                                      | 2.68 us: 1.06x slower                                                     |
| sqlglot_optimize           | 59.0 ms                                                      | 62.9 ms: 1.07x slower                                                     |
| gc_traversal               | 4.15 ms                                                      | 4.44 ms: 1.07x slower                                                     |
| mypy2                      | 762 ms                                                       | 820 ms: 1.08x slower                                                      |
| docutils                   | 2.85 sec                                                     | 3.08 sec: 1.08x slower                                                    |
| regex_v8                   | 24.4 ms                                                      | 26.6 ms: 1.09x slower                                                     |
| nbody                      | 92.9 ms                                                      | 103 ms: 1.11x slower                                                      |
| pickle_list                | 3.94 us                                                      | 4.38 us: 1.11x slower                                                     |
| unpickle                   | 13.3 us                                                      | 14.8 us: 1.11x slower                                                     |
| pyflate                    | 449 ms                                                       | 504 ms: 1.12x slower                                                      |
| go                         | 158 ms                                                       | 177 ms: 1.12x slower                                                      |
| gunicorn                   | 966 us                                                       | 1.09 ms: 1.13x slower                                                     |
| scimark_fft                | 281 ms                                                       | 319 ms: 1.14x slower                                                      |
| aiohttp                    | 986 us                                                       | 1.13 ms: 1.15x slower                                                     |
| create_gc_cycles           | 1.58 ms                                                      | 1.87 ms: 1.19x slower                                                     |
| async_generators           | 322 ms                                                       | 383 ms: 1.19x slower                                                      |
| telco                      | 6.81 ms                                                      | 8.29 ms: 1.22x slower                                                     |
| coverage                   | 66.1 ms                                                      | 80.7 ms: 1.22x slower                                                     |
| python_startup             | 10.7 ms                                                      | 13.4 ms: 1.25x slower                                                     |
| scimark_sor                | 110 ms                                                       | 152 ms: 1.38x slower                                                      |
| python_startup_no_site     | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                              |

Benchmark hidden because not significant (4): float, dulwich_log, asyncio_websockets, bench_mp_pool
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 93.60% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x