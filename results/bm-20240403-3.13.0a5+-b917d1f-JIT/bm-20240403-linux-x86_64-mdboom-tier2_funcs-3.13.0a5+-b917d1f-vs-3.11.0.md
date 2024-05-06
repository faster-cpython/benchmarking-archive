# Results vs. 3.11.0

- fork: mdboom
- ref: tier2_funcs
- machine: linux-x86_64
- commit hash: b917d1f
- commit date: 2024-04-03
- overall geometric mean: 1.04x faster
- HPT reliability: 69.73%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 278 ms: 1.05x slower                                          |
| chameleon      | 6.70 ms                                                | 6.92 ms: 1.03x slower                                         |
| docutils       | 2.66 sec                                               | 2.89 sec: 1.08x slower                                        |
| html5lib       | 64.8 ms                                                | 68.0 ms: 1.05x slower                                         |
| tornado_http   | 98.1 ms                                                | 97.0 ms: 1.01x faster                                         |
| Geometric mean | (ref)                                                  | 1.04x slower                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 342 ms: 1.43x faster                                          |
| async_tree_memoization     | 639 ms                                                 | 457 ms: 1.40x faster                                          |
| async_tree_io_tg           | 1.29 sec                                               | 930 ms: 1.39x faster                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 451 ms: 1.39x faster                                          |
| async_tree_none            | 528 ms                                                 | 390 ms: 1.35x faster                                          |
| async_tree_io              | 1.29 sec                                               | 951 ms: 1.35x faster                                          |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 584 ms: 1.30x faster                                          |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 600 ms: 1.25x faster                                          |
| Geometric mean             | (ref)                                                  | 1.36x faster                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 92.8 ms: 1.03x faster                                         |
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                          |
| float          | 78.9 ms                                                | 77.6 ms: 1.02x faster                                         |
| Geometric mean | (ref)                                                  | 1.02x faster                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 147 ms: 1.04x slower                                          |
| regex_effbot   | 3.51 ms                                                | 3.75 ms: 1.07x slower                                         |
| regex_dna      | 205 ms                                                 | 229 ms: 1.12x slower                                          |
| regex_v8       | 22.9 ms                                                | 25.9 ms: 1.13x slower                                         |
| Geometric mean | (ref)                                                  | 1.09x slower                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                         |
| tomli_loads          | 2.30 sec                                               | 2.08 sec: 1.11x faster                                        |
| pickle_pure_python   | 320 us                                                 | 307 us: 1.04x faster                                          |
| json_loads           | 29.2 us                                                | 28.4 us: 1.03x faster                                         |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.03x faster                                          |
| unpickle_list        | 5.21 us                                                | 5.14 us: 1.01x faster                                         |
| unpickle_pure_python | 242 us                                                 | 239 us: 1.01x faster                                          |
| pickle_dict          | 34.6 us                                                | 34.5 us: 1.00x faster                                         |
| xml_etree_process    | 56.9 ms                                                | 59.9 ms: 1.05x slower                                         |
| pickle               | 11.0 us                                                | 11.8 us: 1.07x slower                                         |
| xml_etree_generate   | 81.1 ms                                                | 87.2 ms: 1.08x slower                                         |
| pickle_list          | 4.59 us                                                | 5.00 us: 1.09x slower                                         |
| unpickle             | 13.8 us                                                | 16.0 us: 1.15x slower                                         |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                  |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.30x slower                                         |
| python_startup_no_site | 6.01 ms                                                | 9.57 ms: 1.59x slower                                         |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 10.7 ms: 1.01x slower                                         |
| genshi_xml      | 53.4 ms                                                | 55.3 ms: 1.03x slower                                         |
| genshi_text     | 22.5 ms                                                | 24.3 ms: 1.08x slower                                         |
| django_template | 33.5 ms                                                | 36.3 ms: 1.08x slower                                         |
| Geometric mean  | (ref)                                                  | 1.05x slower                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-mdboom-tier2_funcs-3.13.0a5+-b917d1f |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 110 us: 4.71x faster                                          |
| generators                 | 74.9 ms                                                | 30.1 ms: 2.49x faster                                         |
| asyncio_tcp                | 875 ms                                                 | 508 ms: 1.72x faster                                          |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.68x faster                                        |
| async_tree_none_tg         | 491 ms                                                 | 342 ms: 1.43x faster                                          |
| pylint                     | 476 ms                                                 | 336 ms: 1.42x faster                                          |
| async_tree_memoization     | 639 ms                                                 | 457 ms: 1.40x faster                                          |
| async_tree_io_tg           | 1.29 sec                                               | 930 ms: 1.39x faster                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 451 ms: 1.39x faster                                          |
| async_tree_none            | 528 ms                                                 | 390 ms: 1.35x faster                                          |
| async_tree_io              | 1.29 sec                                               | 951 ms: 1.35x faster                                          |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 584 ms: 1.30x faster                                          |
| comprehensions             | 23.6 us                                                | 18.5 us: 1.28x faster                                         |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                         |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 600 ms: 1.25x faster                                          |
| coroutines                 | 27.0 ms                                                | 22.4 ms: 1.21x faster                                         |
| richards_super             | 61.9 ms                                                | 53.6 ms: 1.15x faster                                         |
| chaos                      | 71.9 ms                                                | 63.0 ms: 1.14x faster                                         |
| deltablue                  | 3.92 ms                                                | 3.47 ms: 1.13x faster                                         |
| tomli_loads                | 2.30 sec                                               | 2.08 sec: 1.11x faster                                        |
| djangocms                  | 33.5 us                                                | 30.8 us: 1.09x faster                                         |
| sqlglot_parse              | 1.43 ms                                                | 1.34 ms: 1.07x faster                                         |
| logging_silent             | 111 ns                                                 | 104 ns: 1.07x faster                                          |
| richards                   | 49.8 ms                                                | 46.9 ms: 1.06x faster                                         |
| sqlglot_transpile          | 1.75 ms                                                | 1.66 ms: 1.06x faster                                         |
| raytrace                   | 309 ms                                                 | 294 ms: 1.05x faster                                          |
| mdp                        | 2.77 sec                                               | 2.66 sec: 1.04x faster                                        |
| logging_simple             | 6.22 us                                                | 5.97 us: 1.04x faster                                         |
| pickle_pure_python         | 320 us                                                 | 307 us: 1.04x faster                                          |
| nbody                      | 96.0 ms                                                | 92.8 ms: 1.03x faster                                         |
| crypto_pyaes               | 76.7 ms                                                | 74.5 ms: 1.03x faster                                         |
| json_loads                 | 29.2 us                                                | 28.4 us: 1.03x faster                                         |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.03x faster                                          |
| deepcopy_memo              | 40.2 us                                                | 39.1 us: 1.03x faster                                         |
| sympy_str                  | 297 ms                                                 | 290 ms: 1.02x faster                                          |
| fannkuch                   | 405 ms                                                 | 396 ms: 1.02x faster                                          |
| sympy_sum                  | 169 ms                                                 | 165 ms: 1.02x faster                                          |
| logging_format             | 6.81 us                                                | 6.67 us: 1.02x faster                                         |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                          |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.93 ms: 1.02x faster                                         |
| deepcopy_reduce            | 3.22 us                                                | 3.16 us: 1.02x faster                                         |
| float                      | 78.9 ms                                                | 77.6 ms: 1.02x faster                                         |
| gc_traversal               | 4.01 ms                                                | 3.94 ms: 1.02x faster                                         |
| pprint_pformat             | 1.55 sec                                               | 1.53 sec: 1.02x faster                                        |
| unpickle_list              | 5.21 us                                                | 5.14 us: 1.01x faster                                         |
| deepcopy                   | 365 us                                                 | 360 us: 1.01x faster                                          |
| scimark_monte_carlo        | 70.7 ms                                                | 69.8 ms: 1.01x faster                                         |
| unpickle_pure_python       | 242 us                                                 | 239 us: 1.01x faster                                          |
| tornado_http               | 98.1 ms                                                | 97.0 ms: 1.01x faster                                         |
| pickle_dict                | 34.6 us                                                | 34.5 us: 1.00x faster                                         |
| sqlglot_normalize          | 113 ms                                                 | 113 ms: 1.00x slower                                          |
| mako                       | 10.7 ms                                                | 10.7 ms: 1.01x slower                                         |
| sympy_expand               | 484 ms                                                 | 489 ms: 1.01x slower                                          |
| pprint_safe_repr           | 747 ms                                                 | 755 ms: 1.01x slower                                          |
| sympy_integrate            | 21.5 ms                                                | 21.9 ms: 1.02x slower                                         |
| meteor_contest             | 109 ms                                                 | 111 ms: 1.02x slower                                          |
| json                       | 5.24 ms                                                | 5.37 ms: 1.02x slower                                         |
| bench_thread_pool          | 834 us                                                 | 855 us: 1.02x slower                                          |
| nqueens                    | 87.9 ms                                                | 90.7 ms: 1.03x slower                                         |
| chameleon                  | 6.70 ms                                                | 6.92 ms: 1.03x slower                                         |
| pathlib                    | 18.5 ms                                                | 19.2 ms: 1.03x slower                                         |
| genshi_xml                 | 53.4 ms                                                | 55.3 ms: 1.03x slower                                         |
| asyncio_websockets         | 550 ms                                                 | 570 ms: 1.04x slower                                          |
| dask                       | 365 ms                                                 | 379 ms: 1.04x slower                                          |
| pycparser                  | 1.19 sec                                               | 1.23 sec: 1.04x slower                                        |
| regex_compile              | 141 ms                                                 | 147 ms: 1.04x slower                                          |
| thrift                     | 784 us                                                 | 817 us: 1.04x slower                                          |
| sqlglot_optimize           | 55.3 ms                                                | 57.9 ms: 1.05x slower                                         |
| html5lib                   | 64.8 ms                                                | 68.0 ms: 1.05x slower                                         |
| 2to3                       | 264 ms                                                 | 278 ms: 1.05x slower                                          |
| xml_etree_process          | 56.9 ms                                                | 59.9 ms: 1.05x slower                                         |
| go                         | 149 ms                                                 | 157 ms: 1.06x slower                                          |
| hexiom                     | 6.89 ms                                                | 7.33 ms: 1.06x slower                                         |
| pickle                     | 11.0 us                                                | 11.8 us: 1.07x slower                                         |
| regex_effbot               | 3.51 ms                                                | 3.75 ms: 1.07x slower                                         |
| xml_etree_generate         | 81.1 ms                                                | 87.2 ms: 1.08x slower                                         |
| genshi_text                | 22.5 ms                                                | 24.3 ms: 1.08x slower                                         |
| scimark_sor                | 121 ms                                                 | 131 ms: 1.08x slower                                          |
| django_template            | 33.5 ms                                                | 36.3 ms: 1.08x slower                                         |
| docutils                   | 2.66 sec                                               | 2.89 sec: 1.08x slower                                        |
| aiohttp                    | 1.12 ms                                                | 1.21 ms: 1.09x slower                                         |
| pickle_list                | 4.59 us                                                | 5.00 us: 1.09x slower                                         |
| gunicorn                   | 1.20 ms                                                | 1.31 ms: 1.09x slower                                         |
| spectral_norm              | 108 ms                                                 | 118 ms: 1.09x slower                                          |
| dulwich_log                | 64.6 ms                                                | 70.6 ms: 1.09x slower                                         |
| pyflate                    | 434 ms                                                 | 483 ms: 1.11x slower                                          |
| regex_dna                  | 205 ms                                                 | 229 ms: 1.12x slower                                          |
| sqlite_synth               | 2.57 us                                                | 2.89 us: 1.12x slower                                         |
| regex_v8                   | 22.9 ms                                                | 25.9 ms: 1.13x slower                                         |
| scimark_lu                 | 116 ms                                                 | 133 ms: 1.14x slower                                          |
| mypy2                      | 686 ms                                                 | 787 ms: 1.15x slower                                          |
| unpickle                   | 13.8 us                                                | 16.0 us: 1.15x slower                                         |
| create_gc_cycles           | 1.43 ms                                                | 1.69 ms: 1.18x slower                                         |
| coverage                   | 78.8 ms                                                | 97.0 ms: 1.23x slower                                         |
| async_generators           | 374 ms                                                 | 461 ms: 1.23x slower                                          |
| telco                      | 6.86 ms                                                | 8.73 ms: 1.27x slower                                         |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.30x slower                                         |
| python_startup_no_site     | 6.01 ms                                                | 9.57 ms: 1.59x slower                                         |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                  |

Benchmark hidden because not significant (3): scimark_fft, xml_etree_iterparse, bench_mp_pool
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 69.73% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x