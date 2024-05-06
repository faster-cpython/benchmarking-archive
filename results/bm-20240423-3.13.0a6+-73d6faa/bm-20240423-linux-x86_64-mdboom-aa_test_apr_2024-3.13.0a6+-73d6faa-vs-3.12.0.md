# Results vs. 3.12.0

- fork: mdboom
- ref: aa_test_apr_2024
- machine: linux-x86_64
- commit hash: 73d6faa
- commit date: 2024-04-23
- overall geometric mean: 1.04x faster
- HPT reliability: 99.92%
- HPT 99th percentile: 1.00x faster
- Memory change: 0.96x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 271 ms: 1.01x faster                                               |
| chameleon      | 7.41 ms                                                | 6.90 ms: 1.07x faster                                              |
| docutils       | 2.77 sec                                               | 2.81 sec: 1.02x slower                                             |
| tornado_http   | 103 ms                                                 | 94.1 ms: 1.09x faster                                              |
| Geometric mean | (ref)                                                  | 1.04x faster                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 334 ms: 1.35x faster                                               |
| async_tree_none            | 472 ms                                                 | 352 ms: 1.34x faster                                               |
| async_tree_memoization_tg  | 575 ms                                                 | 440 ms: 1.31x faster                                               |
| async_tree_io              | 1.16 sec                                               | 908 ms: 1.27x faster                                               |
| async_tree_memoization     | 578 ms                                                 | 461 ms: 1.25x faster                                               |
| async_tree_io_tg           | 1.18 sec                                               | 944 ms: 1.25x faster                                               |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 605 ms: 1.20x faster                                               |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 613 ms: 1.18x faster                                               |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                       |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 79.2 ms: 1.07x faster                                              |
| nbody          | 97.0 ms                                                | 95.5 ms: 1.02x faster                                              |
| pidigits       | 187 ms                                                 | 190 ms: 1.01x slower                                               |
| Geometric mean | (ref)                                                  | 1.02x faster                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 136 ms: 1.09x faster                                               |
| regex_effbot   | 3.61 ms                                                | 3.73 ms: 1.03x slower                                              |
| regex_dna      | 212 ms                                                 | 225 ms: 1.06x slower                                               |
| regex_v8       | 23.1 ms                                                | 25.8 ms: 1.11x slower                                              |
| Geometric mean | (ref)                                                  | 1.03x slower                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| pickle_pure_python   | 324 us                                                 | 306 us: 1.06x faster                                               |
| tomli_loads          | 2.33 sec                                               | 2.21 sec: 1.06x faster                                             |
| unpickle_pure_python | 230 us                                                 | 219 us: 1.05x faster                                               |
| unpickle_list        | 5.29 us                                                | 5.11 us: 1.03x faster                                              |
| json_loads           | 28.5 us                                                | 27.8 us: 1.02x faster                                              |
| xml_etree_process    | 61.7 ms                                                | 60.4 ms: 1.02x faster                                              |
| unpickle             | 15.9 us                                                | 15.6 us: 1.02x faster                                              |
| xml_etree_generate   | 89.2 ms                                                | 87.7 ms: 1.02x faster                                              |
| pickle_dict          | 35.5 us                                                | 35.3 us: 1.01x faster                                              |
| xml_etree_iterparse  | 107 ms                                                 | 108 ms: 1.01x slower                                               |
| json_dumps           | 10.4 ms                                                | 10.6 ms: 1.02x slower                                              |
| pickle               | 11.6 us                                                | 12.1 us: 1.04x slower                                              |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                       |

