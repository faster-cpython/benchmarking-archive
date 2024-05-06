# Results vs. 3.11.0

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: linux-x86_64
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.06x faster
- HPT reliability: 91.52%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 273 ms: 1.03x slower                                                           |
| chameleon      | 6.70 ms                                                | 7.17 ms: 1.07x slower                                                          |
| docutils       | 2.66 sec                                               | 2.82 sec: 1.06x slower                                                         |
| html5lib       | 64.8 ms                                                | 66.5 ms: 1.03x slower                                                          |
| tornado_http   | 98.1 ms                                                | 94.7 ms: 1.04x faster                                                          |
| Geometric mean | (ref)                                                  | 1.03x slower                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none            | 528 ms                                                 | 356 ms: 1.48x faster                                                           |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.47x faster                                                           |
| async_tree_memoization_tg  | 626 ms                                                 | 440 ms: 1.42x faster                                                           |
| async_tree_io              | 1.29 sec                                               | 929 ms: 1.39x faster                                                           |
| async_tree_io_tg           | 1.29 sec                                               | 946 ms: 1.37x faster                                                           |
| async_tree_memoization     | 639 ms                                                 | 470 ms: 1.36x faster                                                           |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                           |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 609 ms: 1.23x faster                                                           |
| Geometric mean             | (ref)                                                  | 1.37x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| nbody          | 96.0 ms                                                | 92.6 ms: 1.04x faster                                                          |
| pidigits       | 194 ms                                                 | 193 ms: 1.01x faster                                                           |
| Geometric mean | (ref)                                                  | 1.01x faster                                                                   |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 141 ms                                                 | 137 ms: 1.03x faster                                                           |
| regex_effbot   | 3.51 ms                                                | 3.83 ms: 1.09x slower                                                          |
| regex_v8       | 22.9 ms                                                | 25.8 ms: 1.13x slower                                                          |
| regex_dna      | 205 ms                                                 | 233 ms: 1.14x slower                                                           |
| Geometric mean | (ref)                                                  | 1.08x slower                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| json_dumps           | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                          |
| unpickle_pure_python | 242 us                                                 | 224 us: 1.08x faster                                                           |
| json_loads           | 29.2 us                                                | 27.5 us: 1.06x faster                                                          |
| tomli_loads          | 2.30 sec                                               | 2.20 sec: 1.05x faster                                                         |
| pickle_pure_python   | 320 us                                                 | 308 us: 1.04x faster                                                           |
| xml_etree_parse      | 164 ms                                                 | 158 ms: 1.04x faster                                                           |
| xml_etree_iterparse  | 108 ms                                                 | 107 ms: 1.01x faster                                                           |
| pickle_dict          | 34.6 us                                                | 35.4 us: 1.02x slower                                                          |
| unpickle_list        | 5.21 us                                                | 5.35 us: 1.03x slower                                                          |
| xml_etree_process    | 56.9 ms                                                | 61.2 ms: 1.08x slower                                                          |
| pickle               | 11.0 us                                                | 11.9 us: 1.08x slower                                                          |
| unpickle             | 13.8 us                                                | 15.1 us: 1.09x slower                                                          |
| xml_etree_generate   | 81.1 ms                                                | 88.6 ms: 1.09x slower                                                          |
| pickle_list          | 4.59 us                                                | 5.21 us: 1.14x slower                                                          |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 6.01 ms                                                | 7.11 ms: 1.18x slower                                                          |
| python_startup         | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                          |
| Geometric mean         | (ref)                                                  | 1.21x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| genshi_xml      | 53.4 ms                                                | 52.2 ms: 1.02x faster                                                          |
| mako            | 10.7 ms                                                | 11.3 ms: 1.06x slower                                                          |
| django_template | 33.5 ms                                                | 35.6 ms: 1.06x slower                                                          |
| genshi_text     | 22.5 ms                                                | 24.0 ms: 1.07x slower                                                          |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 520 us                                                 | 116 us: 4.47x faster                                                           |
| generators                 | 74.9 ms                                                | 30.3 ms: 2.47x faster                                                          |
| asyncio_tcp                | 875 ms                                                 | 511 ms: 1.71x faster                                                           |
| asyncio_tcp_ssl            | 3.11 sec                                               | 1.85 sec: 1.68x faster                                                         |
| pylint                     | 476 ms                                                 | 320 ms: 1.49x faster                                                           |
| async_tree_none            | 528 ms                                                 | 356 ms: 1.48x faster                                                           |
| async_tree_none_tg         | 491 ms                                                 | 335 ms: 1.47x faster                                                           |
| async_tree_memoization_tg  | 626 ms                                                 | 440 ms: 1.42x faster                                                           |
| async_tree_io              | 1.29 sec                                               | 929 ms: 1.39x faster                                                           |
| async_tree_io_tg           | 1.29 sec                                               | 946 ms: 1.37x faster                                                           |
| comprehensions             | 23.6 us                                                | 17.3 us: 1.37x faster                                                          |
| async_tree_memoization     | 639 ms                                                 | 470 ms: 1.36x faster                                                           |
| json_dumps                 | 13.3 ms                                                | 10.5 ms: 1.27x faster                                                          |
| async_tree_cpu_io_mixed_tg | 761 ms                                                 | 605 ms: 1.26x faster                                                           |
| async_tree_cpu_io_mixed    | 749 ms                                                 | 609 ms: 1.23x faster                                                           |
| coroutines                 | 27.0 ms                                                | 22.5 ms: 1.20x faster                                                          |
| chaos                      | 71.9 ms                                                | 61.0 ms: 1.18x faster                                                          |
| deltablue                  | 3.92 ms                                                | 3.34 ms: 1.18x faster                                                          |
| raytrace                   | 309 ms                                                 | 263 ms: 1.18x faster                                                           |
| richards_super             | 61.9 ms                                                | 53.3 ms: 1.16x faster                                                          |
| sqlglot_parse              | 1.43 ms                                                | 1.29 ms: 1.11x faster                                                          |
| logging_silent             | 111 ns                                                 | 102 ns: 1.09x faster                                                           |
| sqlglot_transpile          | 1.75 ms                                                | 1.60 ms: 1.09x faster                                                          |
| unpickle_pure_python       | 242 us                                                 | 224 us: 1.08x faster                                                           |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.08x faster                                                           |
| nqueens                    | 87.9 ms                                                | 81.9 ms: 1.07x faster                                                          |
| hexiom                     | 6.89 ms                                                | 6.45 ms: 1.07x faster                                                          |
| logging_simple             | 6.22 us                                                | 5.84 us: 1.06x faster                                                          |
| richards                   | 49.8 ms                                                | 46.9 ms: 1.06x faster                                                          |
| json_loads                 | 29.2 us                                                | 27.5 us: 1.06x faster                                                          |
| djangocms                  | 33.5 us                                                | 31.8 us: 1.06x faster                                                          |
| sympy_integrate            | 21.5 ms                                                | 20.4 ms: 1.05x faster                                                          |
| sympy_str                  | 297 ms                                                 | 283 ms: 1.05x faster                                                           |
| logging_format             | 6.81 us                                                | 6.48 us: 1.05x faster                                                          |
| tomli_loads                | 2.30 sec                                               | 2.20 sec: 1.05x faster                                                         |
| pathlib                    | 18.5 ms                                                | 17.8 ms: 1.04x faster                                                          |
| pickle_pure_python         | 320 us                                                 | 308 us: 1.04x faster                                                           |
| xml_etree_parse            | 164 ms                                                 | 158 ms: 1.04x faster                                                           |
| go                         | 149 ms                                                 | 143 ms: 1.04x faster                                                           |
| nbody                      | 96.0 ms                                                | 92.6 ms: 1.04x faster                                                          |
| tornado_http               | 98.1 ms                                                | 94.7 ms: 1.04x faster                                                          |
| regex_compile              | 141 ms                                                 | 137 ms: 1.03x faster                                                           |
| scimark_monte_carlo        | 70.7 ms                                                | 68.8 ms: 1.03x faster                                                          |
| genshi_xml                 | 53.4 ms                                                | 52.2 ms: 1.02x faster                                                          |
| sqlglot_normalize          | 113 ms                                                 | 110 ms: 1.02x faster                                                           |
| deepcopy_memo              | 40.2 us                                                | 39.4 us: 1.02x faster                                                          |
| sympy_expand               | 484 ms                                                 | 477 ms: 1.01x faster                                                           |
| deepcopy                   | 365 us                                                 | 360 us: 1.01x faster                                                           |
| deepcopy_reduce            | 3.22 us                                                | 3.18 us: 1.01x faster                                                          |
| xml_etree_iterparse        | 108 ms                                                 | 107 ms: 1.01x faster                                                           |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                          |
| json                       | 5.24 ms                                                | 5.20 ms: 1.01x faster                                                          |
| gc_traversal               | 4.01 ms                                                | 3.98 ms: 1.01x faster                                                          |
| pidigits                   | 194 ms                                                 | 193 ms: 1.01x faster                                                           |
| crypto_pyaes               | 76.7 ms                                                | 76.3 ms: 1.00x faster                                                          |
| sqlglot_optimize           | 55.3 ms                                                | 55.6 ms: 1.01x slower                                                          |
| mdp                        | 2.77 sec                                               | 2.79 sec: 1.01x slower                                                         |
| scimark_sor                | 121 ms                                                 | 123 ms: 1.01x slower                                                           |
| dask                       | 365 ms                                                 | 371 ms: 1.02x slower                                                           |
| pprint_safe_repr           | 747 ms                                                 | 760 ms: 1.02x slower                                                           |
| pickle_dict                | 34.6 us                                                | 35.4 us: 1.02x slower                                                          |
| asyncio_websockets         | 550 ms                                                 | 563 ms: 1.02x slower                                                           |
| thrift                     | 784 us                                                 | 804 us: 1.02x slower                                                           |
| pycparser                  | 1.19 sec                                               | 1.22 sec: 1.03x slower                                                         |
| unpickle_list              | 5.21 us                                                | 5.35 us: 1.03x slower                                                          |
| html5lib                   | 64.8 ms                                                | 66.5 ms: 1.03x slower                                                          |
| meteor_contest             | 109 ms                                                 | 112 ms: 1.03x slower                                                           |
| 2to3                       | 264 ms                                                 | 273 ms: 1.03x slower                                                           |
| dulwich_log                | 64.6 ms                                                | 66.8 ms: 1.03x slower                                                          |
| aiohttp                    | 1.12 ms                                                | 1.17 ms: 1.05x slower                                                          |
| mako                       | 10.7 ms                                                | 11.3 ms: 1.06x slower                                                          |
| gunicorn                   | 1.20 ms                                                | 1.27 ms: 1.06x slower                                                          |
| scimark_sparse_mat_mult    | 5.03 ms                                                | 5.33 ms: 1.06x slower                                                          |
| docutils                   | 2.66 sec                                               | 2.82 sec: 1.06x slower                                                         |
| django_template            | 33.5 ms                                                | 35.6 ms: 1.06x slower                                                          |
| genshi_text                | 22.5 ms                                                | 24.0 ms: 1.07x slower                                                          |
| chameleon                  | 6.70 ms                                                | 7.17 ms: 1.07x slower                                                          |
| xml_etree_process          | 56.9 ms                                                | 61.2 ms: 1.08x slower                                                          |
| pickle                     | 11.0 us                                                | 11.9 us: 1.08x slower                                                          |
| mypy2                      | 686 ms                                                 | 741 ms: 1.08x slower                                                           |
| spectral_norm              | 108 ms                                                 | 117 ms: 1.08x slower                                                           |
| unpickle                   | 13.8 us                                                | 15.1 us: 1.09x slower                                                          |
| regex_effbot               | 3.51 ms                                                | 3.83 ms: 1.09x slower                                                          |
| xml_etree_generate         | 81.1 ms                                                | 88.6 ms: 1.09x slower                                                          |
| scimark_fft                | 345 ms                                                 | 379 ms: 1.10x slower                                                           |
| regex_v8                   | 22.9 ms                                                | 25.8 ms: 1.13x slower                                                          |
| pickle_list                | 4.59 us                                                | 5.21 us: 1.14x slower                                                          |
| regex_dna                  | 205 ms                                                 | 233 ms: 1.14x slower                                                           |
| pyflate                    | 434 ms                                                 | 495 ms: 1.14x slower                                                           |
| sqlite_synth               | 2.57 us                                                | 2.97 us: 1.16x slower                                                          |
| python_startup_no_site     | 6.01 ms                                                | 7.11 ms: 1.18x slower                                                          |
| async_generators           | 374 ms                                                 | 451 ms: 1.21x slower                                                           |
| python_startup             | 8.56 ms                                                | 10.5 ms: 1.23x slower                                                          |
| create_gc_cycles           | 1.43 ms                                                | 1.77 ms: 1.24x slower                                                          |
| coverage                   | 78.8 ms                                                | 98.8 ms: 1.25x slower                                                          |
| telco                      | 6.86 ms                                                | 8.65 ms: 1.26x slower                                                          |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                                   |

Benchmark hidden because not significant (5): float, scimark_lu, bench_thread_pool, fannkuch, pprint_pformat
Ignored benchmarks (4) of results/bm-20221024-3.11.0-deaf509/bm-20221024-linux-x86_64-python-v3.11.0-3.11.0-deaf509.json: flaskblogging, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence

# HPT report

- Reliability score: 91.52% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x