# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_ghccc_cache_4
- machine: linux-x86_64
- commit hash: b309fd7
- commit date: 2024-04-24
- overall geometric mean: 1.03x faster
- HPT reliability: 72.39%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 290 ms: 1.10x slower                                                         |
| chameleon      | 6.70 ms                                                | 7.24 ms: 1.08x slower                                                        |
| docutils       | 2.66 sec                                               | 3.00 sec: 1.13x slower                                                       |
| html5lib       | 64.8 ms                                                | 70.0 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                  | 1.08x slower                                                                 |

Benchmark hidden because not significant (1): tornado_http

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 367 ms: 1.44x faster                                                         |
| async_tree_none_tg         | 491 ms                                                 | 344 ms: 1.43x faster                                                         |
| async_tree_memoization_tg  | 626 ms                                                 | 450 ms: 1.39x faster                                                         |
| async_tree_io              | 1.29 sec                                               | 940 ms: 1.37x faster                                                         |
| async_tree_io_tg           | 1.29 sec                                               | 950 ms: 1.36x faster                                                         |
| async_tree_memoization     | 639 ms                                                 | 478 ms: 1.34x faster                                                         |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 612 ms: 1.24x faster                                                         |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 624 ms: 1.20x faster                                                         |
| Geometric mean             | (ref)                                                  | 1.34x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 83.1 ms: 1.15x faster                                                        |
| float          | 78.9 ms                                                | 75.3 ms: 1.05x faster                                                        |
| pidigits       | 194 ms                                                 | 210 ms: 1.08x slower                                                         |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_v8       | 22.9 ms                                                | 24.5 ms: 1.07x slower                                                        |
| regex_dna      | 205 ms                                                 | 225 ms: 1.10x slower                                                         |
| regex_effbot   | 3.51 ms                                                | 4.23 ms: 1.21x slower                                                        |
| regex_compile  | 141 ms                                                 | 171 ms: 1.21x slower                                                         |
| Geometric mean | (ref)                                                  | 1.14x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                        |
| xml_etree_parse      | 164 ms                                                 | 148 ms: 1.11x faster                                                         |
| tomli_loads          | 2.30 sec                                               | 2.15 sec: 1.07x faster                                                       |
| json_loads           | 29.2 us                                                | 27.4 us: 1.07x faster                                                        |
| xml_etree_iterparse  | 108 ms                                                 | 104 ms: 1.04x faster                                                         |
| pickle_pure_python   | 320 us                                                 | 309 us: 1.03x faster                                                         |
| unpickle_pure_python | 242 us                                                 | 240 us: 1.01x faster                                                         |
| pickle_dict          | 34.6 us                                                | 34.9 us: 1.01x slower                                                        |
| unpickle_list        | 5.21 us                                                | 5.34 us: 1.02x slower                                                        |
| xml_etree_process    | 56.9 ms                                                | 60.9 ms: 1.07x slower                                                        |
| xml_etree_generate   | 81.1 ms                                                | 88.1 ms: 1.09x slower                                                        |
| pickle               | 11.0 us                                                | 12.0 us: 1.10x slower                                                        |
| unpickle             | 13.8 us                                                | 15.2 us: 1.10x slower                                                        |
| pickle_list          | 4.59 us                                                | 5.08 us: 1.11x slower                                                        |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.71 ms: 1.28x slower                                                        |
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                        |
| Geometric mean         | (ref)                                                  | 1.29x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.7 ms: 1.00x slower                                                        |
| genshi_text     | 22.5 ms                                                | 25.2 ms: 1.12x slower                                                        |
| django_template | 33.5 ms                                                | 37.5 ms: 1.12x slower                                                        |
| genshi_xml      | 53.4 ms                                                | 61.1 ms: 1.14x slower                                                        |
| Geometric mean  | (ref)                                                  | 1.09x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240424-linux-x86_64-brandtbucher-justin_ghccc_cache_4-3.13.0a6+-b309fd7 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 116 us: 4.49x faster                                                         |
| generators                 | 74.9 ms                                                | 30.0 ms: 2.49x faster                                                        |
| asyncio_tcp                | 875 ms                                                 | 517 ms: 1.69x faster                                                         |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.87 sec: 1.67x faster                                                       |
| async_tree_none            | 528 ms                                                 | 367 ms: 1.44x faster                                                         |
| async_tree_none_tg         | 491 ms                                                 | 344 ms: 1.43x faster                                                         |
| pylint                     | 476 ms                                                 | 341 ms: 1.40x faster                                                         |
| async_tree_memoization_tg  | 626 ms                                                 | 450 ms: 1.39x faster                                                         |
| async_tree_io              | 1.29 sec                                               | 940 ms: 1.37x faster                                                         |
| async_tree_io_tg           | 1.29 sec                                               | 950 ms: 1.36x faster                                                         |
| async_tree_memoization     | 639 ms                                                 | 478 ms: 1.34x faster                                                         |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                        |
| comprehensions             | 23.6 us                                                | 19.0 us: 1.24x faster                                                        |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 612 ms: 1.24x faster                                                         |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 624 ms: 1.20x faster                                                         |
| coroutines                 | 27.0 ms                                                | 22.9 ms: 1.18x faster                                                        |
| nbody                      | 96.0 ms                                                | 83.1 ms: 1.15x faster                                                        |
| richards_super             | 61.9 ms                                                | 54.3 ms: 1.14x faster                                                        |
| xml_etree_parse            | 164 ms                                                 | 148 ms: 1.11x faster                                                         |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.55 ms: 1.10x faster                                                        |
| logging_silent             | 111 ns                                                 | 102 ns: 1.09x faster                                                         |
| tomli_loads                | 2.30 sec                                               | 2.15 sec: 1.07x faster                                                       |
| raytrace                   | 309 ms                                                 | 288 ms: 1.07x faster                                                         |
| chaos                      | 71.9 ms                                                | 67.4 ms: 1.07x faster                                                        |
| json_loads                 | 29.2 us                                                | 27.4 us: 1.07x faster                                                        |
| float                      | 78.9 ms                                                | 75.3 ms: 1.05x faster                                                        |
| xml_etree_iterparse        | 108 ms                                                 | 104 ms: 1.04x faster                                                         |
| richards                   | 49.8 ms                                                | 47.7 ms: 1.04x faster                                                        |
| crypto_pyaes               | 76.7 ms                                                | 73.7 ms: 1.04x faster                                                        |
| deltablue                  | 3.92 ms                                                | 3.77 ms: 1.04x faster                                                        |
| scimark_fft                | 345 ms                                                 | 333 ms: 1.04x faster                                                         |
| fannkuch                   | 405 ms                                                 | 391 ms: 1.04x faster                                                         |
| mdp                        | 2.77 sec                                               | 2.68 sec: 1.04x faster                                                       |
| sqlglot_parse              | 1.43 ms                                                | 1.38 ms: 1.04x faster                                                        |
| pickle_pure_python         | 320 us                                                 | 309 us: 1.03x faster                                                         |
| djangocms                  | 33.5 us                                                | 32.5 us: 1.03x faster                                                        |
| sqlglot_transpile          | 1.75 ms                                                | 1.70 ms: 1.03x faster                                                        |
| pathlib                    | 18.5 ms                                                | 18.0 ms: 1.03x faster                                                        |
| json                       | 5.24 ms                                                | 5.13 ms: 1.02x faster                                                        |
| gc_traversal               | 4.01 ms                                                | 3.93 ms: 1.02x faster                                                        |
| logging_simple             | 6.22 us                                                | 6.11 us: 1.02x faster                                                        |
| logging_format             | 6.81 us                                                | 6.70 us: 1.02x faster                                                        |
| unpickle_pure_python       | 242 us                                                 | 240 us: 1.01x faster                                                         |
| mako                       | 10.7 ms                                                | 10.7 ms: 1.00x slower                                                        |
| deepcopy_reduce            | 3.22 us                                                | 3.23 us: 1.01x slower                                                        |
| pickle_dict                | 34.6 us                                                | 34.9 us: 1.01x slower                                                        |
| deepcopy                   | 365 us                                                 | 372 us: 1.02x slower                                                         |
| pycparser                  | 1.19 sec                                               | 1.21 sec: 1.02x slower                                                       |
| meteor_contest             | 109 ms                                                 | 112 ms: 1.02x slower                                                         |
| unpickle_list              | 5.21 us                                                | 5.34 us: 1.02x slower                                                        |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.03x slower                                                         |
| sympy_sum                  | 169 ms                                                 | 174 ms: 1.03x slower                                                         |
| sqlglot_normalize          | 113 ms                                                 | 116 ms: 1.03x slower                                                         |
| go                         | 149 ms                                                 | 155 ms: 1.04x slower                                                         |
| dask                       | 365 ms                                                 | 380 ms: 1.04x slower                                                         |
| sympy_str                  | 297 ms                                                 | 310 ms: 1.04x slower                                                         |
| bench_thread_pool          | 834 us                                                 | 874 us: 1.05x slower                                                         |
| scimark_monte_carlo        | 70.7 ms                                                | 74.6 ms: 1.05x slower                                                        |
| thrift                     | 784 us                                                 | 829 us: 1.06x slower                                                         |
| sympy_integrate            | 21.5 ms                                                | 22.8 ms: 1.06x slower                                                        |
| xml_etree_process          | 56.9 ms                                                | 60.9 ms: 1.07x slower                                                        |
| regex_v8                   | 22.9 ms                                                | 24.5 ms: 1.07x slower                                                        |
| sqlglot_optimize           | 55.3 ms                                                | 59.5 ms: 1.08x slower                                                        |
| html5lib                   | 64.8 ms                                                | 70.0 ms: 1.08x slower                                                        |
| sympy_expand               | 484 ms                                                 | 524 ms: 1.08x slower                                                         |
| chameleon                  | 6.70 ms                                                | 7.24 ms: 1.08x slower                                                        |
| pidigits                   | 194 ms                                                 | 210 ms: 1.08x slower                                                         |
| nqueens                    | 87.9 ms                                                | 95.5 ms: 1.09x slower                                                        |
| xml_etree_generate         | 81.1 ms                                                | 88.1 ms: 1.09x slower                                                        |
| pickle                     | 11.0 us                                                | 12.0 us: 1.10x slower                                                        |
| 2to3                       | 264 ms                                                 | 290 ms: 1.10x slower                                                         |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.10x slower                                                        |
| scimark_sor                | 121 ms                                                 | 133 ms: 1.10x slower                                                         |
| regex_dna                  | 205 ms                                                 | 225 ms: 1.10x slower                                                         |
| gunicorn                   | 1.20 ms                                                | 1.32 ms: 1.10x slower                                                        |
| aiohttp                    | 1.12 ms                                                | 1.23 ms: 1.10x slower                                                        |
| pickle_list                | 4.59 us                                                | 5.08 us: 1.11x slower                                                        |
| scimark_lu                 | 116 ms                                                 | 130 ms: 1.11x slower                                                         |
| dulwich_log                | 64.6 ms                                                | 72.2 ms: 1.12x slower                                                        |
| genshi_text                | 22.5 ms                                                | 25.2 ms: 1.12x slower                                                        |
| django_template            | 33.5 ms                                                | 37.5 ms: 1.12x slower                                                        |
| sqlite_synth               | 2.57 us                                                | 2.89 us: 1.13x slower                                                        |
| docutils                   | 2.66 sec                                               | 3.00 sec: 1.13x slower                                                       |
| genshi_xml                 | 53.4 ms                                                | 61.1 ms: 1.14x slower                                                        |
| mypy2                      | 686 ms                                                 | 809 ms: 1.18x slower                                                         |
| pyflate                    | 434 ms                                                 | 514 ms: 1.19x slower                                                         |
| hexiom                     | 6.89 ms                                                | 8.20 ms: 1.19x slower                                                        |
| pprint_safe_repr           | 747 ms                                                 | 897 ms: 1.20x slower                                                         |
| regex_effbot               | 3.51 ms                                                | 4.23 ms: 1.21x slower                                                        |
| regex_compile              | 141 ms                                                 | 171 ms: 1.21x slower                                                         |
| pprint_pformat             | 1.55 sec                                               | 1.94 sec: 1.25x slower                                                       |
| create_gc_cycles           | 1.43 ms                                                | 1.79 ms: 1.25x slower                                                        |
| coverage                   | 78.8 ms                                                | 98.3 ms: 1.25x slower                                                        |
| async_generators           | 374 ms                                                 | 471 ms: 1.26x slower                                                         |
| python_startup_no_site     | 6.01 ms                                                | 7.71 ms: 1.28x slower                                                        |
| telco                      | 6.86 ms                                                | 8.84 ms: 1.29x slower                                                        |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                        |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                                 |

Benchmark hidden because not significant (4): deepcopy_memo, tornado_http, bench_mp_pool, spectral_norm
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 72.39% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.16x