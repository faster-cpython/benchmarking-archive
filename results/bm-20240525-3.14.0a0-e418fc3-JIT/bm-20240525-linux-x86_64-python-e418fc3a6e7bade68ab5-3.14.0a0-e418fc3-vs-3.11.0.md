# Results vs. 3.11.0

- fork: python
- ref: e418fc3a6e7bade68ab5
- machine: linux-x86_64
- commit hash: e418fc3
- commit date: 2024-05-25
- overall geometric mean: 1.07x faster
- HPT reliability: 97.63%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 279 ms: 1.06x slower                                                  |
| chameleon      | 6.70 ms                                                | 7.04 ms: 1.05x slower                                                 |
| docutils       | 2.66 sec                                               | 2.95 sec: 1.11x slower                                                |
| html5lib       | 64.8 ms                                                | 68.1 ms: 1.05x slower                                                 |
| tornado_http   | 98.1 ms                                                | 97.0 ms: 1.01x faster                                                 |
| Geometric mean | (ref)                                                  | 1.05x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 334 ms: 1.47x faster                                                  |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.41x faster                                                  |
| async_tree_io_tg           | 1.29 sec                                               | 942 ms: 1.37x faster                                                  |
| async_tree_none            | 528 ms                                                 | 385 ms: 1.37x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 466 ms: 1.37x faster                                                  |
| async_tree_io              | 1.29 sec                                               | 957 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 585 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 617 ms: 1.21x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.36x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 80.8 ms: 1.19x faster                                                 |
| float          | 78.9 ms                                                | 72.2 ms: 1.09x faster                                                 |
| pidigits       | 194 ms                                                 | 188 ms: 1.03x faster                                                  |
| Geometric mean | (ref)                                                  | 1.10x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 138 ms: 1.02x faster                                                  |
| regex_effbot   | 3.51 ms                                                | 3.72 ms: 1.06x slower                                                 |
| regex_v8       | 22.9 ms                                                | 25.1 ms: 1.10x slower                                                 |
| regex_dna      | 205 ms                                                 | 229 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.3 ms: 1.29x faster                                                 |
| tomli_loads          | 2.30 sec                                               | 1.96 sec: 1.17x faster                                                |
| xml_etree_parse      | 164 ms                                                 | 150 ms: 1.09x faster                                                  |
| unpickle_pure_python | 242 us                                                 | 224 us: 1.08x faster                                                  |
| xml_etree_iterparse  | 108 ms                                                 | 101 ms: 1.07x faster                                                  |
| pickle_pure_python   | 320 us                                                 | 301 us: 1.06x faster                                                  |
| json_loads           | 29.2 us                                                | 29.0 us: 1.01x faster                                                 |
| xml_etree_generate   | 81.1 ms                                                | 81.8 ms: 1.01x slower                                                 |
| xml_etree_process    | 56.9 ms                                                | 57.8 ms: 1.02x slower                                                 |
| unpickle_list        | 5.21 us                                                | 5.34 us: 1.02x slower                                                 |
| pickle_dict          | 34.6 us                                                | 35.9 us: 1.04x slower                                                 |
| pickle               | 11.0 us                                                | 11.9 us: 1.09x slower                                                 |
| pickle_list          | 4.59 us                                                | 5.07 us: 1.11x slower                                                 |
| unpickle             | 13.8 us                                                | 15.5 us: 1.12x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.59 ms: 1.26x slower                                                 |
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.29x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.28x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| mako            | 10.7 ms                                                | 9.82 ms: 1.09x faster                                                 |
| django_template | 33.5 ms                                                | 36.0 ms: 1.07x slower                                                 |
| genshi_xml      | 53.4 ms                                                | 57.4 ms: 1.07x slower                                                 |
| genshi_text     | 22.5 ms                                                | 25.0 ms: 1.11x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240525-linux-x86_64-python-e418fc3a6e7bade68ab5-3.14.0a0-e418fc3 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 173 us: 3.01x faster                                                  |
| generators                 | 74.9 ms                                                | 30.4 ms: 2.46x faster                                                 |
| asyncio_tcp                | 875 ms                                                 | 520 ms: 1.68x faster                                                  |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                |
| async_tree_none_tg         | 491 ms                                                 | 334 ms: 1.47x faster                                                  |
| comprehensions             | 23.6 us                                                | 16.6 us: 1.42x faster                                                 |
| async_tree_memoization_tg  | 626 ms                                                 | 443 ms: 1.41x faster                                                  |
| async_tree_io_tg           | 1.29 sec                                               | 942 ms: 1.37x faster                                                  |
| async_tree_none            | 528 ms                                                 | 385 ms: 1.37x faster                                                  |
| async_tree_memoization     | 639 ms                                                 | 466 ms: 1.37x faster                                                  |
| pylint                     | 476 ms                                                 | 353 ms: 1.35x faster                                                  |
| async_tree_io              | 1.29 sec                                               | 957 ms: 1.35x faster                                                  |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 585 ms: 1.30x faster                                                  |
| json_dumps                 | 13.3 ms                                                | 10.3 ms: 1.29x faster                                                 |
| richards_super             | 61.9 ms                                                | 48.0 ms: 1.29x faster                                                 |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 617 ms: 1.21x faster                                                  |
| chaos                      | 71.9 ms                                                | 59.7 ms: 1.20x faster                                                 |
| richards                   | 49.8 ms                                                | 41.7 ms: 1.19x faster                                                 |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.21 ms: 1.19x faster                                                 |
| nbody                      | 96.0 ms                                                | 80.8 ms: 1.19x faster                                                 |
| coroutines                 | 27.0 ms                                                | 22.9 ms: 1.18x faster                                                 |
| tomli_loads                | 2.30 sec                                               | 1.96 sec: 1.17x faster                                                |
| fannkuch                   | 405 ms                                                 | 356 ms: 1.14x faster                                                  |
| scimark_monte_carlo        | 70.7 ms                                                | 62.1 ms: 1.14x faster                                                 |
| crypto_pyaes               | 76.7 ms                                                | 67.4 ms: 1.14x faster                                                 |
| pathlib                    | 18.5 ms                                                | 16.4 ms: 1.13x faster                                                 |
| scimark_fft                | 345 ms                                                 | 309 ms: 1.12x faster                                                  |
| raytrace                   | 309 ms                                                 | 278 ms: 1.11x faster                                                  |
| logging_simple             | 6.22 us                                                | 5.67 us: 1.10x faster                                                 |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.09x faster                                                 |
| float                      | 78.9 ms                                                | 72.2 ms: 1.09x faster                                                 |
| xml_etree_parse            | 164 ms                                                 | 150 ms: 1.09x faster                                                  |
| mako                       | 10.7 ms                                                | 9.82 ms: 1.09x faster                                                 |
| logging_format             | 6.81 us                                                | 6.29 us: 1.08x faster                                                 |
| mdp                        | 2.77 sec                                               | 2.57 sec: 1.08x faster                                                |
| unpickle_pure_python       | 242 us                                                 | 224 us: 1.08x faster                                                  |
| spectral_norm              | 108 ms                                                 | 100 ms: 1.08x faster                                                  |
| sqlglot_transpile          | 1.75 ms                                                | 1.63 ms: 1.08x faster                                                 |
| xml_etree_iterparse        | 108 ms                                                 | 101 ms: 1.07x faster                                                  |
| pickle_pure_python         | 320 us                                                 | 301 us: 1.06x faster                                                  |
| pprint_pformat             | 1.55 sec                                               | 1.47 sec: 1.05x faster                                                |
| deltablue                  | 3.92 ms                                                | 3.72 ms: 1.05x faster                                                 |
| hexiom                     | 6.89 ms                                                | 6.56 ms: 1.05x faster                                                 |
| gc_traversal               | 4.01 ms                                                | 3.85 ms: 1.04x faster                                                 |
| deepcopy_memo              | 40.2 us                                                | 38.6 us: 1.04x faster                                                 |
| pidigits                   | 194 ms                                                 | 188 ms: 1.03x faster                                                  |
| pprint_safe_repr           | 747 ms                                                 | 725 ms: 1.03x faster                                                  |
| logging_silent             | 111 ns                                                 | 108 ns: 1.03x faster                                                  |
| regex_compile              | 141 ms                                                 | 138 ms: 1.02x faster                                                  |
| nqueens                    | 87.9 ms                                                | 86.6 ms: 1.01x faster                                                 |
| tornado_http               | 98.1 ms                                                | 97.0 ms: 1.01x faster                                                 |
| json_loads                 | 29.2 us                                                | 29.0 us: 1.01x faster                                                 |
| meteor_contest             | 109 ms                                                 | 108 ms: 1.01x faster                                                  |
| sqlglot_normalize          | 113 ms                                                 | 114 ms: 1.01x slower                                                  |
| xml_etree_generate         | 81.1 ms                                                | 81.8 ms: 1.01x slower                                                 |
| sympy_sum                  | 169 ms                                                 | 171 ms: 1.01x slower                                                  |
| json                       | 5.24 ms                                                | 5.32 ms: 1.02x slower                                                 |
| xml_etree_process          | 56.9 ms                                                | 57.8 ms: 1.02x slower                                                 |
| sympy_str                  | 297 ms                                                 | 303 ms: 1.02x slower                                                  |
| sqlglot_optimize           | 55.3 ms                                                | 56.4 ms: 1.02x slower                                                 |
| unpickle_list              | 5.21 us                                                | 5.34 us: 1.02x slower                                                 |
| pycparser                  | 1.19 sec                                               | 1.22 sec: 1.03x slower                                                |
| asyncio_websockets         | 550 ms                                                 | 566 ms: 1.03x slower                                                  |
| dask                       | 365 ms                                                 | 376 ms: 1.03x slower                                                  |
| pickle_dict                | 34.6 us                                                | 35.9 us: 1.04x slower                                                 |
| bench_thread_pool          | 834 us                                                 | 867 us: 1.04x slower                                                  |
| thrift                     | 784 us                                                 | 816 us: 1.04x slower                                                  |
| deepcopy_reduce            | 3.22 us                                                | 3.35 us: 1.04x slower                                                 |
| pyflate                    | 434 ms                                                 | 455 ms: 1.05x slower                                                  |
| html5lib                   | 64.8 ms                                                | 68.1 ms: 1.05x slower                                                 |
| scimark_lu                 | 116 ms                                                 | 122 ms: 1.05x slower                                                  |
| sympy_expand               | 484 ms                                                 | 509 ms: 1.05x slower                                                  |
| sympy_integrate            | 21.5 ms                                                | 22.6 ms: 1.05x slower                                                 |
| chameleon                  | 6.70 ms                                                | 7.04 ms: 1.05x slower                                                 |
| 2to3                       | 264 ms                                                 | 279 ms: 1.06x slower                                                  |
| regex_effbot               | 3.51 ms                                                | 3.72 ms: 1.06x slower                                                 |
| dulwich_log                | 64.6 ms                                                | 69.3 ms: 1.07x slower                                                 |
| django_template            | 33.5 ms                                                | 36.0 ms: 1.07x slower                                                 |
| genshi_xml                 | 53.4 ms                                                | 57.4 ms: 1.07x slower                                                 |
| pickle                     | 11.0 us                                                | 11.9 us: 1.09x slower                                                 |
| regex_v8                   | 22.9 ms                                                | 25.1 ms: 1.10x slower                                                 |
| pickle_list                | 4.59 us                                                | 5.07 us: 1.11x slower                                                 |
| docutils                   | 2.66 sec                                               | 2.95 sec: 1.11x slower                                                |
| genshi_text                | 22.5 ms                                                | 25.0 ms: 1.11x slower                                                 |
| sqlite_synth               | 2.57 us                                                | 2.86 us: 1.11x slower                                                 |
| unpickle                   | 13.8 us                                                | 15.5 us: 1.12x slower                                                 |
| regex_dna                  | 205 ms                                                 | 229 ms: 1.12x slower                                                  |
| scimark_sor                | 121 ms                                                 | 138 ms: 1.13x slower                                                  |
| telco                      | 6.86 ms                                                | 8.12 ms: 1.18x slower                                                 |
| coverage                   | 78.8 ms                                                | 94.0 ms: 1.19x slower                                                 |
| async_generators           | 374 ms                                                 | 462 ms: 1.24x slower                                                  |
| python_startup_no_site     | 6.01 ms                                                | 7.59 ms: 1.26x slower                                                 |
| flaskblogging              | 7.28 ms                                                | 9.20 ms: 1.26x slower                                                 |
| create_gc_cycles           | 1.43 ms                                                | 1.84 ms: 1.28x slower                                                 |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.29x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                          |

Benchmark hidden because not significant (3): go, deepcopy, bench_mp_pool
Ignored benchmarks (7) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, djangocms, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 97.63% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.13x