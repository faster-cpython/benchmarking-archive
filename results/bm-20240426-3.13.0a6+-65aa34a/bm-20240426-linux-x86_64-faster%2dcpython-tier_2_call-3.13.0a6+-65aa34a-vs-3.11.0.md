# Results vs. 3.11.0

- fork: faster-cpython
- ref: tier_2_call
- machine: linux-x86_64
- commit hash: 65aa34a
- commit date: 2024-04-26
- overall geometric mean: 1.07x faster
- HPT reliability: 99.24%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 267 ms: 1.01x slower                                                    |
| chameleon      | 6.70 ms                                                | 6.96 ms: 1.04x slower                                                   |
| docutils       | 2.66 sec                                               | 2.80 sec: 1.05x slower                                                  |
| tornado_http   | 98.1 ms                                                | 94.4 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                  | 1.01x slower                                                            |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 352 ms: 1.50x faster                                                    |
| async_tree_none_tg         | 491 ms                                                 | 330 ms: 1.49x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 436 ms: 1.44x faster                                                    |
| async_tree_io              | 1.29 sec                                               | 917 ms: 1.40x faster                                                    |
| async_tree_io_tg           | 1.29 sec                                               | 935 ms: 1.38x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 465 ms: 1.37x faster                                                    |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 609 ms: 1.25x faster                                                    |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 615 ms: 1.22x faster                                                    |
| Geometric mean             | (ref)                                                  | 1.38x faster                                                            |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 87.4 ms: 1.10x faster                                                   |
| pidigits       | 194 ms                                                 | 194 ms: 1.00x faster                                                    |
| Geometric mean | (ref)                                                  | 1.03x faster                                                            |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 134 ms: 1.05x faster                                                    |
| regex_effbot   | 3.51 ms                                                | 3.85 ms: 1.10x slower                                                   |
| regex_dna      | 205 ms                                                 | 232 ms: 1.14x slower                                                    |
| regex_v8       | 22.9 ms                                                | 26.3 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x slower                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                   |
| unpickle_pure_python | 242 us                                                 | 213 us: 1.13x faster                                                    |
| tomli_loads          | 2.30 sec                                               | 2.14 sec: 1.08x faster                                                  |
| pickle_pure_python   | 320 us                                                 | 299 us: 1.07x faster                                                    |
| json_loads           | 29.2 us                                                | 27.4 us: 1.06x faster                                                   |
| xml_etree_parse      | 164 ms                                                 | 159 ms: 1.03x faster                                                    |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                    |
| pickle_dict          | 34.6 us                                                | 34.4 us: 1.01x faster                                                   |
| unpickle_list        | 5.21 us                                                | 5.19 us: 1.00x faster                                                   |
| xml_etree_process    | 56.9 ms                                                | 60.2 ms: 1.06x slower                                                   |
| pickle               | 11.0 us                                                | 11.6 us: 1.06x slower                                                   |
| xml_etree_generate   | 81.1 ms                                                | 86.7 ms: 1.07x slower                                                   |
| unpickle             | 13.8 us                                                | 15.0 us: 1.08x slower                                                   |
| pickle_list          | 4.59 us                                                | 5.21 us: 1.14x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                            |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.11 ms: 1.18x slower                                                   |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                   |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|-----------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 51.1 ms: 1.05x faster                                                   |
| mako            | 10.7 ms                                                | 10.9 ms: 1.02x slower                                                   |
| django_template | 33.5 ms                                                | 34.4 ms: 1.03x slower                                                   |
| genshi_text     | 22.5 ms                                                | 23.2 ms: 1.03x slower                                                   |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                            |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240426-linux-x86_64-faster%2dcpython-tier_2_call-3.13.0a6+-65aa34a |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 163 us: 3.19x faster                                                    |
| generators                 | 74.9 ms                                                | 29.8 ms: 2.51x faster                                                   |
| asyncio_tcp                | 875 ms                                                 | 506 ms: 1.73x faster                                                    |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                                  |
| async_tree_none            | 528 ms                                                 | 352 ms: 1.50x faster                                                    |
| pylint                     | 476 ms                                                 | 318 ms: 1.50x faster                                                    |
| async_tree_none_tg         | 491 ms                                                 | 330 ms: 1.49x faster                                                    |
| async_tree_memoization_tg  | 626 ms                                                 | 436 ms: 1.44x faster                                                    |
| async_tree_io              | 1.29 sec                                               | 917 ms: 1.40x faster                                                    |
| comprehensions             | 23.6 us                                                | 16.9 us: 1.40x faster                                                   |
| async_tree_io_tg           | 1.29 sec                                               | 935 ms: 1.38x faster                                                    |
| async_tree_memoization     | 639 ms                                                 | 465 ms: 1.37x faster                                                    |
| json_dumps                 | 13.3 ms                                                | 10.6 ms: 1.26x faster                                                   |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 609 ms: 1.25x faster                                                    |
| deltablue                  | 3.92 ms                                                | 3.22 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 615 ms: 1.22x faster                                                    |
| coroutines                 | 27.0 ms                                                | 22.6 ms: 1.20x faster                                                   |
| chaos                      | 71.9 ms                                                | 60.3 ms: 1.19x faster                                                   |
| richards_super             | 61.9 ms                                                | 53.2 ms: 1.16x faster                                                   |
| raytrace                   | 309 ms                                                 | 267 ms: 1.16x faster                                                    |
| logging_silent             | 111 ns                                                 | 96.3 ns: 1.15x faster                                                   |
| unpickle_pure_python       | 242 us                                                 | 213 us: 1.13x faster                                                    |
| gc_traversal               | 4.01 ms                                                | 3.55 ms: 1.13x faster                                                   |
| hexiom                     | 6.89 ms                                                | 6.15 ms: 1.12x faster                                                   |
| sqlglot_parse              | 1.43 ms                                                | 1.29 ms: 1.11x faster                                                   |
| sqlglot_transpile          | 1.75 ms                                                | 1.59 ms: 1.10x faster                                                   |
| nbody                      | 96.0 ms                                                | 87.4 ms: 1.10x faster                                                   |
| sympy_sum                  | 169 ms                                                 | 155 ms: 1.09x faster                                                    |
| nqueens                    | 87.9 ms                                                | 81.6 ms: 1.08x faster                                                   |
| tomli_loads                | 2.30 sec                                               | 2.14 sec: 1.08x faster                                                  |
| sympy_str                  | 297 ms                                                 | 276 ms: 1.08x faster                                                    |
| pickle_pure_python         | 320 us                                                 | 299 us: 1.07x faster                                                    |
| djangocms                  | 33.5 us                                                | 31.4 us: 1.07x faster                                                   |
| logging_simple             | 6.22 us                                                | 5.83 us: 1.07x faster                                                   |
| json_loads                 | 29.2 us                                                | 27.4 us: 1.06x faster                                                   |
| sympy_integrate            | 21.5 ms                                                | 20.2 ms: 1.06x faster                                                   |
| logging_format             | 6.81 us                                                | 6.42 us: 1.06x faster                                                   |
| richards                   | 49.8 ms                                                | 47.0 ms: 1.06x faster                                                   |
| fannkuch                   | 405 ms                                                 | 383 ms: 1.06x faster                                                    |
| pathlib                    | 18.5 ms                                                | 17.6 ms: 1.05x faster                                                   |
| scimark_monte_carlo        | 70.7 ms                                                | 67.2 ms: 1.05x faster                                                   |
| regex_compile              | 141 ms                                                 | 134 ms: 1.05x faster                                                    |
| go                         | 149 ms                                                 | 142 ms: 1.05x faster                                                    |
| genshi_xml                 | 53.4 ms                                                | 51.1 ms: 1.05x faster                                                   |
| tornado_http               | 98.1 ms                                                | 94.4 ms: 1.04x faster                                                   |
| sympy_expand               | 484 ms                                                 | 467 ms: 1.04x faster                                                    |
| sqlglot_normalize          | 113 ms                                                 | 109 ms: 1.04x faster                                                    |
| xml_etree_parse            | 164 ms                                                 | 159 ms: 1.03x faster                                                    |
| deepcopy                   | 365 us                                                 | 355 us: 1.03x faster                                                    |
| deepcopy_memo              | 40.2 us                                                | 39.1 us: 1.03x faster                                                   |
| pprint_pformat             | 1.55 sec                                               | 1.52 sec: 1.02x faster                                                  |
| json                       | 5.24 ms                                                | 5.12 ms: 1.02x faster                                                   |
| crypto_pyaes               | 76.7 ms                                                | 75.2 ms: 1.02x faster                                                   |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                    |
| sqlglot_optimize           | 55.3 ms                                                | 54.7 ms: 1.01x faster                                                   |
| bench_thread_pool          | 834 us                                                 | 829 us: 1.01x faster                                                    |
| pprint_safe_repr           | 747 ms                                                 | 742 ms: 1.01x faster                                                    |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.01x faster                                                   |
| pickle_dict                | 34.6 us                                                | 34.4 us: 1.01x faster                                                   |
| unpickle_list              | 5.21 us                                                | 5.19 us: 1.00x faster                                                   |
| pidigits                   | 194 ms                                                 | 194 ms: 1.00x faster                                                    |
| mdp                        | 2.77 sec                                               | 2.79 sec: 1.01x slower                                                  |
| meteor_contest             | 109 ms                                                 | 110 ms: 1.01x slower                                                    |
| scimark_lu                 | 116 ms                                                 | 118 ms: 1.01x slower                                                    |
| 2to3                       | 264 ms                                                 | 267 ms: 1.01x slower                                                    |
| dulwich_log                | 64.6 ms                                                | 66.0 ms: 1.02x slower                                                   |
| mako                       | 10.7 ms                                                | 10.9 ms: 1.02x slower                                                   |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                                    |
| scimark_sor                | 121 ms                                                 | 124 ms: 1.02x slower                                                    |
| django_template            | 33.5 ms                                                | 34.4 ms: 1.03x slower                                                   |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.17 ms: 1.03x slower                                                   |
| genshi_text                | 22.5 ms                                                | 23.2 ms: 1.03x slower                                                   |
| chameleon                  | 6.70 ms                                                | 6.96 ms: 1.04x slower                                                   |
| thrift                     | 784 us                                                 | 816 us: 1.04x slower                                                    |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                   |
| docutils                   | 2.66 sec                                               | 2.80 sec: 1.05x slower                                                  |
| scimark_fft                | 345 ms                                                 | 365 ms: 1.06x slower                                                    |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                                   |
| xml_etree_process          | 56.9 ms                                                | 60.2 ms: 1.06x slower                                                   |
| pickle                     | 11.0 us                                                | 11.6 us: 1.06x slower                                                   |
| xml_etree_generate         | 81.1 ms                                                | 86.7 ms: 1.07x slower                                                   |
| pyflate                    | 434 ms                                                 | 464 ms: 1.07x slower                                                    |
| spectral_norm              | 108 ms                                                 | 116 ms: 1.07x slower                                                    |
| mypy2                      | 686 ms                                                 | 737 ms: 1.08x slower                                                    |
| unpickle                   | 13.8 us                                                | 15.0 us: 1.08x slower                                                   |
| regex_effbot               | 3.51 ms                                                | 3.85 ms: 1.10x slower                                                   |
| regex_dna                  | 205 ms                                                 | 232 ms: 1.14x slower                                                    |
| pickle_list                | 4.59 us                                                | 5.21 us: 1.14x slower                                                   |
| sqlite_synth               | 2.57 us                                                | 2.95 us: 1.15x slower                                                   |
| regex_v8                   | 22.9 ms                                                | 26.3 ms: 1.15x slower                                                   |
| async_generators           | 374 ms                                                 | 440 ms: 1.18x slower                                                    |
| python_startup_no_site     | 6.01 ms                                                | 7.11 ms: 1.18x slower                                                   |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                                   |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                   |
| telco                      | 6.86 ms                                                | 8.49 ms: 1.24x slower                                                   |
| coverage                   | 78.8 ms                                                | 98.6 ms: 1.25x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                            |

Benchmark hidden because not significant (5): deepcopy_reduce, float, dask, pycparser, html5lib
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 99.24% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x