# Results vs. 3.11.0

- fork: Fidget-Spinner
- ref: stackref_all
- machine: linux-x86_64
- commit hash: 78dbf36
- commit date: 2024-06-08
- overall geometric mean: 1.08x faster
- HPT reliability: 99.94%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-78dbf36 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 268 ms: 1.01x slower                                                    |
| docutils       | 2.66 sec                                               | 2.77 sec: 1.04x slower                                                  |
| html5lib       | 64.8 ms                                                | 67.3 ms: 1.04x slower                                                   |
| tornado_http   | 98.1 ms                                                | 93.8 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                  | 1.01x slower                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-78dbf36 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 439 ms: 1.43x faster                                                    |
| async_tree_none            | 528 ms                                                 | 374 ms: 1.41x faster                                                    |
| async_tree_io_tg           | 1.29 sec                                               | 919 ms: 1.41x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 468 ms: 1.37x faster                                                    |
| async_tree_io              | 1.29 sec                                               | 954 ms: 1.35x faster                                                    |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 595 ms: 1.28x faster                                                    |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 631 ms: 1.19x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.36x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-78dbf36 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 86.3 ms: 1.11x faster                                                   |
| pidigits       | 194 ms                                                 | 190 ms: 1.02x faster                                                    |
| float          | 78.9 ms                                                | 77.9 ms: 1.01x faster                                                   |
| Geometric mean | (ref)                                                  | 1.05x faster                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-78dbf36 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 132 ms: 1.07x faster                                                    |
| regex_effbot   | 3.51 ms                                                | 3.80 ms: 1.08x slower                                                   |
| regex_v8       | 22.9 ms                                                | 26.0 ms: 1.14x slower                                                   |
| regex_dna      | 205 ms                                                 | 233 ms: 1.14x slower                                                    |
| Geometric mean | (ref)                                                  | 1.07x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-78dbf36 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.4 ms: 1.28x faster                                                   |
| unpickle_pure_python | 242 us                                                 | 216 us: 1.12x faster                                                    |
| tomli_loads          | 2.30 sec                                               | 2.15 sec: 1.07x faster                                                  |
| pickle_pure_python   | 320 us                                                 | 299 us: 1.07x faster                                                    |
| xml_etree_parse      | 164 ms                                                 | 156 ms: 1.05x faster                                                    |
| xml_etree_iterparse  | 108 ms                                                 | 106 ms: 1.02x faster                                                    |
| json_loads           | 29.2 us                                                | 28.6 us: 1.02x faster                                                   |
| unpickle_list        | 5.21 us                                                | 5.31 us: 1.02x slower                                                   |
| pickle_dict          | 34.6 us                                                | 35.2 us: 1.02x slower                                                   |
| xml_etree_process    | 56.9 ms                                                | 59.6 ms: 1.05x slower                                                   |
| xml_etree_generate   | 81.1 ms                                                | 85.6 ms: 1.06x slower                                                   |
| pickle               | 11.0 us                                                | 11.8 us: 1.07x slower                                                   |
| unpickle             | 13.8 us                                                | 15.1 us: 1.09x slower                                                   |
| pickle_list          | 4.59 us                                                | 5.18 us: 1.13x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-78dbf36 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.12 ms: 1.18x slower                                                   |
| python_startup         | 8.56 ms                                                | 10.6 ms: 1.24x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-78dbf36 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 50.1 ms: 1.07x faster                                                   |
| django_template | 33.5 ms                                                | 34.2 ms: 1.02x slower                                                   |
| genshi_text     | 22.5 ms                                                | 23.2 ms: 1.03x slower                                                   |
| mako            | 10.7 ms                                                | 11.2 ms: 1.05x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240608-linux-x86_64-Fidget%2dSpinner-stackref_all-3.14.0a0-78dbf36 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 164 us: 3.17x faster                                                    |
| generators                 | 74.9 ms                                                | 29.0 ms: 2.58x faster                                                   |
| asyncio_tcp                | 875 ms                                                 | 501 ms: 1.75x faster                                                    |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.83 sec: 1.70x faster                                                  |
| pylint                     | 476 ms                                                 | 314 ms: 1.52x faster                                                    |
| async_tree_none_tg         | 491 ms                                                 | 336 ms: 1.46x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 439 ms: 1.43x faster                                                    |
| comprehensions             | 23.6 us                                                | 16.5 us: 1.43x faster                                                   |
| async_tree_none            | 528 ms                                                 | 374 ms: 1.41x faster                                                    |
| async_tree_io_tg           | 1.29 sec                                               | 919 ms: 1.41x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 468 ms: 1.37x faster                                                    |
| async_tree_io              | 1.29 sec                                               | 954 ms: 1.35x faster                                                    |
| json_dumps                 | 13.3 ms                                                | 10.4 ms: 1.28x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 595 ms: 1.28x faster                                                    |
| chaos                      | 71.9 ms                                                | 59.3 ms: 1.21x faster                                                   |
| deltablue                  | 3.92 ms                                                | 3.29 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 631 ms: 1.19x faster                                                    |
| raytrace                   | 309 ms                                                 | 264 ms: 1.17x faster                                                    |
| coroutines                 | 27.0 ms                                                | 23.1 ms: 1.17x faster                                                   |
| pathlib                    | 18.5 ms                                                | 16.1 ms: 1.15x faster                                                   |
| richards_super             | 61.9 ms                                                | 54.0 ms: 1.15x faster                                                   |
| unpickle_pure_python       | 242 us                                                 | 216 us: 1.12x faster                                                    |
| hexiom                     | 6.89 ms                                                | 6.19 ms: 1.11x faster                                                   |
| nbody                      | 96.0 ms                                                | 86.3 ms: 1.11x faster                                                   |
| nqueens                    | 87.9 ms                                                | 79.3 ms: 1.11x faster                                                   |
| logging_simple             | 6.22 us                                                | 5.62 us: 1.11x faster                                                   |
| sqlglot_parse              | 1.43 ms                                                | 1.31 ms: 1.10x faster                                                   |
| sympy_sum                  | 169 ms                                                 | 154 ms: 1.09x faster                                                    |
| logging_format             | 6.81 us                                                | 6.24 us: 1.09x faster                                                   |
| sqlglot_transpile          | 1.75 ms                                                | 1.61 ms: 1.09x faster                                                   |
| mdp                        | 2.77 sec                                               | 2.56 sec: 1.09x faster                                                  |
| sympy_str                  | 297 ms                                                 | 277 ms: 1.07x faster                                                    |
| tomli_loads                | 2.30 sec                                               | 2.15 sec: 1.07x faster                                                  |
| pickle_pure_python         | 320 us                                                 | 299 us: 1.07x faster                                                    |
| regex_compile              | 141 ms                                                 | 132 ms: 1.07x faster                                                    |
| genshi_xml                 | 53.4 ms                                                | 50.1 ms: 1.07x faster                                                   |
| sympy_integrate            | 21.5 ms                                                | 20.3 ms: 1.06x faster                                                   |
| logging_silent             | 111 ns                                                 | 105 ns: 1.05x faster                                                    |
| richards                   | 49.8 ms                                                | 47.4 ms: 1.05x faster                                                   |
| go                         | 149 ms                                                 | 142 ms: 1.05x faster                                                    |
| xml_etree_parse            | 164 ms                                                 | 156 ms: 1.05x faster                                                    |
| tornado_http               | 98.1 ms                                                | 93.8 ms: 1.05x faster                                                   |
| scimark_monte_carlo        | 70.7 ms                                                | 67.7 ms: 1.04x faster                                                   |
| sqlglot_normalize          | 113 ms                                                 | 109 ms: 1.03x faster                                                    |
| sympy_expand               | 484 ms                                                 | 471 ms: 1.03x faster                                                    |
| deepcopy_memo              | 40.2 us                                                | 39.3 us: 1.02x faster                                                   |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.92 ms: 1.02x faster                                                   |
| xml_etree_iterparse        | 108 ms                                                 | 106 ms: 1.02x faster                                                    |
| pidigits                   | 194 ms                                                 | 190 ms: 1.02x faster                                                    |
| json_loads                 | 29.2 us                                                | 28.6 us: 1.02x faster                                                   |
| crypto_pyaes               | 76.7 ms                                                | 75.2 ms: 1.02x faster                                                   |
| pprint_pformat             | 1.55 sec                                               | 1.53 sec: 1.02x faster                                                  |
| fannkuch                   | 405 ms                                                 | 398 ms: 1.02x faster                                                    |
| float                      | 78.9 ms                                                | 77.9 ms: 1.01x faster                                                   |
| meteor_contest             | 109 ms                                                 | 108 ms: 1.01x faster                                                    |
| deepcopy                   | 365 us                                                 | 362 us: 1.01x faster                                                    |
| sqlglot_optimize           | 55.3 ms                                                | 54.8 ms: 1.01x faster                                                   |
| gc_traversal               | 4.01 ms                                                | 3.98 ms: 1.01x faster                                                   |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                   |
| pprint_safe_repr           | 747 ms                                                 | 744 ms: 1.00x faster                                                    |
| dulwich_log                | 64.6 ms                                                | 65.1 ms: 1.01x slower                                                   |
| deepcopy_reduce            | 3.22 us                                                | 3.24 us: 1.01x slower                                                   |
| 2to3                       | 264 ms                                                 | 268 ms: 1.01x slower                                                    |
| unpickle_list              | 5.21 us                                                | 5.31 us: 1.02x slower                                                   |
| pickle_dict                | 34.6 us                                                | 35.2 us: 1.02x slower                                                   |
| django_template            | 33.5 ms                                                | 34.2 ms: 1.02x slower                                                   |
| json                       | 5.24 ms                                                | 5.36 ms: 1.02x slower                                                   |
| thrift                     | 784 us                                                 | 806 us: 1.03x slower                                                    |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                                    |
| genshi_text                | 22.5 ms                                                | 23.2 ms: 1.03x slower                                                   |
| scimark_sor                | 121 ms                                                 | 126 ms: 1.04x slower                                                    |
| html5lib                   | 64.8 ms                                                | 67.3 ms: 1.04x slower                                                   |
| docutils                   | 2.66 sec                                               | 2.77 sec: 1.04x slower                                                  |
| xml_etree_process          | 56.9 ms                                                | 59.6 ms: 1.05x slower                                                   |
| mako                       | 10.7 ms                                                | 11.2 ms: 1.05x slower                                                   |
| xml_etree_generate         | 81.1 ms                                                | 85.6 ms: 1.06x slower                                                   |
| spectral_norm              | 108 ms                                                 | 114 ms: 1.06x slower                                                    |
| pickle                     | 11.0 us                                                | 11.8 us: 1.07x slower                                                   |
| regex_effbot               | 3.51 ms                                                | 3.80 ms: 1.08x slower                                                   |
| scimark_fft                | 345 ms                                                 | 376 ms: 1.09x slower                                                    |
| pyflate                    | 434 ms                                                 | 473 ms: 1.09x slower                                                    |
| unpickle                   | 13.8 us                                                | 15.1 us: 1.09x slower                                                   |
| pickle_list                | 4.59 us                                                | 5.18 us: 1.13x slower                                                   |
| regex_v8                   | 22.9 ms                                                | 26.0 ms: 1.14x slower                                                   |
| sqlite_synth               | 2.57 us                                                | 2.93 us: 1.14x slower                                                   |
| regex_dna                  | 205 ms                                                 | 233 ms: 1.14x slower                                                    |
| coverage                   | 78.8 ms                                                | 92.1 ms: 1.17x slower                                                   |
| async_generators           | 374 ms                                                 | 441 ms: 1.18x slower                                                    |
| python_startup_no_site     | 6.01 ms                                                | 7.12 ms: 1.18x slower                                                   |
| telco                      | 6.86 ms                                                | 8.35 ms: 1.22x slower                                                   |
| python_startup             | 8.56 ms                                                | 10.6 ms: 1.24x slower                                                   |
| create_gc_cycles           | 1.43 ms                                                | 1.78 ms: 1.24x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.08x faster                                                            |

Benchmark hidden because not significant (4): bench_thread_pool, scimark_lu, pycparser, dask
Ignored benchmarks (9) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: aiohttp, chameleon, djangocms, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.94% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x