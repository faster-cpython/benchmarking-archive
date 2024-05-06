# Results vs. 3.11.0

- fork: mdboom
- ref: tier2_func_simple
- machine: linux-x86_64
- commit hash: 81bda60
- commit date: 2024-04-05
- overall geometric mean: 1.05x faster
- HPT reliability: 51.39%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 279 ms: 1.06x slower                                                |
| chameleon      | 6.70 ms                                                | 7.07 ms: 1.05x slower                                               |
| docutils       | 2.66 sec                                               | 2.94 sec: 1.10x slower                                              |
| html5lib       | 64.8 ms                                                | 68.7 ms: 1.06x slower                                               |
| tornado_http   | 98.1 ms                                                | 96.6 ms: 1.02x faster                                               |
| Geometric mean | (ref)                                                  | 1.05x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 354 ms: 1.49x faster                                                |
| async_tree_none_tg         | 491 ms                                                 | 337 ms: 1.46x faster                                                |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.41x faster                                                |
| async_tree_memoization     | 639 ms                                                 | 459 ms: 1.39x faster                                                |
| async_tree_io_tg           | 1.29 sec                                               | 940 ms: 1.38x faster                                                |
| async_tree_io              | 1.29 sec                                               | 937 ms: 1.37x faster                                                |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 600 ms: 1.27x faster                                                |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 610 ms: 1.23x faster                                                |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                        |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 92.3 ms: 1.04x faster                                               |
| float          | 78.9 ms                                                | 77.0 ms: 1.03x faster                                               |
| pidigits       | 194 ms                                                 | 193 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                  | 1.02x faster                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 144 ms: 1.02x slower                                                |
| regex_effbot   | 3.51 ms                                                | 3.86 ms: 1.10x slower                                               |
| regex_v8       | 22.9 ms                                                | 25.5 ms: 1.12x slower                                               |
| regex_dna      | 205 ms                                                 | 230 ms: 1.13x slower                                                |
| Geometric mean | (ref)                                                  | 1.09x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                               |
| tomli_loads          | 2.30 sec                                               | 2.03 sec: 1.14x faster                                              |
| pickle_pure_python   | 320 us                                                 | 306 us: 1.04x faster                                                |
| json_loads           | 29.2 us                                                | 28.2 us: 1.03x faster                                               |
| unpickle_list        | 5.21 us                                                | 5.12 us: 1.02x faster                                               |
| xml_etree_parse      | 164 ms                                                 | 162 ms: 1.02x faster                                                |
| pickle_dict          | 34.6 us                                                | 34.1 us: 1.01x faster                                               |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                |
| unpickle_pure_python | 242 us                                                 | 241 us: 1.00x faster                                                |
| xml_etree_process    | 56.9 ms                                                | 60.2 ms: 1.06x slower                                               |
| pickle               | 11.0 us                                                | 11.6 us: 1.06x slower                                               |
| xml_etree_generate   | 81.1 ms                                                | 87.8 ms: 1.08x slower                                               |
| pickle_list          | 4.59 us                                                | 4.99 us: 1.09x slower                                               |
| unpickle             | 13.8 us                                                | 16.1 us: 1.16x slower                                               |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                        |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 11.0 ms: 1.28x slower                                               |
| python_startup_no_site | 6.01 ms                                                | 9.45 ms: 1.57x slower                                               |
| Geometric mean         | (ref)                                                  | 1.42x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| mako           | 10.7 ms                                                | 10.7 ms: 1.01x slower                                               |
| genshi_xml     | 53.4 ms                                                | 54.1 ms: 1.01x slower                                               |
| genshi_text    | 22.5 ms                                                | 25.2 ms: 1.12x slower                                               |
| Geometric mean | (ref)                                                  | 1.04x slower                                                        |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240405-linux-x86_64-mdboom-tier2_func_simple-3.13.0a5+-81bda60 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 114 us: 4.54x faster                                                |
| generators                 | 74.9 ms                                                | 30.0 ms: 2.50x faster                                               |
| asyncio_tcp                | 875 ms                                                 | 513 ms: 1.71x faster                                                |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                              |
| pylint                     | 476 ms                                                 | 295 ms: 1.61x faster                                                |
| async_tree_none            | 528 ms                                                 | 354 ms: 1.49x faster                                                |
| async_tree_none_tg         | 491 ms                                                 | 337 ms: 1.46x faster                                                |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.41x faster                                                |
| async_tree_memoization     | 639 ms                                                 | 459 ms: 1.39x faster                                                |
| async_tree_io_tg           | 1.29 sec                                               | 940 ms: 1.38x faster                                                |
| async_tree_io              | 1.29 sec                                               | 937 ms: 1.37x faster                                                |
| comprehensions             | 23.6 us                                                | 17.9 us: 1.32x faster                                               |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                               |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 600 ms: 1.27x faster                                                |
| richards_super             | 61.9 ms                                                | 50.3 ms: 1.23x faster                                               |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 610 ms: 1.23x faster                                                |
| coroutines                 | 27.0 ms                                                | 22.6 ms: 1.19x faster                                               |
| chaos                      | 71.9 ms                                                | 62.6 ms: 1.15x faster                                               |
| tomli_loads                | 2.30 sec                                               | 2.03 sec: 1.14x faster                                              |
| richards                   | 49.8 ms                                                | 44.2 ms: 1.13x faster                                               |
| raytrace                   | 309 ms                                                 | 275 ms: 1.12x faster                                                |
| sqlglot_parse              | 1.43 ms                                                | 1.33 ms: 1.08x faster                                               |
| logging_simple             | 6.22 us                                                | 5.83 us: 1.07x faster                                               |
| gc_traversal               | 4.01 ms                                                | 3.77 ms: 1.06x faster                                               |
| sqlglot_transpile          | 1.75 ms                                                | 1.65 ms: 1.06x faster                                               |
| logging_format             | 6.81 us                                                | 6.42 us: 1.06x faster                                               |
| deltablue                  | 3.92 ms                                                | 3.70 ms: 1.06x faster                                               |
| logging_silent             | 111 ns                                                 | 106 ns: 1.04x faster                                                |
| pickle_pure_python         | 320 us                                                 | 306 us: 1.04x faster                                                |
| nbody                      | 96.0 ms                                                | 92.3 ms: 1.04x faster                                               |
| json_loads                 | 29.2 us                                                | 28.2 us: 1.03x faster                                               |
| deepcopy_memo              | 40.2 us                                                | 39.0 us: 1.03x faster                                               |
| fannkuch                   | 405 ms                                                 | 393 ms: 1.03x faster                                                |
| float                      | 78.9 ms                                                | 77.0 ms: 1.03x faster                                               |
| unpickle_list              | 5.21 us                                                | 5.12 us: 1.02x faster                                               |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.94 ms: 1.02x faster                                               |
| tornado_http               | 98.1 ms                                                | 96.6 ms: 1.02x faster                                               |
| xml_etree_parse            | 164 ms                                                 | 162 ms: 1.02x faster                                                |
| pickle_dict                | 34.6 us                                                | 34.1 us: 1.01x faster                                               |
| crypto_pyaes               | 76.7 ms                                                | 75.6 ms: 1.01x faster                                               |
| scimark_fft                | 345 ms                                                 | 341 ms: 1.01x faster                                                |
| sympy_sum                  | 169 ms                                                 | 168 ms: 1.01x faster                                                |
| pidigits                   | 194 ms                                                 | 193 ms: 1.01x faster                                                |
| deepcopy                   | 365 us                                                 | 363 us: 1.01x faster                                                |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                |
| unpickle_pure_python       | 242 us                                                 | 241 us: 1.00x faster                                                |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                                |
| mako                       | 10.7 ms                                                | 10.7 ms: 1.01x slower                                               |
| deepcopy_reduce            | 3.22 us                                                | 3.25 us: 1.01x slower                                               |
| genshi_xml                 | 53.4 ms                                                | 54.1 ms: 1.01x slower                                               |
| hexiom                     | 6.89 ms                                                | 7.01 ms: 1.02x slower                                               |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                                |
| regex_compile              | 141 ms                                                 | 144 ms: 1.02x slower                                                |
| pprint_safe_repr           | 747 ms                                                 | 762 ms: 1.02x slower                                                |
| json                       | 5.24 ms                                                | 5.36 ms: 1.02x slower                                               |
| sympy_expand               | 484 ms                                                 | 496 ms: 1.02x slower                                                |
| pprint_pformat             | 1.55 sec                                               | 1.59 sec: 1.03x slower                                              |
| pathlib                    | 18.5 ms                                                | 19.0 ms: 1.03x slower                                               |
| dask                       | 365 ms                                                 | 375 ms: 1.03x slower                                                |
| bench_thread_pool          | 834 us                                                 | 857 us: 1.03x slower                                                |
| pycparser                  | 1.19 sec                                               | 1.22 sec: 1.03x slower                                              |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                                |
| nqueens                    | 87.9 ms                                                | 90.5 ms: 1.03x slower                                               |
| sympy_integrate            | 21.5 ms                                                | 22.1 ms: 1.03x slower                                               |
| sqlglot_optimize           | 55.3 ms                                                | 57.6 ms: 1.04x slower                                               |
| go                         | 149 ms                                                 | 155 ms: 1.04x slower                                                |
| chameleon                  | 6.70 ms                                                | 7.07 ms: 1.05x slower                                               |
| thrift                     | 784 us                                                 | 828 us: 1.06x slower                                                |
| 2to3                       | 264 ms                                                 | 279 ms: 1.06x slower                                                |
| xml_etree_process          | 56.9 ms                                                | 60.2 ms: 1.06x slower                                               |
| pickle                     | 11.0 us                                                | 11.6 us: 1.06x slower                                               |
| html5lib                   | 64.8 ms                                                | 68.7 ms: 1.06x slower                                               |
| spectral_norm              | 108 ms                                                 | 115 ms: 1.07x slower                                                |
| pyflate                    | 434 ms                                                 | 468 ms: 1.08x slower                                                |
| aiohttp                    | 1.12 ms                                                | 1.21 ms: 1.08x slower                                               |
| gunicorn                   | 1.20 ms                                                | 1.30 ms: 1.08x slower                                               |
| xml_etree_generate         | 81.1 ms                                                | 87.8 ms: 1.08x slower                                               |
| dulwich_log                | 64.6 ms                                                | 70.1 ms: 1.08x slower                                               |
| pickle_list                | 4.59 us                                                | 4.99 us: 1.09x slower                                               |
| regex_effbot               | 3.51 ms                                                | 3.86 ms: 1.10x slower                                               |
| docutils                   | 2.66 sec                                               | 2.94 sec: 1.10x slower                                              |
| regex_v8                   | 22.9 ms                                                | 25.5 ms: 1.12x slower                                               |
| genshi_text                | 22.5 ms                                                | 25.2 ms: 1.12x slower                                               |
| sqlite_synth               | 2.57 us                                                | 2.88 us: 1.12x slower                                               |
| regex_dna                  | 205 ms                                                 | 230 ms: 1.13x slower                                                |
| scimark_lu                 | 116 ms                                                 | 132 ms: 1.14x slower                                                |
| mypy2                      | 686 ms                                                 | 786 ms: 1.15x slower                                                |
| scimark_sor                | 121 ms                                                 | 140 ms: 1.16x slower                                                |
| unpickle                   | 13.8 us                                                | 16.1 us: 1.16x slower                                               |
| create_gc_cycles           | 1.43 ms                                                | 1.73 ms: 1.21x slower                                               |
| async_generators           | 374 ms                                                 | 461 ms: 1.23x slower                                                |
| coverage                   | 78.8 ms                                                | 98.9 ms: 1.26x slower                                               |
| telco                      | 6.86 ms                                                | 8.68 ms: 1.27x slower                                               |
| python_startup             | 8.56 ms                                                | 11.0 ms: 1.28x slower                                               |
| python_startup_no_site     | 6.01 ms                                                | 9.45 ms: 1.57x slower                                               |
| Geometric mean             | (ref)                                                  | 1.05x faster                                                        |

Benchmark hidden because not significant (4): bench_mp_pool, mdp, sympy_str, scimark_monte_carlo
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 51.39% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.10x