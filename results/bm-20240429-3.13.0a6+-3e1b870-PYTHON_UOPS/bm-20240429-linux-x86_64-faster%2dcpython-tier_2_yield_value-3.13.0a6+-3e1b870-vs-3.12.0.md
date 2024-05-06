# Results vs. 3.12.0

- fork: faster-cpython
- ref: tier_2_yield_value
- machine: linux-x86_64
- commit hash: 3e1b870
- commit date: 2024-04-29
- overall geometric mean: 1.21x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 0.97x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 361 ms: 1.32x slower                                                           |
| chameleon      | 7.41 ms                                                | 8.81 ms: 1.19x slower                                                          |
| docutils       | 2.77 sec                                               | 3.37 sec: 1.22x slower                                                         |
| tornado_http   | 103 ms                                                 | 105 ms: 1.02x slower                                                           |
| Geometric mean | (ref)                                                  | 1.18x slower                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 366 ms: 1.23x faster                                                           |
| async_tree_memoization_tg  | 575 ms                                                 | 478 ms: 1.20x faster                                                           |
| async_tree_io_tg           | 1.18 sec                                               | 986 ms: 1.20x faster                                                           |
| async_tree_none            | 472 ms                                                 | 393 ms: 1.20x faster                                                           |
| async_tree_io              | 1.16 sec                                               | 1.00 sec: 1.15x faster                                                         |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 643 ms: 1.13x faster                                                           |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 658 ms: 1.10x faster                                                           |
| async_tree_memoization     | 578 ms                                                 | 526 ms: 1.10x faster                                                           |
| Geometric mean             | (ref)                                                  | 1.16x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                 | 194 ms: 1.03x slower                                                           |
| float          | 84.7 ms                                                | 129 ms: 1.52x slower                                                           |
| nbody          | 97.0 ms                                                | 197 ms: 2.03x slower                                                           |
| Geometric mean | (ref)                                                  | 1.47x slower                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_effbot   | 3.61 ms                                                | 3.74 ms: 1.04x slower                                                          |
| regex_dna      | 212 ms                                                 | 226 ms: 1.07x slower                                                           |
| regex_v8       | 23.1 ms                                                | 26.4 ms: 1.14x slower                                                          |
| regex_compile  | 148 ms                                                 | 223 ms: 1.50x slower                                                           |
| Geometric mean | (ref)                                                  | 1.17x slower                                                                   |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| unpickle             | 15.9 us                                                | 14.9 us: 1.06x faster                                                          |
| json_loads           | 28.5 us                                                | 27.5 us: 1.04x faster                                                          |
| xml_etree_parse      | 159 ms                                                 | 154 ms: 1.03x faster                                                           |
| pickle_pure_python   | 324 us                                                 | 317 us: 1.02x faster                                                           |
| pickle_dict          | 35.5 us                                                | 35.1 us: 1.01x faster                                                          |
| unpickle_list        | 5.29 us                                                | 5.33 us: 1.01x slower                                                          |
| pickle_list          | 5.08 us                                                | 5.13 us: 1.01x slower                                                          |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                          |
| xml_etree_generate   | 89.2 ms                                                | 103 ms: 1.15x slower                                                           |
| xml_etree_iterparse  | 107 ms                                                 | 127 ms: 1.19x slower                                                           |
| xml_etree_process    | 61.7 ms                                                | 74.0 ms: 1.20x slower                                                          |
| tomli_loads          | 2.33 sec                                               | 3.37 sec: 1.45x slower                                                         |
| unpickle_pure_python | 230 us                                                 | 398 us: 1.73x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                                   |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.12 ms: 1.03x slower                                                          |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                          |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| django_template | 34.6 ms                                                | 47.5 ms: 1.37x slower                                                          |
| mako            | 11.9 ms                                                | 20.3 ms: 1.71x slower                                                          |
| Geometric mean  | (ref)                                                  | 1.53x slower                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 366 ms: 1.23x faster                                                           |
| async_tree_memoization_tg  | 575 ms                                                 | 478 ms: 1.20x faster                                                           |
| async_tree_io_tg           | 1.18 sec                                               | 986 ms: 1.20x faster                                                           |
| async_tree_none            | 472 ms                                                 | 393 ms: 1.20x faster                                                           |
| async_tree_io              | 1.16 sec                                               | 1.00 sec: 1.15x faster                                                         |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 643 ms: 1.13x faster                                                           |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 658 ms: 1.10x faster                                                           |
| async_tree_memoization     | 578 ms                                                 | 526 ms: 1.10x faster                                                           |
| unpickle                   | 15.9 us                                                | 14.9 us: 1.06x faster                                                          |
| gc_traversal               | 3.79 ms                                                | 3.61 ms: 1.05x faster                                                          |
| json_loads                 | 28.5 us                                                | 27.5 us: 1.04x faster                                                          |
| xml_etree_parse            | 159 ms                                                 | 154 ms: 1.03x faster                                                           |
| pickle_pure_python         | 324 us                                                 | 317 us: 1.02x faster                                                           |
| pickle_dict                | 35.5 us                                                | 35.1 us: 1.01x faster                                                          |
| json                       | 5.26 ms                                                | 5.20 ms: 1.01x faster                                                          |
| pathlib                    | 19.3 ms                                                | 19.2 ms: 1.01x faster                                                          |
| unpickle_list              | 5.29 us                                                | 5.33 us: 1.01x slower                                                          |
| pickle_list                | 5.08 us                                                | 5.13 us: 1.01x slower                                                          |
| tornado_http               | 103 ms                                                 | 105 ms: 1.02x slower                                                           |
| python_startup_no_site     | 6.94 ms                                                | 7.12 ms: 1.03x slower                                                          |
| generators                 | 31.2 ms                                                | 32.1 ms: 1.03x slower                                                          |
| asyncio_websockets         | 551 ms                                                 | 567 ms: 1.03x slower                                                           |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                          |
| pidigits                   | 187 ms                                                 | 194 ms: 1.03x slower                                                           |
| regex_effbot               | 3.61 ms                                                | 3.74 ms: 1.04x slower                                                          |
| logging_silent             | 104 ns                                                 | 108 ns: 1.04x slower                                                           |
| coroutines                 | 23.2 ms                                                | 24.1 ms: 1.04x slower                                                          |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.87 sec: 1.05x slower                                                         |
| dask                       | 372 ms                                                 | 396 ms: 1.07x slower                                                           |
| regex_dna                  | 212 ms                                                 | 226 ms: 1.07x slower                                                           |
| sqlite_synth               | 2.83 us                                                | 3.08 us: 1.09x slower                                                          |
| async_generators           | 463 ms                                                 | 504 ms: 1.09x slower                                                           |
| asyncio_tcp                | 491 ms                                                 | 539 ms: 1.10x slower                                                           |
| logging_format             | 7.23 us                                                | 7.96 us: 1.10x slower                                                          |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                                          |
| gunicorn                   | 1.24 ms                                                | 1.37 ms: 1.10x slower                                                          |
| deepcopy                   | 371 us                                                 | 411 us: 1.11x slower                                                           |
| aiohttp                    | 1.15 ms                                                | 1.28 ms: 1.11x slower                                                          |
| logging_simple             | 6.46 us                                                | 7.21 us: 1.12x slower                                                          |
| sympy_sum                  | 169 ms                                                 | 192 ms: 1.14x slower                                                           |
| dulwich_log                | 68.5 ms                                                | 77.9 ms: 1.14x slower                                                          |
| regex_v8                   | 23.1 ms                                                | 26.4 ms: 1.14x slower                                                          |
| xml_etree_generate         | 89.2 ms                                                | 103 ms: 1.15x slower                                                           |
| sqlglot_transpile          | 1.68 ms                                                | 1.94 ms: 1.15x slower                                                          |
| bench_thread_pool          | 842 us                                                 | 976 us: 1.16x slower                                                           |
| sqlglot_parse              | 1.36 ms                                                | 1.59 ms: 1.17x slower                                                          |
| pycparser                  | 1.18 sec                                               | 1.38 sec: 1.17x slower                                                         |
| chameleon                  | 7.41 ms                                                | 8.81 ms: 1.19x slower                                                          |
| xml_etree_iterparse        | 107 ms                                                 | 127 ms: 1.19x slower                                                           |
| xml_etree_process          | 61.7 ms                                                | 74.0 ms: 1.20x slower                                                          |
| raytrace                   | 312 ms                                                 | 377 ms: 1.21x slower                                                           |
| create_gc_cycles           | 1.48 ms                                                | 1.78 ms: 1.21x slower                                                          |
| sympy_str                  | 300 ms                                                 | 362 ms: 1.21x slower                                                           |
| sympy_expand               | 478 ms                                                 | 583 ms: 1.22x slower                                                           |
| docutils                   | 2.77 sec                                               | 3.37 sec: 1.22x slower                                                         |
| deepcopy_memo              | 40.7 us                                                | 50.7 us: 1.25x slower                                                          |
| mdp                        | 2.63 sec                                               | 3.33 sec: 1.26x slower                                                         |
| coverage                   | 72.7 ms                                                | 92.3 ms: 1.27x slower                                                          |
| sqlglot_normalize          | 110 ms                                                 | 141 ms: 1.28x slower                                                           |
| meteor_contest             | 112 ms                                                 | 144 ms: 1.28x slower                                                           |
| sympy_integrate            | 21.4 ms                                                | 27.6 ms: 1.29x slower                                                          |
| 2to3                       | 274 ms                                                 | 361 ms: 1.32x slower                                                           |
| sqlglot_optimize           | 54.8 ms                                                | 73.3 ms: 1.34x slower                                                          |
| telco                      | 7.10 ms                                                | 9.63 ms: 1.36x slower                                                          |
| scimark_sor                | 129 ms                                                 | 176 ms: 1.37x slower                                                           |
| django_template            | 34.6 ms                                                | 47.5 ms: 1.37x slower                                                          |
| typing_runtime_protocols   | 158 us                                                 | 219 us: 1.39x slower                                                           |
| tomli_loads                | 2.33 sec                                               | 3.37 sec: 1.45x slower                                                         |
| deltablue                  | 3.72 ms                                                | 5.46 ms: 1.47x slower                                                          |
| regex_compile              | 148 ms                                                 | 223 ms: 1.50x slower                                                           |
| float                      | 84.7 ms                                                | 129 ms: 1.52x slower                                                           |
| richards_super             | 51.5 ms                                                | 78.6 ms: 1.52x slower                                                          |
| crypto_pyaes               | 81.9 ms                                                | 125 ms: 1.53x slower                                                           |
| chaos                      | 67.0 ms                                                | 103 ms: 1.54x slower                                                           |
| scimark_fft                | 382 ms                                                 | 597 ms: 1.56x slower                                                           |
| richards                   | 45.8 ms                                                | 71.7 ms: 1.56x slower                                                          |
| pprint_safe_repr           | 776 ms                                                 | 1.29 sec: 1.66x slower                                                         |
| fannkuch                   | 417 ms                                                 | 705 ms: 1.69x slower                                                           |
| pprint_pformat             | 1.57 sec                                               | 2.66 sec: 1.70x slower                                                         |
| mako                       | 11.9 ms                                                | 20.3 ms: 1.71x slower                                                          |
| comprehensions             | 21.8 us                                                | 37.5 us: 1.72x slower                                                          |
| scimark_lu                 | 118 ms                                                 | 203 ms: 1.72x slower                                                           |
| unpickle_pure_python       | 230 us                                                 | 398 us: 1.73x slower                                                           |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 8.81 ms: 1.74x slower                                                          |
| pyflate                    | 482 ms                                                 | 862 ms: 1.79x slower                                                           |
| scimark_monte_carlo        | 75.1 ms                                                | 135 ms: 1.80x slower                                                           |
| nqueens                    | 83.3 ms                                                | 153 ms: 1.83x slower                                                           |
| spectral_norm              | 115 ms                                                 | 215 ms: 1.87x slower                                                           |
| go                         | 139 ms                                                 | 261 ms: 1.87x slower                                                           |
| nbody                      | 97.0 ms                                                | 197 ms: 2.03x slower                                                           |
| hexiom                     | 6.41 ms                                                | 15.2 ms: 2.37x slower                                                          |
| Geometric mean             | (ref)                                                  | 1.21x slower                                                                   |

Benchmark hidden because not significant (4): deepcopy_reduce, pickle, bench_mp_pool, mypy2
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240429-3.13.0a6+-3e1b870-PYTHON_UOPS/bm-20240429-linux-x86_64-faster%2dcpython-tier_2_yield_value-3.13.0a6+-3e1b870.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 0.97x