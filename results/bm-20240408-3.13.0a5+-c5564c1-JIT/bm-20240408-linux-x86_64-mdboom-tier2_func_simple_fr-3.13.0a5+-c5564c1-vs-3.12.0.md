# Results vs. 3.12.0

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: linux-x86_64
- commit hash: c5564c1
- commit date: 2024-04-08
- overall geometric mean: 1.02x faster
- HPT reliability: 82.07%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 278 ms: 1.02x slower                                                   |
| chameleon      | 7.41 ms                                                | 7.12 ms: 1.04x faster                                                  |
| docutils       | 2.77 sec                                               | 2.94 sec: 1.06x slower                                                 |
| tornado_http   | 103 ms                                                 | 96.7 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 337 ms: 1.33x faster                                                   |
| async_tree_none            | 472 ms                                                 | 357 ms: 1.32x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 445 ms: 1.29x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 949 ms: 1.25x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 464 ms: 1.25x faster                                                   |
| async_tree_io              | 1.16 sec                                               | 956 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 609 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 615 ms: 1.18x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.25x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 78.4 ms: 1.08x faster                                                  |
| nbody          | 97.0 ms                                                | 90.9 ms: 1.07x faster                                                  |
| pidigits       | 187 ms                                                 | 211 ms: 1.13x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 145 ms: 1.02x faster                                                   |
| regex_effbot   | 3.61 ms                                                | 3.80 ms: 1.05x slower                                                  |
| regex_dna      | 212 ms                                                 | 230 ms: 1.08x slower                                                   |
| regex_v8       | 23.1 ms                                                | 26.0 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.06x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.07 sec: 1.13x faster                                                 |
| unpickle             | 15.9 us                                                | 15.0 us: 1.06x faster                                                  |
| pickle_pure_python   | 324 us                                                 | 309 us: 1.05x faster                                                   |
| xml_etree_process    | 61.7 ms                                                | 60.2 ms: 1.03x faster                                                  |
| xml_etree_generate   | 89.2 ms                                                | 87.7 ms: 1.02x faster                                                  |
| json_loads           | 28.5 us                                                | 28.2 us: 1.01x faster                                                  |
| pickle_dict          | 35.5 us                                                | 35.4 us: 1.00x faster                                                  |
| unpickle_list        | 5.29 us                                                | 5.32 us: 1.01x slower                                                  |
| pickle               | 11.6 us                                                | 11.8 us: 1.02x slower                                                  |
| pickle_list          | 5.08 us                                                | 5.28 us: 1.04x slower                                                  |
| unpickle_pure_python | 230 us                                                 | 240 us: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (3): json_dumps, xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 11.0 ms: 1.15x slower                                                  |
| python_startup_no_site | 6.94 ms                                                | 9.51 ms: 1.37x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.26x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|-----------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako      | 11.9 ms                                                | 10.8 ms: 1.10x faster                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 113 us: 1.39x faster                                                   |
| async_tree_none_tg         | 450 ms                                                 | 337 ms: 1.33x faster                                                   |
| async_tree_none            | 472 ms                                                 | 357 ms: 1.32x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 445 ms: 1.29x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 949 ms: 1.25x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 464 ms: 1.25x faster                                                   |
| comprehensions             | 21.8 us                                                | 17.9 us: 1.21x faster                                                  |
| async_tree_io              | 1.16 sec                                               | 956 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 609 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 615 ms: 1.18x faster                                                   |
| raytrace                   | 312 ms                                                 | 274 ms: 1.14x faster                                                   |
| tomli_loads                | 2.33 sec                                               | 2.07 sec: 1.13x faster                                                 |
| logging_format             | 7.23 us                                                | 6.51 us: 1.11x faster                                                  |
| logging_simple             | 6.46 us                                                | 5.84 us: 1.11x faster                                                  |
| mako                       | 11.9 ms                                                | 10.8 ms: 1.10x faster                                                  |
| scimark_fft                | 382 ms                                                 | 349 ms: 1.09x faster                                                   |
| scimark_monte_carlo        | 75.1 ms                                                | 68.9 ms: 1.09x faster                                                  |
| crypto_pyaes               | 81.9 ms                                                | 75.6 ms: 1.08x faster                                                  |
| float                      | 84.7 ms                                                | 78.4 ms: 1.08x faster                                                  |
| chaos                      | 67.0 ms                                                | 62.2 ms: 1.08x faster                                                  |
| nbody                      | 97.0 ms                                                | 90.9 ms: 1.07x faster                                                  |
| tornado_http               | 103 ms                                                 | 96.7 ms: 1.06x faster                                                  |
| unpickle                   | 15.9 us                                                | 15.0 us: 1.06x faster                                                  |
| deepcopy_memo              | 40.7 us                                                | 38.5 us: 1.06x faster                                                  |
| fannkuch                   | 417 ms                                                 | 397 ms: 1.05x faster                                                   |
| pickle_pure_python         | 324 us                                                 | 309 us: 1.05x faster                                                   |
| generators                 | 31.2 ms                                                | 29.8 ms: 1.05x faster                                                  |
| coroutines                 | 23.2 ms                                                | 22.1 ms: 1.05x faster                                                  |
| chameleon                  | 7.41 ms                                                | 7.12 ms: 1.04x faster                                                  |
| richards                   | 45.8 ms                                                | 44.1 ms: 1.04x faster                                                  |
| richards_super             | 51.5 ms                                                | 49.8 ms: 1.03x faster                                                  |
| deepcopy_reduce            | 3.35 us                                                | 3.25 us: 1.03x faster                                                  |
| xml_etree_process          | 61.7 ms                                                | 60.2 ms: 1.03x faster                                                  |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.93 ms: 1.03x faster                                                  |
| pyflate                    | 482 ms                                                 | 471 ms: 1.03x faster                                                   |
| deepcopy                   | 371 us                                                 | 362 us: 1.02x faster                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.33 ms: 1.02x faster                                                  |
| regex_compile              | 148 ms                                                 | 145 ms: 1.02x faster                                                   |
| sqlglot_transpile          | 1.68 ms                                                | 1.65 ms: 1.02x faster                                                  |
| pprint_safe_repr           | 776 ms                                                 | 762 ms: 1.02x faster                                                   |
| xml_etree_generate         | 89.2 ms                                                | 87.7 ms: 1.02x faster                                                  |
| logging_silent             | 104 ns                                                 | 103 ns: 1.01x faster                                                   |
| json_loads                 | 28.5 us                                                | 28.2 us: 1.01x faster                                                  |
| pathlib                    | 19.3 ms                                                | 19.1 ms: 1.01x faster                                                  |
| async_generators           | 463 ms                                                 | 459 ms: 1.01x faster                                                   |
| sympy_str                  | 300 ms                                                 | 298 ms: 1.01x faster                                                   |
| pickle_dict                | 35.5 us                                                | 35.4 us: 1.00x faster                                                  |
| sympy_sum                  | 169 ms                                                 | 168 ms: 1.00x faster                                                   |
| meteor_contest             | 112 ms                                                 | 113 ms: 1.00x slower                                                   |
| unpickle_list              | 5.29 us                                                | 5.32 us: 1.01x slower                                                  |
| dask                       | 372 ms                                                 | 376 ms: 1.01x slower                                                   |
| 2to3                       | 274 ms                                                 | 278 ms: 1.02x slower                                                   |
| bench_thread_pool          | 842 us                                                 | 856 us: 1.02x slower                                                   |
| sqlite_synth               | 2.83 us                                                | 2.89 us: 1.02x slower                                                  |
| pickle                     | 11.6 us                                                | 11.8 us: 1.02x slower                                                  |
| asyncio_tcp                | 491 ms                                                 | 501 ms: 1.02x slower                                                   |
| gc_traversal               | 3.79 ms                                                | 3.88 ms: 1.02x slower                                                  |
| dulwich_log                | 68.5 ms                                                | 70.2 ms: 1.03x slower                                                  |
| asyncio_websockets         | 551 ms                                                 | 567 ms: 1.03x slower                                                   |
| sqlglot_normalize          | 110 ms                                                 | 114 ms: 1.03x slower                                                   |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.85 sec: 1.04x slower                                                 |
| sympy_integrate            | 21.4 ms                                                | 22.2 ms: 1.04x slower                                                  |
| pickle_list                | 5.08 us                                                | 5.28 us: 1.04x slower                                                  |
| scimark_sor                | 129 ms                                                 | 134 ms: 1.04x slower                                                   |
| pycparser                  | 1.18 sec                                               | 1.23 sec: 1.04x slower                                                 |
| sympy_expand               | 478 ms                                                 | 498 ms: 1.04x slower                                                   |
| unpickle_pure_python       | 230 us                                                 | 240 us: 1.05x slower                                                   |
| sqlglot_optimize           | 54.8 ms                                                | 57.4 ms: 1.05x slower                                                  |
| gunicorn                   | 1.24 ms                                                | 1.30 ms: 1.05x slower                                                  |
| regex_effbot               | 3.61 ms                                                | 3.80 ms: 1.05x slower                                                  |
| aiohttp                    | 1.15 ms                                                | 1.21 ms: 1.05x slower                                                  |
| docutils                   | 2.77 sec                                               | 2.94 sec: 1.06x slower                                                 |
| mdp                        | 2.63 sec                                               | 2.83 sec: 1.08x slower                                                 |
| regex_dna                  | 212 ms                                                 | 230 ms: 1.08x slower                                                   |
| nqueens                    | 83.3 ms                                                | 90.9 ms: 1.09x slower                                                  |
| hexiom                     | 6.41 ms                                                | 7.04 ms: 1.10x slower                                                  |
| go                         | 139 ms                                                 | 157 ms: 1.12x slower                                                   |
| regex_v8                   | 23.1 ms                                                | 26.0 ms: 1.12x slower                                                  |
| pidigits                   | 187 ms                                                 | 211 ms: 1.13x slower                                                   |
| scimark_lu                 | 118 ms                                                 | 134 ms: 1.13x slower                                                   |
| python_startup             | 9.55 ms                                                | 11.0 ms: 1.15x slower                                                  |
| create_gc_cycles           | 1.48 ms                                                | 1.76 ms: 1.19x slower                                                  |
| telco                      | 7.10 ms                                                | 8.68 ms: 1.22x slower                                                  |
| coverage                   | 72.7 ms                                                | 98.3 ms: 1.35x slower                                                  |
| python_startup_no_site     | 6.94 ms                                                | 9.51 ms: 1.37x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (9): mypy2, deltablue, bench_mp_pool, spectral_norm, json_dumps, xml_etree_iterparse, xml_etree_parse, json, pprint_pformat
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240408-3.13.0a5+-c5564c1-JIT/bm-20240408-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c5564c1.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 82.07% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x