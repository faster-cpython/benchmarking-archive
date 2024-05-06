# Results vs. 3.12.0

- fork: man-group
- ref: io_flush_full_buffer
- machine: linux-x86_64
- commit hash: 9cf294a
- commit date: 2024-03-26
- overall geometric mean: 1.02x faster
- HPT reliability: 78.11%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 278 ms: 1.01x slower                                                        |
| chameleon      | 7.41 ms                                                | 6.93 ms: 1.07x faster                                                       |
| docutils       | 2.77 sec                                               | 2.87 sec: 1.04x slower                                                      |
| tornado_http   | 103 ms                                                 | 96.4 ms: 1.06x faster                                                       |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 575 ms                                                 | 443 ms: 1.30x faster                                                        |
| async_tree_io_tg           | 1.18 sec                                               | 919 ms: 1.29x faster                                                        |
| async_tree_none_tg         | 450 ms                                                 | 351 ms: 1.28x faster                                                        |
| async_tree_none            | 472 ms                                                 | 374 ms: 1.26x faster                                                        |
| async_tree_io              | 1.16 sec                                               | 919 ms: 1.26x faster                                                        |
| async_tree_memoization     | 578 ms                                                 | 462 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 594 ms: 1.22x faster                                                        |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 605 ms: 1.20x faster                                                        |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                                |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 77.5 ms: 1.09x faster                                                       |
| nbody          | 97.0 ms                                                | 93.8 ms: 1.03x faster                                                       |
| pidigits       | 187 ms                                                 | 189 ms: 1.01x slower                                                        |
| Geometric mean | (ref)                                                  | 1.04x faster                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 146 ms: 1.02x faster                                                        |
| regex_effbot   | 3.61 ms                                                | 3.69 ms: 1.02x slower                                                       |
| regex_dna      | 212 ms                                                 | 230 ms: 1.08x slower                                                        |
| regex_v8       | 23.1 ms                                                | 26.2 ms: 1.13x slower                                                       |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.09 sec: 1.11x faster                                                      |
| pickle_dict          | 35.5 us                                                | 33.5 us: 1.06x faster                                                       |
| pickle_pure_python   | 324 us                                                 | 309 us: 1.05x faster                                                        |
| unpickle             | 15.9 us                                                | 15.2 us: 1.05x faster                                                       |
| unpickle_list        | 5.29 us                                                | 5.11 us: 1.03x faster                                                       |
| xml_etree_generate   | 89.2 ms                                                | 86.7 ms: 1.03x faster                                                       |
| pickle_list          | 5.08 us                                                | 5.02 us: 1.01x faster                                                       |
| xml_etree_process    | 61.7 ms                                                | 61.0 ms: 1.01x faster                                                       |
| json_loads           | 28.5 us                                                | 28.3 us: 1.01x faster                                                       |
| pickle               | 11.6 us                                                | 11.8 us: 1.02x slower                                                       |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                       |
| unpickle_pure_python | 230 us                                                 | 243 us: 1.05x slower                                                        |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                                |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 11.0 ms: 1.16x slower                                                       |
| python_startup_no_site | 6.94 ms                                                | 9.50 ms: 1.37x slower                                                       |
| Geometric mean         | (ref)                                                  | 1.26x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.7 ms: 1.11x faster                                                       |
| django_template | 34.6 ms                                                | 36.3 ms: 1.05x slower                                                       |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 113 us: 1.39x faster                                                        |
| async_tree_memoization_tg  | 575 ms                                                 | 443 ms: 1.30x faster                                                        |
| async_tree_io_tg           | 1.18 sec                                               | 919 ms: 1.29x faster                                                        |
| async_tree_none_tg         | 450 ms                                                 | 351 ms: 1.28x faster                                                        |
| async_tree_none            | 472 ms                                                 | 374 ms: 1.26x faster                                                        |
| async_tree_io              | 1.16 sec                                               | 919 ms: 1.26x faster                                                        |
| async_tree_memoization     | 578 ms                                                 | 462 ms: 1.25x faster                                                        |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 594 ms: 1.22x faster                                                        |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 605 ms: 1.20x faster                                                        |
| comprehensions             | 21.8 us                                                | 18.2 us: 1.19x faster                                                       |
| tomli_loads                | 2.33 sec                                               | 2.09 sec: 1.11x faster                                                      |
| mako                       | 11.9 ms                                                | 10.7 ms: 1.11x faster                                                       |
| scimark_fft                | 382 ms                                                 | 347 ms: 1.10x faster                                                        |
| crypto_pyaes               | 81.9 ms                                                | 74.6 ms: 1.10x faster                                                       |
| float                      | 84.7 ms                                                | 77.5 ms: 1.09x faster                                                       |
| logging_format             | 7.23 us                                                | 6.62 us: 1.09x faster                                                       |
| logging_simple             | 6.46 us                                                | 6.00 us: 1.08x faster                                                       |
| deltablue                  | 3.72 ms                                                | 3.47 ms: 1.07x faster                                                       |
| chameleon                  | 7.41 ms                                                | 6.93 ms: 1.07x faster                                                       |
| tornado_http               | 103 ms                                                 | 96.4 ms: 1.06x faster                                                       |
| raytrace                   | 312 ms                                                 | 293 ms: 1.06x faster                                                        |
| pickle_dict                | 35.5 us                                                | 33.5 us: 1.06x faster                                                       |
| deepcopy_reduce            | 3.35 us                                                | 3.17 us: 1.05x faster                                                       |
| scimark_monte_carlo        | 75.1 ms                                                | 71.4 ms: 1.05x faster                                                       |
| fannkuch                   | 417 ms                                                 | 397 ms: 1.05x faster                                                        |
| pickle_pure_python         | 324 us                                                 | 309 us: 1.05x faster                                                        |
| unpickle                   | 15.9 us                                                | 15.2 us: 1.05x faster                                                       |
| generators                 | 31.2 ms                                                | 30.0 ms: 1.04x faster                                                       |
| pprint_safe_repr           | 776 ms                                                 | 748 ms: 1.04x faster                                                        |
| chaos                      | 67.0 ms                                                | 64.6 ms: 1.04x faster                                                       |
| nbody                      | 97.0 ms                                                | 93.8 ms: 1.03x faster                                                       |
| unpickle_list              | 5.29 us                                                | 5.11 us: 1.03x faster                                                       |
| coroutines                 | 23.2 ms                                                | 22.5 ms: 1.03x faster                                                       |
| xml_etree_generate         | 89.2 ms                                                | 86.7 ms: 1.03x faster                                                       |
| sympy_str                  | 300 ms                                                 | 292 ms: 1.03x faster                                                        |
| sympy_sum                  | 169 ms                                                 | 165 ms: 1.03x faster                                                        |
| pathlib                    | 19.3 ms                                                | 18.9 ms: 1.02x faster                                                       |
| deepcopy_memo              | 40.7 us                                                | 39.8 us: 1.02x faster                                                       |
| pprint_pformat             | 1.57 sec                                               | 1.53 sec: 1.02x faster                                                      |
| logging_silent             | 104 ns                                                 | 102 ns: 1.02x faster                                                        |
| deepcopy                   | 371 us                                                 | 364 us: 1.02x faster                                                        |
| regex_compile              | 148 ms                                                 | 146 ms: 1.02x faster                                                        |
| meteor_contest             | 112 ms                                                 | 111 ms: 1.02x faster                                                        |
| sqlglot_transpile          | 1.68 ms                                                | 1.66 ms: 1.02x faster                                                       |
| sqlglot_parse              | 1.36 ms                                                | 1.34 ms: 1.01x faster                                                       |
| pickle_list                | 5.08 us                                                | 5.02 us: 1.01x faster                                                       |
| xml_etree_process          | 61.7 ms                                                | 61.0 ms: 1.01x faster                                                       |
| json_loads                 | 28.5 us                                                | 28.3 us: 1.01x faster                                                       |
| spectral_norm              | 115 ms                                                 | 114 ms: 1.01x faster                                                        |
| pyflate                    | 482 ms                                                 | 480 ms: 1.01x faster                                                        |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.04 ms: 1.00x faster                                                       |
| mdp                        | 2.63 sec                                               | 2.65 sec: 1.01x slower                                                      |
| pidigits                   | 187 ms                                                 | 189 ms: 1.01x slower                                                        |
| richards                   | 45.8 ms                                                | 46.4 ms: 1.01x slower                                                       |
| sqlite_synth               | 2.83 us                                                | 2.87 us: 1.01x slower                                                       |
| richards_super             | 51.5 ms                                                | 52.3 ms: 1.01x slower                                                       |
| 2to3                       | 274 ms                                                 | 278 ms: 1.01x slower                                                        |
| sympy_integrate            | 21.4 ms                                                | 21.8 ms: 1.02x slower                                                       |
| pickle                     | 11.6 us                                                | 11.8 us: 1.02x slower                                                       |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                                       |
| bench_thread_pool          | 842 us                                                 | 858 us: 1.02x slower                                                        |
| sqlglot_normalize          | 110 ms                                                 | 113 ms: 1.02x slower                                                        |
| regex_effbot               | 3.61 ms                                                | 3.69 ms: 1.02x slower                                                       |
| asyncio_tcp                | 491 ms                                                 | 504 ms: 1.03x slower                                                        |
| dulwich_log                | 68.5 ms                                                | 70.6 ms: 1.03x slower                                                       |
| sympy_expand               | 478 ms                                                 | 494 ms: 1.03x slower                                                        |
| asyncio_websockets         | 551 ms                                                 | 570 ms: 1.03x slower                                                        |
| scimark_sor                | 129 ms                                                 | 133 ms: 1.03x slower                                                        |
| docutils                   | 2.77 sec                                               | 2.87 sec: 1.04x slower                                                      |
| gc_traversal               | 3.79 ms                                                | 3.94 ms: 1.04x slower                                                       |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                                      |
| pycparser                  | 1.18 sec                                               | 1.23 sec: 1.05x slower                                                      |
| django_template            | 34.6 ms                                                | 36.3 ms: 1.05x slower                                                       |
| gunicorn                   | 1.24 ms                                                | 1.31 ms: 1.05x slower                                                       |
| unpickle_pure_python       | 230 us                                                 | 243 us: 1.05x slower                                                        |
| sqlglot_optimize           | 54.8 ms                                                | 57.9 ms: 1.06x slower                                                       |
| aiohttp                    | 1.15 ms                                                | 1.22 ms: 1.06x slower                                                       |
| regex_dna                  | 212 ms                                                 | 230 ms: 1.08x slower                                                        |
| nqueens                    | 83.3 ms                                                | 90.4 ms: 1.09x slower                                                       |
| go                         | 139 ms                                                 | 156 ms: 1.12x slower                                                        |
| hexiom                     | 6.41 ms                                                | 7.20 ms: 1.12x slower                                                       |
| scimark_lu                 | 118 ms                                                 | 133 ms: 1.13x slower                                                        |
| regex_v8                   | 23.1 ms                                                | 26.2 ms: 1.13x slower                                                       |
| create_gc_cycles           | 1.48 ms                                                | 1.69 ms: 1.15x slower                                                       |
| python_startup             | 9.55 ms                                                | 11.0 ms: 1.16x slower                                                       |
| telco                      | 7.10 ms                                                | 8.59 ms: 1.21x slower                                                       |
| coverage                   | 72.7 ms                                                | 98.7 ms: 1.36x slower                                                       |
| python_startup_no_site     | 6.94 ms                                                | 9.50 ms: 1.37x slower                                                       |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                                |

Benchmark hidden because not significant (7): mypy2, async_generators, xml_etree_iterparse, bench_mp_pool, xml_etree_parse, json, dask
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240326-3.13.0a5+-9cf294a-JIT/bm-20240326-linux-x86_64-man%2dgroup-io_flush_full_buffer-3.13.0a5+-9cf294a.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 78.11% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x