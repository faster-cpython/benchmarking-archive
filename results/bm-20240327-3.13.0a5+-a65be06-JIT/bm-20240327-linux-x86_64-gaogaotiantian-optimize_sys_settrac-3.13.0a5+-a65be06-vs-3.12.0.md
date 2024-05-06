# Results vs. 3.12.0

- fork: gaogaotiantian
- ref: optimize_sys_settrac
- machine: linux-x86_64
- commit hash: a65be06
- commit date: 2024-03-27
- overall geometric mean: 1.01x faster
- HPT reliability: 52.19%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 280 ms: 1.02x slower                                                           |
| chameleon      | 7.41 ms                                                | 7.00 ms: 1.06x faster                                                          |
| docutils       | 2.77 sec                                               | 2.89 sec: 1.04x slower                                                         |
| tornado_http   | 103 ms                                                 | 96.9 ms: 1.06x faster                                                          |
| Geometric mean | (ref)                                                  | 1.01x faster                                                                   |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| async_tree_none            | 472 ms                                                 | 357 ms: 1.32x faster                                                           |
| async_tree_io_tg           | 1.18 sec                                               | 900 ms: 1.31x faster                                                           |
| async_tree_none_tg         | 450 ms                                                 | 347 ms: 1.29x faster                                                           |
| async_tree_memoization_tg  | 575 ms                                                 | 449 ms: 1.28x faster                                                           |
| async_tree_io              | 1.16 sec                                               | 923 ms: 1.25x faster                                                           |
| async_tree_memoization     | 578 ms                                                 | 462 ms: 1.25x faster                                                           |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 596 ms: 1.22x faster                                                           |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 611 ms: 1.19x faster                                                           |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                                   |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 76.4 ms: 1.11x faster                                                          |
| nbody          | 97.0 ms                                                | 92.5 ms: 1.05x faster                                                          |
| pidigits       | 187 ms                                                 | 189 ms: 1.01x slower                                                           |
| Geometric mean | (ref)                                                  | 1.05x faster                                                                   |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 147 ms: 1.01x faster                                                           |
| regex_dna      | 212 ms                                                 | 219 ms: 1.03x slower                                                           |
| regex_v8       | 23.1 ms                                                | 25.5 ms: 1.10x slower                                                          |
| Geometric mean | (ref)                                                  | 1.03x slower                                                                   |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.09 sec: 1.11x faster                                                         |
| pickle_pure_python   | 324 us                                                 | 311 us: 1.04x faster                                                           |
| unpickle             | 15.9 us                                                | 15.5 us: 1.02x faster                                                          |
| xml_etree_process    | 61.7 ms                                                | 60.8 ms: 1.02x faster                                                          |
| unpickle_list        | 5.29 us                                                | 5.21 us: 1.01x faster                                                          |
| pickle_list          | 5.08 us                                                | 5.04 us: 1.01x faster                                                          |
| xml_etree_generate   | 89.2 ms                                                | 88.8 ms: 1.00x faster                                                          |
| xml_etree_iterparse  | 107 ms                                                 | 108 ms: 1.01x slower                                                           |
| pickle_dict          | 35.5 us                                                | 36.0 us: 1.01x slower                                                          |
| xml_etree_parse      | 159 ms                                                 | 162 ms: 1.02x slower                                                           |
| json_loads           | 28.5 us                                                | 29.3 us: 1.03x slower                                                          |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                          |
| pickle               | 11.6 us                                                | 11.9 us: 1.03x slower                                                          |
| unpickle_pure_python | 230 us                                                 | 245 us: 1.06x slower                                                           |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                                   |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 11.1 ms: 1.17x slower                                                          |
| python_startup_no_site | 6.94 ms                                                | 9.56 ms: 1.38x slower                                                          |
| Geometric mean         | (ref)                                                  | 1.27x slower                                                                   |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.9 ms: 1.09x faster                                                          |
| django_template | 34.6 ms                                                | 36.0 ms: 1.04x slower                                                          |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                                   |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 111 us: 1.42x faster                                                           |
| async_tree_none            | 472 ms                                                 | 357 ms: 1.32x faster                                                           |
| async_tree_io_tg           | 1.18 sec                                               | 900 ms: 1.31x faster                                                           |
| async_tree_none_tg         | 450 ms                                                 | 347 ms: 1.29x faster                                                           |
| async_tree_memoization_tg  | 575 ms                                                 | 449 ms: 1.28x faster                                                           |
| async_tree_io              | 1.16 sec                                               | 923 ms: 1.25x faster                                                           |
| async_tree_memoization     | 578 ms                                                 | 462 ms: 1.25x faster                                                           |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 596 ms: 1.22x faster                                                           |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 611 ms: 1.19x faster                                                           |
| comprehensions             | 21.8 us                                                | 18.4 us: 1.18x faster                                                          |
| tomli_loads                | 2.33 sec                                               | 2.09 sec: 1.11x faster                                                         |
| scimark_fft                | 382 ms                                                 | 343 ms: 1.11x faster                                                           |
| float                      | 84.7 ms                                                | 76.4 ms: 1.11x faster                                                          |
| crypto_pyaes               | 81.9 ms                                                | 74.8 ms: 1.09x faster                                                          |
| mako                       | 11.9 ms                                                | 10.9 ms: 1.09x faster                                                          |
| logging_format             | 7.23 us                                                | 6.64 us: 1.09x faster                                                          |
| logging_simple             | 6.46 us                                                | 6.01 us: 1.08x faster                                                          |
| scimark_monte_carlo        | 75.1 ms                                                | 70.3 ms: 1.07x faster                                                          |
| tornado_http               | 103 ms                                                 | 96.9 ms: 1.06x faster                                                          |
| chameleon                  | 7.41 ms                                                | 7.00 ms: 1.06x faster                                                          |
| chaos                      | 67.0 ms                                                | 63.4 ms: 1.06x faster                                                          |
| raytrace                   | 312 ms                                                 | 296 ms: 1.06x faster                                                           |
| deltablue                  | 3.72 ms                                                | 3.53 ms: 1.05x faster                                                          |
| nbody                      | 97.0 ms                                                | 92.5 ms: 1.05x faster                                                          |
| deepcopy_reduce            | 3.35 us                                                | 3.21 us: 1.04x faster                                                          |
| pickle_pure_python         | 324 us                                                 | 311 us: 1.04x faster                                                           |
| pprint_safe_repr           | 776 ms                                                 | 748 ms: 1.04x faster                                                           |
| generators                 | 31.2 ms                                                | 30.1 ms: 1.04x faster                                                          |
| pprint_pformat             | 1.57 sec                                               | 1.52 sec: 1.04x faster                                                         |
| fannkuch                   | 417 ms                                                 | 403 ms: 1.03x faster                                                           |
| deepcopy                   | 371 us                                                 | 360 us: 1.03x faster                                                           |
| sympy_str                  | 300 ms                                                 | 291 ms: 1.03x faster                                                           |
| pathlib                    | 19.3 ms                                                | 18.8 ms: 1.03x faster                                                          |
| deepcopy_memo              | 40.7 us                                                | 39.7 us: 1.02x faster                                                          |
| unpickle                   | 15.9 us                                                | 15.5 us: 1.02x faster                                                          |
| sympy_sum                  | 169 ms                                                 | 166 ms: 1.02x faster                                                           |
| coroutines                 | 23.2 ms                                                | 22.8 ms: 1.02x faster                                                          |
| xml_etree_process          | 61.7 ms                                                | 60.8 ms: 1.02x faster                                                          |
| sqlglot_parse              | 1.36 ms                                                | 1.34 ms: 1.02x faster                                                          |
| sqlglot_transpile          | 1.68 ms                                                | 1.66 ms: 1.01x faster                                                          |
| unpickle_list              | 5.29 us                                                | 5.21 us: 1.01x faster                                                          |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.01 ms: 1.01x faster                                                          |
| regex_compile              | 148 ms                                                 | 147 ms: 1.01x faster                                                           |
| pickle_list                | 5.08 us                                                | 5.04 us: 1.01x faster                                                          |
| xml_etree_generate         | 89.2 ms                                                | 88.8 ms: 1.00x faster                                                          |
| logging_silent             | 104 ns                                                 | 105 ns: 1.00x slower                                                           |
| xml_etree_iterparse        | 107 ms                                                 | 108 ms: 1.01x slower                                                           |
| pyflate                    | 482 ms                                                 | 488 ms: 1.01x slower                                                           |
| pidigits                   | 187 ms                                                 | 189 ms: 1.01x slower                                                           |
| mdp                        | 2.63 sec                                               | 2.66 sec: 1.01x slower                                                         |
| pickle_dict                | 35.5 us                                                | 36.0 us: 1.01x slower                                                          |
| dask                       | 372 ms                                                 | 378 ms: 1.02x slower                                                           |
| xml_etree_parse            | 159 ms                                                 | 162 ms: 1.02x slower                                                           |
| 2to3                       | 274 ms                                                 | 280 ms: 1.02x slower                                                           |
| sqlite_synth               | 2.83 us                                                | 2.89 us: 1.02x slower                                                          |
| bench_thread_pool          | 842 us                                                 | 860 us: 1.02x slower                                                           |
| sympy_integrate            | 21.4 ms                                                | 21.9 ms: 1.02x slower                                                          |
| json                       | 5.26 ms                                                | 5.40 ms: 1.03x slower                                                          |
| json_loads                 | 28.5 us                                                | 29.3 us: 1.03x slower                                                          |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                          |
| richards                   | 45.8 ms                                                | 47.2 ms: 1.03x slower                                                          |
| pickle                     | 11.6 us                                                | 11.9 us: 1.03x slower                                                          |
| sqlglot_normalize          | 110 ms                                                 | 114 ms: 1.03x slower                                                           |
| asyncio_tcp                | 491 ms                                                 | 506 ms: 1.03x slower                                                           |
| dulwich_log                | 68.5 ms                                                | 70.7 ms: 1.03x slower                                                          |
| regex_dna                  | 212 ms                                                 | 219 ms: 1.03x slower                                                           |
| asyncio_websockets         | 551 ms                                                 | 569 ms: 1.03x slower                                                           |
| richards_super             | 51.5 ms                                                | 53.2 ms: 1.03x slower                                                          |
| sympy_expand               | 478 ms                                                 | 495 ms: 1.04x slower                                                           |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.85 sec: 1.04x slower                                                         |
| scimark_sor                | 129 ms                                                 | 134 ms: 1.04x slower                                                           |
| gc_traversal               | 3.79 ms                                                | 3.95 ms: 1.04x slower                                                          |
| django_template            | 34.6 ms                                                | 36.0 ms: 1.04x slower                                                          |
| docutils                   | 2.77 sec                                               | 2.89 sec: 1.04x slower                                                         |
| gunicorn                   | 1.24 ms                                                | 1.31 ms: 1.06x slower                                                          |
| sqlglot_optimize           | 54.8 ms                                                | 58.0 ms: 1.06x slower                                                          |
| aiohttp                    | 1.15 ms                                                | 1.22 ms: 1.06x slower                                                          |
| unpickle_pure_python       | 230 us                                                 | 245 us: 1.06x slower                                                           |
| nqueens                    | 83.3 ms                                                | 90.2 ms: 1.08x slower                                                          |
| regex_v8                   | 23.1 ms                                                | 25.5 ms: 1.10x slower                                                          |
| go                         | 139 ms                                                 | 155 ms: 1.11x slower                                                           |
| scimark_lu                 | 118 ms                                                 | 133 ms: 1.13x slower                                                           |
| hexiom                     | 6.41 ms                                                | 7.29 ms: 1.14x slower                                                          |
| create_gc_cycles           | 1.48 ms                                                | 1.70 ms: 1.15x slower                                                          |
| python_startup             | 9.55 ms                                                | 11.1 ms: 1.17x slower                                                          |
| telco                      | 7.10 ms                                                | 8.59 ms: 1.21x slower                                                          |
| coverage                   | 72.7 ms                                                | 98.1 ms: 1.35x slower                                                          |
| python_startup_no_site     | 6.94 ms                                                | 9.56 ms: 1.38x slower                                                          |
| unpack_sequence            | 54.0 ns                                                | 85.5 ns: 1.58x slower                                                          |
| Geometric mean             | (ref)                                                  | 1.01x faster                                                                   |

Benchmark hidden because not significant (7): mypy2, bench_mp_pool, meteor_contest, spectral_norm, async_generators, regex_effbot, pycparser
Ignored benchmarks (2) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (6) of results/bm-20240327-3.13.0a5+-a65be06-JIT/bm-20240327-linux-x86_64-gaogaotiantian-optimize_sys_settrac-3.13.0a5+-a65be06.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 52.19% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x