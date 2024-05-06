# Results vs. 3.12.0

- fork: faster-cpython
- ref: tier1_eval_breaker
- machine: linux-x86_64
- commit hash: a6d4fd4
- commit date: 2024-04-22
- overall geometric mean: 1.03x faster
- HPT reliability: 99.12%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 273 ms: 1.00x faster                                                           |
| chameleon      | 7.41 ms                                                | 7.17 ms: 1.03x faster                                                          |
| docutils       | 2.77 sec                                               | 2.82 sec: 1.02x slower                                                         |
| tornado_http   | 103 ms                                                 | 94.7 ms: 1.08x faster                                                          |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                                           |
| async_tree_none            | 472 ms                                                 | 356 ms: 1.32x faster                                                           |
| async_tree_memoization_tg  | 575 ms                                                 | 440 ms: 1.31x faster                                                           |
| async_tree_io_tg           | 1.18 sec                                               | 946 ms: 1.25x faster                                                           |
| async_tree_io              | 1.16 sec                                               | 929 ms: 1.24x faster                                                           |
| async_tree_memoization     | 578 ms                                                 | 470 ms: 1.23x faster                                                           |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 605 ms: 1.20x faster                                                           |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 609 ms: 1.19x faster                                                           |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 78.9 ms: 1.07x faster                                                          |
| nbody          | 97.0 ms                                                | 92.6 ms: 1.05x faster                                                          |
| pidigits       | 187 ms                                                 | 193 ms: 1.03x slower                                                           |
| Geometric mean | (ref)                                                  | 1.03x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 137 ms: 1.08x faster                                                           |
| regex_effbot   | 3.61 ms                                                | 3.83 ms: 1.06x slower                                                          |
| regex_dna      | 212 ms                                                 | 233 ms: 1.10x slower                                                           |
| regex_v8       | 23.1 ms                                                | 25.8 ms: 1.12x slower                                                          |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.20 sec: 1.06x faster                                                         |
| pickle_pure_python   | 324 us                                                 | 308 us: 1.05x faster                                                           |
| unpickle             | 15.9 us                                                | 15.1 us: 1.05x faster                                                          |
| json_loads           | 28.5 us                                                | 27.5 us: 1.03x faster                                                          |
| unpickle_pure_python | 230 us                                                 | 224 us: 1.03x faster                                                           |
| xml_etree_process    | 61.7 ms                                                | 61.2 ms: 1.01x faster                                                          |
| xml_etree_generate   | 89.2 ms                                                | 88.6 ms: 1.01x faster                                                          |
| pickle_dict          | 35.5 us                                                | 35.4 us: 1.00x faster                                                          |
| unpickle_list        | 5.29 us                                                | 5.35 us: 1.01x slower                                                          |
| json_dumps           | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                          |
| pickle               | 11.6 us                                                | 11.9 us: 1.02x slower                                                          |
| pickle_list          | 5.08 us                                                | 5.21 us: 1.02x slower                                                          |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                                   |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.11 ms: 1.02x slower                                                          |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                          |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 11.3 ms: 1.06x faster                                                          |
| django_template | 34.6 ms                                                | 35.6 ms: 1.03x slower                                                          |
| Geometric mean  | (ref)                                                  | 1.01x faster                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 116 us: 1.36x faster                                                           |
| async_tree_none_tg         | 450 ms                                                 | 335 ms: 1.34x faster                                                           |
| async_tree_none            | 472 ms                                                 | 356 ms: 1.32x faster                                                           |
| async_tree_memoization_tg  | 575 ms                                                 | 440 ms: 1.31x faster                                                           |
| comprehensions             | 21.8 us                                                | 17.3 us: 1.26x faster                                                          |
| async_tree_io_tg           | 1.18 sec                                               | 946 ms: 1.25x faster                                                           |
| async_tree_io              | 1.16 sec                                               | 929 ms: 1.24x faster                                                           |
| async_tree_memoization     | 578 ms                                                 | 470 ms: 1.23x faster                                                           |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 605 ms: 1.20x faster                                                           |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 609 ms: 1.19x faster                                                           |
| raytrace                   | 312 ms                                                 | 263 ms: 1.19x faster                                                           |
| mypy2                      | 830 ms                                                 | 741 ms: 1.12x faster                                                           |
| logging_format             | 7.23 us                                                | 6.48 us: 1.12x faster                                                          |
| deltablue                  | 3.72 ms                                                | 3.34 ms: 1.11x faster                                                          |
| logging_simple             | 6.46 us                                                | 5.84 us: 1.11x faster                                                          |
| chaos                      | 67.0 ms                                                | 61.0 ms: 1.10x faster                                                          |
| scimark_monte_carlo        | 75.1 ms                                                | 68.8 ms: 1.09x faster                                                          |
| pathlib                    | 19.3 ms                                                | 17.8 ms: 1.09x faster                                                          |
| tornado_http               | 103 ms                                                 | 94.7 ms: 1.08x faster                                                          |
| regex_compile              | 148 ms                                                 | 137 ms: 1.08x faster                                                           |
| sympy_sum                  | 169 ms                                                 | 156 ms: 1.08x faster                                                           |
| float                      | 84.7 ms                                                | 78.9 ms: 1.07x faster                                                          |
| crypto_pyaes               | 81.9 ms                                                | 76.3 ms: 1.07x faster                                                          |
| sympy_str                  | 300 ms                                                 | 283 ms: 1.06x faster                                                           |
| tomli_loads                | 2.33 sec                                               | 2.20 sec: 1.06x faster                                                         |
| mako                       | 11.9 ms                                                | 11.3 ms: 1.06x faster                                                          |
| deepcopy_reduce            | 3.35 us                                                | 3.18 us: 1.05x faster                                                          |
| pickle_pure_python         | 324 us                                                 | 308 us: 1.05x faster                                                           |
| sqlglot_parse              | 1.36 ms                                                | 1.29 ms: 1.05x faster                                                          |
| scimark_sor                | 129 ms                                                 | 123 ms: 1.05x faster                                                           |
| sympy_integrate            | 21.4 ms                                                | 20.4 ms: 1.05x faster                                                          |
| sqlglot_transpile          | 1.68 ms                                                | 1.60 ms: 1.05x faster                                                          |
| unpickle                   | 15.9 us                                                | 15.1 us: 1.05x faster                                                          |
| nbody                      | 97.0 ms                                                | 92.6 ms: 1.05x faster                                                          |
| json_loads                 | 28.5 us                                                | 27.5 us: 1.03x faster                                                          |
| deepcopy_memo              | 40.7 us                                                | 39.4 us: 1.03x faster                                                          |
| chameleon                  | 7.41 ms                                                | 7.17 ms: 1.03x faster                                                          |
| coroutines                 | 23.2 ms                                                | 22.5 ms: 1.03x faster                                                          |
| generators                 | 31.2 ms                                                | 30.3 ms: 1.03x faster                                                          |
| deepcopy                   | 371 us                                                 | 360 us: 1.03x faster                                                           |
| logging_silent             | 104 ns                                                 | 102 ns: 1.03x faster                                                           |
| unpickle_pure_python       | 230 us                                                 | 224 us: 1.03x faster                                                           |
| async_generators           | 463 ms                                                 | 451 ms: 1.03x faster                                                           |
| fannkuch                   | 417 ms                                                 | 406 ms: 1.03x faster                                                           |
| dulwich_log                | 68.5 ms                                                | 66.8 ms: 1.02x faster                                                          |
| pprint_safe_repr           | 776 ms                                                 | 760 ms: 1.02x faster                                                           |
| nqueens                    | 83.3 ms                                                | 81.9 ms: 1.02x faster                                                          |
| scimark_lu                 | 118 ms                                                 | 117 ms: 1.01x faster                                                           |
| json                       | 5.26 ms                                                | 5.20 ms: 1.01x faster                                                          |
| xml_etree_process          | 61.7 ms                                                | 61.2 ms: 1.01x faster                                                          |
| bench_mp_pool              | 24.0 ms                                                | 23.8 ms: 1.01x faster                                                          |
| bench_thread_pool          | 842 us                                                 | 836 us: 1.01x faster                                                           |
| xml_etree_generate         | 89.2 ms                                                | 88.6 ms: 1.01x faster                                                          |
| scimark_fft                | 382 ms                                                 | 379 ms: 1.01x faster                                                           |
| pprint_pformat             | 1.57 sec                                               | 1.56 sec: 1.01x faster                                                         |
| pickle_dict                | 35.5 us                                                | 35.4 us: 1.00x faster                                                          |
| 2to3                       | 274 ms                                                 | 273 ms: 1.00x faster                                                           |
| hexiom                     | 6.41 ms                                                | 6.45 ms: 1.01x slower                                                          |
| unpickle_list              | 5.29 us                                                | 5.35 us: 1.01x slower                                                          |
| json_dumps                 | 10.4 ms                                                | 10.5 ms: 1.01x slower                                                          |
| sqlglot_optimize           | 54.8 ms                                                | 55.6 ms: 1.01x slower                                                          |
| docutils                   | 2.77 sec                                               | 2.82 sec: 1.02x slower                                                         |
| spectral_norm              | 115 ms                                                 | 117 ms: 1.02x slower                                                           |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.02x slower                                                          |
| asyncio_websockets         | 551 ms                                                 | 563 ms: 1.02x slower                                                           |
| richards                   | 45.8 ms                                                | 46.9 ms: 1.02x slower                                                          |
| pickle                     | 11.6 us                                                | 11.9 us: 1.02x slower                                                          |
| gunicorn                   | 1.24 ms                                                | 1.27 ms: 1.02x slower                                                          |
| python_startup_no_site     | 6.94 ms                                                | 7.11 ms: 1.02x slower                                                          |
| pickle_list                | 5.08 us                                                | 5.21 us: 1.02x slower                                                          |
| pyflate                    | 482 ms                                                 | 495 ms: 1.03x slower                                                           |
| go                         | 139 ms                                                 | 143 ms: 1.03x slower                                                           |
| django_template            | 34.6 ms                                                | 35.6 ms: 1.03x slower                                                          |
| pidigits                   | 187 ms                                                 | 193 ms: 1.03x slower                                                           |
| pycparser                  | 1.18 sec                                               | 1.22 sec: 1.03x slower                                                         |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.85 sec: 1.03x slower                                                         |
| richards_super             | 51.5 ms                                                | 53.3 ms: 1.04x slower                                                          |
| asyncio_tcp                | 491 ms                                                 | 511 ms: 1.04x slower                                                           |
| gc_traversal               | 3.79 ms                                                | 3.98 ms: 1.05x slower                                                          |
| sqlite_synth               | 2.83 us                                                | 2.97 us: 1.05x slower                                                          |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.33 ms: 1.05x slower                                                          |
| mdp                        | 2.63 sec                                               | 2.79 sec: 1.06x slower                                                         |
| regex_effbot               | 3.61 ms                                                | 3.83 ms: 1.06x slower                                                          |
| regex_dna                  | 212 ms                                                 | 233 ms: 1.10x slower                                                           |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                          |
| regex_v8                   | 23.1 ms                                                | 25.8 ms: 1.12x slower                                                          |
| create_gc_cycles           | 1.48 ms                                                | 1.77 ms: 1.20x slower                                                          |
| telco                      | 7.10 ms                                                | 8.65 ms: 1.22x slower                                                          |
| coverage                   | 72.7 ms                                                | 98.8 ms: 1.36x slower                                                          |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                                   |

Benchmark hidden because not significant (6): xml_etree_parse, meteor_contest, dask, sympy_expand, sqlglot_normalize, xml_etree_iterparse
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240422-3.13.0a6+-a6d4fd4/bm-20240422-linux-x86_64-faster%2dcpython-tier1_eval_breaker-3.13.0a6+-a6d4fd4.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.12% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.96x