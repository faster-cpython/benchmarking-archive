# Results vs. 3.11.0

- fork: brandtbucher
- ref: hoist
- machine: linux-x86_64
- commit hash: bc99ede
- commit date: 2024-05-08
- overall geometric mean: 1.03x faster
- HPT reliability: 96.95%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-hoist-3.14.0a0-bc99ede |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 279 ms: 1.06x slower                                         |
| chameleon      | 6.70 ms                                                | 7.07 ms: 1.05x slower                                        |
| docutils       | 2.66 sec                                               | 2.96 sec: 1.11x slower                                       |
| html5lib       | 64.8 ms                                                | 69.7 ms: 1.08x slower                                        |
| tornado_http   | 98.1 ms                                                | 97.4 ms: 1.01x faster                                        |
| Geometric mean | (ref)                                                  | 1.06x slower                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-hoist-3.14.0a0-bc99ede |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 364 ms: 1.45x faster                                         |
| async_tree_none_tg         | 491 ms                                                 | 344 ms: 1.43x faster                                         |
| async_tree_memoization_tg  | 626 ms                                                 | 451 ms: 1.39x faster                                         |
| async_tree_io              | 1.29 sec                                               | 932 ms: 1.38x faster                                         |
| async_tree_memoization     | 639 ms                                                 | 478 ms: 1.34x faster                                         |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 583 ms: 1.31x faster                                         |
| async_tree_io_tg           | 1.29 sec                                               | 1.02 sec: 1.27x faster                                       |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 617 ms: 1.21x faster                                         |
| Geometric mean             | (ref)                                                  | 1.34x faster                                                 |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-hoist-3.14.0a0-bc99ede |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 86.0 ms: 1.12x faster                                        |
| float          | 78.9 ms                                                | 70.8 ms: 1.11x faster                                        |
| pidigits       | 194 ms                                                 | 188 ms: 1.03x faster                                         |
| Geometric mean | (ref)                                                  | 1.09x faster                                                 |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-hoist-3.14.0a0-bc99ede |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 140 ms: 1.01x faster                                         |
| regex_effbot   | 3.51 ms                                                | 3.66 ms: 1.04x slower                                        |
| regex_v8       | 22.9 ms                                                | 24.6 ms: 1.08x slower                                        |
| regex_dna      | 205 ms                                                 | 221 ms: 1.08x slower                                         |
| Geometric mean | (ref)                                                  | 1.05x slower                                                 |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-hoist-3.14.0a0-bc99ede |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.4 ms: 1.29x faster                                        |
| tomli_loads          | 2.30 sec                                               | 1.99 sec: 1.16x faster                                       |
| unpickle_pure_python | 242 us                                                 | 221 us: 1.09x faster                                         |
| xml_etree_parse      | 164 ms                                                 | 153 ms: 1.07x faster                                         |
| xml_etree_iterparse  | 108 ms                                                 | 102 ms: 1.06x faster                                         |
| pickle_pure_python   | 320 us                                                 | 308 us: 1.04x faster                                         |
| pickle_dict          | 34.6 us                                                | 33.9 us: 1.02x faster                                        |
| json_loads           | 29.2 us                                                | 29.0 us: 1.01x faster                                        |
| xml_etree_process    | 56.9 ms                                                | 57.9 ms: 1.02x slower                                        |
| xml_etree_generate   | 81.1 ms                                                | 82.5 ms: 1.02x slower                                        |
| unpickle_list        | 5.21 us                                                | 5.40 us: 1.04x slower                                        |
| pickle               | 11.0 us                                                | 11.8 us: 1.07x slower                                        |
| pickle_list          | 4.59 us                                                | 5.14 us: 1.12x slower                                        |
| unpickle             | 13.8 us                                                | 16.2 us: 1.17x slower                                        |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                 |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-hoist-3.14.0a0-bc99ede |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.67 ms: 1.28x slower                                        |
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.30x slower                                        |
| Geometric mean         | (ref)                                                  | 1.29x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-hoist-3.14.0a0-bc99ede |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 9.52 ms: 1.12x faster                                        |
| django_template | 33.5 ms                                                | 36.0 ms: 1.07x slower                                        |
| genshi_xml      | 53.4 ms                                                | 58.5 ms: 1.09x slower                                        |
| genshi_text     | 22.5 ms                                                | 24.7 ms: 1.10x slower                                        |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240508-linux-x86_64-brandtbucher-hoist-3.14.0a0-bc99ede |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 177 us: 2.93x faster                                         |
| generators                 | 74.9 ms                                                | 29.7 ms: 2.52x faster                                        |
| asyncio_tcp                | 875 ms                                                 | 515 ms: 1.70x faster                                         |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                       |
| async_tree_none            | 528 ms                                                 | 364 ms: 1.45x faster                                         |
| async_tree_none_tg         | 491 ms                                                 | 344 ms: 1.43x faster                                         |
| comprehensions             | 23.6 us                                                | 16.6 us: 1.42x faster                                        |
| async_tree_memoization_tg  | 626 ms                                                 | 451 ms: 1.39x faster                                         |
| async_tree_io              | 1.29 sec                                               | 932 ms: 1.38x faster                                         |
| async_tree_memoization     | 639 ms                                                 | 478 ms: 1.34x faster                                         |
| pylint                     | 476 ms                                                 | 357 ms: 1.33x faster                                         |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 583 ms: 1.31x faster                                         |
| json_dumps                 | 13.3 ms                                                | 10.4 ms: 1.29x faster                                        |
| richards_super             | 61.9 ms                                                | 48.8 ms: 1.27x faster                                        |
| async_tree_io_tg           | 1.29 sec                                               | 1.02 sec: 1.27x faster                                       |
| chaos                      | 71.9 ms                                                | 59.0 ms: 1.22x faster                                        |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 617 ms: 1.21x faster                                         |
| coroutines                 | 27.0 ms                                                | 22.7 ms: 1.19x faster                                        |
| richards                   | 49.8 ms                                                | 42.7 ms: 1.17x faster                                        |
| tomli_loads                | 2.30 sec                                               | 1.99 sec: 1.16x faster                                       |
| mako                       | 10.7 ms                                                | 9.52 ms: 1.12x faster                                        |
| nbody                      | 96.0 ms                                                | 86.0 ms: 1.12x faster                                        |
| float                      | 78.9 ms                                                | 70.8 ms: 1.11x faster                                        |
| crypto_pyaes               | 76.7 ms                                                | 69.1 ms: 1.11x faster                                        |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.55 ms: 1.11x faster                                        |
| scimark_monte_carlo        | 70.7 ms                                                | 64.1 ms: 1.10x faster                                        |
| fannkuch                   | 405 ms                                                 | 368 ms: 1.10x faster                                         |
| unpickle_pure_python       | 242 us                                                 | 221 us: 1.09x faster                                         |
| spectral_norm              | 108 ms                                                 | 99.0 ms: 1.09x faster                                        |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.09x faster                                        |
| raytrace                   | 309 ms                                                 | 283 ms: 1.09x faster                                         |
| logging_simple             | 6.22 us                                                | 5.72 us: 1.09x faster                                        |
| scimark_fft                | 345 ms                                                 | 321 ms: 1.08x faster                                         |
| xml_etree_parse            | 164 ms                                                 | 153 ms: 1.07x faster                                         |
| mdp                        | 2.77 sec                                               | 2.61 sec: 1.06x faster                                       |
| deepcopy_memo              | 40.2 us                                                | 37.7 us: 1.06x faster                                        |
| sqlglot_transpile          | 1.75 ms                                                | 1.65 ms: 1.06x faster                                        |
| logging_format             | 6.81 us                                                | 6.41 us: 1.06x faster                                        |
| xml_etree_iterparse        | 108 ms                                                 | 102 ms: 1.06x faster                                         |
| deltablue                  | 3.92 ms                                                | 3.73 ms: 1.05x faster                                        |
| logging_silent             | 111 ns                                                 | 106 ns: 1.05x faster                                         |
| gc_traversal               | 4.01 ms                                                | 3.84 ms: 1.04x faster                                        |
| pathlib                    | 18.5 ms                                                | 17.8 ms: 1.04x faster                                        |
| pickle_pure_python         | 320 us                                                 | 308 us: 1.04x faster                                         |
| pycparser                  | 1.19 sec                                               | 1.15 sec: 1.03x faster                                       |
| pidigits                   | 194 ms                                                 | 188 ms: 1.03x faster                                         |
| pprint_pformat             | 1.55 sec                                               | 1.51 sec: 1.03x faster                                       |
| pprint_safe_repr           | 747 ms                                                 | 727 ms: 1.03x faster                                         |
| hexiom                     | 6.89 ms                                                | 6.73 ms: 1.02x faster                                        |
| pickle_dict                | 34.6 us                                                | 33.9 us: 1.02x faster                                        |
| go                         | 149 ms                                                 | 147 ms: 1.01x faster                                         |
| json_loads                 | 29.2 us                                                | 29.0 us: 1.01x faster                                        |
| tornado_http               | 98.1 ms                                                | 97.4 ms: 1.01x faster                                        |
| regex_compile              | 141 ms                                                 | 140 ms: 1.01x faster                                         |
| sqlglot_normalize          | 113 ms                                                 | 113 ms: 1.00x slower                                         |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                         |
| xml_etree_process          | 56.9 ms                                                | 57.9 ms: 1.02x slower                                        |
| xml_etree_generate         | 81.1 ms                                                | 82.5 ms: 1.02x slower                                        |
| json                       | 5.24 ms                                                | 5.34 ms: 1.02x slower                                        |
| sympy_str                  | 297 ms                                                 | 304 ms: 1.02x slower                                         |
| deepcopy_reduce            | 3.22 us                                                | 3.31 us: 1.03x slower                                        |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                         |
| sympy_sum                  | 169 ms                                                 | 174 ms: 1.03x slower                                         |
| sqlglot_optimize           | 55.3 ms                                                | 57.1 ms: 1.03x slower                                        |
| thrift                     | 784 us                                                 | 809 us: 1.03x slower                                         |
| pyflate                    | 434 ms                                                 | 449 ms: 1.03x slower                                         |
| deepcopy                   | 365 us                                                 | 378 us: 1.03x slower                                         |
| unpickle_list              | 5.21 us                                                | 5.40 us: 1.04x slower                                        |
| dask                       | 365 ms                                                 | 379 ms: 1.04x slower                                         |
| bench_thread_pool          | 834 us                                                 | 868 us: 1.04x slower                                         |
| regex_effbot               | 3.51 ms                                                | 3.66 ms: 1.04x slower                                        |
| chameleon                  | 6.70 ms                                                | 7.07 ms: 1.05x slower                                        |
| sympy_expand               | 484 ms                                                 | 511 ms: 1.06x slower                                         |
| 2to3                       | 264 ms                                                 | 279 ms: 1.06x slower                                         |
| sympy_integrate            | 21.5 ms                                                | 22.8 ms: 1.06x slower                                        |
| scimark_sor                | 121 ms                                                 | 129 ms: 1.06x slower                                         |
| django_template            | 33.5 ms                                                | 36.0 ms: 1.07x slower                                        |
| pickle                     | 11.0 us                                                | 11.8 us: 1.07x slower                                        |
| html5lib                   | 64.8 ms                                                | 69.7 ms: 1.08x slower                                        |
| regex_v8                   | 22.9 ms                                                | 24.6 ms: 1.08x slower                                        |
| scimark_lu                 | 116 ms                                                 | 125 ms: 1.08x slower                                         |
| regex_dna                  | 205 ms                                                 | 221 ms: 1.08x slower                                         |
| dulwich_log                | 64.6 ms                                                | 70.1 ms: 1.09x slower                                        |
| genshi_xml                 | 53.4 ms                                                | 58.5 ms: 1.09x slower                                        |
| genshi_text                | 22.5 ms                                                | 24.7 ms: 1.10x slower                                        |
| docutils                   | 2.66 sec                                               | 2.96 sec: 1.11x slower                                       |
| sqlite_synth               | 2.57 us                                                | 2.87 us: 1.11x slower                                        |
| pickle_list                | 4.59 us                                                | 5.14 us: 1.12x slower                                        |
| coverage                   | 78.8 ms                                                | 88.7 ms: 1.13x slower                                        |
| aiohttp                    | 1.12 ms                                                | 1.26 ms: 1.13x slower                                        |
| gunicorn                   | 1.20 ms                                                | 1.35 ms: 1.13x slower                                        |
| unpickle                   | 13.8 us                                                | 16.2 us: 1.17x slower                                        |
| async_generators           | 374 ms                                                 | 465 ms: 1.24x slower                                         |
| create_gc_cycles           | 1.43 ms                                                | 1.81 ms: 1.26x slower                                        |
| flaskblogging              | 7.28 ms                                                | 9.23 ms: 1.27x slower                                        |
| python_startup_no_site     | 6.01 ms                                                | 7.67 ms: 1.28x slower                                        |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.30x slower                                        |
| telco                      | 6.86 ms                                                | 171 ms: 24.99x slower                                        |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                 |

Benchmark hidden because not significant (2): nqueens, bench_mp_pool
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: djangocms, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 96.95% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.14x