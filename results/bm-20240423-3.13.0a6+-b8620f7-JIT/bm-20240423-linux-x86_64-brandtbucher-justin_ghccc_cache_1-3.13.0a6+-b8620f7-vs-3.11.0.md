# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_ghccc_cache_1
- machine: linux-x86_64
- commit hash: b8620f7
- commit date: 2024-04-23
- overall geometric mean: 1.07x faster
- HPT reliability: 99.14%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 277 ms: 1.05x slower                                                         |
| chameleon      | 6.70 ms                                                | 7.12 ms: 1.06x slower                                                        |
| docutils       | 2.66 sec                                               | 2.90 sec: 1.09x slower                                                       |
| html5lib       | 64.8 ms                                                | 68.8 ms: 1.06x slower                                                        |
| tornado_http   | 98.1 ms                                                | 95.7 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 359 ms: 1.47x faster                                                         |
| async_tree_none_tg         | 491 ms                                                 | 337 ms: 1.46x faster                                                         |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.42x faster                                                         |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                                         |
| async_tree_io_tg           | 1.29 sec                                               | 955 ms: 1.36x faster                                                         |
| async_tree_io              | 1.29 sec                                               | 949 ms: 1.36x faster                                                         |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 604 ms: 1.26x faster                                                         |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 611 ms: 1.23x faster                                                         |
| Geometric mean             | (ref)                                                  | 1.36x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 81.0 ms: 1.19x faster                                                        |
| float          | 78.9 ms                                                | 73.7 ms: 1.07x faster                                                        |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                         |
| Geometric mean | (ref)                                                  | 1.09x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 140 ms: 1.01x faster                                                         |
| regex_v8       | 22.9 ms                                                | 25.0 ms: 1.09x slower                                                        |
| regex_dna      | 205 ms                                                 | 229 ms: 1.12x slower                                                         |
| regex_effbot   | 3.51 ms                                                | 4.21 ms: 1.20x slower                                                        |
| Geometric mean | (ref)                                                  | 1.10x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                        |
| tomli_loads          | 2.30 sec                                               | 1.92 sec: 1.20x faster                                                       |
| xml_etree_parse      | 164 ms                                                 | 148 ms: 1.11x faster                                                         |
| unpickle_pure_python | 242 us                                                 | 223 us: 1.08x faster                                                         |
| json_loads           | 29.2 us                                                | 27.3 us: 1.07x faster                                                        |
| xml_etree_iterparse  | 108 ms                                                 | 101 ms: 1.07x faster                                                         |
| pickle_pure_python   | 320 us                                                 | 309 us: 1.04x faster                                                         |
| pickle_dict          | 34.6 us                                                | 35.6 us: 1.03x slower                                                        |
| xml_etree_process    | 56.9 ms                                                | 60.6 ms: 1.07x slower                                                        |
| pickle               | 11.0 us                                                | 11.8 us: 1.07x slower                                                        |
| xml_etree_generate   | 81.1 ms                                                | 87.6 ms: 1.08x slower                                                        |
| pickle_list          | 4.59 us                                                | 5.06 us: 1.10x slower                                                        |
| unpickle             | 13.8 us                                                | 15.3 us: 1.10x slower                                                        |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                 |

