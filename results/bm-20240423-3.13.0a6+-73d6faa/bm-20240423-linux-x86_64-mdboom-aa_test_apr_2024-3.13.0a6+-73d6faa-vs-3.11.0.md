# Results vs. 3.11.0

- fork: mdboom
- ref: aa_test_apr_2024
- machine: linux-x86_64
- commit hash: 73d6faa
- commit date: 2024-04-23
- overall geometric mean: 1.07x faster
- HPT reliability: 97.97%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 271 ms: 1.02x slower                                               |
| chameleon      | 6.70 ms                                                | 6.90 ms: 1.03x slower                                              |
| docutils       | 2.66 sec                                               | 2.81 sec: 1.06x slower                                             |
| html5lib       | 64.8 ms                                                | 67.4 ms: 1.04x slower                                              |
| tornado_http   | 98.1 ms                                                | 94.1 ms: 1.04x faster                                              |
| Geometric mean | (ref)                                                  | 1.02x slower                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 352 ms: 1.50x faster                                               |
| async_tree_none_tg         | 491 ms                                                 | 334 ms: 1.47x faster                                               |
| async_tree_memoization_tg  | 626 ms                                                 | 440 ms: 1.43x faster                                               |
| async_tree_io              | 1.29 sec                                               | 908 ms: 1.42x faster                                               |
| async_tree_memoization     | 639 ms                                                 | 461 ms: 1.39x faster                                               |
| async_tree_io_tg           | 1.29 sec                                               | 944 ms: 1.37x faster                                               |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                               |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 613 ms: 1.22x faster                                               |
| Geometric mean             | (ref)                                                  | 1.38x faster                                                       |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                               |
| Geometric mean | (ref)                                                  | 1.01x faster                                                       |

