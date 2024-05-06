# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_ghccc_cache_2
- machine: linux-x86_64
- commit hash: 7fbb9a2
- commit date: 2024-04-23
- overall geometric mean: 1.07x faster
- HPT reliability: 99.63%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 275 ms: 1.04x slower                                                         |
| chameleon      | 6.70 ms                                                | 6.88 ms: 1.03x slower                                                        |
| docutils       | 2.66 sec                                               | 2.89 sec: 1.09x slower                                                       |
| html5lib       | 64.8 ms                                                | 68.0 ms: 1.05x slower                                                        |
| tornado_http   | 98.1 ms                                                | 96.2 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 356 ms: 1.48x faster                                                         |
| async_tree_none_tg         | 491 ms                                                 | 339 ms: 1.45x faster                                                         |
| async_tree_memoization_tg  | 626 ms                                                 | 447 ms: 1.40x faster                                                         |
| async_tree_memoization     | 639 ms                                                 | 463 ms: 1.38x faster                                                         |
| async_tree_io_tg           | 1.29 sec                                               | 949 ms: 1.36x faster                                                         |
| async_tree_io              | 1.29 sec                                               | 944 ms: 1.36x faster                                                         |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 612 ms: 1.24x faster                                                         |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 620 ms: 1.21x faster                                                         |
| Geometric mean             | (ref)                                                  | 1.36x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 77.3 ms: 1.24x faster                                                        |
| float          | 78.9 ms                                                | 72.4 ms: 1.09x faster                                                        |
| pidigits       | 194 ms                                                 | 189 ms: 1.03x faster                                                         |
| Geometric mean | (ref)                                                  | 1.12x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 139 ms: 1.01x faster                                                         |
| regex_effbot   | 3.51 ms                                                | 3.71 ms: 1.06x slower                                                        |
| regex_dna      | 205 ms                                                 | 218 ms: 1.07x slower                                                         |
| regex_v8       | 22.9 ms                                                | 24.7 ms: 1.08x slower                                                        |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                        |
| tomli_loads          | 2.30 sec                                               | 1.92 sec: 1.20x faster                                                       |
| xml_etree_parse      | 164 ms                                                 | 150 ms: 1.09x faster                                                         |
| unpickle_pure_python | 242 us                                                 | 221 us: 1.09x faster                                                         |
| json_loads           | 29.2 us                                                | 27.5 us: 1.06x faster                                                        |
| pickle_pure_python   | 320 us                                                 | 304 us: 1.05x faster                                                         |
| xml_etree_iterparse  | 108 ms                                                 | 103 ms: 1.05x faster                                                         |
| unpickle_list        | 5.21 us                                                | 5.42 us: 1.04x slower                                                        |
| xml_etree_process    | 56.9 ms                                                | 59.2 ms: 1.04x slower                                                        |
| pickle_dict          | 34.6 us                                                | 36.8 us: 1.07x slower                                                        |
| xml_etree_generate   | 81.1 ms                                                | 86.7 ms: 1.07x slower                                                        |
| pickle               | 11.0 us                                                | 11.9 us: 1.08x slower                                                        |
| unpickle             | 13.8 us                                                | 15.0 us: 1.08x slower                                                        |
| pickle_list          | 4.59 us                                                | 5.38 us: 1.17x slower                                                        |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.63 ms: 1.27x slower                                                        |
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.29x slower                                                        |
| Geometric mean         | (ref)                                                  | 1.28x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.1 ms: 1.05x faster                                                        |
| django_template | 33.5 ms                                                | 35.6 ms: 1.06x slower                                                        |
| genshi_text     | 22.5 ms                                                | 24.1 ms: 1.07x slower                                                        |
| Geometric mean  | (ref)                                                  | 1.02x slower                                                                 |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-brandtbucher-justin_ghccc_cache_2-3.13.0a6+-7fbb9a2 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 111 us: 4.68x faster                                                         |
| generators                 | 74.9 ms                                                | 30.0 ms: 2.50x faster                                                        |
| asyncio_tcp                | 875 ms                                                 | 504 ms: 1.74x faster                                                         |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                       |
| async_tree_none            | 528 ms                                                 | 356 ms: 1.48x faster                                                         |
| async_tree_none_tg         | 491 ms                                                 | 339 ms: 1.45x faster                                                         |
| pylint                     | 476 ms                                                 | 331 ms: 1.44x faster                                                         |
| async_tree_memoization_tg  | 626 ms                                                 | 447 ms: 1.40x faster                                                         |
| comprehensions             | 23.6 us                                                | 17.1 us: 1.38x faster                                                        |
| async_tree_memoization     | 639 ms                                                 | 463 ms: 1.38x faster                                                         |
| async_tree_io_tg           | 1.29 sec                                               | 949 ms: 1.36x faster                                                         |
| async_tree_io              | 1.29 sec                                               | 944 ms: 1.36x faster                                                         |
| richards_super             | 61.9 ms                                                | 48.2 ms: 1.28x faster                                                        |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                        |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 612 ms: 1.24x faster                                                         |
| nbody                      | 96.0 ms                                                | 77.3 ms: 1.24x faster                                                        |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 620 ms: 1.21x faster                                                         |
| tomli_loads                | 2.30 sec                                               | 1.92 sec: 1.20x faster                                                       |
| coroutines                 | 27.0 ms                                                | 22.5 ms: 1.20x faster                                                        |
| richards                   | 49.8 ms                                                | 42.0 ms: 1.19x faster                                                        |
| chaos                      | 71.9 ms                                                | 60.8 ms: 1.18x faster                                                        |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.29 ms: 1.17x faster                                                        |
| fannkuch                   | 405 ms                                                 | 349 ms: 1.16x faster                                                         |
| scimark_fft                | 345 ms                                                 | 302 ms: 1.14x faster                                                         |
| crypto_pyaes               | 76.7 ms                                                | 68.3 ms: 1.12x faster                                                        |
| raytrace                   | 309 ms                                                 | 276 ms: 1.12x faster                                                         |
| scimark_monte_carlo        | 70.7 ms                                                | 63.3 ms: 1.12x faster                                                        |
| spectral_norm              | 108 ms                                                 | 97.7 ms: 1.11x faster                                                        |
| sqlglot_parse              | 1.43 ms                                                | 1.30 ms: 1.10x faster                                                        |
| logging_silent             | 111 ns                                                 | 102 ns: 1.09x faster                                                         |
| xml_etree_parse            | 164 ms                                                 | 150 ms: 1.09x faster                                                         |
| unpickle_pure_python       | 242 us                                                 | 221 us: 1.09x faster                                                         |
| float                      | 78.9 ms                                                | 72.4 ms: 1.09x faster                                                        |
| gc_traversal               | 4.01 ms                                                | 3.70 ms: 1.08x faster                                                        |
| sqlglot_transpile          | 1.75 ms                                                | 1.63 ms: 1.07x faster                                                        |
| deltablue                  | 3.92 ms                                                | 3.67 ms: 1.07x faster                                                        |
| logging_simple             | 6.22 us                                                | 5.84 us: 1.06x faster                                                        |
| json_loads                 | 29.2 us                                                | 27.5 us: 1.06x faster                                                        |
| mdp                        | 2.77 sec                                               | 2.63 sec: 1.05x faster                                                       |
| pickle_pure_python         | 320 us                                                 | 304 us: 1.05x faster                                                         |
| xml_etree_iterparse        | 108 ms                                                 | 103 ms: 1.05x faster                                                         |
| mako                       | 10.7 ms                                                | 10.1 ms: 1.05x faster                                                        |
| logging_format             | 6.81 us                                                | 6.49 us: 1.05x faster                                                        |
| hexiom                     | 6.89 ms                                                | 6.56 ms: 1.05x faster                                                        |
| djangocms                  | 33.5 us                                                | 32.0 us: 1.05x faster                                                        |
| deepcopy_memo              | 40.2 us                                                | 38.4 us: 1.04x faster                                                        |
| pprint_safe_repr           | 747 ms                                                 | 718 ms: 1.04x faster                                                         |
| json                       | 5.24 ms                                                | 5.05 ms: 1.04x faster                                                        |
| pathlib                    | 18.5 ms                                                | 17.8 ms: 1.04x faster                                                        |
| pprint_pformat             | 1.55 sec                                               | 1.50 sec: 1.04x faster                                                       |
| nqueens                    | 87.9 ms                                                | 85.1 ms: 1.03x faster                                                        |
| pidigits                   | 194 ms                                                 | 189 ms: 1.03x faster                                                         |
| sympy_str                  | 297 ms                                                 | 290 ms: 1.02x faster                                                         |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.02x faster                                                       |
| deepcopy                   | 365 us                                                 | 358 us: 1.02x faster                                                         |
| tornado_http               | 98.1 ms                                                | 96.2 ms: 1.02x faster                                                        |
| deepcopy_reduce            | 3.22 us                                                | 3.16 us: 1.02x faster                                                        |
| sympy_sum                  | 169 ms                                                 | 166 ms: 1.02x faster                                                         |
| regex_compile              | 141 ms                                                 | 139 ms: 1.01x faster                                                         |
| go                         | 149 ms                                                 | 147 ms: 1.01x faster                                                         |
| sqlglot_normalize          | 113 ms                                                 | 112 ms: 1.00x faster                                                         |
| sympy_integrate            | 21.5 ms                                                | 21.8 ms: 1.01x slower                                                        |
| sympy_expand               | 484 ms                                                 | 493 ms: 1.02x slower                                                         |
| sqlglot_optimize           | 55.3 ms                                                | 56.7 ms: 1.03x slower                                                        |
| dask                       | 365 ms                                                 | 375 ms: 1.03x slower                                                         |
| chameleon                  | 6.70 ms                                                | 6.88 ms: 1.03x slower                                                        |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                                         |
| bench_thread_pool          | 834 us                                                 | 862 us: 1.03x slower                                                         |
| pyflate                    | 434 ms                                                 | 450 ms: 1.04x slower                                                         |
| unpickle_list              | 5.21 us                                                | 5.42 us: 1.04x slower                                                        |
| xml_etree_process          | 56.9 ms                                                | 59.2 ms: 1.04x slower                                                        |
| 2to3                       | 264 ms                                                 | 275 ms: 1.04x slower                                                         |
| thrift                     | 784 us                                                 | 822 us: 1.05x slower                                                         |
| html5lib                   | 64.8 ms                                                | 68.0 ms: 1.05x slower                                                        |
| regex_effbot               | 3.51 ms                                                | 3.71 ms: 1.06x slower                                                        |
| django_template            | 33.5 ms                                                | 35.6 ms: 1.06x slower                                                        |
| scimark_lu                 | 116 ms                                                 | 124 ms: 1.06x slower                                                         |
| pickle_dict                | 34.6 us                                                | 36.8 us: 1.07x slower                                                        |
| regex_dna                  | 205 ms                                                 | 218 ms: 1.07x slower                                                         |
| xml_etree_generate         | 81.1 ms                                                | 86.7 ms: 1.07x slower                                                        |
| dulwich_log                | 64.6 ms                                                | 69.1 ms: 1.07x slower                                                        |
| genshi_text                | 22.5 ms                                                | 24.1 ms: 1.07x slower                                                        |
| aiohttp                    | 1.12 ms                                                | 1.20 ms: 1.08x slower                                                        |
| regex_v8                   | 22.9 ms                                                | 24.7 ms: 1.08x slower                                                        |
| gunicorn                   | 1.20 ms                                                | 1.30 ms: 1.08x slower                                                        |
| pickle                     | 11.0 us                                                | 11.9 us: 1.08x slower                                                        |
| unpickle                   | 13.8 us                                                | 15.0 us: 1.08x slower                                                        |
| docutils                   | 2.66 sec                                               | 2.89 sec: 1.09x slower                                                       |
| scimark_sor                | 121 ms                                                 | 132 ms: 1.09x slower                                                         |
| sqlite_synth               | 2.57 us                                                | 2.85 us: 1.11x slower                                                        |
| mypy2                      | 686 ms                                                 | 778 ms: 1.13x slower                                                         |
| pickle_list                | 4.59 us                                                | 5.38 us: 1.17x slower                                                        |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                                        |
| coverage                   | 78.8 ms                                                | 97.2 ms: 1.23x slower                                                        |
| telco                      | 6.86 ms                                                | 8.53 ms: 1.24x slower                                                        |
| async_generators           | 374 ms                                                 | 470 ms: 1.26x slower                                                         |
| python_startup_no_site     | 6.01 ms                                                | 7.63 ms: 1.27x slower                                                        |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.29x slower                                                        |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                                 |

Benchmark hidden because not significant (3): meteor_contest, bench_mp_pool, genshi_xml
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.63% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x