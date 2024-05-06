# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_ghccc_cache_3
- machine: linux-x86_64
- commit hash: a9d8d6e
- commit date: 2024-04-23
- overall geometric mean: 1.07x faster
- HPT reliability: 98.00%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 275 ms: 1.04x slower                                                         |
| chameleon      | 6.70 ms                                                | 6.97 ms: 1.04x slower                                                        |
| docutils       | 2.66 sec                                               | 2.90 sec: 1.09x slower                                                       |
| html5lib       | 64.8 ms                                                | 67.9 ms: 1.05x slower                                                        |
| tornado_http   | 98.1 ms                                                | 96.6 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 353 ms: 1.50x faster                                                         |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.47x faster                                                         |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                         |
| async_tree_io              | 1.29 sec                                               | 921 ms: 1.40x faster                                                         |
| async_tree_io_tg           | 1.29 sec                                               | 941 ms: 1.38x faster                                                         |
| async_tree_memoization     | 639 ms                                                 | 471 ms: 1.36x faster                                                         |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 603 ms: 1.26x faster                                                         |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 612 ms: 1.22x faster                                                         |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 76.0 ms: 1.26x faster                                                        |
| float          | 78.9 ms                                                | 73.1 ms: 1.08x faster                                                        |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                         |
| Geometric mean | (ref)                                                  | 1.12x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 141 ms: 1.00x faster                                                         |
| regex_v8       | 22.9 ms                                                | 24.5 ms: 1.07x slower                                                        |
| regex_effbot   | 3.51 ms                                                | 3.76 ms: 1.07x slower                                                        |
| regex_dna      | 205 ms                                                 | 221 ms: 1.08x slower                                                         |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.8 ms: 1.24x faster                                                        |
| tomli_loads          | 2.30 sec                                               | 1.90 sec: 1.21x faster                                                       |
| xml_etree_parse      | 164 ms                                                 | 149 ms: 1.10x faster                                                         |
| unpickle_pure_python | 242 us                                                 | 224 us: 1.08x faster                                                         |
| json_loads           | 29.2 us                                                | 27.7 us: 1.05x faster                                                        |
| xml_etree_iterparse  | 108 ms                                                 | 103 ms: 1.05x faster                                                         |
| pickle_pure_python   | 320 us                                                 | 306 us: 1.04x faster                                                         |
| pickle_dict          | 34.6 us                                                | 34.8 us: 1.01x slower                                                        |
| unpickle_list        | 5.21 us                                                | 5.31 us: 1.02x slower                                                        |
| xml_etree_process    | 56.9 ms                                                | 59.9 ms: 1.05x slower                                                        |
| xml_etree_generate   | 81.1 ms                                                | 87.1 ms: 1.07x slower                                                        |
| pickle               | 11.0 us                                                | 11.8 us: 1.08x slower                                                        |
| unpickle             | 13.8 us                                                | 15.3 us: 1.10x slower                                                        |
| pickle_list          | 4.59 us                                                | 5.18 us: 1.13x slower                                                        |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.65 ms: 1.27x slower                                                        |
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.29x slower                                                        |
| Geometric mean         | (ref)                                                  | 1.28x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.0 ms: 1.06x faster                                                        |
| django_template | 33.5 ms                                                | 35.9 ms: 1.07x slower                                                        |
| genshi_text     | 22.5 ms                                                | 24.6 ms: 1.09x slower                                                        |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                                 |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_3-3.13.0a6+-a9d8d6e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 115 us: 4.52x faster                                                         |
| generators                 | 74.9 ms                                                | 29.7 ms: 2.52x faster                                                        |
| asyncio_tcp                | 875 ms                                                 | 516 ms: 1.70x faster                                                         |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                       |
| async_tree_none            | 528 ms                                                 | 353 ms: 1.50x faster                                                         |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.47x faster                                                         |
| pylint                     | 476 ms                                                 | 334 ms: 1.42x faster                                                         |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                         |
| async_tree_io              | 1.29 sec                                               | 921 ms: 1.40x faster                                                         |
| async_tree_io_tg           | 1.29 sec                                               | 941 ms: 1.38x faster                                                         |
| comprehensions             | 23.6 us                                                | 17.4 us: 1.36x faster                                                        |
| async_tree_memoization     | 639 ms                                                 | 471 ms: 1.36x faster                                                         |
| nbody                      | 96.0 ms                                                | 76.0 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 603 ms: 1.26x faster                                                         |
| richards_super             | 61.9 ms                                                | 49.5 ms: 1.25x faster                                                        |
| json_dumps                 | 13.3 ms                                                | 10.8 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 612 ms: 1.22x faster                                                         |
| tomli_loads                | 2.30 sec                                               | 1.90 sec: 1.21x faster                                                       |
| coroutines                 | 27.0 ms                                                | 22.6 ms: 1.20x faster                                                        |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.22 ms: 1.19x faster                                                        |
| chaos                      | 71.9 ms                                                | 60.6 ms: 1.19x faster                                                        |
| fannkuch                   | 405 ms                                                 | 349 ms: 1.16x faster                                                         |
| richards                   | 49.8 ms                                                | 43.2 ms: 1.15x faster                                                        |
| scimark_fft                | 345 ms                                                 | 302 ms: 1.14x faster                                                         |
| crypto_pyaes               | 76.7 ms                                                | 67.9 ms: 1.13x faster                                                        |
| scimark_monte_carlo        | 70.7 ms                                                | 62.6 ms: 1.13x faster                                                        |
| raytrace                   | 309 ms                                                 | 277 ms: 1.11x faster                                                         |
| xml_etree_parse            | 164 ms                                                 | 149 ms: 1.10x faster                                                         |
| logging_silent             | 111 ns                                                 | 101 ns: 1.10x faster                                                         |
| spectral_norm              | 108 ms                                                 | 99.2 ms: 1.09x faster                                                        |
| sqlglot_parse              | 1.43 ms                                                | 1.32 ms: 1.08x faster                                                        |
| float                      | 78.9 ms                                                | 73.1 ms: 1.08x faster                                                        |
| unpickle_pure_python       | 242 us                                                 | 224 us: 1.08x faster                                                         |
| sqlglot_transpile          | 1.75 ms                                                | 1.64 ms: 1.07x faster                                                        |
| mako                       | 10.7 ms                                                | 10.0 ms: 1.06x faster                                                        |
| deltablue                  | 3.92 ms                                                | 3.72 ms: 1.05x faster                                                        |
| json_loads                 | 29.2 us                                                | 27.7 us: 1.05x faster                                                        |
| xml_etree_iterparse        | 108 ms                                                 | 103 ms: 1.05x faster                                                         |
| logging_simple             | 6.22 us                                                | 5.93 us: 1.05x faster                                                        |
| mdp                        | 2.77 sec                                               | 2.65 sec: 1.05x faster                                                       |
| pickle_pure_python         | 320 us                                                 | 306 us: 1.04x faster                                                         |
| pprint_pformat             | 1.55 sec                                               | 1.49 sec: 1.04x faster                                                       |
| hexiom                     | 6.89 ms                                                | 6.61 ms: 1.04x faster                                                        |
| pathlib                    | 18.5 ms                                                | 17.8 ms: 1.04x faster                                                        |
| logging_format             | 6.81 us                                                | 6.57 us: 1.04x faster                                                        |
| djangocms                  | 33.5 us                                                | 32.4 us: 1.04x faster                                                        |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                         |
| deepcopy_memo              | 40.2 us                                                | 39.5 us: 1.02x faster                                                        |
| pycparser                  | 1.19 sec                                               | 1.17 sec: 1.02x faster                                                       |
| tornado_http               | 98.1 ms                                                | 96.6 ms: 1.02x faster                                                        |
| deepcopy                   | 365 us                                                 | 361 us: 1.01x faster                                                         |
| sympy_str                  | 297 ms                                                 | 294 ms: 1.01x faster                                                         |
| sympy_sum                  | 169 ms                                                 | 167 ms: 1.01x faster                                                         |
| regex_compile              | 141 ms                                                 | 141 ms: 1.00x faster                                                         |
| pickle_dict                | 34.6 us                                                | 34.8 us: 1.01x slower                                                        |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                                         |
| gc_traversal               | 4.01 ms                                                | 4.06 ms: 1.01x slower                                                        |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                                         |
| unpickle_list              | 5.21 us                                                | 5.31 us: 1.02x slower                                                        |
| sympy_expand               | 484 ms                                                 | 495 ms: 1.02x slower                                                         |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.03x slower                                                         |
| sympy_integrate            | 21.5 ms                                                | 22.1 ms: 1.03x slower                                                        |
| dask                       | 365 ms                                                 | 376 ms: 1.03x slower                                                         |
| pyflate                    | 434 ms                                                 | 447 ms: 1.03x slower                                                         |
| sqlglot_optimize           | 55.3 ms                                                | 57.2 ms: 1.03x slower                                                        |
| chameleon                  | 6.70 ms                                                | 6.97 ms: 1.04x slower                                                        |
| 2to3                       | 264 ms                                                 | 275 ms: 1.04x slower                                                         |
| bench_thread_pool          | 834 us                                                 | 872 us: 1.04x slower                                                         |
| html5lib                   | 64.8 ms                                                | 67.9 ms: 1.05x slower                                                        |
| xml_etree_process          | 56.9 ms                                                | 59.9 ms: 1.05x slower                                                        |
| scimark_sor                | 121 ms                                                 | 128 ms: 1.05x slower                                                         |
| scimark_lu                 | 116 ms                                                 | 123 ms: 1.06x slower                                                         |
| thrift                     | 784 us                                                 | 836 us: 1.07x slower                                                         |
| django_template            | 33.5 ms                                                | 35.9 ms: 1.07x slower                                                        |
| regex_v8                   | 22.9 ms                                                | 24.5 ms: 1.07x slower                                                        |
| regex_effbot               | 3.51 ms                                                | 3.76 ms: 1.07x slower                                                        |
| xml_etree_generate         | 81.1 ms                                                | 87.1 ms: 1.07x slower                                                        |
| pickle                     | 11.0 us                                                | 11.8 us: 1.08x slower                                                        |
| regex_dna                  | 205 ms                                                 | 221 ms: 1.08x slower                                                         |
| dulwich_log                | 64.6 ms                                                | 70.1 ms: 1.09x slower                                                        |
| gunicorn                   | 1.20 ms                                                | 1.30 ms: 1.09x slower                                                        |
| docutils                   | 2.66 sec                                               | 2.90 sec: 1.09x slower                                                       |
| genshi_text                | 22.5 ms                                                | 24.6 ms: 1.09x slower                                                        |
| aiohttp                    | 1.12 ms                                                | 1.22 ms: 1.09x slower                                                        |
| unpickle                   | 13.8 us                                                | 15.3 us: 1.10x slower                                                        |
| sqlite_synth               | 2.57 us                                                | 2.84 us: 1.10x slower                                                        |
| pickle_list                | 4.59 us                                                | 5.18 us: 1.13x slower                                                        |
| mypy2                      | 686 ms                                                 | 786 ms: 1.15x slower                                                         |
| create_gc_cycles           | 1.43 ms                                                | 1.77 ms: 1.23x slower                                                        |
| telco                      | 6.86 ms                                                | 8.53 ms: 1.24x slower                                                        |
| coverage                   | 78.8 ms                                                | 98.4 ms: 1.25x slower                                                        |
| async_generators           | 374 ms                                                 | 468 ms: 1.25x slower                                                         |
| python_startup_no_site     | 6.01 ms                                                | 7.65 ms: 1.27x slower                                                        |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.29x slower                                                        |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                                 |

Benchmark hidden because not significant (7): pprint_safe_repr, json, nqueens, bench_mp_pool, go, deepcopy_reduce, genshi_xml
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 98.00% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x