Benchmark hidden because not significant (1): unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.68 ms: 1.28x slower                                                        |
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                        |
| Geometric mean         | (ref)                                                  | 1.29x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 9.91 ms: 1.08x faster                                                        |
| genshi_xml      | 53.4 ms                                                | 55.9 ms: 1.05x slower                                                        |
| django_template | 33.5 ms                                                | 35.8 ms: 1.07x slower                                                        |
| genshi_text     | 22.5 ms                                                | 24.1 ms: 1.07x slower                                                        |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_1-3.13.0a6+-b8620f7 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 115 us: 4.52x faster                                                         |
| generators                 | 74.9 ms                                                | 29.9 ms: 2.50x faster                                                        |
| asyncio_tcp                | 875 ms                                                 | 515 ms: 1.70x faster                                                         |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                       |
| async_tree_none            | 528 ms                                                 | 359 ms: 1.47x faster                                                         |
| async_tree_none_tg         | 491 ms                                                 | 337 ms: 1.46x faster                                                         |
| pylint                     | 476 ms                                                 | 333 ms: 1.43x faster                                                         |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.42x faster                                                         |
| comprehensions             | 23.6 us                                                | 16.9 us: 1.39x faster                                                        |
| async_tree_memoization     | 639 ms                                                 | 462 ms: 1.38x faster                                                         |
| async_tree_io_tg           | 1.29 sec                                               | 955 ms: 1.36x faster                                                         |
| async_tree_io              | 1.29 sec                                               | 949 ms: 1.36x faster                                                         |
| richards_super             | 61.9 ms                                                | 49.1 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 604 ms: 1.26x faster                                                         |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 611 ms: 1.23x faster                                                         |
| tomli_loads                | 2.30 sec                                               | 1.92 sec: 1.20x faster                                                       |
| coroutines                 | 27.0 ms                                                | 22.6 ms: 1.20x faster                                                        |
| nbody                      | 96.0 ms                                                | 81.0 ms: 1.19x faster                                                        |
| richards                   | 49.8 ms                                                | 42.4 ms: 1.18x faster                                                        |
| chaos                      | 71.9 ms                                                | 61.8 ms: 1.16x faster                                                        |
| fannkuch                   | 405 ms                                                 | 356 ms: 1.14x faster                                                         |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.42 ms: 1.14x faster                                                        |
| raytrace                   | 309 ms                                                 | 274 ms: 1.13x faster                                                         |
| logging_silent             | 111 ns                                                 | 99.0 ns: 1.12x faster                                                        |
| scimark_fft                | 345 ms                                                 | 310 ms: 1.11x faster                                                         |
| crypto_pyaes               | 76.7 ms                                                | 68.9 ms: 1.11x faster                                                        |
| scimark_monte_carlo        | 70.7 ms                                                | 63.6 ms: 1.11x faster                                                        |
| xml_etree_parse            | 164 ms                                                 | 148 ms: 1.11x faster                                                         |
| spectral_norm              | 108 ms                                                 | 98.5 ms: 1.10x faster                                                        |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.09x faster                                                        |
| unpickle_pure_python       | 242 us                                                 | 223 us: 1.08x faster                                                         |
| logging_simple             | 6.22 us                                                | 5.76 us: 1.08x faster                                                        |
| deltablue                  | 3.92 ms                                                | 3.64 ms: 1.08x faster                                                        |
| mako                       | 10.7 ms                                                | 9.91 ms: 1.08x faster                                                        |
| gc_traversal               | 4.01 ms                                                | 3.74 ms: 1.07x faster                                                        |
| sqlglot_transpile          | 1.75 ms                                                | 1.63 ms: 1.07x faster                                                        |
| float                      | 78.9 ms                                                | 73.7 ms: 1.07x faster                                                        |
| json_loads                 | 29.2 us                                                | 27.3 us: 1.07x faster                                                        |
| xml_etree_iterparse        | 108 ms                                                 | 101 ms: 1.07x faster                                                         |
| logging_format             | 6.81 us                                                | 6.41 us: 1.06x faster                                                        |
| hexiom                     | 6.89 ms                                                | 6.54 ms: 1.05x faster                                                        |
| pprint_pformat             | 1.55 sec                                               | 1.48 sec: 1.05x faster                                                       |
| mdp                        | 2.77 sec                                               | 2.64 sec: 1.05x faster                                                       |
| pprint_safe_repr           | 747 ms                                                 | 717 ms: 1.04x faster                                                         |
| pathlib                    | 18.5 ms                                                | 17.8 ms: 1.04x faster                                                        |
| djangocms                  | 33.5 us                                                | 32.3 us: 1.04x faster                                                        |
| pickle_pure_python         | 320 us                                                 | 309 us: 1.04x faster                                                         |
| json                       | 5.24 ms                                                | 5.08 ms: 1.03x faster                                                        |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                         |
| deepcopy_memo              | 40.2 us                                                | 39.1 us: 1.03x faster                                                        |
| tornado_http               | 98.1 ms                                                | 95.7 ms: 1.02x faster                                                        |
| pycparser                  | 1.19 sec                                               | 1.17 sec: 1.01x faster                                                       |
| sympy_str                  | 297 ms                                                 | 293 ms: 1.01x faster                                                         |
| nqueens                    | 87.9 ms                                                | 86.7 ms: 1.01x faster                                                        |
| regex_compile              | 141 ms                                                 | 140 ms: 1.01x faster                                                         |
| sympy_sum                  | 169 ms                                                 | 167 ms: 1.01x faster                                                         |
| meteor_contest             | 109 ms                                                 | 108 ms: 1.01x faster                                                         |
| go                         | 149 ms                                                 | 148 ms: 1.01x faster                                                         |
| deepcopy                   | 365 us                                                 | 364 us: 1.00x faster                                                         |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                                         |
| sympy_integrate            | 21.5 ms                                                | 21.9 ms: 1.02x slower                                                        |
| sympy_expand               | 484 ms                                                 | 494 ms: 1.02x slower                                                         |
| pyflate                    | 434 ms                                                 | 443 ms: 1.02x slower                                                         |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                                         |
| dask                       | 365 ms                                                 | 374 ms: 1.02x slower                                                         |
| pickle_dict                | 34.6 us                                                | 35.6 us: 1.03x slower                                                        |
| sqlglot_optimize           | 55.3 ms                                                | 57.1 ms: 1.03x slower                                                        |
| bench_thread_pool          | 834 us                                                 | 864 us: 1.04x slower                                                         |
| genshi_xml                 | 53.4 ms                                                | 55.9 ms: 1.05x slower                                                        |
| 2to3                       | 264 ms                                                 | 277 ms: 1.05x slower                                                         |
| thrift                     | 784 us                                                 | 827 us: 1.06x slower                                                         |
| scimark_sor                | 121 ms                                                 | 129 ms: 1.06x slower                                                         |
| html5lib                   | 64.8 ms                                                | 68.8 ms: 1.06x slower                                                        |
| chameleon                  | 6.70 ms                                                | 7.12 ms: 1.06x slower                                                        |
| xml_etree_process          | 56.9 ms                                                | 60.6 ms: 1.07x slower                                                        |
| django_template            | 33.5 ms                                                | 35.8 ms: 1.07x slower                                                        |
| dulwich_log                | 64.6 ms                                                | 69.0 ms: 1.07x slower                                                        |
| pickle                     | 11.0 us                                                | 11.8 us: 1.07x slower                                                        |
| genshi_text                | 22.5 ms                                                | 24.1 ms: 1.07x slower                                                        |
| scimark_lu                 | 116 ms                                                 | 125 ms: 1.08x slower                                                         |
| xml_etree_generate         | 81.1 ms                                                | 87.6 ms: 1.08x slower                                                        |
| gunicorn                   | 1.20 ms                                                | 1.30 ms: 1.09x slower                                                        |
| aiohttp                    | 1.12 ms                                                | 1.21 ms: 1.09x slower                                                        |
| docutils                   | 2.66 sec                                               | 2.90 sec: 1.09x slower                                                       |
| regex_v8                   | 22.9 ms                                                | 25.0 ms: 1.09x slower                                                        |
| pickle_list                | 4.59 us                                                | 5.06 us: 1.10x slower                                                        |
| unpickle                   | 13.8 us                                                | 15.3 us: 1.10x slower                                                        |
| sqlite_synth               | 2.57 us                                                | 2.85 us: 1.11x slower                                                        |
| regex_dna                  | 205 ms                                                 | 229 ms: 1.12x slower                                                         |
| mypy2                      | 686 ms                                                 | 785 ms: 1.14x slower                                                         |
| regex_effbot               | 3.51 ms                                                | 4.21 ms: 1.20x slower                                                        |
| create_gc_cycles           | 1.43 ms                                                | 1.77 ms: 1.24x slower                                                        |
| coverage                   | 78.8 ms                                                | 98.1 ms: 1.25x slower                                                        |
| telco                      | 6.86 ms                                                | 8.56 ms: 1.25x slower                                                        |
| async_generators           | 374 ms                                                 | 467 ms: 1.25x slower                                                         |
| python_startup_no_site     | 6.01 ms                                                | 7.68 ms: 1.28x slower                                                        |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.30x slower                                                        |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                                 |

Benchmark hidden because not significant (3): unpickle_list, deepcopy_reduce, bench_mp_pool
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.14% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.12x