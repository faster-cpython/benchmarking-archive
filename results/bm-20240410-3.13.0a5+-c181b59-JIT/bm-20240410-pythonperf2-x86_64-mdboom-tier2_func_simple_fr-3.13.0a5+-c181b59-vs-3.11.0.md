# Results vs. 3.11.0

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: linux-x86_64
- commit hash: c181b59
- commit date: 2024-04-10
- overall geometric mean: 1.05x faster
- HPT reliability: 85.65%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 287 ms                                                       | 300 ms: 1.05x slower                                                         |
| chameleon      | 7.92 ms                                                      | 7.65 ms: 1.04x faster                                                        |
| docutils       | 2.85 sec                                                     | 3.10 sec: 1.09x slower                                                       |
| html5lib       | 72.2 ms                                                      | 75.3 ms: 1.04x slower                                                        |
| tornado_http   | 124 ms                                                       | 122 ms: 1.02x faster                                                         |
| Geometric mean | (ref)                                                        | 1.02x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none_tg         | 474 ms                                                       | 333 ms: 1.42x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 446 ms: 1.41x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 425 ms: 1.41x faster                                                         |
| async_tree_none            | 518 ms                                                       | 378 ms: 1.37x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 871 ms: 1.34x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 868 ms: 1.33x faster                                                         |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 591 ms: 1.27x faster                                                         |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 609 ms: 1.24x faster                                                         |
| Geometric mean             | (ref)                                                        | 1.35x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 74.9 ms                                                      | 76.1 ms: 1.02x slower                                                        |
| nbody          | 92.9 ms                                                      | 96.2 ms: 1.04x slower                                                        |
| pidigits       | 251 ms                                                       | 261 ms: 1.04x slower                                                         |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 156 ms                                                       | 148 ms: 1.05x faster                                                         |
| regex_v8       | 24.4 ms                                                      | 25.5 ms: 1.04x slower                                                        |
| regex_dna      | 227 ms                                                       | 245 ms: 1.08x slower                                                         |
| regex_effbot   | 3.34 ms                                                      | 3.71 ms: 1.11x slower                                                        |
| Geometric mean | (ref)                                                        | 1.04x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                      | 10.4 ms: 1.27x faster                                                        |
| json_loads           | 28.9 us                                                      | 25.5 us: 1.13x faster                                                        |
| tomli_loads          | 2.25 sec                                                     | 2.13 sec: 1.06x faster                                                       |
| xml_etree_iterparse  | 107 ms                                                       | 102 ms: 1.05x faster                                                         |
| xml_etree_parse      | 155 ms                                                       | 148 ms: 1.04x faster                                                         |
| unpickle_pure_python | 238 us                                                       | 232 us: 1.03x faster                                                         |
| pickle_pure_python   | 316 us                                                       | 311 us: 1.02x faster                                                         |
| pickle_dict          | 32.3 us                                                      | 32.6 us: 1.01x slower                                                        |
| unpickle_list        | 4.60 us                                                      | 4.66 us: 1.01x slower                                                        |
| xml_etree_process    | 55.9 ms                                                      | 59.0 ms: 1.06x slower                                                        |
| xml_etree_generate   | 79.7 ms                                                      | 84.6 ms: 1.06x slower                                                        |
| pickle               | 9.89 us                                                      | 10.6 us: 1.07x slower                                                        |
| pickle_list          | 3.94 us                                                      | 4.39 us: 1.11x slower                                                        |
| unpickle             | 13.3 us                                                      | 15.0 us: 1.13x slower                                                        |
| Geometric mean       | (ref)                                                        | 1.01x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup         | 10.7 ms                                                      | 13.4 ms: 1.25x slower                                                        |
| python_startup_no_site | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                                        |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako           | 11.0 ms                                                      | 10.1 ms: 1.09x faster                                                        |
| genshi_xml     | 57.1 ms                                                      | 61.8 ms: 1.08x slower                                                        |
| genshi_text    | 25.5 ms                                                      | 28.0 ms: 1.10x slower                                                        |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240410-pythonperf2-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 532 us                                                       | 124 us: 4.28x faster                                                         |
| asyncio_tcp                | 747 ms                                                       | 374 ms: 2.00x faster                                                         |
| asyncio_tcp_ssl            | 3.07 sec                                                     | 1.58 sec: 1.94x faster                                                       |
| generators                 | 54.6 ms                                                      | 33.2 ms: 1.65x faster                                                        |
| pylint                     | 514 ms                                                       | 333 ms: 1.54x faster                                                         |
| async_tree_none_tg         | 474 ms                                                       | 333 ms: 1.42x faster                                                         |
| async_tree_memoization     | 629 ms                                                       | 446 ms: 1.41x faster                                                         |
| async_tree_memoization_tg  | 600 ms                                                       | 425 ms: 1.41x faster                                                         |
| async_tree_none            | 518 ms                                                       | 378 ms: 1.37x faster                                                         |
| async_tree_io              | 1.17 sec                                                     | 871 ms: 1.34x faster                                                         |
| async_tree_io_tg           | 1.15 sec                                                     | 868 ms: 1.33x faster                                                         |
| comprehensions             | 25.1 us                                                      | 19.1 us: 1.31x faster                                                        |
| json_dumps                 | 13.3 ms                                                      | 10.4 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed_tg | 750 ms                                                       | 591 ms: 1.27x faster                                                         |
| coroutines                 | 27.8 ms                                                      | 22.1 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed    | 753 ms                                                       | 609 ms: 1.24x faster                                                         |
| richards_super             | 63.6 ms                                                      | 53.7 ms: 1.18x faster                                                        |
| chaos                      | 74.9 ms                                                      | 64.8 ms: 1.16x faster                                                        |
| logging_simple             | 7.24 us                                                      | 6.27 us: 1.16x faster                                                        |
| raytrace                   | 309 ms                                                       | 272 ms: 1.14x faster                                                         |
| sympy_sum                  | 186 ms                                                       | 164 ms: 1.14x faster                                                         |
| json_loads                 | 28.9 us                                                      | 25.5 us: 1.13x faster                                                        |
| logging_format             | 7.71 us                                                      | 6.95 us: 1.11x faster                                                        |
| mako                       | 11.0 ms                                                      | 10.1 ms: 1.09x faster                                                        |
| sympy_str                  | 337 ms                                                       | 309 ms: 1.09x faster                                                         |
| crypto_pyaes               | 83.3 ms                                                      | 76.9 ms: 1.08x faster                                                        |
| bench_thread_pool          | 1.00 ms                                                      | 930 us: 1.08x faster                                                         |
| fannkuch                   | 416 ms                                                       | 389 ms: 1.07x faster                                                         |
| sympy_expand               | 553 ms                                                       | 518 ms: 1.07x faster                                                         |
| mdp                        | 2.77 sec                                                     | 2.59 sec: 1.07x faster                                                       |
| sqlglot_parse              | 1.51 ms                                                      | 1.42 ms: 1.06x faster                                                        |
| richards                   | 49.7 ms                                                      | 46.7 ms: 1.06x faster                                                        |
| tomli_loads                | 2.25 sec                                                     | 2.13 sec: 1.06x faster                                                       |
| regex_compile              | 156 ms                                                       | 148 ms: 1.05x faster                                                         |
| sqlglot_transpile          | 1.91 ms                                                      | 1.82 ms: 1.05x faster                                                        |
| xml_etree_iterparse        | 107 ms                                                       | 102 ms: 1.05x faster                                                         |
| deltablue                  | 3.97 ms                                                      | 3.80 ms: 1.05x faster                                                        |
| xml_etree_parse            | 155 ms                                                       | 148 ms: 1.04x faster                                                         |
| thrift                     | 931 us                                                       | 897 us: 1.04x faster                                                         |
| chameleon                  | 7.92 ms                                                      | 7.65 ms: 1.04x faster                                                        |
| json                       | 5.58 ms                                                      | 5.40 ms: 1.03x faster                                                        |
| nqueens                    | 103 ms                                                       | 99.8 ms: 1.03x faster                                                        |
| sympy_integrate            | 25.8 ms                                                      | 25.1 ms: 1.03x faster                                                        |
| pycparser                  | 1.31 sec                                                     | 1.27 sec: 1.03x faster                                                       |
| unpickle_pure_python       | 238 us                                                       | 232 us: 1.03x faster                                                         |
| dask                       | 410 ms                                                       | 400 ms: 1.02x faster                                                         |
| tornado_http               | 124 ms                                                       | 122 ms: 1.02x faster                                                         |
| pickle_pure_python         | 316 us                                                       | 311 us: 1.02x faster                                                         |
| logging_silent             | 100 ns                                                       | 98.9 ns: 1.01x faster                                                        |
| spectral_norm              | 95.1 ms                                                      | 93.8 ms: 1.01x faster                                                        |
| pickle_dict                | 32.3 us                                                      | 32.6 us: 1.01x slower                                                        |
| dulwich_log                | 67.4 ms                                                      | 68.2 ms: 1.01x slower                                                        |
| meteor_contest             | 131 ms                                                       | 132 ms: 1.01x slower                                                         |
| unpickle_list              | 4.60 us                                                      | 4.66 us: 1.01x slower                                                        |
| float                      | 74.9 ms                                                      | 76.1 ms: 1.02x slower                                                        |
| sqlglot_normalize          | 122 ms                                                       | 124 ms: 1.02x slower                                                         |
| deepcopy                   | 391 us                                                       | 401 us: 1.03x slower                                                         |
| pprint_safe_repr           | 805 ms                                                       | 827 ms: 1.03x slower                                                         |
| hexiom                     | 6.98 ms                                                      | 7.17 ms: 1.03x slower                                                        |
| scimark_sparse_mat_mult    | 4.06 ms                                                      | 4.18 ms: 1.03x slower                                                        |
| scimark_monte_carlo        | 69.8 ms                                                      | 72.0 ms: 1.03x slower                                                        |
| deepcopy_memo              | 37.5 us                                                      | 38.8 us: 1.03x slower                                                        |
| pathlib                    | 18.9 ms                                                      | 19.6 ms: 1.03x slower                                                        |
| pprint_pformat             | 1.67 sec                                                     | 1.72 sec: 1.03x slower                                                       |
| nbody                      | 92.9 ms                                                      | 96.2 ms: 1.04x slower                                                        |
| pidigits                   | 251 ms                                                       | 261 ms: 1.04x slower                                                         |
| html5lib                   | 72.2 ms                                                      | 75.3 ms: 1.04x slower                                                        |
| regex_v8                   | 24.4 ms                                                      | 25.5 ms: 1.04x slower                                                        |
| 2to3                       | 287 ms                                                       | 300 ms: 1.05x slower                                                         |
| xml_etree_process          | 55.9 ms                                                      | 59.0 ms: 1.06x slower                                                        |
| gc_traversal               | 4.15 ms                                                      | 4.38 ms: 1.06x slower                                                        |
| xml_etree_generate         | 79.7 ms                                                      | 84.6 ms: 1.06x slower                                                        |
| scimark_lu                 | 114 ms                                                       | 121 ms: 1.06x slower                                                         |
| sqlglot_optimize           | 59.0 ms                                                      | 62.9 ms: 1.07x slower                                                        |
| pickle                     | 9.89 us                                                      | 10.6 us: 1.07x slower                                                        |
| pyflate                    | 449 ms                                                       | 483 ms: 1.08x slower                                                         |
| sqlite_synth               | 2.52 us                                                      | 2.71 us: 1.08x slower                                                        |
| regex_dna                  | 227 ms                                                       | 245 ms: 1.08x slower                                                         |
| genshi_xml                 | 57.1 ms                                                      | 61.8 ms: 1.08x slower                                                        |
| mypy2                      | 762 ms                                                       | 828 ms: 1.09x slower                                                         |
| docutils                   | 2.85 sec                                                     | 3.10 sec: 1.09x slower                                                       |
| deepcopy_reduce            | 3.40 us                                                      | 3.72 us: 1.09x slower                                                        |
| genshi_text                | 25.5 ms                                                      | 28.0 ms: 1.10x slower                                                        |
| go                         | 158 ms                                                       | 175 ms: 1.11x slower                                                         |
| regex_effbot               | 3.34 ms                                                      | 3.71 ms: 1.11x slower                                                        |
| pickle_list                | 3.94 us                                                      | 4.39 us: 1.11x slower                                                        |
| unpickle                   | 13.3 us                                                      | 15.0 us: 1.13x slower                                                        |
| scimark_fft                | 281 ms                                                       | 317 ms: 1.13x slower                                                         |
| gunicorn                   | 966 us                                                       | 1.10 ms: 1.14x slower                                                        |
| aiohttp                    | 986 us                                                       | 1.15 ms: 1.16x slower                                                        |
| create_gc_cycles           | 1.58 ms                                                      | 1.87 ms: 1.19x slower                                                        |
| coverage                   | 66.1 ms                                                      | 78.8 ms: 1.19x slower                                                        |
| async_generators           | 322 ms                                                       | 384 ms: 1.19x slower                                                         |
| telco                      | 6.81 ms                                                      | 8.29 ms: 1.22x slower                                                        |
| python_startup             | 10.7 ms                                                      | 13.4 ms: 1.25x slower                                                        |
| scimark_sor                | 110 ms                                                       | 152 ms: 1.38x slower                                                         |
| python_startup_no_site     | 7.73 ms                                                      | 11.8 ms: 1.52x slower                                                        |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                                 |

Benchmark hidden because not significant (2): bench_mp_pool, asyncio_websockets
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-pythonperf2-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 85.65% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x