Benchmark hidden because not significant (2): xml_etree_parse, pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup_no_site | 6.94 ms                                                | 7.09 ms: 1.02x slower                                              |
| python_startup         | 9.55 ms                                                | 10.5 ms: 1.10x slower                                              |
| Geometric mean         | (ref)                                                  | 1.06x slower                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| mako            | 11.9 ms                                                | 10.9 ms: 1.09x faster                                              |
| django_template | 34.6 ms                                                | 35.0 ms: 1.01x slower                                              |
| Geometric mean  | (ref)                                                  | 1.04x faster                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 113 us: 1.39x faster                                               |
| async_tree_none_tg         | 450 ms                                                 | 334 ms: 1.35x faster                                               |
| async_tree_none            | 472 ms                                                 | 352 ms: 1.34x faster                                               |
| async_tree_memoization_tg  | 575 ms                                                 | 440 ms: 1.31x faster                                               |
| comprehensions             | 21.8 us                                                | 17.0 us: 1.28x faster                                              |
| async_tree_io              | 1.16 sec                                               | 908 ms: 1.27x faster                                               |
| async_tree_memoization     | 578 ms                                                 | 461 ms: 1.25x faster                                               |
| async_tree_io_tg           | 1.18 sec                                               | 944 ms: 1.25x faster                                               |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 605 ms: 1.20x faster                                               |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 613 ms: 1.18x faster                                               |
| raytrace                   | 312 ms                                                 | 264 ms: 1.18x faster                                               |
| deltablue                  | 3.72 ms                                                | 3.27 ms: 1.14x faster                                              |
| mypy2                      | 830 ms                                                 | 737 ms: 1.13x faster                                               |
| logging_format             | 7.23 us                                                | 6.49 us: 1.11x faster                                              |
| logging_simple             | 6.46 us                                                | 5.83 us: 1.11x faster                                              |
| pathlib                    | 19.3 ms                                                | 17.6 ms: 1.10x faster                                              |
| mako                       | 11.9 ms                                                | 10.9 ms: 1.09x faster                                              |
| regex_compile              | 148 ms                                                 | 136 ms: 1.09x faster                                               |
| tornado_http               | 103 ms                                                 | 94.1 ms: 1.09x faster                                              |
| crypto_pyaes               | 81.9 ms                                                | 75.1 ms: 1.09x faster                                              |
| chaos                      | 67.0 ms                                                | 61.8 ms: 1.08x faster                                              |
| sympy_sum                  | 169 ms                                                 | 157 ms: 1.08x faster                                               |
| chameleon                  | 7.41 ms                                                | 6.90 ms: 1.07x faster                                              |
| float                      | 84.7 ms                                                | 79.2 ms: 1.07x faster                                              |
| sympy_str                  | 300 ms                                                 | 281 ms: 1.07x faster                                               |
| scimark_monte_carlo        | 75.1 ms                                                | 70.6 ms: 1.06x faster                                              |
| pickle_pure_python         | 324 us                                                 | 306 us: 1.06x faster                                               |
| deepcopy_memo              | 40.7 us                                                | 38.5 us: 1.06x faster                                              |
| tomli_loads                | 2.33 sec                                               | 2.21 sec: 1.06x faster                                             |
| fannkuch                   | 417 ms                                                 | 396 ms: 1.05x faster                                               |
| sqlglot_transpile          | 1.68 ms                                                | 1.60 ms: 1.05x faster                                              |
| sympy_integrate            | 21.4 ms                                                | 20.4 ms: 1.05x faster                                              |
| sqlglot_parse              | 1.36 ms                                                | 1.29 ms: 1.05x faster                                              |
| unpickle_pure_python       | 230 us                                                 | 219 us: 1.05x faster                                               |
| deepcopy_reduce            | 3.35 us                                                | 3.19 us: 1.05x faster                                              |
| generators                 | 31.2 ms                                                | 29.8 ms: 1.05x faster                                              |
| async_generators           | 463 ms                                                 | 444 ms: 1.04x faster                                               |
| deepcopy                   | 371 us                                                 | 357 us: 1.04x faster                                               |
| scimark_sor                | 129 ms                                                 | 124 ms: 1.04x faster                                               |
| nqueens                    | 83.3 ms                                                | 80.5 ms: 1.03x faster                                              |
| unpickle_list              | 5.29 us                                                | 5.11 us: 1.03x faster                                              |
| pprint_safe_repr           | 776 ms                                                 | 752 ms: 1.03x faster                                               |
| pyflate                    | 482 ms                                                 | 469 ms: 1.03x faster                                               |
| dulwich_log                | 68.5 ms                                                | 66.8 ms: 1.03x faster                                              |
| json                       | 5.26 ms                                                | 5.13 ms: 1.03x faster                                              |
| json_loads                 | 28.5 us                                                | 27.8 us: 1.02x faster                                              |
| xml_etree_process          | 61.7 ms                                                | 60.4 ms: 1.02x faster                                              |
| pprint_pformat             | 1.57 sec                                               | 1.54 sec: 1.02x faster                                             |
| unpickle                   | 15.9 us                                                | 15.6 us: 1.02x faster                                              |
| coroutines                 | 23.2 ms                                                | 22.8 ms: 1.02x faster                                              |
| meteor_contest             | 112 ms                                                 | 111 ms: 1.02x faster                                               |
| xml_etree_generate         | 89.2 ms                                                | 87.7 ms: 1.02x faster                                              |
| nbody                      | 97.0 ms                                                | 95.5 ms: 1.02x faster                                              |
| 2to3                       | 274 ms                                                 | 271 ms: 1.01x faster                                               |
| mdp                        | 2.63 sec                                               | 2.60 sec: 1.01x faster                                             |
| bench_thread_pool          | 842 us                                                 | 833 us: 1.01x faster                                               |
| hexiom                     | 6.41 ms                                                | 6.35 ms: 1.01x faster                                              |
| pickle_dict                | 35.5 us                                                | 35.3 us: 1.01x faster                                              |
| sympy_expand               | 478 ms                                                 | 475 ms: 1.01x faster                                               |
| bench_mp_pool              | 24.0 ms                                                | 23.9 ms: 1.00x faster                                              |
| sqlglot_normalize          | 110 ms                                                 | 111 ms: 1.01x slower                                               |
| sqlglot_optimize           | 54.8 ms                                                | 55.2 ms: 1.01x slower                                              |
| scimark_lu                 | 118 ms                                                 | 119 ms: 1.01x slower                                               |
| xml_etree_iterparse        | 107 ms                                                 | 108 ms: 1.01x slower                                               |
| django_template            | 34.6 ms                                                | 35.0 ms: 1.01x slower                                              |
| pidigits                   | 187 ms                                                 | 190 ms: 1.01x slower                                               |
| docutils                   | 2.77 sec                                               | 2.81 sec: 1.02x slower                                             |
| aiohttp                    | 1.15 ms                                                | 1.17 ms: 1.02x slower                                              |
| pycparser                  | 1.18 sec                                               | 1.20 sec: 1.02x slower                                             |
| gc_traversal               | 3.79 ms                                                | 3.87 ms: 1.02x slower                                              |
| asyncio_websockets         | 551 ms                                                 | 563 ms: 1.02x slower                                               |
| gunicorn                   | 1.24 ms                                                | 1.27 ms: 1.02x slower                                              |
| python_startup_no_site     | 6.94 ms                                                | 7.09 ms: 1.02x slower                                              |
| json_dumps                 | 10.4 ms                                                | 10.6 ms: 1.02x slower                                              |
| asyncio_tcp                | 491 ms                                                 | 505 ms: 1.03x slower                                               |
| logging_silent             | 104 ns                                                 | 108 ns: 1.03x slower                                               |
| go                         | 139 ms                                                 | 144 ms: 1.03x slower                                               |
| regex_effbot               | 3.61 ms                                                | 3.73 ms: 1.03x slower                                              |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.85 sec: 1.03x slower                                             |
| sqlite_synth               | 2.83 us                                                | 2.95 us: 1.04x slower                                              |
| pickle                     | 11.6 us                                                | 12.1 us: 1.04x slower                                              |
| richards                   | 45.8 ms                                                | 48.2 ms: 1.05x slower                                              |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.33 ms: 1.05x slower                                              |
| richards_super             | 51.5 ms                                                | 54.4 ms: 1.06x slower                                              |
| regex_dna                  | 212 ms                                                 | 225 ms: 1.06x slower                                               |
| python_startup             | 9.55 ms                                                | 10.5 ms: 1.10x slower                                              |
| regex_v8                   | 23.1 ms                                                | 25.8 ms: 1.11x slower                                              |
| create_gc_cycles           | 1.48 ms                                                | 1.75 ms: 1.18x slower                                              |
| telco                      | 7.10 ms                                                | 8.78 ms: 1.24x slower                                              |
| coverage                   | 72.7 ms                                                | 98.3 ms: 1.35x slower                                              |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                       |

Benchmark hidden because not significant (5): dask, xml_etree_parse, pickle_list, scimark_fft, spectral_norm
Ignored benchmarks (3) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (6) of results/bm-20240423-3.13.0a6+-73d6faa/bm-20240423-linux-x86_64-mdboom-aa_test_apr_2024-3.13.0a6+-73d6faa.json: djangocms, genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 99.92% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 0.96x