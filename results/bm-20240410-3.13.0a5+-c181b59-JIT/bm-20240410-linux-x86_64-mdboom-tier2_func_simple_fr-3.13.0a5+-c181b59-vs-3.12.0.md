# Results vs. 3.12.0

- fork: mdboom
- ref: tier2_func_simple_fr
- machine: linux-x86_64
- commit hash: c181b59
- commit date: 2024-04-10
- overall geometric mean: 1.02x faster
- HPT reliability: 84.88%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 279 ms: 1.02x slower                                                   |
| chameleon      | 7.41 ms                                                | 7.06 ms: 1.05x faster                                                  |
| docutils       | 2.77 sec                                               | 2.92 sec: 1.06x slower                                                 |
| tornado_http   | 103 ms                                                 | 96.9 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 336 ms: 1.34x faster                                                   |
| async_tree_none            | 472 ms                                                 | 353 ms: 1.34x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 442 ms: 1.30x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 457 ms: 1.26x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 936 ms: 1.26x faster                                                   |
| async_tree_io              | 1.16 sec                                               | 923 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 606 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 613 ms: 1.18x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.27x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 78.0 ms: 1.09x faster                                                  |
| nbody          | 97.0 ms                                                | 91.4 ms: 1.06x faster                                                  |
| pidigits       | 187 ms                                                 | 189 ms: 1.01x slower                                                   |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 144 ms: 1.03x faster                                                   |
| regex_effbot   | 3.61 ms                                                | 3.59 ms: 1.01x faster                                                  |
| regex_dna      | 212 ms                                                 | 221 ms: 1.04x slower                                                   |
| regex_v8       | 23.1 ms                                                | 25.1 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.07 sec: 1.13x faster                                                 |
| unpickle             | 15.9 us                                                | 14.9 us: 1.06x faster                                                  |
| pickle_pure_python   | 324 us                                                 | 307 us: 1.05x faster                                                   |
| unpickle_list        | 5.29 us                                                | 5.15 us: 1.03x faster                                                  |
| pickle_list          | 5.08 us                                                | 5.01 us: 1.01x faster                                                  |
| pickle_dict          | 35.5 us                                                | 35.1 us: 1.01x faster                                                  |
| xml_etree_generate   | 89.2 ms                                                | 88.7 ms: 1.00x faster                                                  |
| json_loads           | 28.5 us                                                | 28.4 us: 1.00x faster                                                  |
| pickle               | 11.6 us                                                | 11.9 us: 1.03x slower                                                  |
| unpickle_pure_python | 230 us                                                 | 242 us: 1.05x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (4): xml_etree_process, json_dumps, xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 11.0 ms: 1.15x slower                                                  |
| python_startup_no_site | 6.94 ms                                                | 9.50 ms: 1.37x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.26x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|-----------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako      | 11.9 ms                                                | 10.7 ms: 1.11x faster                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 113 us: 1.39x faster                                                   |
| async_tree_none_tg         | 450 ms                                                 | 336 ms: 1.34x faster                                                   |
| async_tree_none            | 472 ms                                                 | 353 ms: 1.34x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 442 ms: 1.30x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 457 ms: 1.26x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 936 ms: 1.26x faster                                                   |
| async_tree_io              | 1.16 sec                                               | 923 ms: 1.25x faster                                                   |
| comprehensions             | 21.8 us                                                | 17.9 us: 1.22x faster                                                  |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 606 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 613 ms: 1.18x faster                                                   |
| logging_format             | 7.23 us                                                | 6.40 us: 1.13x faster                                                  |
| tomli_loads                | 2.33 sec                                               | 2.07 sec: 1.13x faster                                                 |
| raytrace                   | 312 ms                                                 | 278 ms: 1.12x faster                                                   |
| scimark_fft                | 382 ms                                                 | 342 ms: 1.12x faster                                                   |
| logging_simple             | 6.46 us                                                | 5.80 us: 1.11x faster                                                  |
| mako                       | 11.9 ms                                                | 10.7 ms: 1.11x faster                                                  |
| scimark_monte_carlo        | 75.1 ms                                                | 69.0 ms: 1.09x faster                                                  |
| float                      | 84.7 ms                                                | 78.0 ms: 1.09x faster                                                  |
| crypto_pyaes               | 81.9 ms                                                | 75.6 ms: 1.08x faster                                                  |
| chaos                      | 67.0 ms                                                | 62.6 ms: 1.07x faster                                                  |
| nbody                      | 97.0 ms                                                | 91.4 ms: 1.06x faster                                                  |
| unpickle                   | 15.9 us                                                | 14.9 us: 1.06x faster                                                  |
| deepcopy_memo              | 40.7 us                                                | 38.4 us: 1.06x faster                                                  |
| tornado_http               | 103 ms                                                 | 96.9 ms: 1.06x faster                                                  |
| pickle_pure_python         | 324 us                                                 | 307 us: 1.05x faster                                                   |
| chameleon                  | 7.41 ms                                                | 7.06 ms: 1.05x faster                                                  |
| richards                   | 45.8 ms                                                | 44.0 ms: 1.04x faster                                                  |
| fannkuch                   | 417 ms                                                 | 400 ms: 1.04x faster                                                   |
| deepcopy_reduce            | 3.35 us                                                | 3.21 us: 1.04x faster                                                  |
| pyflate                    | 482 ms                                                 | 464 ms: 1.04x faster                                                   |
| generators                 | 31.2 ms                                                | 30.2 ms: 1.03x faster                                                  |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 4.91 ms: 1.03x faster                                                  |
| regex_compile              | 148 ms                                                 | 144 ms: 1.03x faster                                                   |
| richards_super             | 51.5 ms                                                | 50.1 ms: 1.03x faster                                                  |
| unpickle_list              | 5.29 us                                                | 5.15 us: 1.03x faster                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.33 ms: 1.03x faster                                                  |
| sqlglot_transpile          | 1.68 ms                                                | 1.64 ms: 1.02x faster                                                  |
| logging_silent             | 104 ns                                                 | 102 ns: 1.02x faster                                                   |
| deepcopy                   | 371 us                                                 | 363 us: 1.02x faster                                                   |
| meteor_contest             | 112 ms                                                 | 110 ms: 1.02x faster                                                   |
| coroutines                 | 23.2 ms                                                | 22.8 ms: 1.02x faster                                                  |
| pickle_list                | 5.08 us                                                | 5.01 us: 1.01x faster                                                  |
| pickle_dict                | 35.5 us                                                | 35.1 us: 1.01x faster                                                  |
| sympy_str                  | 300 ms                                                 | 297 ms: 1.01x faster                                                   |
| regex_effbot               | 3.61 ms                                                | 3.59 ms: 1.01x faster                                                  |
| xml_etree_generate         | 89.2 ms                                                | 88.7 ms: 1.00x faster                                                  |
| sympy_sum                  | 169 ms                                                 | 168 ms: 1.00x faster                                                   |
| json_loads                 | 28.5 us                                                | 28.4 us: 1.00x faster                                                  |
| spectral_norm              | 115 ms                                                 | 116 ms: 1.01x slower                                                   |
| pidigits                   | 187 ms                                                 | 189 ms: 1.01x slower                                                   |
| sqlite_synth               | 2.83 us                                                | 2.87 us: 1.01x slower                                                  |
| 2to3                       | 274 ms                                                 | 279 ms: 1.02x slower                                                   |
| bench_thread_pool          | 842 us                                                 | 858 us: 1.02x slower                                                   |
| asyncio_websockets         | 551 ms                                                 | 567 ms: 1.03x slower                                                   |
| pickle                     | 11.6 us                                                | 11.9 us: 1.03x slower                                                  |
| dulwich_log                | 68.5 ms                                                | 70.6 ms: 1.03x slower                                                  |
| sympy_integrate            | 21.4 ms                                                | 22.1 ms: 1.03x slower                                                  |
| scimark_sor                | 129 ms                                                 | 134 ms: 1.04x slower                                                   |
| sympy_expand               | 478 ms                                                 | 497 ms: 1.04x slower                                                   |
| regex_dna                  | 212 ms                                                 | 221 ms: 1.04x slower                                                   |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                                 |
| gc_traversal               | 3.79 ms                                                | 3.96 ms: 1.04x slower                                                  |
| asyncio_tcp                | 491 ms                                                 | 512 ms: 1.04x slower                                                   |
| sqlglot_normalize          | 110 ms                                                 | 115 ms: 1.05x slower                                                   |
| gunicorn                   | 1.24 ms                                                | 1.30 ms: 1.05x slower                                                  |
| unpickle_pure_python       | 230 us                                                 | 242 us: 1.05x slower                                                   |
| aiohttp                    | 1.15 ms                                                | 1.21 ms: 1.05x slower                                                  |
| docutils                   | 2.77 sec                                               | 2.92 sec: 1.06x slower                                                 |
| sqlglot_optimize           | 54.8 ms                                                | 58.2 ms: 1.06x slower                                                  |
| mdp                        | 2.63 sec                                               | 2.82 sec: 1.07x slower                                                 |
| regex_v8                   | 23.1 ms                                                | 25.1 ms: 1.08x slower                                                  |
| nqueens                    | 83.3 ms                                                | 90.9 ms: 1.09x slower                                                  |
| hexiom                     | 6.41 ms                                                | 7.04 ms: 1.10x slower                                                  |
| go                         | 139 ms                                                 | 155 ms: 1.11x slower                                                   |
| scimark_lu                 | 118 ms                                                 | 134 ms: 1.13x slower                                                   |
| python_startup             | 9.55 ms                                                | 11.0 ms: 1.15x slower                                                  |
| create_gc_cycles           | 1.48 ms                                                | 1.76 ms: 1.19x slower                                                  |
| telco                      | 7.10 ms                                                | 8.79 ms: 1.24x slower                                                  |
| coverage                   | 72.7 ms                                                | 99.0 ms: 1.36x slower                                                  |
| python_startup_no_site     | 6.94 ms                                                | 9.50 ms: 1.37x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (14): mypy2, deltablue, pathlib, pprint_pformat, xml_etree_process, json_dumps, bench_mp_pool, pprint_safe_repr, async_generators, xml_etree_parse, xml_etree_iterparse, pycparser, json, dask
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240410-3.13.0a5+-c181b59-JIT/bm-20240410-linux-x86_64-mdboom-tier2_func_simple_fr-3.13.0a5+-c181b59.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 84.88% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.03x