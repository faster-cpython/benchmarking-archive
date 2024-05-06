# Results vs. 3.11.0

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: 8eee1b4
- commit date: 2024-04-02
- overall geometric mean: 1.08x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 313 ms: 1.18x slower                                              |
| chameleon      | 6.70 ms                                                | 7.85 ms: 1.17x slower                                             |
| docutils       | 2.66 sec                                               | 3.16 sec: 1.19x slower                                            |
| html5lib       | 64.8 ms                                                | 73.9 ms: 1.14x slower                                             |
| tornado_http   | 98.1 ms                                                | 103 ms: 1.05x slower                                              |
| Geometric mean | (ref)                                                  | 1.15x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 382 ms: 1.38x faster                                              |
| async_tree_none_tg         | 491 ms                                                 | 363 ms: 1.35x faster                                              |
| async_tree_memoization_tg  | 626 ms                                                 | 473 ms: 1.33x faster                                              |
| async_tree_io              | 1.29 sec                                               | 982 ms: 1.31x faster                                              |
| async_tree_io_tg           | 1.29 sec                                               | 1.01 sec: 1.28x faster                                            |
| async_tree_memoization     | 639 ms                                                 | 515 ms: 1.24x faster                                              |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 634 ms: 1.20x faster                                              |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 643 ms: 1.17x faster                                              |
| Geometric mean             | (ref)                                                  | 1.28x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 197 ms: 1.02x slower                                              |
| float          | 78.9 ms                                                | 94.6 ms: 1.20x slower                                             |
| nbody          | 96.0 ms                                                | 132 ms: 1.37x slower                                              |
| Geometric mean | (ref)                                                  | 1.19x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.79 ms: 1.08x slower                                             |
| regex_dna      | 205 ms                                                 | 227 ms: 1.11x slower                                              |
| regex_v8       | 22.9 ms                                                | 26.7 ms: 1.17x slower                                             |
| regex_compile  | 141 ms                                                 | 194 ms: 1.37x slower                                              |
| Geometric mean | (ref)                                                  | 1.18x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.8 ms: 1.24x faster                                             |
| json_loads           | 29.2 us                                                | 28.5 us: 1.02x faster                                             |
| pickle_dict          | 34.6 us                                                | 34.1 us: 1.01x faster                                             |
| pickle_pure_python   | 320 us                                                 | 316 us: 1.01x faster                                              |
| unpickle_list        | 5.21 us                                                | 5.16 us: 1.01x faster                                             |
| xml_etree_iterparse  | 108 ms                                                 | 115 ms: 1.07x slower                                              |
| pickle               | 11.0 us                                                | 11.9 us: 1.08x slower                                             |
| pickle_list          | 4.59 us                                                | 5.00 us: 1.09x slower                                             |
| unpickle             | 13.8 us                                                | 15.4 us: 1.11x slower                                             |
| xml_etree_process    | 56.9 ms                                                | 65.8 ms: 1.16x slower                                             |
| xml_etree_generate   | 81.1 ms                                                | 96.8 ms: 1.19x slower                                             |
| tomli_loads          | 2.30 sec                                               | 2.78 sec: 1.21x slower                                            |
| unpickle_pure_python | 242 us                                                 | 309 us: 1.28x slower                                              |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                      |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.7 ms: 1.25x slower                                             |
| python_startup_no_site | 6.01 ms                                                | 9.10 ms: 1.51x slower                                             |
| Geometric mean         | (ref)                                                  | 1.38x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_text    | 22.5 ms                                                | 26.0 ms: 1.16x slower                                             |
| genshi_xml     | 53.4 ms                                                | 62.7 ms: 1.17x slower                                             |
| mako           | 10.7 ms                                                | 13.9 ms: 1.30x slower                                             |
| Geometric mean | (ref)                                                  | 1.21x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 129 us: 4.03x faster                                              |
| generators                 | 74.9 ms                                                | 30.0 ms: 2.50x faster                                             |
| asyncio_tcp                | 875 ms                                                 | 517 ms: 1.69x faster                                              |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.87 sec: 1.66x faster                                            |
| pylint                     | 476 ms                                                 | 315 ms: 1.51x faster                                              |
| async_tree_none            | 528 ms                                                 | 382 ms: 1.38x faster                                              |
| async_tree_none_tg         | 491 ms                                                 | 363 ms: 1.35x faster                                              |
| async_tree_memoization_tg  | 626 ms                                                 | 473 ms: 1.33x faster                                              |
| async_tree_io              | 1.29 sec                                               | 982 ms: 1.31x faster                                              |
| async_tree_io_tg           | 1.29 sec                                               | 1.01 sec: 1.28x faster                                            |
| async_tree_memoization     | 639 ms                                                 | 515 ms: 1.24x faster                                              |
| json_dumps                 | 13.3 ms                                                | 10.8 ms: 1.24x faster                                             |
| coroutines                 | 27.0 ms                                                | 22.3 ms: 1.21x faster                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 634 ms: 1.20x faster                                              |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 643 ms: 1.17x faster                                              |
| logging_silent             | 111 ns                                                 | 108 ns: 1.03x faster                                              |
| json_loads                 | 29.2 us                                                | 28.5 us: 1.02x faster                                             |
| pickle_dict                | 34.6 us                                                | 34.1 us: 1.01x faster                                             |
| pickle_pure_python         | 320 us                                                 | 316 us: 1.01x faster                                              |
| unpickle_list              | 5.21 us                                                | 5.16 us: 1.01x faster                                             |
| gc_traversal               | 4.01 ms                                                | 4.00 ms: 1.00x faster                                             |
| pidigits                   | 194 ms                                                 | 197 ms: 1.02x slower                                              |
| mdp                        | 2.77 sec                                               | 2.84 sec: 1.02x slower                                            |
| asyncio_websockets         | 550 ms                                                 | 565 ms: 1.03x slower                                              |
| deepcopy_reduce            | 3.22 us                                                | 3.35 us: 1.04x slower                                             |
| json                       | 5.24 ms                                                | 5.47 ms: 1.04x slower                                             |
| tornado_http               | 98.1 ms                                                | 103 ms: 1.05x slower                                              |
| dask                       | 365 ms                                                 | 384 ms: 1.05x slower                                              |
| xml_etree_iterparse        | 108 ms                                                 | 115 ms: 1.07x slower                                              |
| deepcopy                   | 365 us                                                 | 391 us: 1.07x slower                                              |
| sqlglot_transpile          | 1.75 ms                                                | 1.88 ms: 1.07x slower                                             |
| logging_simple             | 6.22 us                                                | 6.68 us: 1.07x slower                                             |
| bench_thread_pool          | 834 us                                                 | 897 us: 1.08x slower                                              |
| regex_effbot               | 3.51 ms                                                | 3.79 ms: 1.08x slower                                             |
| logging_format             | 6.81 us                                                | 7.37 us: 1.08x slower                                             |
| pickle                     | 11.0 us                                                | 11.9 us: 1.08x slower                                             |
| thrift                     | 784 us                                                 | 850 us: 1.08x slower                                              |
| sqlglot_parse              | 1.43 ms                                                | 1.55 ms: 1.08x slower                                             |
| pickle_list                | 4.59 us                                                | 5.00 us: 1.09x slower                                             |
| sympy_sum                  | 169 ms                                                 | 184 ms: 1.09x slower                                              |
| comprehensions             | 23.6 us                                                | 25.9 us: 1.10x slower                                             |
| richards_super             | 61.9 ms                                                | 68.0 ms: 1.10x slower                                             |
| pathlib                    | 18.5 ms                                                | 20.4 ms: 1.10x slower                                             |
| unpickle                   | 13.8 us                                                | 15.4 us: 1.11x slower                                             |
| regex_dna                  | 205 ms                                                 | 227 ms: 1.11x slower                                              |
| chaos                      | 71.9 ms                                                | 79.9 ms: 1.11x slower                                             |
| sympy_integrate            | 21.5 ms                                                | 24.1 ms: 1.12x slower                                             |
| aiohttp                    | 1.12 ms                                                | 1.25 ms: 1.13x slower                                             |
| gunicorn                   | 1.20 ms                                                | 1.36 ms: 1.13x slower                                             |
| sympy_str                  | 297 ms                                                 | 338 ms: 1.14x slower                                              |
| html5lib                   | 64.8 ms                                                | 73.9 ms: 1.14x slower                                             |
| sympy_expand               | 484 ms                                                 | 554 ms: 1.14x slower                                              |
| genshi_text                | 22.5 ms                                                | 26.0 ms: 1.16x slower                                             |
| deltablue                  | 3.92 ms                                                | 4.53 ms: 1.16x slower                                             |
| xml_etree_process          | 56.9 ms                                                | 65.8 ms: 1.16x slower                                             |
| sqlglot_normalize          | 113 ms                                                 | 131 ms: 1.17x slower                                              |
| regex_v8                   | 22.9 ms                                                | 26.7 ms: 1.17x slower                                             |
| meteor_contest             | 109 ms                                                 | 127 ms: 1.17x slower                                              |
| chameleon                  | 6.70 ms                                                | 7.85 ms: 1.17x slower                                             |
| genshi_xml                 | 53.4 ms                                                | 62.7 ms: 1.17x slower                                             |
| dulwich_log                | 64.6 ms                                                | 76.3 ms: 1.18x slower                                             |
| 2to3                       | 264 ms                                                 | 313 ms: 1.18x slower                                              |
| docutils                   | 2.66 sec                                               | 3.16 sec: 1.19x slower                                            |
| xml_etree_generate         | 81.1 ms                                                | 96.8 ms: 1.19x slower                                             |
| float                      | 78.9 ms                                                | 94.6 ms: 1.20x slower                                             |
| sqlite_synth               | 2.57 us                                                | 3.09 us: 1.20x slower                                             |
| tomli_loads                | 2.30 sec                                               | 2.78 sec: 1.21x slower                                            |
| raytrace                   | 309 ms                                                 | 373 ms: 1.21x slower                                              |
| crypto_pyaes               | 76.7 ms                                                | 93.4 ms: 1.22x slower                                             |
| mypy2                      | 686 ms                                                 | 836 ms: 1.22x slower                                              |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                             |
| sqlglot_optimize           | 55.3 ms                                                | 67.5 ms: 1.22x slower                                             |
| pycparser                  | 1.19 sec                                               | 1.45 sec: 1.22x slower                                            |
| fannkuch                   | 405 ms                                                 | 497 ms: 1.23x slower                                              |
| richards                   | 49.8 ms                                                | 61.1 ms: 1.23x slower                                             |
| go                         | 149 ms                                                 | 185 ms: 1.24x slower                                              |
| deepcopy_memo              | 40.2 us                                                | 49.9 us: 1.24x slower                                             |
| scimark_sor                | 121 ms                                                 | 151 ms: 1.25x slower                                              |
| coverage                   | 78.8 ms                                                | 98.2 ms: 1.25x slower                                             |
| python_startup             | 8.56 ms                                                | 10.7 ms: 1.25x slower                                             |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 6.33 ms: 1.26x slower                                             |
| scimark_monte_carlo        | 70.7 ms                                                | 90.2 ms: 1.28x slower                                             |
| unpickle_pure_python       | 242 us                                                 | 309 us: 1.28x slower                                              |
| async_generators           | 374 ms                                                 | 483 ms: 1.29x slower                                              |
| mako                       | 10.7 ms                                                | 13.9 ms: 1.30x slower                                             |
| scimark_fft                | 345 ms                                                 | 463 ms: 1.34x slower                                              |
| nbody                      | 96.0 ms                                                | 132 ms: 1.37x slower                                              |
| regex_compile              | 141 ms                                                 | 194 ms: 1.37x slower                                              |
| nqueens                    | 87.9 ms                                                | 121 ms: 1.38x slower                                              |
| telco                      | 6.86 ms                                                | 9.69 ms: 1.41x slower                                             |
| spectral_norm              | 108 ms                                                 | 153 ms: 1.42x slower                                              |
| hexiom                     | 6.89 ms                                                | 10.2 ms: 1.48x slower                                             |
| pyflate                    | 434 ms                                                 | 651 ms: 1.50x slower                                              |
| pprint_pformat             | 1.55 sec                                               | 2.35 sec: 1.51x slower                                            |
| scimark_lu                 | 116 ms                                                 | 176 ms: 1.51x slower                                              |
| pprint_safe_repr           | 747 ms                                                 | 1.13 sec: 1.51x slower                                            |
| python_startup_no_site     | 6.01 ms                                                | 9.10 ms: 1.51x slower                                             |
| unpack_sequence            | 43.5 ns                                                | 79.3 ns: 1.83x slower                                             |
| Geometric mean             | (ref)                                                  | 1.08x slower                                                      |

Benchmark hidden because not significant (2): xml_etree_parse, bench_mp_pool
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.03x