# Results vs. 3.12.0

- fork: python
- ref: 027fa2eccf39ddccdf7b
- machine: linux-x86_64
- commit hash: 027fa2e
- commit date: 2024-04-02
- overall geometric mean: 1.02x faster
- HPT reliability: 92.16%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.04x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 274 ms                                                 | 277 ms: 1.01x slower                                                   |
| chameleon      | 7.41 ms                                                | 6.86 ms: 1.08x faster                                                  |
| docutils       | 2.77 sec                                               | 2.90 sec: 1.05x slower                                                 |
| tornado_http   | 103 ms                                                 | 96.1 ms: 1.07x faster                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_none_tg         | 450 ms                                                 | 338 ms: 1.33x faster                                                   |
| async_tree_none            | 472 ms                                                 | 355 ms: 1.33x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 443 ms: 1.30x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 454 ms: 1.27x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 952 ms: 1.24x faster                                                   |
| async_tree_io              | 1.16 sec                                               | 933 ms: 1.24x faster                                                   |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 609 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 617 ms: 1.18x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.26x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 84.7 ms                                                | 76.2 ms: 1.11x faster                                                  |
| nbody          | 97.0 ms                                                | 91.7 ms: 1.06x faster                                                  |
| pidigits       | 187 ms                                                 | 202 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 148 ms                                                 | 146 ms: 1.02x faster                                                   |
| regex_effbot   | 3.61 ms                                                | 3.60 ms: 1.00x faster                                                  |
| regex_dna      | 212 ms                                                 | 220 ms: 1.04x slower                                                   |
| regex_v8       | 23.1 ms                                                | 25.0 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.33 sec                                               | 2.07 sec: 1.13x faster                                                 |
| unpickle             | 15.9 us                                                | 14.8 us: 1.07x faster                                                  |
| pickle_pure_python   | 324 us                                                 | 305 us: 1.06x faster                                                   |
| pickle_dict          | 35.5 us                                                | 34.0 us: 1.05x faster                                                  |
| xml_etree_process    | 61.7 ms                                                | 59.7 ms: 1.03x faster                                                  |
| xml_etree_generate   | 89.2 ms                                                | 86.7 ms: 1.03x faster                                                  |
| unpickle_list        | 5.29 us                                                | 5.18 us: 1.02x faster                                                  |
| pickle_list          | 5.08 us                                                | 5.02 us: 1.01x faster                                                  |
| json_loads           | 28.5 us                                                | 28.8 us: 1.01x slower                                                  |
| unpickle_pure_python | 230 us                                                 | 236 us: 1.03x slower                                                   |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                  |
| pickle               | 11.6 us                                                | 12.0 us: 1.04x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 9.55 ms                                                | 11.0 ms: 1.16x slower                                                  |
| python_startup_no_site | 6.94 ms                                                | 9.49 ms: 1.37x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.26x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|-----------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako      | 11.9 ms                                                | 10.9 ms: 1.09x faster                                                  |

All benchmarks:
===============

