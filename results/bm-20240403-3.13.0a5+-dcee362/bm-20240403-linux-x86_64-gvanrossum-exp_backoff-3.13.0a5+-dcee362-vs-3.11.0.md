# Results vs. 3.11.0

- fork: gvanrossum
- ref: exp_backoff
- machine: linux-x86_64
- commit hash: dcee362
- commit date: 2024-04-03
- overall geometric mean: 1.07x faster
- HPT reliability: 98.77%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 270 ms: 1.02x slower                                              |
| chameleon      | 6.70 ms                                                | 6.92 ms: 1.03x slower                                             |
| docutils       | 2.66 sec                                               | 2.82 sec: 1.06x slower                                            |
| html5lib       | 64.8 ms                                                | 68.2 ms: 1.05x slower                                             |
| tornado_http   | 98.1 ms                                                | 94.2 ms: 1.04x faster                                             |
| Geometric mean | (ref)                                                  | 1.02x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 350 ms: 1.51x faster                                              |
| async_tree_none_tg         | 491 ms                                                 | 330 ms: 1.49x faster                                              |
| async_tree_memoization_tg  | 626 ms                                                 | 437 ms: 1.43x faster                                              |
| async_tree_io_tg           | 1.29 sec                                               | 917 ms: 1.41x faster                                              |
| async_tree_io              | 1.29 sec                                               | 913 ms: 1.41x faster                                              |
| async_tree_memoization     | 639 ms                                                 | 461 ms: 1.39x faster                                              |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 601 ms: 1.27x faster                                              |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 609 ms: 1.23x faster                                              |
| Geometric mean             | (ref)                                                  | 1.39x faster                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 90.1 ms: 1.07x faster                                             |
| Geometric mean | (ref)                                                  | 1.02x faster                                                      |