Benchmark hidden because not significant (2): nbody, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 136 ms: 1.04x faster                                               |
| regex_effbot   | 3.51 ms                                                | 3.73 ms: 1.06x slower                                              |
| regex_dna      | 205 ms                                                 | 225 ms: 1.10x slower                                               |
| regex_v8       | 22.9 ms                                                | 25.8 ms: 1.13x slower                                              |
| Geometric mean | (ref)                                                  | 1.06x slower                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.25x faster                                              |
| unpickle_pure_python | 242 us                                                 | 219 us: 1.10x faster                                               |
| json_loads           | 29.2 us                                                | 27.8 us: 1.05x faster                                              |
| pickle_pure_python   | 320 us                                                 | 306 us: 1.05x faster                                               |
| tomli_loads          | 2.30 sec                                               | 2.21 sec: 1.04x faster                                             |
| xml_etree_parse      | 164 ms                                                 | 159 ms: 1.03x faster                                               |
| unpickle_list        | 5.21 us                                                | 5.11 us: 1.02x faster                                              |
| pickle_dict          | 34.6 us                                                | 35.3 us: 1.02x slower                                              |
| xml_etree_process    | 56.9 ms                                                | 60.4 ms: 1.06x slower                                              |
| xml_etree_generate   | 81.1 ms                                                | 87.7 ms: 1.08x slower                                              |
| pickle               | 11.0 us                                                | 12.1 us: 1.10x slower                                              |
| pickle_list          | 4.59 us                                                | 5.07 us: 1.11x slower                                              |
| unpickle             | 13.8 us                                                | 15.6 us: 1.13x slower                                              |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                       |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.09 ms: 1.18x slower                                              |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                              |
| Geometric mean         | (ref)                                                  | 1.20x slower                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 51.9 ms: 1.03x faster                                              |
| mako            | 10.7 ms                                                | 10.9 ms: 1.02x slower                                              |
| django_template | 33.5 ms                                                | 35.0 ms: 1.04x slower                                              |
| genshi_text     | 22.5 ms                                                | 23.9 ms: 1.06x slower                                              |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 113 us: 4.58x faster                                               |
| generators                 | 74.9 ms                                                | 29.8 ms: 2.51x faster                                              |
| asyncio_tcp                | 875 ms                                                 | 505 ms: 1.73x faster                                               |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                             |
| async_tree_none            | 528 ms                                                 | 352 ms: 1.50x faster                                               |
| pylint                     | 476 ms                                                 | 319 ms: 1.49x faster                                               |
| async_tree_none_tg         | 491 ms                                                 | 334 ms: 1.47x faster                                               |
| async_tree_memoization_tg  | 626 ms                                                 | 440 ms: 1.43x faster                                               |
| async_tree_io              | 1.29 sec                                               | 908 ms: 1.42x faster                                               |
| comprehensions             | 23.6 us                                                | 17.0 us: 1.39x faster                                              |
| async_tree_memoization     | 639 ms                                                 | 461 ms: 1.39x faster                                               |
| async_tree_io_tg           | 1.29 sec                                               | 944 ms: 1.37x faster                                               |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                               |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.25x faster                                              |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 613 ms: 1.22x faster                                               |
| deltablue                  | 3.92 ms                                                | 3.27 ms: 1.20x faster                                              |
| coroutines                 | 27.0 ms                                                | 22.8 ms: 1.19x faster                                              |
| raytrace                   | 309 ms                                                 | 264 ms: 1.17x faster                                               |
| chaos                      | 71.9 ms                                                | 61.8 ms: 1.16x faster                                              |
| richards_super             | 61.9 ms                                                | 54.4 ms: 1.14x faster                                              |
| sqlglot_parse              | 1.43 ms                                                | 1.29 ms: 1.11x faster                                              |
| unpickle_pure_python       | 242 us                                                 | 219 us: 1.10x faster                                               |
| sqlglot_transpile          | 1.75 ms                                                | 1.60 ms: 1.09x faster                                              |
| nqueens                    | 87.9 ms                                                | 80.5 ms: 1.09x faster                                              |
| hexiom                     | 6.89 ms                                                | 6.35 ms: 1.09x faster                                              |
| sympy_sum                  | 169 ms                                                 | 157 ms: 1.08x faster                                               |
| logging_simple             | 6.22 us                                                | 5.83 us: 1.07x faster                                              |
| mdp                        | 2.77 sec                                               | 2.60 sec: 1.07x faster                                             |
| sympy_str                  | 297 ms                                                 | 281 ms: 1.06x faster                                               |
| sympy_integrate            | 21.5 ms                                                | 20.4 ms: 1.05x faster                                              |
| djangocms                  | 33.5 us                                                | 31.9 us: 1.05x faster                                              |
| pathlib                    | 18.5 ms                                                | 17.6 ms: 1.05x faster                                              |
| json_loads                 | 29.2 us                                                | 27.8 us: 1.05x faster                                              |
| logging_format             | 6.81 us                                                | 6.49 us: 1.05x faster                                              |
| pickle_pure_python         | 320 us                                                 | 306 us: 1.05x faster                                               |
| tomli_loads                | 2.30 sec                                               | 2.21 sec: 1.04x faster                                             |
| deepcopy_memo              | 40.2 us                                                | 38.5 us: 1.04x faster                                              |
| tornado_http               | 98.1 ms                                                | 94.1 ms: 1.04x faster                                              |
| regex_compile              | 141 ms                                                 | 136 ms: 1.04x faster                                               |
| gc_traversal               | 4.01 ms                                                | 3.87 ms: 1.04x faster                                              |
| xml_etree_parse            | 164 ms                                                 | 159 ms: 1.03x faster                                               |
| go                         | 149 ms                                                 | 144 ms: 1.03x faster                                               |
| richards                   | 49.8 ms                                                | 48.2 ms: 1.03x faster                                              |
| logging_silent             | 111 ns                                                 | 108 ns: 1.03x faster                                               |
| genshi_xml                 | 53.4 ms                                                | 51.9 ms: 1.03x faster                                              |
| fannkuch                   | 405 ms                                                 | 396 ms: 1.02x faster                                               |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                               |
| deepcopy                   | 365 us                                                 | 357 us: 1.02x faster                                               |
| json                       | 5.24 ms                                                | 5.13 ms: 1.02x faster                                              |
| crypto_pyaes               | 76.7 ms                                                | 75.1 ms: 1.02x faster                                              |
| sympy_expand               | 484 ms                                                 | 475 ms: 1.02x faster                                               |
| unpickle_list              | 5.21 us                                                | 5.11 us: 1.02x faster                                              |
| sqlglot_normalize          | 113 ms                                                 | 111 ms: 1.02x faster                                               |
| pprint_pformat             | 1.55 sec                                               | 1.54 sec: 1.01x faster                                             |
| deepcopy_reduce            | 3.22 us                                                | 3.19 us: 1.01x faster                                              |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.00x faster                                              |
| bench_thread_pool          | 834 us                                                 | 833 us: 1.00x faster                                               |
| pprint_safe_repr           | 747 ms                                                 | 752 ms: 1.01x slower                                               |
| pycparser                  | 1.19 sec                                               | 1.20 sec: 1.01x slower                                             |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.01x slower                                               |
| mako                       | 10.7 ms                                                | 10.9 ms: 1.02x slower                                              |
| pickle_dict                | 34.6 us                                                | 35.3 us: 1.02x slower                                              |
| scimark_lu                 | 116 ms                                                 | 119 ms: 1.02x slower                                               |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                               |
| scimark_sor                | 121 ms                                                 | 124 ms: 1.02x slower                                               |
| 2to3                       | 264 ms                                                 | 271 ms: 1.02x slower                                               |
| chameleon                  | 6.70 ms                                                | 6.90 ms: 1.03x slower                                              |
| thrift                     | 784 us                                                 | 809 us: 1.03x slower                                               |
| dulwich_log                | 64.6 ms                                                | 66.8 ms: 1.03x slower                                              |
| html5lib                   | 64.8 ms                                                | 67.4 ms: 1.04x slower                                              |
| django_template            | 33.5 ms                                                | 35.0 ms: 1.04x slower                                              |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                              |
| docutils                   | 2.66 sec                                               | 2.81 sec: 1.06x slower                                             |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                              |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.33 ms: 1.06x slower                                              |
| genshi_text                | 22.5 ms                                                | 23.9 ms: 1.06x slower                                              |
| xml_etree_process          | 56.9 ms                                                | 60.4 ms: 1.06x slower                                              |
| regex_effbot               | 3.51 ms                                                | 3.73 ms: 1.06x slower                                              |
| spectral_norm              | 108 ms                                                 | 116 ms: 1.07x slower                                               |
| mypy2                      | 686 ms                                                 | 737 ms: 1.07x slower                                               |
| pyflate                    | 434 ms                                                 | 469 ms: 1.08x slower                                               |
| xml_etree_generate         | 81.1 ms                                                | 87.7 ms: 1.08x slower                                              |
| regex_dna                  | 205 ms                                                 | 225 ms: 1.10x slower                                               |
| pickle                     | 11.0 us                                                | 12.1 us: 1.10x slower                                              |
| scimark_fft                | 345 ms                                                 | 382 ms: 1.11x slower                                               |
| pickle_list                | 4.59 us                                                | 5.07 us: 1.11x slower                                              |
| unpickle                   | 13.8 us                                                | 15.6 us: 1.13x slower                                              |
| regex_v8                   | 22.9 ms                                                | 25.8 ms: 1.13x slower                                              |
| sqlite_synth               | 2.57 us                                                | 2.95 us: 1.15x slower                                              |
| python_startup_no_site     | 6.01 ms                                                | 7.09 ms: 1.18x slower                                              |
| async_generators           | 374 ms                                                 | 444 ms: 1.19x slower                                               |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                              |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                              |
| coverage                   | 78.8 ms                                                | 98.3 ms: 1.25x slower                                              |
| telco                      | 6.86 ms                                                | 8.78 ms: 1.28x slower                                              |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                       |

Benchmark hidden because not significant (6): nbody, scimark_monte_carlo, sqlglot_optimize, xml_etree_iterparse, float, dask
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 97.97% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x