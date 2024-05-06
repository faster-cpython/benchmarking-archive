# Results vs. 3.11.0

- fork: faster-cpython
- ref: return_gen_tier_2
- machine: linux-x86_64
- commit hash: fad1c67
- commit date: 2024-04-23
- overall geometric mean: 1.03x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 301 ms: 1.14x slower                                                          |
| chameleon      | 6.70 ms                                                | 7.62 ms: 1.14x slower                                                         |
| docutils       | 2.66 sec                                               | 3.07 sec: 1.15x slower                                                        |
| html5lib       | 64.8 ms                                                | 72.4 ms: 1.12x slower                                                         |
| tornado_http   | 98.1 ms                                                | 102 ms: 1.04x slower                                                          |
| Geometric mean | (ref)                                                  | 1.12x slower                                                                  |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 373 ms: 1.41x faster                                                          |
| async_tree_none_tg         | 491 ms                                                 | 351 ms: 1.40x faster                                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 459 ms: 1.37x faster                                                          |
| async_tree_io_tg           | 1.29 sec                                               | 969 ms: 1.34x faster                                                          |
| async_tree_io              | 1.29 sec                                               | 966 ms: 1.33x faster                                                          |
| async_tree_memoization     | 639 ms                                                 | 499 ms: 1.28x faster                                                          |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 623 ms: 1.22x faster                                                          |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 632 ms: 1.18x faster                                                          |
| Geometric mean             | (ref)                                                  | 1.31x faster                                                                  |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| pidigits       | 194 ms                                                 | 218 ms: 1.12x slower                                                          |
| float          | 78.9 ms                                                | 89.3 ms: 1.13x slower                                                         |
| nbody          | 96.0 ms                                                | 120 ms: 1.25x slower                                                          |
| Geometric mean | (ref)                                                  | 1.17x slower                                                                  |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| regex_effbot   | 3.51 ms                                                | 3.69 ms: 1.05x slower                                                         |
| regex_v8       | 22.9 ms                                                | 25.4 ms: 1.11x slower                                                         |
| regex_dna      | 205 ms                                                 | 228 ms: 1.12x slower                                                          |
| regex_compile  | 141 ms                                                 | 179 ms: 1.26x slower                                                          |
| Geometric mean | (ref)                                                  | 1.13x slower                                                                  |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.8 ms: 1.23x faster                                                         |
| xml_etree_parse      | 164 ms                                                 | 154 ms: 1.06x faster                                                          |
| json_loads           | 29.2 us                                                | 27.5 us: 1.06x faster                                                         |
| pickle_pure_python   | 320 us                                                 | 314 us: 1.02x faster                                                          |
| unpickle_list        | 5.21 us                                                | 5.26 us: 1.01x slower                                                         |
| pickle_dict          | 34.6 us                                                | 35.0 us: 1.01x slower                                                         |
| xml_etree_iterparse  | 108 ms                                                 | 110 ms: 1.02x slower                                                          |
| pickle               | 11.0 us                                                | 11.9 us: 1.09x slower                                                         |
| tomli_loads          | 2.30 sec                                               | 2.53 sec: 1.10x slower                                                        |
| xml_etree_process    | 56.9 ms                                                | 64.2 ms: 1.13x slower                                                         |
| pickle_list          | 4.59 us                                                | 5.19 us: 1.13x slower                                                         |
| unpickle             | 13.8 us                                                | 15.7 us: 1.13x slower                                                         |
| xml_etree_generate   | 81.1 ms                                                | 93.3 ms: 1.15x slower                                                         |
| unpickle_pure_python | 242 us                                                 | 283 us: 1.17x slower                                                          |
| Geometric mean       | (ref)                                                  | 1.04x slower                                                                  |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.15 ms: 1.19x slower                                                         |
| python_startup         | 8.56 ms                                                | 10.6 ms: 1.23x slower                                                         |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                                  |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 58.7 ms: 1.10x slower                                                         |
| genshi_text     | 22.5 ms                                                | 25.6 ms: 1.14x slower                                                         |
| django_template | 33.5 ms                                                | 39.8 ms: 1.19x slower                                                         |
| mako            | 10.7 ms                                                | 13.8 ms: 1.29x slower                                                         |
| Geometric mean  | (ref)                                                  | 1.18x slower                                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240423-linux-x86_64-faster%2dcpython-return_gen_tier_2-3.13.0a6+-fad1c67 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 123 us: 4.21x faster                                                          |
| generators                 | 74.9 ms                                                | 30.2 ms: 2.48x faster                                                         |
| asyncio_tcp                | 875 ms                                                 | 517 ms: 1.69x faster                                                          |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.87 sec: 1.67x faster                                                        |
| async_tree_none            | 528 ms                                                 | 373 ms: 1.41x faster                                                          |
| async_tree_none_tg         | 491 ms                                                 | 351 ms: 1.40x faster                                                          |
| pylint                     | 476 ms                                                 | 343 ms: 1.39x faster                                                          |
| async_tree_memoization_tg  | 626 ms                                                 | 459 ms: 1.37x faster                                                          |
| async_tree_io_tg           | 1.29 sec                                               | 969 ms: 1.34x faster                                                          |
| async_tree_io              | 1.29 sec                                               | 966 ms: 1.33x faster                                                          |
| async_tree_memoization     | 639 ms                                                 | 499 ms: 1.28x faster                                                          |
| json_dumps                 | 13.3 ms                                                | 10.8 ms: 1.23x faster                                                         |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 623 ms: 1.22x faster                                                          |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 632 ms: 1.18x faster                                                          |
| coroutines                 | 27.0 ms                                                | 22.8 ms: 1.18x faster                                                         |
| gc_traversal               | 4.01 ms                                                | 3.64 ms: 1.10x faster                                                         |
| xml_etree_parse            | 164 ms                                                 | 154 ms: 1.06x faster                                                          |
| json_loads                 | 29.2 us                                                | 27.5 us: 1.06x faster                                                         |
| logging_silent             | 111 ns                                                 | 105 ns: 1.06x faster                                                          |
| comprehensions             | 23.6 us                                                | 22.6 us: 1.04x faster                                                         |
| djangocms                  | 33.5 us                                                | 32.7 us: 1.03x faster                                                         |
| pickle_pure_python         | 320 us                                                 | 314 us: 1.02x faster                                                          |
| pathlib                    | 18.5 ms                                                | 18.2 ms: 1.02x faster                                                         |
| mdp                        | 2.77 sec                                               | 2.79 sec: 1.01x slower                                                        |
| unpickle_list              | 5.21 us                                                | 5.26 us: 1.01x slower                                                         |
| asyncio_websockets         | 550 ms                                                 | 555 ms: 1.01x slower                                                          |
| pickle_dict                | 34.6 us                                                | 35.0 us: 1.01x slower                                                         |
| xml_etree_iterparse        | 108 ms                                                 | 110 ms: 1.02x slower                                                          |
| deepcopy_reduce            | 3.22 us                                                | 3.28 us: 1.02x slower                                                         |
| logging_simple             | 6.22 us                                                | 6.40 us: 1.03x slower                                                         |
| deepcopy                   | 365 us                                                 | 376 us: 1.03x slower                                                          |
| sqlglot_transpile          | 1.75 ms                                                | 1.80 ms: 1.03x slower                                                         |
| sqlglot_parse              | 1.43 ms                                                | 1.48 ms: 1.03x slower                                                         |
| raytrace                   | 309 ms                                                 | 319 ms: 1.03x slower                                                          |
| tornado_http               | 98.1 ms                                                | 102 ms: 1.04x slower                                                          |
| dask                       | 365 ms                                                 | 382 ms: 1.05x slower                                                          |
| thrift                     | 784 us                                                 | 821 us: 1.05x slower                                                          |
| sympy_sum                  | 169 ms                                                 | 177 ms: 1.05x slower                                                          |
| logging_format             | 6.81 us                                                | 7.17 us: 1.05x slower                                                         |
| regex_effbot               | 3.51 ms                                                | 3.69 ms: 1.05x slower                                                         |
| deltablue                  | 3.92 ms                                                | 4.15 ms: 1.06x slower                                                         |
| bench_thread_pool          | 834 us                                                 | 883 us: 1.06x slower                                                          |
| pycparser                  | 1.19 sec                                               | 1.27 sec: 1.07x slower                                                        |
| sympy_integrate            | 21.5 ms                                                | 23.1 ms: 1.08x slower                                                         |
| sympy_str                  | 297 ms                                                 | 321 ms: 1.08x slower                                                          |
| pickle                     | 11.0 us                                                | 11.9 us: 1.09x slower                                                         |
| deepcopy_memo              | 40.2 us                                                | 43.8 us: 1.09x slower                                                         |
| chaos                      | 71.9 ms                                                | 78.4 ms: 1.09x slower                                                         |
| sqlglot_normalize          | 113 ms                                                 | 123 ms: 1.10x slower                                                          |
| meteor_contest             | 109 ms                                                 | 119 ms: 1.10x slower                                                          |
| genshi_xml                 | 53.4 ms                                                | 58.7 ms: 1.10x slower                                                         |
| tomli_loads                | 2.30 sec                                               | 2.53 sec: 1.10x slower                                                        |
| sympy_expand               | 484 ms                                                 | 534 ms: 1.10x slower                                                          |
| regex_v8                   | 22.9 ms                                                | 25.4 ms: 1.11x slower                                                         |
| gunicorn                   | 1.20 ms                                                | 1.33 ms: 1.11x slower                                                         |
| regex_dna                  | 205 ms                                                 | 228 ms: 1.12x slower                                                          |
| richards                   | 49.8 ms                                                | 55.6 ms: 1.12x slower                                                         |
| html5lib                   | 64.8 ms                                                | 72.4 ms: 1.12x slower                                                         |
| aiohttp                    | 1.12 ms                                                | 1.25 ms: 1.12x slower                                                         |
| pidigits                   | 194 ms                                                 | 218 ms: 1.12x slower                                                          |
| xml_etree_process          | 56.9 ms                                                | 64.2 ms: 1.13x slower                                                         |
| float                      | 78.9 ms                                                | 89.3 ms: 1.13x slower                                                         |
| pickle_list                | 4.59 us                                                | 5.19 us: 1.13x slower                                                         |
| unpickle                   | 13.8 us                                                | 15.7 us: 1.13x slower                                                         |
| genshi_text                | 22.5 ms                                                | 25.6 ms: 1.14x slower                                                         |
| chameleon                  | 6.70 ms                                                | 7.62 ms: 1.14x slower                                                         |
| 2to3                       | 264 ms                                                 | 301 ms: 1.14x slower                                                          |
| dulwich_log                | 64.6 ms                                                | 73.8 ms: 1.14x slower                                                         |
| sqlglot_optimize           | 55.3 ms                                                | 63.3 ms: 1.15x slower                                                         |
| xml_etree_generate         | 81.1 ms                                                | 93.3 ms: 1.15x slower                                                         |
| docutils                   | 2.66 sec                                               | 3.07 sec: 1.15x slower                                                        |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.85 ms: 1.16x slower                                                         |
| sqlite_synth               | 2.57 us                                                | 3.00 us: 1.17x slower                                                         |
| unpickle_pure_python       | 242 us                                                 | 283 us: 1.17x slower                                                          |
| mypy2                      | 686 ms                                                 | 807 ms: 1.18x slower                                                          |
| django_template            | 33.5 ms                                                | 39.8 ms: 1.19x slower                                                         |
| python_startup_no_site     | 6.01 ms                                                | 7.15 ms: 1.19x slower                                                         |
| nqueens                    | 87.9 ms                                                | 105 ms: 1.20x slower                                                          |
| crypto_pyaes               | 76.7 ms                                                | 92.0 ms: 1.20x slower                                                         |
| fannkuch                   | 405 ms                                                 | 487 ms: 1.20x slower                                                          |
| scimark_monte_carlo        | 70.7 ms                                                | 86.0 ms: 1.22x slower                                                         |
| scimark_sor                | 121 ms                                                 | 149 ms: 1.23x slower                                                          |
| create_gc_cycles           | 1.43 ms                                                | 1.76 ms: 1.23x slower                                                         |
| python_startup             | 8.56 ms                                                | 10.6 ms: 1.23x slower                                                         |
| go                         | 149 ms                                                 | 185 ms: 1.24x slower                                                          |
| pprint_pformat             | 1.55 sec                                               | 1.94 sec: 1.25x slower                                                        |
| nbody                      | 96.0 ms                                                | 120 ms: 1.25x slower                                                          |
| pprint_safe_repr           | 747 ms                                                 | 939 ms: 1.26x slower                                                          |
| coverage                   | 78.8 ms                                                | 99.3 ms: 1.26x slower                                                         |
| scimark_fft                | 345 ms                                                 | 436 ms: 1.26x slower                                                          |
| regex_compile              | 141 ms                                                 | 179 ms: 1.26x slower                                                          |
| spectral_norm              | 108 ms                                                 | 138 ms: 1.28x slower                                                          |
| async_generators           | 374 ms                                                 | 478 ms: 1.28x slower                                                          |
| mako                       | 10.7 ms                                                | 13.8 ms: 1.29x slower                                                         |
| telco                      | 6.86 ms                                                | 9.13 ms: 1.33x slower                                                         |
| pyflate                    | 434 ms                                                 | 588 ms: 1.36x slower                                                          |
| hexiom                     | 6.89 ms                                                | 9.45 ms: 1.37x slower                                                         |
| scimark_lu                 | 116 ms                                                 | 163 ms: 1.40x slower                                                          |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                                  |

Benchmark hidden because not significant (3): richards_super, bench_mp_pool, json
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.04x