| Benchmark                  | bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0 | bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| typing_runtime_protocols   | 158 us                                                 | 111 us: 1.42x faster                                                   |
| async_tree_none_tg         | 450 ms                                                 | 338 ms: 1.33x faster                                                   |
| async_tree_none            | 472 ms                                                 | 355 ms: 1.33x faster                                                   |
| async_tree_memoization_tg  | 575 ms                                                 | 443 ms: 1.30x faster                                                   |
| async_tree_memoization     | 578 ms                                                 | 454 ms: 1.27x faster                                                   |
| async_tree_io_tg           | 1.18 sec                                               | 952 ms: 1.24x faster                                                   |
| async_tree_io              | 1.16 sec                                               | 933 ms: 1.24x faster                                                   |
| comprehensions             | 21.8 us                                                | 17.9 us: 1.22x faster                                                  |
| async_tree_cpu_io_mixed_tg | 726 ms                                                 | 609 ms: 1.19x faster                                                   |
| async_tree_cpu_io_mixed    | 726 ms                                                 | 617 ms: 1.18x faster                                                   |
| tomli_loads                | 2.33 sec                                               | 2.07 sec: 1.13x faster                                                 |
| raytrace                   | 312 ms                                                 | 280 ms: 1.11x faster                                                   |
| float                      | 84.7 ms                                                | 76.2 ms: 1.11x faster                                                  |
| scimark_fft                | 382 ms                                                 | 346 ms: 1.11x faster                                                   |
| logging_format             | 7.23 us                                                | 6.61 us: 1.09x faster                                                  |
| crypto_pyaes               | 81.9 ms                                                | 74.9 ms: 1.09x faster                                                  |
| mako                       | 11.9 ms                                                | 10.9 ms: 1.09x faster                                                  |
| deltablue                  | 3.72 ms                                                | 3.42 ms: 1.09x faster                                                  |
| scimark_monte_carlo        | 75.1 ms                                                | 69.3 ms: 1.08x faster                                                  |
| chameleon                  | 7.41 ms                                                | 6.86 ms: 1.08x faster                                                  |
| logging_simple             | 6.46 us                                                | 5.98 us: 1.08x faster                                                  |
| chaos                      | 67.0 ms                                                | 62.1 ms: 1.08x faster                                                  |
| unpickle                   | 15.9 us                                                | 14.8 us: 1.07x faster                                                  |
| tornado_http               | 103 ms                                                 | 96.1 ms: 1.07x faster                                                  |
| logging_silent             | 104 ns                                                 | 97.9 ns: 1.07x faster                                                  |
| pickle_pure_python         | 324 us                                                 | 305 us: 1.06x faster                                                   |
| pprint_safe_repr           | 776 ms                                                 | 733 ms: 1.06x faster                                                   |
| nbody                      | 97.0 ms                                                | 91.7 ms: 1.06x faster                                                  |
| deepcopy_memo              | 40.7 us                                                | 38.5 us: 1.06x faster                                                  |
| generators                 | 31.2 ms                                                | 29.7 ms: 1.05x faster                                                  |
| fannkuch                   | 417 ms                                                 | 398 ms: 1.05x faster                                                   |
| pickle_dict                | 35.5 us                                                | 34.0 us: 1.05x faster                                                  |
| coroutines                 | 23.2 ms                                                | 22.2 ms: 1.04x faster                                                  |
| deepcopy_reduce            | 3.35 us                                                | 3.23 us: 1.04x faster                                                  |
| pprint_pformat             | 1.57 sec                                               | 1.51 sec: 1.04x faster                                                 |
| xml_etree_process          | 61.7 ms                                                | 59.7 ms: 1.03x faster                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.32 ms: 1.03x faster                                                  |
| pyflate                    | 482 ms                                                 | 469 ms: 1.03x faster                                                   |
| xml_etree_generate         | 89.2 ms                                                | 86.7 ms: 1.03x faster                                                  |
| sqlglot_transpile          | 1.68 ms                                                | 1.64 ms: 1.03x faster                                                  |
| unpickle_list              | 5.29 us                                                | 5.18 us: 1.02x faster                                                  |
| pycparser                  | 1.18 sec                                               | 1.16 sec: 1.02x faster                                                 |
| deepcopy                   | 371 us                                                 | 364 us: 1.02x faster                                                   |
| sympy_str                  | 300 ms                                                 | 294 ms: 1.02x faster                                                   |
| regex_compile              | 148 ms                                                 | 146 ms: 1.02x faster                                                   |
| pathlib                    | 19.3 ms                                                | 19.1 ms: 1.01x faster                                                  |
| meteor_contest             | 112 ms                                                 | 111 ms: 1.01x faster                                                   |
| pickle_list                | 5.08 us                                                | 5.02 us: 1.01x faster                                                  |
| sympy_sum                  | 169 ms                                                 | 167 ms: 1.01x faster                                                   |
| scimark_sparse_mat_mult    | 5.06 ms                                                | 5.02 ms: 1.01x faster                                                  |
| async_generators           | 463 ms                                                 | 460 ms: 1.01x faster                                                   |
| regex_effbot               | 3.61 ms                                                | 3.60 ms: 1.00x faster                                                  |
| sqlite_synth               | 2.83 us                                                | 2.85 us: 1.01x slower                                                  |
| json_loads                 | 28.5 us                                                | 28.8 us: 1.01x slower                                                  |
| 2to3                       | 274 ms                                                 | 277 ms: 1.01x slower                                                   |
| richards_super             | 51.5 ms                                                | 52.2 ms: 1.01x slower                                                  |
| bench_thread_pool          | 842 us                                                 | 859 us: 1.02x slower                                                   |
| asyncio_websockets         | 551 ms                                                 | 564 ms: 1.02x slower                                                   |
| sympy_integrate            | 21.4 ms                                                | 22.0 ms: 1.03x slower                                                  |
| unpickle_pure_python       | 230 us                                                 | 236 us: 1.03x slower                                                   |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.03x slower                                                  |
| sympy_expand               | 478 ms                                                 | 494 ms: 1.03x slower                                                   |
| json                       | 5.26 ms                                                | 5.44 ms: 1.03x slower                                                  |
| sqlglot_normalize          | 110 ms                                                 | 114 ms: 1.03x slower                                                   |
| pickle                     | 11.6 us                                                | 12.0 us: 1.04x slower                                                  |
| dulwich_log                | 68.5 ms                                                | 71.2 ms: 1.04x slower                                                  |
| regex_dna                  | 212 ms                                                 | 220 ms: 1.04x slower                                                   |
| asyncio_tcp_ssl            | 1.79 sec                                               | 1.86 sec: 1.04x slower                                                 |
| gunicorn                   | 1.24 ms                                                | 1.30 ms: 1.05x slower                                                  |
| scimark_sor                | 129 ms                                                 | 135 ms: 1.05x slower                                                   |
| docutils                   | 2.77 sec                                               | 2.90 sec: 1.05x slower                                                 |
| aiohttp                    | 1.15 ms                                                | 1.21 ms: 1.05x slower                                                  |
| sqlglot_optimize           | 54.8 ms                                                | 58.0 ms: 1.06x slower                                                  |
| asyncio_tcp                | 491 ms                                                 | 520 ms: 1.06x slower                                                   |
| pidigits                   | 187 ms                                                 | 202 ms: 1.08x slower                                                   |
| regex_v8                   | 23.1 ms                                                | 25.0 ms: 1.08x slower                                                  |
| go                         | 139 ms                                                 | 153 ms: 1.10x slower                                                   |
| nqueens                    | 83.3 ms                                                | 91.4 ms: 1.10x slower                                                  |
| hexiom                     | 6.41 ms                                                | 7.08 ms: 1.10x slower                                                  |
| scimark_lu                 | 118 ms                                                 | 132 ms: 1.12x slower                                                   |
| python_startup             | 9.55 ms                                                | 11.0 ms: 1.16x slower                                                  |
| create_gc_cycles           | 1.48 ms                                                | 1.76 ms: 1.19x slower                                                  |
| telco                      | 7.10 ms                                                | 8.51 ms: 1.20x slower                                                  |
| coverage                   | 72.7 ms                                                | 98.1 ms: 1.35x slower                                                  |
| python_startup_no_site     | 6.94 ms                                                | 9.49 ms: 1.37x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (9): mypy2, xml_etree_iterparse, bench_mp_pool, xml_etree_parse, gc_traversal, spectral_norm, mdp, richards, dask
Ignored benchmarks (4) of results/bm-20231002-3.12.0-0fb18b0/bm-20231002-linux-x86_64-python-v3.12.0-3.12.0-0fb18b0.json: django_template, sqlalchemy_declarative, sqlalchemy_imperative, unpack_sequence
Ignored benchmarks (5) of results/bm-20240402-3.13.0a5+-027fa2e-JIT/bm-20240402-linux-x86_64-python-027fa2eccf39ddccdf7b-3.13.0a5+-027fa2e.json: genshi_text, genshi_xml, html5lib, pylint, thrift

# HPT report

- Reliability score: 92.16% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.04x