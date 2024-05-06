# Results vs. 3.11.0

- fork: brandtbucher
- ref: justin_preserve_most
- machine: linux-x86_64
- commit hash: 377ec17
- commit date: 2024-04-18
- overall geometric mean: 1.06x faster
- HPT reliability: 75.15%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 276 ms: 1.04x slower                                                         |
| chameleon      | 6.70 ms                                                | 6.92 ms: 1.03x slower                                                        |
| docutils       | 2.66 sec                                               | 2.90 sec: 1.09x slower                                                       |
| html5lib       | 64.8 ms                                                | 67.2 ms: 1.04x slower                                                        |
| tornado_http   | 98.1 ms                                                | 96.0 ms: 1.02x faster                                                        |
| Geometric mean | (ref)                                                  | 1.04x slower                                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 354 ms: 1.49x faster                                                         |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.46x faster                                                         |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                         |
| async_tree_io              | 1.29 sec                                               | 923 ms: 1.39x faster                                                         |
| async_tree_memoization     | 639 ms                                                 | 465 ms: 1.37x faster                                                         |
| async_tree_io_tg           | 1.29 sec                                               | 945 ms: 1.37x faster                                                         |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                         |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 609 ms: 1.23x faster                                                         |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| float          | 78.9 ms                                                | 76.6 ms: 1.03x faster                                                        |
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                                         |
| nbody          | 96.0 ms                                                | 95.1 ms: 1.01x faster                                                        |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 142 ms: 1.01x slower                                                         |
| regex_effbot   | 3.51 ms                                                | 3.78 ms: 1.08x slower                                                        |
| regex_v8       | 22.9 ms                                                | 25.3 ms: 1.11x slower                                                        |
| regex_dna      | 205 ms                                                 | 228 ms: 1.12x slower                                                         |
| Geometric mean | (ref)                                                  | 1.08x slower                                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                        |
| tomli_loads          | 2.30 sec                                               | 1.99 sec: 1.16x faster                                                       |
| pickle_pure_python   | 320 us                                                 | 304 us: 1.05x faster                                                         |
| json_loads           | 29.2 us                                                | 27.8 us: 1.05x faster                                                        |
| unpickle_pure_python | 242 us                                                 | 231 us: 1.05x faster                                                         |
| unpickle_list        | 5.21 us                                                | 5.00 us: 1.04x faster                                                        |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.02x faster                                                         |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                         |
| pickle_dict          | 34.6 us                                                | 35.7 us: 1.03x slower                                                        |
| xml_etree_process    | 56.9 ms                                                | 60.0 ms: 1.05x slower                                                        |
| pickle               | 11.0 us                                                | 11.7 us: 1.06x slower                                                        |
| xml_etree_generate   | 81.1 ms                                                | 87.2 ms: 1.08x slower                                                        |
| unpickle             | 13.8 us                                                | 15.2 us: 1.10x slower                                                        |
| pickle_list          | 4.59 us                                                | 5.15 us: 1.12x slower                                                        |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.55 ms: 1.26x slower                                                        |
| python_startup         | 8.56 ms                                                | 10.9 ms: 1.28x slower                                                        |
| Geometric mean         | (ref)                                                  | 1.27x slower                                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.6 ms: 1.01x faster                                                        |
| genshi_text     | 22.5 ms                                                | 24.0 ms: 1.07x slower                                                        |
| django_template | 33.5 ms                                                | 35.9 ms: 1.07x slower                                                        |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                                 |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240418-linux-x86_64-brandtbucher-justin_preserve_most-3.13.0a6+-377ec17 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 114 us: 4.56x faster                                                         |
| generators                 | 74.9 ms                                                | 30.0 ms: 2.49x faster                                                        |
| asyncio_tcp                | 875 ms                                                 | 510 ms: 1.72x faster                                                         |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                       |
| async_tree_none            | 528 ms                                                 | 354 ms: 1.49x faster                                                         |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.46x faster                                                         |
| pylint                     | 476 ms                                                 | 334 ms: 1.43x faster                                                         |
| async_tree_memoization_tg  | 626 ms                                                 | 441 ms: 1.42x faster                                                         |
| async_tree_io              | 1.29 sec                                               | 923 ms: 1.39x faster                                                         |
| async_tree_memoization     | 639 ms                                                 | 465 ms: 1.37x faster                                                         |
| async_tree_io_tg           | 1.29 sec                                               | 945 ms: 1.37x faster                                                         |
| comprehensions             | 23.6 us                                                | 17.4 us: 1.35x faster                                                        |
| richards_super             | 61.9 ms                                                | 48.4 ms: 1.28x faster                                                        |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                         |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                        |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 609 ms: 1.23x faster                                                         |
| coroutines                 | 27.0 ms                                                | 22.8 ms: 1.19x faster                                                        |
| richards                   | 49.8 ms                                                | 42.1 ms: 1.18x faster                                                        |
| tomli_loads                | 2.30 sec                                               | 1.99 sec: 1.16x faster                                                       |
| chaos                      | 71.9 ms                                                | 62.3 ms: 1.15x faster                                                        |
| raytrace                   | 309 ms                                                 | 269 ms: 1.15x faster                                                         |
| logging_silent             | 111 ns                                                 | 102 ns: 1.09x faster                                                         |
| deltablue                  | 3.92 ms                                                | 3.62 ms: 1.08x faster                                                        |
| sqlglot_parse              | 1.43 ms                                                | 1.32 ms: 1.08x faster                                                        |
| sqlglot_transpile          | 1.75 ms                                                | 1.63 ms: 1.07x faster                                                        |
| logging_simple             | 6.22 us                                                | 5.81 us: 1.07x faster                                                        |
| logging_format             | 6.81 us                                                | 6.38 us: 1.07x faster                                                        |
| mdp                        | 2.77 sec                                               | 2.62 sec: 1.06x faster                                                       |
| pickle_pure_python         | 320 us                                                 | 304 us: 1.05x faster                                                         |
| json_loads                 | 29.2 us                                                | 27.8 us: 1.05x faster                                                        |
| deepcopy_memo              | 40.2 us                                                | 38.3 us: 1.05x faster                                                        |
| unpickle_pure_python       | 242 us                                                 | 231 us: 1.05x faster                                                         |
| unpickle_list              | 5.21 us                                                | 5.00 us: 1.04x faster                                                        |
| scimark_monte_carlo        | 70.7 ms                                                | 67.8 ms: 1.04x faster                                                        |
| pathlib                    | 18.5 ms                                                | 17.9 ms: 1.04x faster                                                        |
| djangocms                  | 33.5 us                                                | 32.4 us: 1.03x faster                                                        |
| crypto_pyaes               | 76.7 ms                                                | 74.1 ms: 1.03x faster                                                        |
| fannkuch                   | 405 ms                                                 | 392 ms: 1.03x faster                                                         |
| gc_traversal               | 4.01 ms                                                | 3.89 ms: 1.03x faster                                                        |
| float                      | 78.9 ms                                                | 76.6 ms: 1.03x faster                                                        |
| deepcopy                   | 365 us                                                 | 356 us: 1.03x faster                                                         |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.02x faster                                                         |
| deepcopy_reduce            | 3.22 us                                                | 3.14 us: 1.02x faster                                                        |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                                         |
| tornado_http               | 98.1 ms                                                | 96.0 ms: 1.02x faster                                                        |
| json                       | 5.24 ms                                                | 5.15 ms: 1.02x faster                                                        |
| nbody                      | 96.0 ms                                                | 95.1 ms: 1.01x faster                                                        |
| mako                       | 10.7 ms                                                | 10.6 ms: 1.01x faster                                                        |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                         |
| sympy_sum                  | 169 ms                                                 | 168 ms: 1.01x faster                                                         |
| hexiom                     | 6.89 ms                                                | 6.86 ms: 1.00x faster                                                        |
| regex_compile              | 141 ms                                                 | 142 ms: 1.01x slower                                                         |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                                         |
| nqueens                    | 87.9 ms                                                | 89.6 ms: 1.02x slower                                                        |
| pycparser                  | 1.19 sec                                               | 1.21 sec: 1.02x slower                                                       |
| sympy_integrate            | 21.5 ms                                                | 21.9 ms: 1.02x slower                                                        |
| scimark_fft                | 345 ms                                                 | 353 ms: 1.02x slower                                                         |
| bench_thread_pool          | 834 us                                                 | 855 us: 1.02x slower                                                         |
| meteor_contest             | 109 ms                                                 | 112 ms: 1.03x slower                                                         |
| dask                       | 365 ms                                                 | 375 ms: 1.03x slower                                                         |
| sympy_expand               | 484 ms                                                 | 498 ms: 1.03x slower                                                         |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                         |
| go                         | 149 ms                                                 | 153 ms: 1.03x slower                                                         |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.19 ms: 1.03x slower                                                        |
| pickle_dict                | 34.6 us                                                | 35.7 us: 1.03x slower                                                        |
| chameleon                  | 6.70 ms                                                | 6.92 ms: 1.03x slower                                                        |
| html5lib                   | 64.8 ms                                                | 67.2 ms: 1.04x slower                                                        |
| sqlglot_optimize           | 55.3 ms                                                | 57.6 ms: 1.04x slower                                                        |
| 2to3                       | 264 ms                                                 | 276 ms: 1.04x slower                                                         |
| thrift                     | 784 us                                                 | 826 us: 1.05x slower                                                         |
| xml_etree_process          | 56.9 ms                                                | 60.0 ms: 1.05x slower                                                        |
| pickle                     | 11.0 us                                                | 11.7 us: 1.06x slower                                                        |
| genshi_text                | 22.5 ms                                                | 24.0 ms: 1.07x slower                                                        |
| pyflate                    | 434 ms                                                 | 463 ms: 1.07x slower                                                         |
| django_template            | 33.5 ms                                                | 35.9 ms: 1.07x slower                                                        |
| dulwich_log                | 64.6 ms                                                | 69.3 ms: 1.07x slower                                                        |
| xml_etree_generate         | 81.1 ms                                                | 87.2 ms: 1.08x slower                                                        |
| regex_effbot               | 3.51 ms                                                | 3.78 ms: 1.08x slower                                                        |
| aiohttp                    | 1.12 ms                                                | 1.20 ms: 1.08x slower                                                        |
| gunicorn                   | 1.20 ms                                                | 1.30 ms: 1.08x slower                                                        |
| docutils                   | 2.66 sec                                               | 2.90 sec: 1.09x slower                                                       |
| scimark_sor                | 121 ms                                                 | 133 ms: 1.09x slower                                                         |
| unpickle                   | 13.8 us                                                | 15.2 us: 1.10x slower                                                        |
| spectral_norm              | 108 ms                                                 | 119 ms: 1.10x slower                                                         |
| regex_v8                   | 22.9 ms                                                | 25.3 ms: 1.11x slower                                                        |
| regex_dna                  | 205 ms                                                 | 228 ms: 1.12x slower                                                         |
| pickle_list                | 4.59 us                                                | 5.15 us: 1.12x slower                                                        |
| scimark_lu                 | 116 ms                                                 | 131 ms: 1.13x slower                                                         |
| sqlite_synth               | 2.57 us                                                | 2.91 us: 1.13x slower                                                        |
| mypy2                      | 686 ms                                                 | 781 ms: 1.14x slower                                                         |
| create_gc_cycles           | 1.43 ms                                                | 1.76 ms: 1.23x slower                                                        |
| async_generators           | 374 ms                                                 | 462 ms: 1.24x slower                                                         |
| coverage                   | 78.8 ms                                                | 98.4 ms: 1.25x slower                                                        |
| python_startup_no_site     | 6.01 ms                                                | 7.55 ms: 1.26x slower                                                        |
| telco                      | 6.86 ms                                                | 8.64 ms: 1.26x slower                                                        |
| python_startup             | 8.56 ms                                                | 10.9 ms: 1.28x slower                                                        |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                 |

Benchmark hidden because not significant (5): pprint_pformat, bench_mp_pool, sympy_str, pprint_safe_repr, genshi_xml
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 75.15% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x