# Results vs. 3.11.0

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: 8eee1b4
- commit date: 2024-04-02
- overall geometric mean: 1.04x faster
- HPT reliability: 81.89%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 279 ms: 1.06x slower                                              |
| chameleon      | 6.70 ms                                                | 6.88 ms: 1.03x slower                                             |
| docutils       | 2.66 sec                                               | 2.91 sec: 1.09x slower                                            |
| html5lib       | 64.8 ms                                                | 65.7 ms: 1.01x slower                                             |
| tornado_http   | 98.1 ms                                                | 95.7 ms: 1.02x faster                                             |
| Geometric mean | (ref)                                                  | 1.03x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 353 ms: 1.50x faster                                              |
| async_tree_none_tg         | 491 ms                                                 | 334 ms: 1.47x faster                                              |
| async_tree_memoization_tg  | 626 ms                                                 | 444 ms: 1.41x faster                                              |
| async_tree_memoization     | 639 ms                                                 | 455 ms: 1.41x faster                                              |
| async_tree_io              | 1.29 sec                                               | 933 ms: 1.38x faster                                              |
| async_tree_io_tg           | 1.29 sec                                               | 945 ms: 1.37x faster                                              |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 602 ms: 1.26x faster                                              |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 609 ms: 1.23x faster                                              |
| Geometric mean             | (ref)                                                  | 1.38x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 91.9 ms: 1.04x faster                                             |
| float          | 78.9 ms                                                | 78.1 ms: 1.01x faster                                             |
| pidigits       | 194 ms                                                 | 194 ms: 1.00x faster                                              |
| Geometric mean | (ref)                                                  | 1.02x faster                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 145 ms: 1.03x slower                                              |
| regex_effbot   | 3.51 ms                                                | 3.75 ms: 1.07x slower                                             |
| regex_dna      | 205 ms                                                 | 233 ms: 1.14x slower                                              |
| regex_v8       | 22.9 ms                                                | 26.1 ms: 1.14x slower                                             |
| Geometric mean | (ref)                                                  | 1.09x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                             |
| tomli_loads          | 2.30 sec                                               | 2.07 sec: 1.11x faster                                            |
| pickle_pure_python   | 320 us                                                 | 304 us: 1.05x faster                                              |
| json_loads           | 29.2 us                                                | 28.6 us: 1.02x faster                                             |
| pickle_dict          | 34.6 us                                                | 34.1 us: 1.01x faster                                             |
| xml_etree_parse      | 164 ms                                                 | 162 ms: 1.01x faster                                              |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                              |
| unpickle_pure_python | 242 us                                                 | 240 us: 1.01x faster                                              |
| unpickle_list        | 5.21 us                                                | 5.24 us: 1.01x slower                                             |
| xml_etree_process    | 56.9 ms                                                | 60.6 ms: 1.06x slower                                             |
| pickle               | 11.0 us                                                | 11.8 us: 1.07x slower                                             |
| xml_etree_generate   | 81.1 ms                                                | 87.4 ms: 1.08x slower                                             |
| pickle_list          | 4.59 us                                                | 5.06 us: 1.10x slower                                             |
| unpickle             | 13.8 us                                                | 15.9 us: 1.15x slower                                             |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 11.1 ms: 1.30x slower                                             |
| python_startup_no_site | 6.01 ms                                                | 9.55 ms: 1.59x slower                                             |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml     | 53.4 ms                                                | 53.2 ms: 1.01x faster                                             |
| mako           | 10.7 ms                                                | 10.9 ms: 1.02x slower                                             |
| genshi_text    | 22.5 ms                                                | 24.2 ms: 1.07x slower                                             |
| Geometric mean | (ref)                                                  | 1.03x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240402-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-8eee1b4 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 113 us: 4.58x faster                                              |
| generators                 | 74.9 ms                                                | 29.7 ms: 2.52x faster                                             |
| asyncio_tcp                | 875 ms                                                 | 513 ms: 1.71x faster                                              |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.86 sec: 1.67x faster                                            |
| pylint                     | 476 ms                                                 | 298 ms: 1.60x faster                                              |
| async_tree_none            | 528 ms                                                 | 353 ms: 1.50x faster                                              |
| async_tree_none_tg         | 491 ms                                                 | 334 ms: 1.47x faster                                              |
| async_tree_memoization_tg  | 626 ms                                                 | 444 ms: 1.41x faster                                              |
| async_tree_memoization     | 639 ms                                                 | 455 ms: 1.41x faster                                              |
| async_tree_io              | 1.29 sec                                               | 933 ms: 1.38x faster                                              |
| async_tree_io_tg           | 1.29 sec                                               | 945 ms: 1.37x faster                                              |
| comprehensions             | 23.6 us                                                | 17.8 us: 1.33x faster                                             |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 602 ms: 1.26x faster                                              |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 609 ms: 1.23x faster                                              |
| coroutines                 | 27.0 ms                                                | 22.1 ms: 1.22x faster                                             |
| richards_super             | 61.9 ms                                                | 53.1 ms: 1.17x faster                                             |
| chaos                      | 71.9 ms                                                | 61.7 ms: 1.17x faster                                             |
| tomli_loads                | 2.30 sec                                               | 2.07 sec: 1.11x faster                                            |
| raytrace                   | 309 ms                                                 | 278 ms: 1.11x faster                                              |
| logging_silent             | 111 ns                                                 | 101 ns: 1.10x faster                                              |
| sqlglot_parse              | 1.43 ms                                                | 1.32 ms: 1.08x faster                                             |
| sqlglot_transpile          | 1.75 ms                                                | 1.63 ms: 1.07x faster                                             |
| richards                   | 49.8 ms                                                | 46.7 ms: 1.07x faster                                             |
| gc_traversal               | 4.01 ms                                                | 3.79 ms: 1.06x faster                                             |
| deepcopy_memo              | 40.2 us                                                | 38.0 us: 1.06x faster                                             |
| pickle_pure_python         | 320 us                                                 | 304 us: 1.05x faster                                              |
| deltablue                  | 3.92 ms                                                | 3.76 ms: 1.04x faster                                             |
| nbody                      | 96.0 ms                                                | 91.9 ms: 1.04x faster                                             |
| deepcopy                   | 365 us                                                 | 353 us: 1.04x faster                                              |
| logging_format             | 6.81 us                                                | 6.59 us: 1.03x faster                                             |
| scimark_monte_carlo        | 70.7 ms                                                | 68.7 ms: 1.03x faster                                             |
| mdp                        | 2.77 sec                                               | 2.70 sec: 1.03x faster                                            |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 4.89 ms: 1.03x faster                                             |
| tornado_http               | 98.1 ms                                                | 95.7 ms: 1.02x faster                                             |
| logging_simple             | 6.22 us                                                | 6.08 us: 1.02x faster                                             |
| json_loads                 | 29.2 us                                                | 28.6 us: 1.02x faster                                             |
| scimark_fft                | 345 ms                                                 | 338 ms: 1.02x faster                                              |
| crypto_pyaes               | 76.7 ms                                                | 75.4 ms: 1.02x faster                                             |
| fannkuch                   | 405 ms                                                 | 399 ms: 1.02x faster                                              |
| pickle_dict                | 34.6 us                                                | 34.1 us: 1.01x faster                                             |
| xml_etree_parse            | 164 ms                                                 | 162 ms: 1.01x faster                                              |
| float                      | 78.9 ms                                                | 78.1 ms: 1.01x faster                                             |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                              |
| unpickle_pure_python       | 242 us                                                 | 240 us: 1.01x faster                                              |
| sympy_sum                  | 169 ms                                                 | 168 ms: 1.01x faster                                              |
| sympy_str                  | 297 ms                                                 | 295 ms: 1.01x faster                                              |
| genshi_xml                 | 53.4 ms                                                | 53.2 ms: 1.01x faster                                             |
| pidigits                   | 194 ms                                                 | 194 ms: 1.00x faster                                              |
| unpickle_list              | 5.21 us                                                | 5.24 us: 1.01x slower                                             |
| hexiom                     | 6.89 ms                                                | 6.93 ms: 1.01x slower                                             |
| go                         | 149 ms                                                 | 150 ms: 1.01x slower                                              |
| deepcopy_reduce            | 3.22 us                                                | 3.24 us: 1.01x slower                                             |
| nqueens                    | 87.9 ms                                                | 89.0 ms: 1.01x slower                                             |
| html5lib                   | 64.8 ms                                                | 65.7 ms: 1.01x slower                                             |
| mako                       | 10.7 ms                                                | 10.9 ms: 1.02x slower                                             |
| sympy_integrate            | 21.5 ms                                                | 21.9 ms: 1.02x slower                                             |
| pycparser                  | 1.19 sec                                               | 1.21 sec: 1.02x slower                                            |
| bench_thread_pool          | 834 us                                                 | 854 us: 1.02x slower                                              |
| sympy_expand               | 484 ms                                                 | 496 ms: 1.02x slower                                              |
| asyncio_websockets         | 550 ms                                                 | 564 ms: 1.03x slower                                              |
| chameleon                  | 6.70 ms                                                | 6.88 ms: 1.03x slower                                             |
| meteor_contest             | 109 ms                                                 | 112 ms: 1.03x slower                                              |
| regex_compile              | 141 ms                                                 | 145 ms: 1.03x slower                                              |
| pathlib                    | 18.5 ms                                                | 19.1 ms: 1.03x slower                                             |
| json                       | 5.24 ms                                                | 5.39 ms: 1.03x slower                                             |
| dask                       | 365 ms                                                 | 377 ms: 1.03x slower                                              |
| sqlglot_optimize           | 55.3 ms                                                | 57.6 ms: 1.04x slower                                             |
| spectral_norm              | 108 ms                                                 | 113 ms: 1.05x slower                                              |
| thrift                     | 784 us                                                 | 827 us: 1.05x slower                                              |
| 2to3                       | 264 ms                                                 | 279 ms: 1.06x slower                                              |
| xml_etree_process          | 56.9 ms                                                | 60.6 ms: 1.06x slower                                             |
| regex_effbot               | 3.51 ms                                                | 3.75 ms: 1.07x slower                                             |
| pickle                     | 11.0 us                                                | 11.8 us: 1.07x slower                                             |
| genshi_text                | 22.5 ms                                                | 24.2 ms: 1.07x slower                                             |
| scimark_sor                | 121 ms                                                 | 130 ms: 1.08x slower                                              |
| xml_etree_generate         | 81.1 ms                                                | 87.4 ms: 1.08x slower                                             |
| gunicorn                   | 1.20 ms                                                | 1.30 ms: 1.08x slower                                             |
| aiohttp                    | 1.12 ms                                                | 1.21 ms: 1.08x slower                                             |
| docutils                   | 2.66 sec                                               | 2.91 sec: 1.09x slower                                            |
| pickle_list                | 4.59 us                                                | 5.06 us: 1.10x slower                                             |
| dulwich_log                | 64.6 ms                                                | 71.3 ms: 1.10x slower                                             |
| pyflate                    | 434 ms                                                 | 481 ms: 1.11x slower                                              |
| sqlite_synth               | 2.57 us                                                | 2.89 us: 1.12x slower                                             |
| scimark_lu                 | 116 ms                                                 | 131 ms: 1.13x slower                                              |
| regex_dna                  | 205 ms                                                 | 233 ms: 1.14x slower                                              |
| regex_v8                   | 22.9 ms                                                | 26.1 ms: 1.14x slower                                             |
| mypy2                      | 686 ms                                                 | 788 ms: 1.15x slower                                              |
| unpickle                   | 13.8 us                                                | 15.9 us: 1.15x slower                                             |
| create_gc_cycles           | 1.43 ms                                                | 1.75 ms: 1.22x slower                                             |
| async_generators           | 374 ms                                                 | 459 ms: 1.23x slower                                              |
| telco                      | 6.86 ms                                                | 8.65 ms: 1.26x slower                                             |
| coverage                   | 78.8 ms                                                | 101 ms: 1.28x slower                                              |
| python_startup             | 8.56 ms                                                | 11.1 ms: 1.30x slower                                             |
| python_startup_no_site     | 6.01 ms                                                | 9.55 ms: 1.59x slower                                             |
| unpack_sequence            | 43.5 ns                                                | 89.6 ns: 2.06x slower                                             |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                      |

Benchmark hidden because not significant (4): pprint_pformat, pprint_safe_repr, sqlglot_normalize, bench_mp_pool
Ignored benchmarks (5) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 81.89% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.10x