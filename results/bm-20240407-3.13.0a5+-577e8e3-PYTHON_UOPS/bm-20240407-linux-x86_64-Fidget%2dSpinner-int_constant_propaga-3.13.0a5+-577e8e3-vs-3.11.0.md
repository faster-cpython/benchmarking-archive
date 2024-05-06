# Results vs. 3.11.0

- fork: Fidget-Spinner
- ref: int_constant_propaga
- machine: linux-x86_64
- commit hash: 577e8e3
- commit date: 2024-04-07
- overall geometric mean: 1.09x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 320 ms: 1.21x slower                                                             |
| chameleon      | 6.70 ms                                                | 7.95 ms: 1.19x slower                                                            |
| docutils       | 2.66 sec                                               | 3.18 sec: 1.19x slower                                                           |
| html5lib       | 64.8 ms                                                | 74.9 ms: 1.16x slower                                                            |
| tornado_http   | 98.1 ms                                                | 104 ms: 1.06x slower                                                             |
| Geometric mean | (ref)                                                  | 1.16x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 385 ms: 1.37x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 363 ms: 1.35x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 471 ms: 1.33x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 976 ms: 1.32x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 1.00 sec: 1.29x faster                                                           |
| async_tree_memoization     | 639 ms                                                 | 515 ms: 1.24x faster                                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 635 ms: 1.20x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 648 ms: 1.16x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.28x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 202 ms: 1.04x slower                                                             |
| float          | 78.9 ms                                                | 96.6 ms: 1.22x slower                                                            |
| nbody          | 96.0 ms                                                | 134 ms: 1.40x slower                                                             |
| Geometric mean | (ref)                                                  | 1.21x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.78 ms: 1.08x slower                                                            |
| regex_dna      | 205 ms                                                 | 227 ms: 1.11x slower                                                             |
| regex_v8       | 22.9 ms                                                | 26.9 ms: 1.18x slower                                                            |
| regex_compile  | 141 ms                                                 | 208 ms: 1.47x slower                                                             |
| Geometric mean | (ref)                                                  | 1.20x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.8 ms: 1.23x faster                                                            |
| json_loads           | 29.2 us                                                | 28.5 us: 1.02x faster                                                            |
| pickle_pure_python   | 320 us                                                 | 318 us: 1.01x faster                                                             |
| unpickle_list        | 5.21 us                                                | 5.23 us: 1.00x slower                                                            |
| pickle_dict          | 34.6 us                                                | 34.8 us: 1.01x slower                                                            |
| xml_etree_iterparse  | 108 ms                                                 | 115 ms: 1.06x slower                                                             |
| pickle               | 11.0 us                                                | 12.0 us: 1.09x slower                                                            |
| pickle_list          | 4.59 us                                                | 5.02 us: 1.09x slower                                                            |
| xml_etree_process    | 56.9 ms                                                | 66.2 ms: 1.16x slower                                                            |
| tomli_loads          | 2.30 sec                                               | 2.72 sec: 1.18x slower                                                           |
| xml_etree_generate   | 81.1 ms                                                | 98.1 ms: 1.21x slower                                                            |
| unpickle             | 13.8 us                                                | 16.7 us: 1.21x slower                                                            |
| unpickle_pure_python | 242 us                                                 | 333 us: 1.38x slower                                                             |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                                     |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.7 ms: 1.24x slower                                                            |
| python_startup_no_site | 6.01 ms                                                | 9.09 ms: 1.51x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.37x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_text    | 22.5 ms                                                | 26.1 ms: 1.16x slower                                                            |
| genshi_xml     | 53.4 ms                                                | 62.9 ms: 1.18x slower                                                            |
| mako           | 10.7 ms                                                | 14.3 ms: 1.34x slower                                                            |
| Geometric mean | (ref)                                                  | 1.22x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240407-linux-x86_64-Fidget%2dSpinner-int_constant_propaga-3.13.0a5+-577e8e3 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 127 us: 4.10x faster                                                             |
| generators                 | 74.9 ms                                                | 30.3 ms: 2.47x faster                                                            |
| asyncio_tcp                | 875 ms                                                 | 518 ms: 1.69x faster                                                             |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                                           |
| pylint                     | 476 ms                                                 | 312 ms: 1.52x faster                                                             |
| async_tree_none            | 528 ms                                                 | 385 ms: 1.37x faster                                                             |
| async_tree_none_tg         | 491 ms                                                 | 363 ms: 1.35x faster                                                             |
| async_tree_memoization_tg  | 626 ms                                                 | 471 ms: 1.33x faster                                                             |
| async_tree_io              | 1.29 sec                                               | 976 ms: 1.32x faster                                                             |
| async_tree_io_tg           | 1.29 sec                                               | 1.00 sec: 1.29x faster                                                           |
| async_tree_memoization     | 639 ms                                                 | 515 ms: 1.24x faster                                                             |
| json_dumps                 | 13.3 ms                                                | 10.8 ms: 1.23x faster                                                            |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 635 ms: 1.20x faster                                                             |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 648 ms: 1.16x faster                                                             |
| coroutines                 | 27.0 ms                                                | 24.3 ms: 1.11x faster                                                            |
| json_loads                 | 29.2 us                                                | 28.5 us: 1.02x faster                                                            |
| pickle_pure_python         | 320 us                                                 | 318 us: 1.01x faster                                                             |
| unpickle_list              | 5.21 us                                                | 5.23 us: 1.00x slower                                                            |
| pickle_dict                | 34.6 us                                                | 34.8 us: 1.01x slower                                                            |
| gc_traversal               | 4.01 ms                                                | 4.03 ms: 1.01x slower                                                            |
| logging_silent             | 111 ns                                                 | 112 ns: 1.01x slower                                                             |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.03x slower                                                             |
| json                       | 5.24 ms                                                | 5.41 ms: 1.03x slower                                                            |
| pidigits                   | 194 ms                                                 | 202 ms: 1.04x slower                                                             |
| deepcopy_reduce            | 3.22 us                                                | 3.34 us: 1.04x slower                                                            |
| mdp                        | 2.77 sec                                               | 2.94 sec: 1.06x slower                                                           |
| dask                       | 365 ms                                                 | 388 ms: 1.06x slower                                                             |
| tornado_http               | 98.1 ms                                                | 104 ms: 1.06x slower                                                             |
| xml_etree_iterparse        | 108 ms                                                 | 115 ms: 1.06x slower                                                             |
| logging_simple             | 6.22 us                                                | 6.61 us: 1.06x slower                                                            |
| comprehensions             | 23.6 us                                                | 25.3 us: 1.07x slower                                                            |
| logging_format             | 6.81 us                                                | 7.32 us: 1.07x slower                                                            |
| thrift                     | 784 us                                                 | 843 us: 1.07x slower                                                             |
| deepcopy                   | 365 us                                                 | 394 us: 1.08x slower                                                             |
| regex_effbot               | 3.51 ms                                                | 3.78 ms: 1.08x slower                                                            |
| sympy_sum                  | 169 ms                                                 | 183 ms: 1.08x slower                                                             |
| sqlglot_transpile          | 1.75 ms                                                | 1.90 ms: 1.09x slower                                                            |
| sqlglot_parse              | 1.43 ms                                                | 1.56 ms: 1.09x slower                                                            |
| pickle                     | 11.0 us                                                | 12.0 us: 1.09x slower                                                            |
| deltablue                  | 3.92 ms                                                | 4.28 ms: 1.09x slower                                                            |
| pickle_list                | 4.59 us                                                | 5.02 us: 1.09x slower                                                            |
| bench_thread_pool          | 834 us                                                 | 917 us: 1.10x slower                                                             |
| regex_dna                  | 205 ms                                                 | 227 ms: 1.11x slower                                                             |
| pathlib                    | 18.5 ms                                                | 20.6 ms: 1.11x slower                                                            |
| gunicorn                   | 1.20 ms                                                | 1.35 ms: 1.13x slower                                                            |
| aiohttp                    | 1.12 ms                                                | 1.26 ms: 1.13x slower                                                            |
| sympy_str                  | 297 ms                                                 | 337 ms: 1.13x slower                                                             |
| raytrace                   | 309 ms                                                 | 350 ms: 1.14x slower                                                             |
| sympy_integrate            | 21.5 ms                                                | 24.5 ms: 1.14x slower                                                            |
| chaos                      | 71.9 ms                                                | 82.2 ms: 1.14x slower                                                            |
| sympy_expand               | 484 ms                                                 | 556 ms: 1.15x slower                                                             |
| html5lib                   | 64.8 ms                                                | 74.9 ms: 1.16x slower                                                            |
| genshi_text                | 22.5 ms                                                | 26.1 ms: 1.16x slower                                                            |
| xml_etree_process          | 56.9 ms                                                | 66.2 ms: 1.16x slower                                                            |
| richards_super             | 61.9 ms                                                | 72.2 ms: 1.17x slower                                                            |
| pycparser                  | 1.19 sec                                               | 1.39 sec: 1.17x slower                                                           |
| regex_v8                   | 22.9 ms                                                | 26.9 ms: 1.18x slower                                                            |
| genshi_xml                 | 53.4 ms                                                | 62.9 ms: 1.18x slower                                                            |
| sqlglot_normalize          | 113 ms                                                 | 133 ms: 1.18x slower                                                             |
| tomli_loads                | 2.30 sec                                               | 2.72 sec: 1.18x slower                                                           |
| dulwich_log                | 64.6 ms                                                | 76.5 ms: 1.18x slower                                                            |
| chameleon                  | 6.70 ms                                                | 7.95 ms: 1.19x slower                                                            |
| deepcopy_memo              | 40.2 us                                                | 47.8 us: 1.19x slower                                                            |
| docutils                   | 2.66 sec                                               | 3.18 sec: 1.19x slower                                                           |
| mypy2                      | 686 ms                                                 | 827 ms: 1.21x slower                                                             |
| xml_etree_generate         | 81.1 ms                                                | 98.1 ms: 1.21x slower                                                            |
| unpickle                   | 13.8 us                                                | 16.7 us: 1.21x slower                                                            |
| 2to3                       | 264 ms                                                 | 320 ms: 1.21x slower                                                             |
| float                      | 78.9 ms                                                | 96.6 ms: 1.22x slower                                                            |
| sqlite_synth               | 2.57 us                                                | 3.15 us: 1.23x slower                                                            |
| create_gc_cycles           | 1.43 ms                                                | 1.76 ms: 1.23x slower                                                            |
| meteor_contest             | 109 ms                                                 | 134 ms: 1.23x slower                                                             |
| python_startup             | 8.56 ms                                                | 10.7 ms: 1.24x slower                                                            |
| sqlglot_optimize           | 55.3 ms                                                | 68.8 ms: 1.24x slower                                                            |
| coverage                   | 78.8 ms                                                | 98.1 ms: 1.25x slower                                                            |
| crypto_pyaes               | 76.7 ms                                                | 96.7 ms: 1.26x slower                                                            |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 6.38 ms: 1.27x slower                                                            |
| fannkuch                   | 405 ms                                                 | 524 ms: 1.29x slower                                                             |
| async_generators           | 374 ms                                                 | 486 ms: 1.30x slower                                                             |
| richards                   | 49.8 ms                                                | 64.8 ms: 1.30x slower                                                            |
| scimark_sor                | 121 ms                                                 | 160 ms: 1.32x slower                                                             |
| go                         | 149 ms                                                 | 198 ms: 1.33x slower                                                             |
| mako                       | 10.7 ms                                                | 14.3 ms: 1.34x slower                                                            |
| scimark_fft                | 345 ms                                                 | 470 ms: 1.36x slower                                                             |
| scimark_monte_carlo        | 70.7 ms                                                | 97.3 ms: 1.38x slower                                                            |
| unpickle_pure_python       | 242 us                                                 | 333 us: 1.38x slower                                                             |
| nbody                      | 96.0 ms                                                | 134 ms: 1.40x slower                                                             |
| spectral_norm              | 108 ms                                                 | 153 ms: 1.42x slower                                                             |
| telco                      | 6.86 ms                                                | 9.89 ms: 1.44x slower                                                            |
| regex_compile              | 141 ms                                                 | 208 ms: 1.47x slower                                                             |
| pyflate                    | 434 ms                                                 | 641 ms: 1.48x slower                                                             |
| hexiom                     | 6.89 ms                                                | 10.4 ms: 1.51x slower                                                            |
| python_startup_no_site     | 6.01 ms                                                | 9.09 ms: 1.51x slower                                                            |
| scimark_lu                 | 116 ms                                                 | 178 ms: 1.53x slower                                                             |
| pprint_pformat             | 1.55 sec                                               | 2.40 sec: 1.54x slower                                                           |
| pprint_safe_repr           | 747 ms                                                 | 1.18 sec: 1.57x slower                                                           |
| nqueens                    | 87.9 ms                                                | 139 ms: 1.59x slower                                                             |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                                     |

Benchmark hidden because not significant (2): xml_etree_parse, bench_mp_pool
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.03x