Benchmark hidden because not significant (2): pidigits, float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 135 ms: 1.05x faster                                              |
| regex_effbot   | 3.51 ms                                                | 3.72 ms: 1.06x slower                                             |
| regex_dna      | 205 ms                                                 | 224 ms: 1.10x slower                                              |
| regex_v8       | 22.9 ms                                                | 25.5 ms: 1.11x slower                                             |
| Geometric mean | (ref)                                                  | 1.06x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                             |
| unpickle_pure_python | 242 us                                                 | 226 us: 1.07x faster                                              |
| tomli_loads          | 2.30 sec                                               | 2.16 sec: 1.07x faster                                            |
| pickle_pure_python   | 320 us                                                 | 303 us: 1.06x faster                                              |
| pickle_dict          | 34.6 us                                                | 32.9 us: 1.05x faster                                             |
| unpickle_list        | 5.21 us                                                | 5.02 us: 1.04x faster                                             |
| json_loads           | 29.2 us                                                | 28.5 us: 1.03x faster                                             |
| xml_etree_parse      | 164 ms                                                 | 160 ms: 1.02x faster                                              |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                              |
| pickle_list          | 4.59 us                                                | 4.79 us: 1.04x slower                                             |
| pickle               | 11.0 us                                                | 11.6 us: 1.06x slower                                             |
| xml_etree_process    | 56.9 ms                                                | 60.4 ms: 1.06x slower                                             |
| unpickle             | 13.8 us                                                | 14.9 us: 1.08x slower                                             |
| xml_etree_generate   | 81.1 ms                                                | 87.9 ms: 1.08x slower                                             |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                             |
| python_startup_no_site | 6.01 ms                                                | 8.98 ms: 1.49x slower                                             |
| Geometric mean         | (ref)                                                  | 1.36x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml     | 53.4 ms                                                | 52.1 ms: 1.03x faster                                             |
| mako           | 10.7 ms                                                | 10.7 ms: 1.00x slower                                             |
| genshi_text    | 22.5 ms                                                | 24.0 ms: 1.07x slower                                             |
| Geometric mean | (ref)                                                  | 1.01x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240403-linux-x86_64-gvanrossum-exp_backoff-3.13.0a5+-dcee362 |
|----------------------------|:------------------------------------------------------:|:-----------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 114 us: 4.56x faster                                              |
| generators                 | 74.9 ms                                                | 30.0 ms: 2.49x faster                                             |
| asyncio_tcp                | 875 ms                                                 | 506 ms: 1.73x faster                                              |
| pylint                     | 476 ms                                                 | 281 ms: 1.70x faster                                              |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.84 sec: 1.69x faster                                            |
| async_tree_none            | 528 ms                                                 | 350 ms: 1.51x faster                                              |
| async_tree_none_tg         | 491 ms                                                 | 330 ms: 1.49x faster                                              |
| async_tree_memoization_tg  | 626 ms                                                 | 437 ms: 1.43x faster                                              |
| comprehensions             | 23.6 us                                                | 16.5 us: 1.43x faster                                             |
| async_tree_io_tg           | 1.29 sec                                               | 917 ms: 1.41x faster                                              |
| async_tree_io              | 1.29 sec                                               | 913 ms: 1.41x faster                                              |
| async_tree_memoization     | 639 ms                                                 | 461 ms: 1.39x faster                                              |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                             |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 601 ms: 1.27x faster                                              |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 609 ms: 1.23x faster                                              |
| deltablue                  | 3.92 ms                                                | 3.20 ms: 1.23x faster                                             |
| coroutines                 | 27.0 ms                                                | 22.2 ms: 1.22x faster                                             |
| chaos                      | 71.9 ms                                                | 60.9 ms: 1.18x faster                                             |
| raytrace                   | 309 ms                                                 | 264 ms: 1.17x faster                                              |
| richards_super             | 61.9 ms                                                | 53.1 ms: 1.16x faster                                             |
| logging_silent             | 111 ns                                                 | 99.5 ns: 1.12x faster                                             |
| sqlglot_parse              | 1.43 ms                                                | 1.29 ms: 1.11x faster                                             |
| hexiom                     | 6.89 ms                                                | 6.28 ms: 1.10x faster                                             |
| sqlglot_transpile          | 1.75 ms                                                | 1.60 ms: 1.10x faster                                             |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.08x faster                                              |
| logging_simple             | 6.22 us                                                | 5.76 us: 1.08x faster                                             |
| logging_format             | 6.81 us                                                | 6.36 us: 1.07x faster                                             |
| unpickle_pure_python       | 242 us                                                 | 226 us: 1.07x faster                                              |
| nbody                      | 96.0 ms                                                | 90.1 ms: 1.07x faster                                             |
| tomli_loads                | 2.30 sec                                               | 2.16 sec: 1.07x faster                                            |
| sympy_str                  | 297 ms                                                 | 279 ms: 1.07x faster                                              |
| deepcopy_memo              | 40.2 us                                                | 37.9 us: 1.06x faster                                             |
| richards                   | 49.8 ms                                                | 47.0 ms: 1.06x faster                                             |
| pickle_pure_python         | 320 us                                                 | 303 us: 1.06x faster                                              |
| nqueens                    | 87.9 ms                                                | 83.5 ms: 1.05x faster                                             |
| sympy_integrate            | 21.5 ms                                                | 20.4 ms: 1.05x faster                                             |
| pickle_dict                | 34.6 us                                                | 32.9 us: 1.05x faster                                             |
| go                         | 149 ms                                                 | 142 ms: 1.05x faster                                              |
| mdp                        | 2.77 sec                                               | 2.65 sec: 1.05x faster                                            |
| regex_compile              | 141 ms                                                 | 135 ms: 1.05x faster                                              |
| tornado_http               | 98.1 ms                                                | 94.2 ms: 1.04x faster                                             |
| unpickle_list              | 5.21 us                                                | 5.02 us: 1.04x faster                                             |
| sympy_expand               | 484 ms                                                 | 470 ms: 1.03x faster                                              |
| scimark_monte_carlo        | 70.7 ms                                                | 68.9 ms: 1.03x faster                                             |
| json_loads                 | 29.2 us                                                | 28.5 us: 1.03x faster                                             |
| genshi_xml                 | 53.4 ms                                                | 52.1 ms: 1.03x faster                                             |
| fannkuch                   | 405 ms                                                 | 396 ms: 1.02x faster                                              |
| xml_etree_parse            | 164 ms                                                 | 160 ms: 1.02x faster                                              |
| sqlglot_normalize          | 113 ms                                                 | 110 ms: 1.02x faster                                              |
| pycparser                  | 1.19 sec                                               | 1.16 sec: 1.02x faster                                            |
| scimark_lu                 | 116 ms                                                 | 114 ms: 1.02x faster                                              |
| deepcopy                   | 365 us                                                 | 359 us: 1.02x faster                                              |
| pprint_pformat             | 1.55 sec                                               | 1.53 sec: 1.01x faster                                            |
| gc_traversal               | 4.01 ms                                                | 3.97 ms: 1.01x faster                                             |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                              |
| crypto_pyaes               | 76.7 ms                                                | 76.3 ms: 1.01x faster                                             |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.00x faster                                             |
| mako                       | 10.7 ms                                                | 10.7 ms: 1.00x slower                                             |
| scimark_sor                | 121 ms                                                 | 123 ms: 1.01x slower                                              |
| 2to3                       | 264 ms                                                 | 270 ms: 1.02x slower                                              |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.15 ms: 1.03x slower                                             |
| thrift                     | 784 us                                                 | 804 us: 1.03x slower                                              |
| json                       | 5.24 ms                                                | 5.39 ms: 1.03x slower                                             |
| asyncio_websockets         | 550 ms                                                 | 567 ms: 1.03x slower                                              |
| pathlib                    | 18.5 ms                                                | 19.1 ms: 1.03x slower                                             |
| chameleon                  | 6.70 ms                                                | 6.92 ms: 1.03x slower                                             |
| spectral_norm              | 108 ms                                                 | 112 ms: 1.04x slower                                              |
| dulwich_log                | 64.6 ms                                                | 67.3 ms: 1.04x slower                                             |
| aiohttp                    | 1.12 ms                                                | 1.16 ms: 1.04x slower                                             |
| pickle_list                | 4.59 us                                                | 4.79 us: 1.04x slower                                             |
| gunicorn                   | 1.20 ms                                                | 1.26 ms: 1.05x slower                                             |
| html5lib                   | 64.8 ms                                                | 68.2 ms: 1.05x slower                                             |
| docutils                   | 2.66 sec                                               | 2.82 sec: 1.06x slower                                            |
| pickle                     | 11.0 us                                                | 11.6 us: 1.06x slower                                             |
| regex_effbot               | 3.51 ms                                                | 3.72 ms: 1.06x slower                                             |
| xml_etree_process          | 56.9 ms                                                | 60.4 ms: 1.06x slower                                             |
| genshi_text                | 22.5 ms                                                | 24.0 ms: 1.07x slower                                             |
| pyflate                    | 434 ms                                                 | 465 ms: 1.07x slower                                              |
| mypy2                      | 686 ms                                                 | 737 ms: 1.07x slower                                              |
| unpickle                   | 13.8 us                                                | 14.9 us: 1.08x slower                                             |
| scimark_fft                | 345 ms                                                 | 374 ms: 1.08x slower                                              |
| xml_etree_generate         | 81.1 ms                                                | 87.9 ms: 1.08x slower                                             |
| regex_dna                  | 205 ms                                                 | 224 ms: 1.10x slower                                              |
| regex_v8                   | 22.9 ms                                                | 25.5 ms: 1.11x slower                                             |
| sqlite_synth               | 2.57 us                                                | 2.95 us: 1.15x slower                                             |
| async_generators           | 374 ms                                                 | 445 ms: 1.19x slower                                              |
| create_gc_cycles           | 1.43 ms                                                | 1.73 ms: 1.20x slower                                             |
| coverage                   | 78.8 ms                                                | 96.2 ms: 1.22x slower                                             |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                             |
| telco                      | 6.86 ms                                                | 8.65 ms: 1.26x slower                                             |
| python_startup_no_site     | 6.01 ms                                                | 8.98 ms: 1.49x slower                                             |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                      |

Benchmark hidden because not significant (8): sqlglot_optimize, bench_thread_pool, pidigits, deepcopy_reduce, float, pprint_safe_repr, meteor_contest, dask
Ignored benchmarks (6) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: django_template, djangocms, flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 98.77% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x